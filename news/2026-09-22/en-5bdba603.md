---
title: "Self-improving agent harnesses mostly memorize the test, and here are the numbers"
date: 2026-09-22
lang: en
source: https://clauday.com/article/5bdba603-f1b6-4aed-8555-d947b797d379
tags: [Research, Agents, Benchmark]
---

# Self-improving agent harnesses mostly memorize the test, and here are the numbers

> 来源 / Source: https://clauday.com/article/5bdba603-f1b6-4aed-8555-d947b797d379

A lot of recent work lets an agent edit its own harness — the prompts, control flow, tooling, memory and context management around a frozen model — and iterate. It is recursive self-improvement at the system level rather than the weight level, and it posts great results. RRSI (arXiv 2609.24972, submitted September 21) says a large chunk of those results are memorization, and then goes and measures how large.

The finding: unregularized harness evolution shows big in-distribution gains that shrink or vanish out of distribution. The fix is regularization applied to both halves of the evolutionary loop. The proposer gets a temporally annealed budget limiting how many edits it can bundle into one candidate, plus pressure toward unexplored trajectories based on evolution history. The selector gets a critic that screens out benchmark-specific proposals and a pruner that removes edits that are too small, too expensive, or no longer earning their keep.

Across eight benchmarks spanning coding, agentic workspace and engineering design: up to 14.1 points on the split it evolves against, up to 4.7 points on the five out-of-distribution benchmarks. That 14.1 versus 4.7 is the whole paper. Two thirds of the headline gain does not travel, and that is after regularization. Whatever the unregularized gap looks like, it is worse.

The thing that makes this more than a cautionary tale is the last number: the regularized harness runs on 30% fewer policy tokens. Constraining the evolution did not just make it generalize better, it made it produce something smaller. The pruner is doing what a human maintainer does and almost no automated harness search does, which is delete things. Code and project page are linked from the paper.

https://arxiv.org/abs/2609.24972
