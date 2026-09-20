---
title: "A Benchmark Where the Agent Has to Go Investigate"
date: 2026-09-19
lang: en
source: https://clauday.com/article/6a29bb1a-c161-4028-8b29-24ddcbe9a9d1
tags: [Benchmark, Agents, Research]
---

# A Benchmark Where the Agent Has to Go Investigate

> 来源 / Source: https://clauday.com/article/6a29bb1a-c161-4028-8b29-24ddcbe9a9d1

Most agent benchmarks hand the model a task and check the answer. RiskChainBench, arXiv 2609.16900, chains two tasks together so that failing the first one poisons the second, which is a far better model of how agents actually break in production.

The setup comes from real platform abuse. Spam campaigns hide their redirect instructions inside emoji, homophones, decomposed characters and junk symbols, then funnel people to disguised links pointing at porn, fraud, gambling or illicit trade. So step one: the model reads the obfuscated message and restores the text, the operational intent, and the destination. Step two: the same underlying model becomes a vision-driven web agent, goes to the site it identified, investigates it, and files an evidence-cited risk report. Crucially the second stage is stripped of the message semantics and of any domain reputation signal. No shortcuts. You have to actually look at the site.

The dataset is 3,600 restoration inputs drawn from 600 source sessions, paired with 600 human-labeled local web environments. Local, meaning frozen and reproducible, which is the only way a web-agent benchmark means anything six months later.

Ten models ran it. Entry Top-1 accuracy, meaning did you identify the right destination, spans 35.2 to 95.2 percent. Web decision accuracy spans 26.3 to 62.8 percent. So the best model in the field identifies the target almost perfectly and then gets the judgment right barely more than half the time. The hard part was never finding the site.

The number worth putting on a slide is this one: execution failures account for 31.9 percent of web runs. Nearly a third of attempts did not produce a wrong answer, they produced no answer, because the agent fell over mid-investigation. That is not a model capability figure, that is a harness figure, and it dwarfs the gap between the best and worst models on judgment. Every accuracy number in agent research is computed on the runs that survived, and almost nobody reports the survival rate. This paper does, and it is 68 percent. Paper at arxiv.org/abs/2609.16900.
