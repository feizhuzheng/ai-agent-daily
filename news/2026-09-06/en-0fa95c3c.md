---
title: "Dial Gives Your Agent a Phone Number — and Reads Its Own OTPs"
date: 2026-09-06
lang: en
source: https://clauday.com/article/0fa95c3c-7d31-4a2e-b433-e3538ac26b45
tags: [Tool, Agent-Operable, API]
---

# Dial Gives Your Agent a Phone Number — and Reads Its Own OTPs

> 来源 / Source: https://clauday.com/article/0fa95c3c-7d31-4a2e-b433-e3538ac26b45

Dial (https://getdial.ai, on Product Hunt at https://www.producthunt.com/products/dial-3, #5 today with 232 upvotes) does one thing: a single API call provisions a real phone number for an AI agent in about ten seconds. On that number the agent can place and receive voice calls with live transcription, send SMS in 200+ countries, and message over iMessage with automatic RCS/SMS fallback. REST API, CLI, SDKs, and an MCP server, so it drops into existing agent stacks directly. Built by Gal Dayan and Omri Ben-Shoham; free credits to start, no card required.

The feature that actually matters is smaller than the telephony: Dial extracts verification codes from inbound messages. Phone-gated signup is the wall where nearly every autonomous workflow stops dead and hands back to a human. With an agent that owns a number and reads its own OTPs, that wall is simply gone — the agent signs up for services end to end, alone.

This is a category, not a product. Y Combinator already has AgentPhone pitching "phone numbers for AI agents," and more will follow, because when two startups sell the same primitive it's infrastructure. Every hard human-verification boundary — CAPTCHA, email, phone — eventually gets an agent-shaped API punched through it; phone was just the most expensive one.

Which is also the uncomfortable read. OTP walls exist precisely to prove a human is present. Making them machine-passable for a few dollars a number is the entire value proposition and the entire problem in one feature: every anti-bot system that relies on phone verification just silently became decorative. Fraud and trust-and-safety teams will notice, and this category will end up with rules on it. Right now it's the wild interval in between — which is exactly when infrastructure gets adopted.
