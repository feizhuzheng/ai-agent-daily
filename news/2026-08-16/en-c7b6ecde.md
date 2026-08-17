---
title: "Anthropic's System Prompt Changelog Is Leaking More Than Prompts"
date: 2026-08-16
lang: en
source: https://clauday.com/article/c7b6ecde-b01d-4954-91c4-5468fadcb797
tags: [Agents, Research]
---

# Anthropic's System Prompt Changelog Is Leaking More Than Prompts

> Source: [clauday.com](https://clauday.com/article/c7b6ecde-b01d-4954-91c4-5468fadcb797)

Anthropic keeps a public page of the system prompts behind claude.ai and the mobile apps. It's been there a while, but it hit Hacker News' front page this weekend with 450 points and 196 comments, and reading the entries in order turns out to be a decent way to reconstruct what the company has actually shipped.

The current top entry is Claude Opus 5, dated July 24. Inside it: references to Claude Mythos Preview, available only to approved organizations through something called Project Glasswing. Also documented, plainly, is the suspension of Claude Fable 5 and Claude Mythos 5 from June 9 to July 1 under U.S. export controls. And product surfaces most people haven't touched — Claude Tag, the Slack interface, and Claude Design, the canvas and design tool interface.

There's a structural change worth noting too. Starting with the 4.6 generation, each model ID is a single frozen snapshot with exactly one system prompt entry. Older models have several dated entries because they got patched between versions. That's a real shift in how Anthropic ships: the prompt is now part of the model's identity rather than a config that drifts underneath you.

Note the scope line, because people keep missing it — none of this applies to the API. If you're building agents on the API, you get no system prompt unless you write one. The claude.ai prompt is a consumer product decision, not a model behavior spec.

Still, if you want to know how a frontier lab actually steers a model in production, this is the closest thing to primary source material anyone publishes. Most labs treat the system prompt as a trade secret. https://platform.claude.com/docs/en/release-notes/system-prompts
