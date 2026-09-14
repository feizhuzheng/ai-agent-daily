---
title: "8.7x Less Memory per Agent Sandbox, and the Trick Is When You Compress"
date: 2026-09-13
lang: en
source: https://clauday.com/article/0cbe1a5a-069d-4ecb-bed1-c2ed3f35462a
tags: [Infrastructure, Research, Agents]
---

# 8.7x Less Memory per Agent Sandbox, and the Trick Is When You Compress

> 来源 / Source: https://clauday.com/article/0cbe1a5a-069d-4ecb-bed1-c2ed3f35462a

If you run agents at scale you run sandboxes at scale, and sandboxes are mostly idle RAM. Every one of them boots from the same template, does a little work, then sits there holding memory while a model thinks. AgentZip, arXiv 2609.11294, submitted September 10, gets up to 8.7x memory reduction on sandbox-owned memory where standard Linux compression manages 2.1x. https://arxiv.org/abs/2609.11294

Three things get it there, and the third is the one worth stealing. First, it exploits template-relative and cross-sandbox redundancy — a thousand sandboxes from one template share enormous amounts of nearly-identical state, and the compressor is built to profit from pages that are similar rather than requiring them to be identical, which is where dedup normally gives up. Second, it widens the scope to any page with a profitable representation instead of only cold ones. Third, and this is the insight: compression is scheduled by execution phase, not by memory pressure. Standard systems compress when they are running out of RAM, which is exactly when the workload needs to be fast. AgentZip compresses while the LLM is thinking, because that is dead time on the sandbox anyway.

That reframing moves the cost from the wrong place to the right one. The overhead stops being compression-time page selection and becomes restore-time prefetching, which you can predict. The result is that aggressive compression, which normally costs 3.1x slowdown, drops to 1.40x while keeping nearly all the memory savings. Seven authors led by Mengming Li, filed under both AI and operating systems, which is the correct pair of categories and a sign of where this field is drifting. No code repo in the abstract.

The context is that fleet economics have become a real line item. [Herdr went multi-machine](https://clauday.com/article/f99c62c2-f0ff-486e-a796-8cd16b4d2e07) because agent fleets outgrew a laptop, and [substrate blindness got a name and a number](https://clauday.com/article/129f2a0b-e389-46b6-9e8a-3a4f7550d9c0) because agents keep behaving as if the machine underneath them is free. It is not. Somewhere between "one agent on my laptop" and "high-fanout sandboxes," memory per sandbox stopped being a rounding error and became the thing that decides how many agents you can afford to run in parallel.

The general lesson outruns this paper. The agent loop has a huge, predictable, periodic idle window baked into it — every time the model is generating, the sandbox has nothing to do. Most infrastructure still schedules work by resource pressure, a habit inherited from workloads that did not pause for several seconds on a fixed rhythm. Anyone building agent infra should be asking what else belongs in that window. Snapshotting, GC, index rebuilds, log shipping, all of it is currently competing with execution for no reason.
