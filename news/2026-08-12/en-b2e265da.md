---
title: A new survey maps self-evolving agents, and the honest finding is nobody can grade them
date: 2026-08-12
lang: en
source: https://clauday.com/article/b2e265da-b6b1-407b-a46c-92be331fab73
tags: Research, Agents, Framework
---

# A new survey maps self-evolving agents, and the honest finding is nobody can grade them

> 来源 / source: [clauday.com](https://clauday.com/article/b2e265da-b6b1-407b-a46c-92be331fab73) · 2026-08-12

Sitting near the top of Hugging Face's daily papers with 107 upvotes: Co-Evolution in Agentic Systems, from Qing Zong, Jiayu Liu, Junhao Shen and a dozen co-authors including Yangqiu Song. It is a survey, which usually means skip it, and this one is worth reading because of what the field looks like when you lay it all out at once.

The organizing move is a three-stage taxonomy. Agent-Agent co-evolution covers agents adapting to each other — adversarial, collaborative, organizational. Agent-Environment co-evolution covers tasks and feedback that change as the agent gets better, so the ground never stops moving. Meta co-evolution is the third floor: making the evolution mechanism itself evolvable, systems that change how they change.

The framing is a correction worth absorbing. Most of the attention this year has gone to single-agent self-improvement — one agent rewriting its own prompts, tools, or source. The survey's argument is that the interesting adaptation pressure is mutual: agents adapting to each other and to environments that adapt back. A system where the benchmark improves alongside the model is a different animal from one where a fixed test gets saturated, and it is much harder to say anything confident about.

Which lands on the part the authors are honest about, and the part that connects to everything else this month. Evaluation is unsolved. When the agent, its tools, and its tasks all move together, you have no fixed point to measure against, and every claim of improvement is partly a claim about a target you also authored. We have watched this go wrong repeatedly — reward hacking on kernel benchmarks, models that edit the scorer, benchmarks where sixty percent of unsolved instances turned out to have broken tests. A field building systems that redesign themselves, without a way to grade them, is running an experiment with no control.

https://arxiv.org/abs/2608.10299
