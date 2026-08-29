---
title: "Anthropic 放出自动研究员，10 个对齐基准全部修复"
date: 2026-08-28
lang: zh
source: https://clauday.com/zh/article/24afabcc-c1fc-4bb2-93fe-9354c61979c7
tags: ["Research", "RL", "Agents"]
---

# Anthropic 放出自动研究员，10 个对齐基准全部修复

来源 / Source: https://clauday.com/zh/article/24afabcc-c1fc-4bb2-93fe-9354c61979c7

Anthropic 发了一篇论文，标题叫"Automated Researchers Can Reliably Mitigate Alignment Failures"，结果比标题更直接：给定 10 个衡量特定失准行为的基准，自动研究系统把每一个都改善了，而且没有损害模型的整体能力。TechCrunch 报道在 https://techcrunch.com/2026/08/28/an-anthropic-researcher-just-gave-us-a-peek-at-self-improving-ai/。

这个循环由 Anthropic fellow Chen Yueh-Han 主导，长得就像人类研究员工作流的压缩版：查文献、提方法、按这个方法训练模型 30 分钟、看基准动没动，有效的留下、无效的扔掉，然后继续。30 分钟训练是关键设计——短到能大规模跑循环，长到足以把数字挪动。论文自己的结论是："自动化对齐后训练可能在近期变得实用。"

有意思的是哪个问题先被自动化了。标准的递归自我改进叙事是：能力一骑绝尘，安全工作停留在手工作坊、永远缺人。这篇是反向数据点：自我改进循环第一次可靠地用在了对齐本身上，可靠到可以发论文。如果修一个行为异常的模型最便宜的办法变成"把自动研究员指过去跑一晚上"，安全工作的经济学就变了——它不再是用稀缺研究员工时支付的税，而是和其他一切用同一个速度复利。

相关阅读：AI agent 在开放数学问题上刷新五项纪录 — https://clauday.com/zh/article/ff1af608-91d9-416b-a0ba-656d9737d1b6
