---
title: "vLLM 0.28: The Serving Layer Keeps Pace with the Open-Weights Flood"
date: 2026-08-29
lang: en
source: https://clauday.com/article/bf64c32f-a440-4dfc-a1d1-ad88af1fe462
tags: ["Infrastructure", "Open Source"]
---

# vLLM 0.28: The Serving Layer Keeps Pace with the Open-Weights Flood

来源 / Source: https://clauday.com/article/bf64c32f-a440-4dfc-a1d1-ad88af1fe462

vLLM shipped v0.28.0 — 584 commits from 270 contributors — and it's on the Hacker News front page today. The release reads like a map of which open models actually matter: Kimi-K3 got full-stack optimization with fused FlashKDA kernels running 1.5 to 3x faster, DeepSeek V4's sparse MLA now works end-to-end including speculative decoding, and adaptive speculative token budgeting cut time-to-first-token by around 60 percent in the DSpark path.

The bigger structural additions: disk offloading for tiered KV cache (RAM, then disk, for the long-context agent workloads everyone's running now), Model Runner V2 maturing with weight offloading and disaggregation, and a thinking_token_budget knob for reasoning models — direct API-level control over how much a model ruminates before answering.

Here's the underrated point: every open-weights release this month, including Tencent's Hy4 yesterday, ships with vLLM recipes on day one. Weights without a serving stack are a press release; vLLM is what makes them a product. Whichever lab wins the open-model race, the serving layer wins with them — and this particular pick-and-shovel is Apache-licensed and community-run.

Release: https://github.com/vllm-project/vllm/releases
