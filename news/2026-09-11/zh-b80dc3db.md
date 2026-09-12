---
title: "EvoSafeHarness：护栏应该是定制的，不是通用的"
date: 2026-09-11
lang: zh
source: https://clauday.com/zh/article/b80dc3db-4fc8-45ef-8d45-36223640097c
tags: [Research, Agents, Infrastructure]
---

# EvoSafeHarness：护栏应该是定制的，不是通用的

> 来源 / Source: https://clauday.com/zh/article/b80dc3db-4fc8-45ef-8d45-36223640097c

今天 HuggingFace 每日论文榜第一是 EvoSafeHarness，arXiv 2609.05903，作者是 Nanxi Li、Yingzi Ma、Yulong Cao、Edward Suh、李博、Dawn Song 和 Chaowei Xiao。前提那句话，每个在做 agent 的人都该坐下来想想：现有的 harness 通常由专家一次性设计好，然后套在异构的模型和领域上。一套安全配置，所有模型，所有部署。这显然是错的，而且几乎人人都在这么干。

他们做的是一个合成循环，把自然语言策略和可执行代码逻辑联合优化，针对特定模型、特定领域、特定对手来拟合。策略和代码一起优化是对的选择，因为纯文字策略会漂移，而纯代码表达不了意图。数字站得住：DecodingTrust-Agent 上攻击成功率从 45.6% 降到 10.0%，效用损失很小；AgentDojo 上做到 0% 攻击成功率的同时保住 82.8% 效用，大约是同等安全水平下对比方法的两倍。在精修预算受限的自适应攻击下，平均攻击成功率保持在 20% 以下。https://arxiv.org/abs/2609.05903

基准表格底下那个发现，对实践者更有用：执行强度取决于部署。同一条策略，不同模型需要不同的执行力度，因为一个模型对某种措辞能稳稳拒绝，换个措辞就跪了。不同领域需要不同形状的策略。推论是，一个安全厂商把同一套加固 harness 卖给所有客户，等于卖了一个对一半客户过度限制、对另一半千疮百孔的东西。

把它和 Ecdysis 放一起看——同一周出来的那篇，主张 harness 优化应该批量化并且考虑泛化。两篇论文说的是同一件事：harness 是一个拟合出来的产物，不是一个固定的东西。这跟大多数团队对待自己 agent 脚手架的姿态很不一样，后者基本是「三月份某人写的一个配置文件」。

相关阅读：https://clauday.com/article/59e92235-8f6c-4768-81c5-7c42bc384d1a
