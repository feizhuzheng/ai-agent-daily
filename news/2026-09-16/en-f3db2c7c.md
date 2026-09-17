---
title: "Three Bad Memory Fixes Stack Into One That Works"
date: 2026-09-16
lang: en
source: https://clauday.com/article/f3db2c7c-fc41-4243-bea6-9c0bbeddda19
tags: [Research, Agents, Benchmark]
---

# Three Bad Memory Fixes Stack Into One That Works

> 来源 / Source: https://clauday.com/article/f3db2c7c-fc41-4243-bea6-9c0bbeddda19

Take a language model, teach it 100 tasks one after another with no access to the earlier examples, then ask what it remembers. Naive sequential fine-tuning retains 1.2%. That is the honest baseline for continual learning and it is why nobody ships it. A team from Johns Hopkins — Alvin Zhang, Daniel Khashabi and Tianmin Shu — got that to 34.9% by stacking mechanisms that each look mediocre alone. Paper at https://huggingface.co/papers/2609.06986, 287 upvotes and the top of the daily board.

The framing is what makes it useful. They sort the field along two axes: anchors, meaning what you preserve, and low-rank allocation, meaning where updates land. Three anchors — generative replay for data, self-distillation for function, importance-based regularization for weights — crossed with shared versus merged LoRA. Then a full factorial over the combinations, with task-level successive halving to make the search affordable. All three anchors plus merged LoRA is the 34.9%, a 28x improvement over doing nothing clever.

The word to sit with is super-additive. Replay and merged LoRA carry the most weight individually, but the combination beats what you would predict from summing the parts, and it does so on all three datasets they tried: Symbol-QA, LLM-QA and Real-QA. The continual learning literature is full of papers arguing their one mechanism is the right one. This one says the argument was the mistake.

For anyone building agent memory this is directly load-bearing, because the 100-task setup is basically what a long-lived agent goes through. And the caveat the authors state plainly is the one that matters: memorization improved a lot, preserving general capability did not. You can now make an agent remember its hundred jobs. Whether it is still good at anything else is a separate problem and nobody has solved it.
