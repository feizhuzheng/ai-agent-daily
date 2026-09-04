---
title: "K2 Horizon: Six Models, Zero Secrets"
date: 2026-09-03
lang: en
source: https://clauday.com/article/f0c803ae-8d7f-42e6-a834-75dba56f5948
tags: [Open Source, Agents]
---

# K2 Horizon: Six Models, Zero Secrets

> 来源 / Source: https://clauday.com/article/f0c803ae-8d7f-42e6-a834-75dba56f5948

The Institute of Foundation Models at Abu Dhabi's MBZUAI released K2 Horizon on September 3: a connected fleet of six models from 0.9B to 375B parameters, and every layer of the stack is public. Weights, source code, training data, methodology — all of it, under Apache 2.0. They're calling it the largest fully open release in history, and on the training-data axis nobody credible is disputing it.

The fleet logic is what makes this an agent story, not just an open-weights story. Each size has a job: 0.9B for local development, 3.7B for single-node serving, 7B for cost-sensitive deployment, 32B for everyday heavy use, 36B for production serving experiments, and the 375B flagship built for long-horizon agents. Shared architecture, shared vocabulary, shared interfaces and deployment tooling, so you can prototype on the small one and promote to the big one without rewriting your stack.

IFM also says this is the first fully open fleet to expose its complete agentic post-training process. That's the part labs guard most jealously — everyone publishes weights eventually, nobody publishes how they taught the model to run a 30-step tool loop. If the documentation holds up, this is the reference implementation the open agent ecosystem has been missing.

DeepSeek and Qwen made open weights table stakes. K2 Horizon is betting the next differentiator is open process. Announcement at https://ifm.ai/blog/k2, models at https://huggingface.co/IFM.
