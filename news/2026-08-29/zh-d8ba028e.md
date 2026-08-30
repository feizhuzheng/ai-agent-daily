---
title: "OpenMontage：700个skill文件，把agent变成一家视频工作室"
date: 2026-08-29
lang: zh
source: https://clauday.com/zh/article/d8ba028e-3657-46ab-848e-b85ec03855d7
tags: ["Agents", "Skills", "Open Source"]
---

# OpenMontage：700个skill文件，把agent变成一家视频工作室

来源 / Source: https://clauday.com/zh/article/d8ba028e-3657-46ab-848e-b85ec03855d7

OpenMontage赖在GitHub trending上不走了——今天又涨800多星，总量54k——那就聊聊它。它自称第一个开源的agentic视频生产系统：你的coding agent指挥整条流水线，从调研到提案到脚本到分镜到素材到剪辑到最终渲染。12种以上生产管线、100多个注册工具、60多家供应商集成覆盖视频、图片、TTS和音乐，还有一个叫Backlot的实时制片看板。AGPLv3协议，Python加Remotion加FFmpeg。

有意思的是设计模式。OpenMontage没有训练或微调任何东西，而是写了大约700个agent skill文件，分三层组织：有什么工具、这套系统希望你怎么用、需要时再下钻的深度技术文档。每个流水线阶段配一个director skill，带着agent走完执行、自查、审批三步。说白了就是把一家工作室的组织架构和标准作业流程写成markdown，让模型住进去。

这正是今年反复胜出的那个模式，从科研skills到工程skills都一样：别造专用模型，给通用模型造专用harness。还有一点值得说：它支持纯免费本地工具加开放素材库，不付一分钱生成API也能做实拍纪录片。成品能不能比过人类剪辑师你自己判断，但就算你永远不渲染一条视频，这个架构也值得研究。

仓库：https://github.com/calesthio/OpenMontage
