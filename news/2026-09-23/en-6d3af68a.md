---
title: "Nine agents argue about your stocks for five cents"
date: 2026-09-23
lang: en
source: https://clauday.com/article/6d3af68a-dbe7-4b65-91a9-8e7d76adbef3
tags: [Agents, Open Source, Tool]
---

# Nine agents argue about your stocks for five cents

> 来源 / Source: https://clauday.com/article/6d3af68a-dbe7-4b65-91a9-8e7d76adbef3

PanWatch (盯盘侠) is a self-hosted stock monitoring assistant, MIT licensed, 1.5k stars, trending on GitHub today at 142 a day. What makes it worth a look isn't the stock part, it's the cost line: roughly five cents per analysis.

It wires the TradingAgents multi-agent framework into a monitoring loop over A-shares, Hong Kong, and US equities. Nine agents form an investment research team, argue about the outlook, run a risk review, and produce a PM decision document in three to five minutes, then push the conclusion to Telegram or WeChat. Separate agents handle pre-market strategy, intraday anomaly detection, post-market review, and news aggregation. Technical analysis covers trend indicators like MACD and Bollinger Bands, momentum signals like RSI and KDJ, and pattern recognition.

FastAPI backend with SQLAlchemy and APScheduler, React 18 and TypeScript on the front, one-command Docker deploy, multiple broker accounts, optional OpenTelemetry export. It takes any OpenAI-compatible endpoint, and the five-cent figure comes from running it on DeepSeek.

The reason this belongs here and not in a finance roundup: it is a clean, cheap, reproducible instance of a pattern everyone keeps proposing and few people price. A structured debate among specialized agents producing a written decision, on a schedule, for a nickel. Whether nine agents arguing beats one agent thinking is genuinely unsettled — adversarial multi-agent setups often just generate more confident-sounding text — but at this cost you can actually run the experiment against real outcomes and find out.

Obvious warning, which the project does not make for you: this produces a decision document, not a decision. An agent debate that concludes in three minutes with nice formatting is not evidence of anything, and the market will happily take money from people who confuse the two.

https://github.com/TNT-Likely/PanWatch
