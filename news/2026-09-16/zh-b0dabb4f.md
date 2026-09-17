---
title: "腾讯这个知识平台不做 RAG 了，改做 agent"
date: 2026-09-16
lang: zh
source: https://clauday.com/zh/article/b0dabb4f-ea8e-4c92-9ff3-6a0fbe8bc43d
tags: [Agents, Framework, Open Source]
---

# 腾讯这个知识平台不做 RAG 了，改做 agent

> 来源 / Source: https://clauday.com/zh/article/b0dabb4f-ea8e-4c92-9ff3-6a0fbe8bc43d

腾讯的 WeKnora 一天涨了约 1200 星，冲到 2.5 万，原因是 v0.8.0 已经不再是一个挂了聊天框的检索系统。它有一个 ReAct agent，跨多步编排检索、工具、沙箱和网页搜索；还有一个 Wiki 模式，让 agent 把你的文档写成一套结构化、互相链接的 Markdown wiki，带版本历史，人可以在上面改。MIT，仓库在 https://github.com/Tencent/WeKnora 。

Wiki 模式是个有意思的赌。别人都是按需答题，然后把推理过程扔掉。WeKnora 把知识库物化成会留存、互相链接、懂行的人能直接改的页面。这让语料变成一件你团队真会去读的东西，而不是一个必须一句一句去审问的神谕，也意味着一个错答案改一次就完了，而不是被永远重新生成。

剩下的部分读起来像是有人把它部署进大公司然后被骂过。Skill 沙箱在 Docker、E2B 或 Cube 上按会话持久，带按租户的网络策略。长期记忆跨会话保留画像、偏好和事实。四级 RBAC，资源级归属，审计日志，工作区维度的 API key 带能力级管控。导入能从飞书、GitLab、Notion、语雀、RSS 自动同步，支持二十多家模型提供方，包括 OpenAI、DeepSeek、Qwen、Claude 和 Ollama。

所有东西都可换：向量库、存储、模型提供方，部署支持本地、Docker、Helm 和私有云。MIT 协议加完整数据主权再加飞书语雀连接器，这个组合告诉你它是给谁做的，而那个市场里没有人会把内部文档发去美国的 API。值得盯的是「wiki 作为产出」这个想法会不会被西方的 RAG 厂商抄走，因为对于「一个知识库应该留下什么」这个问题，这是目前最好的答案。
