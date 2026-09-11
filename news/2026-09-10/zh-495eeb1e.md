---
title: "PI-Desktop 赌的是你的编程 agent 永远不该联外"
date: 2026-09-10
lang: zh
source: https://clauday.com/zh/article/495eeb1e-621e-432f-a7e4-1ba15ccfa233
tags: [Coding, Open Source, Tool]
---

# PI-Desktop 赌的是你的编程 agent 永远不该联外

> 来源 / Source: https://clauday.com/zh/article/495eeb1e-621e-432f-a7e4-1ba15ccfa233

PI-Desktop 一天涨了 636 颗星到 2250。一个 Electron 加 Rust 内核的应用能这样，说明有不少人默默同意它的前提。前提是：你的编程 agent 应该跑在你自己的机器上，用你自己的密钥，中间不该有强制的云端中继。

它是一个桌面工作台，Electron 前端加 Rust host core，包着 pi agent harness。自带模型，OpenAI、Anthropic、本地端点或者任何 OpenAI 兼容接口都行。三个模式：Agent 自主跑，Plan 每一步等你批，Goal 盯着结果。多项目多会话管理，会话能钉住能分叉，内置 diff、命令输出和应用预览的审查面板。扩展靠 Skills、MCP server、子 agent 和用户可装插件，还能从其他编程 agent 工具导入会话。

local-first 这部分不是装饰。没有强制中继，不需要账号，凭据存在操作系统钥匙串里而不是别人的服务器上。考虑到过去两周先是出了会话 token 窃取活动，接着又出了一份关于流量被悄悄转发给第三方模型的威胁报告，"你的密钥不出钥匙串"这句话已经开始像安全特性而不是哲学立场了。

LGPL-3.0，版本 0.14.x，早期预览，macOS Windows Linux 都有构建，在 https://github.com/vastsa/PI-Desktop

老实说的顾虑是这个赛道很挤，一半产品是给别人的 harness 套个好看点的 diff 视图。PI-Desktop 值得看一眼的地方在于插件层加会话导入这条路，两者合起来说明它的野心是成为你跑所有 agent 的地方，而不是你跑某一个 agent 的地方。一个两千星的早期预览能不能在 OpenAI 同一周推出免费托管循环的情况下守住这个位置，是个真正没有答案的问题。

相关阅读：https://clauday.com/article/c13bbd85-af80-44d3-9337-a8446a0f017c
