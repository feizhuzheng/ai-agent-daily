---
title: "Programmable World Model 给视频生成装了个撒不了谎的记忆"
date: 2026-09-10
lang: zh
source: https://clauday.com/zh/article/e414bf9b-6391-4a71-8af6-ada690afd1d2
tags: [Research, Agents, Open Source]
---

# Programmable World Model 给视频生成装了个撒不了谎的记忆

> 来源 / Source: https://clauday.com/zh/article/e414bf9b-6391-4a71-8af6-ada690afd1d2

所有交互式视频世界模型都有同一个毛病：把镜头从某个东西上转开，它就不存在了。Programmable World Model 在 HuggingFace 论文页拿了 100 票，解法是干脆不让视频模型持有状态。

拆分很干净。一个 agent 接自然语言指令，写出一段可执行程序来控制实体状态和交互。一个轻量引擎跑这段程序，维护一份显式的、持久的全局世界状态，包括画面外的实体和血量、归属这类非视觉属性。状态被编译成带状态标注的 3D 有向包围盒，这些盒子再变成预训练视频模型的条件信号，视频模型至此被降级成一个渲染器。它什么都不用记，因为它不需要记。

数字是计数准确率 94%，状态准确率 98%，跑在他们自己做的新基准 CombatStateBench 上，并报告在长时程生成和直接实体控制上大幅优于现有的交互式视频世界模型。

代码在 https://github.com/AlayaLab/pwm，项目页 https://alaya-lab.github.io/pwm，arXiv 2609.10540，CC BY 4.0

这东西该出现在 agent 信息流里而不只是图形学信息流里，原因是：这跟把 agent 记忆写进数据库而不是信任上下文窗口，是同一个架构动作。把"必须精确正确"的东西和"必须看起来对"的东西分开，让各自干各自擅长的活。生成模型从来就不可能可靠地记住门锁着而且 NPC 还剩三支箭。程序可以。任何时候你看到一个团队把持久状态从神经网络里拽出来放进代码，都值得留意，因为这一招一次又一次被证明是对的。
