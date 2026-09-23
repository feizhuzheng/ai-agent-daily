---
title: "Google's agent runtime has a floor under it, and the floor is the real story"
date: 2026-09-22
lang: en
source: https://clauday.com/article/f8a7b0b9-4e3b-4b63-8607-c1c72c955da6
tags: [Infrastructure, Open Source, Agents]
---

# Google's agent runtime has a floor under it, and the floor is the real story

> 来源 / Source: https://clauday.com/article/f8a7b0b9-4e3b-4b63-8607-c1c72c955da6

When google/ax landed last week as Google's open agentic orchestration runtime, the README mentioned it was built on something called Agent Substrate. That thing now has its own repo and it is trending on its own, 301 stars today on 2,923 total.

The claim is specific enough to argue with: a secure-by-default agent execution runtime engineered to run millions of sandboxes at 10x the density of standard container runtimes. It gets there by mapping many actors onto far fewer workers and harvesting idle time, and the number that makes it credible is sub-500ms resume at over 500 suspend/resume activations per second. Zero-trust isolation at the kernel and network level, microVMs or gVisor for the sandbox, Kubernetes underneath for provisioning and worker lifecycle.

Read that density claim as a statement about what agent workloads actually look like. An agent spends most of its wall-clock waiting — on a model call, on a tool, on a human. A container that sits resident through all of that is paying full price for mostly nothing. Suspend and resume fast enough and idle stops costing anything, which is the only way the per-agent economics work when you have millions of them instead of thousands.

The Apache 2.0 license and the non-officially-supported disclaimer are both there, and the README says early development, not ready for production. Fine. The layering is what to watch: ax is the harness, Substrate is the substrate, and Google is publishing both separately. That is an invitation for other harnesses to run on the same floor, which is a very different move from shipping one integrated runtime.

https://github.com/agent-substrate/substrate
