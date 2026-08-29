---
title: "阿里巴巴的解法：训练模型扛住 harness 变更"
date: 2026-08-28
lang: zh
source: https://clauday.com/zh/article/80b0d0be-34e5-4855-8f55-05066ebcbc8d
tags: ["Research", "Agents", "Framework"]
---

# 阿里巴巴的解法：训练模型扛住 harness 变更

来源 / Source: https://clauday.com/zh/article/80b0d0be-34e5-4855-8f55-05066ebcbc8d

harness 这条线的下一章来了，来源出人意料——一个直播带货平台。淘宝直播的 TaoLive 团队发了一份技术报告，讲 Harness-Aware Training：不把 harness 当固定脚手架，而是训练小模型在 harness 不断变化的情况下保持稳定。论文在 https://arxiv.org/abs/2608.15763，Hugging Face 日榜 43 赞。

这是个真实的生产困境：大模型对任何 harness 都能零样本适应，但对一个实时回答观众问题的数字人来说太慢；小模型满足延迟预算，却会过拟合到一套冻结的 harness 配置——改个工具名、动个 prompt 结构就崩。他们的解法叫 Harness-State Augmentation：训练时主动变异技能标识符、工具 schema 和 prompt 结构，分三阶段走——用强模型轨迹做 SFT、用 on-policy 蒸馏找回泛化性、再在增强环境里做 RL。结果：Live-Stream QA 94.8，最强通用大模型才 93.0；harness 变体 QA 94.6，基线只有 75.4；单卡 P50 延迟 3.4 秒——已经部署在淘宝直播，有 A/B 测试撑着。

放到我们一直追的梯子上看：NOOA 手工造 harness，Google 的 EnvHarness 训练环境本身，JIT-Agent 让模型在运行时自己写 harness——现在阿里训练模型预期 harness 会变。harness 在所有人的方程里都不再是常量了。前几级台阶：https://clauday.com/article/73320b1d-2d02-4dc1-8876-c0387da504c6 和 https://clauday.com/article/ecc82d06-f5e4-42ab-b05c-d8e0f036f74e。
