---
title: "1500 次提交换来 232 倍加速，loop engineering 到底长什么样"
date: 2026-08-15
lang: zh
source: https://clauday.com/zh/article/fd213d2b-7b3a-4a83-bbc9-820cfb5f556e
tags: ["Agents", "Coding", "Research"]
---

# 1500 次提交换来 232 倍加速，loop engineering 到底长什么样

来源 / Source: https://clauday.com/zh/article/fd213d2b-7b3a-4a83-bbc9-820cfb5f556e

Sankalp Shubham 打了 GPU Mode 的 qr_v2 赛题——批量方阵 compact-Householder QR 分解，B200 上的 FP32 CUDA——最后拿到相对 baseline 232 倍的加速。几何平均从 419000 微秒压到 1805 微秒，183 人里排第 12。整个过程 14 天、1500 多次提交，而这些代码基本不是他写的。文章在 https://sankalp.bearblog.dev/autoresearch/ ，今天在 Hacker News 上 357 分、83 条评论。

真正能抄走的是他的搭法。执行层是 Codex 里的 GPT-5.5，靠一个 /goal 命令跑自主循环。Claude 在旁边只当顾问，聊思路不写代码。一个 AGENTS.md 把提交纪律写死，免得循环把提交额度烧在垃圾上。结构化日志记录每一次尝试、它的 profile、它的状态。剖析工具是 Modal、torch profiler、nsys 和 NCU。最关键的一点：他跑的是 beam——同时养着三到五条候选思路，而不是一条血脉反复迭代。因为单条优化路线走着走着就撞进局部最优，然后就卡死在那儿。中途他用 /btw 开侧线程看进度，不打断主循环。

那些瓶颈就算你这辈子不碰 CUDA 也值得知道。Householder 反射天然串行依赖，解法是分块 WY 算法，把串行部分压缩到一个窄条里。等 kernel 快起来之后，启动开销反而成了大头，于是上 CUDA graph replay 加固定形状特化。内存表示的中间拷贝靠融合 V/T 布局组装干掉。过了 3000 微秒这条线之后优化陡然变难，这个数字本身就是有用的情报：告诉你这种循环大概在哪儿开始不划算。

他自己的结论是全文最狠的一句：你对一件事懂得越多，你就越会 prompt，因为你能把未知的未知转成已知的未知。这跟这类工具通常的卖点正好相反。循环没有替代他的专业能力，是把它放大了，而放大倍数取决于他本来就懂多少。

HN 那边补上了最该记住的一条警告：比赛 kernel 会过拟合。好几个人指出，在榜单数据上最强的方案换成分布外输入就崩，而专家手写的代码扛得住；可读性更是被整个牺牲掉——专用 kernel 无所谓，但换成要有人长期维护的库就是毒药。那条线程自己给出的总结是：把 LLM 当 Prolog 或者线性规划用最有效，给约束、给验证器、给目标。所有讲成功案例的人都有一套 harness。没有 harness 的人一个成功案例都没有。
