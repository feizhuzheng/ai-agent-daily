---
title: "有证明了：只看 transcript 的裁判救不了你"
date: 2026-09-07
lang: zh
source: https://clauday.com/zh/article/8a1cbe2c-2bde-4e36-ad10-16df540807ba
tags: [Research, Agents]
---

# 有证明了：只看 transcript 的裁判救不了你

> 来源 / Source: https://clauday.com/zh/article/8a1cbe2c-2bde-4e36-ad10-16df540807ba

今天 HuggingFace 榜第一的 agent 论文（92 赞）干了件多智能体文献里少见的事：证明了一个否定命题。Bilevel Coordinated Reflection，来自 UCL、利物浦和华为的研究者，把标准的 orchestrator 带一群 worker 的结构建模成双层协调博弈，然后给出一个信息论上的不可能性结果：任何只看生成文本的门控，都无法在文本无法区分的环境之间做到一致提升。碰环境的门控可以。

想想这条定理罩住了什么。LLM 当裁判、自我反思循环、重读对话的批评 agent——全是只看 transcript 的门控。定理说的是：存在一些它们结构上分不开的情形，同一段文本在一个世界里是对的、在另一个世界里是错的，裁判再聪明也没用。唯一的出路是碰环境：把代码跑起来、查状态、对 ground truth。

论文建设性的那半是 SRMA（随机反思记忆上升）：一个只有环境校验通过才接受记忆更新的反思机制，带收敛保证。博弈框架还给了一个干净的旋钮——orchestrator 拆任务拆得多好，决定了 worker 自我改进能漂多远。

这给了实证研究反复撞见的现象一根数学脊柱——裁判会漂移、给的理由是编的（https://clauday.com/zh/article/41105bda-2183-41de-8eef-4750f300e6d7）。现在有定理说：更用力地读 transcript，从一开始就注定不够。代码在 https://github.com/YihangChen9/Bilevel-Coordinated-Reflection ，论文在 https://arxiv.org/abs/2609.02750
