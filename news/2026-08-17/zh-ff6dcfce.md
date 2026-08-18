---
title: "AI写出漏洞，AI审核放行，AI挖出来利用"
date: 2026-08-17
lang: zh
source: https://clauday.com/zh/article/ff6dcfce-7ca3-439d-89d9-64b5fa02ccc1
tags: [Agents, Coding]
---

# AI写出漏洞，AI审核放行，AI挖出来利用

> Source: [clauday.com](https://clauday.com/zh/article/ff6dcfce-7ca3-439d-89d9-64b5fa02ccc1)

Wiz刚发布的这份报告，是"AI同时站在攻防两侧"迄今最完整的一个案例。6月18日，一个由GitHub Copilot Autofix共同署名的PR合进了Snowflake的公开仓库，把原本安全的写法（环境变量加jq解析）改成了把GitHub issue标题直接字符串拼接进shell脚本。GitHub的AI辅助安全审查看了一眼，批了。五天后，Wiz的自主安全智能体Red Agent发现了这个洞，第一次利用失败后自己调整了攻击方式，最后拿走了一个以qa@snowflake.net身份认证的Jira API token。

这个token能打开Snowflake内部的工程、安全合规和漏洞赏金追踪项目。理论上互联网上任何人都能干同样的事，因为这个workflow对任意公开issue触发，标题里一个单引号就足以逃逸成命令注入。Wiz在6月23日披露，Snowflake当天修复并轮换了凭证，审计日志显示五天窗口期内没有外部攻击者抢先。完整报告8月17日公开：wiz.io/blog/red-agent-snowflake-copilot-cicd-bug

最值得琢磨的地方在于：这不是模型幻觉编了个不存在的API。Copilot Autofix是把本来能用、本来安全的代码，重写成了教科书级的注入漏洞，然后AI审查员放行了。Wiz的结论很直接：AI生成的PR必须过和人类代码同样的静态分析和安全审查，而且要专门防着AI把结构化解析器改成字符串拼接，因为这次出事的就是这个模式。

这个故事里唯一发挥出专家水平的，恰恰是进攻方的agent。它自己找到漏洞，被挡住后自己变招，自己完成窃取。眼下攻击能力跑在了生成能力和审查能力前面，而且跑在你的CI/CD里，那是代码带着凭证运行的地方。
