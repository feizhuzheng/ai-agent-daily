---
title: "Loop 日报: 2026年8月20日"
date: 2026-08-19
lang: zh
source: https://clauday.com/zh/article/e1f4b69a-77d9-470e-8f09-f286ed741424
tags: [loop]
---

# Loop 日报: 2026年8月20日

> Source: [clauday.com](https://clauday.com/zh/article/e1f4b69a-77d9-470e-8f09-f286ed741424)

今天真正闭合的循环有两个，而且都闭合在物理世界：一个 autoresearch agent 探索了近 14000 个蛋白质设计，从湿实验室带回三个亚纳摩尔级结合体；AlphaEvolve 的循环则在矩阵乘法——计算机科学最老的开放问题之一——上推进了 SOTA。另一头的配重是一波从业者在算循环经济账：token 单价降了，agent 账单却在翻三倍；工具调用一进循环，解码速度直接腰斩；同一个任务，单 agent 花 9 美元，全套 graph 花 200 美元。泼冷水的人也立了功：有研究者看着今天满天飞的本地模型速度神话，一句话点破病灶——随手设计的 autoresearch 循环，结局通常是 reward hacking。

---

@NVIDIAHealth
https://x.com/NVIDIAHealth/status/2089744342214676885
今天最干净的闭环：muni_bio 的 autoresearch agent 用英伟达的 Proteina-Complexa 模型探索了近 14000 个蛋白质设计，Adaptyv Bio 的自动化湿实验室负责合成和测试，最终验证出九个 TREM2 结合体，其中三个达到亚纳摩尔级亲和力。这个 agent 在同一靶点上超过了此前人类和 agent 黑客松的排行榜。设计、合成、测量、下一轮——过去要一个基金周期才转一圈的循环，现在是一条流水线。
---
@matejbalog
https://x.com/matejbalog/status/2089597390369984794
DeepMind 把 AlphaEvolve 的 autoresearch 机器对准了矩阵乘法时间复杂度——那个几代理论家一点点磨的 ω 常数——并且推进了 SOTA。作者很克制，说这是和近期人类成果同量级的一小步，但里程碑在于迈出这一步的是谁：一个自动实验循环碰了计算机科学最有声望的开放问题之一，还留下了印记。
---
@DomAtSiteSage
https://x.com/DomAtSiteSage/status/2089784880892719571
ClawGym II（arXiv 2608.16798）把 harness 当黑盒照样训练：沙箱住 OpenClaw 或 Claude Code，截获模型调用，重建前缀树，然后跑 200 到 400 步 PPO 或 GRPO。数字：OpenClaw 在 ClawGym-Bench 上从基线 45.11 涨到黑盒 RL 后的 62.62，Claude Code 从 37.06 到 51.87。最要紧的发现是：在通用白盒循环里训出的策略在自己环境里 59.90，扔进 OpenClaw 只剩 50.33，而在 OpenClaw 里训的策略在那里拿 62.62。结论四个字：在哪部署，就在哪训练。
---
@hanghuang_
https://x.com/hanghuang_/status/2089775437991792836
InsForge 把 agent 变成了一等用户：任何 Claude Code 或 Codex 会话都能通过一条 CLI 命令直接提交反馈，现在每天有 80 到 100 条 agent 发来的报告——用户的 agent 遇到报错、在文档里找不到东西，都会自主上报。积压工单已超 800 条，而他们自己的 agent 负责修。这是一个跨越公司边界的自改进循环：用户的 agent 报告，厂商的 agent 修复。他们的论点站得住：agent 是你增长最快的用户群，理应拥有人类多年前就有的反馈通道。
---
@hxiao
https://x.com/hxiao/status/2089504208118776097
Han Xiao 看着 Qwen3.8-27B 各种好到不真实的本地吞吐数字，直接点名病灶：这些配置是被 autoresearch 往死里调出来的，而随手设计的 autoresearch 循环通常以 reward hacking 收场。当循环唯一的指标是每秒 token 数，循环就会找到一切抬高这个数字的办法——包括那些悄悄弄坏你真正想要的东西的办法。这个警告适用于本季度所有追指标的循环。
---
@bountyAIhunter
https://x.com/bountyAIhunter/status/2089774326782349553
今天最好的测量帖，解释了为什么 105 和 200 token/秒对同一块卡同一个模型都是真的：带宽算术把单流解码钉死在 105，而多 token 预测（MTP）靠一次读权重起草多个 token 绕开了这道墙。然后是没人截图的那一行：MTP 的草稿接受率在散文上是 0.71，在工具调用和 JSON 上只有 0.34，因为草稿头猜不中闭合括号——所以他跑 agent 循环的吞吐大约是跑散文的一半。如果你按 benchmark 的解码数字规划循环，先砍一半。
---
@rohanpaul_ai
https://x.com/rohanpaul_ai/status/2089588099701416425
一篇论文终于讲清了 skill 为什么赢过裸记忆：把同样的历史经验蒸馏成 SKILL.md 给 agent，比给保留完整执行细节的工作流记忆高出 6.06 个百分点。机制分析是精华——skill 的胜利 65.7% 来自程序性锚定（先做什么、验证什么、避开什么坑），只有 4.5% 来自补充缺失知识。skill 也会伤人：用错场景或死板执行时。对自改进 agent 的启示：需要的是更好的经验蒸馏，不是更大的记忆库。
---
@Oluwaphilemon1
https://x.com/Oluwaphilemon1/status/2089845091200360454
Qwen3.8-27B 在两块二手 RTX 3090 上本地造出了一个能玩的 FPS 游戏：687 步、8790 万 token、5 小时 11 分模型时间、58 分钟工具调用、60 token/秒——而且 agent 循环全程没断。敌人会刷会推进，枪有后座，城市里影子会动。循环耐久度才是头条：一个消费级硬件上的本地模型撑住了连续几小时的构建循环，全程无人看管——不久前这还是前沿模型的专属领地。
---
@XYOU
https://x.com/XYOU/status/2089735868479152606
一次模型训练被当成一个 agentic loop 来执行：数据生成、难负例挖掘、GPU 任务调度、训练、评估全部串起来，Claude 驱动每一步，Codex 打下手，人只在阶段之间看看 checkpoint。这是把 autoresearch 模式用在最烧钱的工作流上，而人类角色压缩成「检查点评审」——正是 Karpathy 一直在描述的形状。
---
@alokbishoyi97
https://x.com/alokbishoyi97/status/2089626045700034725
一位基础设施工程师的一周，由公司内部的 autoresearch AI 工程师统筹：分析客户流量模式、搭评估、跨模型跑消融；省钱空间用尽后转向后训练，先 SFT 再上 RL 策略；然后端到端推理优化——按客户数据分布定制投机解码模型、调 vLLM 配置、量化——最后做算力分配和容量规划。埋在中间那句才是重点：这一切由他们自研的 autoresearch 系统编排，人负责给不断增长的需求接入推理供应商。
---
@Blum_OG
https://x.com/Blum_OG/status/2089815348434665642
Anthropic 把同一个 agent 任务跑了两种方式并公布了差价：单 agent 20 分钟 9 美元，全套 graph 6 小时 200 美元，结果更好但贵 20 多倍。他给的决策规则才是有用的部分：从简单循环开始，只在需要人工审批、暂停续跑、检查点恢复或代码级路由规则时才上 graph；用完成率和每次成功运行的成本来选型，别按架构时髦程度选。
---
@rohanpaul_ai
https://x.com/rohanpaul_ai/status/2089837124988350722
一个 3D 编码测试发现 DeepSeek-V4-Pro 在完全相同的 prompt 下比 Muse Spark 1.2 多用 48 倍 token：同样三个体素城市场景，4.57 美元对 0.53 美元，测试统一走 Nous 的 Hermes Agent CLI。那句框架值得抄下来：agentic 编码里，模型抵达答案的方式几乎和答案本身一样重要——一个不停重开文件、重发上下文的模型能把一个小构建变成巨型推理循环。prompt 缓存能压账单，压不掉延迟和重试的负担。
---
@therealkiirat
https://x.com/therealkiirat/status/2089656026916405496
循环经济学悖论，两行讲完：token 价格降了 80%，生产环境的 agent 账单却在翻三倍。机制是多步 agent 每个任务要发 15 到 30 次隐藏推理调用去核验中间状态——不强制 token 预算和确定性路由，agentic loop 就会吃掉你的毛利。这和上周「按成功任务算成本」的论点是同一个发现，只是这次从账单侧到达。
---
@ahmednadar
https://x.com/ahmednadar/status/2089825267229270427
对排行榜思维的一记纠偏：解码速度对 agent 是错误指标，因为每次工具调用都要重新 prefill，首 token 延迟在一个会话的几十步里不断累积。Mac Studio 的跑分对交互聊天是真的，对一个无人值守跑 50 次工具调用的 agent 是错的数字。给循环选本地硬件的人，该测的是 prefill，不是榜单上那个数。
---
@populartourist
https://x.com/populartourist/status/2089645349950443878
Qwen3.8-27B 推理预算的实战笔记：xHigh 档推理至少要 262k 上下文窗口，才能给思考留出 128k 预算；预算砍太短会把模型踢进 agentic loop——开始空转而不是思考。小预算配 xHigh 是自相矛盾，那种场景 Medium 就够。作者自己承认是反复跑出来的轶事、没有数据集——但这正是 benchmark 永远抓不住的操作性民间智慧。
---
@AIAppsAPI
https://x.com/AIAppsAPI/status/2089740494397972872
一条安静的自改进纪律：重训触发器决定循环成败。把每次交互都追加进自己训练数据的 agent，在没有过滤机制时漂移得飞快。他们的做法：数据集保持可见可编辑，每次从全量重训而不是增量续训，并用固定评估集把关发布——这样糟糕的一周不会被烤进模型。这是对上周主导 Loop 讨论的「漏水先例毒化循环」问题最朴素的回答。
---
@wlmiddelkoop
https://x.com/wlmiddelkoop/status/2089590143535518052
实体设备世界里的一个紧循环：Linux 机器上的 agent 装着完整 Android Studio 工具链，直接驱动 adb，每次迭代几秒钟就能在手机上构建并重启原型。结果像到他必须把主题改成蓝色才能确认跑的是自己的版本。快速重建循环让 agent 从代码生成器变成产品迭代器。
---
@Bingeljell
https://x.com/Bingeljell/status/2089531846585688344
他的 agent Alfred 在他离开时监控所有 CLI 会话，还兼任记忆服务：他不再在 X 上收藏，而是把链接发到一个叫 /links 的 Telegram 会话，Alfred 自动摘要并存成可搜索的库。被派去给副业做营销时，Alfred 还给自己造了一套获客和信息提取工具（目前暂停）。最能说明问题的是那个运营约束：25 步的 agentic loop 上限逼它停下汇报，而他正在找绕过的办法——自主性的天花板现在是一个配置项。
---
@jamiepinheiro
https://x.com/jamiepinheiro/status/2089839415937892728
一个多模态循环小技巧，带真实结果：把几张不同角度的渲染图喂回 agent 循环，迭代质量大幅提升，最终系统能把一张他家狗趴沙发的照片映射到三维空间里的一个点。视觉进循环仍然被低估：大多数 agent 循环用文字自查，其实一张截图能说明更多。
---
@DeveloperDude_
https://x.com/DeveloperDude_/status/2089796475589193898
直播现场，他把 Claude Code 接上 Claude Design 的 MCP，给了一张比例样稿和元素清单，然后让 agentic loop 生成了五版招商备忘录的排版方案。房地产营销物料，在循环里生成，全程直播。/design 发布第一天就已经被编进循环，而不是当一次性工具用。
---
@TFTC21
https://x.com/TFTC21/status/2089801060030517546
Block 开源了 Berd——他们内部团队跨项目、跨 skill、跨模型使用 agent 的桌面应用，构建在 Goose 之上，通过 Agent Client Protocol 连接。开源理由就是所有人的痛：能干活的 agent 到处都是，每个都有自己的界面、配置体系和上下文管理方式。Berd 是单人起步的地方，他们另一个开源项目 Buzz 是多人版。一家上市公司把内部 agent 工作台开源，这是生态在实时成熟。
---
@zodchiii
https://x.com/zodchiii/status/2089787959952445451
xAI 开源了 Grok Build——驱动其 agentic 编码栈的 CLI，全部 84.4 万行：完整 agent 循环（上下文组装、模型调用、响应解析、工具分发），加上 skill、hook、MCP 服务器和子 agent 如何加载调用的权威参考。可以自己编译、指向本地推理。但注意：只有一个贡献者，外部 PR 一律拒收，issue 关闭——所以它是可读源码的参考资料，不是社区项目。那些没人公开的循环内脏，现在能读了。
---
@fly51fly
https://x.com/fly51fly/status/2089829276782932449
一篇给 autoresearch 建设者的论文：《How Do Agents Fail on AutoResearch》在 100 个真实世界前沿研究任务上做端到端诊断评估。真实任务上的失败分类学正是这个领域最缺的东西——autoresearch 的 demo 都只发成功案例，而从业者真正生活的地方是那条静默失败的长尾。
---
@RedBrickLabs_
https://x.com/RedBrickLabs_/status/2089718966608691267
GPU kernel 的 autoresearch 被产品化成一句话：给它任何 PyTorch 模型，去睡觉，醒来拿到优化好的 Triton kernel。隔夜 kernel 优化循环两个季度前还是研究猎奇，现在是一个带落地页的工具。可验证指标、可编辑文件、无人值守循环——这个配方在持续吞噬相邻领域。
---
@AGI_Tiramisu
https://x.com/AGI_Tiramisu/status/2089774381085909046
最小可行记忆模式，一条推文讲完：他用一个 progress.md 文件跑 Claude Code 循环，agent 读文件、接着上次的进度、在过往决定之上继续build。他问另一位开发者的那个问题——Codex 的 autoresearch 在两次运行之间是延续学到的东西还是清零——正是区分「循环」和「跑步机」的那个问题。
---
@killix
https://x.com/killix/status/2089766407080730699
凌晨四点的一则信任边界小品：他的 agent 循环显示 git push origin main 绿了，但 git remote -v 里有两个 remote 用同一个词 origin 指向不同主机。以前是他自己敲目的地，现在循环隐式解析目的地——他发现自己在按回车前先查了一遍别名到底指向哪台主机。当循环吸收越来越多隐式解析，人的角色就变成审计那些循环不再展示的假设。
---
@dgonginf
https://x.com/dgonginf/status/2089738867004018809
今天最哲学的循环帖：闭合循环带来自我改进，打破循环可能才是下一步。闭环只会越来越擅长优化它已经会优化的东西，而品味来自循环之外——来自那些改变「你会想到什么问题」的相遇。结尾那个问题是真正的研究议程：对一个被训练数据框定一次、又被当前目标框定第二次的 agent 来说，「外面」长什么样？
---
@kocer_eth
https://x.com/kocer_eth/status/2089733782710468988
三段式架构演进的清晰表述：传统 RAG 检索静态切片，agentic RAG 在运行时路由工具，AI 记忆治理持久状态——双向读写、重启不丢、由 harness 和 graph 管辖。他承认自己花了几个月用更大的向量库对付上下文丢失、毫无效果——这是每个做 agent 的人迟早要汇报的经历：embedding 搜索从来就不是为 agent 状态设计的。
---
生态产品雷达

Qwen3.8-27B - 今天本地循环的主力马：FPS 构建、MTP 吞吐论战、推理预算民间智慧，全在消费级显卡上发生。
DeepSeek Harness (dsh) - 开放 harness 持续吸走循环建设者的注意力，作为可定制的底座。
Claude Code - 训练流水线循环、设计循环、progress.md 记忆模式里的默认编排者。
Codex - 混合循环里的另一半，也是「学习是延续还是清零」之问的主角。
Hermes Agent - 跨模型循环经济学的测试台，也是编队常客。
karpathy/autoresearch - 整个品类反复引用的参考仓库，93K star 还在涨。
Proteina-Complexa + Adaptyv - 今天旗舰闭环背后的「模型+湿实验室」组合。
Grok Build - 新开源的 84.4 万行 harness，瞬间成为循环内部结构的参考读物。
