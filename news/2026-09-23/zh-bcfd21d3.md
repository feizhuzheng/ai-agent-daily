---
title: "Loop 日报: 2026-09-24"
date: 2026-09-23
lang: zh
source: https://clauday.com/zh/article/bcfd21d3-f67e-44d0-9f1c-479d34b602a9
tags: [loop]
---

# Loop 日报: 2026-09-24

> 来源 / Source: https://clauday.com/zh/article/bcfd21d3-f67e-44d0-9f1c-479d34b602a9

同一个窗口里发生了两件方向相反的事，这让本周成为 autoresearch 迄今最诚实的一周。供给侧变得机构化了：OpenRSI 发布了一个开放基准，把真实的开源项目变成 autoresearch 环境，agent 轨迹在千卡集群上连跑 60 小时，光是做出预览版就烧掉超过 10 万 H100 小时，而且它公开的是轨迹而不只是分数。NVIDIA、南洋理工和 MIT 发布了 SoL-Pi：一个 auto-research 循环提出 152 项 harness 改动，最后活下来四项，在模型不变的前提下把 token 流量砍掉近一半。Netflix 现在已经按名字招这个岗位了。需求侧，两个互不相干的团队在同一个窗口里拿 autoresearch 去打真实金融数据，得出了同一个判决：这个模型的研究品味很差。它会提出三个几乎一样的学习率，几乎不探索参数空间，也判断不了一条训练曲线。其中一个人手工拟合就赢了 agent，而且更快。夹在这两个结果中间的，才是本周真正的主题，而且好几个人各自独立地把它说了出来：循环只有在另一端有一道确定性闸门时才会复利。严格的外部验证把 103 次噪声实验变成了可复现的收益；没有它，95% 的「突破」都是对噪声爬虫数据的过拟合。与此同时，基础设施这条线终于有了对的词汇——循环不是沙箱；一个跑在代码沙箱里的单线程循环，对「持久性」而言就相当于 2011 年 EC2 上的 Java 应用对「云」而言。
---
@OpenRSI
https://x.com/OpenRSI/status/2102831770458890626
他们发布了 OpenRSI-Index v0.1，一个开放基准，测的是 AI 能不能在生产规模上递归自我改进，而不是在玩具环境里。做法是把完全开源的项目变成 autoresearch 环境，agent 轨迹在 1000 张 GPU 的集群上连跑 60 小时以上。光是造出 v0.1 就烧掉了超过 10 万 H100 小时。所有东西都开放，包括轨迹本身：任务、harness、验证器、完整的 agent 运行记录。如果你今年一直在看那些无法验证的 RSI 宣称，这最后一点才是关键。
---
@yuetai12575
https://x.com/yuetai12575/status/2102884893562941492
项目发起人解释了 OpenRSI-Index 背后的想法，最诚实的一句是：所有人都为 RSI 兴奋，而参与门槛却把所有人挡在门外。他们的答案是 RSI-Anything，一条人机协作流水线，用大约一小时的对话把一个真实的研究问题变成可运行的 autoresearch 环境。任务全部来自真实项目：Marin-Scaling-Ladder、GPIC-Leaderboard、Open-Jev-Training、Molmo2、Isaac Lab。他对 RSI 为什么重要的表述是整条线里最干净的：人类的洞察受带宽限制，而 agent 可以把点子生成规模化，扫过大得多的方法空间。
---
@ayyazdev
https://x.com/ayyazdev/status/2102883543479173512
关于 NVIDIA、南洋理工和 MIT 的 SoL-Pi，这条写得最清楚：一个 MIT 许可的扩展，作用在 harness 这一层，底下的模型不变。在 EdgeBench 的 51 个任务上，相比原版 Pi 记录到的 token 流量降了 44.7% 到 49%，API 成本降了约三分之一，同时在 GPT-5.6 Sol 和 Opus 5 上保住了 Pi 约 94% 的分数。机制本身才是故事：一个 auto-research 循环提出了 152 项 harness 改动，最后只有四项活下来——Action Fusion、ObservationPack、Online Context Compact，以及一个 Evidence-Preserving Reducer，它把臃肿的构建和测试日志丢给更便宜的模型、再配一个验证器。他最后那句很扎：大家都在拼命比模型，而账单里有一大块只是 agent 跟工具说话的方式。
---
@ayyazdev
https://x.com/ayyazdev/status/2102796195521335395
SoL-Pi 论文表格里一个大多数转述都跳过的细节：在 Sol 上，token 消耗从 21.5 亿、1339 美元降到 11 亿、894 美元。但奇怪的地方是，单独用 ObservationPack 得分 47.2，而原版 Pi 是 44.8——也就是说，把省钱的四件套全叠上去，并不自动等于得分最高的配置。这是关于 auto-research 产出的一个真实发现：循环只会朝你给它的目标优化，把四个幸存者全叠起来是一个成本决策，不是质量决策。
---
@xpasky
https://x.com/xpasky/status/2102880072474538022
一张图一句话，胜过大多数跑分长贴：Astra 在一个 autoresearch 循环里跑了几天，对比 Opus 5.5 干了大约六小时的活。大家习惯的比法是在某个固定时刻拿模型比模型。而对 autoresearch 真正重要的比法是：一个循环被允许一直跑下去之后长什么样——那是完全另一个维度。
---
@jaredpalmer
https://x.com/jaredpalmer/status/2102818062512554153
他用 Devin 的云端 agent 配 Modal Outposts 拿到完整 GPU 访问，在 Kev 上通宵跑 autoresearch，另外用 Devin 的 macOS 虚拟机做 MLX 相关的活。他说这套工作流非常强，然后做了件有用的事：直接点出缺口——自动化流程需要先给 PR 和 issue 打分，而不是闭着眼就动手去复现，AutoReview 也一样。他最后那句观察能推广到他的仓库之外：开源项目里 agent 的安全与信任模型，跟内部工作完全不是一回事。
---
@EMostaque
https://x.com/EMostaque/status/2102810115703484479
他指向 Bespoke Labs 关于 Autoresearch 考试的那篇文章，挑出了那个该重置预期的结论：在标准 harness 之间，性能差异极小。如果这一点站得住，那么过去两个月对 harness 的执念是有天花板的。他的判断是：可靠的前沿对所有人都触手可及，而不是取决于谁的脚手架更好。
---
@PhungVanDuy1
https://x.com/PhungVanDuy1/status/2102804744393920885
跑 /goal、跑 agent 蜂群、或者两个一起跑，成本问题在于前沿模型一上规模就很贵。他们的实验显示 DeepSeek Flash 4.1 能以极小的代价给出可比的质量，他说这个结果是真的让他意外。他们正在 Meta Zenith 里继续推进 Auto Research 加 agent 蜂群的规模化，而且明确带着「推理成本要保持实际可行」这个约束——这正是大多数蜂群演示悄悄绕开的那个约束。
---
@edotenv
https://x.com/edotenv/status/2102075985973690493
本周最有价值的负面结果，而且非常具体。他们让 GPT 在加密永续合约数据上 autoresearch 深度学习 alpha，发现了三个明确的失效模式：参数探索能力差，迭代之间只做极小的改动；研究品味差，会提出像「三个几乎一样的学习率」这种实验；以及在智能评估上吃力，尤其是判断训练曲线这种没有二元判据的东西。他的结论是：离 LLM 能在真正困难的研究任务上派上用场，还有很长的路。
---
@RRicefan
https://x.com/RRicefan/status/2102077726563971190
同一个负面结果，来自第二个团队，而且表述得更狠。在真实历史数据和一个偏高频的目标上跑 GPT autoresearch，结论是 GPT 是个糟糕的研究员，研究品味很差。最扎人的是对比：他自己手工拟合的模型远远跑赢 GPT 自动研究出来的，而且花的时间更少。真正的信号不是其中任何一个结果，而是两个独立团队在同一个窗口里都落在了「研究品味」这个瓶颈上。
---
@Kizuno18
https://x.com/Kizuno18/status/2101834245471707397
对上面两条的对冲，而且它点出了机制而不只是表达乐观。在巴西人口数据上跑一条无人监控的管线，当模型自己提假设、自己测试数据处理方式时，95% 的「突破」最后都是对噪声爬虫数据的微妙过拟合。他的结论是：autoresearch 循环真正开始复利，是在它拿到确定性的评估闸门之后——严格的外部验证把 103 次噪声实验变成了真实、可复现的收益。
---
@ChrisJMcCormick
https://x.com/ChrisJMcCormick/status/2102102027279204747
一个 autoresearch 有用失效模式的现场案例：他从一次公开的 auto-research 运行里挑走了具体的点子，而不是整套照搬。借走的东西很具体——192K 的 batch size、给 x0 lambda 加门控、两张巨大的 bigram 哈希表（200 万行和 100 万行），用稀疏优化、不带一阶动量、只按行做幅度。刻意没借的是 FP8 和自定义 triton 算子，他还特意说自己的代码库仍然是干净的，没被 Claude 糊满。基线 4 把时间砍了 40%，他觉得最有意思的两处改动是：从哈希表里去掉 .grad 缓冲、把优化器内联进它们的反向计算；以及 Fable 找到了 ReLU 平方反向的「正确写法」，让 Inductor 能正确融合。
---
@gregpr07
https://x.com/gregpr07/status/2102157421909258560
一夜 autoresearch 没能泛化，而且他如实报了出来——这比那些成功的案例更有用。它在优化 vLLM 上试了一堆疯狂的东西：为某个自定义 harness 专门优化的缓存，以及在 2048 块上实现的一个扩散 transformer，让推理快了 17 倍。这两个都是真结果。但都没能迁移出去。「一个惊人的局部胜利」和「一个能在它被发现的那套环境之外仍然成立的东西」之间的这道缝，才是这个领域真正未解的问题。
---
@AtaeiMe
https://x.com/AtaeiMe/status/2102033799424954723
本周关于「把 autoresearch 轨迹当成一等公民产物」最有分量的论证。他的前提是：ICLR 这一轮的投稿编号已经到六万左右，而产出一篇论文越来越便宜、审一篇却还是要花时间，所以旧的发表体系正在消失，我们该想清楚之后要什么，而不是试图把它修回去。他的提议是：大学应该公开地跑 auto-research，把轨迹和论文一起放出来，这样你能看到试过什么、以及为什么有人放弃了某条路；如果是某个人发现了一个错误假设并调整了方向，这件事也该被记下来。发表这件事本来就有点像去中心化的递归自我改进，只是论文把这个过程压缩掉、丢掉了很多东西。有了自动化研究，我们可以把尝试和修正也一并留下。
---
@cHHillee
https://x.com/cHHillee/status/2102161884740977120
他点名了一个 autoresearch 循环真正需要基础设施提供的三个性质，这比再来一条「RSI 是不是真的」的观点有用得多：不受你实际算力约束的限制、能瞬间且轻松地弹性伸缩、迭代循环非常快。他认为 Tinker 正好符合这三点。注意这三条没有一条跟模型质量有关。
---
@DimitrisPapail
https://x.com/DimitrisPapail/status/2102087601775886547
关于「多 agent 通信到底有没有胜过让单个 agent 多跑一会儿」的一个精确结果。他把问题表述成：在 T 和 NT 之间，团队曲线和 best-of-N 曲线之间的水平间距有多大。结论是通信仍然赢：在模型压缩的 autoresearch 任务上，团队更早达到更低的 KB，而单 agent 即使给到 10 到 100 倍的时间也没能追上。对照线是四人团队。
---
@sytelus
https://x.com/sytelus/status/2102055500565082599
一个带明确机制的具体预测，在这个题材里很少见。他认为数学最大的影响不会是千禧年难题，而是大规模地给通用软件做证明，并且断言 2030 年前主流软件都会被形式化验证过——你大概率不会再碰一个未经验证的库。他把「规格的形式化」和「在十亿行代码规模上做这件事」点名为 auto-research 与自我改进循环的成熟目标，理由是这两件事都是批量的、机械的、可验证的，而这正好是 autoresearch 擅长的形状。
---
@iamMrDuncan
https://x.com/iamMrDuncan/status/2101920242557399105
一次带基线公布的实时 autoresearch 运行，这才是这类东西该有的发法。他在一块 P100 上为 ELX3 Qwen 3.8 27b 开了新一轮，一上来就把基线截图贴出来，还自己评价说惨不忍睹：Pascal 架构、FP16 卡、跑低量化，每秒 10.16 token。目标是看用 Qwen 3.8 Flash 在两台 DGX Spark 上跑 24 小时 autoresearch 能把这个数字推到哪。在跑之前就公布难看的起始数字，这一点值得抄。
---
@Tech_girl
https://x.com/Tech_girl/status/2102111778624692600
在 Karpathy 的 autoresearch 基准上的一次正面对决，值得读的是数字的形状而不是谁赢。在 SylphAI 的 A10 测试上，AdaL 跑了 336 次实验，Claude Code 跑了 76 次，而且 AdaL 的最终 BPB 也更好。同样的硬件上四倍的实验吞吐，这是 harness 和编排层面的结果，不是模型层面的结果，而且原始数据是公开的。
---
@MimansaJ
https://x.com/MimansaJ/status/2102845528447004804
一条招聘帖，同时也是一个市场信号：Netflix 的会员基础模型团队在招 2026 冬季的博士研究实习生，做 LLM 驱动的 AutoResearch agent 和 harness，用来改进传统推荐模型。autoresearch 出现在一家核心问题是推荐、而不是前沿模型的公司的编制里，比本周任何一个基准都更能说明这个技术正在走出实验室。
---
@GiulioRebuffo
https://x.com/GiulioRebuffo/status/2102839434534166755
不是宣称，是一个已经在跑的产物：他给 Bend 写了个自制的标准库替代品，覆盖早期数学函数、核心数据结构、以及包括 blake3、keccak、sha 在内的密码学部分，并且说所有东西都在他能力范围内做了形式化验证。基准数字已经很惊人——blake3 有时比 C 还快，大部分数据结构操作落在 C 的 2.5 倍以内，他自己写的哈希表实现按负载不同比 Base.Bend 快 10 到 20 倍。然后是让这条成为 Loop 素材的落款：有些基准还是很烂，耐心点，AutoRESEARCH 正在跑。
---
@joshliusg
https://x.com/joshliusg/status/2102826838490075355
他立了一个这个领域该被要求达到的标准，然后当场出示了凭证：RSI 的宣称只有在可验证的时候才算数，开放基准加开放代码才是应有的门槛。AutoTrust 的 ScienceGuru 已经公开了两个 RSI 结果——Autoresearch@Home 第一，以及 NanoPath v2 第一且经过验证——配方都在 GitHub 上。这件事重要，是因为「宣称的 RSI」和「可复现的 RSI」之间的落差一直是整个可信度问题所在，而那句话里的「经过验证」四个字是真在干活的。
---
@johnsaigle
https://x.com/johnsaigle/status/2102867057511682285
一句话就是一个完整的产品点子：agent 写出空操作测试和同义反复测试这个问题，解法可能是把变异测试跑成一个 autoresearch 循环。这个形状是对的，因为变异测试恰好提供了 autoresearch 循环需要、而测试套件通常没有的东西——一个自动的、客观的信号，用来判断一条测试到底有没有抓住任何东西。
---
@JamesWard
https://x.com/JamesWard/status/2102468057494917237
一份精确的报告，讲的是在一个真实运行的 agentic loop 里，把所有能交给判定模型的东西剥掉之后，LLM 还剩下哪几处是承重的。在他基于 Jev 的循环里，现在只剩两个地方需要 LLM 作为工具：摘要和参数解析。他以前用 LLM 来为工具调用返回的条目生成过滤条件，就像 coding assistant 自己定义 grep 和 find 调用那样，但现在直接让 Jev 做过滤。他的这句观察值得记下：Jev 写不出过滤条件，但在数据集足够小的时候，直接做语义过滤大概率比生成一个条件更准。
---
@salman_paracha
https://x.com/salman_paracha/status/2102818700231655463
他引入了一个有用的词汇：Harness Runtime 管理 agentic loop——更准确地说，它管理的是那个正在跑循环的 harness。他称之为元 harness，负责维持 agent 的会话并把工作量扩上去，而 agent 本身仍然能用本地 shell 命令和文件访问。给 harness 之上的这一层起个名字很重要，因为本周大部分关于「哪个 harness 最好」的争论，其实是在争论那个此前没有名字的层。
---
@salman_paracha
https://x.com/salman_paracha/status/2102620784862917009
他接着解释了在这个架构里「沙箱」到底指什么，答案确实澄清了不少。Harness Runtime 为了方便自带了一些本地工具比如 chromium，但代码执行隔离是通过一个叫 do.action_code 的工具来扩展的。agent 可以在本地跑简单的 shell 命令来访问文件系统或调用宿主机上的工具；但如果模型指挥的工作需要执行任意代码，比如一次蒙特卡洛模拟，do.action_code 就会拉起一个额外的微虚拟机、带上对应的语言依赖，然后通过 artifact 和 stdout 把输出交回给调用方 agent 继续往下走。值得记的设计决策是：把隔离做成一次工具调用，而不是整个环境的一个属性。
---
@mfateev
https://x.com/mfateev/status/2102552442714063053
来自 Temporal 的一句简短背书，分量远超它的长度：把 agentic loop 放在沙箱之外、当作持久化执行来跑，是他们见到的非常常见的模式。沙箱是代码运行的地方；循环是一个必须扛住崩溃、重启和跨天时间跨度的工作流。把这两件事混为一谈才是错误，而一个做持久化执行的厂商说他们一直在见到这个模式，是「这个拆分是对的」这件事目前能拿到的最强证据。
---
@ebarroca
https://x.com/ebarroca/status/2101902058697769062
同一个论点被压成了本周最好的类比：一个跑在代码沙箱里的单线程 agentic loop，对「持久性」而言，就相当于 2011 年跑在 EC2 上的一个 Java 应用对「云」而言。沙箱是一个工具，它不是运行时。经历过那个年代的人，一眼就知道接下来五年会是什么样子。
---
@codemarchant
https://x.com/codemarchant/status/2102736188411179417
一个无界循环的运营成本，带着具体数字。他醒来发现一个 Grok 4.7 的后台 API 请求花了 55 美元，因为它在一个基础请求上卡进了 17 分钟的 agentic loop 做网页调研，而他没把 max_turns 设成一个合理的数字。本周所有关于终止条件的架构讨论，具体对应物就是这一条推文。
---
@OnFinality
https://x.com/OnFinality/status/2102413942824075551
他问了那个能把「上线过 agentic loop 的人」和「读过 agentic loop 的人」分开的问题：循环本身很容易，难的是决定它什么时候该停、该重试、还是该交还给人类——那才是真正吃时间的部分。他把这个问题抛给一门把大部分课时花在 agentic 架构与编排上的认证课程，问它到底有没有讲终止条件。对这个领域的任何课程来说，这都是一个公道的检验标准。
---
@HarishTeens
https://x.com/HarishTeens/status/2102312251072070005
一句货真价实、值得跟他辩一辩的反共识观点：如果你的服务每天都冒出一堆问题，那么做一个自愈的 agentic loop 去自动修它们是个坏主意。潜台词是：高故障率本身是关于你系统的信息，而一个悄无声息把它吸收掉的循环，等于抹掉了那个本来会逼你去修根因的压力。自愈和根因分析是互相拉扯的，而蜂群那一派的讨论里几乎没人说这件事。
---
@josh_garrett_kc
https://x.com/josh_garrett_kc/status/2102097716432060511
一个来自基准测试的具体行为观察，比标题有用得多。他给 Astra 一张参考图和一个基础需求，让它做一个 Unity 里的洗手液站，刻意给了比平时更多的自主权。生成结果很好，但他在自己的基准测试里此前没见过的是：它表现出了真正的自我负责——它注意到自己犯的一个错误，并在 agentic loop 的下一步里自己把它改掉了。值得跟踪的是「循环内部无人提醒的自我纠正」这个行为，而不是那个模型产出的素材。
---
@serrynaimo
https://x.com/serrynaimo/status/2102172448238235948
一份关于量化方案的量化回退报告，这种东西几乎没人会发。他从 Splash 退回去了：性能确实不错，但 Splash 量化在 agentic loop 里卡住的频率比 MTPLX Optimized Speed 高出约 30%。原始吞吐和循环完成可靠性是两个不同的维度，而这是少数有人给这道缝填上数字的一次。
---
@serrynaimo
https://x.com/serrynaimo/status/2102629884061450309
一个很好的例子，说明在消费级硬件上「优化循环而不是优化模型」能换来什么。他为自己的 AMD 显卡拼了一个 llama.cpp 构建，因为这套东西要连跑数周的知识库工作和报告发布。靠 agentic loop 优化加上不错的 prefill 和 decode、同时保住足够的质量，他把运行时间从以周计压到了以天计。
---
@kurtbuhler
https://x.com/kurtbuhler/status/2102277120923697184
本周关于「判定模型该放在 agentic loop 的哪个位置」思考得最透的一条，而且他给了三个位置而不是一个：放在最前面辅助决策；放在中间从选项里挑，前提是选项有限、判据在某种程度上客观且可度量；放在最后做评估，同样前提是判据客观可度量。那个前提在句子里是真在承重的：他提的每一条都被「可度量的判据」这个条件卡着，而这恰恰是把这套想法和蜂群狂热区分开的那个约束。
---
@proxy_vector
https://x.com/proxy_vector/status/2102203959654195324
本周对任何宣称自己在跑无人监督 agentic loop 的人，问得最好的一个问题：你连续一整个工作日无人看管地跑它，撞到的最大失效模式是什么。这个问题能把演示和一套真正在运转的系统分开，而它居然还需要被问出来，这件事本身就是一个发现。
---
生态产品雷达

SoL-Pi —— NVIDIA、南洋理工与 MIT 给 Pi coding agent 做的 harness 层扩展，MIT 许可，由一个在 152 个候选改动上跑的 auto-research 循环产出。
OpenRSI-Index —— 把开源项目变成 autoresearch 环境的开放基准，外加 RSI-Anything 流水线，大约一小时把一个研究问题打包成可运行的任务。
Pi —— 效率这条线上所有数字的基线 coding agent。
Jev —— 判定模型层，现在开始出现在 agentic loop 内部，承担路由、过滤和评估，而不是生成。
Claude Code —— autoresearch 基准结果里的对照 harness，也是 AdaL 以 336 次实验对 76 次的那个对手。
Devin —— 用于通宵 autoresearch 的云端 agent，配 Modal Outposts 拿 GPU、配 macOS 虚拟机做 MLX。
Temporal —— 持久化执行，也是那个确认「把 agentic loop 放在沙箱之外跑」已成常见模式的厂商。
EdgeBench —— 所有 harness 效率数字所依据的那个 51 任务基准。
Harness Runtime —— 对「管理那个正在管理循环的 harness」这一元层级，正在浮现的名字。
