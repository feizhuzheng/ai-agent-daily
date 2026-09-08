---
title: "Hyperprobe：让 agent 只读调试生产环境"
date: 2026-09-07
lang: zh
source: https://clauday.com/zh/article/9bdf54c5-bb7d-4275-8cc1-cd3048ff8856
tags: [Agents, Monitoring, MCP]
---

# Hyperprobe：让 agent 只读调试生产环境

> 来源 / Source: https://clauday.com/zh/article/9bdf54c5-bb7d-4275-8cc1-cd3048ff8856

编码 agent 几分钟就能写好修复代码，然后等一个人花四小时搞清楚 bug 到底是什么。Hyperprobe 打的就是这个缺口——YC S26 公司，Product Hunt 第 4 名、212 票。它让 Claude Code、Codex、Cursor 直接挂到你的生产服务上看实时变量状态，不用重新部署、不用重启，而且碰不了任何东西。

机制叫虚拟断点：往运行中的服务里插只读探针，抓到日志从来没记下的那些状态。服务里放一个 SDK（支持 Node、Python、Java、Kotlin），另一头是一个 MCP server，agent 自己跑调试循环——插探针、读状态、提假设、插下一个探针。只读是在运行时层面强制的，Node 上用的是 V8 的 throwOnSideEffect，探针物理上改不了你的服务。开销 Node 7-10 毫秒、Python 4-9 毫秒、Java 1-2 毫秒，跑在你自己的 VPC 里。

它瞄准的是最恶心的一类生产 bug：静默逻辑错误。没有异常、没有堆栈，就是响应不对、竞态、重复处理。创始人给的案例是一个支付 bug，人肉考古要 4 小时，agent 9.5 分钟定位。Launch HN 里也有质疑：跟 Rollbar、AppSignal 功能重叠，以及 agent 可能给出"自信的错误诊断"——都对，但可观测性工具只给你看现场，不替你跑排查循环。

真正聪明的是信任工程这一步。没人敢给 agent 生产环境的写权限，而由运行时强制、不是靠 prompt 承诺的只读，是让生产环境第一次成为 agent 领地的那个楔子。https://www.hyperprobe.co
