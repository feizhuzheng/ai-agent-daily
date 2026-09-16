---
title: "Salesforce 自己训了个推理模型，不再给 OpenAI 打电话"
date: 2026-09-15
lang: zh
source: https://clauday.com/zh/article/2eaa788d-e038-4c20-8974-d8c27ed11192
tags: [Agents, Open Source, Framework]
---

# Salesforce 自己训了个推理模型，不再给 OpenAI 打电话

> 来源 / Source: https://clauday.com/zh/article/2eaa788d-e038-4c20-8974-d8c27ed11192

9 月 15 日，Salesforce 和英伟达发布了一个叫 Koa 的推理模型，基于英伟达的开放权重 Nemotron，直接对准 Agentforce 的活——销售、市场、客服。报道见 https://techcrunch.com/2026/09/15/salesforce-and-nvidias-new-reasoning-model-is-everything-the-ai-labs-should-fear/ 。真正会让某个实验室高管放下咖啡杯的，是 Salesforce AI 执行副总裁 Jayesh Govindarajan 的那句话：推理这件事我们一直依赖前沿模型厂商，直到现在。

战略逻辑不在于要打赢 GPT-6。而在于 Salesforce 根本不需要赢。一个企业智能体去关掉一张工单，做的是窄的、重复的、定义清晰的活；干这个活，一个按任务训过的开放权重模型每 token 更便宜、首 token 更快，而且跑在 Salesforce 已有的数据治理框架里，不用再签一份新的供应商合同。Salesforce 还特别强调 Koa 从未吃进真实客户数据，这一条直接消掉了最常搞黄企业单子的那个反对意见。

token 效率是那记闷刀。前沿实验室按 token 收钱，有一万个理由让你的智能体多想一会儿。如果你的供应商就是你的模型提供方，你在这件事上没有任何筹码。而如果模型是你自己的、栈是你自己的，你可以直接拍板：一次客服分流不需要四千个推理 token。乘上 Salesforce 的处理量，省下来的就不是一个科目，是一整笔预算。

这是本周第二次看到同一个模式，只是方向相反。[Jev 的整个论点是大多数生产调用本来就不需要散文模型](https://clauday.com/article/d9b194d4-282e-4954-a4a2-f93fe37522a1)，Koa 的论点是大多数企业推理本来就不需要前沿模型。[Nemotron 从 550B 那一版开始就是为智能体而不是聊天造的](https://clauday.com/article/4dad5d61-7c9e-46d6-b7c6-992376f1d052)，而英伟达的 Kari Ann Briski 把它包装成主权 AI 加首 token 时延加高效推理，已经说明英伟达认为买家是谁了。不是那几家实验室。

接下来要盯的是 Salesforce 会不会公布数字。目前发布里既没有 benchmark 也没有参数量，这是一个选择，而且是个方便的选择。但方向毫不含糊：地球上最大的企业软件厂商刚刚把推理搬回了自己家，底座是开放权重。今早每一家跟英伟达有关系的应用层公司，都在非常仔细地读这份新闻稿。
