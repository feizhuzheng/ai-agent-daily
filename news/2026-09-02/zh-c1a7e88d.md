---
title: "Harness-of-Harness：harness 也有了自己的 harness"
date: 2026-09-02
lang: zh
source: https://clauday.com/zh/article/c1a7e88d-4f79-4a2f-9ce2-9ebfa2cf4481
tags: [Research, Agents, Coding]
---

# Harness-of-Harness：harness 也有了自己的 harness

> 来源 / Source: https://clauday.com/zh/article/c1a7e88d-4f79-4a2f-9ce2-9ebfa2cf4481

光是名字就值得点进去。Harness-of-Harness（HoH），9 月 1 日挂上 arXiv，Haoyang Yan 领衔的九人团队。做法是把现有的编码 agent harness——他们测了 Codex 配 GPT-5.5、OpenCode 配 DeepSeek-V4-Pro、Pi 配 MiniMax-M3——包进一个外层循环：规划、写码、测试，然后下一轮迭代继续改进同一个软件。不是新 agent，是让你手上已有的 harness 连跑好几天的元层。

数字：三个 benchmark 上平均相对提升 52.25%，三轮迭代后最高 82.86%。最抓人的 demo：70 多轮自主迭代做出了一个完整可玩的第一人称射击游戏，有剧情、核心玩法、像样的视觉和音效。设计取舍都很朴素：修 bug 和长能力之间做平衡，把工作切成小的可验证增量，工具和技能渐进开放而不是规定死流程。

这正好接上我们整个季度都在追的线：现在智能增益最便宜的地方就是 harness（参考 HarnessLens 那篇，讲怎么进化 harness 又不烧光评测预算：https://clauday.com/zh/article/737350d4-c375-403c-bf69-6e69838eb434）。HoH 的贡献是证明 harness 本身可以成为被编排的单元——而且同一个外层循环能同时抬起三套完全不同的 harness-模型组合。给包装再包一层就能涨 52%，这个信息其实挺扎心的：模型还有一大截余量，是脚手架没用出来的。

论文：https://arxiv.org/abs/2609.01481
