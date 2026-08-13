---
title: Macro 把整个工作空间开源了，为了让 agent 真的够得着你的活
date: 2026-08-12
lang: zh
source: https://clauday.com/zh/article/cc5c895d-f877-4252-bfe8-eed5cb3cc98f
tags: Agents, Open Source, MCP
---

# Macro 把整个工作空间开源了，为了让 agent 真的够得着你的活

> 来源 / source: [clauday.com](https://clauday.com/zh/article/cc5c895d-f877-4252-bfe8-eed5cb3cc98f) · 2026-08-12

macro-inc/macro 今天上了 GitHub trending：一个面向团队的统一工作空间，把邮件、聊天、文档、任务、agent、通话和 CRM 打包在一起，用 @ 互相链接，共享一层 AI 记忆。Rust 后端，SolidJS 前端，将近 5000 个 commit，AGPLv3。README 特意强调这是完全开源而不是 open core，商业授权另谈。

它赌的设计判断是：agent 干不好活不是因为笨，是因为活散在八个互相不说话的产品里。你的 agent 能读到那张工单，但读不到引出这张工单的邮件线程，也读不到真正做决定的那通电话。Macro 的答案是把这些全放在一个地方，加一层从对话、邮件、任务和通话里合成出来的共享记忆，然后把整体暴露出去。

真正要紧的细节在工具那一侧。跨多家供应商的 MCP 集成。一个宣称覆盖率接近 100% 的工具面——意思是 agent 不被限制在一小撮精挑的动作里，坐在这个应用前的人能干什么它就能干什么。MCP 操作没有速率限制。文档通过 CRDT 协作做到 agent 原生编辑，人和 agent 可以同时在一篇文档里而不互相覆盖。

"issue tracking 已死"这种话通常过几年会很难看，而这类"把一切合并"的打法在历史上经常输给只做好一件事的好产品。但工具覆盖率那个论点是真的，而且被严重低估。大多数企业 MCP server 客客气气暴露几个只读操作就管这叫集成，然后大家又对 agent 什么都干不完感到意外。要么把整个界面给它，要么接受它会不停把活退回给你。

https://github.com/macro-inc/macro
