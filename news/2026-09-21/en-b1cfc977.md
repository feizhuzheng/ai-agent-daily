---
title: "agent-native's bet: stop making your agent click buttons"
date: 2026-09-21
lang: en
source: https://clauday.com/article/b1cfc977-f5ce-4881-a778-3b4b8463bd7c
tags: [Agents, Framework, Open Source]
---

# agent-native's bet: stop making your agent click buttons

> 来源 / Source: https://clauday.com/article/b1cfc977-f5ce-4881-a778-3b4b8463bd7c

BuilderIO's agent-native jumped 607 stars in a day to 5,837, and the core idea is one sentence long: the agent does not click through the UI, it works through the same action layer as the UI. MIT licensed, TypeScript, at github.com/BuilderIO/agent-native.

Here is the mechanic. You define each capability once as an action. That single definition then shows up as an agent tool, a React component the UI calls from code, an HTTP endpoint, an MCP interface, and a CLI command. Their hello-world example is literally one action surfacing five ways. Everything the human can do, the agent can do, through the same door, with the same permission checks, and it is impossible for the two surfaces to drift apart because there is only one of them.

Compare that to how most agentic apps work today. You build a product, then you bolt an agent on by either giving it a browser and letting it hunt for buttons, or by writing a second parallel set of tool definitions that shadow your real API and rot the moment someone ships a feature. Computer-use agents exist precisely because software was built for eyes and hands. agent-native's answer is to stop building software that way.

The rest of the framework is the boring stuff you actually need in production and rarely get from a demo framework: PostgreSQL backing, auth and permissions, skills and memory, automations, multi-agent teams. The permissions bit is the one that earns its keep, because a shared action layer means the agent's authority is defined in exactly the same place as the user's, instead of being whatever the browser session happens to allow.

The honest caveat is that this only works for software you are writing from scratch or willing to restructure, which is not most software. But the trend line is clear and this is the cleanest artifact of it yet. Between this, MCP, and the agent-readable web push, the question every product team is about to face is not whether to add an agent, it is whether their app has an action layer at all or just a pile of React components with business logic smeared inside them. https://github.com/BuilderIO/agent-native
