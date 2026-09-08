---
title: "context-mode: Don't Show the Agent Its Tool Output"
date: 2026-09-07
lang: en
source: https://clauday.com/article/2580fddf-86b4-472a-8190-1adee6bccdd8
tags: [MCP, Infrastructure, Open Source]
---

# context-mode: Don't Show the Agent Its Tool Output

> 来源 / Source: https://clauday.com/article/2580fddf-86b4-472a-8190-1adee6bccdd8

Most of what kills an agent's context window isn't conversation — it's tool output. One fat grep, one verbose API response, and a third of the window is gone. context-mode, trending today with a fresh push on September 7 (20.8k stars), applies the obvious-in-retrospect fix: run tool output in a sandboxed subprocess, index it, and hand the agent a reference instead of the dump. The claim is up to 98% context reduction.

The other half is persistence. Session state goes into SQLite with FTS5, searched by BM25, and survives compactions — the thing where your agent summarizes its own history and loses the details it needs an hour later. It ships as an MCP server plus hooks, with support claimed across 17 platforms; Claude Code, Gemini CLI and OpenCode get full hook coverage. License is ELv2, worth noting before you build a business on it.

This is the same architectural conclusion the whole harness layer keeps arriving at from different directions: the context window is a scarce, expensive cache, not a scratch disk. caveman got there by making the agent talk less (https://clauday.com/article/6d20896b-bfb0-41ca-bf12-69c4eca17bd8); context-mode gets there by making it read less. Retrieval on demand beats hoarding in window, and the numbers — token bills, compaction losses — keep agreeing.

https://github.com/mksglu/context-mode
