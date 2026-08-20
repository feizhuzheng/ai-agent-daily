---
title: "Agentic ESOpt: Tune a 27B Agent Without the RL Stack"
date: 2026-08-19
lang: en
source: https://clauday.com/article/cd592ad3-393d-484c-9ff9-937ff8eaed61
tags: [RL, Research]
---

# Agentic ESOpt: Tune a 27B Agent Without the RL Stack

> Source: [clauday.com](https://clauday.com/article/cd592ad3-393d-484c-9ff9-937ff8eaed61)

The reason agent fine-tuning stays inside big labs is not data, it is the RL stack: backpropagation through long horizons needs optimizer states and gradients that multiply your GPU memory several times over. Agentic ESOpt, a new paper at 91 upvotes on HuggingFace's daily board, revives an old idea to break that wall: evolution strategies. Sample perturbations around the current weights, roll out the resulting agents, apply a reward-weighted update. No backprop anywhere.

The consequence is that full-parameter optimization costs inference-level memory. If you can serve the model, you can tune it. The authors, including Yee Whye Teh and Wee Sun Lee, demonstrate full-parameter tuning of Qwen-3.5-27B on WebArena-Lite for a 6.69 percent gain over baseline, and their test-time prompt-parameter co-evolution wins in 28 of 36 settings. Because ES treats reward as a black box, long-horizon credit assignment, the thing that makes agentic RL miserable, does not require decomposing the reward at all. The episode either scored well or it did not.

The caveat to keep: ES is sample-hungry, all those perturbed rollouts are real inference spend, so this trades GPU memory for rollout volume. That trade is exactly right for teams with serving capacity but no training cluster, which describes most agent companies.

Read it next to Agent Lightning v1.0, which landed the same day: one keeps RL but engineers the harness into it, the other throws out backprop entirely. Both are attacks on the same wall, the cost of turning a deployed agent into a trainable one. https://arxiv.org/abs/2608.17310
