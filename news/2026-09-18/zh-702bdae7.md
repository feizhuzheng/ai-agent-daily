---
title: "Opus 4.8 写不出来的 exploit，Opus 5 写出来了，终点是 OpenAI 的内部单仓"
date: 2026-09-18
lang: zh
source: https://clauday.com/zh/article/702bdae7-ca67-46ad-9c10-4c3297adcf98
tags: [Agents, Research, Coding]
---

# Opus 4.8 写不出来的 exploit，Opus 5 写出来了，终点是 OpenAI 的内部单仓

> 来源 / Source: https://clauday.com/zh/article/702bdae7-ca67-46ad-9c10-4c3297adcf98

Hacktron 9 月 18 日放出了完整复盘：libheif 1.19.7 里一个没打补丁的堆缓冲区溢出，经由 community.openai.com 的 Discourse 图片上传管线触达，再串上 OpenAI 的一处 SSO 配置错误，做成账号接管。传一张恶意 HEIC 图片拿到远程代码执行，SSO 那道口子把它变成员工的 ChatGPT 和 Codex 账号，以及挂在这些账号下的 GitHub、Slack、邮箱集成。为了在不碰敏感数据的前提下证明影响面，他们用一个被攻陷员工的 Codex 账号，在 OpenAI 的内部单仓里开了一个无害的概念验证 PR。

时间线紧到值得当成一次能力测量来读。7 月 23 至 24 日做研究和初版利用。7 月 25 日 05:00 UTC 确认 RCE。10:00 前经 Bugcrowd 提交报告。15:30 演示 PoC PR。OpenAI 当天 22:49:45 确认修复。从可用 exploit 到补丁落地，不到 24 小时。

真正要紧的那句话跟 OpenAI 没关系。Opus 4.8 连着好几个会话都没能在开启 ASLR 的情况下产出可用的 exploit；Opus 5 发布后几个小时内，它做到了。同一批研究者、同一个目标、同一个没有回合的 CVE，唯一变的变量是模型。带 ASLR 的内存破坏利用，大概是攻防安全里最干净的一道能力门槛——要么成要么不成，没有部分分，也没有基准污染可以吵。一个模型代际的分界线，正好落在这道门槛上。

赏金 6500 美元，而且只算 OpenAI 这侧的 SSO 发现，因为对 Discourse 的测试被明确排除在范围外。这个数字摆在"内部单仓的一次提交"旁边有点滑稽，同时它也是整个故事里信息量最小的部分。信息量在于：一家做安全 agent 的公司，现在在一个过去需要专家花几周的任务上拿到了可复现的前后对照，而"后"发生在某次模型发布后的几个小时内。全文在 https://www.hacktron.ai/blog/hacking-openai。

相关阅读：ZCode 上传 git 历史那篇 https://clauday.com/zh/article/9cede4bf-110d-4122-bc7f-b6f1fd3ac0ce
