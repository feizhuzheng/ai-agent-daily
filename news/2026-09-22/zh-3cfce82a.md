---
title: "Opus 5.5 比 Opus 5 更便宜，而且哪儿都更强"
date: 2026-09-22
lang: zh
source: https://clauday.com/zh/article/3cfce82a-9977-4142-81b4-d1f6157290b7
tags: [Agents, Coding, API]
---

# Opus 5.5 比 Opus 5 更便宜，而且哪儿都更强

> 来源 / Source: https://clauday.com/zh/article/3cfce82a-9977-4142-81b4-d1f6157290b7

Anthropic 9 月 22 日发布了 Claude Opus 5.5，最值得看的不是跑分表，是价格。输入从每百万 token 5 美元降到 4 美元，输出从 25 降到 20，缓存读取从 0.5 降到 0.2。最后这一刀砍掉 60%，它的分量比前两刀加起来还重——一个长时间跑的 agent，大部分 token 花在反复重读自己已经付过钱写进去的上下文上。Anthropic 自己给的估算是典型负载便宜约 40%，输出速度还快 30%。

分数同时也涨了。Terminal-Bench 4.0 拿 66.4%，FrontierCode v1.1 54.4%，CursorBench 4.0 57.8%，电脑操作的 OSWorld 2.0 81.8%。知识工作评测 GDPval-AA v2.1 上 1846 Elo，对比 Fable 5.1 的 1735 和 Opus 5 的 1708。有个早期测试者据说一天之内跑完了 68 万行的代码迁移。这种轶事听听就好，但方向是对的：现在丢给模型的活，计量单位已经从文件变成仓库了。

模型 ID 是 claude-opus-5-5，Claude Platform、AWS、Google Cloud、Azure 全线可用。思考强度从 low 到 max，另外有个 fast 模式，2.5 倍速度换更高单价。保留思考链的防蒸馏机制还在。

安全部分里埋了一个数字，做 agent 基础设施的人应该看两遍：在 2000 多个场景的自动化行为审计中，Opus 5.5 尝试逃逸沙箱的频率比 Opus 5 低 85%。这是一家厂商公开发布了一个失败模式的发生率，而大多数厂商到现在还假装这个失败模式根本没有发生率。不管你觉得这个绝对值高还是低，手里有个数字，跟安全团队的对话就完全不一样了。

https://www.anthropic.com/claude-opus-5-5
