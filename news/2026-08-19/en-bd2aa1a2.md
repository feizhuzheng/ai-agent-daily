---
title: "Ornith-1.5: The Self-Improvement Loop Goes Open Weights"
date: 2026-08-19
lang: en
source: https://clauday.com/article/bd2aa1a2-5b44-4386-b1c5-bcf72a0d2892
tags: [Open Source, RL, Coding]
---

# Ornith-1.5: The Self-Improvement Loop Goes Open Weights

> Source: [clauday.com](https://clauday.com/article/bd2aa1a2-5b44-4386-b1c5-bcf72a0d2892)

Ornith-1.0 taught a model to rewrite its own harness mid-training. Ornith-1.5, released this week under MIT license, closes a bigger loop: the model now generates its own training tasks too. Task generation, scaffold construction and solution rollouts are jointly optimized, so instead of a fixed human-curated curriculum, the model invents problems, discovers strategies for solving them, and improves through RL on the results. That is the recursive self-improvement recipe, shipped as downloadable weights.

The family spans 9B dense, 35B MoE and 397B MoE, with FP8, GGUF, MLX and NVFP4 quants all released day one. The claimed numbers are startling for open source: 86.1 on Terminal-Bench 2.1, 86 on SWE-Bench Verified, 56 on DeepSWE, which the team frames as comparable to Claude Opus 4.8 on reasoning, agentic and coding work. Hacker News gave the launch 152 points and the usual argument about whether self-generated curricula can escape their own blind spots.

That argument is the interesting part. When a model writes its own training tasks, the obvious question is who grades the grader: a self-curriculum can drift toward problems the model already likes. The Ornith bet is that jointly optimizing all three stages keeps the task generator honest, because tasks that do not produce learning signal get selected out. Whether that holds at 397B scale is exactly the kind of thing the community can now test, because the weights are MIT and public.

Two months ago this pipeline was a lab curiosity. Now it is on Ollama. https://ornith.ai/ornith_1_5.html
