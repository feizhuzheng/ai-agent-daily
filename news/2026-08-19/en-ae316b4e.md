---
title: "Agent Lightning 1.0: RL That Keeps the Harness"
date: 2026-08-19
lang: en
source: https://clauday.com/article/ae316b4e-cbf4-4810-9d2d-f86eb31473d9
tags: [RL, Framework, Open Source]
---

# Agent Lightning 1.0: RL That Keeps the Harness

> Source: [clauday.com](https://clauday.com/article/ae316b4e-cbf4-4810-9d2d-f86eb31473d9)

The standard way to RL-train an agent model is to strip away its deployment harness, train the bare model in a sanitized loop, then bolt the harness back on and hope the skills transfer. Agent Lightning v1.0, from a Microsoft Research team, argues that is backwards. Its term is harnessed agentic RL: the harness that manages tools, context and control flow at deployment time participates in post-training. You train the thing you actually ship.

The engineering is a disaggregated architecture where any agent connects to RL training through an LLM endpoint proxy, no rewrite of your agent required. The unglamorous problems that kill these projects, retokenization, sample merging, advantage calculation, loss normalization, backend scheduling, are handled in the framework, and the whole thing is about 3,500 lines of code. Training scripts and the complete workflow are released.

The headline number: Qwen3.5-9B on SWE-bench Verified goes from 41.8 to 56.4 percent, a 14.6 point jump, using just 6,000 training examples and modest compute. A 9B model past 56 on Verified is territory that belonged to much bigger models a few months ago, and the sample efficiency is the tell that harness-in-the-loop training captures something bare-model RL misses.

This is now a wave, not a paper. DeepSeek shipped its Harness v0.1 last week, LEGO-RL appeared on the same daily board calling itself harness-native, and the shared thesis is that agent capability lives in the model-harness system, so that is the unit you should train. arXiv: https://arxiv.org/abs/2608.17528
