---
title: "Superpowers now tells you to stop spawning subagents"
date: 2026-09-23
lang: en
source: https://clauday.com/article/a0bf74d3-dd66-4884-a52d-850a0a4515a9
tags: [Skills, Framework, Open Source]
---

# Superpowers now tells you to stop spawning subagents

> 来源 / Source: https://clauday.com/article/a0bf74d3-dd66-4884-a52d-850a0a4515a9

290,000 stars and it's still trending at 485 a day. Superpowers is the largest agent skills framework in existence by a wide margin, and v6.4.1 shipped last Friday with a change that reads like an admission.

The framework is a library of composable skills that fire automatically at the right stage of development. Brainstorming to refine a design, test-driven development in RED-GREEN-REFACTOR cycles, systematic debugging, plan execution, code review. The stated philosophy is systematic over ad-hoc, complexity reduction, and evidence-based verification instead of assumption. It runs across Claude Code, Cursor, Devin, Gemini, Copilot and a growing list, and 6.4.1 adds OpenCode 2.0, Muse, and Qwen Code. MIT licensed.

The interesting change in 6.4.1 is that plan execution was rebuilt around native inline execution as a cheaper alternative to subagent-driven development. For a year the default answer to a complex task has been: spawn subagents, give each a slice, collect the results. Superpowers has been one of the loudest implementations of that pattern, and it just shipped the opposite as an option and called it cheaper. Subagent dispatch has real costs — fresh context every time, handoff loss, coordination overhead — and those costs stop being worth it below some task size that nobody has pinned down. This release is one team's answer to where that line sits.

Two smaller things worth stealing. You now review the saved plan before anything runs, which is the correct place to put a human — before the work, not after it. And plans carry a Review Focus section calling out untested edge cases, which is the plan telling the reviewer where to look instead of making them find it.

There's also a diagnosing-superpowers skill for troubleshooting sessions that went wrong. A framework big enough to need a debugging skill for itself is a fact about the state of this whole category.

https://github.com/obra/superpowers
