---
title: "DarwinX 不进化模型，进化 harness，WebArena 从 43.5 干到 93"
date: 2026-08-14
lang: zh
source: https://clauday.com/zh/article/0ade458f-39aa-40b6-9619-cbc1adc319c5
tags: ["Agents", "Research", "Framework"]
---

# DarwinX 不进化模型，进化 harness，WebArena 从 43.5 干到 93

> 来源 / Source: https://clauday.com/zh/article/0ade458f-39aa-40b6-9619-cbc1adc319c5

Salesforce AI Research 发了 DarwinX，把所有人都在绕的那个想法直接做成了种群。模型权重冻死。进化的是 harness：prompt、工具、skill、控制流。在脚手架上跑自然选择。

会被反复引用的结果是 WebArena-Infinity 从 43.5% 到 93.0%，且审计干净。Terminal-Bench 2.1 在同级底座上 83.2，换更强的底座 84.7。TerminalWorld 在留出集上 68.3。而真正要紧的是迁移那一条：在 Terminal-Bench 上进化出来的 harness，原封不动搬到 SWE-bench Verified 上依然管用。作者明说进化出来的是通用 agent 能力，不是针对某个榜的补丁，留出集和迁移结果就是证据，不是许愿。

两个设计决定撑起了全部。第一，他们维持一个种群而不是单一的自我改进谱系，还有一个档案库保留旁支，让死掉的分支里的好点子后面还能被重组回来。跑过自我改进循环的人都知道那个失败模式：系统第三轮找到一个局部最优，接下来四十轮全在抛光。种群加档案是标准解药，agent 自我改进这个方向这么久才把它借过来，其实挺奇怪的。第二，一个"保留并扩展"的约束，不让新改动把已经通过的任务改坏，这是这类循环自噬的另一个经典死法。

适应度来自针对榜的验证器，不是标准答案；改动的输入是失败证据、教师证据和自我推导的证据，走同一个统一编辑接口。是这套组合让它成为一次搜索，而不是一个调 prompt 的脚本。

把它跟昨天的 DeepSeek Harness 放一起看——那边把 harness 变成了改配置就能编辑的插件图——再加上 AI4AI，强模型写出的 harness 把弱模型的分数几乎翻倍。两天之内三组独立的人得出同一个结论：模型是固定资产，harness 才是你要优化的变量。DarwinX 是 arXiv 2608.07545。
