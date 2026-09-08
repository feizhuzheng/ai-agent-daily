---
title: "换个模型，你 agent 的记忆可能就没了"
date: 2026-09-07
lang: zh
source: https://clauday.com/zh/article/ebff88cb-a0d3-41b0-b610-00cb076fd41e
tags: [Research, Infrastructure, Open Source]
---

# 换个模型，你 agent 的记忆可能就没了

> 来源 / Source: https://clauday.com/zh/article/ebff88cb-a0d3-41b0-b610-00cb076fd41e

有一个几乎没人测的故障模式：模型升级了，记忆库还是原来的，agent 悄悄失忆了。一项新的对照研究（arXiv 2609.05339）显示，同一份存储历史在新模型眼里读出来不一样——旧笔记被重新解读，新旧混用的 embedding 让检索失灵，而且往往没有原始证据可以用来修复。

数字很扎眼。存成固定 schema 知识图谱的记忆，换模型基本无损——精度只动了 0.0004。被旧模型压缩成自然语言笔记的记忆，摆动 10 到 13 个百分点，而且不对称，取决于往哪个方向迁移。那些笔记不是知识，是用旧模型方言写的知识，新模型只能听懂一半。RAG 用五五混合的 embedding 索引，结果居中。原文照存最安全，但上下文会爆。

这让 OKF Agent Memory 出现的时机显得很妙——HN 78 分，452 star。它赌的是 Open Knowledge Format：agent 记忆就是纯 markdown 加 YAML，住在你的 git 仓库里，内存 BM25 检索 300 微秒以内，走 MCP 暴露，纯 Go，MIT，零 embedding API 成本，明着对标 Mem0 和 Letta。

两件事放在一起是一条设计规则：以可读文本形式活在版本控制里的记忆，天生可以跨模型；被压缩成某个模型自己摘要的记忆，跟那个模型的脑子绑死了。选记忆方案的时候，就当你一定会换模型——因为你真的会，差不多一个季度一次。https://arxiv.org/abs/2609.05339 和 https://github.com/okf-memory/okf-agent-memory ，记忆当产品那条线看 https://clauday.com/zh/article/37007d2e-9638-46c1-9e5b-d4c95b7b511f。
