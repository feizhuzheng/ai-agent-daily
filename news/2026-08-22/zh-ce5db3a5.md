---
title: "MCP 新路线图：默认打电话来的不是人"
date: 2026-08-22
lang: zh
source: https://clauday.com/zh/article/ce5db3a5-6389-4cec-bacb-aec269504d1a
tags: ["MCP", "Infrastructure"]
---

# MCP 新路线图：默认打电话来的不是人

来源 / Source: https://clauday.com/zh/article/ce5db3a5-6389-4cec-bacb-aec269504d1a

MCP 8月22日发布的新路线图里最扎眼的一句话："MCP 的授权模型假设授权那一刻有个人坐在浏览器前。而现在，调用方越来越多是 agent。"HN 上几小时冲到 160 分。距离 MCP 成为 AI 工具的 USB 接口刚一年，协议开始围绕"键盘前没有人"这个假设重造自己。

具体动作是新成立 Agent Identity 工作组：DPoP 持有证明、workload identity federation、OAuth token exchange——让 agent 用自己的身份或用户委托的身份访问 MCP 服务器，让子 agent 拿到比父 agent 更窄的权限。路线图直接承认现状：今天大家靠的是贴进配置的 API key 和长期有效的 refresh token。他们甚至在讨论 human-presence attestation：让服务器能分辨对面到底有没有人。

传输层的动作同样激进。Streamable HTTP 成为唯一绑定——本地服务器通过 HTTP/2 跑在 stdin/stdout 上，直接干掉每个 SDK 现在都要维护的 stdio/HTTP 双管道。服务器获得推送能力：channel、订阅、webhook，长时间运行的 agent 任务不用再靠客户端轮询烧钱。

对 agent 开发者最有体感的是 progressive discovery：客户端按需学习服务器的工具，而不是一上来吞下整个目录。看过 agent 淹死在 200 个工具列表里的人都知道这刀砍向哪里——各家 harness 私下都在做的延迟加载，现在要进协议本身了。再加上重designed tools/call 来解决 content 和 structuredContent 的混乱，这份路线图读起来不像功能清单，更像一个宣言：agent 基础设施正在往协议层收敛。

路线图：https://modelcontextprotocol.io/development/roadmap
