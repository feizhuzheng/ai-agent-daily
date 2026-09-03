---
title: "Gemini 3.8 Flash：六周第三发，还带了个网安特供版"
date: 2026-09-02
lang: zh
source: https://clauday.com/zh/article/9bbb73f1-52f6-42d3-b078-43a25a14caa1
tags: [Agents, Coding, Infrastructure]
---

# Gemini 3.8 Flash：六周第三发，还带了个网安特供版

> 来源 / Source: https://clauday.com/zh/article/9bbb73f1-52f6-42d3-b078-43a25a14caa1

Google 9 月 2 日发了 Gemini 3.8 Flash，距离 3.7 Flash 只有三周，六周内第三个 Flash 版本。现在它是 Google 官方推荐的软件工程、自主 agent 和多步推理模型。这个节奏本身就是信息：Flash 是 Google 迭代最快的线，而且明确瞄着 agent 负载打。

定价里有个坑，值得多读一遍。输入每百万 token 0.75 美元、输出 3.75 美元——但这是促销价，只到 12 月 31 日。1 月 1 日起翻倍，变成 1.50 和 7.50。模型 API 搞首发促销价是个新玩法：先用低价让开发者把它接进 agent 里，等切换成本真实存在了再恢复原价。三周前 3.7 Flash 价格砍半的时候我们叫它价格战，现在看其实是促销：https://clauday.com/zh/article/19079738-4585-4b7d-bb92-eb0028b96548

更有意思的是 Gemini 3.8 Flash Cyber，一个专门调过漏洞发现和自动修补的变体，只通过 Google Fairwind 开放——一个面向政府和可信伙伴的新准入计划。Google 说它生成的 Chrome 漏洞补丁正确数量是更大的商业模型的 2.6 倍。Anthropic 把 Mythos 锁在审核准入后面，Google 把 Cyber 锁进 Fairwind，一周之内两家 lab 给出了同一个答案：危险能力单独出一个版本，凭名单进。

HN 讨论已经 700 多分：https://news.ycombinator.com/
