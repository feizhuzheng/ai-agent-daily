---
title: "LycheeMemory V2：晚一点写，成本降 86%"
date: 2026-08-16
lang: zh
source: https://clauday.com/zh/article/847eec2b-7bc2-48b7-b885-d93ca304a3b0
tags: [Research, Agents, Infrastructure]
---

# LycheeMemory V2：晚一点写，成本降 86%

> Source: [clauday.com](https://clauday.com/zh/article/847eec2b-7bc2-48b7-b885-d93ca304a3b0)

几乎所有 agent 记忆系统都是每轮对话之后做一次固化。agent 说完一句，系统编码、建索引、归档。8 月 13 日挂出的 LycheeMemory V2，来自 Dongfang Li 带的一个中国团队，问了一个明显但没人问的问题：凭什么按轮？

他们的答案是改成按语义段固化。先检测一个话题到底在哪儿结束，然后把整段当成一个单位编码。昂贵的编码动作触发频率大幅下降，而且因为切分依据是意义不是消息条数，事件级和时间上的连贯性被保住了——那恰好是按轮切碎会毁掉的东西。记录再配上轻量的结构化索引，检索也不贵。

值得在意的是数字。LoCoMo 89.22%，LongMemEval-S 92.20%，跑在 GPT-4.1-Mini 上，不是前沿模型。跟 A-Mem 比，构建阶段的 token 在 LoCoMo 上降 86.0%，在 LongMemEval-S 上降 75.9%，而查询阶段的 token 没有增加。通常这类省成本的论文是拿写的成本换读的成本，这篇没有。

榜单之外为什么重要：记忆的写入成本是长时运行 agent 身上一笔隐形的税。单看一轮完全看不见，连续跑一周就很要命，而且它随 agent 说了多少话增长，不随它学到多少东西增长。在保住准确率的前提下砍掉 86%，意味着一整类原本算不过账的常驻 agent，现在算得过来了。

论文底下还有个朴素的教训。大部分系统按节拍固化，因为按节拍好写。按意义固化更难实现，但更便宜。https://arxiv.org/abs/2608.12990
