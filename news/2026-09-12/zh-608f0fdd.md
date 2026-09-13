---
title: "worktrunk 悄悄变成了平台，因为现在人人同时跑五个 agent"
date: 2026-09-12
lang: zh
source: https://clauday.com/zh/article/608f0fdd-7bdc-4c97-a227-2a98c6f55731
tags: [Tool, Coding, Agents]
---

# worktrunk 悄悄变成了平台，因为现在人人同时跑五个 agent

> 来源 / Source: https://clauday.com/zh/article/608f0fdd-7bdc-4c97-a227-2a98c6f55731

max-sixty/worktrunk 是个管理 git worktree 的命令行工具，专门为并行跑 AI agent 的工作流设计。7,198 个 star，又一次上了 GitHub 趋势榜，一天涨 137 星，9 月 8 日发了 v0.77.0，最近的提交就在昨天。仓库在 https://github.com/max-sixty/worktrunk 。这是个健康的工具。但真正有意思的是它周围长出来的东西。

在 GitHub 上搜 worktrunk，能搜出十几个第三方项目：herdr-worktrunk 有 144 星，把它接进了一个 agent 舰队管理器；pi-worktrunk 会重绘分支标记来显示 agent 状态；worktrunk-sync 按依赖顺序 rebase 堆叠的 worktree 分支；还有 opencode-worktrunk、worktrunk-codex、两个显然互相不知道对方存在的人各写了一个的 Neovim 插件、两个 zsh 插件、一个 Node 封装。没有人会给一个 git 便利脚本建生态，只会给一个卡在日常工作流正中间的东西建生态。

原因特别平淡，而平淡才说明是真的。在同一个仓库上同时跑好几个编码 agent，如果它们共用一棵工作树就完全没法干活，因为会互相踩掉对方没提交的改动。这个问题 git 2015 年就用 worktree 解决了，只是那套命令别扭到没人愿意随手用。worktrunk 把「开一棵树、跑个 agent、用完扔掉」压成一条又快又短的命令，而这件事一旦变快，同时跑四个 agent 就从炫技变成了默认姿势。

把插件列表摊开看，正在成形的那一层栈的形状就摆在那了：上面是舰队编排，下面是 worktree 作为隔离原语，中间是编辑器和 shell 集成在粘合。那几个状态标记插件尤其能说明问题，它们存在的唯一目的是回答「我这五个分支里，哪个上面有 agent 正在干活」——十八个月前这根本不是一个日常问题。

它和[Herdr 走向多机](https://clauday.com/zh/article/a54f4a11-575b-4ca5-baf1-ca251ad8af0d)正好是一对。Herdr 对舰队问题的答案是加机器，worktrunk 的答案是在你手上这台机器里加隔离，而已经有人写了连接两者的桥接，说明大家两样都在干。如果你现在还在主工作目录里一次跑一个 agent，这是最便宜的一次升级：一个命令行工具，不改变你任何工作习惯，只是把原本最贵的那一步变成免费的。
