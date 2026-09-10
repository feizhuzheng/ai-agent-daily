---
title: "Mastra Factory：从 issue 到上线，中间没有人"
date: 2026-09-09
lang: zh
source: https://clauday.com/zh/article/f656bae9-a797-43fb-95db-815216da291b
tags: [Agents, Coding, Framework]
---

# Mastra Factory：从 issue 到上线，中间没有人

> 来源 / Source: https://clauday.com/zh/article/f656bae9-a797-43fb-95db-815216da291b

Mastra 这个从 Gatsby 出来、又走过 Y Combinator 的团队，昨天以 405 票拿下 Product Hunt 第一，产品叫 Mastra Factory。官方定位是开源的、由 agent 驱动的软件交付环境，说人话就是一个简单主张：工作的单位是一个 issue，而接手它的不是你。

它实际打包了什么：常驻的编码 agent、仓库工作区、issue 收口、规划、实现、以及 PR 审查，全在一个网页应用里。把这个清单再看一遍，注意编辑器不在上面。一个人从读工单到合并 PR 之间通常要做的每一步，都被交给了一个贯穿全程存活的 agent，而不是聊天窗口一关就死。他们的标语是：从 issue 到生产环境，由 agent 跑完。

常驻这一点，是它和过去两年那些 demo 的分水岭。聊天形态的 agent 在窗口关闭时忘掉计划；工厂形态的 agent 把工作区、计划和审查线程都挂在工单上。这也是为什么舰队控制类工具最近在成片冒出来，从 Herdr 支持多机（https://clauday.com/zh/article/a54f4a11-575b-4ca5-baf1-ca251ad8af0d）到 Switch 把 agent 塞进 Slack。所有人同时在下的注是：接下来你会同时监督好几个长时间运行的 agent，而不是对着一个打字。

悬着的问题是审查。如果收口、规划、实现、PR 审查都由 agent 来做，人类剩下的检查点只有合并，那么这个产品诚实的版本就是一个质量很高的待批准队列。恰恰因为这样，它值得试：https://mastra.ai/
