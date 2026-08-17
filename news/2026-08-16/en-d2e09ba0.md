---
title: "MathCode Turns Your Terminal Into a Lean 4 Proof Machine"
date: 2026-08-16
lang: en
source: https://clauday.com/article/d2e09ba0-bf8c-4a2b-b010-a88954a62327
tags: [Coding, Open Source, Agents]
---

# MathCode Turns Your Terminal Into a Lean 4 Proof Machine

> Source: [clauday.com](https://clauday.com/article/d2e09ba0-bf8c-4a2b-b010-a88954a62327)

Team Math-AI released MathCode, a terminal coding agent with a math formalization engine bolted in. You state a problem in plain language, it turns it into a Lean 4 theorem, and then it tries to prove it. 619 stars, built on their earlier AUTOLEAN work, and it landed on Hacker News over the weekend.

The engineering detail that makes it usable is the persistent Lean REPL. Lean's compile cycle is what kills agentic proving — every check costs about 30 seconds, and an agent that iterates fifty times has burned 25 minutes waiting. MathCode warms the REPL once for roughly 90 seconds, and every check after that takes about 0.4 seconds. That's not an optimization, that's the difference between the loop being possible and not.

Around that sit the pieces you'd want: a theorem library that stores and reuses what it has already proven, an axiom library for formalizing assumptions you stated in conversation, LSP integration so it can actually find relevant lemmas instead of guessing names, tree-of-subgoals decomposition for proving branches in parallel, and multiple planners running different proof strategies at the same time. It'll also generate an Obsidian vault visualizing how your theorems depend on each other.

Why this is more interesting than a math tool. Formal proof is the one domain where an agent gets a perfect, instant, non-negotiable verifier — Lean either accepts the proof or it doesn't, no judge model, no rubric, no vibes. Everyone chasing self-improving agents is starving for signal that clean. Here it's free.

The bet worth watching is whether the harness patterns that work here — parallel subgoals, a reusable proof library, multiple competing planners — transfer to domains where the verifier is a test suite instead of a type checker. https://github.com/math-ai-org/mathcode
