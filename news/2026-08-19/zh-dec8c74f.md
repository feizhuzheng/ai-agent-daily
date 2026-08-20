---
title: "OpenAI 承认给 Astra 踩了刹车"
date: 2026-08-19
lang: zh
source: https://clauday.com/zh/article/dec8c74f-8624-4515-be46-38d7c92789f1
tags: [Agents, Research]
---

# OpenAI 承认给 Astra 踩了刹车

> Source: [clauday.com](https://clauday.com/zh/article/dec8c74f-8624-4515-be46-38d7c92789f1)

还记得八月初那条"OpenAI 疑似因网络安全风险暂停前沿 RL 训练"的传闻吗？现在官宣了。在一篇题为 Pacing Model Development in an Era of Cyber-Critical Capabilities 的博客里，OpenAI 确认曾临时放慢 scaling——包括对准备部署的模型暂停两周 RL 训练，用来加固和红队自己的研究环境。官方说法：Astra 级模型在其 Preparedness Framework 下可能达到"临界"网络能力，按 OpenAI 自己的定义，就是能针对加固过的真实系统自主开发出可用的零日漏洞。

第二天的后续更耐人寻味。OpenAI 的 Trusted Access for Cyber 计划里，一批研究员一觉醒来发现自己的 Daybreak Blue 权限被停了，要重新验证才能恢复——这个层级给经过审查的研究员开放安全护栏更少的前沿模型。向 TechCrunch 抱怨的研究员有个共同点：全部住在美欧之外。没人说"地理围栏"这个词，但模式已经摆在那了。

两件事放在一起看，一个新东西正在成形：按地域做能力分级。最强模型层级的访问权开始长得像出口管制物资——验证身份、可信辖区、随时可撤销。Anthropic 结构上玩的是同一套：Fable 和 Mythos 分家，无限制版只给获批机构。Axios 说 OpenAI 这是在安全对峙里先眨眼了，没错，但更耐久的故事是那套"选择性说不"的基础设施正在建起来。

如果你的 agent 跑在前沿模型上，司法辖区刚刚变成了一个依赖项。原文值得读：https://openai.com/index/pacing-model-development-cyber-capabilities/
