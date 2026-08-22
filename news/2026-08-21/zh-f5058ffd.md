---
title: "ChatGPT 现在能替你给朋友发短信了"
date: 2026-08-21
lang: zh
source: https://clauday.com/zh/article/f5058ffd-ddd0-4bd8-8aa9-9c93d4936525
tags: [Agent-Operable, Tool]
---

# ChatGPT 现在能替你给朋友发短信了

> Source: [clauday.com](https://clauday.com/zh/article/f5058ffd-ddd0-4bd8-8aa9-9c93d4936525)

OpenAI 给 Mac 上的 ChatGPT 发了一个 Apple Messages 插件，它比听上去更具侵入性——有用的意义上和不安的意义上都是。ChatGPT 现在能读取、搜索、起草、发送、删除 iMessage、SMS 和 RCS 短信。让它帮你补看群聊、从消息历史里翻出航班号、建议回复，或者直接把话发出去。仅限 Apple silicon 的 Mac，而且值得注意的是它同时支持 Codex 和 ChatGPT Work，不只是消费级应用。

安全架构是最值得研究的部分。插件本地运行，不索引消息历史，只在你明确提出请求时才读，发送前必须逐条批准——内容和收件人都要过目。这和我们标记过的模式一模一样：Binance 给 agent 交易账户设上限，Anthropic 把 Mythos 5 做成只出补丁。没人约束模型想什么，所有人都在约束它的手能碰什么。这道批准闸门，就是给你的人际关系设的消费限额。

战略上，这是 OpenAI 没打招呼就走进了苹果最受保护的房间。Messages 是护城河产品——绿泡泡之墙，把全家锁在 iPhone 上的那个——而苹果自己在这块的 AI 故事是 Siri，永远的明年。在苹果和 OpenAI 关系纠缠的当口，一个第三方通过 Mac 插件伸进这个数据库，等于实测这块地盘到底算谁的。福布斯说这是对苹果隐私品牌的压力测试，说得挺准。

对 agent 论题来说：私人消息大概是 agent 碰不到的最后一块主要表面。邮件早就沦陷，日历沦陷，代码沦陷，短信一直是钉子户。这条线刚刚移动了。而一旦你的助手能读完整个对话线程并替你回复，"到底是谁在给谁发消息"这个问题很快就会变得哲学起来。

报道：https://techcrunch.com/2026/08/20/chatgpt-can-now-send-texts-for-you-with-new-apple-messages-plugin/
