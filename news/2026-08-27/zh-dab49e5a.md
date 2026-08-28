---
title: "JIT-Agent：harness 变成模型在运行时现写的东西"
date: 2026-08-27
lang: zh
source: https://clauday.com/zh/article/dab49e5a-4759-4b69-bfda-379192c926a2
tags: ["Research", "Agents", "Framework"]
---

# JIT-Agent：harness 变成模型在运行时现写的东西

来源 / Source: https://clauday.com/zh/article/dab49e5a-4759-4b69-bfda-379192c926a2

harness 这条线迎来了逻辑上的下一章。新加坡国立大学的团队发布了 JIT-Agent，一个被训练来干一件元层面事情的模型：即时生成 agent 的 harness 本身，为眼前的任务量身定制。记忆管理、规划策略、行动协议、工具编排——所有目前靠人手按任务设计的部分——被形式化成可组合、可机器生成的构件，收在一个固定的四模块协议之下。

数字就是论点。套上 JIT 生成的 harness，DeepSeek-V4-Flash 在 DeepSearchQA 上反超 GPT-5.6 达 9.1 分，在 OdysseyBench 上多 4.3 分。GLM-5.2 最多能涨 20.2 分。带着本周的经济学再读一遍：一个便宜的开源模型,装进为任务定制的 harness，分数压过前沿旗舰。它跨 DeepSeek、Mimo、Qwen 家族通用，还能在运行中修复 harness、从历史配置档案里学习，越用越强。

过去一个月的轨迹已经很难看漏。NVIDIA 的 NOOA 展示了手工 harness 把 Opus 5 在 ARC-AGI-3 上从 30% 拽到 100%。Google 的 EnvHarness 让 agent 重写环境。JIT-Agent 把 harness 的编写本身自动化了。先是发现 harness 比所有人预算的都重要，接着发现环境也是，现在 harness 正在变成模型互相生成的东西。手工 harness 时代大概率会被记成一段短暂的手工业时期。

对做 agent 的人，实际的启示是：harness 设计知识正在被编译进模型，就像当年 prompt engineering 被编译进指令微调一样。耐用的本事是定义任务和检查标准，因为中间那层脚手架正在变成生成出来的产物。论文在 arxiv.org/abs/2608.25593。
