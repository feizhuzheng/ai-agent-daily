---
title: 有人正冒充 ClaudeBot 扫全网，找的是 AI 工具的密钥
date: 2026-08-12
lang: zh
source: https://clauday.com/zh/article/2da1cab7-0416-4b25-aaab-5fc871eab696
tags: Agents, Infrastructure, Monitoring
---

# 有人正冒充 ClaudeBot 扫全网，找的是 AI 工具的密钥

> 来源 / source: [clauday.com](https://clauday.com/zh/article/2da1cab7-0416-4b25-aaab-5fc871eab696) · 2026-08-12

Known Agents 这周放出的流量数据显示，声称自己是已知 AI 爬虫（ClaudeBot 在内）、但过不了该爬虫真实认证的请求出现了统计意义上显著的激增。样本是一批完全不相关的随机网站，这意味着真实规模远大于看得见的部分。这些请求打的是和 AI 编程工具相关的路径。有人正在互联网尺度上搜刮暴露在外的 agent 配置和凭证，披着一家 AI 公司的名字。

原理很无聊，无聊恰恰是重点。User agent 是一句声明，不是身份。任何东西都能发一个写着 ClaudeBot 的头。真爬虫和冒牌货的区别在于源 IP 验证或 Web Bot Auth，而大多数站点运营者两样都不查——看一眼 user agent，认出一家友好的 AI 公司，就放行了。有些人还更进一步，专门把 AI 爬虫加进白名单以求被收录。这份白名单现在成了攻击面。

Hacker News 那条帖子里有一个有用的纠正：这些日志里的很多路径完全早于生成式 AI。大规模扫描暴露的 dotfile 和配置文件是几十年的老活。变的是找到之后的价值。以前一个 .env 泄的是数据库密码。今天它可能泄的是一把绑在某个有 shell 权限、有仓库、有预算的 agent 上的 API key。伪装也变了，因为 AI 爬虫流量恰好是站点运营者最近才学会挥手放行的那一类。

补救办法不好看但今天就能做。别再信 user agent。任何进白名单的爬虫都用 IP 段或 Web Bot Auth 验一遍，对 agent 凭证路径要像对生产数据库一样偏执。更值得坐下来想一会儿的是这个模式本身：agent 生态过去两年攒下来的信任，它自己现在也成了值得偷的东西。

数据在 https://knownagents.com/insights
