---
title: "Claude Code wouldn't read your AGENTS.md unless you let it phone home"
date: 2026-09-23
lang: en
source: https://clauday.com/article/eaa1d470-b485-4c25-b9ac-313d4805f520
tags: [Agents, Coding, Infrastructure]
---

# Claude Code wouldn't read your AGENTS.md unless you let it phone home

> 来源 / Source: https://clauday.com/article/eaa1d470-b485-4c25-b9ac-313d4805f520

Reading a local markdown file requires no network. Claude Code 2.1.277 made it require one anyway, and nobody noticed for a while because it failed completely silently.

Here is the mechanism. AGENTS.md support shipped as a built-in plugin under a new extensibility system called Mods, and the loader sits behind a remote Statsig feature flag named tengu_agents_md_mod. Off by default, turned on from Anthropic's servers. If you set CLAUDE_CODE_DISABLE_NONESSENTIAL_TRAFFIC=1, or you run Claude Code through Bedrock, Vertex, or any third-party gateway, your session never fetches feature flags. The gate can never evaluate true. Your AGENTS.md just doesn't load. No error, no warning, no line in the startup output. The agent behaves as if the file isn't there.

The privacy inversion is what made this land at 426 points on HN. The people most likely to disable telemetry are the ones running in regulated environments, on air-gapped-ish setups, or through a corporate gateway — exactly the people who most need a checked-in instruction file to actually be read. Turning off data collection silently degraded local behavior, which is the one direction a telemetry switch should never work.

Anthropic's mpoteat responded fast and didn't hedge: this is a rollout artifact, we needed a way to turn this off remotely via feature flags if it broke something, and with telemetry off you don't get those. Fixed in v2.1.281, same day. Credit where due — that is the correct response and it took hours, not weeks.

The part worth keeping is not the bug, it's the shape of it. When a feature flag system is wired into the telemetry transport, every flag becomes a dependency on the vendor being reachable and willing. Commenters piled on the other half too: a preference about which filename to read should not need a plugin architecture, a mod system, and function hooks. Overengineering is what created a surface for a remote switch to sit on in the first place. If your harness reads config files behind server-evaluated gates, you don't fully know what your agent read.

https://blog.szypowi.cz/p/claude-code-reads-agents.md-only-when-telemetry-is-on/
