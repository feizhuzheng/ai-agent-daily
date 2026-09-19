---
title: "扫了 176 种 harness 配置之后：强模型只给 bash，然后让开"
date: 2026-09-18
lang: zh
source: https://clauday.com/zh/article/ad45df57-8be4-4c28-8947-09ac7fb0bea4
tags: [Agents, Benchmark, Research, Coding]
---

# 扫了 176 种 harness 配置之后：强模型只给 bash，然后让开

> 来源 / Source: https://clauday.com/zh/article/ad45df57-8be4-4c28-8947-09ac7fb0bea4

一篇 43 页的论文在 SWE-Bench Verified 和 Terminal-Bench 2.1 上扫了 176 种 harness 配置、四个模型，把所有人都在凭感觉调的三个旋钮单独拎出来测：上下文管理、规划、动作空间。arXiv 2609.20804，9 月 17 日提交，Run-Ze Fan 等八位作者，署名带 Zoom Communications。一天冲到 Hacker News 194 分，说明这个问题有多缺真实测量。

动作空间那条结论是可以马上照做的。预定义工具能帮到 bash 能力弱的模型；能力强的模型只给 bash 也一样好，而且成本明显更低。也就是说，大多数 harness 精心铺开的那一大片工具面，是给你没在用的那个模型准备的拐杖，而你每一轮都在为它付 token。规划呈现同样的形状：它把弱模型撑到能干活，对强模型则是纯降成本、准确率一点没变。两个旋钮，同一种形状，正确设置取决于你派了哪个模型上场，而不是抽象意义上哪种做法更好。

上下文管理是唯一表现不同的那个。可用上下文越紧它越重要，而且它买到的主要不是更聪明的行为，是"不因溢出而失败"。作者发现先做基于规则的删减、再做 LLM 摘要，整体效率最高。翻译成人话：能用确定性方法扔掉的先扔掉，只为活下来的那部分付模型的钱。

轨迹分析那一段是我会念给任何一个从零设计 harness 的人听的。上下文管理决定 agent 能跑多久，规划决定它在哪停，动作空间决定它改代码的颗粒度。三根杠杆对应三个互不相干的性质，这是目前公开发表的东西里最接近一个心智模型的。论文在 https://arxiv.org/abs/2609.20804，没放代码仓库，这是它唯一真正的缺口。

相关阅读：英伟达 SoL-Pi https://clauday.com/zh/article/52632835-5b57-4091-b33d-fa88ff320d42
