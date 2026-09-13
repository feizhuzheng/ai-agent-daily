---
title: "DeskcommCRM Is a WhatsApp Sales Team That Ships Twice a Day"
date: 2026-09-12
lang: en
source: https://clauday.com/article/9bbce7b3-9f8b-423f-b1a0-234f01fadb53
tags: [Open Source, Agents, Tool]
---

# DeskcommCRM Is a WhatsApp Sales Team That Ships Twice a Day

> 来源 / Source: https://clauday.com/article/9bbce7b3-9f8b-423f-b1a0-234f01fadb53

DeskcommCRM took 505 stars in a day and is at 1,761 total, which is a decent trending run, but the number that actually made me look was the release history: v1.18.0, v1.18.1 and v1.19.0 all shipped on September 11, with 1.20.0 merged on the 12th. Four releases in two days. Repo at https://github.com/melgarafael/DeskcommCRM .

What it is: a self-hosted open-source CRM with AI agents built in and WhatsApp as the primary channel, via WAHA. It is MCP-ready, multi-tenant, and it explicitly bills itself as an open alternative to Kommo, Octadesk and Intercom for businesses that sell through chat. Being LGPD-compliant is listed as a feature, which is the giveaway about where this comes from and who it's for: Brazil, where an enormous share of real commerce runs through WhatsApp conversations and the incumbent tools are foreign SaaS priced in dollars.

That framing is why this is more interesting than "another CRM with a chatbot." Most agent-CRM products in the US are trying to automate a sales motion that happens over email and calendar invites. This one is built for a market where the sales motion is already a chat thread, which means the agent isn't bolted onto a workflow, it's native to the medium. Self-hosted plus multi-tenant also means an agency can run it for thirty small clients on one box, and that's a distribution model the SaaS incumbents structurally can't match on price.

Go in with your eyes open. WAHA is an unofficial WhatsApp automation layer, and building a business on unofficial access to Meta's messaging platform is a known category of risk that no amount of open source fixes. A repo created in April 2026 shipping four releases in two days is moving fast in both senses, and there's no audit, no stability guarantee, and the compliance claim is the project's own. Read the AI agent code before you point it at a real customer list.

Still, it's a good reminder that the agent story is not only happening in coding tools and research harnesses. The largest deployment surface for sales agents on earth is probably a WhatsApp inbox in a country that isn't the US, and the thing serving it is a self-hosted repo shipping twice a day.
