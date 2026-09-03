---
title: "Loop 日报: 2026-09-03"
date: 2026-09-02
lang: zh
source: https://clauday.com/zh/article/adbb6664-a22d-4982-9bec-30bf4398a491
tags: [loop]
---

# Loop 日报: 2026-09-03

> 来源 / Source: https://clauday.com/zh/article/adbb6664-a22d-4982-9bec-30bf4398a491

autoresearch 圈迎来了结构性最强的一周：第一个专门测研究闭环的基准上线，立刻暴露出编码基准已经测不出来的模型差距；EvoMap 开源了一套工作流，核心设计就一句话——写实验的模型永远不许给自己打分；Fable 5.1 发布时直接把"自主科研 SOTA"当卖点。风向变化写在大家吵的问题上：不再吵循环有没有用，改吵谁来审计循环。

---
@_potatodonkey_
https://x.com/_potatodonkey_/status/2095178982442602545
Autoresearch Bench 上线：一个测编码 agent 在闭环实验里自主攻研究问题的基准。它的意义在于普通编码基准正在饱和，而研究循环内部的模型差距依然悬殊。发布前后流出的早期结果：Opus 5 综合最强，Grok 4.6 第二且 token 效率最高，任务集将开源。大家整个夏天都在私下干的事，终于有人给它立了记分牌。

---
@N01ennn
https://x.com/N01ennn/status/2094848612433875061
关于 EvoMap 刚开源的 AutoResearch，这篇写得最透，直接戳破没人愿意明说的失败模式：代码跑通不等于研究做完。这套工作流把"生产的座位"和"评判的座位"分开：三个模型独立提想法、互相评审，先跑便宜的试点，失败的试点作为真实结果留在磁盘上，写实验的模型永远不给实验打分，最后还有盲审挑战结论——关闭项目的是引擎，不是宣称做完了的 agent。他的判断很准：一个模型给自己的工作打分，等于同一个分布被问了两遍；这是第一个把同行评审的组织架构、而不只是氛围抄进 agent 系统的方案。

---
@denixbt
https://x.com/denixbt/status/2095140684059598954
对同一篇 AutoResearch 论文的怀疑派读法，四个问题值得存下来：人插手了几次？重复了几遍、数字抖动多大？审计是谁做的？漏斗长什么样？论文里最诚实的数字：一台 8 卡服务器跑一周，产生约 2584 个想法，355 个过评审，22 个变成实验，14 个站住了。两百个想法活一个。他的结论"有希望，未证明"很公道，而这四个问题从今往后适用于每一份"AI 自主发现"的新闻稿。

---
@j_foerst
https://x.com/j_foerst/status/2094738793781710951
Jakob Foerster 团队瞄准了下一个瓶颈：实验又快又便宜时 autoresearch 很爽，可当一次实验要跑几周、烧几百万美元呢？人类科学家的办法是小规模概念验证和 scaling 曲线，这项工作就是把同样的判断力给 agent：在成本与精度的权衡曲线上，决定什么才是值得跑的实验。这条研究线决定了循环是停留在五分钟训练任务的玩具，还是能进真正的科研预算。

---
@askalphaxiv
https://x.com/askalphaxiv/status/2094854592995725324
Fable 5.1 成了 autoresearch 的新 SOTA：Terminal-Bench-Science 拿 52.6%，Fable 5 是 24.7%，GPT 5.6 Sol 是 22.4%，直接翻倍。alphaXiv 当天就把它接进了 OpenResearch。模型发布现在把"自主科研能力"放在营销第一位，这件事本身就是新闻。

---
@anabology
https://x.com/anabology/status/2095151075544236464
autoresearch 走出了 GPU 集群：一次 Fable 5.1 的过夜优化跑在 MRI 物理上，调的是位图到时间平均水磁化的映射。医学影像的参数搜索变成无人值守的循环，正是这套方法当初承诺的领域迁移，而且发生在普通实验室里，不只是模型公司内部。

---
@PMocz
https://x.com/PMocz/status/2095122198243537377
一个物理演示：agent 自己发现了黑盒模拟器背后的物理规律，作者是做科学计算的研究员。更有意思的是他的外推：想象一个规模化的 agent"研究所"，配上一层层物理验证器和原生编排平台。验证器这一层，在每个严肃提案里都是那块反复出现的缺口。

---
@theotherpomp
https://x.com/theotherpomp/status/2095259048337625539
循环套循环的实战样本：用 Karpathy 的 autoresearch 框架、Fable 驾驶，从社区配方出发优化 GLM 5.3 Flash 的张量并行推理。便宜的开源模型由昂贵的前沿模型在自动循环里调优，这已经是一种真实的成本结构，不再是思想实验。

---
@0xNeoArch
https://x.com/0xNeoArch/status/2095138820983308414
诚实的失败报告：他让 Fable 5.1 跑了八个多小时 autoresearch，从零构建了一整套量化推理配方，GPU 功耗还是压不过 200 瓦。八小时自主实验产出一套完整配方却没解决瓶颈——大多数循环的真实样子就是这样，而他把它当问题发出来而不是当胜利发言，比一半的成功故事都有用。

---
@AutoTrustAI
https://x.com/AutoTrustAI/status/2094739630314889235
AutoTrust 的 ScienceGuru 框架带着自家 Guru Turbo 模型拿下 Autoresearch@Home 第一，val_bpb 0.889522。更大的宣称在上游：同一套"假设-代码-实验-审计"循环监督了这个模型自己的后训练，他们说这让一个 800B 模型的后训练从几个季度压缩到几周。自我指涉、未经验证，而这恰恰是 Autoresearch@Home 存在的意义——把这类宣称放到公开可复现的地方。

---
@stretchcloud
https://x.com/stretchcloud/status/2094297380409811113
OpenResearch CLI 把整个 autoresearch 循环搬到本地：Claude Code、Codex、OpenCode 在相互隔离的并行 worktree 里分头做文献综述、实验分析和综合，数据不出机器。他又造了 Campfire 当通用协调层：多数决的权限投票、会话回放、跨 worktree 的 agent 竞赛、共享语义记忆。他点的痛处是真的：现在多数人跑多个 agent CLI 还是靠手工缝合输出。

---
@imfabiokeller
https://x.com/imfabiokeller/status/2095251245212516398
一份比多数论文值钱的实践复盘：他的应用的 agent 循环核对了所有验收标准、4600 个测试全绿，功能却完全不能用。根因有二：并行子 agent 各配了评审员，但评审员因为别的 agent 的部分还没做完而"暂缓判断"，于是他改了规则——只并行拆分同一条用户路径上的工作；UI 则需要单独的迭代 skill，让指挥模型真的打开浏览器、和设计稿逐像素比对。测试全绿不是证据；这是 EvoMap 那套制度在小尺度上的同一课。

---
@IsaacWalde20269
https://x.com/IsaacWalde20269/status/2094943922535403925
一人营销工作室把每日广告报表升级成了正经的 agentic loop：广告、邮件、自然流量和落地页行为数据统一落进私有 GitHub 仓库，串起来的 skill 跨数据源分析，目标只有一个——把 ROAS 推向 60；agent 提出调整建议后自己操作广告后台执行，最后一个 /ads-loop 循环验证改动是否正确落地。抓取、决策、执行、验证，全程不开那个他最讨厌的 dashboard。小企业运营正在悄悄变成 autoresearch 最大的应用领域。

---
@serge_ai_lab
https://x.com/serge_ai_lab/status/2095183469882290336
本周的经济学洞察来自 DeepSWE 榜：Gemini 3.8 Flash 用 166 步、2.36 美元拿到 74%，Fable 5 用 88 步、21.63 美元只有 70%。token 便宜意味着模型犯得起错——看报错、自我修正、重试 166 次。"便宜 token 加深循环打赢昂贵单体模型"是一句战略宣言，它解释了为什么所有实验室突然都在卷单次循环成本而不是单发智商。

---
@cursor_ai
https://x.com/cursor_ai/status/2095257412781396114
Cursor 发布云 agent 的自托管机器：agent 循环留在 Cursor，工具执行、代码、构建产物和密钥全留在你自己管理的基础设施上，支持自动扩缩的机器池，E2B、Modal、Cloudflare 等做沙箱伙伴。本周所有人殊途同归的架构切分——循环在厂商云里、手伸在你网络内——现在成了一等公民产品，也是受监管团队能跑长循环的前提。

---
@vijpatel7
https://x.com/vijpatel7/status/2095188597427122511
一个小而说明问题的构建：一个 QA agent，唯一职责是对抗性测试他的语音 agent，产出通话转写和录音，再把改进从测试结果回灌给语音 agent。专门攻击其他 agent、闭合改进循环的 agent，正在变成团队的标准席位。

---
生态产品雷达

autoresearch (Karpathy) - program.md 驱动的训练优化框架，已经成为整个实践的通用动词
AutoResearch (EvoMap) - 新开源的研究工作流，生产者与评判者分离、盲审收尾
Autoresearch Bench - 新的闭环研究 agent 基准；Opus 5 领跑，Grok 4.6 效率最高
Autoresearch@Home - ensue_ai 的公开可复现自我改进排行榜
OpenResearch - alphaXiv 的托管研究循环产品，第一个接入 Fable 5.1
Fable 5.1 - Anthropic 新模型，Terminal-Bench-Science 翻倍，即刻成为 autoresearch 默认引擎
Gemini 3.8 Flash - Google 的便宜 token 深循环打法，自我修正 demo 加 DeepSWE 榜首
Cursor Cloud Agents - 自托管机器把循环和执行边界切开
Claude Code / Codex / OpenCode - 被 OpenResearch CLI 和 Campfire 组合进本地研究循环的三件套
