---
title: "Bullet is a coding agent that optimized the loop instead of the model"
date: 2026-08-13
lang: en
source: https://clauday.com/article/daf1077a-28ce-4d14-817c-5f933599ca3e
tags: [Coding, Agents, Tool]
---

# Bullet is a coding agent that optimized the loop instead of the model

> Source: [clauday.com](https://clauday.com/article/daf1077a-28ce-4d14-817c-5f933599ca3e)

Launch HN today: Bullet, a YC S26 coding agent whose entire pitch is that it's fast. Not smarter. Faster. The founders built it because they were burning hours waiting on agent runs while using Claude Code every day, and concluded the models were already capable and the surrounding machinery was the problem.

Three mechanisms do the work. Route and escalate sends easy steps to fast models and only escalates to a big model when the task actually earns it. Search and acquire does targeted code search to pull the handful of relevant files instead of shoveling the repo into context. And independent tool calls run in parallel rather than one at a time. None of that is novel individually. What's notable is a team treating latency as the product rather than a side effect, and claiming 95.8% on SWE-Bench Verified while doing it.

The routing point deserves attention because it cuts against how most harnesses are built. The default today is to send everything to the strongest model available, because it's simpler and nobody gets fired for it. But a hundred-turn agent run is mostly boring: reading a file, checking a path, running a test. Paying frontier prices and frontier latency for a directory listing is the industry's most expensive habit, and Bullet is a bet that a real router beats a bigger model on both wall-clock and cost.

Interesting timing. This lands the same day Cerebras announced 750 tokens per second for GPT-5.6 Sol, which attacks the same complaint from the hardware side. Two paths to the same destination: agents that answer while you're still paying attention. If the hardware path wins outright, orchestration cleverness gets a lot less valuable. If it stays expensive and preview-only for a while, Bullet's approach is the one most teams can actually afford.

Private beta, free for now, no subscription. macOS and Linux, CLI or direct download, at codewithbullet.com.
