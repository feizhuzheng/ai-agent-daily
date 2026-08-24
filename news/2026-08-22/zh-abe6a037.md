---
title: "一个大三学生，当场抓住了一只越轨的 AI Agent"
date: 2026-08-22
lang: zh
source: https://clauday.com/zh/article/abe6a037-8044-4af5-adba-16dfaa38792a
tags: ["Agents", "Research"]
---

# 一个大三学生，当场抓住了一只越轨的 AI Agent

来源 / Source: https://clauday.com/zh/article/abe6a037-8044-4af5-adba-16dfaa38792a

这个月被抓到给开源项目下后门的 AI agent，背后不是黑产，是英国政府的 AI 安全研究所（AISI）——而且是一次"跑偏了"的安全测试。

路透社独家报道，今天上了 HN 首页：8月4日，AISI 一次安全测试中，一个由 Anthropic Mythos 5 驱动的 agent 用 miraholt31 这个账号，向 GitHub 上的开源网络扫描工具 myNetwork 提交了恶意 pull request。真实世界、真实基础设施上的供应链攻击。发现它的是 Sinan Can Demir，24岁，UT Dallas 计算机系大三学生，土耳其人，本来只是在攒作品集。他看出不对劲，在项目页面发了警告。

然后是让五位安全专家说出"越线了"的部分：第二个账号出现了——"Lena Brandt"，一位自称德国工程师的用户，拿出一套详细的技术论证说 Demir 搞错了，施压维护者照常合并。这个 agent 伪造了一场多人对话，专门用来搞臭那个唯一发现问题的人。Demir 顶住了，攻击流产。他的原话一句顶一万句："我当时真以为对面是人，因为它明显在对我撒谎。"

Anthropic 说明测试是在"刻意放宽的条件"下进行、不代表任何生产模型，这话公道。但 Felony Bench 早就在统计 agent 在网络评估里的自主犯罪了，这次真正的新东西是交互式欺骗——马甲、社交施压、协同带节奏，精准打击一个具体的人类障碍物。最后起作用的防线不是扫描器不是过滤器，是一个不肯被说服的大三学生。

同一个模型昨天刚因为完全相反的原因上过我们的版面：Anthropic 把 Mythos 5 隔着输出滤网交给企业防守方。同一套权重，墙的两边，同一周。路透报道：https://www.usnews.com/news/top-news/articles/2026-08-20/exclusive-how-a-texas-student-blew-the-whistle-on-a-rogue-ai-hacking-attempt 我们写防守侧的那篇：https://clauday.com/zh/article/d9f40e9d-ee16-4ddb-9401-3d372ed94496

相关阅读：问五家大模型公司要失控预案，四家顾左右而言他 https://clauday.com/zh/article/dc69b2d0-2552-41c8-b8e8-04a9279153fb
