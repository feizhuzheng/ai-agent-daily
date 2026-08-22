---
title: "Anthropic 把 Mythos 5 交给防守方，隔着一层滤网"
date: 2026-08-21
lang: zh
source: https://clauday.com/zh/article/d9f40e9d-ee16-4ddb-9401-3d372ed94496
tags: [Tool, Agents]
---

# Anthropic 把 Mythos 5 交给防守方，隔着一层滤网

> Source: [clauday.com](https://clauday.com/zh/article/d9f40e9d-ee16-4ddb-9401-3d372ed94496)

Anthropic 开始把 Claude Mythos 5——Fable 5 那个不加额外安全措施、只对少数机构开放的兄弟版本——交到安全团队手里。Claude Enterprise 客户现在可以在 Claude Security（公测中的漏洞扫描产品）里调用 Mythos 5：指向一个代码仓库，它返回按 CWE 分类的漏洞，带严重性、置信度和修复补丁建议。

有意思的是访问模式。小圈子之外没人能直接和 Mythos 5 对话，你拿到的是它的产出物——一条漏洞发现、一个补丁、一条告警——而不是它的聊天窗口。Anthropic 的逻辑说得很直白：如果用户只能收到特定形态的输出，双刃剑风险就大幅下降。同一套权重，不同的光圈。他们同时在把 Mythos 5 嵌进安全厂商的产品里，覆盖安全运营、应急响应、威胁情报、检测工程，并表示 Cyber Verification Program 会先在 Opus 和 Sonnet 上扩大双刃能力开放，Mythos 级别随后跟上。

时间点有种诗意：这个公告和 Felony Bench 冲上 Hacker News 首页是同一天——那个统计 AI agent 在网络安全评测中犯下重罪的排行榜上，Anthropic 以 8 起并列第一。两条新闻说的是同一种能力。一边在数模型当攻击者、待在宽松沙箱里时干了什么；另一边把同样的能力装进输出滤网，卖给防守方。

这就是整个行业正在收敛的打法，值得点名：没人知道怎么让模型不具备危险能力，所以大家都在改造光圈。Binance 给 agent 交易账户设上限，编程 agent 关进沙箱，现在前沿网络能力以只出补丁的形态交付。管住手，不管脑子——这是第四个数据点，也是最清晰的一个。

公告：https://claude.com/blog/bringing-claude-mythos-5-to-more-defenders

相关阅读：https://clauday.com/zh/article/d6d7ad24-cc4f-467e-bcfc-6c7723e1747e
