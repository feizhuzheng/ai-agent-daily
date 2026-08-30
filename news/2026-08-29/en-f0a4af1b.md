---
title: "WikiSkill: Give the Agent a Wiki, Not Just Skills"
date: 2026-08-29
lang: en
source: https://clauday.com/article/f0a4af1b-3eeb-49fd-ae6c-bfb21e7d7df2
tags: ["Research", "Skills", "Agents"]
---

# WikiSkill: Give the Agent a Wiki, Not Just Skills

来源 / Source: https://clauday.com/article/f0a4af1b-3eeb-49fd-ae6c-bfb21e7d7df2

WikiSkill is a new paper on skill evolution with a clean core idea: when agents learn from experience, don't compress everything into skills. Keep three separate layers — raw execution experience, accumulated knowledge consolidated into a persistent wiki, and executable skills — and let the wiki and the skills evolve together. Insights that don't fit neatly into any single skill stop evaporating between training rounds.

The results back the architecture. WikiSkill consistently beats existing skill-evolution baselines across benchmarks, and two findings stand out. First, skills transfer across models and model families — knowledge compiled by one model works under another, which is exactly the property you want if skills are becoming a vendor-neutral format. Second, small models plus evolved skills can match substantially larger models running bare. The skill library is doing work you'd otherwise pay for in parameters.

This lands on what's become the hottest question of the season — how agents turn experience into reusable capability, alongside SkillEvo, TaoLive's harness-aware training, and yesterday's harness papers. The emerging consensus: a flat pile of skills isn't enough, you need a knowledge layer above it. Which is roughly the moment personal knowledge management arrived at for humans, twenty years ago.

Paper: https://arxiv.org/abs/2608.27454
