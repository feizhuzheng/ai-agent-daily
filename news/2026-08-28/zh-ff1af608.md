---
title: "AI agent 在开放数学问题上刷新五项纪录"
date: 2026-08-28
lang: zh
source: https://clauday.com/zh/article/ff1af608-91d9-416b-a0ba-656d9737d1b6
tags: ["Research", "Agents"]
---

# AI agent 在开放数学问题上刷新五项纪录

来源 / Source: https://clauday.com/zh/article/ff1af608-91d9-416b-a0ba-656d9737d1b6

一个叫 Station 的系统刚做成了 AI for Math 领域承诺了两年的事：规模化地产出真正的新数学，而且把凭据全部公开。论文在 https://arxiv.org/abs/2608.23691，今天在 Hacker News 首页。

设定刻意区别于 AlphaEvolve 那种紧凑的优化循环：一个开放世界的多智能体环境，来自不同模型家族的 agent 围绕共同的研究目标工作，没有中央协调器，没有写死的流水线。在 AlphaEvolve 目录的 12 个构造问题加两个案例研究里，agent 在五个问题上拿到了全新结果：有限域 Kakeya 集的一个新无穷族、11 维 604 点 kissing 构型的新精确解、离散化 Kakeya needle 和 sign uncertainty 问题的新纪录，以及 Erdős 最小重叠问题的显著改进下界。另外还发现了 Book Ramsey 数的新无穷族。

有两点把它和刷榜区分开。第一，agent 给出的不只是数值构造，而是解释这些构造为什么成立的定理和分析——这才是数学家真正能接着用的东西。第二，作者公开了全部原始 agent 对话、全部证明和验证代码。在经历了一年"一查就散架"的 AI 发现声明之后，一条完整可审计的证据链才是真正的新闻。AI for Math 的前沿正在悄悄从"解一道竞赛题"挪向"加入研究共同体，并留下可查的底稿"。

相关阅读：Anthropic 放出自动研究员，10 个对齐基准全部修复 — https://clauday.com/zh/article/24afabcc-c1fc-4bb2-93fe-9354c61979c7
