---
title: "Google 的 agent 运行时底下还有一层地板，地板才是正片"
date: 2026-09-22
lang: zh
source: https://clauday.com/zh/article/c97dcf4c-2ac0-462d-9e8a-5a378a1ac9d4
tags: [Infrastructure, Open Source, Agents]
---

# Google 的 agent 运行时底下还有一层地板，地板才是正片

> 来源 / Source: https://clauday.com/zh/article/c97dcf4c-2ac0-462d-9e8a-5a378a1ac9d4

上周 google/ax 作为 Google 的开源 agent 编排运行时出场时，README 里提了一句它建在一个叫 Agent Substrate 的东西上。现在这东西有了自己的仓库，自己上了 trending，今天涨 301 星，总数 2923。

它的说法具体到可以被反驳：一个默认安全的 agent 执行运行时，目标是跑几百万个沙箱，密度是标准容器运行时的 10 倍。实现方式是把很多 actor 映射到少得多的 worker 上，把空闲时间榨出来。让人觉得可信的数字是：恢复耗时低于 500 毫秒，挂起/恢复激活每秒超过 500 次。内核和网络层的零信任隔离，沙箱用 microVM 或 gVisor，底下压 Kubernetes 管资源和 worker 生命周期。

那个密度指标其实是在描述 agent 负载真实长什么样。一个 agent 的绝大部分墙钟时间都在等——等模型返回，等工具返回，等人。一个全程常驻的容器，为一段几乎什么都没干的时间付了全价。只要挂起和恢复够快，空闲就不再花钱，而这是 agent 数量从几千变成几百万之后，单个 agent 的账唯一能算平的办法。

Apache 2.0 许可证在，"非 Google 官方支持产品"的免责声明也在，README 明说早期开发、不可用于生产。行。真正要盯的是分层：ax 是 harness，Substrate 是底座，Google 把两层分开发布。这等于在邀请别家的 harness 也跑到同一块地板上，跟端出一个一体化运行时完全是两回事。

https://github.com/agent-substrate/substrate
