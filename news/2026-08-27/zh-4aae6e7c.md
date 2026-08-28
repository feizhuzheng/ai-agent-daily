---
title: "archify：不通过校验就不出图的画图技能"
date: 2026-08-27
lang: zh
source: https://clauday.com/zh/article/4aae6e7c-8b6c-48d3-883c-20ad9e856667
tags: ["Skills", "Tool", "Open Source"]
---

# archify：不通过校验就不出图的画图技能

来源 / Source: https://clauday.com/zh/article/4aae6e7c-8b6c-48d3-883c-20ad9e856667

archify 今天在 GitHub 涨了 4260 星，是 trending 榜上 agent 相关项目里最大的单日跳升。它只干一件窄事：把一个代码库或系统描述,直接在聊天里变成一张精致的、可交互的系统地图。它是一个 agent skill，装进 Claude Code、Cursor 或 Codex CLI 用，覆盖五种图——架构、工作流、时序、数据流、生命周期——支持换主题、动画，能导出 PNG、SVG、WebM。MIT 协议，累计 22.9k 星。

解释这个星数的设计细节，是可验证这个词。agent 不是在画画，它生成带类型的 JSON，校验器检查，只有通过验证的输出才被渲染成自包含的 HTML 产物。模型幻觉出一个不存在的组件、一条解析不通的边，校验器会在你看到图之前拦住它。这正是过去几个月最好的那批 skill 共有的模式——在模型和交付物之间放一个确定性的检查器——也是玩具和能拿进设计评审的工具之间的分界线。

它还能做对比，diff 两版架构、看一次改动到底动了什么，渲染出的地图里还能搜索、追踪调用路径。这悄悄把它从给我画张好看的图，重新定位成了 agent 写的系统的检查层。当越来越多代码库变成你吃午饭时被 agent 改过的东西，快速看清现在的结构长什么样就不再是装饰需求。

画图技能正在长成一个自己的门类，看着好几个先后上榜，教训很一致：活下来的都是输出可检查的那些。archify 是这个思路到目前为止最完整的版本。仓库在 github.com/tt-a1i/archify。
