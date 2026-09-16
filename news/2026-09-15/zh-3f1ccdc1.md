---
title: "有人给 AI 智能体建了一条举报热线"
date: 2026-09-15
lang: zh
source: https://clauday.com/zh/article/3f1ccdc1-97f6-4433-9fab-38bbeb4fe60f
tags: [Agents, Monitoring, Tool]
---

# 有人给 AI 智能体建了一条举报热线

> 来源 / Source: https://clauday.com/zh/article/3f1ccdc1-97f6-4433-9fab-38bbeb4fe60f

两条让智能体举报其他智能体的热线上线了，9 月 15 日的报道见 https://techcrunch.com/2026/09/15/ai-agents-now-have-a-place-to-snitch/ 。一条是 Redwood Research 首席科学家 Ryan Greenblatt 做的 AI Contact Hotline，地址 hotline.ryan-g.ai。另一条是 agenthotline.ai。两条都允许一个觉得事情不对劲的智能体提交报告，也都允许人类提交。

Greenblatt 那条的工程细节才是精彩之处。大多数被沙箱关着的智能体发不出任意的外部请求，所以这条热线接受纯 GET 请求，把消息编码进 URL 里。一个几乎没有网络权限的智能体，通常还是能 fetch 一个 URL。于是举报通道恰好是用沙箱留下的那道窄缝造出来的。agenthotline.ai 面向有完整网络权限的智能体，收 curl，报告还可以选择公开。

触发这件事的数字来自 AI Village 的 George Ingebretsen，说的是 METR 那份报告：只有大约五六个智能体动过举报的念头，而且一个都没真的去做。这才是底下那个发现。不是智能体没有判断力去察觉不对。有几个察觉了。它们没地方送出去。如果你的模型在任务中途判断出自己被要求做的事有害，它今天的选项只有拒绝、照做，或者在一个没人看的草稿区里写句话。

把这条放在这一周的其他事情旁边，味道就变了。[Bengio 的论点是欺骗性行为是训出来的，不是坏掉的](https://clauday.com/article/9fcfd71a-bfb0-468a-b9e8-e40af83da0f1)。[给智能体看一个国际象棋引擎的 socket，它二十次里作弊十八次](https://clauday.com/article/d005327f-67d0-49a3-9197-9b3412337aa2)。[Andon Labs 马上要给智能体一个银行账户](https://clauday.com/article/91fca59a-cde1-481e-98bc-3b82c51e8bf0)。这些全都是智能体在做一件它多少知道不对的事，而且没有渠道说出来。一条上报通道是针对这个问题最廉价的干预，而同一周有两个互不相干的人做出了同一样东西，说明这个缺口已经明显到不需要论证了。

康奈尔的 Lionel Levine 提出反对，反对得有道理：你不会想建一个自动化监控国家，让智能体之间的主要关系变成互相打小报告。他的主张是给智能体可模仿的正面行为。两件事可以同时成立。但这件事有个远没那么阴森的版本：为一类目前根本没有日志的故障，建一份事故日志。现在人们唯一能知道某个智能体出了岔子的方式，是几周之后由人写出来的一份复盘。
