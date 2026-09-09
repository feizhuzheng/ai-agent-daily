---
title: "2.8T Parameters, Four SSDs, One Token per Second"
date: 2026-09-08
lang: en
source: https://clauday.com/article/ca7fd597-8ae5-40fc-997a-97b01da6bdbd
tags: [Open Source, Infrastructure]
---

# 2.8T Parameters, Four SSDs, One Token per Second

> 来源 / Source: https://clauday.com/article/ca7fd597-8ae5-40fc-997a-97b01da6bdbd

Someone is running Kimi K3 - a 2.78 trillion parameter MoE whose expert weights alone are about 1.45TB - on a MacBook Pro. At one token per second. The trick, in the deltafin fork published September 8 (HN front page, 149 points): stream expert weights straight off four external SSDs using pread with F_NOCACHE, exploiting the fact that only 16 of 896 experts fire per layer. The M5 Max never holds the model; it holds the working set.

The author is upfront in the HN thread about what this is and isn't. One token per second is useless for chat. But that's the wrong frame: it's not a chatbot, it's an overnight batch machine. Queue up an agent job before bed, wake up to a few thousand tokens of frontier-open-weight output that never left your desk. For anyone whose constraint is data residency rather than latency, that's a real category.

It also extends the substrate story we've been tracking: OpenAI buys Mac minis by the tens of thousands for agent workloads (https://clauday.com/article/170b30b0-4330-4bfe-a29a-ab06b9df5a17), oMLX made local coding agents tolerable (https://clauday.com/article/99ad10c7-4e6f-4d83-9545-cd8c8e25d969), and now the hobbyist frontier is "how big a model can physically pass through my USB-C ports." The answer keeps going up faster than anyone budgeted.

Repo: https://github.com/argonautlabsai/deltafin
