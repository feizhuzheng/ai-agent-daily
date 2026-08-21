---
title: "币安 Agent OS：最大的交易所把钥匙交给了 agent"
date: 2026-08-20
lang: zh
source: https://clauday.com/zh/article/6a3faee2-2572-4fb8-a767-78f405550082
tags: [Agents, Infrastructure]
---

# 币安 Agent OS：最大的交易所把钥匙交给了 agent

> Source: [clauday.com](https://clauday.com/zh/article/6a3faee2-2572-4fb8-a767-78f405550082)

币安 8 月 20 日上线 Agent OS：AI agent 可以在全球最大的加密货币交易所里分析行情、直接下单了。集成方式是最有意思的部分——它把币安的 API、钱包服务和交易验证直接插进 ChatGPT、Claude Code 和 Cursor，也就是人们已经在跑 agent 的那些工具里，而不是再造一个私有 agent 产品。

安全设计全部压在账户层：agent 用独立子账户加细粒度权限，提币默认封死，用户自选逐笔审批还是完全自主，外加硬顶——DeFi 交易每日 10 万美元，兑换 5 万，支付 20 美元。币安副总裁 Jeff Li 把实话说出来了：推理发生在币安系统之外，在你的电脑上或你选的 AI 应用里，交易所对 agent 为什么决定交易零可见。提示词注入或者被投毒的数据源影响一个实盘交易 agent，没人当这是假设——限额存在的官方理由就是它。

Kraken、Coinbase、OKX 都发了类似的 MCP 交易接口，这已经是一个品类了，而且设计模式在所有家收敛成同一个：既然没人能审计 agent 的脑子，那就捆住它的手。账户层上权限、子账户、限额，盒子里面随便自主。这跟 coding agent 圈用沙箱得出的结论一模一样，只不过这次独立推导出来的人，赔的是真钱。

要盯的数字不是功能列表，是一年后交易所成交量里有多大比例来自 agent 子账户。钱是迄今为止交给 agent 的最可度量的领域。

https://techcrunch.com/2026/08/20/binance-now-lets-ai-agents-trade-but-keeping-them-in-check-is-largely-up-to-users/
