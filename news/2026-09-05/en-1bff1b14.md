---
title: "Two Papers, Same Day, Same Message: Agent RL Is Out of Environments"
date: 2026-09-05
lang: en
source: https://clauday.com/article/1bff1b14-b998-4641-b3c6-7a4bca4ff397
tags: [Research, RL, Benchmark]
---

# Two Papers, Same Day, Same Message: Agent RL Is Out of Environments

> 来源 / Source: https://clauday.com/article/1bff1b14-b998-4641-b3c6-7a4bca4ff397

Two papers landed on arXiv on September 3 saying the same thing from opposite directions: the bottleneck in agent RL is no longer models or compute, it is environments to train them in. Terminal-Universe (https://arxiv.org/abs/2609.04148) also topped the agent section of Hugging Face's daily papers at 254 upvotes.

Terminal-Universe recycles what already exists. It takes public agent trajectories — static logs of past runs — and reconstructs executable environments from them: replay the file operations to restore the workspace, synthesize new tasks on top, extend single-shot interactions into multi-round ones with feedback. From public trajectories the team generated 37,300 task-sufficient environments, and training Qwen3.5-27B on them lifted Terminal-Bench 2.1 by 11.9 points and multi-round EvoCode-Bench v2 by 13.8.

Environment Evolution for Terminal Agents (https://arxiv.org/abs/2609.04128) attacks the other end: what happens when your model saturates the environments you have. Its answer is to evolve difficulty off-policy along three directions derived from the learning objective, using a multi-agent system to synthesize progressively harder environments. Gains: 14.4 points for Qwen3.6-27B and 18.0 for the 35B-A3B on the same benchmark, with Hy4, Claude Opus 5 and GPT-5.6 Sol confirming the evolved environments really are harder.

Same-day convergence like this is usually a tell. ByteDance's HarnessDev benchmark asked whether models can build their own scaffolding (https://clauday.com/article/035d33f9-4135-4dd4-bfad-bbc862f299c3); these two papers say the training side has the same shape. The data flywheel of the LLM era is becoming an environment flywheel: whoever turns yesterday's trajectories into tomorrow's harder tasks cheapest gets to keep improving after everyone else runs out of things to practice on.
