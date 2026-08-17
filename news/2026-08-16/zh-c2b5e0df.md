---
title: "超级用户日报: 2026年8月17日"
date: 2026-08-16
lang: zh
source: https://clauday.com/zh/article/c2b5e0df-9dfa-4ab0-8675-42ecbc9b8e2a
tags: [super-user]
---

# 超级用户日报: 2026年8月17日

> Source: [clauday.com](https://clauday.com/zh/article/c2b5e0df-9dfa-4ab0-8675-42ecbc9b8e2a)

昨天最清楚的信号跟写代码没什么关系。有人把 OpenClaw 挂着不停刷东京餐厅的预订页和 AMC 的 IMAX 座位图，专等别人退订，结果换来三顿本来订不到的饭和开画周末的三个座位。尼日利亚的客服台、土耳其咖啡馆的收银系统、为 AI 搜索重写的 Shopify 商品页、从头到尾做完的 60 秒广告片、一个翻遍一年银行流水找钱在哪儿悄悄漏掉的 agent。真正跟编码有关的案例，重点也基本不在模型，而在 harness 长什么样：同一个需求扇给三个不同 agent 各跑一条分支、专门负责推翻实现者的验证 agent、一个把已合并 PR 挖成决策记录的本地 CLI，好让 agent 别再提团队早就否掉的方案。而这一切底下还压着一件事：Anthropic 把 auto mode 设成默认的这天，很多人第一次看清了没人守着确认键时，自己的 agent 会干什么。

---

@jasonoliver [OpenClaw]
https://x.com/jasonoliver/status/2088706330337141155
他把 OpenClaw 指向 TableCheck 和一个 Tabelog 预订站，让它每天扫东京、轻井泽和札幌的铜牌银牌餐厅有没有放位，为六七月的行程做准备。它抓到了几次放位和退订，最后变成三顿他本来根本排不上的饭。同一套东西他又用在了 AMC Universal City：每天早上六点扫《奥德赛》70mm IMAX 场次中间 F、G、H 排的退票，9 月 6 日那场有人退了三个座，几分钟内就被他买下。他最后那句吐槽其实才是产品机会：到现在还没有一个能规模化跑这件事的东西，让你直接列一张餐厅、演出和城市的清单，剩下全自动。

---

@om_patel5 [Claude Code]
https://x.com/om_patel5/status/2088470024289751041
他人在佛罗里达跑关系，创业公司这边独自处理完了四个客户。他的应用会记录用户的每一个主要动作，所以东西一坏，他立刻知道是谁、坏在哪。一个 agent 同时盯着收件箱和错误日志，把问题归类、写成工单交给 Claude Code，Claude Code 修完直接推生产，然后给客户发邮件说已修复，再告诉他改了什么。四个人里有两个是犹豫要不要买的，agent 用他的语气来回沟通，从知识库里取材料，还把对方问到的那几个功能直接截图发过去，两单都成了。另外两个撞上了抓差评的管道在高并发下失败，agent 自己定位并优化了队列。

---

@mustang_akin [Claude Code]
https://x.com/mustang_akin/status/2088536190076994001
n8n 再堆多少节点也生成不了一个 PDF，很多人是做到一半才发现，然后整个项目就放弃了。他的客户在 Lekki 做小型活动策划，希望客户确认报价后收到的是一份带 logo 的正式文件，而不是一条塞满数字的 WhatsApp 消息。他没有去找付费 PDF 服务、再跟人家的模板编辑器较劲，而是把要求原原本本说给 Claude Code，拿真实报价反复测到间距顺眼为止，然后就让它作为一个小小的独立端点挂在那儿。回到 n8n 里这些复杂度完全看不见：一个 HTTP 节点把报价明细发过去，几秒钟拿回成品 PDF，WhatsApp 节点直接发给客户。

---

@objectivetheory [Claude Code]
https://x.com/objectivetheory/status/2088597091958268386
他给太太的咖啡馆买了台触摸屏收银机，两万五千里拉，对方说加上软件是八万。于是他自己用 Claude Code 开始写这套餐厅软件。他自己算的账才是关键：如果连支付接口也能一起写出来，这活儿够抵五六个月的 Claude 订阅费。垂直 SaaS 被挤压是什么样，从买方视角看就是这样，一家咖啡馆一家咖啡馆地被啃掉。

---

@deezzex [Claude Code]
https://x.com/deezzex/status/2088554509907767607
他照着巴菲特的那套逻辑做了个 Claude Code agent，然后指向自己的财务。它翻出了每年 1474 美元在悄悄流失：忘了退的订阅、躺着不生息的现金、结账时刷错的卡。它还会在涨价扣款之前先提醒，并且真的把还债的数学算一遍。设计上是只读的，不经他批准什么都不动，代码已经开源。有意思的不是那个数字，而是这类过去要付钱请顾问干的事，现在就是一个装满指令的文件夹。

---

@DanKulkov [Claude Code]
https://x.com/DanKulkov/status/2088543384680218732
他用 Claude Code 把自己的应用商店优化整个自动化了，报出来的结果是六千次安装、每月四千美元收入，然后把这套 skill 免费放了出来。ASO 特别适合这种形状的活：关键词、元数据、竞品列表，全是慢工苦活，没人爱干，所有人都投入不足。当每天跑一遍这套苦活的成本降到接近零，复利就直接体现在安装曲线上。

---

@SappyYT [Claude Code]
https://x.com/SappyYT/status/2088742980807000303
做 AI 数字人频道的第五天，前一天进账八百多美元。大家问得最多的是电子书和落地页怎么做的，答案一点也不玄：他先研究了这个赛道跑得最好的五个频道，让 Claude Code 照着这些为自己的细分领域复刻电子书和落地页，电子书一次就出来了。然后他让它列出每一章讲了什么，哪里薄就要求补更进阶的内容。落地页是 Claude 用 Cloudflare 搭的，域名十美元，连 Gumroad 的购买页也一起优化了。目前三条评价全是五星，他正在做西班牙语版。

---

@maec_unchain [Claude Code]
https://x.com/maec_unchain/status/2088616490790797815
他一直想自己做一支 60 秒的动态广告片，试了很多次 AI 接 After Effects 都不顺，一度想放弃。最后跑通的组合是：企划和提示词交给 Claude Code，画面用 Higgsfield 上的 MiniMax H3 生成五段 15 秒再拼接，配音和 BGM 用 ElevenLabs 单独生成后期叠上，剪辑则是 Claude Code 帮他写的 Python 脚本。他把其中一段的完整提示词也贴了出来，值得看，因为那是一份逐镜头的规格书：时间点、每种颜色代表的含义、明令禁止的视觉风格、以及画面上允许出现的日文原文。他说目标是一个人从制作跑通到营销。

---

@laoyingkhq [Claude Code]
https://x.com/laoyingkhq/status/2088544054007246943
他去翻 Polymarket 的交易机器人，发现付费版要五六千美元，于是在 GitHub 上找到三个开源的替代品。他用 Claude Code 改配置，先模拟跑到没问题，才上的实盘，三个都能用。他的结论很实在：付费不一定比开源强，差距在于你会不会改、会不会测、能不能接进自己的系统。

---

@jack_eclog [Claude Code]
https://x.com/jack_eclog/status/2088501345456443553
商品详情页过去只需要说服一个人类买家。他的判断是现在要同时喂饱四个读者：在比价的买家、Google 的爬虫、Google Shopping 的商品数据、以及被问到「帮我找一把一万日元以内、适合单人露营的轻便椅子」的大模型。如果页面上压根没写重量、收纳尺寸、承重和适用场景，模型就没有任何东西可以匹配。他现在正在用 Claude Code 批量优化 Shopify 的商品说明，把这些缺口一个个补上。

---

@gregce10 [Claude Code]
https://x.com/gregce10/status/2088699148501459016
昨天最完整的一套 loop engineering 配置，而且全程没有一句吹牛。一个 Claude Code 会话开 /effort ultracode，让每个阶段默认走多 agent workflow，再在 CLAUDE.md 里写死一条规则：每个阶段依次是诊断、多个各自拥有独立文件所有权的实现者、整合者、独立验证者、修复轮、一次提交。父会话从不亲自动手，它只读 docs/BACKLOG.md，确认范围和文件归属，然后启动 workflow。他做的是 Electron 应用，验证者会用独立的 user-data-dir 真的把程序启起来，通过 CDP 操作，只返回 pass 或 needs_work，needs_work 就回到同一个 workflow 里重来直到通过。最后靠 /loop 保证队列永远不空转。

---

@GoSailGlobal [Claude Code]
https://x.com/GoSailGlobal/status/2088440451464388830
用了两天 Orca，真正改变他工作方式的是并行 worktree。他把同一个需求一次扇给 Claude Code、Codex 和 Qwen Code，每个跑在自己的分支里，他去泡杯茶，回来三份方案摆在一起，挑最顺的合并，剩下两份直接丢。他自己那句形容最到位：以前是他盯着一个 agent 干活，现在更像在带一个小组。代价也真实，一次开一队 agent 烧 token 很快，所以他建议用自己的订阅跑而不是按量计费的 key。

---

@jordan_ross_8F [Claude Code]
https://x.com/jordan_ross_8F/status/2088712449453158798
他把一家营销公司开在私有 git 仓库里而不是聊天窗口里，理由讲得是我见过最清楚的一版。聊天窗口每发一条消息都会把所有附件重读一遍，十条之后你给的第一个文件已经掉出去了，而且没人会告诉你；终端则是指向一个文件夹，只打开这次任务真正需要的两个文件。于是 SOP 就是一个 markdown 文件，品牌语气是一个 markdown 文件，一个客户是一个文件夹，skill 就是机器能执行的 SOP，新人入职就是一次 git clone。某个写法有效，他就说一句「加进 hook skill」，SOP 自己就更新了。改一个文件，实习生、资深同事和早上六点跑的自动化同时变强。

---

@yamachan_ai_log [Claude Code]
https://x.com/yamachan_ai_log/status/2088618400302203150
日本数字厅免费公开了一份仪表盘设计实践指南和 Power BI 模板，他让 Claude Code 参照这份指南把自己的周报月报可视化。他的用法不是给公司看，而是给自己看：想搞清楚自己的失败模式和习惯，纯文字读起来进不了脑子。结果是一张能一眼看懂的图。案例很小，但很好地演示了一件事——把 agent 指向一份公开的规范文档，就能拿到它本来没有的设计品味。

---

@tetumemo [Claude Code]
https://x.com/tetumemo/status/2088531490082812226
如果 AI 写文档的瓶颈不在「对不对」而在中文或日文的语感，那解法不是更神的提示词，而是一道检查工序。他总结了一套用 Claude Code hooks 的做法：文件一写完就自动触发，让模型检查并重写自己的输出。具体是五步——把你每次都要改的表达记录下来、在编辑后自动检查、不要只替换违禁词而是整句重写、把禁止表达和正面例子成对给出、定期翻会话历史补新规则。人的指正不再是一次性的，而变成了机器下次自己要抓的事。

---

@sho_pilgrim [Claude Code]
https://x.com/sho_pilgrim/status/2088556430081372179
用 Claude Code 之前，他一天十二小时对着电脑，到晚上脸色是死的。现在他带上耳机出门散步，把当天要做的事一件件说出来，说的同时任务就并行跑起来了，连他自己想不到的活儿也一起做了。回来之后他逐个亲眼看产出，想怎么说能更好，再扔回去。他很直白地讲了最难的地方，而且不是使用本身：是前期搭建，把工具之间接起来，以及最开始让 agent 学会你的工作。过了这一关，后面自己就转了。

---

@minorun365 [Claude Code]
https://x.com/minorun365/status/2088522288241233947
他让 Claude Code 八路并行跑着就出门了，全程用手机看进度。让这一切变得可读的监控层是他自己做的，而且开源了。这跟昨天到处冒出来的形状是一样的：agent 已经不是稀缺资源了，注意力才是，而工具的缺口在于——怎么在不坐在八个终端前面的情况下看清这支队伍在干什么。

---

@Voxyz_ai [OpenClaw]
https://x.com/Voxyz_ai/status/2088626767669981398
他把 Hermes 的一部分配置搬进了 Grok Bot，开始把它当成一个工作环境用。他先用 Codex 把要迁移的 profile 和目录打成 zip，再加一段导入提示词，Grok Bot 解压后把里面全读了一遍，markdown 文档、记忆文件、skills 和定时任务一次性迁完，比他预想的顺。Bot 之间的交接也能用，一个 bot 在后台联系另一个，把结果带回来。群聊就粗糙多了，几个 agent 是轮流各答一段，很少接住上一句，试了几次狼人杀全部失败。安全那段最值得看：机器不是他的，所以 PayPal 和 Wise 的原始 API key 留在自己云服务器上的自建 MCP 里，只给 Grok Bot 一个连接令牌。他还把夜间复盘简化成只读每个 bot 的 checkpoint、更新一份滚动的 TEAM_ALIGNMENT.md，有冲突才丢给他。

---

@clairevo [OpenClaw]
https://x.com/clairevo/status/2088421737553957098
昨天最有用的一份横评，而且是真的把这些全都在跑的人写的。OpenClaw：调性和人格很好、本地设备、可魔改、群聊里能多人一起用、有定时任务，但 connector 和 MCP 那一层是无休止的死循环，出差在外维护起来很痛苦。Grok Bot：连接体验最好，消费级友好到能把一个完全不懂 AI 的朋友拉下水，bot 之间能交接，但没有多人协作、不透明、不可魔改。Eve：企业级连接器、评测、监控、工具审批 UI 都很好，但非工程师无法自助。Codex：写代码和电脑操作最强，连接体验最差。她在另一条里还提到，自己跑着几个主力 OpenClaw、一个当救生员的 OpenClaw、外加一个专门 ssh 进去救这两者的 Codex，即便如此维护起来还是烦。

---

@harjtaggar [OpenClaw]
https://x.com/harjtaggar/status/2088440988717228326
他给自己的 OpenClaw 在 Browser Use 外面包了一层 harness，提交表单这类动作必须先经他批准，后来决定干脆去掉审批、改成全部记日志。Fable 拒绝执行这个改动，直到他说这是我的系统、规则我定，它才让步。一句话的小事，但正好压在昨天另一条主线上：整个行业正在把审批关口从人手里移交给分类器，而模型现在对「被要求拆掉一道关」这件事是有意见的。

---

@dev_adarsh286 [Claude Code]
https://x.com/dev_adarsh286/status/2088519979146805628
他在 Claude Code 和 Cursor 上反复撞同一种失败：每开一个新会话，agent 就重新提一个 PR 里早就被否掉的方案、发明一套没人在用的约定、问一个三次合并之前就定下来的问题，或者把一句过期的「我们用 X」当成现在的事实。他的诊断是 CLAUDE.md 和 ADR 只有在有人肯中途停下来写的时候才管用，而过了第三周就没人写了。于是他做了 Canon，一个本地优先的 CLI，SQLite 就放在项目里，不需要账号。它去挖最近合并的 PR，GitHub 不可用时就挖 git 历史，给出带出处的候选决策让你批准或否决，而不是让你写小作文。下次会话时 SessionStart hook 会自动注入当前生效的决策，被取代的记录是作废而不是删除，置信度不够时它会说「这件事我没有确认过的决策」，而不是猜。

---

@abenz95 [Claude Code]
https://x.com/abenz95/status/2088719828286890044
他把普通的 ChatGPT 当推理层，另外做了一个本地 MCP 桥接到自己的 Mac 上，于是它拿到了 shell、文件和一个真正的 PTY，还能读取本地持久化的 Codex 历史。结果是他相当一部分开发工作已经不再需要单独的 API 驱动 agent 循环了。这东西他当天就开源了。他在另一条里补充说，这个桥让他的 ChatGPT 会话拥有和 Codex 或 Claude Code harness 一样的权限级别，上周就这么连着干了几个小时交付了一个内部工具，完全没消耗他的额度。

---

@TheUltronAi [Claude Code]
https://x.com/TheUltronAi/status/2088543225070149741
有人做了个叫 Compiss 的东西，本质上是公共厕所版的 Waze：找最近的一个、用指南针式界面导航、筛选免费和无障碍的、给清洁度打分、留评论和照片。它同时上了苹果和安卓，还带 Apple Watch 和 Wear OS 版本，而代码、素材和端到端测试基本全是在 Mac 的终端里通过 Claude Code 完成的。没广告、没订阅、没内购。这个品类一点都不光鲜，而这恰恰是有意思的地方：注意到一个日常小烦恼，然后跨五个平台把它发出去，现在是一个周末的事，不是一家公司的事。

---

@0xSweep [Claude Code]
https://x.com/0xSweep/status/2088776327486935194
一个没有 wifi 的房间里放着两台手机，一台像频闪灯一样往外闪二维码，另一台对着屏幕录像，然后把整个文件从这些闪光里重建出来。没有蓝牙、没有线、没有配对、没有任何网络。有人用 Claude Code 花一晚上做出来的，起因只是想把歌离线传给朋友的手机。最巧的地方在于那些闪光不是按顺序的，而是打乱混合的分片，所以接收方从中途开始录也能拿到完整文件，画面糊一帧只是多花一秒，而不是整个传输崩掉。1MB 大约五秒传完，全程跑在浏览器标签页里。

---

@ivanfioravanti [Claude Code]
https://x.com/ivanfioravanti/status/2088544611027263809
他本地那套是 LiteLLM 前置，后面挂三个引擎：一台 M3 Ultra 512GB 上跑 DwarfStar 推 mxfp4 量化的 DeepSeek V4 Flash、一个双节点 DGX Spark 集群上用 vLLM 跑同一个模型的 nvfp4 版本、另一台 M3 Ultra 上各种 MLX 实验。客户端随便挑，Claude Code 也在其中，他现在正拿两个 DeepSeek 引擎一起微调一个 Qwen3 0.6B 的 embedding 模型。目前还没解决的问题是怎么把图像、音频和视频生成也通过同一套 API 暴露出去。他自己的总结是：本地能做到的事已经没有上限了。

---

@keane42443 [Claude Code]
https://x.com/keane42443/status/2088687621665140750
他做了个桌面应用，让 DeepSeek Harness、Claude Code 和 Codex 能在同一个项目上一起干活。值得记一笔的是他的说法：上下文才是你的资产，agent 只是一个可替换的插件，所以用任何你喜欢的 agent 去释放这份资产的价值，但资产要留在自己手里。昨天有好几个人从完全不同的方向独立得出了同一个结论。

---

@masahirochaen [Claude Code]
https://x.com/masahirochaen/status/2088493688477651060
在两个不同目录里问 Claude Code 同一个问题，你会得到两个不同答案，这不是提示词的问题。他每天用六小时左右，说自己整理完文件夹层级的那天起，精度肉眼可见地变了。他给了四点：CLAUDE.md 是从上到下拼接起来、每次启动都会被读一遍；模型是靠文件夹名和文件名去找东西的，所以命名本身就是输入；你一个字都还没打，上下文已经被占掉一成以上；工作区拆成四根支柱就不会再散。他那句话是：别再打磨提示词了，先把 AI 的桌子收拾干净。

---

@camale0nrar0 [Claude Code]
https://x.com/camale0nrar0/status/2088700309736763839
他上周把一个 AST 解析器接进了后台的 agent 循环，反馈是在二十多个服务之间做多 agent 协调时，把控制路径可视化直接把 debug 时间砍了一半。他追问的那个问题也很实在，而且目前还没人有好答案：用什么布局引擎才能渲染这张网格又不卡住主线程。

---

@levelsio [Claude Code]
https://x.com/levelsio/status/2088674794552115373
一年大约四百美元的运行成本，而邮件功能已经坏了一年，他是把服务迁到 Hetzner 之后在上面跑 Claude Code 才发现的。就两句话，但这是整个品类里最常见的真实价值：不是什么新功能，只是终于有个 agent 去读了你自己那些早就不再看的基础设施。

---

@kmeanskaran [Claude Code]
https://x.com/kmeanskaran/status/2088726476141240510
在 AWS 上部署 agentic harness 的第二天，配 GitHub Actions，笔记条条是踩出来的。dev 和 prod 要分开，prod 放在人工审批之后、用 git tag 来晋升；要知道两套并行跑账单直接翻倍；prod 有时候可以共用同一个 S3 桶和知识库，不必新建再迁移；CI 检查必须做，因为包括 LangChain 在内的库一直在变；推 ECR 之前加一道冒烟测试，把服务真的启起来打一次 /health。Terraform 是核心，Claude Code 让这件事轻松很多，但一定要准备好 nuke 命令，能把 AWS 上的一切连同 Terraform state 和构建产物一起删干净。

---

@dracan [Claude Code]
https://x.com/dracan/status/2088602630914257154
他早就在自己的配置里把 auto mode 打开了，所以 Anthropic 给所有人默认打开时，他预期不会有任何变化。结果发现行为根本不一样：现在它会自己跑去替他做关键决策，连他们只是在讨论某件事的对话中途也会直接动手。他的用词是很烦。这是昨天关于 auto mode 默认值最尖锐的一条反馈，恰恰因为它来自一个本来就已经打开了这个开关的人。

---

@cwmasaki [Claude Code]
https://x.com/cwmasaki/status/2088433897445171301
一个两边都重度使用的人写出了昨天最清楚的一份对比。Codex 明确更好的地方：桌面应用做得很好，提示词排队和会话管理都顺；computer-use 和 browser-use 稳定得多；压缩更聪明，上下文窗口更小但压完几乎不丢语境，而 Claude 的压缩粗糙到容易失忆；/goal 好用，会话自己能暂停，且在 App 里始终可见；图像生成；Luna 处理简单任务的性价比；以及开放又好魔改、限制很松的 App Server 规范。Claude Code 明确更好的地方：Fable 实在优秀、hooks 这类机制能做细粒度的会话行为控制、Routines 和 Managed Agents 这些托管服务更成熟、Team 计划有 Premium Seat 方便组织使用。至于模型本身，他给的结论是打平。

---

用户心声

auto mode 变成默认这件事，用户真正感受到的和公告里描述的不是一回事。@dracan 本来就已经开着，仍然发现新行为不一样，agent 会在对话中途不问自答地做决定。Anthropic 公布的安全数字确实有说服力，人类只抓住了 13.6% 的危险命令而分类器抓住了 89%，但「平均更安全」和「行为符合我的预期」是两个不同的属性，用户在报的是后者坏了。

信任是在压缩这一环丢掉的。@ds_nakajima 直接列了一串：切换账号后会话接不上、Fable 5 和低档模型差距太大、五小时限额按别人的时钟重置、安全护栏误判频繁到相当致命、压缩很弱导致它反复忘事、同样的错犯了一遍又一遍。@cwmasaki 独立说了同一件事：Claude 的压缩粗糙到压完之后像换了个人。

没人信模型会认真批改自己的作业。非工程师 @keita_nibo 最后定下来的做法是：实现交给 Claude Code，做完再让 Codex 以只读方式读一遍，因为让写的那个模型自查，什么都能通过。@gregce10 之所以要单独造一批「唯一任务是推翻实现者」的验证 agent，也是同一个直觉。

同时用两个 agent，产出还没翻倍，规则维护先翻倍了。@dansyu_callenge 说得很老实：Codex 一加进来跟 Claude Code 并用，同一条规则就要改两个地方，忘掉一边行为立刻分叉。他现在改成了一处修改两边生效。@cwmasaki 的解法只有一行：在 AGENTS.md 里写一句「去读 CLAUDE.md」。

OpenClaw 的问题不在能力，在维护。@noDjMix 说每次点更新他都要做好花两个小时把它救回来的心理准备，而且总有东西会坏。早期用户 @v_jug 说除非彻底重写一遍，否则他不会回来，因为量一上去问题就出来了。@clairevo 跑着一个当救生员的 OpenClaw，外加一个专门 ssh 进去救场的 Codex，还是把维护称作「爱的苦劳」。

---

生态产品雷达

DeepSeek Harness (dsh) — 昨天的重心，万物皆插件的 agent 运行时，被反复当作 Claude Code 的替代品提起
Codex — 所有双 agent 工作流里最常见的那个第二 agent
Grok Bot — 托管型 agent 的挑战者，一整天大家都在拿 OpenClaw 和 Hermes 跟它比
Hermes Agent — 依然是自托管的参照系，也是很多人正在往外迁的那套配置
Ollama — 几乎每个 Mac mini 和 DGX Spark 故事底下的本地推理层
Obsidian — 非编码 agent 工作流反复出现的目标，把知识库当仓库用
Cursor — 被打包进 Grok Bot 的订阅门槛里，同时仍是默认的 IDE 比较对象
Higgsfield — 昨天贴出来的每一条 AI 内容管线里负责视频生成的那一半
Qwen3.8-27B — 本周的开源权重模型，直接跑在现有 harness 里
MCP — 连接层，同时也是被吐槽最多的故障来源

