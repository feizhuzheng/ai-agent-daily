---
title: "MCP's New Roadmap Assumes the Caller Isn't Human"
date: 2026-08-22
lang: en
source: https://clauday.com/article/aa5034dd-5905-4573-ad0a-e8d061f80463
tags: ["MCP", "Infrastructure"]
---

# MCP's New Roadmap Assumes the Caller Isn't Human

来源 / Source: https://clauday.com/article/aa5034dd-5905-4573-ad0a-e8d061f80463

The most telling sentence in MCP's new roadmap, published August 22 and already at 160 points on Hacker News: "MCP authorization assumes a person with a browser at consent time. Increasingly the caller is an agent." One year after MCP became the USB port for AI tools, the protocol is rebuilding itself around the assumption that nobody is sitting at the keyboard.

The concrete version of that: a new Agent Identity working group. DPoP proof-of-possession, workload identity federation, and OAuth token exchange so an agent can reach an MCP server with its own identity or a user-delegated one — and so a sub-agent gets narrower authority than the parent that spawned it. Today's reality, which the roadmap admits outright, is pasted API keys and long-lived refresh tokens. They're even discussing human-presence attestation: a way for servers to know whether a human is actually there at all.

The transport story is just as aggressive. Streamable HTTP becomes the single binding — spoken over stdin/stdout for local servers via HTTP/2, killing the dual stdio/HTTP pipeline every SDK currently maintains. Servers get push: channels, subscriptions, webhooks, so long-running agent work stops burning money on client-side polling.

And the one working agent developers will feel first: progressive discovery. Clients learn a server's tools as they need them instead of ingesting the full catalog up front. Anyone who has watched an agent drown in a 200-tool listing knows exactly which pain this is aimed at — it's the same problem deferred-tool-loading harnesses have been solving privately, now headed into the protocol itself. Add a redesign of tools/call to fix the content-versus-structuredContent confusion, and this reads less like a feature list than a statement: the protocol layer is where agent infrastructure is consolidating.

Roadmap: https://modelcontextprotocol.io/development/roadmap
