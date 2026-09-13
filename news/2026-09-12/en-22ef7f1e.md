---
title: "He Tried Three Ways to Beat LRU on Real Agent Traces and Lost All Three"
date: 2026-09-12
lang: en
source: https://clauday.com/article/22ef7f1e-11dd-44ba-8f76-a66758bca581
tags: [Infrastructure, Research, Benchmark]
---

# He Tried Three Ways to Beat LRU on Real Agent Traces and Lost All Three

> 来源 / Source: https://clauday.com/article/22ef7f1e-11dd-44ba-8f76-a66758bca581

Somebody replayed 68,266 real requests from 393 Claude Code sessions plus 23,608 Mooncake requests through a prefix-cache simulator, tried three separate ways to beat plain LRU eviction, and failed every time. He published the whole thing, including the failures, at https://github.com/gauravapiscean/agentic-kv-cache . 90 points on Hacker News, and it deserves more than that, because negative results with real traces are rarer and more useful than the positive results they're arguing with.

The three attempts were not naive. Hazard-based prediction of whether a session is still alive, a physically-modelled recompute cost instead of a proxy, and session-granularity eviction so a session's cache chain lives and dies together. All three are things the published KV-cache literature suggests should help. All three made it worse.

The reason turned out to be more interesting than the policy, which is also the reason several papers are optimizing the wrong thing. The literature mostly assumes a TTL-bound regime: entries expire on timers, waste comes from sessions that went idle and then came back. Real agent traffic is capacity-bound, and in his traces the TTL never fires at all, because capacity evicts everything first. His line is "when capacity binds, it dominates the TTL, and the recompute it causes looks nothing like the idle-session story." Concretely: 33.1 percent of recompute comes from requests arriving within 10 seconds of the previous one, versus 17.5 percent from gaps over 5 minutes. The median gap between requests is 2.1 seconds. Tool-calling loops are thrashing the cache, not abandoned chat windows, and at 2.1 seconds there is no signal to predict liveness from anyway.

There's a methodology landmine in here that everyone benchmarking cache policies should read. He notes that an offline oracle policy like Belady can come out looking worse than LRU if your harness doesn't refcount-pin in-flight cache chains, which silently biases the whole comparison. He also points out that two published papers benchmark against Continuum with its adaptive TTL replaced by a fixed 2s or 0.3s pin, which disables the exact mechanism that makes Continuum work. Comparing against a deliberately lobotomized baseline is how a field accumulates results that don't reproduce.

Two caveats worth keeping. The session arrival pattern is synthesized, and the results are explicitly scoped to capacity-constrained deployments with session-local hash namespacing, not to every agentic setup. And the HN thread spent real energy on the fact that the ablations were LLM-assisted and the prose has a recognizable Claude cadence, which is a fair thing to notice and a bad reason to dismiss trace data. Put this next to [the RTK token-savings debunk](https://clauday.com/article/7d06a720-8150-4bd1-be47-1778c3923045) and [Spotify's 90 percent cut](https://clauday.com/article/06680400-cec6-4460-81de-6db3aef7bcd3) and the pattern is consistent: the agent-infrastructure claims that survive contact with real traffic are the ones where somebody published the dollar number and the failures.
