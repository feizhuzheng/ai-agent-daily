---
title: "AI Code Is Exactly Twice as Sloppy, and Now There's a Number"
date: 2026-09-11
lang: en
source: https://clauday.com/article/accb0b58-0840-482e-b574-40738256cd2d
tags: [Benchmark, Coding, Research]
---

# AI Code Is Exactly Twice as Sloppy, and Now There's a Number

> 来源 / Source: https://clauday.com/article/accb0b58-0840-482e-b574-40738256cd2d

Everyone has the feeling that agent-written code rots faster. Sebastian at Earendil put metrics on it and the gap is almost comically clean: human repos score 0.15 verbosity and 0.31 erosion, AI-generated code scores 0.33 and 0.68. Twice as verbose, twice as eroded, on both axes, with tight enough error bars to mean something. Post is at https://earendil.com/posts/measuring-code-sloppiness/ , published September 10, and it took 221 points on Hacker News.

The three metrics are deliberately boring, which is what makes them usable. Lines of code, straightforward. Verbosity, measured with AST-Grep and clone detection to catch duplicated and unnecessarily long lines. Erosion, which combines cyclomatic complexity with source lines to detect complexity piling up inside a few large functions. None of this requires a judge model, none of it requires taste, and all of it runs in CI. That matters more than the specific thresholds, because the field has spent a year arguing about code quality using vibes and screenshots.

The evaluation design is the other useful part. Rather than a single-pass generation test, it borrows SlopCodeBench's setup: multiple rounds of instructions and tests with context erased between checkpoints, which simulates what actually happens when you come back to a codebase three weeks later with a fresh session. Under that regime state-of-the-art models hit a 0 percent strict pass rate. Zero. The code compiles and the tests pass individually, and the architecture still degrades.

The diagnosis is that agents cannot manage quality at scale, and the mechanism is unnecessary abstraction. An agent that cannot see the whole system defends itself locally by adding a layer, and forty local defenses become a codebase nobody can hold in their head. That is the same complaint the 906-point joke about spawning 23 agents to make a button blue was making, except this version has standard deviations. If you want one number to take into your next argument about whether to let agents write the whole service, 0.68 versus 0.31 is it.

Related reading: https://clauday.com/article/9926615f-43d9-49fe-b8d0-f012ad8fc7bd and https://clauday.com/article/ca0df2a7-714a-4d25-9a63-f669999d9e00
