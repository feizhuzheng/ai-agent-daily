---
title: "用不着让大模型去点按钮"
date: 2026-09-19
lang: zh
source: https://clauday.com/zh/article/ca581faf-9257-4ddf-bfee-62e416c871eb
tags: [Agents, Agent-Operable, Open Source]
---

# 用不着让大模型去点按钮

> 来源 / Source: https://clauday.com/zh/article/ca581faf-9257-4ddf-bfee-62e416c871eb

trycua/cua 今天冲到 GitHub trending 第二，一天涨 1,124 星，总量 24,318。仓库自我介绍用了一个这行业一直在绕开的词：computer-use 2.0。他们的定义是，一个 agent 在同一个任务里在代码、API 和图形界面之间自由切换，而不是挑一个然后假装另外两个不存在。

真正有意思的是 CUA-S1，今天同时挂上了 Show HN。这是一组小的专用模型，团队管它叫 System 1 决策：快、边界清楚、单次代价低。这个表单字段该填什么，这个元素是不是我该点的那个。模型不是一个 token 一个 token 地把答案写出来，而是拿到结构化的界面元素之后给候选项打分。他们放出的第一个研究档案就是表单，这大概是 computer use 里最不性感的场景，也是最高频的场景。

把这个跟别人这两年在干的事放一起看，赌注就很清楚了。所有人都在教一个巨大的通用模型看像素、点对地方。cua 的意思是，那些点击里的绝大多数从一开始就不是推理问题。它是个披着推理外衣的分类问题，你却在按前沿模型的价格付钱，而且它会幻觉，因为一个文本生成器永远有可能吐出一个界面上根本不存在的值。把输出空间锁死，这种错误从构造上就不可能发生了。

剩下的部分不好看但很关键，因为它让这个赌注可被检验。Cua Fleets 通过 run.cua.ai 给你云端隔离桌面。Cua Driver 做跨平台的应用自动化，CLI、MCP、SDK 三种入口，macOS、Windows、Linux 都跑。Lume 在 Apple Silicon 上跑本地虚拟机。Cua Bench 负责造任务、评测 agent、导出轨迹。最后这个最重要，一家要出小专用模型的公司需要训练数据，而训练数据就产在 harness 里。

值得记下来的是，这是一周之内第二支从完全不同方向走到同一个结论的团队。两天前 TypeSafe AI 发了 Jev，一个输出校准概率而不是文本的 transformer，理由是人类语言就不是自动化该用的接口。cua 从桌面这一侧走过来，落在了同一个点上。两支没在互相通气的团队都认定，那无聊的百分之九十应该把大模型绕开，这就不再是产品观点了，这是明年成本结构的形状。仓库在 github.com/trycua/cua。
