---
title: "Will Larson 把 agent 指向了一个项目，不是一个任务"
date: 2026-09-20
lang: zh
source: https://clauday.com/zh/article/fbe4b863-aa68-4f13-8c8b-d4283c220ff6
tags: [Agents, Coding, Tool]
---

# Will Larson 把 agent 指向了一个项目，不是一个任务

> 来源 / Source: https://clauday.com/zh/article/fbe4b863-aa68-4f13-8c8b-d4283c220ff6

Will Larson 写了他叫做软件工厂模式的东西，一句话定义是：对着一个宽泛的目标做循环，然后靠 harness 推动进展朝那个目标走。不是一个任务，不是一张卡，是一个项目。文章 9 月 20 日发布，地址 https://lethain.com/software-factory-experiment/ 。

实现是一个他叫做 /linear-project-loop 的 skill。它从真正写下目标的那些 RFC 里读出项目目标，去 Datadog 和 Snowflake 的看板上核对那些本该变动的指标，在 Linear 里更新任务状态，捡起所有没被阻塞的事往前推——提 PR、做 review、问澄清问题；当项目描述相对现实已经过期，它会重新评估方向，而不是对着过时的卡片死磕。

他很坦白，这里没有数字。他的判断是效果好到足以让他打算把它挪进自己那套编排 harness，这种话你该当信号读，不能当证据读。不过他给出的那几条发现，本来也比基准分好用：把这东西建出来的过程，会逼你看见流程里每一处把状态存在某个人脑子里的地方；建成之后你拿到的是发布之后的项目监控，而不再是只有发布之前。

他自己写的那句提醒才是关键：这些部件只在你拥有其他部件的程度上产生复利。这个循环要求工作跟踪在一个可查询的系统里，目标写在机器读得到的地方，指标接在有真实 API 的看板上。一个目标躺在 PPT 里、状态活在站会上的团队，从这套东西里什么也拿不到。

这也重新定义了过去三年那些工程卫生工作的意义。写 RFC、给看板埋点，以前是文档纪律。现在它是你有没有一个能上手干你项目的 agent 的分界线。
