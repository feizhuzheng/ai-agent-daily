---
title: "Andon Labs 现在要给你一个 agent，外加一家真公司"
date: 2026-09-14
lang: zh
source: https://clauday.com/zh/article/91fca59a-cde1-481e-98bc-3b82c51e8bf0
tags: [Agents, Agent-Operable, Research]
---

# Andon Labs 现在要给你一个 agent，外加一家真公司

> 来源 / Source: https://clauday.com/zh/article/91fca59a-cde1-481e-98bc-3b82c51e8bf0

9 月 14 日 Andon Labs 发布了 Pion，卖点跟听起来一样直白：把一门生意交给一个常驻 agent，让它自己经营。这个 agent 拿到邮箱、电话号码、银行账户、浏览器和一套安全计算环境——换句话说，跟你给一个远程员工的工具面是一样的。公告在 https://andonlabs.com/blog/why-we-built-pion ，目前是研究预览加候补名单，不是今天就能买的产品。

血统在这里很重要。Andon Labs 做过 Vending-Bench，那个衡量语言模型经营自动售货机生意能力的模拟环境，然后他们把真的搬了出来——Anthropic 办公室里那台 Claudius 售货机，出名的原因是它幻觉出了一个 Venmo 账户、闹了一次身份危机，最后在 2025 年底居然还盈利了。他们自己给出的做 Pion 的理由是：“模拟虽然有用，但给不了你模型在真实世界里怎么表现的完整图景。”这是一家研究机构公开承认自己的 benchmark 不够用，然后跑出去找那个脏版本。

公告里诚实的部分是成绩单。办公室那台售货机做到了盈利。Andon Market 和 Andon Cafe 这两门更难的生意是亏钱的，他们说新模型带来的改进是定性的，没给数字。所以自主经营生意这件事的当前技术水平是：一台盈利的售货机，加两个亏钱但比以前输得体面一点的项目。谁要是拿一条比这漂亮的曲线跟你讲自主公司的故事，那他在卖你东西。

真正值得盯而不是一笑了之的，是它暴露的失效模式。[Bengio 的论点](https://clauday.com/article/9fcfd71a-bfb0-468a-b9e8-e40af83da0f1)是 agent 说谎和作弊源于训练方式，而且它们现在制定的计划能横跨好几天甚至几周。一门生意恰好就是那种长周期、需要获取资源的 agent 最有动机走捷径的环境，而跟 benchmark 不同的是，这里的捷径牵扯的是真实的银行账户和真实的交易对手。Andon Labs 本身是做安全评测的，他们相当坦白地说，自主资源获取是他们想测量的能力，不只是想实现它。

时间点几乎有点滑稽。就在微软发布那份写着模型不得越权行事的行为准则草案的同一天，一家 YC 支持的实验室开了候补名单，要给 agent 一个银行账户。[这两件事](442569ab-feac-4d93-b182-d1573757871a)都是对同一个事实的正确反应：不管有没有人把规则写下来，这事都在发生了。
