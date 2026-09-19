---
title: "Octop：自托管多 agent 助手，直接长在你本来就在聊天的地方"
date: 2026-09-18
lang: zh
source: https://clauday.com/zh/article/22ba6e6e-5ae1-4832-905a-31befb2924dd
tags: [Agents, Open Source, Framework, Infrastructure]
---

# Octop：自托管多 agent 助手，直接长在你本来就在聊天的地方

> 来源 / Source: https://clauday.com/zh/article/22ba6e6e-5ae1-4832-905a-31befb2924dd

Octop 今天冲上了 GitHub 趋势榜，单日涨 571 星，总数越过 3900，405 个 fork。MIT 协议，版本 1.0.0，来自 TencentCloud，地址 https://github.com/TencentCloud/Octop。它的自我介绍是"更聪明的自托管 AI 助手，多用户、多 agent"，而它的形态是一个 Python 3.12 的 FastAPI 单进程，同时供着网页面板、CLI、若干 IM 通道和后台自动化任务。

把它和一堆 agent 框架区分开的设计选择是：它不试图成为一个你要专门去访问的地方。它桥接飞书、钉钉、Discord、企业微信和 QQ，也就是说 agent 长在对话本来就发生的地方，而不是要求你的团队再多开一个标签页。在这之上它还做网页自动化、终端助手和浏览器里的远程桌面。harness 栈拆成 agent 运行时、网关桥接、记忆和浏览器自动化四层，并且讲 ACP，也就是 Agent Client Protocol。

状态默认存在 SQLite，想换 Postgres 也行，放在 ~/.octop/ 下，配多用户 JWT 认证和本地优先路径上的 PII 脱敏。这个组合才是真正的产品：多用户意味着它瞄准的是一个团队或一个家庭而不是某个开发者的笔记本；多用户加自托管加 PII 脱敏，意味着有人认真想过六个人的消息落进同一个 agent 的记忆之后会发生什么。RAG 知识库和插件生态在今天只能算入场券。

唯一让我挑眉的是给 agent 配的 MBTI 人格模板，那是穿着配置文件的流行心理学。把这块忽略掉，剩下的是对一个很多团队正在拙劣提问的问题的一个完整回答：怎么给一群人跑 agent，同时不用把聊天记录和终端交给第三方。挂在腾讯云的组织下、同时用 MIT 协议，这个组合不常见，值得记一笔——因为在战略调整之后，能活下来的是协议。
