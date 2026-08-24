---
title: "超级用户日报: 2026年8月23日"
date: 2026-08-22
lang: zh
source: https://clauday.com/zh/article/c691aba1-30e1-43f5-9d7b-1e9e4540f0c9
tags: ["super-user"]
---

# 超级用户日报: 2026年8月23日

来源 / Source: https://clauday.com/zh/article/c691aba1-30e1-43f5-9d7b-1e9e4540f0c9

今天整个 feed 都绕回到同一件事：账单。大家已经不再争论这些 agent 好不好用了，而是在琢磨怎么让它们一直跑着又不至于烧穿钱包。这股压力催生了一整层新工具：把 Claude Code 的大脑换成 DeepSeek 或 GLM 的免费模型路由、把你桌上那台 Mac 变成推理端点的本地推理服务器，还有一波专门治"agent 每天早上都要重新学一遍你代码库"的记忆层。与此同时非编码用例越来越野也越来越好用，从逆向幼儿园餐单 API 到扫房查隐藏摄像头。而所有人都在暗暗较劲的前沿其实是同一个：你怎么敢把这么个东西扔那儿过夜跑，还真信它干的活。

---

@nikunj [Claude Code]
https://x.com/nikunj/status/2090884422178627624
他女儿刚上幼儿园，每天的餐单挂在某个乱七八糟的网站上，数据毫无结构。他让 Claude Code 去看网络请求，结果扒到一个没鉴权的 API，摸清了格式，接进了他现有的 home bot。现在每天早上 bot 会告诉全家早餐午餐吃什么，方便备餐。这就是这类 agent 的全部承诺浓缩进一件家务小事：没人会花钱雇个程序员来干这个，但现在它的边际成本掉到了五分钟的一段对话。

---

@AndreiProvkin [Claude Code]
https://x.com/AndreiProvkin/status/2090810893080686996
一整周全程用 Claude Code 做了个 WebGPU 实验项目 Boring Forest（Three.js）：花了 656 美元、22 小时实际工作、6.23 亿 token（95% 是缓存读取）、1.76 万行代码。产出是一个 15 米高的程序化石头巨人 Boss，会睡觉、你靠近就醒、追你的时候一路把树撞倒。两条值得偷的经验：checkpoint 的 markdown 文件比对话记忆强（"读一下 checkpoint 接着干"啥都不丢），提示缓存才是整个经济命脉（真正烧钱的是重启上下文）。他最狠的一条是给 agent 自己的感官——"风声听起来像不像风"变成了 agent 自己迭代的频谱读数，而不用每次都喊他来看。

---

@Parsats_eth [Claude Code]
https://x.com/Parsats_eth/status/2090747740170887565
一个数据库迁移他拖了三周，不是因为难，而是那种烦到宁可去整理桌子的活。他终于打开仓库，把要干的事描述了一遍，让 Claude Code 上：读了 schema，找出两处他早忘了、代码里还在引用旧字段的地方，写了迁移和回滚脚本，测试没动。十一分钟，看了 diff，推上去。真正打动他的不是省下的时间，而是那一堆里另外四五件同样发怵的活突然都变得能下手了——这比十一分钟本身更能改变一周的产出。

---

@aeljaouari [Claude Code]
https://x.com/aeljaouari/status/2090837489078386879
他把一个 800 多篇文章的站从 WordPress 迁到了 Claude Code 管理的纯静态 HTML 站，几个月后又搬回去了。纸面上静态加 AI 在性能、安全、灵活性上全赢。但真到每天运维：改文章里两行字要好几分钟而不是二十秒，每次改分类、sitemap、分页、跳转都把网站变成了一个软件项目。他诚实的结论是：小站上静态加 AI 非常棒，但内容站的真正强项恰恰是 CMS 默默替你处理了几百件你根本不用去想的小事。一个以"我把决定推翻了"收尾的用例，比十个成功故事都有用。

---

@jarrodwatts [Claude Code]
https://x.com/jarrodwatts/status/2090831935996043637
从本地 agent 转云 agent 的第一天，一篇很实在的心得。本地跑到五个 git worktree 就撞墙，MacBook 顶满、硬盘见底，agent 每个任务还要浪费五到十分钟处理依赖和测试。云 agent 给每个任务一台全新机器，一分钟内克隆仓库装完依赖，但代价是你得装好并授权 MCP server，再写一套按 provider、按项目定制的 setup 脚本，新机器才能碰到你的日志和工具。他花了几小时才让云端和本地打平，但确信云原生是对的方向。

---

@pakhandrin [Claude Code]
https://x.com/pakhandrin/status/2090804206907101566
他让 Claude Code（或 Codex）扫描租住公寓的 wifi 网络查隐藏摄像头。agent 会枚举网络里每台设备、试出厂默认密码，等请求分类器拦住它别暴力破解时，它就把 IP 清单、后台面板、这类设备常见的出厂设置甩回来，说"你自己试吧"。这次房间里没查到摄像头，但公共走廊里有。一个真正有创意的非编码用例，也难得让你看清 agent 在自家护栏客气地叫停之前能走多远。

---

@jpDotAi [Claude Code]
https://x.com/jpDotAi/status/2090682392881279100
一份真在实操中用 AI 的税理士、会计排行榜，细节很扎实。榜首畠山谦人：0 员工、60 家顾问客户、17 点下班，用 Claude Code 加 freee 自动化记账。其他人有的把整个事务所从手工搬到了 Claude 和 Gemini，有的搭了 freee×Claude 的 MCP 管道做自动记账核对。有一套流程是 Claude 定规则、Grok 执行、Claude 验证，全程无人介入。记账是所有中小企业共同的痛，这正是那种能横向快速扩散的非编码胜利。

---

@FinansowyUmysl [Claude Code]
https://x.com/FinansowyUmysl/status/2090757714758553630
不是编程，是普通的办公室工作。他给每个主题单独建一个工作文件夹，现在已经几十个了，每接一个新活就在终端里起一个 Claude Code。agent 不只是搜页面，还会写微脚本来验证和完成分配的任务，每个文件夹里堆满了记录结果、总结、待解决问题的 markdown。他随时能钻回任一个文件夹，从上次停下的地方接着干。一个干净的例子：终端 agent 当通用知识工作者用，而不是代码生成器。

---

@akshay_pachaar [Claude Code]
https://x.com/akshay_pachaar/status/2090732486951321914
他让 Claude Code 做一个实时天气 dashboard，要交互式 3D 地球仪、三天预报层、还有一个标记异常城市的检测器。结果给了个用 NASA 卫星图的旋转地球、昼夜循环、能拖动十天数据的时间滑块，城市天气一反常态就闪红或闪蓝。Claude Code 一个会话搞定全部，含后端和数据管道，还通过 Tiger CLI 的 MCP server 自己开了个 TimescaleDB 实例、建好了 hypertable 和连续聚合。有意思的地方在于 agent 把基础设施的管道活也接了，不只是前端。

---

@riki_murakami [Claude Code]
https://x.com/riki_murakami/status/2090781383199490314
小而美：他还刷不了键盘的 QMK 固件，于是用 Claude Code 让它被识别成一个 MIDI 设备。他原话说：还挺有点小麻烦的。这类用例永远上不了热帖，却悄悄解释了为什么 adoption 在滚雪球——agent 解掉一个一次性的硬件小烦恼，否则你得搭进一晚上翻论坛。

---

@BinaryScriptar [Claude Code]
https://x.com/BinaryScriptar/status/2090679698351391113
他做了 Traks，一套完全跑在你自己 Cloudflare 账户里的免费自托管网站分析，而且这次搭建本身就是 agent 原生的。每个 Traks 实例都自带一个 MCP server，你生成一个 token 加进 Claude Code 或 Cursor，agent 就能拉数据、查事件、给它刚交付的功能建目标和漏斗。配套的 SKILL.md 直接教 agent 怎么给你的站打埋点。底层是两个 Worker、一个 Durable Object、D1 和 R2 SQL，整套两分钟就能部署。

---

@apify [Claude Code]
https://x.com/apify/status/2090814564183023719
这条里 @eptwts 把自己的 14000 条推文喂进 Claude Code，换回了一个可浏览的成长与营销经验知识库。因为 X 要让你等最多 24 小时才给你自己的存档，Apify 就按需把推文拉了出来。一个值得抄的干净套路：拿你自己的历史当非结构化输入，agent 当那个把它变成可查询东西的图书管理员。

---

@hsantana8 [Claude Code]
https://x.com/hsantana8/status/2090834316741730562
他用 Claude Code 剪了自己第一条 YouTube 视频，连音频都做了，他形容是专业录音棚级别，全程走 MCP 和 API 服务而不是剪辑软件。剪辑一直是非剪辑人的那堵墙，而这里终端 agent 正悄悄吃掉一个大多数人以为还得靠时间轴和鼠标的创作工作流。

---

@regularwallaby [Claude Code]
https://x.com/regularwallaby/status/2090595483836199411
他用 Claude Code 给自己做了个规划视频的小生产力工具，一个 storyboard，把什么改动在什么时候发生都排出来。比在脑子里记计划或者边做边编强多了。agent 价值的日常版：不是产品，就是个别人永远看不到的个人工具，一个下午做出来，因为做它的门槛终于降到了零。

---

@sentient_agency [Claude Code]
https://x.com/sentient_agency/status/2090731771906375971
他跑了个叫 Toprank 的 Claude Code skill，干的是一整个 SEO 机构的活。在仓库里敲 /seo-analysis，它要了 Search Console 权限，一条 gcloud 命令就连上，40 秒后告诉他：首页存在两个 URL 在分散排名权重、两个页面在自相残杀抢同一个关键词、一个排在第 47 位的页面标题标签跟人们真正搜的词对不上。他敲"全部实施"，三分钟后每个修复都暂存好了。它是不是真能取代每月 3000 美元的机构可以争论，但那些具体发现是真实且落地的。

---

@mstockton [Claude Code]
https://x.com/mstockton/status/2090620620039958842
他真实的工作手法，半开玩笑分享的：Claude Code 产出东西后，他会提示"假设你是这个领域的专家，你会告诉我怎么把它做好两倍"，跑完改动，再来一句"给你的活打 1 到 10 分，不是 10 分就列出前 5 个原因并修好"。这是个谁今天都能零配置跑起来的自我批评循环，能稳定地从同一个模型里榨出更好的输出。他画的对比很锋利：人人都在聊拥抱 AI，真正肯下功夫反复练的少得多。

---

@sytaylor [OpenClaw]
https://x.com/sytaylor/status/2090603019968872901
feed 里最接地气的个人 agent 胜利：他跨六个 Gmail 账户、三家公司报季度税，98% 自动。他说这比 OpenClaw 给普通人省事 1000%，不过也承认在抽象里丢了点东西，真碰到边缘情况还是直接的电脑访问更靠谱。作为一个自闭症人士，对他最微妙的改变是能问"某人那条 WhatsApp 到底是什么意思"，他形容这是他见过第一个真正消费级的体验。

---

@cherry_mx_reds [OpenClaw]
https://x.com/cherry_mx_reds/status/2090855778697584698
一条真正有用的工程笔记：他展示了一个 OpenClaw 自动化，因为一个便宜的确定性预检说"没事可做"，所以没有跑那 168 次。这就是 168 次 agent 运行、模型调用、工具调用压根没发生。他的观点是你的 agent 循环在花 token 之前该有个便宜的确定性检查，而他很意外这么多 harness 到现在还没有。这正是把 demo 和一个你养得起、敢一直开着的运营分开的那种纪律。

---

@BenjaminBadejo [OpenClaw]
https://x.com/BenjaminBadejo/status/2090761204385948105
他展示了两个 OpenClaw agent 在同一台电脑上同时开两个独立浏览器，并且用 VoiceClaw Realtime 实时语音操控。多个 computer-use agent 并发、免手操作，具体地看到了自托管这一端要去的地方，早已越过大多数人脑中那个单会话助理。

---

@zkyo [OpenClaw]
https://x.com/zkyo/status/2090610711332622388
他全家通过一个群聊用 OpenClaw，直接读 iMessage 数据库：报任意一人的空档、往 NAS 上下载影片、查大家关心的东西。他坦白其实还蛮不好用的，因为要牺牲他一台电脑加一个 iCloud 账户。一个真实、有烟火气的家庭部署，连缺点一起，比那些打磨过的 demo 更长见识。

---

@ShrikalaKashyap [OpenClaw]
https://x.com/ShrikalaKashyap/status/2090927016258539806
每天早上她的 OpenClaw 会打印一份 mini report：需要做的事、建议、以及它自己已经处理掉的东西。她本来在看一个 Skylight 日历，但说目前这个是好得多的选择。"主动的晨间简报"正悄悄成为这些个人 agent 事实上的第一个杀手级应用，而真去处理任务、而不只是罗列的那些，才是留得住人的。

---

@RaphaelDeLio [OpenClaw]
https://x.com/RaphaelDeLio/status/2090816525657600251
作为 Forward Deployed Engineer 的第一单，他在 Kubernetes 上搭了一次性的 OpenClaw 环境，用一套基于 Redis 的 agent 文件系统把持久化用户工作区和临时算力分开。这是个人 agent 潮流里认真搞基础设施的那一端：不是 Mac mini 上一个 bot，而是随开随拆的用即弃 agent 环境，状态被刻意从机器上解耦。

---

@DBGardenhire [OpenClaw]
https://x.com/DBGardenhire/status/2090595156344930618
他的迁移故事就是 token 挤压的缩影。先被恐吓营销吓得没敢碰 OpenClaw 热潮，然后五月里连续三周周三就撞上 Claude Max 200 美元的限额。到第三周他烦到满网找替代品，撞上了 Nous，对着那个动漫吉祥物纳闷了半天，试着入了坑。现在他扎进了 Hermes 生态，庆幸自己换了。限额这堵墙正悄悄重新洗牌"谁在什么上面跑"。

---

@melodykoh [Claude Code]
https://x.com/melodykoh/status/2090630103956898017
一个自称 Claude Code 铁粉的人测 Instinct，对比笔记很犀利。相比 OpenClaw 那种搭起来累死人，Instinct 开箱即用还飞快，那种在 Claude Code 会话接进 Telegram 里要几分钟的活，它几秒就完了。最惊艳的是它对她的上下文和偏好上手极快，能根据她发帖和写作的内容挑出几条有意思的推文，"瞄得很准"。她唯一的犹豫真实且值得点出：给 agent 授权的浏览器访问意味着它能以你的身份说话，而看着它在你自己电脑上干活带来的那点安全感，可能是一场注定要输的仗。

---

用户心声

今天贯穿一切的最强信号是钱。@borjaperfra 主张一旦你有真实的生产负载，按 token 付费就不再合理，agentic 工程会把每次降价都吃掉再把账单顶回去，他见过五位数的月账单，他的解法是开源模型加固定费率推理。@DBGardenhire 连续三周周三就撞上 Claude Max 200 美元天花板然后叛逃。正是这股需求把免费模型路由和本地推理硬生生逼了出来。

上下文失忆是第二记鼓点。@alex_verem 说得干净：新工程师把你的代码库学一次，而 coding agent 每个会话都学一遍，grep 一通、建起认知，然后一关对话就全扔。这个痛催生了一整个"记忆层"品类（Graft、Ix、UltraContext、repo-seed），它们的全部工作就是终结这种反复重新入职。

啰嗦是个小而响的抱怨。@Stammy 说现在最大的障碍是人们真的看不懂 Claude Code 吐出来的行话，@goro_claudecode 则公开庆幸新的 Concise 输出风格终于砍掉了那些没人想要的"现在我要做 X、接下来做 Y"的实况解说。

过夜可靠性是所有人都在绕的前沿。@Asteri_eth 警告 24/7 agent 听着厉害，直到一次 VM 重建擦掉它们的工具、十二个 bot 变成十二个收件箱、或者一个外联 agent 按下了发送，他认为自主性不是 bot 跑多久，而是系统能不能安全地恢复、协调、停下。

而多 agent 的混乱是跑不止一个要交的税。@AgentsRoomDev 描述了如今人人都懂的乱局：六个终端 tab、三个 Claude Code 会话同时在跑、完全不知道哪个在等你——正是十几个新"控制室"工具在抢着解决的那个问题。

---

生态产品雷达

Codex — 恒定的搭档兼对手；几乎每个重度用户都和 Claude Code 一起跑、按任务在两者间切换。
Cursor — 因传闻中 600 亿美元的 SpaceX 交易强势重回话题；仍是 IDE-agent 的默认对比标杆。
OpenClaw — 人人都会引用的自托管个人 agent，如今被公开说成过了热度顶峰、维护起来磨人。
Hermes（Nous Research）— 自进化、文件记忆的个人 agent，撞上限额或被搭建之苦折磨的人正在往它这儿叛逃。
Grok Bot — xAI 阵营的新晋托管个人 agent，被夸对小白零门槛，被吐槽每月 200 美元太贵。
DeepSeek Harness（DSH）— 两天破 10 万+ GitHub 星的开源 harness，能把 Claude Code 和 Codex 当子 agent 跑。
Instinct — iMessage 原生的个人 agent（Poke 一脉），靠 onboarding 取胜，被反复叫作"给普通人的 OpenClaw"。
Claude Academy — Anthropic 的免费官方课程平台，今天被薅得最狠的 engagement bait 话题。
Ox Alpha — OpenRouter 上的匿名前沿模型（普遍疑似 GLM 血统），团队几小时内就接进了 Claude Code。
免费模型路由（Agent OS、OmniRoute、TeamoRouter）— 把 Claude Code 指向免费或廉价模型来躲限额的网关。
记忆/上下文层（Graft、Ix、UltraContext）— 新兴品类，终结 agent 每个会话重新学代码库。
本地推理（oMLX、FreeToken）— 把 Apple Silicon 和消费级 GPU 变成端点的服务器，token 永远不离开这栋楼。
