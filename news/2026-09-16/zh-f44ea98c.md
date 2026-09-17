---
title: "Cloudflare 把「让你的 agent 变成安全审计员」这套东西开源了"
date: 2026-09-16
lang: zh
source: https://clauday.com/zh/article/f44ea98c-3c8a-47b5-b6ee-e7731f04cf0c
tags: [Skills, Agent-Operable, Open Source]
---

# Cloudflare 把「让你的 agent 变成安全审计员」这套东西开源了

> 来源 / Source: https://clauday.com/zh/article/f44ea98c-3c8a-47b5-b6ee-e7731f04cf0c

Cloudflare 把 security-audit-skill 放上了 GitHub，一天涨了约 1250 星到接近 7000。MIT 协议，一行装完，干的事是把一个编码 agent 拖着走完六阶段安全审计，而不是客客气气地请它找 bug：侦察、以覆盖为导向的狩猎、候选验证、结构化输出、独立复核、目标中立的报告。仓库在 https://github.com/cloudflare/security-audit-skill ，用 npx skills add 装，然后说一句「审一下这个代码库的安全」。

值得抄走的设计是：findings 由不是发现它的那个 agent 来复核。一个跟这条结论毫无利害关系的新 agent 重新查一遍，才能被标成 confirmed；其余的要么落到 needs_validation 并把未决问题写清楚，要么落到 rejected 并记录为什么被推翻。这是在治 agentic 安全工作最大的失败模式——不是漏报，而是一串听上去都挺有道理的发现，吃掉人类一周去分诊。

另一半是按 JSON schema 做结构化输出。侦察阶段写出机器可读的覆盖笔记，于是「这块我们看过没有」变成一次查询而不是一种感觉，狩猎阶段按覆盖薄的地方派活，而不是模型想戳哪就戳哪。谁把 agent 扔进过大代码库都知道，它能心满意足地反复审同样那三个文件。

更重要的是发布者是谁。Cloudflare 把自己内部的审计方法论当成一个 skill 文件发出来，MIT，才十四个 commit，这是迄今为止最硬的证据：安全实践现在就是靠 skill 格式分发的。被开源的不是代码，是流程，而流程恰恰是 agent 一直缺的东西。接下来别的基础设施厂商会跟，第一场争论大概会是：一个真挖出 CVE 的 skill，算安全工具还是安全产品。

相关阅读：[一个开源模型花 4.65 美元打穿了全部十一个靶子](https://clauday.com/zh/article/52559c6b-0bae-4fd0-971d-9f69ef7ff7ce)
