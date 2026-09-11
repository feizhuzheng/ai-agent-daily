---
title: "AgentGrad 修的是多 agent 调试里所有人都在糊弄的那部分"
date: 2026-09-10
lang: zh
source: https://clauday.com/zh/article/ce334a0f-ee4d-4c24-bf88-58c0dee95f68
tags: [Research, Agents, Framework]
---

# AgentGrad 修的是多 agent 调试里所有人都在糊弄的那部分

> 来源 / Source: https://clauday.com/zh/article/ce334a0f-ee4d-4c24-bf88-58c0dee95f68

一个多 agent 系统给出了烂答案，是哪个 agent 干的？文本梯度这一类方法，就是把写出来的批评意见沿着 prompt 链反传的那类，基本上靠猜。AgentGrad 在 HuggingFace 论文页拿了 73 票，直接把这一点点名为核心缺陷，然后用一个朴素到有点尴尬的办法解决：一次只改一个 agent，看会发生什么。

他们管这叫序贯干预，本质是因果归因而不是相关性甩锅。扰动单个 agent，观察结果，你就知道这个 agent 是不是真的该负责，而不是从一条要穿过另外五个 prompt 才传到你这儿的批评意见里推断。第二个部件是语义抽象，把相似的修正模式归到一组，让优化器学到通用修法而不是背下某一条轨迹。论文明确点出了前人工作的两个失败模式：agent 定位不准，以及修正建议的分组没用。

结果是在五个多 agent 基准上达到当前最优，平均比第二快的基线快 2.5 倍。这个速度数字不是脚注。多 agent 系统的 prompt 优化通常贵到没人会在真实管线上跑，所以便宜的那个版本才是能用的版本。

arXiv 2609.08572，9 月 8 日提交，13 页，作者是 Jaewon Chu、Jinwoo Seo 等人，包括 Hyunwoo J. Kim。

任何上线过多 agent 管线的人都知道，今天真实的工作流就是盯着 trace 猜该动哪个 prompt。一个能自动做逐个消融的方法，是"凭感觉调"和"凭测量调"之间的区别，而且这个想法足够小，几个月内应该就会出现在各个 agent 框架里。
