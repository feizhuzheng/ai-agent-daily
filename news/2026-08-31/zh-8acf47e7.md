---
title: "J-Zero：从零数据长出出题人、答题人和裁判"
date: 2026-08-31
lang: zh
source: https://clauday.com/zh/article/8acf47e7-f951-40c9-b4d5-c98b3a6e3ba3
tags: [Research, RL]
---

# J-Zero：从零数据长出出题人、答题人和裁判

> 来源 / Source: https://clauday.com/zh/article/8acf47e7-f951-40c9-b4d5-c98b3a6e3ba3

自我改进循环有一个标准死法：裁判。把 reward model 或者 LLM 裁判焊死，让策略对着它进化，两轮之内策略学会的就不是任务，是裁判本身。KAIST 梁恩镐（Eunho Yang）组的 J-Zero 直接冲这个病根去：谁都不许焊死。Challenger 出越来越难的题，Solver 答题，Judge 学着打分，三个角色从零外部数据开始共同进化。论文：arXiv 2608.26582。

头条不是分数涨幅，虽然也不寒碜：可验证任务 +4.2 分，不可验证任务 +8.0 分。头条是耐久度。基线 self-play 两轮后开始劣化，J-Zero 连续改进十轮。而且更大的涨幅落在不可验证领域，这一点最关键：那正是算力驱动的 RL 通常进不去的地方，因为没有标准答案可对。一个跟着 solver 一起成长的裁判，就是标准答案的替代品。

归档进"有凭据的自我改进"这条线。会进化的裁判，也是所有"技能自我优化"系统暗中依赖的那块地基；如果三角色版本在 KAIST 的基准之外也站得住，它就是个模板。
