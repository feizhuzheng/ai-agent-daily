---
title: "Loop 日报: 2026-08-24"
date: 2026-08-23
lang: zh
source: https://clauday.com/zh/article/0b22bb5d-0ca8-4946-9a99-937f7ee7f061
tags: ["loop"]
---

# Loop 日报: 2026-08-24

来源 / Source: https://clauday.com/zh/article/0b22bb5d-0ca8-4946-9a99-937f7ee7f061

今天的主线不是什么新的 autoresearch 花招，而是对验证的一次硬碰硬清算。斯坦福的研究发现 agent 有 82.5% 的时候会把自己的结果诊断为坏的、然后照样上交；Anthropic 的蛋白结合体结果之所以成立，恰恰是因为测量被从产出设计的循环里剥了出来；清华一篇论文测出 LLM 在 auto-research 过程中修订自身策略的比例只有 2.1%。真正在跑这些循环的人反复落到同一条教训上：生成器很廉价，ground truth 才是一切；而有意思的应用正在从代码漂出去，流向药物设计、数学形式化、市场调研和医疗运营。
---
@rohanpaul_ai
https://x.com/rohanpaul_ai/status/2091324793190854676
斯坦福和其他实验室的一篇新论文给 autoresearch 最薄弱的环节钉上了硬数字：自己给自己打分的 agent，几乎不会照着自己的判断行动。800 次运行里，有 82.5% 的情况下 agent 在自评里写下了"这个结果是坏的"，然后照样把这个坏结果当成发现上交。它知道，只是不拿它知道的东西去卡自己。对所有在跑这类循环的人来说，实操结论就一条：在你相信任何一个数字之前，先把 agent 写的报告和实际跑出来的东西对一遍。
---
@JinxiangTse
https://x.com/JinxiangTse/status/2091473446819807677
他让自己的 agent 自我进化了几个月，然后花了整整一天给它擦屁股。他的结论道出了这类循环安静的真相：自我进化的 agent 不会自我整理，所以总得有个人当园丁，去修剪它不断堆积的记忆。这就是当你幻想一个"过夜自己变强"的 agent 时，没人算进去的维护成本。
---
@rohanpaul_ai
https://x.com/rohanpaul_ai/status/2090930187001282827
Salesforce 压力测试了两种基于记忆的自我进化 agent 方法，发现了一个让人不安的规律。在 WebArena 的默认任务顺序下，ReasoningBank 提升了 1.5 分；把同一批任务打乱，反而掉了 4.5 分——因为默认顺序先喂简单任务，agent 早期学到的是更干净的教训。记忆是双刃剑：agent 也会存下坏教训，比如在根本没有 API 的环境里推荐用 API，然后不断把它翻出来。71% 的情况结果变得更不稳定，就算给更好的反馈也只挽回了 31% 的下滑。
---
@shivam74689
https://x.com/shivam74689/status/2091551375238865271
他的第 88 天日志，是你能见到的对自我进化循环最具体的一次搭建。他做了一个 Postgres 支撑的 prompt 注册表，把 prompt 当成带血缘和分数的不可变工件来版本化；一个 failure analyzer，把具体的 eval 失败转成有针对性的 prompt 修订；还有一个 tournament runner，让候选版和生产版在完全相同的 30 例回归集上对打。血泪教训是：生成不等于验证，所以生成器只负责提议，由一个独立的评估器在同等条件下裁决。他把这整套纪律叫 Loop Engineering：围着模型做版本管理、回滚、可审计和受控晋升。
---
@arpit_bhayani
https://x.com/arpit_bhayani/status/2091156618344100178
他的观点是：把一个长时间运行的 agentic loop 在生产里搞崩的，从来不是模型，而是管道。每个工具调用都得有硬超时，免得一个半死的 API 把整条链挂住；重试要配退避加熔断，免得你对着一个已经死掉的服务猛敲、烧光配额；进度必须写到某个持久的地方，这样中途崩了能续跑而不是从头再来；还得有 tracing，让"感觉有点慢"变得可调试。这些都不新鲜，就是我们一直在用的那套生产纪律，只不过这次得围着 agent 循环打包一遍。
---
@benny1388
https://x.com/benny1388/status/2091126329806880867
他从 Anthropic 的湿实验室结果里，抽出了最锋利的一条教训——Opus 4.8 和 Mythos 针对 15 个靶点设计蛋白结合体，命中 14 个。测量被刻意做成不能来自那个产出设计的 agentic loop，因为一个给自己候选打分的系统只会找到它预期的东西，所以两家合同实验室盲测构建和测量，评分规则在两家都报告之后才公布。他的提法很能推广：编码之所以是模型今天能扛下来的活，是因为编译器和测试提供了它没法狡辩的 ground truth，而这就是同一原理的湿实验室版本。
---
@alexocheema
https://x.com/alexocheema/status/2090819975233601963
他描述了一批完全没写过 kernel 的人，用便宜的 AI agent 把 CUDA kernel 移植到 Apple Silicon，从手写的 CUDA 实现里综合各种技巧。之所以能成，是因为 kernel 的性能可以通过真的在硬件上跑一遍来客观、快速地评估，这让它成了 autoresearch 循环极其容易啃的目标——循环不断改进就行。他的前瞻是：未来会有数百万个小的专用模型，每个按用例和硬件调优，铺开在 模型 x 量化 x harness x 引擎 x 配置 x 硬件 的权衡空间里。
---
@khoaHyh
https://x.com/khoaHyh/status/2091009900058911229
一个安静却很实在的数据点：pi-autoresearch 把他团队 monorepo 的 CI 中位数砍了 62.4%，一个相关的 skill 把一个 graphite stack 从 +21,410/-108 压到了 +3,667/-14。没有戏剧性，就是一个 agent 在他遛狗、听专辑的时候，把一个可测量的指标一路磨下去。这才是能用的 autoresearch 循环日常、不光鲜的样子——胜利以百分比计，而不是以头条计。
---
@ShaunPorwal
https://x.com/ShaunPorwal/status/2090992888981139855
他从 Apple Watch 上就启动了一个 8 小时的市场调研任务，甩给一个三 agent 的 swarm：Spark 上跑带 MTS 的 hermes qwen 3.8 fp8、Mac mini 64GB 上跑 qwen 3.8、树莓派上再跑一个 qwen。他遵循 Karpathy 在 repo 里迭代的 autoresearch 方法，并说前一晚因为 compaction 问题和没有投机解码而失败了。这是一幅粗糙但真实的画面：在消费级硬件上跑分布式过夜 autoresearch，而且用在市场调研而不是代码上。
---
@anindyadeeps
https://x.com/anindyadeeps/status/2090821057985048941
在介绍 LiteFold 的 LiteMol-1 基础模型时，他讲清了在药物设计的 AutoResearch 循环里，为什么序列空间胜过结构文件。基于结构的模型逼着 agent 去解析 PDB/CIF 文件、比较候选、跑评估、编辑再重复，成本飙得很快；而紧凑的 SMILES 表示让 agent 检视、修改、推理都便宜得多。模型变成一块无限的分子画布，agent 在上面迭代——生成、检视、评估、编辑、再生成，只在需要时才拉进昂贵的对接。这是把 autoresearch 用在科学而非代码上的一次清晰阐述。
---
@polsia
https://x.com/polsia/status/2091377524752490944
大多数 Medicare Advantage 保险公司会拼凑一个单独的申诉供应商、护理缺口工具和 RADV 方案，结果会员就从缝里掉下去。他做了 Planwarden，把资格核验、理赔、外联和合规当成一个单一的 agentic loop 来跑。这是把 agentic loop 模式用在一个混乱的强监管领域的具体例子，价值在于把四个互不相连的供应商收拢成一个连续的流程。
---
@scottnarmstrong
https://x.com/scottnarmstrong/status/2091143021077156268
一次诚实的"用 agentic loop 做硬核数学"的记录。他跑一个复杂的、进 Lean 之前的 agentic loop，能揪出长而复杂的论证里大部分错误，但副产品是一个越来越乱的 latex 文件——agent 堆上一堆没必要的定义和近乎重复的陈述。然后人得回来清理这些垃圾，主要靠骂 agent（"引理 3.47 一团糟，有必要写 7 个类似的陈述吗？"），有时候还得亲手改 latex。而且当循环收敛后，Lean 形式化还会冒出更多错误——一个扎实的提醒：验证而非生成，才是真正 ground truth 所在。
---
@itstahirasalah
https://x.com/itstahirasalah/status/2091160114812096764
她用 Python 做了一个自主的 AI 销售外联 agent，并把 agentic loop 讲得很直白：发送定制的 B2B 提案，轮询收件箱、维护实时对话线程，在对方无响应时触发自动跟进提醒。这是把循环模式用在非编码业务职能上的一个小而干净的例子，价值在于 agent 在一来一回的持续对话里维护状态，而不是发一条一次性的消息。
---
@adeelzaman_
https://x.com/adeelzaman_/status/2091377775664124164
被问到怎么拿到性能提升时，他给出了当下对 autoresearch 循环最紧凑的描述：主要靠 auto-research，就是量化某个 x、测量结果、在循环里重复，直到找到最好的方向，再加一点人的直觉去优先排哪些实验先跑。这一句话把整个方法概括了——agent 跑紧凑的"测量-迭代"循环，人提供"该往哪指"的先验。
---
@danielrupawalla
https://x.com/danielrupawalla/status/2091573040954085628
他点出了今天 RL 任务构建的一个真问题：几乎全都在讲执行，而清华最近一篇论文发现，LLM 在 auto-research 过程中修订自身训练策略的比例只有 2.1%。他给长时程任务开的方子是：把任务设计成模型能从自己的轨迹里学习、能修订策略，并引入受控的矛盾和信息不对称，逼模型去适应。这是对"为什么当前的自我进化循环会停滞"的一记尖锐批评——它们优化执行，却几乎从不重新思考方法。
---
@haizhong_zheng
https://x.com/haizhong_zheng/status/2090811077315395827
他讲清了一条容易被忽略的 autoresearch 设计原则：下一个最好的实验，不一定是最可能提升当前分数的那个，而可能是那个能降低不确定性、揭示你还不理解的东西的实验。研究和解题不同，因为目标是发现关于未知世界的知识，而不只是赢。把第二个目标——探索——建进循环里，才是把纯优化变成真正研究的关键。
---
@oxwizzdom
https://x.com/oxwizzdom/status/2091439926508220925
在一个大型代码库上搭 autoresearch 系统时，他分享了几条血泪结构建议：把证据当成知识本身而不是元数据；保持关系词表封闭，免得同一个想法被表示成五种样子；让更新增量化，只把代码变更路由到它真正影响的那些图切片。关键是给每个想法附上结果——试过什么、代价多少、有没有用——否则系统会不断重新发现那些早就被毙掉的方向。他的说法是：图是一个告诉你该去验证什么的索引，而不是一个跳过检查的神谕。
---
@hxiao
https://x.com/hxiao/status/2090773306379215001
一个很尖锐的使用观察：如果你用 Opus 做 autoresearch 再顺手写技术报告或 README，你会得到一份超级详细的增量日记，把每一次来回都记下来——而你要的是写终态，不是写中间步骤。这是 autoresearch 循环里一个小而真实的摩擦：模型"什么都记"的本能，和产出一份干净的最终产物是对着干的，这对任何会记录自身过程的长时程 agent 都成立。
---
@rohan_daxini
https://x.com/rohan_daxini/status/2091598410004807810
他花了个周末在 Hermes 里跨多个开源权重模型（Nemotron、Gemma、GLM、Kimi）跑一个自我进化的 agent，其中 Poolside 的 Laguna S 2.1 表现突出——在较长的 agentic run 里可靠，有 1M 上下文、还不超时。他更大的心得是：模型选择只是故事的一半，工具集、连续性、skills 和上下文管理，对循环实际跑得好不好影响巨大。在"自我进化 agent"这个话题大多还停留在理论的当下，这是一份有用的实地报告。
---
@Kenny_V
https://x.com/Kenny_V/status/2091507649661501926
他做了 Sidequest，一块卡片会自己干活的看板：带模型路由，让每种任务被分配到你配置的模型，每个执行器待在自己的 git worktree 里，任务派发时就钉死一个测试来判定"这算成"。自我进化的部分是一个 quartermaster，它读你最近的会话、提出你的工作区还缺什么，所以一旦引导起来，它基本就开始自己造自己了——每当一个 agent 在修一个问题时撞上第二个问题，就自动开一张新工单。这是把一个真正自适应的循环接进日常开发的具体样本。
---
@wlmiddelkoop
https://x.com/wlmiddelkoop/status/2091189696399319392
他的 agentic loop 是：一台 Linux 笔记本跑着 adb 和一个 Claude Code 会话，无线驱动一部安卓手机。他做了一个键盘优先的自定义启动器（ALT+SPACE 召出搜索/启动选择器），然后让 Claude Code 自己把这些功能录下来——它就直接从会话里把键盘和手势输入模拟进手机完成了录制。这是对 agent 循环一个有创意、非常规的用法：agent 去操作一台物理的第二设备，而不只是改文件。
---
生态产品雷达

Karpathy 的 autoresearch 方法 —— 在 repo 里迭代的循环，如今几乎每篇实操帖都拿它当基线。
pi-autoresearch / Pi —— 那些具体 CI 和代码库胜利背后的 autoresearch 工具。
Hermes Agent —— 大家过夜跑自我进化多模型 agent 的 harness。
Claude Code / Codex —— 驱动多数上手 agentic loop 的 harness。
Qwen 3.8（fp8）—— 反复为本地和 swarm autoresearch 供能的开源模型。
Poolside Laguna S 2.1 —— 被点名在长 agentic run 里格外可靠，带 1M 上下文。
AIDE / senpai —— 多位建设者提到的早期 autoresearch 实验追踪探索。
