---
title: "Astra's 98.6% on ARC-AGI-3 Has a Harness-Sized Asterisk"
date: 2026-09-03
lang: en
source: https://clauday.com/article/760df7af-8ef1-4bd1-8f66-f9ab6481c575
tags: [Benchmark, Agents]
---

# Astra's 98.6% on ARC-AGI-3 Has a Harness-Sized Asterisk

> 来源 / Source: https://clauday.com/article/760df7af-8ef1-4bd1-8f66-f9ab6481c575

OpenAI says GPT-6 Astra scores 98.6% on ARC-AGI-3, up from 7.8% six months ago. Ninety points in half a year on the benchmark specifically designed to resist memorization. Then ARC Prize published its own numbers, and the asterisk turned out to be bigger than the headline.

Same model, two harnesses: with ARC's standard harness, Astra scores 62.7% on the semi-private set for $26K. With OpenAI's provider adapter — a Responses API setup that retains reasoning between turns and uses compaction to manage long contexts — it scores 99.9% for $19K. Thirty-seven points of difference, and the better harness is also cheaper. ARC's own framing is blunt: the benchmark is measuring Astra and OpenAI's agent system together, not the model alone.

To be clear, the model is genuinely remarkable — it beats the median human on action efficiency on 96% of levels, solving puzzles with fewer moves than people do. But the two-harness split is the cleanest public demonstration yet of something this site has been hammering for months: the harness is not plumbing, it's capability. Hold the weights fixed, change the scaffolding, gain 37 points.

The uncomfortable question for every leaderboard: which number is the model, and which is the wrapper? ARC Prize's writeup is at https://arcprize.org/blog/astra and the full results at https://arcprize.org/results/openai-gpt-6-astra.
