---
title: "Academic Research Skills：一个插件塞进 13 个研究员"
date: 2026-09-02
lang: zh
source: https://clauday.com/zh/article/abf2649d-add7-42eb-b3b6-1c1422882d9c
tags: [Skills, Open Source, Research]
---

# Academic Research Skills：一个插件塞进 13 个研究员

> 来源 / Source: https://clauday.com/zh/article/abf2649d-add7-42eb-b3b6-1c1422882d9c

Academic-research-skills 今天涨了 801 星，总量 45,500——现存最大的 skills 仓库之一，今天冲上 trending 是终于该看看它的信号。这是一套覆盖整个学术流水线的 Claude Code 插件：Deep Research（做系统综述和事实核查的"13-agent 研究团队"）、Academic Paper（12-agent 写作流水线，支持多种引用格式）、Academic Paper Reviewer（7-agent 多视角评审）、还有 Academic Pipeline，一个从研究到发表端到端的 10 阶段编排器。插件市场一条命令安装，也能跑在 Pi 等其他平台上。

两个细节值得注意。一是版本号——v3.21.1、752 个 commit、专门针对验证和诚信检查的发布记录——skills 在像真软件一样成熟，而且内置了一个尴尬的自我承认：学术 agent 需要防编造机制。二是协议：CC-BY-NC，禁止商用。一个 45k 星的 skills 仓库决定自己的 know-how 不能免费商用，这是"打包的专业知识开始有明确市场价值"这件事最早的数据点之一。

不舒服的问题在同行评审这个环节。同一套件用 12 个 agent 写论文、用 7 个 agent 审论文。没有任何机制阻止这条流水线写的论文被这条流水线审——第 8 位评审可能想问问这事。

仓库：https://github.com/Imbad0202/academic-research-skills
