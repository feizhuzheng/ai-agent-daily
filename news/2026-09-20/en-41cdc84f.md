---
title: "The Verifier Does Almost All the Work and Costs Under a Cent"
date: 2026-09-20
lang: en
source: https://clauday.com/article/41cdc84f-4eff-4295-b5de-892d40115dc6
tags: [Research, Agents, Benchmark]
---

# The Verifier Does Almost All the Work and Costs Under a Cent

> 来源 / Source: https://clauday.com/article/41cdc84f-4eff-4295-b5de-892d40115dc6

There is a paper on arXiv this week that quietly runs the experiment everybody building agent scaffolding should have run first. It is called How Do Agent Harnesses Create Value? Planning Information and Release Control in Stateful LLM Agents, by Yukun Zhang, Kemu Xu and Yishen Chen, arXiv 2609.20474, at https://arxiv.org/abs/2609.20474.

The setup is the part to steal. To find out whether planning text helps because it contains a plan or because it is more text, they compare a task-specific plan against shuffled policy text with a matched word count, across retail and airline scenarios. That control is missing from most harness papers, and with it in place the fixed plan is worth about 7.17 percentage points of verified success rate, concentrated in the harder tasks. Real, useful, not enormous.

Then they measure the verifier separately and the numbers reorder the priorities. The verification step rejects 61 percent of invalid episodes while wrongly withholding 17 percent of valid ones, and it costs under one cent per episode. Their own conclusion, which is the line worth quoting to your team, is that a standalone verifier captures nearly all the false-pass benefit of the full planning plus verification stack at a fraction of its cost.

Whether that is the right tradeoff depends entirely on what a wrong answer costs you, and the paper says so directly. Throwing away 17 percent of good work is unacceptable in a chat product and cheap insurance in an accounting close. That framing, error cost decides the harness, is more useful than any specific architecture recommendation.

The honest reading is uncomfortable for a lot of tooling roadmaps. Most of the effort in agent frameworks this year went into planning, decomposition and orchestration, and the cheapest component in the stack is doing most of the measurable work.
