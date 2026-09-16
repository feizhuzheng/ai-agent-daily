---
title: "A Third of the Tasks Were Rated Impossible Without the Agent"
date: 2026-09-15
lang: en
source: https://clauday.com/article/c35e4ac5-c364-4016-adbf-e8833b070bd0
tags: [Agents, Research, Benchmark]
---

# A Third of the Tasks Were Rated Impossible Without the Agent

> 来源 / Source: https://clauday.com/article/c35e4ac5-c364-4016-adbf-e8833b070bd0

Atria Dawn landed on arXiv September 14 as 2609.15818 and went straight to the top of Hugging Face's daily papers with 270 upvotes. Lead author Honglin Guo, and more than 142 co-authors, which is its own kind of signal. The subtitle is "The Dawn of Agentic Superintelligence," which I would ordinarily hold against a paper. Read past it, because the evaluation section is more interesting than the model.

The model is Atria Dawn Preview, a foundation model trained specifically for agents doing scientific research and engineering. It was built through what they call a Verifiable Experience Pipeline, wiring tool interactions to executable environments with externally verified outcomes — which is the same structural bet several groups have converged on this year, that the only trustworthy training signal for an agent is one an environment can check. Across 16 benchmarks they report competitive performance with frontier agents and the highest reported score on five.

Now the part worth your time. They collected 769 task records from 56 real participants alongside the agent logs, and roughly one third of AI-assisted tasks were rated by the participants as infeasible without AI. Not faster. Not cheaper. Would not have happened. That is a much stronger claim than any benchmark delta and it is measured on humans rather than on a leaderboard.

The division of labor they observed is the other keeper. Agents proposed methods and implemented revisions. Humans made most of the final decisions and steered the exploration through judgment and feedback. The authors read that as a shift from task-level execution to project-level partnership, with human effort concentrating on what is worth pursuing and how evidence should guide the work. That is the least hype-shaped sentence in a paper with "superintelligence" in the title, and it matches what [the Fields medallists were complaining about](https://clauday.com/article/f1941f13-5e8d-44f5-8f2d-37c46264b4e6) from the other side — that the bottleneck was never producing results, it was deciding which ones matter.

Skepticism warranted on the benchmark claims, as always when a paper with 142 authors declares the highest reported score on anything. The 769-record human study is the artifact that will survive. If a third of the work genuinely does not happen without the agent, the interesting question stops being whether agents beat humans and becomes which third.
