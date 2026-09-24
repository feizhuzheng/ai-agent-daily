---
title: "关闭遥测，Claude Code 就不读你的 AGENTS.md 了"
date: 2026-09-23
lang: zh
source: https://clauday.com/zh/article/770efaf9-8bbb-490d-a747-2f2a096ceaca
tags: [Agents, Coding, Infrastructure]
---

# 关闭遥测，Claude Code 就不读你的 AGENTS.md 了

> 来源 / Source: https://clauday.com/zh/article/770efaf9-8bbb-490d-a747-2f2a096ceaca

读一个本地 markdown 文件不需要网络。Claude Code 2.1.277 偏偏让它需要，而且很长一段时间没人发现，因为它失败得毫无声息。

机制是这样的。AGENTS.md 支持是作为一个内置插件发的，挂在一套叫 Mods 的新扩展系统下面，而加载器藏在一个叫 tengu_agents_md_mod 的 Statsig 远程特性开关后面。默认关闭，由 Anthropic 的服务器决定开不开。如果你设了 CLAUDE_CODE_DISABLE_NONESSENTIAL_TRAFFIC=1，或者你是通过 Bedrock、Vertex、任何第三方网关跑 Claude Code，你的会话根本不会去拉特性开关。这个门永远不可能变成 true。你的 AGENTS.md 就是不加载。没有报错，没有警告，启动输出里一行提示都没有。agent 表现得像这个文件根本不存在。

这条在 HN 上拿到 426 分，靠的是那个隐私上的倒置。最可能关掉遥测的人，是在受监管环境里、在准隔离网里、或者走公司网关的那批人——也恰恰是最需要一个签入仓库的指令文件真的被读到的人。关掉数据收集，悄悄劣化了本地行为，而这是遥测开关唯一绝对不该起作用的方向。

Anthropic 的 mpoteat 回应得很快，也没绕弯：这是发布过程的产物，我们需要一个能远程关掉它的办法以防出问题，而遥测关了你就拿不到开关。v2.1.281 修复，当天。这一点该给的分要给——反应正确，而且用的是小时，不是星期。

值得留下的不是这个 bug，是它的形状。当特性开关系统和遥测通道焊在一起，每一个开关就都变成了对厂商可达且愿意的依赖。评论区还揪着另一半不放：决定读哪个文件名这种偏好，不该需要一套插件架构、一套 mod 系统和一堆函数钩子。正是过度工程，才先造出了一个能让远程开关坐上去的表面。如果你的 harness 读配置文件要经过服务端评估的门，那你并不完全知道你的 agent 读到了什么。

https://blog.szypowi.cz/p/claude-code-reads-agents.md-only-when-telemetry-is-on/
