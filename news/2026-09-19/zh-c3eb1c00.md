---
title: "Anthropic 把十一份岗位说明书开源了"
date: 2026-09-19
lang: zh
source: https://clauday.com/zh/article/c3eb1c00-9aa0-45b9-9694-2c00c0641efc
tags: [Skills, Agents, Open Source]
---

# Anthropic 把十一份岗位说明书开源了

> 来源 / Source: https://clauday.com/zh/article/c3eb1c00-9aa0-45b9-9694-2c00c0641efc

anthropics/knowledge-work-plugins 今天在 trending 上，一天 280 星，总数 25,100。里面是十一个插件，把 Claude 变成某个具体岗位的专才，为 Claude Cowork 做的，Claude Code 里也能用。生产力、销售、客服、产品、市场、法务、财务、数据、企业搜索、生物研究，外加一个用来做你自己插件的。

结构每一个都一样，值得看一眼，因为这是 Anthropic 自己对一个生态吵了好几个月的问题给出的答案。每个插件就是一个 manifest、一个声明连哪些工具的 .mcp.json、一个放斜杠命令的 commands 目录、一个放领域知识的 skills 目录。完了。没有框架，没有编排层，没有图。连接、命令、知识。

连接器清单暴露了这是冲谁去的。销售接 HubSpot、Close、Clay、ZoomInfo。法务接 Box、Egnyte、Microsoft 365。财务和数据直接怼 Snowflake、Databricks、BigQuery。产品接 Linear、Figma、Amplitude、Intercom。这些不是加了个 agent 的开发者工具，这是一家公司赖以运转的软件，而 Anthropic 公开了一张从单个助手触达全部这些系统的地图。

最该先读的是 Bio-Research，它接的是 PubMed、BioRender、Benchling、ChEMBL。它发布的同一周，Anthropic 确认自己在湾区运营一个湿生物实验室。这两件事是同一个战略的两个侧面，而插件是便宜的那一半：他们把一个生命科学研究者工作时所处的工具图谱公开了，而 skills 文件是他们对这活儿到底怎么干的看法。

这才是真正新的东西，而它不是代码。一个 skills 目录是一份关于某个岗位由什么构成的书面主张，提交进公开仓库，有版本，可以提 PR。Anthropic 一次公开了十一份。不管你用不用 Cowork，一家前沿实验室里有人把他认为法务审查、管线复盘、对账到底是什么写了下来，你可以去读，也可以用一个 diff 表示不同意。仓库在 github.com/anthropics/knowledge-work-plugins。
