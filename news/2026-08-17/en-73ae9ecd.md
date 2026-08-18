---
title: "ai-memory: One Memory for Every Coding Agent You Run"
date: 2026-08-17
lang: en
source: https://clauday.com/article/73ae9ecd-2f23-48e7-ae06-dcf675122302
tags: [Open Source, Agents, MCP]
---

# ai-memory: One Memory for Every Coding Agent You Run

> Source: [clauday.com](https://clauday.com/article/73ae9ecd-2f23-48e7-ae06-dcf675122302)

Trending on GitHub today, up 207 stars: ai-memory by Fabio Akita (akitaonrails), a single Rust binary, MIT licensed, that gives coding agents persistent memory and, more interestingly, lets you hand off between vendors. It hooks into agent lifecycle events, prompts, tool calls, session boundaries, and compiles those observations into a git-versioned markdown wiki, indexed by SQLite with full-text search, entities and optional embeddings, served over MCP and HTTP. When a session ends, observations become a summary; the next agent, whether Claude Code, Codex or another CLI, starts with "where you left off." github.com/akitaonrails/ai-memory

The design choice worth stealing is compile, don't retrieve, borrowed from Karpathy. Instead of storing raw transcripts and searching them at recall time, it synthesizes coherent pages, decision records, session summaries, from the observation stream. A memory you can read is also a memory you can audit and edit, and markdown files in git are the most boring possible storage, which is exactly why they work: diffable, portable, vendor-neutral. It even runs without any LLM at all, falling back to full-text and entity search.

The cross-vendor handoff is the real product. Every harness now has its own resume feature and none of them talk to each other, while actual usage increasingly means running two or three agents on the same codebase. The memory layer keeps arriving from every direction this month, DeepSeek Harness's append-only session log, holaOS's editable memory files, and MobileMem benchmarking it on the research side today. Everyone has concluded the same thing: context windows forget, so the system around the model has to remember.
