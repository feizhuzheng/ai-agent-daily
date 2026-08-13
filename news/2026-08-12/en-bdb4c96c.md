---
title: Macro open-sourced a whole workspace so agents can actually reach your work
date: 2026-08-12
lang: en
source: https://clauday.com/article/bdb4c96c-d087-4cd6-8f9a-8e561e843b97
tags: Agents, Open Source, MCP
---

# Macro open-sourced a whole workspace so agents can actually reach your work

> 来源 / source: [clauday.com](https://clauday.com/article/bdb4c96c-d087-4cd6-8f9a-8e561e843b97) · 2026-08-12

macro-inc/macro hit GitHub trending today: a unified workspace for teams bundling email, chat, docs, tasks, agents, calls and CRM, all @-linked with shared AI memory. Rust backend, SolidJS frontend, nearly 5,000 commits, AGPLv3. The README is pointed about it being fully open source and not open core, with commercial licensing available separately.

The design bet is that agents fail at work not because they are dumb but because the work is scattered across eight products that do not talk. Your agent can read the ticket but not the email thread that caused it, or the call where the decision was actually made. Macro's answer is to put all of it in one place with a shared memory layer synthesized across conversations, emails, tasks and calls, then expose the whole thing.

The details that matter are on the tooling side. MCP integration across multiple providers. A tool surface claiming near 100% coverage of what the UI can do — meaning an agent is not limited to a curated subset of actions, it can do anything a human sitting at the app could. No rate limits on MCP operations. And documents edit agent-natively through CRDT collaboration, so a human and an agent can be in the same doc at the same time without one clobbering the other.

The declaration that "issue tracking is dead" is the kind of line that ages badly, and consolidation plays like this have a long history of losing to good products that do one thing. But the tool-coverage argument is real and underappreciated. Most enterprise MCP servers expose a polite handful of read operations and call it integration, and then everyone is surprised when the agent cannot finish anything. Give it the whole surface or accept that it will keep handing work back to you.

https://github.com/macro-inc/macro
