---
title: "magnitude 对 agent 成本战的回答：0 美元，烧自家显卡"
date: 2026-09-06
lang: zh
source: https://clauday.com/zh/article/7afcead0-1924-4555-a77b-534b57ae6127
tags: [Infrastructure, Open Source, Tool]
---

# magnitude 对 agent 成本战的回答：0 美元，烧自家显卡

> 来源 / Source: https://clauday.com/zh/article/7afcead0-1924-4555-a77b-534b57ae6127

magnitude（https://github.com/magnitudedev/magnitude）正在真正地爆发：3,600 star 的底子上单日涨 604，是今天 trending 榜上速度体量比最高的仓库。它是个 Apache-2.0 的本地推理服务器，干一件很具体的事——扫描你的硬件配置，推荐并下载真装得下的 GGUF 权重，本地起服务，然后接进你已经在用的 agent CLI。支持列表基本等于全员：Claude Code、Codex、Cline、OpenCode、OpenClaw、Pi、Hermes。

时机解释了速度。过去两周是实验室在 agent 循环成本上贴身肉搏——Anthropic 砍缓存价、Google 搞促销定价、OpenAI 赌 token 效率。magnitude 是社区从价格表外面给出的回答：循环跑在自己的芯片上，边际 token 成本就是零。隐私和离线算附赠。

诚实的提醒：消费级显卡上的本地 GGUF 干不过前沿模型的硬推理，谁说能就是在卖东西。现实的打法是分流——起草、lint、摘要、写测试放本地，真正要紧的时刻才升级到贵模型。这恰好是 Spotify 刚用"便宜实习生"模式在生产环境验证过的架构，附带 90% 的 token 节省。Apple Silicon 那头有 oMLX（https://clauday.com/zh/article/73bb73f5-e4a7-499d-ab19-7312b166b6e6），其余硬件这头有 magnitude，"agent 底下垫一层本地推理"这个货架正在快速补齐——它正在变成 agent 循环预算里的一个常设科目。
