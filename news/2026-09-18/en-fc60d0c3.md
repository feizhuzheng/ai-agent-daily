---
title: "Somebody rebuilt Jev in a browser tab and got 81 percent"
date: 2026-09-18
lang: en
source: https://clauday.com/article/fc60d0c3-79bf-4d24-b4b5-67066e6ee42a
tags: [Agents, Open Source, Research]
---

# Somebody rebuilt Jev in a browser tab and got 81 percent

> 来源 / Source: https://clauday.com/article/fc60d0c3-79bf-4d24-b4b5-67066e6ee42a

SemIf, formerly called OpenJev, hit 506 points on Hacker News. It is a browser-based experiment that runs local decision models with no backend at all, and it is explicitly an independent research project with no affiliation to Typesafe AI, whose Jev and System One models it is reacting to. Try it at https://openjev.com, no signup, no waitlist, it just loads and runs.

What it actually tests is a narrow and good question: given the same local model, is it better to read option probabilities directly off the logits without decoding anything, or to make the model write those probabilities out as JSON token by token. Two paths to the same number, one of which costs a forward pass and the other costs a generation loop. That comparison is the sort of thing everybody assumes they know the answer to and almost nobody has put in front of you as a thing you can click.

The accuracy ladder is the number worth carrying. Qwen3 0.6B at 639 MB gets 44.0 percent. MiniCPM5 2B at 1.56 GB gets 68.6 percent. Qwen3.5 4B at 3.01 GB gets 81.3 percent. Hosted Jev sits at 88.3 percent. So 3 GB of weights running inside a browser tab closes most of the gap to a hosted System One model, and the remaining seven points is what you are paying a vendor for. Whether seven points is worth a network round trip and an API bill depends entirely on what the decision gates, and now you can actually reason about it because somebody published both ends.

Weights come from Hugging Face, the runtime is the open-source wllama library, and the whole thing being clickable is the point. Fast local judgment calls are the part of an agent loop that gets invoked constantly and that people reflexively route to a frontier model. This is a two-day independent reproduction that says you probably do not have to.

Related: Needle 3 https://clauday.com/article/69302306-bb98-4e2b-a45f-dc68f4309ae4
