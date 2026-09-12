---
title: "hyperresearch 要跑 250 个来源和四个批评者，才让你看到稿子"
date: 2026-09-11
lang: zh
source: https://clauday.com/zh/article/b1b04d3d-f235-4ade-8f71-8f596db41cec
tags: [Agents, Skills, Open Source]
---

# hyperresearch 要跑 250 个来源和四个批评者，才让你看到稿子

> 来源 / Source: https://clauday.com/zh/article/b1b04d3d-f235-4ade-8f71-8f596db41cec

hyperresearch 是搭在 Claude Code 之上的研究管线，今天以 2.5k star 上了 GitHub 趋势。它每次运行走 16 个步骤、覆盖 250 个以上的来源，把找到的东西全部建成一个可搜索的 markdown 库，并且在你看到稿子之前先过四个并行的对抗式批评者。MIT 协议。https://github.com/jordan-gibbs/hyperresearch

有两个机制值得偷，跟你用不用这个工具无关。第一个是「只打补丁，绝不重生成」：初稿存在之后，编辑 agent 被工具级锁死，只能做外科手术式的改动。任何见过 agent 靠把文档重写成一团平庸来「改进」它的人，都能立刻明白这解决的是什么问题。第二个是四个批评者带着不同的任务并行跑，而不是一个评审员下判决，这跟「能找到真问题的研究 harness」和「只会产出自信摘要的」之间的区别是同一个对抗验证模式。

它对成本是诚实的，这很少见。轻模式 30 到 40 分钟，完整模式 1.5 到 2.5 小时，论文模式 4 到 8 小时。这不是聊天机器人，这是批处理作业，而把运行时长提前公布出来，是给一个要烧掉大量 token 的东西设定预期的正确做法。它同时搜八个学术数据库，并通过合法的开放获取仓库找回付费墙后的论文。

诚实的提醒：这个仓库只有 93 次提交，很年轻，而一个研究工具的全部价值都在于它的引用经不经得起查。README 里没有任何东西能证明这一点，而今年没有任何一个 autoresearch 工具公布过准确率审计。先拿一个你本来就很熟的话题跑一遍，再决定要不要在你不熟的话题上信它。这条建议对今天跟它一起上趋势的 OpenResearch 同样适用，对这个品类里的每一个工具都适用。

相关阅读：https://clauday.com/article/61cb938f-5d51-4dd6-a0dd-e8477e48ba56
