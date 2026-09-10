---
title: "Miles v0.1 Is the Post-Training Stack Labs Usually Don't Open Source"
date: 2026-09-09
lang: en
source: https://clauday.com/article/fddd3c8c-8b19-4d65-995f-7172879a4d55
tags: [Infrastructure, RL, Open Source]
---

# Miles v0.1 Is the Post-Training Stack Labs Usually Don't Open Source

> 来源 / Source: https://clauday.com/article/fddd3c8c-8b19-4d65-995f-7172879a4d55

RadixArk dropped Miles v0.1 and called it production-level post-training, which is a boring name for the least boring thing on Hugging Face's board today. This is the plumbing under every agent RL story of the past six months, released whole instead of described in a paper.

What is in the box: rollout engines on SGLang, training backends on both Megatron-LM and PyTorch FSDP, and several weight-synchronization protocols so you can pick a topology instead of inheriting one. Past plain RL it covers LoRA-based RL, on-policy distillation, supervised fine-tuning, asynchronous agentic RL, and, oddly but usefully, diffusion models. The design line they lead with is that components should be verified, clean, and customizable, which reads as a shot at the research-code-in-production problem everyone has been quietly eating.

The demo is the flex. Fully asynchronous agentic RL on GLM-5.2, a 744B-A40B model, doing terminal-based coding tasks across 64 NVIDIA GB300s. Asynchronous agentic RL is the hard case: rollouts take minutes and finish out of order, so the training loop has to keep learning while half the fleet is still typing. Most open frameworks quietly do not do that at this size. This one shows it running.

The pattern worth noticing is who is shipping the post-training layer as open infrastructure right now. Weights get released and get all the attention, but the thing that decides whether your agent gets better next month is the loop that turns its trajectories back into gradients (https://clauday.com/article/035d33f9-4135-4dd4-bfad-bbc862f299c3). NeoHorse released the loop's product today, Miles releases its machinery. Repo and report: https://arxiv.org/abs/2609.08368
