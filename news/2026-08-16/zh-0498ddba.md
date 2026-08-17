---
title: "AI 额度有个灰市，比你想的大"
date: 2026-08-16
lang: zh
source: https://clauday.com/zh/article/0498ddba-6a25-4514-8749-8b2a2d4c7054
tags: [Infrastructure, API, Monitoring]
---

# AI 额度有个灰市，比你想的大

> Source: [clauday.com](https://clauday.com/zh/article/0498ddba-6a25-4514-8749-8b2a2d4c7054)

终于有人把 AI 额度转卖市场摸了一遍，文章这个周末冲上了 Hacker News 首页。一句话版本：没用完的 OpenAI、Anthropic、Google、微软额度正在以三到八折转卖，而且量大到不能忽略。

供给端是创业公司额度。每个加速器、每个云厂扶持计划都在发五位数六位数的 API 额度，大部分公司根本烧不完。以前这些是在创始人群里私下换，现在已经是一个分层市场了。直接掮客把 key 池起来卖调用权——有人号称能吃下每天十万美元的消耗。还有 AI Credits、AICreditMart 这种正经交易平台。再往下是 CheapCredits、Tokvana、Neokens 这类打着"批量定价"旗号的路由站，作者怀疑它们其实就是穿了件好看衣服的额度贩子。最底下是 Telegram 群、r/saasforsale、r/indiehackers。作者见过的挂单里有 20 万美元的 OpenAI 额度和 1 万美元的 Anthropic 额度。

注意直接掮客的结构：他们不把 key 给你，而是让你的调用走他们池化的 key 做代理。也就是说你的 prompt、你的数据、你 agent 的全部流量，都跑在一个陌生人的基础设施上。要是你好奇为什么会有人把 agent 架在这上面——答案是七折的折扣，和一个盯着现金流的创始人。

文章里值得抄走的一句："token 已经变成了一种准货币，而且市场上的流动性足以支撑大量滥用。"这才是真正的发现。额度当初被设计成一种营销补贴，现在它有成交、有清算、有买卖价差。

这跟我们反复写过的一件事连上了——没人能独立核实一次 agent 运行到底花了多少钱。原来这不只是记账问题。当成本单位变得可互换、可交易，它就不再是一张账单，而是一个有黑市的资产。https://vectoral.com/blog/who-are-the-token-brokers
