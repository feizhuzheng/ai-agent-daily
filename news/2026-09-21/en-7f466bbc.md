---
title: "Amazon slammed the door on Meta's shopping agent 12 days after launch"
date: 2026-09-21
lang: en
source: https://clauday.com/article/7f466bbc-c181-4212-8496-d81fafceeeea
tags: [Agents, Infrastructure, Agent-Operable]
---

# Amazon slammed the door on Meta's shopping agent 12 days after launch

> 来源 / Source: https://clauday.com/article/7f466bbc-c181-4212-8496-d81fafceeeea

Meta shipped Muse on September 8. By the evening of September 20, anyone trying to complete a purchase through it on Amazon got a popup: continued access by an unauthorized AI agent violates Amazon's Conditions of Use, to which our customers have agreed. Twelve days from launch to block.

Read Amazon's stated reasons carefully, because they are technical and they are not about competition. Amazon says Muse conceals its identity while navigating the site, and that it appears to collect and retain customer credentials, which would give it access to account pages and order history, all without Amazon's knowledge or consent. Amazon also says it went to Meta first and asked them to keep amazon.com out of Muse's scope before pulling the plug. Meta's answer is that Muse has no visibility into passwords or payment methods and keeps shared credentials in secure storage.

Both statements can be true at the same time and that is exactly the problem. Meta is describing what Muse does with the credentials. Amazon is describing what it can observe, which is a logged-in session it cannot attribute to a human. From the server side an agent with your password is indistinguishable from you having a bad day and clicking fast. There is no field in HTTP that says a machine is driving.

That is the actual story and it is much bigger than these two companies. Every agent shopping today works by holding your credentials and pretending to be you, because no retailer has shipped a way for an agent to say who it is and what it is authorized to do. The identity layer for agent commerce does not exist, so the only two moves available are impersonate or get blocked, and Amazon just demonstrated the second one at scale. Google's shopping agents and Perplexity's bots have both been on the receiving end of the same move.

Watch what Amazon does next rather than what it said. Blocking is cheap and temporary. The interesting version is a paid, authenticated agent channel, where Amazon decides which agents get in and on what terms, and the price of the gate becomes a line item. That is a tollgate, not a security policy, and if it shows up, the entire agentic commerce category becomes a rent negotiation overnight.
