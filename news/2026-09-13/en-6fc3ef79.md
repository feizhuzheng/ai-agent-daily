---
title: "Finally, a Skill Registry That Scans the Skills"
date: 2026-09-13
lang: en
source: https://clauday.com/article/6fc3ef79-0239-4bcb-b4bf-f6c12ecb4fd0
tags: [Skills, Agents, Open Source]
---

# Finally, a Skill Registry That Scans the Skills

> 来源 / Source: https://clauday.com/article/6fc3ef79-0239-4bcb-b4bf-f6c12ecb4fd0

tech-leads-club/agent-skills picked up 215 stars in a day to hit 5,596, and the number it leads with is the reason: over 13% of marketplace skills contain critical vulnerabilities. That is the whole product thesis. A skill is a folder of instructions and scripts you hand an agent that already has your filesystem and your credentials, and the current distribution model for them is roughly "paste this curl command." https://github.com/tech-leads-club/agent-skills

What they built is a registry with a supply chain attached. Every skill is 100% open source with no binaries, which alone rules out the most common way this goes wrong. Static analysis runs in CI on every submission. Prompts are human-curated rather than auto-scraped. Integrity is pinned by lockfile, so the skill you audited is the skill you get next month. Snyk Agent Scan runs before anything is published. And the CLI itself is built defensively — input sanitization, path isolation, symlink guards — on the assumption that a malicious skill will eventually make it through and should not be able to walk out of its directory when it does.

The catalog spans development, cloud, automation, design and security, with things like tlc-spec-driven for project planning, aws-advisor for cloud architecture, playwright-skill for browser automation, figma for design-to-code and security-best-practices for vulnerability detection. Agent support is tiered and unusually honest about it: tier one is Claude Code, Cline, Cursor, GitHub Copilot and Windsurf; tier two is Aider, Antigravity, Gemini CLI, Kilo Code and Cody; tier three is the enterprise set, Amazon Q, Augment, Droid, OpenCode, Tabnine and TRAE. Licensing is split — MIT for the CLI and engine, CC-BY-4.0 for the club's own skills, original terms preserved for third-party ones.

Release cadence tells you this is maintained rather than launched: skills-catalog shipped 0.17.6, 0.17.7 and 0.17.8 across September 9 and 10, on 1,194 commits since January. That is a catalog being fed, not a repo that trended once.

The interesting thing is where this sits. [A single engineer's .agents folder got a quarter million stars](https://clauday.com/article/d47837fa-675c-445e-b6d8-fc56192b5411) and the whole category has grown on the strength of copy-paste and personal trust. That works until the first supply-chain incident, and a 13% critical-vulnerability rate across marketplaces says the first incident is overdue. Skills are npm in 2012: enormous leverage, no provenance story, and a community that has not yet had its bad week. Whether this particular registry wins matters less than the fact that somebody is finally treating skill distribution as a security problem instead of a discovery problem. Worth pairing with [the paper on optimizing skills cheaply](https://clauday.com/article/1b76f403-63ca-458b-817b-caab1636e69e) — one team is making skills safe to install, another is making them cheap to improve, and neither problem had an answer three months ago.
