---
title: "Cognition 的 SWE-2 跑在 Kimi K3 上，这才是重点"
date: 2026-09-10
lang: zh
source: https://clauday.com/zh/article/6ddeccb4-a6cb-4f02-adf2-a7aa229160dd
tags: [Coding, Agents, Benchmark]
---

# Cognition 的 SWE-2 跑在 Kimi K3 上，这才是重点

> 来源 / Source: https://clauday.com/zh/article/6ddeccb4-a6cb-4f02-adf2-a7aa229160dd

9 月 10 日 Cognition 发布 SWE-2，所有人会引用的数字是 Terminal-Bench 2.1 拿到 92.8，SWE-1.7 是 81.5。但真正的信息藏在下一段：底座模型是 Kimi K3，2.8 万亿参数，中国做的，开源权重。

一家估值 480 亿美元的美国编程 agent 公司，拿中国开源底座做后训练，然后在价格上把 GPT-5.6 Sol 和 Fable 5.1 干掉了。这不是脚注。这是目前为止最清楚的证据，说明前沿实验室的护城河是 RL 配方和 harness，不是预训练。Cognition 说这是第一次有人把强化学习扩到万亿级底座上。他们没花十亿美元走到这一步，他们租了月之暗面的地板。

效率数字才是真正的产品。SWE-2 平均比 SWE-1.7 少 58% 的步数，单任务成本低 81%，对上 Fable 5.1 时 FrontierCode 1.1 分数接近但便宜 64%。DeepSWE 1.1 从 37.7 直接到 73.0，这已经不叫进步，这是换了个模型在干别的事。Cognition 把整个发布定义成帕累托前沿的工作而不是天花板的工作，训练路线也对得上：他们优化的是"聚焦探索"，说白了就是让 agent 别在动手之前先把整个代码库读一遍。

Devin Desktop、CLI、Web、Fusion 都已经能用。原文在 https://cognition.com/blog/swe-2

尴尬的地方在于，Cognition 上周刚以"编程 agent 不是赢家通吃"的论点融了 20 亿 E 轮，SWE-2 证明他们对了，但同时也把所有把前沿预训练当差异化卖的人拆台了。如果一家两百人的公司拿开源中国底座就能以三分之一价格贴到实验室的脸上，问题就不再是谁的模型最好，而是谁的循环最好。

相关阅读：https://clauday.com/article/561e1701-0c51-4b6c-9258-ed27880c593a 和 https://clauday.com/article/34c36087-df55-4d0e-9295-6e4783bdfea9 和 https://clauday.com/article/1e40d5ed-8d73-49fc-b686-be744804935a
