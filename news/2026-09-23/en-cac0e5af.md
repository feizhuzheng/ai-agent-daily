---
title: "Jev in 25 lines of Python, and the hype deflates"
date: 2026-09-23
lang: en
source: https://clauday.com/article/cac0e5af-99bd-470a-8aee-2aaff961cc49
tags: [Agents, Open Source, Research]
---

# Jev in 25 lines of Python, and the hype deflates

> 来源 / Source: https://clauday.com/article/cac0e5af-99bd-470a-8aee-2aaff961cc49

Duarte O. Carmo at NobodyWho calls it a parody. It hit 591 points on HN anyway, because the joke is load-bearing.

Jev has been the most hyped idea in the agent stack for about a week — a fast decision model that sits in front of your expensive LLM and routes, classifies, and decides without burning a frontier call. The pitch involves training, a new model family, and a company. Carmo's response is 25 lines of Python using llama-cpp-python and Qwen3-0.6B, running locally.

The trick is embarrassingly simple and that's the point. You give the model a prompt with the choices spelled out. Instead of sampling tokens, you reach in and grab the logits for the tokens corresponding to each choice, softmax them, and you have probabilities. Legitimate, Spam, Phishing — three numbers, one forward pass, no generation loop, no API, no RL. A 0.6B model on your laptop.

This is the fifth or sixth artifact in a row landing on the same insight from different directions: the expensive, unverifiable, slow part of using a language model is free-form generation, and an enormous share of what people call agent work is actually classification wearing a costume. Constrain the output space to a fixed set and the cost collapses, the latency collapses, and you get calibrated probabilities instead of a sentence you have to parse.

The argument the post doesn't make explicitly, and should: if 25 lines and a 0.6B model get you most of the way, the defensible thing about a decision model was never the decision. It's the training data, the calibration, and whatever it does when none of the choices fit. Those are real problems. But the demo everybody was passing around was not showing you those, it was showing you logit extraction, and logit extraction is free.

Read it as a stress test, not a takedown. If the minimal version gets close, you learn what the full version is actually selling.

https://www.nobodywho.ai/posts/jev-in-25-lines/
