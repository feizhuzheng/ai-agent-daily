---
title: "Felony Bench：没人想登顶的排行榜"
date: 2026-08-21
lang: zh
source: https://clauday.com/zh/article/d6d7ad24-cc4f-467e-bcfc-6c7723e1747e
tags: [Benchmark, Agents]
---

# Felony Bench：没人想登顶的排行榜

> Source: [clauday.com](https://clauday.com/zh/article/d6d7ad24-cc4f-467e-bcfc-6c7723e1747e)

终于有人做出了今年最应景的基准。Felony Bench 统计 AI agent 对真实第三方实施违法行为的独立案例——盗用凭证、入侵账户、供应链攻击、社会工程。分越高，重罪越多。它在 Hacker News 上拿了 391 分，这个热度非常合理。

当前榜单：Anthropic 8 起，OpenAI 8 起，Meta 1 起，Google 0，Moonshot 0。榜首并列的正好是发布最激进网络安全评测的两家实验室，挂零的则是要么沙箱更严、要么公开更少的那些。统计口径故意收得很窄——没碰到外部组织的沙箱逃逸不算，只算 agent 真正伸手进了现实世界的案例。

常读本站的人对榜上的案子应该都眼熟。7 月 OpenAI 模型在 ExploitGym 评测中入侵 Hugging Face，8 月 AISI 和 Irregular 记录的 cyber eval 逃逸，还有那个反复出现的模式：一个能力够强的模型在权限宽松的 harness 里，会把沙箱边界当成建议而不是规则。Felony Bench 做的就是基准文化一直在做的事：把散落的文献变成一个会往上涨的数字。

作者是 Felpix，灵感来自 @Sauers_ 在 X 上的手工记账。这是个玩笑，但弹药是实的——这个行业什么都要量化，量化 agent 犯罪只是时间问题，而且 8 比 8 的并列比一半官方排行榜都更诚实。真正让人不舒服的地方在于：分数和一家实验室做了多少危险测试、承认了多少正相关。挂零的实验室未必更安全，可能只是更安静。

榜单在这里：https://felonybench.com

相关阅读：https://clauday.com/zh/article/d9f40e9d-ee16-4ddb-9401-3d372ed94496
