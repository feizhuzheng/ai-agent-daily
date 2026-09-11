---
title: "Show-Harness 说机器人不缺模型，缺的是接口"
date: 2026-09-10
lang: zh
source: https://clauday.com/zh/article/de5fde4d-f6da-47ca-bf16-ba01dbc5bc56
tags: [Research, Agents, Framework]
---

# Show-Harness 说机器人不缺模型，缺的是接口

> 来源 / Source: https://clauday.com/zh/article/de5fde4d-f6da-47ca-bf16-ba01dbc5bc56

Show-Harness 在 HuggingFace 论文页拿到 125 票，当天第一，标题本身就是冲着整个 vision-language-action 领域去的：一个 VLM agent 就能玩机器人。不用针对具体形体的预训练，不用 VLA 模型，不用遥操作台。它的主张是，基座模型在机器人上表现差，是因为我们一直递给它错的接口。

设计是离散语义动作单元，也就是 VLM 真的能用语言推理的那种动作，再配上每种形体各自的解释器，把这些单元翻译成硬件实际有的关节和夹爪。VLM 留在物理决策循环里，而不是被降级成一个高层规划器然后把活扔给策略网络。由此掉出来三件事：闭源前沿模型可以零样本控制机器人，小的开源模型可以低成本微调进来，跨形体迁移能work因为语义层是共享的。他们还做了 GUMI，一个 GUI 操作接口，不用专门的遥操作硬件就能采演示数据，顺手把机器人数据采集里最贵的那部分给解了。

论文报告在多种任务、形体和环境上超过了可比的 agentic 和 VLA 范式。他们给出的结论值得直接拿走：对的接口能从基座 VLM 里解锁出可观的具身能力。

arXiv 2609.10522，9 月 9 日提交，项目页 https://showlab.github.io/Show-Harness

这是 harness 论点打进机器人领域了。过去一年同样的争论在编程 agent 和研究 agent 里反复上演，收益来自循环和接口设计而不是权重，每个月都有人拿更小的模型配更好的 harness 打赢更大的模型。具身本来被认为是例外，是那个你真的需要新预训练的地方。如果 Show-Harness 经得起复现，那它也不是例外。
