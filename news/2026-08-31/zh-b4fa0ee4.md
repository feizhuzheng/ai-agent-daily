---
title: "OpenAI 在成千上万台地买 Mac mini"
date: 2026-08-31
lang: zh
source: https://clauday.com/zh/article/b4fa0ee4-7221-4871-918f-338c381a9aa2
tags: [Infrastructure, Agents]
---

# OpenAI 在成千上万台地买 Mac mini

> 来源 / Source: https://clauday.com/zh/article/b4fa0ee4-7221-4871-918f-338c381a9aa2

苹果 8 月发布了新款 Mac mini 和 Mac Studio。苹果从来不在 8 月发 Mac，那个档期属于十月或十一月。The Information 的报道解释了这次反常：企业级 AI 需求把苹果打了个措手不及，光 OpenAI 一家就买了数以万计的 Mac mini 和 Mac Studio，用来跑强化学习和操作电脑的 agent。很多配置已经断货几个月，另一头还有全球内存短缺在挤压。这条今天在 Hacker News 上挂到 231 分。

好笑的地方在于：这一切苹果完全没计划过。按报道说法，订单涌进来的时候，公司既没有服务企业客户的工程团队，也没有企业 AI 战略。新 Mac Studio 的卖点是把几台机器串成一个能跑前沿大模型的集群，明摆着是冲那批它之前不知道存在的买家去的。苹果被嘲笑错过 AI 两年，结果它的芯片靠着每美元内存的数学，稀里糊涂成了本地 agent 的默认底座。

这个故事的软件那一半我们昨天刚写过：Superagent 给 agent 一台真电脑（https://clauday.com/zh/article/40faf35d-e494-4b82-9d30-477d917fb00f），oMLX 把本地 MLX 推理修到编码 agent 能用（https://clauday.com/zh/article/73bb73f5-e4a7-499d-ab19-7312b166b6e6）。今天补上的是硬件需求曲线，而且排队的不只是玩家：全世界最大的 AI 实验室跟你站在同一条收银线上。agent 需要自己的电脑，就总得有人卖电脑。

报道：https://www.macrumors.com/2026/08/30/apple-unexpected-mac-mini-and-studio-demand/
