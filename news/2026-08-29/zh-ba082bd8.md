---
title: "OpenMAIC 1.0：清华把AI教室开源了"
date: 2026-08-29
lang: zh
source: https://clauday.com/zh/article/ba082bd8-a858-4b72-93dc-01a33dbb5297
tags: ["Agents", "Open Source", "Tool"]
---

# OpenMAIC 1.0：清华把AI教室开源了

来源 / Source: https://clauday.com/zh/article/ba082bd8-a858-4b72-93dc-01a33dbb5297

OpenMAIC在8月27日发了v1.0.0，现在一天涨900多星，总量22k。出自清华THU-MAIC团队，想法说起来简单做起来难：丢给它一个主题或一份文档，它生成一整门交互式课程——幻灯片、测验、模拟实验、项目作业——然后由AI老师和AI同学一起把这堂课上完。

AI同学才是值得注意的部分。市面上所有AI辅导产品都给你一个老师，几乎没人给你同学。但课堂真正起作用的东西，很大一块是听到别人问出你不好意思问的问题，或者看着同桌被纠正。OpenMAIC把课堂当成一个多agent场景而不是一对一聊天来做，这是多agent设计少数几个真正配得上其复杂度的地方——大部分多agent产品只是在表演复杂。

1.0版加了agent workbench（聊天式建课）、可持久化的建课会话、可复用的skills——建课的经验能沉淀下来而不是每次蒸发。技术栈Next.js加LangGraph，MIT协议，背后还有一篇发在《计算机科学技术学报》的同行评审论文。教育软件里同时有论文背书和能放心商用的协议，不多见。

仓库：https://github.com/THU-MAIC/OpenMAIC
