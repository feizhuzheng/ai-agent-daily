---
title: "workweave router：路由淘金热，又来一个能自部署的"
date: 2026-08-29
lang: zh
source: https://clauday.com/zh/article/af129df6-b6c1-45c6-8b68-94ca182348b1
tags: ["Infrastructure", "Tool", "Agents"]
---

# workweave router：路由淘金热，又来一个能自部署的

来源 / Source: https://clauday.com/zh/article/af129df6-b6c1-45c6-8b68-94ca182348b1

workweave/router今天冲上GitHub trending，单日涨284星到2.7k。卖点一句话：一个endpoint，所有模型，永远选对的那个。它是个即插即用代理，同时讲Anthropic Messages、OpenAI Chat Completions和Gemini原生三种方言，50毫秒内把每一个动作路由到最合适的模型，号称只改一个endpoint就能省40%到70%的成本。

技术上值得一提的是它不靠手写规则路由，而是内嵌了一个基于Avengers-Pro研究的聚类打分器，按单个动作打分，不是按整段对话。接Claude Code、Codex、opencode、Cursor都行，密钥本地加密，自带OTLP追踪，Docker加Postgres就能自部署，Go写的。要泼一盆冷水：协议是Elastic License v2，source-available，不算真开源。

数一数光这个月的路由玩家：Stripe花70亿美元买了OpenRouter，Ramp自己造了router，IQ Routing上了Product Hunt，HarnessRouter出了社区版，freellmapi在薅免费额度套利。所有人算的是同一笔账：前沿模型是agent技术栈里最贵的一行账单，而大多数动作根本用不着前沿模型。路由就是把这个套利做成产品。workweave要回答的问题是，凭什么选一个2.7k星的router而不是Stripe亲儿子——他们的答案是自部署加按动作打分。

仓库：https://github.com/workweave/router
