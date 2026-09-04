---
title: "openclaude：把 Claude Code 跑在任何模型上，Google 刚好演示了为什么需要它"
date: 2026-09-03
lang: zh
source: https://clauday.com/zh/article/cbb2d949-2ffe-4ef6-bae1-26feb2c01a0f
tags: [Open Source, Coding, Tool]
---

# openclaude：把 Claude Code 跑在任何模型上，Google 刚好演示了为什么需要它

> 来源 / Source: https://clauday.com/zh/article/cbb2d949-2ffe-4ef6-bae1-26feb2c01a0f

openclaude 连续第二天挂在 GitHub trending 上，今天 +453 星，总量 32.3k。它是什么：Claude Code 的开放代码库，被大改到能跑在 20 多家 provider 上——OpenAI、DeepSeek、Groq、Mistral、GLM、Gemini、GitHub Models、Ollama、本地后端，任何 OpenAI 兼容接口都行。一个 CLI，一套工作流，工具、MCP、斜杠命令全都在，你想接哪个模型接哪个，哪个便宜用哪个。甚至还有一个会对你输入做反应的像素小人，很难说不是故意的。

时机替它把论点写好了。openclaude 上榜的同一天，Hacker News 上一条 236 分的帖子：Google Antigravity 的服务条款写着,第三方使用 agent 可能导致整个 Google 账号被封。把这两条并排看：行业的一边在把 harness 焊死在账号体系上，社区的回应是把 harness 从所有厂商手里一次性撬下来。

这是我们写过的 free-claude-code（https://clauday.com/zh/article/a1824da6-bf46-4957-b52b-ca50279eaaa1）那场"绕开前沿"运动的基建版，而且成熟得多：1196 个 commit，provider 配置体系，修改部分 MIT 协议。把 Anthropic 的代码 fork 出来再 MIT 化，法律上确实站在灰色地带，Anthropic 到现在一个字没说。但 32k 星说明需求是真的：大家想要最好的 harness，但不想跟厂商结婚。

仓库在 https://github.com/Gitlawb/openclaude。
