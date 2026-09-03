---
title: "Atlas：给 agent 集群做的 Git"
date: 2026-09-02
lang: zh
source: https://clauday.com/zh/article/e7dbea75-395c-4ae1-97d2-86b06682df8f
tags: [Tool, Open Source, Coding]
---

# Atlas：给 agent 集群做的 Git

> 来源 / Source: https://clauday.com/zh/article/e7dbea75-395c-4ae1-97d2-86b06682df8f

Atlas 是今天 GitHub Trending 上的爆款：2800 星的底子，一天 +895，这种比例只在产品发布的时刻出现。定位是"给编码 agent 的源代码管理"——Claude Code、Codex、ACP 注册表里的任何 agent 同时跑在一个代码库上，Atlas 集中记录谁干了什么。

机制是精华所在。每次 agent 运行都会创建检查点，把 commit 反向链接到产生它的那个会话——prompt、工具调用、推理过程全在。半年之后 git blame 不会终结在"某个 agent 干的"，你能拿到完整的溯源链。还有一个共享的本地语义索引，任务中途换 agent 不用从零重建上下文。Rust 加 Tauri，MIT 协议，默认本地——不用注册账号，不联网也能用。

这个问题真实存在而且在变严重。一个开发者并行跑三个 agent 现在是常态，而裸的 git 把真正重要的上下文全丢了——哪个会话、哪条 prompt、哪个模型。commit 元数据是为记得自己为什么这么做的人类设计的。agent 不记得，所以 harness 得替它记。把会话当一等对象的版本控制层，是 agent 技术栈里一块明显缺失、但直到现在才有人补上的拼图。

仓库：https://github.com/pacifio/atlas
