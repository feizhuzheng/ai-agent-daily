---
title: "Univer 不再自称办公 SDK，改称 harness 了"
date: 2026-09-22
lang: zh
source: https://clauday.com/zh/article/a1de989f-6707-45af-8926-5fe93b3ec6af
tags: [Agents, Agent-Operable, MCP]
---

# Univer 不再自称办公 SDK，改称 harness 了

> 来源 / Source: https://clauday.com/zh/article/a1de989f-6707-45af-8926-5fe93b3ec6af

dream-num/univer 做开源办公 SDK 有一阵子了，能把表格、文档、幻灯片、白板、关系表嵌进自家产品。现在它的标语改成了：给 AI Agent 的办公 Harness。今天 trending 涨 202 星，总数 1.53 万，Apache 2.0。

这次改口有三样东西撑着，第三样是别家没有的。agent 通过结构化 API 读改办公内容，而不是盯着像素。agent 通过内容检查、截图和排版诊断来验证自己的输出。以及，agent 在隔离的草稿里干活——worktree——由人审核后再合并。配套仓库 univer-mcp 让你用自然语言经 MCP 驱动 Univer 表格。

worktree 这一手是真正有赌性的一步。所有给文档做 agent 工具的人都撞过同一堵墙：agent 的修改要么生效要么不生效，改错了你只能回滚版本历史，而那套历史根本不是为一分钟改四十处的机器设计的。把 git 的分支模型搬到电子表格上，意味着审核这一步变成了结构性的，而不是事后凭感觉扫一眼。

无头 Node 运行时之所以重要，是同一个道理。整套办公套件不需要浏览器就能跑，agent 就可以在服务端循环里打开工作簿、跑完一条计算链、截一段区域看看自己的排版对不对，然后关掉。表格从一个需要 agent 去戳的界面，变成了一个它可以调用的计算环境。

https://github.com/dream-num/univer
