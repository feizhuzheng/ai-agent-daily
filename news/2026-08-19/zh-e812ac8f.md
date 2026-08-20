---
title: "Agentic ESOpt：不碰 RL 全家桶，也能调 27B 的 agent"
date: 2026-08-19
lang: zh
source: https://clauday.com/zh/article/e812ac8f-7895-415c-9dc6-7be81726bdc0
tags: [RL, Research]
---

# Agentic ESOpt：不碰 RL 全家桶，也能调 27B 的 agent

> Source: [clauday.com](https://clauday.com/zh/article/e812ac8f-7895-415c-9dc6-7be81726bdc0)

Agent 微调出不了大实验室，卡的不是数据，是 RL 全家桶：长 horizon 反向传播需要的优化器状态和梯度，会把显存需求翻好几倍。HuggingFace 日榜 91 票的新论文 Agentic ESOpt 复活了一个老思路来拆这堵墙：进化策略。围着当前权重采样扰动，让扰动出来的 agent 跑 rollout，按 reward 加权更新。全程没有反向传播。

直接后果：全参数优化只要推理级显存。你能把模型跑起来做推理，你就能调它。作者里有 Yee Whye Teh 和 Wee Sun Lee，他们演示了对 Qwen-3.5-27B 做全参数调优，WebArena-Lite 上比基线涨 6.69%；测试时的提示词-参数协同进化在 36 个设置里赢了 28 个。因为进化策略把 reward 当黑盒，agentic RL 里最折磨人的长程 credit assignment 根本不需要分解 reward——这一局要么得分要么没得分，就这么简单。

要记住的代价：进化策略吃样本，那些扰动 rollout 全是真金白银的推理开销，等于拿显存换 rollout 量。这笔交换恰好适合一类团队：有推理容量、没训练集群——大多数 agent 公司就长这样。

建议和同天出现的 Agent Lightning v1.0 对照着读：一个保留 RL 但把 harness 工程进去，一个干脆扔掉反向传播。攻的是同一堵墙：把一个已部署的 agent 变成可训练的，到底要花多少钱。https://arxiv.org/abs/2608.17310
