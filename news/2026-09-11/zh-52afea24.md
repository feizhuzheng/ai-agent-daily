---
title: "AI 写的代码正好脏两倍，现在有数字了"
date: 2026-09-11
lang: zh
source: https://clauday.com/zh/article/52afea24-2b4f-4250-a2b9-f3cf9e4f5fba
tags: [Benchmark, Coding, Research]
---

# AI 写的代码正好脏两倍，现在有数字了

> 来源 / Source: https://clauday.com/zh/article/52afea24-2b4f-4250-a2b9-f3cf9e4f5fba

所有人都有那种感觉：agent 写的代码烂得更快。Earendil 的 Sebastian 把它量化了，差距干净得有点滑稽：人类仓库的冗余度 0.15、侵蚀度 0.31，AI 生成的代码是 0.33 和 0.68。两个维度都正好两倍，误差棒还窄到有意义。原文在 https://earendil.com/posts/measuring-code-sloppiness/ ，9 月 10 日发的，Hacker News 上 221 分。

三个指标故意做得很无聊，而这正是它能用的原因。代码行数，直白。冗余度，用 AST-Grep 加克隆检测抓重复和不必要的长行。侵蚀度，把圈复杂度和源码行数结合起来，检测复杂度往少数几个大函数里堆积。全程不需要裁判模型，不需要品味，全部能在 CI 里跑。这比具体阈值重要得多，因为这个领域已经用「感觉」和截图吵了一年代码质量。

评测设计是另一个有用的部分。它没用单次生成测试，而是借了 SlopCodeBench 的做法：多轮指令和测试，检查点之间清空上下文，模拟你三周后开一个全新会话回到这个代码库时真实发生的事。在这套机制下，最前沿的模型严格通过率是 0%。零。代码能编译，单个测试也能过，架构照样崩。

诊断是 agent 没法在规模上管理质量，机制是不必要的抽象。一个看不到整个系统的 agent，只能在局部给自己加一层来自保，四十次局部自保就变成一个没人能在脑子里装下的代码库。那个「为了把按钮改成蓝色生成 23 个 agent」的段子拿 906 分时说的是同一件事，只不过这个版本带标准差。如果你需要一个数字带进下一次「要不要让 agent 写整个服务」的争论，就是 0.68 对 0.31。

相关阅读：https://clauday.com/article/c0f8395c-2ccc-4731-9b07-906a022260fe 和 https://clauday.com/article/219e4893-910e-4bd4-8d64-b477c1ab5102
