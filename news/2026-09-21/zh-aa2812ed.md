---
title: "谷歌把 agent 的 Kubernetes 开源了，叫 AX"
date: 2026-09-21
lang: zh
source: https://clauday.com/zh/article/aa2812ed-17ca-4aa4-b1a6-fd3b2c526d08
tags: [Agents, Infrastructure, Open Source]
---

# 谷歌把 agent 的 Kubernetes 开源了，叫 AX

> 来源 / Source: https://clauday.com/zh/article/aa2812ed-17ca-4aa4-b1a6-fd3b2c526d08

谷歌刚开源了 AX，全名 Agent Executor，口号一点都不含蓄：单集群跑几十亿个自主 agent 任务。仓库在 github.com/google/ax，Apache 2.0，上了 Hacker News 当天 AI 板块第一，600 多分，官网是 agentexecutor.io。

设计刻意做成 kubectl 的形状。四个原语就结束了：Task 是跑活儿的隔离沙箱，Workspace 把环境接起来，Gateway 给网络围栏，Model 管配置。apply、get、describe、watch、delete，再加几个 agent 专属动词。管过集群的人十分钟就能上手，这显然是故意的。

底下垫着 Agent Substrate，谷歌为 actor 密度而不是为容器造的计算运行时。数字也从这儿来：亚秒级恢复、几十个任务复用同一批 worker 资源，还有讨论区里所有人真正盯上的那一条，从内核快照做轨迹分叉。把一个正在跑的 agent 的完整状态 fork 出来，从同一个点探索两个未来。这不是调度功能，这是调试和搜索功能，这一层上目前没有第二家在做。

同时落地的 v0.3.0 更能说明真正的工程发生在哪儿。AX 拆成了三个服务，API 前端、reconciler、沙箱任务执行器，并且把任务状态从 Kubernetes 自定义资源里挪进了 Redis Streams。翻译一下就是：他们撞到了那堵墙——etcd 不再适合存几百万条可变的 agent 状态——然后绕开了它。这是非常具体的一种伤疤，只有真跑过才会有。

比一般谷歌 GitHub 项目值得重视的原因在这儿。仓库挂在官方 google 组织下、带真授权，讨论区把这一点点出来是对的。而且这个框架本身是个赌注：谷歌认为 agent 的稀缺资源不是模型，是控制面。动态调度、恢复、自动容错、审计，全部当一等公民，而不是等 agent 集群着火之后再往上贴。所有还在用一个队列、一个重试循环加祈祷拼 agent 编排的团队，写下一行胶水代码之前应该先看看这个。https://github.com/google/ax
