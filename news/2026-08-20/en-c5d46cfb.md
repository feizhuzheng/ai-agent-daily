---
title: "SemaPLC: The Agent Harness Walks Onto the Factory Floor"
date: 2026-08-20
lang: en
source: https://clauday.com/article/c5d46cfb-15dd-41d4-a2f5-7195632dcc58
tags: [Agents, Infrastructure]
---

# SemaPLC: The Agent Harness Walks Onto the Factory Floor

> Source: [clauday.com](https://clauday.com/article/c5d46cfb-15dd-41d4-a2f5-7195632dcc58)

PLCs are the computers that run factories, assembly lines, water treatment, HVAC. Code that is wrong does not throw an exception, it moves physical machinery the wrong way. SemaPLC, at 110 upvotes on HuggingFace's daily board, is an agent harness for generating PLC code, and it comes from Midea, the appliance giant that owns robot maker KUKA, which means the people publishing it run actual factories.

The architecture will look familiar to anyone following the harness pattern: never trust the model's self-assessment, gate everything through external verification. Generated code must pass three gates, specification compliance, compilation, and runtime behavior verified on live PLC systems. The paper's motto is the thesis of the whole current wave: execution, not static scoring, is the faithful test. Across seven models on 117 tasks, the harness achieves a 72.6 percent mean verified pass rate, and on the harder project-context tasks, where new code has to integrate with an existing codebase, it hits 52.2 percent on dynamic behavior against baselines stuck at 22 to 31 percent.

Read those numbers both ways. The harness more than doubles baseline performance, and it still fails nearly half the time on realistic tasks, which in industrial automation means the human stays in the loop for the foreseeable future. But the same was true of coding agents two years ago.

The larger point is who is publishing. Verification-gated harnesses were a software-industry pattern; a manufacturer applying it to the code that moves physical machines, and open-sourcing the result, says the pattern is escaping the software industry. Code is at github.com/midea-ai/SemaPLC.

https://arxiv.org/abs/2608.18565
