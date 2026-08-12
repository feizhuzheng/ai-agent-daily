---
title: A 150M model scored 29.5% on ARC-AGI-1 at seven ten-thousandths of a dollar per task
date: 2026-08-11
lang: en
source: https://clauday.com/article/ba5ef5f5-b4b3-4c49-a469-22d85ea3b808
tags: Research, Infrastructure
---

# A 150M model scored 29.5% on ARC-AGI-1 at seven ten-thousandths of a dollar per task

> 来源 / source: [clauday.com](https://clauday.com/article/ba5ef5f5-b4b3-4c49-a469-22d85ea3b808) · 2026-08-11

Second on Hugging Face Daily Papers today with 681 upvotes, from Pathway. BDH-CQ does in-context learning with recurrent latent reasoning, and the headline is a 150-million-parameter model hitting 29.5 percent pass@2 on ARC-AGI-1 at $0.0007 per task. That breaks the previously reported cost-accuracy Pareto frontier on that benchmark.

The mechanism is a genuine departure from how everyone currently gets reasoning out of a model. Inputs presented at inference time continuously update the model's recurrent memory. Then the query is solved by iterating in a high-dimensional latent space — without verbalizing any intermediate steps. No chain of thought. No tokens spent narrating. The reasoning happens in the state, not in the output.

That is why the cost number is what it is. Every frontier reasoning system today buys accuracy by generating more tokens, which is why inference bills scale with how hard the problem is. If the computation lives in latent recurrence instead, difficulty costs you iterations of a tiny model rather than thousands of tokens from a huge one. Different curve entirely.

The obvious caveat: ARC-AGI-1 at 29.5 percent is not a frontier result in absolute terms, and one benchmark is not a paradigm. But the interesting axis here was never absolute accuracy — it's that this came out of 150 million parameters. And there's an uncomfortable implication for anyone building agent observability: a model that reasons without verbalizing gives you nothing to read. Every interpretability and monitoring tool built in the last two years assumes there's a trace to look at. Same day, coincidentally, as the paper showing the encrypted traces we do get aren't safe either.

Paper: https://arxiv.org/abs/2608.09888
