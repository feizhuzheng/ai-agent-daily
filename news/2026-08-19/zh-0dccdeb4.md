---
title: "Agent Lightning 1.0：带着 harness 一起做 RL"
date: 2026-08-19
lang: zh
source: https://clauday.com/zh/article/0dccdeb4-cbb3-45c1-b5e3-de9a1f51fba1
tags: [RL, Framework, Open Source]
---

# Agent Lightning 1.0：带着 harness 一起做 RL

> Source: [clauday.com](https://clauday.com/zh/article/0dccdeb4-cbb3-45c1-b5e3-de9a1f51fba1)

给 agent 模型做 RL 训练的标准做法：把部署用的 harness 拆掉，在无菌循环里训裸模型，训完再把 harness 装回去，祈祷能力能迁移过来。微软研究院团队的 Agent Lightning v1.0 说这套流程是反的。他们的词叫 harnessed agentic RL：部署时管工具、上下文、控制流的那个 harness，直接参与后训练。你训的就是你要发货的那个东西。

工程上是一套解耦架构：任何 agent 通过一个 LLM endpoint 代理接进 RL 训练，agent 本身不用重写。真正杀死这类项目的脏活——retokenization、样本合并、advantage 计算、loss 归一化、后端调度——全在框架里处理掉了，整个框架大约 3500 行代码，完整工作流和训练脚本都放出来了。

头条数字：Qwen3.5-9B 在 SWE-bench Verified 上从 41.8% 拉到 56.4%，涨 14.6 个点，只用了 6000 条训练样本和不大的算力。9B 模型在 Verified 上过 56，几个月前还是大得多的模型的领地；而样本效率恰恰说明，带着 harness 训练捕捉到了裸模型 RL 漏掉的东西。

这已经是一波浪潮，不是一篇论文了。DeepSeek 上周发了 Harness v0.1，同一天的日榜上 LEGO-RL 自称 harness-native，共同论点就一句话：agent 的能力长在模型加 harness 这个系统里，所以训练单位就该是这个系统。arXiv：https://arxiv.org/abs/2608.17528
