---
title: "现在，exploit 比补丁先到"
date: 2026-08-28
lang: zh
source: https://clauday.com/zh/article/52c22aba-55d2-4cf9-adac-3519170b29d9
tags: ["Research", "Agents"]
---

# 现在，exploit 比补丁先到

来源 / Source: https://clauday.com/zh/article/52c22aba-55d2-4cf9-adac-3519170b29d9

Anil Madhavapeddy——剑桥教授、OCaml 维护者，不是会制造安全恐慌的人——修了 cohttp 6.3.0 里的一个路径穿越漏洞，全程按规矩办事。然后他看了眼服务器日志：精确匹配这个漏洞模式的探测请求，在他开出修复 PR 几分钟后就来了。不是安全公告发布之后，是 pull request 之后。文章在 https://anil.recoil.org/notes/rumour-is-the-exploit，今天在 Hacker News 上 197 分。

为了验证猜想，他拿自己做了实验：只给自己的 AI agent 一句"大概是什么方向的漏洞"的传闻，agent 就找到了可用的 exploit——在公开补丁可用之前。他引的数字让这事从轶事变成系统性现实：Fang 等人的研究发现，只给 CVE 描述，GPT-4 agent 能利用 87% 的测试漏洞；漏洞平均利用时间现在是负七天。负的。利用先于补丁发生。

难受的结论是：协同披露——整个安全修复的社会契约——是为以人类速度阅读的攻击者设计的。修复 PR 就是传闻，传闻就是 spec，spec 对 agent 来说就够了。这篇文章上首页的同一天，GLM-5.3 放出了可下载的权重，而它最拿手的恰恰就是这类漏洞发现。防守方拿着同样的工具，但防守方要修每一台服务器，攻击方只需要那个 diff。

相关阅读：GLM-5.3 权重来了，MIT 没来 — https://clauday.com/zh/article/16cd4159-d4da-4a85-a965-690a49c9f3b8
