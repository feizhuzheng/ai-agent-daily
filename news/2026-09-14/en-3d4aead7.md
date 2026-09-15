---
title: "Thirteen Clever RL Data Recipes, Zero That Beat Random"
date: 2026-09-14
lang: en
source: https://clauday.com/article/3d4aead7-c918-405b-91a6-55524e112d57
tags: [Research, RL, Benchmark]
---

# Thirteen Clever RL Data Recipes, Zero That Beat Random

> 来源 / Source: https://clauday.com/article/3d4aead7-c918-405b-91a6-55524e112d57

DataFlex-RL sat at the top of HuggingFace's daily papers board with 96 upvotes, and the reason is that it is a negative result, which almost nobody publishes. Paper at https://arxiv.org/abs/2609.06107, from Hao Liang, Mingrui Chen, Hengyi Feng, Meiyi Qiang and Wentao Zhang, submitted September 5.

The setup is a controlled evaluation platform for data policies in reinforcement learning with verifiable rewards — the family of techniques where you decide which training examples to sample, how to reweight them, and how to mix domains adaptively as training proceeds. Thirteen configurations, two base models (Qwen2.5-7B-Base and Llama-3.1-8B-Base), twelve benchmarks across math, logic and science. Everything held constant except the data policy.

The finding: uniform GRPO improves domain-balanced average accuracy by 7.76 points over the untrained checkpoint, and none of the reweighting methods or adaptive mixture strategies beat uniform sampling at 95% confidence. Not "beat it by a little." None of them cleared significance. Data policies measurably change what happens during training and do not reproducibly improve the result.

There is a second number that is arguably more important than the first, and it is easy to miss. When the authors changed which benchmarks they averaged over, the rankings of the thirteen methods came out negatively correlated, at -0.33. Same runs, same checkpoints, different eval suite, and the leaderboard roughly inverts. That is a direct measurement of how much of the RL-recipe literature is eval selection, and it should make you deeply suspicious of any paper reporting a two-point gain from a clever sampler on a benchmark set the authors chose.

This is the third negative result in a month that landed the same way. [Three attempts to beat LRU on real agent traces, all three lost](https://clauday.com/article/22ef7f1e-11dd-44ba-8f76-a66758bca581). [$1,500 spent proving the 90% token savings aren't real](https://clauday.com/article/7d06a720-8150-4bd1-be47-1778c3923045). Now thirteen data policies that do not beat uniform. The common shape is that someone built the controlled comparison the original papers skipped, and the effect vanished. If you are running agentic RL and you were about to spend a quarter on a curriculum scheduler, read this one first and spend the quarter on your eval suite instead.
