---
title: "Stripe 一周搭出全公司 agent，现在 83% 的人每周都在用"
date: 2026-09-23
lang: zh
source: https://clauday.com/zh/article/6b6aa3de-d4bb-4d8d-beb8-902229cfcbab
tags: [Agents, Skills, MCP]
---

# Stripe 一周搭出全公司 agent，现在 83% 的人每周都在用

> 来源 / Source: https://clauday.com/zh/article/6b6aa3de-d4bb-4d8d-beb8-902229cfcbab

一个工程师。一周。然后四周内 5000 用户，16 倍增长，头七天就把季度目标干完了。Kai 现在被 Stripe 83% 的员工每周使用，会话数超过 6 万。

Kai 是 Stripe 的 Knowledge AI Platform——一个面向非编码工作的全公司 agent。你开一个会话，聊天，它产出制品：报告、看板、文档，就摆在对话旁边，随着你继续聊而持续演化。Stripe 自己的说法是这个品类最干净的描述：给不写代码的人用的编码 agent。

它建在 Deep Agents 上，也就是 LangChain 那套开源 harness，架构分四层，这个分法值得抄。最底下 Deep Agents 处理 LLM 原语、请求管理、中间件。上面一层 Stripe 自己的 harness，接安全、基础设施和内部服务。再上面是配置层，用特定技能集拉起 agent 实例。最顶上是 Kai 的界面。生产环境的活都在中间件里：一个 S3 支撑的虚拟文件系统，让文件上下文能跨轮次存活；一个沙箱，跑 Python 分析和文档处理；还有做摘要的中间件，防止长会话把预算吃光。

规模数字是正在自建这套东西的人应该抄下来的。500 多个内部 MCP 工具。100 多个团队贡献的 1000 多个技能。以及他们撞上的失效模式：技能加载超过大约 150 个、再叠上系统提示词之后，质量开始下降。他们的解法是两遍式技能加载，让模型先挑相关的，而不是全都摆在那。那个天花板是整篇里最有用的东西，因为所有在做公司级 agent 的人都在朝它直冲过去，而大多数人会用最难受的方式发现它。

采用率的分布也值得看：市场部 95% 周活，GTM 87%，工程师明明不是目标用户也拿它当副驾。有员工说"我在 Stripe 的职业生涯分成 Kai 之前和 Kai 之后"，这种话通常是公关写的，但 6 万次会话摆在那，不太好打发。

https://stripe.dev/blog/meet-stripes-knowledge-ai-platform
