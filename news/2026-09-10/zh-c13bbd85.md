---
title: "OpenAI 现在替你跑 agent 循环了"
date: 2026-09-10
lang: zh
source: https://clauday.com/zh/article/c13bbd85-af80-44d3-9337-a8446a0f017c
tags: [Agents, Infrastructure, API]
---

# OpenAI 现在替你跑 agent 循环了

> 来源 / Source: https://clauday.com/zh/article/c13bbd85-af80-44d3-9337-a8446a0f017c

9 月 10 日 OpenAI 把 Agents API 放进公开测试，宣传语很短：用 Codex harness 构建和运行云端 agent，全托管。编排、长会话、上下文管理，OpenAI 全包。你只管真正属于你的那部分。

最后这句话就是整个战略动作。过去两年 agent 领域最有意思的活儿全是 harness 的活儿，说白了就是循环设计、上下文压缩、工具路由、重试策略、会话持久化。几十家公司存在的理由就是这一层难而且没人占。OpenAI 现在宣布这层归他们了，定价零。不额外收费，你还是只付 token 和工具钱。

同时发布的是托管沙箱，OpenAI 直接提供执行环境，让 agent 跑代码、动文件、产出物料。CPU、GPU、内存、存储、密钥管理都能选。值得注意的是他们没关门：你也可以指向自己的沙箱，或者 Blaxel、E2B、Modal、DigitalOcean、Vercel。容器按标准容器价单独计费。

文档和申请在 https://openai.com/index/introducing-the-agents-api/

HN 上的讨论很小，34 分，这说明这条东西是当基础设施落地的，不是当新闻。商品化从内部看就是这个样子。如果你的产品是那个循环，那这个循环现在是卖你 token 的那家公司提供的免费托管服务。如果你的产品是 agent 知道什么、被允许碰什么、出事了谁负责，今天是个好日子。
