---
title: "SemaPLC：agent harness 下车间了"
date: 2026-08-20
lang: zh
source: https://clauday.com/zh/article/0b9ebd64-08c3-4a81-a267-ea18243fd0e2
tags: [Agents, Infrastructure]
---

# SemaPLC：agent harness 下车间了

> Source: [clauday.com](https://clauday.com/zh/article/0b9ebd64-08c3-4a81-a267-ea18243fd0e2)

PLC 是跑工厂的计算机——流水线、水处理、暖通空调都归它管。这种代码写错了不会抛异常，会让物理机器往错的方向动。HuggingFace 日榜 110 票的 SemaPLC 是一个生成 PLC 代码的 agent harness，出自美的——那个收了机器人巨头 KUKA 的家电公司，也就是说发这篇论文的人手里有真工厂。

架构对跟过 harness 这条线的人来说很眼熟：绝不信任模型的自我评估，一切过外部验证的闸门。生成的代码要过三道闸：规格合规、编译通过、在真实 PLC 系统上验证运行时行为。论文的口号就是当前这整波浪潮的论点：忠实的检验是执行，不是静态打分。七个模型、117 个任务上,harness 拿到 72.6% 的平均验证通过率；更难的项目上下文任务——新代码要嵌进已有代码库——动态行为通过率 52.2%，基线只有 22% 到 31%。

这组数字要两面读。harness 把基线翻了一倍还多；但现实任务上它仍有近一半在失败，放在工业自动化里意味着可见的未来人还得留在环里。不过两年前的 coding agent 也是这样。

更大的信号是谁在发。验证闸门式 harness 本来是软件业的模式；一家制造商把它用到驱动物理机器的代码上，还把结果开源了——这说明这个模式正在冲出软件业。代码在 github.com/midea-ai/SemaPLC。

https://arxiv.org/abs/2608.18565
