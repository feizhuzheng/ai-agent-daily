---
title: "Superagent 给 Claude Code 配了台真电脑"
date: 2026-08-30
lang: zh
source: https://clauday.com/zh/article/40faf35d-e494-4b82-9d30-477d917fb00f
tags: [Coding, Agent-Operable, Open Source]
---

# Superagent 给 Claude Code 配了台真电脑

> 来源 / Source: https://clauday.com/zh/article/40faf35d-e494-4b82-9d30-477d917fb00f

宣传语是'给普通人用的 Claude Code',但真正的点子比这句话锋利。Claude Code 写完代码，甩给你一屏滚动的终端文字，关掉窗口就把一切忘光，还得你自己 alt-tab 过去看它给你搭的页面到底变没变。Superagent 的答案是：别再让 agent 住在终端里，给它一台电脑——一个它能在你自己已登录会话里操作的真浏览器、一个它能点能滑的 iOS 模拟器、你的文件、一块它自己维护的记事板、以及按定时器跑的例行任务。

值得注意的设计选择，是他们没做的东西。没有 Superagent 的服务器，没有额外订阅。它在本地跑 Claude Code，用你本来就在付费的那个计划，你的工作全留在自己硬盘上。Mac 应用、iPhone 应用、还有那个把你手机拉进回路的中继，全部 MIT 开源、挂在 GitHub 上。在这个每个 agent 产品都想变成你要租的那朵云的季节里，把整套东西做成一个本地的、可读的、MIT 授权的应用，是一个真实的立场，不是脚注。

这跟我们追了好几周的 harness 讨论是同一条线：agent 等于模型加 harness，而你真正的杠杆恰恰长在 harness 上。Superagent 是一个你看得见的 harness——它怎么碰你的浏览器、什么东西离开你的机器、手机消息怎么加密，全摊开让你读。Codex 和 Antigravity 的支持写着即将到来。如果你一直憋屈于机器上最聪明的编码模型被困在一堵文字墙后面，这是目前有人做出来的最直接的解法。在 Product Hunt 和 GitHub 上搜 superagent 就能找到。
