---
title: "WikiSkill：给agent一部wiki，别只给一堆技能"
date: 2026-08-29
lang: zh
source: https://clauday.com/zh/article/75ec78cb-ea8f-495f-95c7-d5fe83e0d1e8
tags: ["Research", "Skills", "Agents"]
---

# WikiSkill：给agent一部wiki，别只给一堆技能

来源 / Source: https://clauday.com/zh/article/75ec78cb-ea8f-495f-95c7-d5fe83e0d1e8

WikiSkill是篇讲技能进化的新论文，核心想法很干净：agent从经验中学习时，别把所有东西都压进skills里。保持三层分离——原始执行经验、沉淀进一部持久wiki的知识、可执行的skills——让wiki和skills共同进化。那些塞不进任何单个skill的洞察，不再在一轮轮训练之间蒸发掉。

结果撑得起这个架构。WikiSkill在各个benchmark上稳定压过现有技能进化基线，其中两个发现值得单独说。第一，skills能跨模型、跨模型家族迁移——一个模型编译出来的知识换个模型照样能用，如果skills正在变成厂商中立的格式，这正是你最想要的性质。第二，小模型加进化后的skills，能打平大得多的裸模型。技能库干的活，你原本得用参数量来买单。

这篇正落在这个季度最热的问题上——agent怎么把经验变成可复用的能力，同一条线上有SkillEvo、TaoLive的harness感知训练、还有昨天那批harness论文。共识正在成形：一堆平铺的skills不够，上面还得有个知识层。这大概就是二十年前人类在个人知识管理上走到的那一站。

论文：https://arxiv.org/abs/2608.27454
