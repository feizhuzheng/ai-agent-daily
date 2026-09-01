---
title: "Simon Willison 让 ChatGPT Work 自己交出了说明书"
date: 2026-08-31
lang: zh
source: https://clauday.com/zh/article/9deb3dfc-80b9-49f3-9994-b7033c46c2b2
tags: [Skills, Agents, Coding]
---

# Simon Willison 让 ChatGPT Work 自己交出了说明书

> 来源 / Source: https://clauday.com/zh/article/9deb3dfc-80b9-49f3-9994-b7033c46c2b2

Simon Willison 干了件很有他风格的事：让 ChatGPT Work 把自己内置的所有工具和技能列成清单，排成一个技术文档站，再用 ChatGPT Work 自带的建站功能托管出来。结果就是一份 OpenAI 自己从没公开过的 agent harness 快照，8 月 31 日版本：232 个工具接口、44 个技能定义，地址 https://codex-tool-reference.simonw.chatgpt.site/。他自嘲这是个"vibe-coded slop site"，Hacker News 照样给了 157 分，因为内容是真金白银。

数字直接暴露了 OpenAI 认为 agent 该在哪干活：232 个工具里 89 个是 GitHub 操作。光是子 agent 协调就有 6 个工具，负责派生、传消息、打断。再加上定时任务、webhook、Gmail、日历、表格。HN 上有人一句话总结：桌面版 ChatGPT Work 就是换了层皮的 Codex。

更有意思的是那 44 个技能。它们叠在工具层之上：做文档、做数据分析、控制浏览器，甚至还有一个"创建新技能"的技能。工程师们最欣赏的一个设计细节：浏览器技能没有把 Playwright 文档整个塞进上下文，而是留到运行时用 browser.documentation() 现取，agent 真要上网了才付这笔上下文的钱。这个省 context 的手法值得抄。

往后退一步看，这是一个月内第二次有人把前沿实验室的 harness 拍了 X 光片。上一次是 Anthropic 的 Project Glasswing 发布说明（https://clauday.com/zh/article/14f45441-d451-4e3d-bdb5-55714515403d）。而这里的技能层，结构上和 Anthropic 的 Agent Skills 一模一样，就是 K-Dense 刚刚围着改名的那个标准（https://clauday.com/zh/article/af6b3f66-e376-4257-a402-2624848493c3）。两家实验室，一种"专业知识打包格式"。收敛已经不是预测了，是两边都上线了的产品。
