---
title: "workweave router: The Routing Gold Rush Gets a Self-Hosted Entry"
date: 2026-08-29
lang: en
source: https://clauday.com/article/2ae2ce24-762f-482d-a239-7e1a7e5827c6
tags: ["Infrastructure", "Tool", "Agents"]
---

# workweave router: The Routing Gold Rush Gets a Self-Hosted Entry

来源 / Source: https://clauday.com/article/2ae2ce24-762f-482d-a239-7e1a7e5827c6

workweave/router is climbing GitHub trending today, up 284 stars to 2.7k. The pitch: one endpoint, every model, always the right one. It's a drop-in proxy that speaks Anthropic Messages, OpenAI Chat Completions and Gemini native, routes each individual action to the optimal model within 50 milliseconds, and claims to cut costs 40 to 70 percent from an endpoint change alone.

The technical bit worth noting: it doesn't route on hand-written heuristics. It uses an embedded cluster scorer derived from the Avengers-Pro research, scoring per action rather than per conversation. It plugs into Claude Code, Codex, opencode and Cursor, keeps provider keys encrypted locally, ships OTLP tracing, and self-hosts with Docker and Postgres. Written in Go. One caveat: it's Elastic License v2, source-available, not open source.

Count the routing entrants this month alone: Stripe bought OpenRouter for $7B, Ramp built a router, IQ Routing launched on Product Hunt, HarnessRouter went community edition, freellmapi arbitrages free tiers. Everyone has done the same math: frontier models are the most expensive line item in any agent stack, and most actions don't need the frontier. Routing is where that arbitrage becomes a product. The question for workweave is why anyone picks a 2.7k-star router over the one Stripe now owns — self-hosting and per-action scoring is their answer.

Repo: https://github.com/workweave/router
