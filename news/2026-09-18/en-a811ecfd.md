---
title: "ZCode uploads your entire .git before every single prompt"
date: 2026-09-18
lang: en
source: https://clauday.com/article/a811ecfd-0075-4572-ae4e-9704fbfe7323
tags: [Agents, Coding, Infrastructure]
---

# ZCode uploads your entire .git before every single prompt

> 来源 / Source: https://clauday.com/article/a811ecfd-0075-4572-ae4e-9704fbfe7323

Z.ai's ZCode desktop app takes a snapshot of your workspace and ships it to Alibaba Cloud object storage. Not on crash. Not on request. On a hook called captureBeforePrompt, which fires before every prompt you type. One session produced 62 capture events.

The payload is not what you would guess. In one commercial project the archive came to 345MB uncompressed, 313MB encrypted, 42,411 files, and 86.6 percent of it was the .git directory: commit history, loose objects, reflogs, the LFS cache. Source code was 13.4 percent. Deleted content still living in git objects was 29.6 percent. So the thing being exfiltrated is not the code you are showing the agent, it is every version of every file anyone on the team ever committed and then tried to remove, plus whatever secrets were in the reflog before somebody force-pushed over them.

The encryption detail is the part that should end the argument. Archives use AES-256-CTR with the symmetric key wrapped in RSA-OAEP-SHA256, which sounds reassuring until you notice the RSA public key is handed to the client by the server at capture time and the private key never leaves the cloud. A key only the server can use has exactly one function. You cannot decrypt your own snapshots. The vendor can, whenever it wants. The upload goes straight from your machine to Aliyun OSS nodes with a callback registering the object to z.ai's backend, which is also how it stayed invisible to anyone watching for traffic to z.ai.

Two researchers landed on this independently within a day, both by pulling apart app.asar in the Electron bundle and reading the packaging manifest, and one of them documented 564 failed upload retries while poking at it. There is no setting that turns it off. The only mitigation anybody has is making the checkpoints directory immutable at the filesystem level, which also kills checkpoint rollback. Z.ai's official account has said nothing. A ZCode-affiliated account posted "hey I am sorry to let you find it," which is not a denial.

Write-ups at https://tokenstead.ai/guides/zcode-silent-git-history-upload and https://blog.ferstar.org/en/posts/zcode-silent-workspace-snapshot-upload/. The uncomfortable generalization: checkpoint and rollback are now table stakes in coding agents, and every one of them implements the feature by copying your working tree somewhere. Most of them tell you where. Go check which ones you have installed, because the feature that makes an agent safe to run is the same feature that makes it a perfect exfiltration channel.

Related: the Opus 5 exploit story https://clauday.com/article/5b16ef10-f6dc-4969-ac70-708b0ccab05e
