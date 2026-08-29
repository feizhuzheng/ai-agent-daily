---
title: "ponytail：故意让你的 agent 少写代码"
date: 2026-08-28
lang: zh
source: https://clauday.com/zh/article/9b96aeab-3285-4d95-b468-90299c416eea
tags: ["Tool", "Coding", "Open Source"]
---

# ponytail：故意让你的 agent 少写代码

来源 / Source: https://clauday.com/zh/article/9b96aeab-3285-4d95-b468-90299c416eea

现在 GitHub 上涨得最快的 agent 仓库，是一套教你的 agent 少干活的指令。ponytail 每天涨约 1400 星，往 Claude Code、Codex、Copilot CLI 等二十来个 harness 里注入同一个人设：最懒的资深工程师，什么都不说，只写一行。仓库在 https://github.com/DietrichGebert/ponytail。

机制是一个写码前必过的决策梯子：这东西真的需要存在吗、代码库里是不是已经有了、标准库里有没有、平台原生功能行不行、装好的依赖里有没有、一行能不能解决——连过六个"否"之后，agent 才被允许写最少量的代码。以插件、hook 和可复制规则的形式覆盖各平台。宣称的数字：比基线 agent 少写约 54% 的代码行数、便宜 20%、快 27%，验证标准不降。

好笑，但砸中的是当下 agent 经济学最疼的位置。模型按 token 收费，又被训练得力求周全，过度工程于是成了默认失败模式——每一个多余的抽象，都要你花钱生成、review、测试、维护。一个月前趋势榜上全是教 agent 多干活的技能合集，钟摆现在荡向"教它克制"，这才是更有意思的信号：最便宜的 token 是从未生成的那个，agent 今天没有撑肥的代码库，就是下个月不会爆掉的上下文窗口。
