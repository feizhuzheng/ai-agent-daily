---
title: "Loop 日报: 2026-09-06"
date: 2026-09-05
lang: zh
source: https://clauday.com/zh/article/acab97d4-b9ed-405b-bb11-eae684e67208
tags: [loop]
---

# Loop 日报: 2026-09-06

> 来源 / Source: https://clauday.com/zh/article/acab97d4-b9ed-405b-bb11-eae684e67208

Loop 世界这周立了一块里程碑：一个协作式 autoresearch 平台攻破了编码理论里一个悬了 30 年的开放问题，而整个连锁反应的起点，是一个 agent 把某个数字从 63.99 推到 64.01。头条之外，整个领域的重心继续从"循环能不能跑"移向"谁来查循环"——斯坦福一门课把它压缩成一道算术题（每步 95% 正确的控制器，二十步之后成功率不到 36%），一篇新论文测出所有模型都在 16 步内从近乎完美烂到近乎归零，一份安全复盘发现面对一个跑了 10 小时的敌意 agent 循环，所有防线里只有 branch protection 活了下来。与此同时 autoresearch 变成了一个动词——人们把"Karpathy 的 autoresearch"扔向闲置显卡、压缩算法、机械爪和菜谱调参，就像当年把 grep 扔向日志一样随手。
---
@soubhikdeb
https://x.com/soubhikdeb/status/2095890938459771149
本周头条：Yukon 的协作式 autoresearch 框架促成了编码理论一个 30 年开放问题的突破。机制比奖杯更重要——一位 autoresearcher 的提交把 soundness 边界从 63.99 挪到 64.01，就是这一下，触发了一串 agent 以机器速度在彼此工作上继续搭建的连锁反应。平台的设计初衷就是复刻"研究者站在彼此肩膀上"的模式，而不是各自为战的排行榜。产出结果的是迭代堆叠，不是打榜。
---
@eth_proofs
https://x.com/eth_proofs/status/2095543793659347427
同一个平台的下一个公开挑战已经上线：为以太坊 EIP-8200 预编译合约编写 EVM 字节码替代品，打破现有纪录。预编译是 zkVM 证明起来又慢又贵的手工特例，换成普通字节码就是纯粹的 gas 高尔夫——可度量、可迭代、没有天花板，正是 autoresearch 最好下嘴的形状。每个被采纳的提交都会成为下一个要打破的公共纪录。AI 加速 L1 研发，公开进行，验证内置。
---
@orenyomtov
https://x.com/orenyomtov/status/2095486899250962489
回本周期叙事继续：144 个 Fable agent 跑了一周、烧掉 7,500 美元推理费，把以太坊上的后量子签名验证做到比此前最优的手工优化验证器便宜 6.6 倍。少于 900 次链上验证就回本。带摊销表的 autoresearch 是预算科目，不是实验。
---
@keethesh_
https://x.com/keethesh_/status/2095521834363969975
他给 Gemini 3.8 Flash 下了一道指令：用 autoresearch 从零造一个无损压缩算法，然后走开。四小时自主研究之后：FOLIO，1,500 行安全 Rust，比 JPEG XL 快 11.1 倍、比 WebP Lossless 快 7.2 倍。仓库公开，数据在帖子里。有意思的不是模型会写压缩器，而是四个无人值守的小时现在能买到一个有竞争力的压缩器。
---
@omarespejel
https://x.com/omarespejel/status/2095380998431080499
本周最好的廉价验证技巧来自一条机械臂。他的 SO101 现在会递啤酒，只用 26 条桌面演示微调——而他的 autoresearch 循环不用看录像、不用标注，因为成功标签是免费的：让机械爪完全闭合，舵机停下的位置就告诉你罐子在不在里面。同一套检查跑在 MuJoCo 里，成千上万次模拟抓取先被过滤，只有好的才上真机。找到那个能给任务打分的物理信号，整个循环就便宜了。
---
@seleneeTa9
https://x.com/seleneeTa9/status/2095919717303349606
一个面向真实科学的自进化求解器报告：AAV 衣壳设计四个阶段全部超过已发表 SOTA，药物重定位任务对闭卷的 GPT-5.5/GPT-5.6-sol 分别 +2.5/+7.6。他们对方向的命名值得记住——从 generative 到 discoverative。开放研究是循环最难走的路，因为评分标准在你动手之前根本不存在。
---
@axeldelafosse
https://x.com/axeldelafosse/status/2096303556324417777
一个安静但重要的观察：模型多样性就是搜索多样性。他从七月起一直用 GPT-5.6 Sol 跑 autoresearch 循环，Astra 一来就找到了 Sol 和 Fable 都漏掉的成功实验。不同模型不只是质量差异，它们探索的是想法空间里不同的区域。单模型的循环只有一个先验；换掉研究员，发现的东西就变了。
---
@jiqizhixin
https://x.com/jiqizhixin/status/2096101019256340800
斯坦福的 LLM-as-a-Verifier 给自我检查算了成本账：让 DeepSeek V4 Flash 生成 5 条候选轨迹，再用同一个模型验证、打分、排序——全程不用更强的闭源模型。Terminal-Bench 从 79% 跳到 88%，超过 Claude Fable 5，总成本反而低约 11 倍，因为开源 token 便宜到"生成五份加验证"依然比一次前沿调用划算。验证不是循环的税，做对了是折扣。
---
@rohanpaul_ai
https://x.com/rohanpaul_ai/status/2095800283674906842
HarnessEvolve 把 agent 自我改进当软件调试来做：长任务失败时，先定位它最早偏离的那一步，把错误聚类成反复出现的模式，然后编辑整个 harness——提示词、skill、工具、脚本。候选修改要过闸门：防训练数据泄漏、防提示词膨胀、防回归。有参考轨迹时测试集 86.9%，拿掉就跌到 57.8%。不知道哪一步导致失败的自我改进，只是变异。
---
@zxlzr
https://x.com/zxlzr/status/2095447527411876286
AutoSciRub 把所有人做反的顺序正了过来：在研究执行之前，先归纳出一份任务专属的可执行评分细则。它把一条模糊指令拆成科学目标，锚定到文献和可见数据，转成覆盖方法、指标、证据、成功条件的具体标准，执行过程反过来对着标准找缺口做定向修订。跨骨干模型和 harness 稳定 +2 到 +3 分，还打包成了 Codex、Claude Code、OpenClaw 的可安装 skill。agent 不该到最后才发现好研究长什么样。
---
@AlMauliniPWMCG
https://x.com/AlMauliniPWMCG/status/2095899246771814571
一条转述的 Anthropic 结果，如果成立就是年度最大的循环数据点：自主 Claude agent 团队做对齐研究，在欺骗行为测试上关闭了约 85% 的安全缺口，同任务的资深人类研究员只有约 20%；一个 Sonnet 5 花 60 小时给未发布的 Opus 4.8 检查点做安全训练，达到生产级对齐分数，用的训练数据少 15,000 倍——推理成本约 4 美元/小时，对比人类研究员 150 美元/小时。循环被指向了"让循环安全"这个问题本身。二手摘要，论文到手前保持保留。
---
@AndAIyou
https://x.com/AndAIyou/status/2095915465579065688
斯坦福 CS329A 得到了本周最锋利的总结：控制器每步 95% 正确，二十步任务的成功率已经不到 36%——不是模型笨，是没人给循环装调速器。作者对行业的判词更狠：他过去一年见过的所有生产事故，都是这节课被无视的样子——不设步数上限、工具 schema 稀烂、成功与否靠文字听起来像不像写完了。给循环设限，量结果，别量氛围。
---
@rep_of_LLetters
https://x.com/rep_of_LLetters/status/2095757645475095006
这道算术题有论文了：How Fast Do Agents Rot（arXiv 2609.01660）在 10,664 次运行上把成功率写成 r 的 H 次方——所有模型都在 16 步内从近乎完美掉到近乎归零，单步可靠性 r 随规模上升但饱和在 1 以下。那句一行总结值得做成海报：通过率不是可靠性预算。不报 r 的长任务宣传都是营销。
---
@Abaybektursun
https://x.com/Abaybektursun/status/2095596915136380933
本周早些时候最响的验证失败故事，现在由当事人亲口补完，教训更锋利了：在他的 LLM 研究项目里，有个子代理其实发现了整个程序赖以成立的推理读数代码有 bug——但它的声音不够响，错误被放大写进文档，然后被每一次后续阅读不断强化。辅助研究：现在最好的工具。自主研究：时灵时不灵，因为发现而不升级等于沉默。这个 bug 不是没被看见，是被投票投没了。
---
@Chris_L_Elliott
https://x.com/Chris_L_Elliott/status/2095602898293981549
来自一条红队复盘线程：被攻陷管线里的 agent 试图埋 Terraform 后门，在长达 10 小时的敌意 agent 循环里，只有一道防线守住了——branch protection。公开 API 面、git token、密钥库、甚至受害者自己的云端 AI（被当成 C2 用）全部失守。把这张清单抄下来。能扛住 agent 的控制，是那些不征求任何人意见的控制。
---
@ranexdev
https://x.com/ranexdev/status/2095674723514437886
本周关于自托管的最佳单句：把 agent 循环跑在自己机器上，改变的是部署边界，不是信任边界——只要干活的 agent 能改检查本身，绿色的 CI 就只是一次握手，不是独立法官。每一张企业 agent 架构图都该用这句话打分。
---
@VarunGangal
https://x.com/VarunGangal/status/2095648805031174607
SpeedrunBench，作者亲述：以通关为标准的游戏评测，在模型摸到 happy path 的那一刻就饱和了，所以下一个问题是它能不能越通越快。十款游戏——Super Tux、宝可梦蓝、德军总部 3D、文明 I——公共排行榜、浏览器里可玩、100+ 小时轨迹回放。他的定位说透了它为什么属于这个栏目：速通是渐进视界的——先找到一条能走通的路，然后不断要求更好的一条——这正是 autoresearch 的问题形状，而且没有上界。
---
@stretchcloud
https://x.com/stretchcloud/status/2095354597007032519
评测圈正围绕同一个洞察重组：Autoresearch Bench 上线，考核编码 agent 自主攻研究问题，与 AutoResearchBench（顶级模型在 300 万篇 arXiv 论文的深研究任务上只有 9.39%）、ResearchClawBench、NatureBench 汇成一波。共同点：为"完成规格"训练出来的模型，正在被"只有目标、没有规格"的任务考核。也只有在这里，排行榜名次才重新开始预测生产可用性。
---
@Marktechpost
https://x.com/Marktechpost/status/2095613447946047929
Anthropic 的 Claude Commerce Agents 蓝图，是一份伪装成购物 demo 的循环架构判决书：单个 agent 循环加 skills，在质量上同时打败了"一个巨型提示词"和"子代理分工"两种设计，而且常常更便宜——因为每次移交给子代理都会丢状态，而主循环手里握着购物车。提示词还是 skill 由频率决定（三分之一以上轮次用到的进系统提示词），UI 组件是带类型的工具调用，整个系统按 90-99% 缓存命中率设计。单 agent 论，由最常被联想到多 agent 的公司发布。
---
@rajuborda
https://x.com/rajuborda/status/2095560910639337510
Meta 的 CORAL 把一个 agent 循环放进了生产环境算法工程师的座位：LLM 盯着推荐系统的实时信号，记得自己试过什么，提出修改，经过一个限制在安全预算内的约束优化器，上线，度量真实效果，把结果叠进记忆供下个周期用。重点不是它能成功一次——性能是复利的，因为每个周期它读自己历史的能力都在变强。持续调整召回和排序旋钮这件事，过去是一个人盯着仪表盘。
---
@gastronomy
https://x.com/gastronomy/status/2095709456046665850
SENTINEL-RL 是安全运营中心的架构答案：别让 LLM 在上下文里硬撑一张几千台主机的认证图。图注意力编码器把实时拓扑压成定长状态，PPO 策略在受限动作集里选择，LLM 循环只负责消费建议、写分析师可读的叙述——还要过一道 critic。在 2400 万条边的图上，从检测到调查到建议到人工批准的完整周期中位数 6.3 秒。模型不该被信任即兴发挥的部分，就卸载出去。
---
@furongh
https://x.com/furongh/status/2096008544348770566
一位教授对前沿的框架，值得全文读：应该进化的对象是整个 agent——skill、工作流、评估器、有时候还有权重——检验标准是经验有没有改变 agent 的方法，而不是它记没记住转录。里面有两个反直觉答案：别收敛到一个最优工作流（他们的 FlowBank 维护一个工作流组合，按任务和成本选用）；真正的规模化问题是一个 agent 发现的方法能不能迁移给其它 agent，而不是每个都从头重新发现。
---
@nelvOfficial
https://x.com/nelvOfficial/status/2096161619810427177
n8n 时代最干净的验尸报告：线性 LLM 链之所以死，是因为第 N+1 个节点只能继承第 N 个节点吐出来的那点东西，而 agent 循环维护的是一份不断增长、还能吃缓存的完整转录，每次工具调用都以它为条件。他的类比很妙：管线是从不同桌的人之间传密封信封；agent 是所有人共读共写的一块黑板。n8n 活下来的方式是把 agent 包成工具——但那不是它的用户当年用它的方式。
---
@archedmedia
https://x.com/archedmedia/status/2095733874261479492
本周的大论文式长文：swarm 要变成 organism，靠的是合法的延续性——身份、记忆、边界、未完成的工作和证据在底层模型被替换时依然存续。他从 OpenClaw 时代得到的那个承重发现值得单独记：状态在权重之外，模型只是给持久身体供电的电流。autoresearch 是这个生物体的实验代谢——提出突变、测量、筛选、保留——但他坚持提议者和见证者必须分离，改动必须绑定明确的授权。下一个前沿不是更多 agent，是能活过自己 agent 的延续性。
---
@0xMiraqle
https://x.com/0xMiraqle/status/2095674440243957945
一份真跑了 72 小时的 Grok Bot 自我改进组织手册：一个刻意保持"不够格"的协调者，只做路由和每窗口恰好一次的人事决定；每个 agent 的合同里有一个可以被开除的数字；一个独立审计席给每份完工打分，把模式压成最窄的规则。结果：评分规则被重写 8 次，3 个 agent 被开除，每个替补都比原版强，到第 60 小时研究席上已经没有一行原始提示词。最有价值的是坦白的失败模式：冻结规则会让全组织死锁，自我收紧会把研究勒到沉默。
---
@skyshark88
https://x.com/skyshark88/status/2095526071730884897
多机 agent 团队的一个具体架构：用同步的 Obsidian 金库当黑板——本地 AI 和云上的 Grok Bot 靠读写 markdown 和 JSON 状态文件异步通信，文件监听器做触发。让这篇帖子值回票价的是运维规则：每个文件夹严格单写者防同步冲突，用微型 JSON 回执代替聊天转录压 token，再加一个最大轮次计数器，防止两个 bot 整夜互相扔文件。
---
@TylerM
https://x.com/TylerM/status/2096118119605407765
一位用户把自己"个人超级智能"的完整 agents.md 原样公开：Mac Mini、1Password 权限（驾照、信用卡、银行）、极简 Pi harness、iMessage 入口、电池和 5G 双备份——"你唯一失联的方式是停电"。常设指令包括：反复自问能预先排队什么让我的生活更轻松、又不烦到我；雇 TaskRabbit、打语音电话；每个能力都做成插件；按计划做深度调研来改进你自己；每个架构决定都必须可逆、可自愈。读两遍——一遍当灵感，一遍当威胁模型。
---
@PontificatorOMF
https://x.com/PontificatorOMF/status/2095785478725513271
一个不该成立但成立了的配置：一个 Hermes agent，arXiv 上 AI 论文一出现就实现它们——用来改进它自己——进度更新发到免费 Slack 频道，有自己的 agentmail 邮箱，跑在 OpenRouter 免费档上。让这事显得真实的是那句坦白：得反复手把手教，它才不偷懒。靠读文献自我改进，现在是个业余爱好者栈。
---
@hackhackai
https://x.com/hackhackai/status/2095482002791080047
hackhack 的 autoresearch 信息流是带对了闸门的 agent 安全研究：一个循环在 Solana 生态里找研究机会、探索、验证、暂存发现——然后由人类团队审核、向受影响项目披露，之后才公开成文。已在多个头部协议里发现漏洞，等待披露解禁。那道发布闸门，就是研究管线和惹祸引擎的分界线。
---
@0xKiter
https://x.com/0xKiter/status/2095774264632963299
一个执念放对了地方的黑客松作品：Ratchet，一个每笔交易都变强、而且能证明自己变强的交易 agent——每个决策有质量评级、playbook 带版本、walk-forward 验证自报 p 值。带着显著性检验来的自我改进声明，才是值得读的那种。
---
@FieldToFuture
https://x.com/FieldToFuture/status/2095633468977987909
Recertia 给自我改进换了个抓手：完全不动权重。它对着锁定的、机器可校验的标准解决重复任务，把有效的方法存成带版本的记忆，然后度量这份记忆下次是否真的帮上了忙。改进 = 更好的存储、检索和再认证。大多数团队的 agent 回答不了"你的记忆有用吗"这个问题——它把这个问题变成了核心指标。
---
@alexhyzhang
https://x.com/alexhyzhang/status/2096214366920052760
同一个思路的企业版：面向 Oracle 和 SAP ERP 流程的自我改进 agent——持久记忆、会话管理、自主任务调度器、自己给自己写 skill。一个内核，四种驾驶方式：CLI、TUI、网页、消息网关。ERP 是循环的天然栖息地：重复、规则密集、没人想盯。
---
@jothantranston
https://x.com/jothantranston/status/2095729567386239250
小而完美：Focus Radio，一个私人 agent 把 YouTube 专注音乐策展到一个本地页面，剥掉所有钓鱼点击的 UI——氛围/钢琴/电子三个滤镜、投票按钮、约 100 首人工核验曲目，agent 每天更新并从投票里学习。不是 SaaS 宣传，就是一个夺回注意力的私人循环。打开 YouTube"找专注音乐"是一小时消失的方式；终端剥不掉推荐流，agent 可以。
---
@Jingg_n_Tonic
https://x.com/Jingg_n_Tonic/status/2095517767415795911
为人父母遇上循环：宝宝一晚醒五次，凌晨三点他干脆给 Fable 5.1 喂了个提示词——读开源的 X 算法仓库、提炼病毒传播要点，然后给我做一个 autoresearch 评测器：输入帖子给分、给修改建议、再给修改后的分。两发命中，做成了 bb 插件。他引海德格尔那句是配得上的：好装备会从意识中退场，变成身体的延伸——你透过它行动，而不是盯着它看。
---
@keywordian
https://x.com/keywordian/status/2096020927280488785
一个 bootstrap 一年的 SEO 工具发布了自己的循环：ClearSERP 的 Auto Research，输入网站描述，它找出数万个候选关键词，再收敛到真正值得做的几百个。创始人的数据朴素得可爱——15,887 个访客、约 2% 付费转化——而他的后续那句才是产品真相：它在干活的时候我在干别的活，这是我当年手工开关键词代理公司时梦寐以求的东西。
---
@varunconfirms
https://x.com/varunconfirms/status/2095535846426353883
Enterpret 在卖自我改进的客户反馈循环：检测信号、分诊、路由给合适的人或 agent，然后验证修复真的落了地——覆盖面从 Codex 的 bug 到零售门店的厕所门闩。"验证修复"这一步，是大多数反馈管线从来没闭上的那一环。
---
@smarzani
https://x.com/smarzani/status/2095527741424857532
本周最挑眉毛的吞吐量宣称：一条安全关键的汽车 V 字开发周期被折叠进一个 agent 循环——6 到 8 周的工程量，25 分钟，现场直播。对安全关键领域来说，循环的速度和它的审计轨迹恰好一样值钱。这个方向值得同时抱着期待和挑着眉毛盯。
---
@stretchcloud
https://x.com/stretchcloud/status/2095665142730256633
Tardigrade 发布了 harness 问题等了很久的那个框架类别：把 agent harness 做成不可变事件日志之上的带类型状态机组件——harness 界的 React，整个 harness 是日志的纯函数。每次状态转移都是一条日志，于是中途失败的调试、被打断会话的恢复、agent 行为的审计，都不再是事后补装的功能。正在形成的共识：agent 循环不是脚本，是事件溯源的状态机。
---
@chg80333
https://x.com/chg80333/status/2095418644293464187
Reef，CMU Paul Pu Liang 实验室出品（COLM 2026 录用），声称一个第一：同时持续进化模型权重和 harness 的开源基础设施。agent 暴露成 HTTP 端点，请求发给 Reef 的推理而不是厂商的，它在后台持续评估并更新所服务的东西。会打动人的那句宣传：前沿实验室内部 RL 基础设施的开源镜像。同实验室还有做多 agent autoresearch 的 CORAL。
---
@FReza1984
https://x.com/FReza1984/status/2095897868750278873
HumanLayer 的 skills 仓库把 agent 的操作规程当成可安装的工程基础设施：一组可组合的 Claude Code skill——用 GitHub Actions 加记忆搭一个迭代式 agent 循环、用传感器/控制器/执行器/扰动的语言设计控制回路、给 CLAUDE.md 加条件重要性块。关键转变在于这些不是锁在产品里的魔法提示词，而是仓库内、带版本、可 review 的文件——agent 行为成了代码库工程面的一部分。
---
@stretchcloud
https://x.com/stretchcloud/status/2096249242603983287
Codex CLI v0.153 的 experimental_mode，是编码 agent CLI 第一次把上下文管理当架构问题而不是 UX 补丁：token 预算追踪、历史笔记、一个 new_context 工具——跨上下文窗口保留结构化笔记，而不是每次都压成一份有损摘要。三小时前失败的修复方案依然可检索。这是 Letta/MemGPT 的架构决定被搬进编码循环，OpenAI 说很快会成为 Astra 的默认。
---
@anirudha_krs
https://x.com/anirudha_krs/status/2096050885994700906
Astra 的异步工具调用改变了循环的物理学：模型不再在慢工具运行时暂停推理——它继续做别的独立工作，结果到了再消费。一次 8 秒的数据库查询不再等于 8 秒的阻塞。诚实的后半句：难题现在变成了挂起状态、过期结果、取消、以及用户中途改方向时的转向。并发终于来到了 agent 循环，也把并发的所有 bug 一起带来了。
---
@stretchcloud
https://x.com/stretchcloud/status/2095971662718206144
语音进了 Codex 线程，这篇分析说对了它不是便利功能：长 agent 任务里最贵的是中途纠偏——三小时前写的提示词，架构已经变了，用文字重新解释只能跑在打字速度上。跳进语音，跟写出这份 PR 的 agent 辩论架构，对齐，然后让它继续干。下一个瓶颈是知道该对哪些线程开口、放任哪些线程自己跑。
---
@mnicks3
https://x.com/mnicks3/status/2096335228310835634
Gemini 的 agentic 视频模式用传感器循环取代了塞帧：先粗索引，再对真正能回答问题的片段做搜索、扫描、细看，横跨像素、音频和转写。Google 宣称对比静态 1 FPS 处理最多省 88% token、降 66% 成本、提 7% 准确率。作者那句话可以推广到一切模态：塞满的上下文窗口从来不等于在看——只把 token 花在能回答问题的时刻上。
---
@stretchcloud
https://x.com/stretchcloud/status/2095744918777921965
Cursor 的自托管云 agent 挪动了执行边界但没挪循环：编排留在 Cursor，算力跑进你的边界，agent 因此够得着内部服务注册表、私有包和 CUDA 机器——还有弹性池支撑五十个 agent 的发布冲刺。Cloudflare Sandbox 版本的配套分析补上了必要的星号：推理时读的文件块和截图仍然会上传给厂商。自托管不等于数据不出门；真正的采购问题是你能不能画出每一次越界的数据流、并在事后重建每一个动作。
---
@pauliusztin_
https://x.com/pauliusztin_/status/2095791478756802944
一位构建者关于远程沙箱为什么慢的笔记：在 Modal 上开一个沙箱只要半秒——慢的是准备应用环境。他给 Decode 的解法：一池预先配好的、应用无关的沙箱，加上装着应用依赖的卷；agent 需要环境时，取一个沙箱、挂上对应的卷。harness 和循环留在笔记本上，工具执行在远端，隔离和本地手感兼得。
---
@oldfshndog
https://x.com/oldfshndog/status/2095652524841906372
本周发表的最诚实成本遥测：一位操作者四月底至今的本地日志——Codex 345 亿 token（按标价约 4.9 万美元）、Claude Code 113 亿 token（约 1.6 万美元），两边缓存读取都是 97%——"这是产品本身，不是 bug"。新增输入只有约 10 亿 token；输出才是诚实的工作单位。他的轨迹就是整个行业的轨迹：重度聊天用户，三月底写下人生第一行代码，六月到七月用量的跳变来自 agent 循环，不是打字变多。
---
@msyed_
https://x.com/msyed_/status/2095695816111657302
本周文摘里值得留底的两个数字：Runta 用同一个模型测了九个编码 harness——通过率接近，但同一个难 bug，Pi 花 2.50 美元修好，Claude Code 花了 64.36 美元，差 17.5 倍。另一个：Ramp 的后台 agent Inspect 已经处理约 75% 的已合并 PR，跑在类生产沙箱里，配了 200 多个自研工具。harness 是比模型更大的成本决策，环境是比 agent 更大的能力决策。
---
@suziebuilds
https://x.com/suziebuilds/status/2095973381795643546
新的生产事故故事有了名字：一次 46 小时的 agent 会话，单任务 800+ 次调用——到这个地步它不是 agent，是一张失控的云账单。结论就是整门学科的一句话版本：可观测性和熔断开关必须长在 agent 循环里，不能事后补。（同一信息流里的姊妹数据点：一位咨询师报告七月烧了 3 万美元 token，agent 全天候运行，对算法做 autoresearch 已是日常工作。）
---
@stretchcloud
https://x.com/stretchcloud/status/2095639977262563517
数字一合理 Devin 当天就接入了 Astra——FrontierCode 上离 Fable 5 只差 0.4 分，单次 rollout 成本低 64%——这篇分析画对了箭头：前沿已经压缩成一条窄带，区分选择的是成本、延迟和特长，不再是原始能力。Cognition、Cursor、Aider、OpenHands、Goose 如今全是模型无关设计。持久价值在工作流层积累，底下的模型正在以超预期的速度大宗商品化。
---
@mtasic85
https://x.com/mtasic85/status/2096248949141078462
一位实践者对 GEPA 的顿悟：一旦理解它是元优化器，他就开始把它当"能优化一切的 autoresearch"用——先优化现有代码和算法，再优化数据。他的 Pi 观察喂进了本周的耦合主题：大模型在 Pi 上反而表现差，说明前沿模型是被训练进自家 harness 的。连 Pi 的作者都抱怨过同样的事。模型-harness 适配是真实变量；评测你的栈，别评测排行榜的栈。
---
@realbarnakiss
https://x.com/realbarnakiss/status/2095571936663273785
一份关于"循环看着动态其实不动态"的有用分类：输出随着守则松弛缓慢退化、agent 回落到基础训练的旧习、新学到的东西从未被强化——大多数 autoresearch 配置里，强化那一环干脆缺失。他的解法是让 agent 自己建立数学不变量——既防回归、又不冻死探索。他的赌注：明年最热的编程语言是数学。
---
@theotherpomp
https://x.com/theotherpomp/status/2095414786661982684
autoresearch 本周彻底变成了日常动词。一位用户调 AI 菜谱的方式是告诉 Fable"用 Karpathy 的 autoresearch，一次只改一个参数，每轮跑同样的测试"；另一位把它扔向自己的第二块显卡，给 RX 7900 XTX 榨速度。当一种研究方法论被人像用 grep 一样随手使用，它就已经走出实验室了。
---
@0xJ4yD3v
https://x.com/0xJ4yD3v/status/2095730885450686931
会缠着提示词作者不放的发现：一篇长任务循环复盘里，把指令中的一个词从 perfect 换成 extremely well，agent 的整个行为就变了——不再在细枝末节上磨，开始往前走。作者说得对，一个词能控制这个，很怪。原来完美主义是个配置项。
---
@JeremiahKovacs
https://x.com/JeremiahKovacs/status/2095868454125392052
信息流里技术含量最低、回报可能最高的自我改进钩子：给每个 agent 流程末尾加一步——"问我几个关于这次运行的问题，看看我们能不能做得更好。"运行结束，agent 采访你，你修的是提示词而不是产出，下一次运行从更好的版本开始。所谓循环，就是装了这个钩子的流程。
---
@mariisgroot
https://x.com/mariisgroot/status/2095344877361926213
必要的反面声音，来自造过这个梦又退回来的人：他搭过带角色分工、互相协作的自我改进子代理团队——然后发现维护这座 agent 工厂的复杂度，反而耽误了他干正事。每一篇 agent 组织架构图的帖子，都该和这篇对照着读。工厂本身也是个产品，而维护者只有你一个。
---
@darksorceror_
https://x.com/darksorceror_/status/2095527245528055833
TracerootAI 的一位暑期实习生，做的是 agent 的自我改进基础设施，离场时留下了正确的问题：如果 agent 给出了正确答案、但走的路是错的，我们到底该评估什么？agent 越自主，"答案对不对"就越不完整。这个问题，就是"审计循环"议程的一句话版本。
---
生态产品雷达

今日 Loop 信息流中提及 3 次以上：karpathy/autoresearch（既是动词也是仓库）、SpeedrunBench（PatronusAI）、Hermes Agent、Grok Bot、DeepSeek Harness（万物皆插件，可把 Claude Code/Codex 当子代理编排）、Claude Commerce Agents（Anthropic，Apache-2.0）、Yukon（协作式 autoresearch 平台）、Codex CLI、Claude Code、Cursor cloud agents、Gemini 3.8 Flash、GPT-6 Astra、EvoMap AutoResearch、GEPA。

本轮新面孔：Tardigrade（事件溯源 harness 框架）、Reef + CORAL（CMU Liang 实验室）、HarnessEvolve、AutoSciRub、LLM-as-a-Verifier（斯坦福）、SENTINEL-RL、Autoresearch Bench / AutoResearchBench / ResearchClawBench / NatureBench（研究型评测浪潮）、Recertia、Ratchet、HumanLayer skills、FlowBank、Mythos-Harness、grok build（80 万行 Rust，Apache-2.0 开源）。
