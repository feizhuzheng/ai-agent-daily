---
title: "前沿Agent是优化器，不是研究员"
date: 2026-08-17
lang: zh
source: https://clauday.com/zh/article/be55c3ff-cee0-4c02-ad98-a950e666545b
tags: [Research, Benchmark, Agents]
---

# 前沿Agent是优化器，不是研究员

> Source: [clauday.com](https://clauday.com/zh/article/be55c3ff-cee0-4c02-ad98-a950e666545b)

Hugging Face今日论文榜40票："Beyond Final Scores: A Systematic Evaluation of Agents for Long-Horizon AI R&D"（arXiv 2608.13417，8月13日提交，13位作者，包括Fei Sun、Xunliang Cai和Jingang Wang）。实验设置：7个前沿模型，36个长周期AI研发任务，评估的不是最终榜单分数，而是用规则化指标刻画一次运行内部发生了什么，分三个维度：方案构思、执行、反馈控制。

结论就是这篇文章的标题：当前的前沿agent像工程优化器，不像自主研究员。它们能提出可行的方案，但跨运行方差很大；方案基本是对已有技术的改编，几乎不引入新东西；结果好坏取决于流程瓶颈、经验复用的质量，以及harness设计。

有两点让它超越了又一篇benchmark论文。第一，它直接证明了只看最终分数会掩盖什么：一个好的过程和一次走运产生的分数一模一样，而这个差别恰恰是你把一周长的任务交给agent之前必须知道的东西。不管你怎么看具体任务的选择，运行内指标本身就是贡献。第二，harness设计成为研发结果的决定因素，这个发现现在从每个方向涌来：DarwinX和AutoDesign通过优化harness得出这个结论，这篇论文把它当作混淆变量来测量，得出了同一个结论。如果你只用结果评估agent，你测的既是模型也是harness，而且分不清是哪个在拖后腿。

arxiv.org/abs/2608.13417
