---
title: "Intern-S2-Preview: 397B for science, and a 4B memory bolt-on that gains 3.4 points"
date: 2026-08-14
lang: en
source: https://clauday.com/article/4f7bdbf3-dab9-4ae4-a2b2-b48726785704
tags: ["Agents", "Research", "Infrastructure"]
---

# Intern-S2-Preview: 397B for science, and a 4B memory bolt-on that gains 3.4 points

> 来源 / Source: https://clauday.com/article/4f7bdbf3-dab9-4ae4-a2b2-b48726785704

Shanghai AI Lab put out Intern-S2-Preview, a scientific agentic foundation model with 149 authors on the paper. The backbone is 397 billion parameters with dedicated time-series modules for numerical forecasting, which is an unusual thing to build into a language model and tells you who this is for. Chemists, biologists, physicists. People whose data is not text.

The design choice worth stealing is a separate 4-billion-parameter Memory Decoder that bolts onto the main model. On specialized biology tasks it moves performance from 56.92 to 60.32 without touching the backbone weights at all. Three and a half points from a small attachable module. That is the same shape as this week's harness papers arriving from a different direction: capability added at the system layer rather than inside the model. If a 4B side module can inject domain memory into a 397B model, the retraining-per-domain playbook looks expensive.

The training pipeline is where the engineering shows. Supervised fine-tuning, reinforcement learning, partial rollout with off-policy correction, and adaptive length regularization. Partial rollout with off-policy correction is the practical answer to the thing that makes long-horizon agentic RL miserable, which is that one straggler trajectory stalls the entire batch. Adaptive length regularization is the answer to the other one, models learning to ramble because longer chains score better. Neither is glamorous. Both are why the run finishes.

The claim is competitive or leading results across multimodal scientific understanding, reasoning, generation and long-horizon tasks, plus general-purpose benchmarks. It handles scientific documents, images and raw text through one pipeline.

Read this alongside the money flowing into AI-for-science and it's a preview in both senses. Thirty-five pages, arXiv 2608.13505, CC BY 4.0.
