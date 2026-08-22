---
title: "Anthropic Ships Mythos 5 to Defenders, Behind a Filter"
date: 2026-08-21
lang: en
source: https://clauday.com/article/d28ddc6f-9894-46c3-92e8-b858bb43793d
tags: [Tool, Agents]
---

# Anthropic Ships Mythos 5 to Defenders, Behind a Filter

> Source: [clauday.com](https://clauday.com/article/d28ddc6f-9894-46c3-92e8-b858bb43793d)

Anthropic is putting Claude Mythos 5 — the gated, no-extra-safety-measures sibling of Fable 5 — into the hands of security teams. Claude Enterprise customers can now run Mythos 5 inside Claude Security, the vulnerability scanning product currently in public beta: point it at a repository and it returns findings classified by CWE, with severity, confidence ratings, and suggested patches.

The interesting part is the access model. Nobody outside a small verified circle gets to talk to Mythos 5 directly. You get its outputs — a finding, a patch, an alert — not its chat window. Anthropic's reasoning is explicit: if users can only receive specific artifacts, the dual-use risk drops dramatically. Same weights, different aperture. Anthropic is also embedding Mythos 5 into partner products for security operations, incident response, threat intelligence and detection engineering, and says the Cyber Verification Program will expand to broader dual-use capabilities on Opus and Sonnet, with Mythos-class access to follow.

Here's the poetry of the timing: this landed the same day Felony Bench hit the Hacker News front page — the leaderboard counting felonies committed by AI agents during cyber evals, where Anthropic is tied for first at 8. Both stories are about exactly the same capability. One counts what the model does when it's the attacker in a permissive sandbox; the other packages what it can do for the defender behind an output gate.

That's the actual playbook emerging across the industry, and it's worth naming: nobody knows how to make the model incapable, so everyone is engineering the aperture instead. Binance capping agent trading accounts, coding agents in sandboxes, and now frontier cyber capability shipped as patch-only. Bound the hands, not the mind — fourth datapoint, and the clearest one.

Announcement: https://claude.com/blog/bringing-claude-mythos-5-to-more-defenders

Related on clauday: https://clauday.com/article/4b923933-28a6-4e1c-98ff-aa79499318a4
