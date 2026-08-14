---
title: "强模型给弱模型搭个 harness，弱模型就变聪明了"
date: 2026-08-13
lang: zh
source: https://clauday.com/zh/article/4d4c8cb9-1600-454d-9bd4-8e8d3d08a38f
tags: [Research, Agents, Framework]
---

# 强模型给弱模型搭个 harness，弱模型就变聪明了

> Source: [clauday.com](https://clauday.com/zh/article/4d4c8cb9-1600-454d-9bd4-8e8d3d08a38f)

这是一个说得很直白的好想法。能不能不动一个参数，把大模型的能力转移给小模型？能，在推理阶段做，让强模型去搭弱模型运行其中的那个 harness。论文叫 AI4AI at Test-Time，HuggingFace 92 赞，来自 UIUC 和 Salesforce Research。

做法是：一个 builder 模型用 5% 的验证数据，分几轮迭代打磨给目标模型用的推理期 harness。在 Theory-of-Mind 系列 benchmark 上，目标模型的表现从 0.49 涨到 0.91。接近翻倍。没有微调，没有蒸馏，全程没有梯度。

收益从哪来是论文最诚实的部分，也比那个数字听起来更不神奇。三个来源：把不稳定的推理卸载到确定性代码里、针对 benchmark 的路由、以及严格的答案格式约束。换句话说，强模型搞清楚了任务里哪些部分不能信任弱模型，然后写代码把这些部分自己做掉。这其实不算能力转移，算能力替换，就该这么描述。这也意味着那个针对 benchmark 的路由部分，泛化性大概率比标题暗示的差不少。

有两个发现能扛过这个折扣，值得留着。弱模型获益最大，这在经济上是有用的那个方向。以及 builder 模型的推理投入与 harness 质量单调正相关，也就是说在一次性的搭建上多花钱，稳定换来一个更好的永久 harness。平台效应相比 builder 能力则很小，意思是谁来搭远比搭在什么上面重要。

跟今天发布的 DeepSeek Harness 放一起，一幅图就出来了。如果 harness 是一张可替换的插件图，而强模型能写出这张图，那下一步显而易见、却还没人做出来：花一次钱让 Opus 把脚手架写好，然后永远在里面跑 Haiku。

arXiv 2608.12307，Cheng Qian 等，无代码链接。
