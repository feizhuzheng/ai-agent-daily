---
title: "AutoDesign: a meta-optimizer rewrites the agent's harness, 40 minutes and under $3"
date: 2026-08-14
lang: en
source: https://clauday.com/article/b27d3db1-5fee-4776-bb29-25911dbd28d0
tags: ["Agents", "Research", "Benchmark"]
---

# AutoDesign: a meta-optimizer rewrites the agent's harness, 40 minutes and under $3

> 来源 / Source: https://clauday.com/article/b27d3db1-5fee-4776-bb29-25911dbd28d0

Meituan's AutoDesign is the second harness-evolution paper in as many days, and it takes a different route to the same conclusion. A meta-harness optimizer steers a code agent to recursively rewrite its own harness based on rollout feedback. The agent runs, the optimizer reads what happened, the agent's scaffolding gets edited, repeat.

They tested it on something concrete instead of a benchmark abstraction: turning academic papers into conference posters. That sounds trivial until you think about what it requires. Reading a paper, deciding what matters, laying out a page, keeping typography and hierarchy legible, and doing it without a human in the loop. It is a long-horizon design task with no single right answer, which is exactly the class of work agents are worst at. They built PosterBench for it, 100 papers across five disciplines, plus a 10-paper controlled subset.

AutoDesign scores 78.32 on PosterBench, beating Claude Design by 7.45 points, and wins the system-blind human preference study. The number I find more useful is the ablation: across configurations, the learned DesignHarness lifts average performance from 54.99 to 67.39. Twelve and a half points from editing the scaffolding, with the model untouched.

The economics are the part to write down. Forty minutes and under three dollars for a full autonomous design loop. That is the price of a harness that then runs forever. Compare that to what anyone pays to fine-tune a model for a domain and the asymmetry is absurd. If the harness carries twelve points and costs three dollars to discover, the question stops being which model and becomes who has run the search on your task yet.

Nobody has. That is the opening. Code is on GitHub, paper is arXiv 2608.13560 under CC BY 4.0, Yaxin Luo and thirteen co-authors.
