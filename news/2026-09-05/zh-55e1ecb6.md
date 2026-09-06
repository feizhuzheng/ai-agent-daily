---
title: "Intelligence Index v4.2：把 40% 的考题藏起来不给实验室看"
date: 2026-09-05
lang: zh
source: https://clauday.com/zh/article/55e1ecb6-a7c3-4fc2-b08d-c34d76c42e38
tags: [Benchmark, Research]
---

# Intelligence Index v4.2：把 40% 的考题藏起来不给实验室看

> 来源 / Source: https://clauday.com/zh/article/55e1ecb6-a7c3-4fc2-b08d-c34d76c42e38

9 月 4 日 Artificial Analysis 发布了 Intelligence Index v4.2（https://artificialanalysis.ai/articles/artificial-analysis-intelligence-index-v4-2），最重要的变化不是任何一个分数，而是私有保留测试集的权重升到了整个指数的 40%，比 v4.1 翻了一倍。给出的理由毫不客气："降低实验室针对评测刷分的能力。"业内被引用最多的独立榜单等于正式宣布：公开基准已经不能当测量工具，只能当营销物料。

两个新评测进场，一个老将退役。AA-Briefcase 是自建的 agent 评测，考察复杂项目里数周量级的真实知识工作，用评分细则加两两对比来打分，题库私有。GDP.pdf 由 Surge AI 打造，让模型在一份 4,592 页的文档上做推理，对着 1,275 条专家撰写的标准逐条核对。退役的是 GPQA Diamond——被正式宣布"已饱和"。一个当了两年发布会头牌的基准，如今因为分不出前沿模型的高下而退场。

分数本身：Claude Fable 5.1 拿下总榜第一，并和 Opus 5 一起领跑 AA-Briefcase（那次发布的报道在 https://clauday.com/zh/article/1022b00f-4b00-4be8-8b0c-06277317e436）。GPT-6 Astra 比前代涨了约 4 个指数点、约 85 Elo，以 33.2% 领跑 4,592 页的 GDP.pdf，并且是输出 token 效率之王。Meta 是第三名的实验室，排在 SpaceXAI、Moonshot、Z.AI 和 Google 前面。

把这个和上周 ARC 亲口承认榜单测的是"模型加 harness"（https://clauday.com/zh/article/3400c65c-371c-492a-ab6b-c246e9512206）放在一起看，其实是同一个故事：评测层正在围绕不信任重建自己——防污染、防刷分、防脚手架。私有题库就是评测界的闭源，而且似乎没人觉得这有什么讽刺。
