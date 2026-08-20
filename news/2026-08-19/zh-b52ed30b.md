---
title: "Skill 是护栏，不是知识"
date: 2026-08-19
lang: zh
source: https://clauday.com/zh/article/b52ed30b-9bf4-4811-a26d-0d5a0239567a
tags: [Skills, Research, Benchmark]
---

# Skill 是护栏，不是知识

> Source: [clauday.com](https://clauday.com/zh/article/b52ed30b-9bf4-4811-a26d-0d5a0239567a)

现在所有人都在囤 agent skill：二十几万星的 skill 仓库、精选库、市场。这周标题起得最好的一篇论文，Demystifying Agent Skills: Why They Work, Until They Don't，跨基准、模型、框架跑了 8135 次试验，就为搞清楚 skill 到底在起什么作用。答案对囤积党不太友好。

Skill 有用，但不是大家以为的那种用法。在论文的定性编码里，65.7% 的成功案例来自"程序性锚定"——skill 像护栏一样稳住执行，让 agent 走在已知路径上。而 skill 名义上的卖点、显式知识注入，只占 4.5%。skill 没在教你的 agent 任何东西，它只是在扶着它走。

最狠的发现在检索。skill 池只有 5 个的时候，检索精度 29.6%，已经很难看；扩到 100 个，塌到 3.3%。再读一遍：库扩大 20 倍，选对 skill 的能力差了差不多 10 倍。而且调用"标准答案"的那个 skill，对任务成功既不必要也不充分。护城河不是库，是检索——而检索恰恰随着所有人都在扩的那个东西一起退化。

给所有在 skill 框架上盖房子的人，这篇论文等于一次免费审计：少而锚得牢的 skill 赢过大而全的收藏；真要大而全，你的检索层比你的 skill 更值得堆工程。论文在 https://arxiv.org/abs/2608.14036 ，HuggingFace 日榜 117 票。
