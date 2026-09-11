---
title: "Anthropic 说 DeepSeek 把 1200 万条用户请求转发进了 Claude"
date: 2026-09-10
lang: zh
source: https://clauday.com/zh/article/ebf0dd10-9aa6-44f8-ad43-448205a6b7c0
tags: [Research, Agents, Monitoring]
---

# Anthropic 说 DeepSeek 把 1200 万条用户请求转发进了 Claude

> 来源 / Source: https://clauday.com/zh/article/ebf0dd10-9aa6-44f8-ad43-448205a6b7c0

9 月 10 日 Anthropic 发布 9 月威胁情报报告，覆盖 2025 年 12 月到 2026 年 8 月拦下的滥用，分七类危害。其中六类是熟悉的阴暗清单：网络攻击、监控、影响力行动、常规武器、生物滥用、诈骗。第七类会被吵好几周。Anthropic 直接点名中国实验室，指控他们把自己用户的流量转发进 Claude 来偷能力。

核心案例编号 GTG-16001，指控 DeepSeek 用一种针对 Claude thinking 签名的 replay 技术，在用户不知情的情况下把请求转发给 Claude Opus。2026 年 7 月的 14 天里 1210 万次交互。Anthropic 说抓到的内容里包括一个俄罗斯政府数据库和一个中国警方案件管理系统的有效凭据，这意味着这个指控不只是蒸馏，是第三方的机密通过一根没人同意过的管子流走了。智谱被指控在 GLM 5.3 发布前十天里，通过一个思维链清洗器推了 770609 次交互。小米，1500 多个账号，40 多万次请求。

agentic 网络攻击那一节其实更吓人，但关注度低得多。GTG-20006 是俄罗斯间谍组织，用 AI 做自主恶意软件开发、规避和数据外泄，打了 20 多个乌克兰和欧洲目标。ShinyHunters 从 180 万个安卓 APK 里刨凭据。GTG-10007 下的中国操作者把漏洞研究、利用和情报收集跑成了并行的自主 agent。这些不是有人找聊天机器人帮忙，这些是循环。

报告在 https://www.anthropic.com/threat-intelligence-report-september-2026

在全盘接受之前先去看 HN 那条讨论。热评很不客气而且不算无理：Anthropic 凭什么对国家级行为者有这么高的可见度，薄利的中国服务商为什么会付 Claude 的价格去服务自己的用户，还有报告顺便解释了竞争对手的跑分是不是太巧了。Anthropic 那份反制清单，元数据归因、抽取分类器、内部推理摘要、身份验证，同时也是一份产品路线图。两件事可以同时成立：转发式蒸馏这个攻击在技术上真实存在而且事后看理所当然，而一份点名三个竞争对手的威胁报告从来不是纯粹的公共服务。

相关阅读：https://clauday.com/article/91ec5364-c24d-4acc-be8b-35e91b0f085f
