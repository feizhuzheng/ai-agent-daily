---
title: "MathCode 把终端变成了一台 Lean 4 证明机"
date: 2026-08-16
lang: zh
source: https://clauday.com/zh/article/7ece44bc-2a52-4f60-8c8d-b007c6fa9ba5
tags: [Coding, Open Source, Agents]
---

# MathCode 把终端变成了一台 Lean 4 证明机

> Source: [clauday.com](https://clauday.com/zh/article/7ece44bc-2a52-4f60-8c8d-b007c6fa9ba5)

Math-AI 团队放出了 MathCode，一个内嵌数学形式化引擎的终端编码 agent。你用大白话说一个问题，它转成 Lean 4 定理，然后去证。619 星，建在他们之前的 AUTOLEAN 上，周末上了 Hacker News。

真正让它可用的工程细节是常驻的 Lean REPL。Lean 的编译周期是 agent 做证明的杀手——每次检查大约 30 秒，一个迭代五十次的 agent 光等就烧掉 25 分钟。MathCode 只在开头热一次 REPL，大约 90 秒，之后每次检查约 0.4 秒。这不叫优化，这是这个循环能不能成立的分界线。

围着它的是些你会想要的部件：一个定理库，把证过的东西存下来复用；一个公理库，把你在对话里陈述的假设形式化保存；接了 LSP，所以它能真的找到相关引理，而不是瞎猜名字；子目标树分解，可以并行去证不同分支；以及多个 planner 同时跑不同的证明策略。它还能生成一个 Obsidian vault，把定理之间的依赖关系画出来。

为什么这比一个数学工具更有意思。形式化证明是唯一一个 agent 能拿到完美、即时、不容商量的验证器的领域——Lean 要么接受这个证明，要么不接受，没有裁判模型，没有评分标准，没有感觉。所有在追自我改进 agent 的人都缺这么干净的信号，而这里它是免费的。

值得盯的赌注是：在这里管用的 harness 模式——并行子目标、可复用的证明库、多个互相竞争的 planner——能不能迁移到验证器是测试套件而不是类型检查器的领域。https://github.com/math-ai-org/mathcode
