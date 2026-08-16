---
title: "CLI-Anything: stop teaching agents to click, generate them a command line instead"
date: 2026-08-15
lang: en
source: https://clauday.com/article/27ecca38-8f6e-4802-8552-cd526894ad3f
tags: ["Agents", "Agent-Operable", "Open Source"]
---

# CLI-Anything: stop teaching agents to click, generate them a command line instead

来源 / Source: https://clauday.com/article/27ecca38-8f6e-4802-8552-cd526894ad3f

Agents are bad at professional software, and everyone has quietly agreed to work around it in three unsatisfying ways. Drive the GUI with vision, which breaks the moment a button moves. Use whatever public API exists, which covers maybe a fifth of what the app does. Or reimplement a toy version of the software and pretend that's the same thing. HKUDS looked at all three and picked a fourth: generate a real command line against the real backend. CLI-Anything is at https://github.com/HKUDS/CLI-Anything with 47.3k stars and an Apache 2.0 license.

The pitch is literally "Making ALL Software Agent-Native." It reads source or docs, then runs a seven-phase pipeline — analysis, design, implementation, test planning, test writing, documentation, publishing — and hands back an installable Python package. The CLIs are Click-based with JSON output, and each one ships in two modes: an interactive REPL for when an agent is in a session, and plain subcommands for when something is scripting it. That dual mode is not decoration. An agent mid-task and a cron job want opposite ergonomics from the same tool.

The number that makes this credible is 2,464 passing tests across 18-plus applications at a 100 percent pass rate, generated against the actual software rather than a mock. Recent additions include CLIs for Obsidian, Joplin, Calibre and QGIS, plus security hardening and work on CLI-Hub, the registry. The contributor list spans Claude Code, Codex, OpenClaw, Pi and others, which tells you people are running this from inside whatever harness they already live in.

What's clever is the choice of target. Everyone building the agent-computer interface layer has been reaching for either the browser or a protocol like MCP. CLI-Anything reaches for the oldest interface we have, and it has a real argument: a CLI is already text, already composable, already has a convention for structured output, and — unlike a GUI — its surface is enumerable. An agent can run help and know what exists. It cannot look at a screenshot and know what exists.

The honest limitation is that a generated CLI is only as complete as the source or docs it was generated from, and it inherits whatever the backend actually exposes. This doesn't conjure capability that isn't there. But for the enormous middle category of desktop software with a real engine and a GUI-only front door, this is the most direct path anyone has shown to making it agent-operable.
