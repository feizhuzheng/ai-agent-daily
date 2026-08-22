---
title: "DeepSeek 终于给 Agent 装上了眼睛"
date: 2026-08-21
lang: zh
source: https://clauday.com/zh/article/4dc234fc-a729-4b4a-92c1-a2823cc9b0f4
tags: [Agents, API]
---

# DeepSeek 终于给 Agent 装上了眼睛

> Source: [clauday.com](https://clauday.com/zh/article/4dc234fc-a729-4b4a-92c1-a2823cc9b0f4)

DeepSeek 8 月 21 日发布了 V4-Flash-Vision-Exp，几小时内 Hacker News 冲过 430 分。这是 V4 Flash——V4 家族里更小更快的那一半——的多模态版本，也是 DeepSeek 第一次真正下场视觉赛道。

参数是经典的 DeepSeek 配方：稀疏 MoE，284B 总参数激活 13B，上下文窗口拉满 1,048,576 token，价格让人怀疑看错了小数点——OpenRouter 上输入每百万 token 0.22 美元，输出 0.66 美元。官方说法是在多模态 agent 基准上接近 Claude Opus 4.8，文本、推理和 agent 能力与基础版 Flash 持平。

这句话里真正干活的词是 agent。它的定位不是一个能看你度假照片的聊天机器人，而是文档理解、图表阅读、视觉问答、图文交错的 agent 工作流——翻译过来就是解析截图、操作 GUI、啃 PDF。这些是 computer-use agent 一天到晚在干的事，也是目前哪怕周边文本任务很便宜、你也不得不路由到昂贵西方模型的地方。

输入百万 token 两毛二美元，窗口一百万，意味着你可以让 agent 什么都看、一直看。如果基准数字站得住——它挂着 experimental 标签，等独立测试落地——视觉 agent 的成本地板直接砸穿地下室。这是 DeepSeek 每次的固定动作，而且每次都奏效。

模型信息：https://api-docs.deepseek.com/ OpenRouter 页面：https://openrouter.ai/deepseek/deepseek-v4-flash-vision-exp
