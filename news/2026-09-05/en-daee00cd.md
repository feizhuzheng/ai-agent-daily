---
title: "dif.sh Puts Feature Flags in Markdown, Where Your Agent Can Read Them"
date: 2026-09-05
lang: en
source: https://clauday.com/article/daee00cd-ed98-4a61-b27c-e5b5440db1bc
tags: [Tool, Coding, Agent-Operable]
---

# dif.sh Puts Feature Flags in Markdown, Where Your Agent Can Read Them

> 来源 / Source: https://clauday.com/article/daee00cd-ed98-4a61-b27c-e5b5440db1bc

Saturday's #1 on Product Hunt (323 upvotes) is dif.sh (https://dif.sh), which takes feature flags and A/B tests out of the SaaS dashboard and puts them in your repo as markdown files. Each experiment is one .md file — frontmatter carrying hypothesis, audience and variants, prose carrying the documentation — living in experiments/active/ until it graduates to experiments/concluded/. A CLI (dif new, validate, build, conclude) compiles everything into a typed client, catches conflicting experiments at build time through exclusion groups, and production never phones home to an external service. PR review replaces the approval workflow; git is the audit log.

The reason it launched now and won the day: agents. On session start a coding agent reads a generated context.json and inherits what every previous experiment learned. There are also per-surface markdown logs — this button has been tested four times, here is what moved — so the agent proposing your next UI change starts from institutional memory instead of rediscovering it.

That inheritance detail is the actual product. Every team running coding agents has the same silent failure: the agent redesigns something an A/B test already killed two quarters ago, because test results live in a dashboard the agent has never seen. Concluded experiments as files in the repo turn dead tests into guardrails.

Zoom out and this is the year's clearest pattern once again: skills became markdown, agent instructions became AGENTS.md, and now experiments follow. Everything that wants to survive contact with agents is migrating into the repo, because the repo is the only surface agents reliably read. Core is free and self-hosted; a paid cloud adds dashboards with confidence intervals.
