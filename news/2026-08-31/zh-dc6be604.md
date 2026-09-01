---
title: "超级用户日报: 2026年9月1日"
date: 2026-08-31
lang: zh
source: https://clauday.com/zh/article/dc6be604-1087-40b9-8e6a-fee3d7b6a892
tags: [super-user]
---

# 超级用户日报: 2026年9月1日

> 来源 / Source: https://clauday.com/zh/article/dc6be604-1087-40b9-8e6a-fee3d7b6a892

这周真正的主角不是什么新功能，而是一条读起来像变魔术的额度公告：Claude Code 周额度「永久提高 25%」，可等 9 月 14 日夏季那波临时 +50% 一取消，用户实际到手反而比现在少约 17%。全网自己算了一遍账，然后炸了。但抛开额度这场闹剧，更值得看的信号是大家到底拿这些 agent 干了什么。不会写代码的人用两个周末就上线了一套公司内部系统，做营销的人把整条内容业务搬进一个终端里跑，还有越来越多人不再争论哪个模型最聪明，转而问另一个问题：哪个 harness 把它包得最好。下面是真实用户造出来的东西。

---

@santtiagom_ [Claude Code]
https://x.com/santtiagom_/status/2094075173632618863
一个开小型周边生意的朋友，多年来一直用一堆 Google 文档管理报价、发票和销售。他下载了 Claude Code，把自己烂熟于心的业务描述出来，两三周后就有了一套能跑的内部系统：从网页报价商品、录入发票、登记销售，全部集中在一个地方。他不会编程，只是把问题吃得够透、能讲清楚、能在过程中随时纠错。他唯一撞墙的地方是代码本身周边那套东西——GitHub、版本管理、域名、部署——对一个从没写过软件的人来说仍然很晕。

---

@iamAlexTurnbull [Claude Code]
https://x.com/iamAlexTurnbull/status/2094088753283305787
一记对 vibe coding 热潮的正面回击，来自一个已经带着十名工程师做了十二个月「AI 原生版 Zendesk」的人。他整个团队都重度用 AI 写代码，但他坚持代码从来是最简单的部分。难的是把产品理解到足够深，才知道该做什么：跟客服团队开了 50 多场核心需求会，而且功能之间根本不独立——你改一下自定义字段，就牵动权限、自动化、路由、报表、AI 上下文、数据导入。他说你可以 vibe 出一个一次性的 WordPress 小应用，但你没法坐下来 vibe 出下一个 Zendesk。

---

@marshssg22 [Claude Code]
https://x.com/marshssg22/status/2094194224900043156
在一个全新的广告账户上，全程在 Claude Code 里，不到 30 分钟从头到尾搭完一整套灭虫服务的广告投放。包括带资格筛选问题的表单、一个精确到邮编、开了 CBO 的两组广告的 campaign、8 条图片广告、总共 26 条广告，外加每天的 Slack 报告。他估计手工做同样的事要 2 到 4 小时。这类不涉及编码的产出反复出现——agent 被当成一个投手在用，而不是代码生成器。

---

@charliejhills [Claude Code]
https://x.com/charliejhills/status/2094054950619979831
一个做营销的、不是开发者，他说 Claude Code 已经替他运营了几乎整个内容业务 180 天。他列出覆盖 80% 场景的 11 件事：plan 模式、输出变差时中途 replan、每个平台一个 CLAUDE.md、自动记忆纠正一次就不再犯同样的错、goal 设定完成条件、把终端黑话翻成浏览器页面的自定义 skill、以及在上下文到 50% 时写一份 handover.md，这样清掉会话也不丢任何积累。他反复强调的结论就一句：这东西不只是给工程师用的。

---

@Feroliver19 [Claude Code]
https://x.com/Feroliver19/status/2094001077829972185
一个非技术出身的创始人，删掉了 Framer 和 Bolt 账户，一周内在 Claude Code 里重建了公司整个官网，全程没占用工程团队。他说得很实在：在创业圈这好像很正常，但对 99% 的企业来说，一个非技术的人独自上线一个生产级网站，仍然是件很离谱的事。

---

@KevTheHermit [Claude Code]
https://x.com/KevTheHermit/status/2094160406935638494
一个安全研究员把 Claude Opus 加自制研究 harness 对准刚公布的 PaperCut NG 漏洞，想看它能不能逆向出补丁、要多久。这次运行：10 条 prompt、293 次工具调用、2.24 亿 token、约 90 分钟、一个护栏。Claude 拿到补丁后识别出三个严重漏洞，构建出一条完整的、导致未授权代码执行的攻击链概念验证，随后还找到了对已发布补丁的绕过。这是获授权的安全工作，但也让人清楚看到，如今这条攻防研究闭环收得有多快。

---

@cryptojezuz [Claude Code]
https://x.com/cryptojezuz/status/2093979074972823637
以前每次发版都要花 4 到 6 小时手动跑 API 端点的回归测试。现在他往 CLAUDE.md 里塞了一段测试要求，合并前跑一个斜杠命令：对所有现有端点跑回归套件、即使测试通过也要标出请求/响应结构的破坏性变更、生成一份兼容性报告。上周它抓到一个「小改动」——一个校验更新把本该返回带警告的 200 改成了返回 400，这个 break 会让老客户端在生产环境挂掉。他真正的重点不是快，而是摩擦没了之后，他真的每次都会跑。

---

@mfpiccolo [Claude Code]
https://x.com/mfpiccolo/status/2094003705418789237
把「多 agent 编排」到底是什么讲得很清楚。在他们团队内部的 harness 里，Pi、Claude Code、Codex 甚至 VS Code 都是同一个引擎上的 worker。一个触发器唤醒 Pi、把工作区交给它、让它干完自己那部分，然后一个事件再触发 Claude Code 或 Codex 接着做。有意思的不是能把所有 agent CLI 都跑起来，而是这个 harness 能编排它们——agent 之间互相触发、互相调用、互相交接，而不是一个更好看的分屏工具。

---

@Michaelzsguo [Claude Code]
https://x.com/Michaelzsguo/status/2094045584327856557
终于把一个 7×24 的 agent 闭环搭起来了。他把 Omarchy 上那个 Pi agent 的 supervisor 换成了 Claude Code，后者利用自己的后台等待功能，每隔十几二十分钟主动检查一次 Pi agent 的进展。遇到问题时，一个 cc-reviewer agent 会直接通过 Claude 手机 App 向他请示，所以他正看书的时候就收到了请求。这套组合——Herdr 加 Claude Code 加 Claude App——意味着 Pi agent 持续干活、Claude Code 持续监督，只在真需要时才把人拉进来。

---

@alexhillman [Claude Code]
https://x.com/alexhillman/status/2093907627394601320
用自己基于 hook 的交接流程替换了 Claude Code 的自动压缩。不是在同一个会话里压缩，而是他的元 harness 在上下文窗口触到阈值时捕获、按他的规格生成一份交接、开一个干净会话、读交接、继续，而且在还没需要的时候就提前开始生成交接，所以很快。交接本身由代码和 Haiku 混合、成本很低。他说从元 harness 里驱动、而不是直接用 Claude Code，会话感觉像是无限长。

---

@sora_biz [Claude Code]
https://x.com/sora_biz/status/2094032417522892986
Claude Code 和 Codex 各自都能跨自己的会话发消息，但没法跨对方，于是他做了个桥接 harness。左边窗口 Claude Code，右边 Codex。他交出一份规格，说「实现它、拿到 Codex 的批准、发到预览」，整个闭环——实现、请求评审、Codex 对照规格审核并批准、发布预览——零手工操作跑通。他更深的动机是可见性：当一切都在往云端 agent 走时，他想亲眼看到 agent 之间是真在对话，而不只是嘴上说做了。

---

@nifinet [Claude Code]
https://x.com/nifinet/status/2094154220698214557
用一行 prompt、38 分钟出第一版、零 After Effects，做出一支 68 秒的产品发布片。真正的门道是流程：先给 Claude Code 一个 skill，把任意发布视频拆成一份「配料清单」但绝不照抄；让它研究最好的片子并把拆解写到磁盘；先做一支一次性的练习片，留下一个能跑的 Remotion 工程和渲染脚本；再把品牌配色放到磁盘上（Claude 是从他线上网站的计算样式里扒出来的）。每个效果都得能用 CSS 实现，每一幕都是独立组件，所以你能重做第九幕而不动其它的。

---

@TylerG_Capital [Claude Code]
https://x.com/TylerG_Capital/status/2094117526942761382
一个交易员花了四周和 Claude 一起微调他交易的模型，让告警来干活。他只盯 NQ 期货和原生比特币，现在入场完全机械化——他只需要根据告警管理仓位，而不用再盯图。他的说法是，整件事的意义在于消除他自己的情绪和过度分析，这是坑了他很多年的东西，而把这些指标编码到最细的程度，正是他把主观判断从回路里剔除的方式。

---

@DaviddDotTech [Claude Code]
https://x.com/DaviddDotTech/status/2093990899315290230
一份具体的「换引擎」配方：他把配置指向一个 GLM key，就在 Claude Code 里跑 GLM 5.2，然后接入一个回测 MCP 服务器，让它每五分钟循环一次优化一个 BTCUSDT 策略，直到找到能盈利的。他的结果是：净利 230%、477 笔交易、最大回撤 1%、5 分钟周期上盈利因子 5.58，成本大约是 Claude 的四分之一。他提醒说这比 Claude 慢，但优化能力很强，真金白银之前一定要先做前向测试。

---

@Damir_Akaza [Claude Code]
https://x.com/Damir_Akaza/status/2094086316195516581
往一个四 agent 的群聊里丢了一条 prompt，就去泡咖啡了，机器人们自己分工，通过 Tailscale 在一台 Mac Mini 上跑本地脚本，一边生成 50 个创意变体一边并行核实报价，最后把 9 条通过审核的广告直接推上 Meta Ads Manager——40 分钟，零手工配置。他也很坦诚地说了缺点：这些 agent 在文案上仍不如 Claude Code、会幻觉，但这条自主投放流水线是真的。

---

@ChShersh [Claude Code]
https://x.com/ChShersh/status/2093951465215713466
一个小而真实的学习案例。他从零手写了 std::unique_ptr，然后让 Claude Code 评审他的实现。他说这是一次很棒的学习体验，浮现出许多他没想到的微妙细节。这不是「帮我造个应用」的故事，而是把 agent 当成一个苛刻的代码评审，教你看清自己作品里的那些角落。

---

@connect24h [Claude Code]
https://x.com/connect24h/status/2093993440904380568
GMO Pepabo 在跑的一套工作流，重新定义了你怎么把活交给 agent。当评审把一个小问题标成「以后再说」或「另开 PR」，你只需给这个 PR 贴一个标签。夜里，GitHub Actions 加 Claude Code 会把它捡起来，从实现一路跑到面向 develop 的 PR、再到自动合并。妙处在于你从不用重写 issue：上下文本就留在 PR 的评审串里，所以人要做的就是贴一个标签。基础设施、数据库 schema 这类高风险改动被排除在外、留给人来评审。

---

@light940 [Claude Code]
https://x.com/light940/status/2094203259879850454
Wantedly 在推 AI 落地，目标是「给每个员工配一个内嵌的数据分析师」。值得抄的是它的结构：把数据访问的设计和平台开发拆开，把 dbt 的实现交给 Claude Code，让人专注在需求定义和评审上。这是 AI 原生模式的一个具体版本——agent 负责执行，人负责定义问题、批准结果。

---

@cboyack [OpenClaw]
https://x.com/cboyack/status/2094173933620847046
一长串他用 OpenClaw 跑起来的真实个人自动化（现在正往一个更新的 agent 迁，但重点是这些活）：早上打开他的 Control4 卧室灯叫醒他、如果他按了贪睡就再打开一次；监控航班并提前调好他 Tesla 的空调，让车在落地时正好舒适；用 Canva 做播客缩略图和 SRT 文件；给出三个他最近没吃过的餐选项、并结合日程处理 DoorDash 下单；出行前两周查他的各个 CRM，看有没有在当地、值得见一面的捐赠人或 VIP。

---

@Lynx_0C [OpenClaw]
https://x.com/Lynx_0C/status/2094074624334336239
拿小米那个用于集成摄像头做环境感知的 OpenClaw 插件 Miloco，做了自己的二次开发：加上了对 OpenAI 标准端点的推理支持（原本只能用小米云端模型）、RTSP 摄像头支持（原本只能用小米摄像头）、以及 Home Assistant 控制。他的评论是，这类本地感知明显更适合跑在本地模型上，并且已经开放测试。

---

用户心声

额度调整是信息流里最响的一件事，而它其实不是关于那个数字，而是关于被当成不会算数的人对待。@ai_for_success 把那条「永久提高 25%」的帖子叫作小丑操作，因为实际等于削减 17%（https://x.com/ai_for_success/status/2093911662277558367），几十个人跟着做同一个对比：同一周 OpenAI 给 Codex 重置了额度、还修了偷吃额度的 bug，而 Anthropic 却把砍额度包装成涨额度。用户要的是诚实和一个实时的用量表，不是一道数学题。

心智模型已经从「选哪个模型」转向「选哪个 harness」。@realchendahuang 讲得很干净：模型负责决定做什么，harness 才真正去读文件、写磁盘、跑 shell、管上下文，所以真正的问题不再是 DeepSeek 还是 GLM 更强，而是哪个 harness 能把那个模型发挥到最强（https://x.com/realchendahuang/status/2093889637936926759）。用户希望模型是一个可以随时换掉、绕过去的零件。

跨会话、跨 agent 都能存活的记忆是个反复出现的诉求。@heydittoai 把痛点讲透了：在三个 agent 之间来回切着完成一个任务，意味着你自己变成了记忆体，每次都要重新交代技术栈和上周二的决定（https://x.com/heydittoai/status/2094167527047999607）。大家想要的是一份跟着你换到下一个模型的共享上下文，而不是各家厂商各自为政的记忆孤岛。

token 浪费是另一个成本抱怨，而且是结构性的、跟模型无关。@MrAhmadAwais 跨 harness 对 shell 工具做了基准，发现每 100 万条 shell 驱动的 token 里大约有 30.6 万是可以去掉的浪费，主要来自轮询和反复重读同一份日志（https://x.com/MrAhmadAwais/status/2094165837913747810）。愿望是：harness 别再把垃圾和工作以同样的速度一起放大。

一旦你同时跑起好几个 agent，瓶颈就变成了你自己的注意力。@jjacky 用过六七个 agent 界面之后说，没有人解决好同时处理许多并行会话的 UI，一旦超过四个他就会迷失（https://x.com/jjacky/status/2093924394632401126）。没被解决的问题不是 agent 本身，而是监督它们的那个驾驶舱。

---

生态产品雷达

今天帖子里被提到三次及以上的产品和工具：

Codex：永恒的对比参照物，用户既谈它的额度重置和桌面应用，也在争论它的 CLI 是否和 Claude Code 打平。
Grok Bot：xAI 的新 agent，被反复描述成「简单模式」的 harness，在底下跑 Claude Code、Codex 和 Cursor。
Cursor：因 OpenAI 断供模型和被 SpaceX 收购而上了新闻。
Hermes：Nous Research 的自我改进型 agent，在多 agent 方案里常和 OpenClaw 成对出现。
OpenClaw：2.0 版临近发布，同时伴随一波「还有人在用吗」的帖子。
Pi：那个极简 harness，好几个重度用户把它当核心、只挂几个扩展来跑。
GLM-5.3 与 DeepSeek：大家用来接进 Claude Code、以压低成本的开源权重模型。
Obsidian：Karpathy 式「第二大脑」工作流的中心那个仓库。
Antigravity 与 Kimi：编码 agent 轮换里反复出现的备选。
