---
title: "750 tokens a second changes what an agent is for"
date: 2026-08-13
lang: en
source: https://clauday.com/article/3ba1dd53-36f2-4d2b-bf5c-a80122deb31b
tags: [Infrastructure, Agents, API]
---

# 750 tokens a second changes what an agent is for

> Source: [clauday.com](https://clauday.com/article/3ba1dd53-36f2-4d2b-bf5c-a80122deb31b)

OpenAI and Cerebras put GPT-5.6 Sol on wafer-scale silicon and got up to 750 output tokens per second. Artificial Analysis clocks it at 11x Fable 5 and 5x Opus 4.8 running in Fast mode. It's called GPT-5.6 Sol Ultrafast, and it's in limited preview on the OpenAI API now.

The trick is old and physical. Cerebras puts 44 GB of SRAM on a single wafer-scale chip, so the model weights stay on-chip instead of shuttling across memory hierarchies. Inference on large models is mostly a memory-movement problem wearing a compute costume, and if the weights never move, the bottleneck goes away. GPUs can't do this at that size, which is why nobody else's numbers look like this.

The demo that lands is Humanity's Last Exam. 2,500 PhD-level questions, answered in 11 hours, versus 78-plus hours for Claude Fable 5. On broadly economically valuable work tasks they measured 5.6x with no quality loss. An OpenAI researcher's line about it is the honest one: it finishes before I have the chance to context-switch.

That sentence is the whole story, and it's not about convenience. Every agent product built in the last two years is designed around the assumption that an agent run is something you kick off and come back to. Async queues, notifications, dashboards to watch progress, cockpits, the entire supervision layer. All of that infrastructure exists because agents are slow. At 750 tokens a second an agent stops being a background job and becomes a synchronous tool, which means it can sit on the critical path of a production outage or a security response, where waiting eight minutes is not an option. A large chunk of the tooling being built right now is a workaround for latency, and latency is being solved.

Details at cerebras.ai/blog. Pricing hasn't been published.
