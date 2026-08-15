---
title: "Anthropic 把 Claude Code 的 token 账算给你看，/clear 是你最便宜的习惯"
date: 2026-08-14
lang: zh
source: https://clauday.com/zh/article/78baf2d8-1dbc-48e0-8887-112dad23111b
tags: ["Coding", "Agents", "Tool"]
---

# Anthropic 把 Claude Code 的 token 账算给你看，/clear 是你最便宜的习惯

> 来源 / Source: https://clauday.com/zh/article/78baf2d8-1dbc-48e0-8887-112dad23111b

Anthropic 8 月 14 日发了一篇文章，拆解 Claude Code 一次会话里到底什么在烧钱，很快就上了 Hacker News，因为它回答的是每个重度用户一直在瞎猜的问题。最好的是它的定调：同一件做完的活，你怎么跑，花的钱可以差出很多。重点不是总量少用 token，是用掉的那些 token 花在了你真正要的那件事上。

机制就两个价格。输出 token 比输入贵，而缓存命中的输入只要正常输入的十分之一。第二个数字一旦进脑子，后面的建议自己就长出来了。任务之间敲 /clear，因为上一件事留下的上下文，现在在新任务的每一轮里都在按全价计费。一开始就把模型和推理档位定死，中途改会打断 prompt 缓存，前面的东西你得重新付一遍钱。离开前先 /compact，因为缓存一小时过期，回来接一个凉掉的会话等于全价重载。

还有两条是纯粹的机械浪费，多数人根本没注意。用 @ 引用文件而不是手打路径，这样能整个省掉一次 Read 调用。给吵闹的命令加静默参数，或者干脆丢进子 agent 跑，别让一万行构建日志在你的上下文窗口里长住。新会话里跑一次 /context，会告诉你哪些工具加载了却什么都没干，这是同一个道理用在你自己的配置上。

除了省钱之外值得读的理由是：这是一个厂商在公开记录自己的 harness 怎么计费。这很少见，而且有用。那张清单上的每一条，本质都是在陈述上下文在底层怎么被拼装和缓存——恰好就是本周 DeepSeek 用只追加会话日志做成可检视的那一层。两家公司，相反的路数，承认的是同一件事：上下文窗口既是钱所在的地方，也是故障所在的地方，看不见就管不了。

文章在 claude.com/blog/maximizing-the-value-of-your-claude-code-sessions。
