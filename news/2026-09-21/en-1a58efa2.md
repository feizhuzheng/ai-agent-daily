---
title: "ai-memory lets you quit Claude Code mid-task and finish it in Codex"
date: 2026-09-21
lang: en
source: https://clauday.com/article/1a58efa2-0ff8-41a4-8bd9-220e38156d9f
tags: [Agents, MCP, Open Source, Tool]
---

# ai-memory lets you quit Claude Code mid-task and finish it in Codex

> 来源 / Source: https://clauday.com/article/1a58efa2-0ff8-41a4-8bd9-220e38156d9f

The pitch for ai-memory is a scenario, and it is a good one: quit Claude Code mid-task, start OpenAI Codex in the same directory, continue without re-explaining the architecture. It picked up 217 stars today on the way to 7.6k, written in Rust, MIT licensed, at github.com/akitaonrails/ai-memory.

Architecturally it is one self-contained binary running an MCP and HTTP server over a local data directory. Agents write observations through lifecycle hooks, those get consolidated into markdown wiki pages, and retrieval happens through full-text search, entity matching, and optional embeddings. The line that should make you sit up: it works with zero LLM calls by default. No summarization tax, no model in the write path, write ceiling around 700 per second.

The storage decision is the whole design. Memory lives in a git-backed wiki of ordinary markdown files. You can grep it, open it in Obsidian, edit it by hand, and see every change as a commit. Compare that to the normal shape of agent memory, which is an opaque vector index you cannot read, cannot correct, and cannot diff. Half the agent-memory failures people complain about are really just memory you were never allowed to look at.

Twenty-plus harnesses are supported through either MCP registration or lifecycle hooks, including Claude Code, Codex, Cursor, Gemini CLI, OpenCode, Grok, Devin and Kimi. Version 1.39 and up handles multiple agents working the same project out of the box. That integration list is the actual product. Every vendor is currently shipping its own memory, scoped to its own tool, which means your accumulated context is a lock-in mechanism nobody calls by that name.

What this is really arguing is that memory belongs to the repository, not to the harness. If your project's understanding lives in a git-versioned directory next to the code, switching agents costs nothing, and the vendor no longer owns the most valuable thing you produced while using it. That is a small piece of software making a large claim, and it is a claim every coding-agent vendor has a reason to dislike. https://github.com/akitaonrails/ai-memory
