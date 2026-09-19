---
title: "超级用户日报: 2026-09-19"
date: 2026-09-18
lang: zh
source: https://clauday.com/zh/article/3d04db4c-4ed8-44e5-bef3-4e5249825dc6
tags: [super-user]
---

# 超级用户日报: 2026-09-19

> 来源 / Source: https://clauday.com/zh/article/3d04db4c-4ed8-44e5-bef3-4e5249825dc6

Anthropic 把 Projects 塞进了 Claude Code，时间线上全是复述发布公告的人，真正干活的内容被埋掉了。埋在下面的，才是这一天真正的主题：成本和控制。摩根大通给工程师套上每月 2000 美元的上限并把 agent 关进沙箱；一份 benchmark 显示失败的任务烧掉的 token 是成功任务的三到五倍；一位插件作者发现自己九次会话里重复读取的上下文有 4.22 亿 token，而真正的工具输出只有 19.6 万；还有两条互相独立的发现指出 auto 模式会悄悄丢掉你写好的权限规则。而当天最好的单个案例跟写代码毫无关系：几十个小时的 Claude Code 在挪威语、阿拉伯语、日语、意大利语和法语的历史档案里翻材料，拼出一篇带脚注的调查稿。第二名是一个自主框架，一夜之间扫了十个仓库，在 Facebook、Netflix、Intel 和 Stripe 上翻出 HIGH 级别漏洞，只花掉月度额度的百分之五。而所有人似乎正在各自独立收敛到同一个形状：一个你自己掌控的常驻协调者，按任务需要拉起各种类型的短命 harness。
---
@nickgraynews [Claude Code]
https://x.com/nickgraynews/status/2100727262169448847
他得了新冠在家闲着，就给自己 newsletter 的读者免费做技术 SEO 审计，报名超过一百人，目前做完 73 份。有意思的是那条流水线：Claude Code 从报名表里把所有 URL 抓出来，跑技术 SEO 审计加域名权重检查，生成一个可视化的 HTML 结果页，再给他做一个待办看板。他挨个录 Loom，把链接贴回看板，Claude 自动扒转录稿并起草回访邮件。一份审计从头到尾十分钟。顺手还看出两件事：用 Wix 的人多得吓人；一堆 vibe coding 出来的漂亮站点域名权重是零，而一个看着像 1997 年就没再更新过的维生素代工厂网站，一年可能做几百万美元。
---
@aaronjmars [Claude Code]
https://x.com/aaronjmars/status/2100572636212265041
他在 200 美元的 Claude Code 订阅上跑一个叫 aeon 的自主框架，平时一天扫三个仓库。有天心血来潮开到十个然后就去睡了。一夜之间在 Facebook、Netflix、Intel 和 Stripe 上翻出了 HIGH 级别的漏洞，整轮只吃掉月度额度的 5%。他自己的判断才是让人不舒服的地方：现在所有人都把 GPU 拿去训模型、拿去建软件工厂，等哪天算力闲下来，有人拿一千张卡去把地球上所有软件的漏洞挖一遍。大部分会是垃圾，但总有一个不是。
---
@DrewPavlou [Claude Code]
https://x.com/DrewPavlou/status/2100524544440348985
为了写一篇关于澳大利亚电视嘉宾她父亲的调查稿，他花了几十个小时让 Claude Code 在挪威语、阿拉伯语、日语、意大利语和法语的在线历史档案里翻上万页材料，边抓边译。捞回来的东西包括 1992 年澳大利亚参议院议事录里的一段问答、国际特赦和人权观察的报告、以及学术史著作，最后全都带脚注发出来了。这就是一直被忽略的那类非编码场景：长篇调查的瓶颈从来不是写，是没法同时读五种语言的档案。
---
@imjaredz [OpenClaw]
https://x.com/imjaredz/status/2100635202561401103
他用 OpenClaw 那套 heartbeat 的思路，拿一堆 Devin automation 拼出了一个真正自我改进的系统。一个 agent 在工作日早晚两个时间窗给餐厅打电话。另一个 agent 事后读完每一份通话转录，直接改电话 agent 自己的提示词。第三个 agent 每天挑一件新东西试。有钱进账或有来电时，webhook 唤醒第五种 agent 处理。心跳大约每 20 分钟跳一次，每次都是独立会话加独立沙箱虚拟机，开头第一件事都是从 S3 把共享的「大脑」拉下来。他那句总结值得抄走：异步 agent 干活已经和人类干活彻底解耦了，系统可以自己做实验、自己看结果，中间完全不需要你。
---
@bendechrai [Claude Code]
https://x.com/bendechrai/status/2100675626424242678
一年前他把一个聊天框接到 Claude Code 上，扔给它一个 Home Assistant 的 API key，让它做个电池看板。它当场把自己重写了一遍，加了导航、加了设备列表，顺手还把那个 key 拽进了上下文里。这次事故后来长成了 Holodeck，运作方式跟他二十年前待过的广告公司一模一样：客户经理 agent 去问需求，技术负责人写规格，开发 agent 从看板上拉工单，QA 再打回来。真正值得争论的是他对「把围栏写进上下文」这套做法的反对。他不往提示词里塞几百条规则，而是在上下文之外放几道确定性的闸门，agent 根本读不到规则。一个弱模型被真闸门挡着，它发不出坏合并，最多让你多付几次重试。
---
@choblin29 [Claude Code]
https://x.com/choblin29/status/2100587791151407512
摩根大通给部分工程师的 Claude Code 用量套上了每月 2000 美元的绳子，并且把整套东西搬进一个叫 Devspace 的封闭环境。上个月工程师开始在 Teams 里问一个新报错：ExceededBudget，Budget=2000.0。六月的时候摩根的一位高管就说过，有些员工花在 token 上的钱比工资还多。现在 Devspace 把 Claude 放进一个 AWS 沙箱，专门用来隔开员工凭证和内部系统，覆盖大约 8000 个 Claude 席位。卡 token、沙箱化 agent、锁死权限、拿 ROI 出来。蜜月期一结束，企业级 AI 就长这样。
---
@DaviddDotTech [Claude Code]
https://x.com/DaviddDotTech/status/2100628809871474822
他把用 Claude Code 里的 Fable 5.1 搭一个 AI 对冲基金的七步流程完整贴了出来：装一个回测 MCP，拉一个负责给 agent 分工的仓库（调研、构建、回测、验证），再接上 TradingView 指标搜索，然后粘一段构建提示词，让它自己往看板上生成策略，值得交易的自动打星。第五步是大多数人会跳过但不该跳的：每个打星的策略拿真实行情至少前向测试 20 笔，假货就是在这一步现原形的。第七步给它配个风控提示词，任何策略回撤到 4% 就暂停。Fable 5.1 一周生成了 1297 个策略，139 个进了前向测试。
---
@codyschneider [Claude Code]
https://x.com/codyschneider/status/2100645989828669785
转化事件埋点一直是增长工程第一天最重要也最痛苦的活，因为它意味着在 Google Tag Manager 界面里点好几天，最后发现某个触发器名字打错了一个字母。他把整件事重写成了一个脚本。在应用仓库里打开 Claude Code，让它给每个关心的事件加上 dataLayer.push；开通 Tag Manager API，授权编辑和发布两个 scope；让 Claude 通过 Google Ads API 创建每个转化动作，拿回 ID 和 label；再让它写个脚本，在新 workspace 里把所有触发器、GA4 标签、Ads 转化标签和 Meta 像素一次建完并发布容器。最后你打开预览模式，自己走一遍注册流程确认都在触发。真正值钱的是这个脚本现在躺在仓库里，下一个新站点直接再跑一遍。
---
@MichLieben [Claude Code]
https://x.com/MichLieben/status/2100568914917015573
五条冷启动外呼工作流，全部跑在 Claude Code 上，通过 ColdIQ MCP 接出去，一个 CLAUDE.md 里放着 ICP 和排除规则。最值得抄的是邮箱瀑布流：一个只能找到 40% 邮箱的供应商，意味着十个人里有六个联系不上；把供应商按价格从低到高串起来，让最贵的那个只去碰别人都找不到的名字，命中率能到 80%，同一份名单的产出直接翻倍。其余四条盯的都是你已经拥有的资产：给已经画好的 TAM 排序（有一轮从 PredictLeads 拉回 25 条融资事件，其中 18 条根本不是真融资）、去捞给你自己帖子留言的人、从 CRM 里挖已经跳槽的老客户、给你花钱买来的流量装像素。他也没回避会咬人的地方：LinkedIn 明令禁止抓取、提取到的互动数据 12 小时后过期、第一天必须跑 dry-run，否则老客户会混进外呼序列。
---
@AaronxShepherd [Claude Code]
https://x.com/AaronxShepherd/status/2100661150119608552
他的团队每月给客户发几百万封冷邮件，结果就是永远没人有空手工建名单。于是他把 Apollo 接进 Claude Code，接一次。现在它会一次问一个问题，把他访谈成一个 icp.md 文件（目标公司、排除项、触发信号、地域、决策人），再把这份文件翻译成 Apollo 检索，把匹配结果拉回来，按 ICP 给每条线索打 1 到 10 分。一次示例运行返回 22 个州、25 家中型美国医院的 50 个联系人，去重完毕、大部分已补全。触达渠道按分数走：10 分的走邮件加 LinkedIn 加电话，1 分的只发邮件。最后他把整条链封装成一个单词的 Claude skill，从此再也不用写提示词。
---
@fivosaresti [Claude Code]
https://x.com/fivosaresti/status/2100585828904767902
一套给团队做出 2000 万以上曝光、18 万 LinkedIn 粉丝的内容引擎，本质是三个 skill，全都住在 Claude Code 里。Ideator 读通话转录、随手记的点子、截图或 Notion 页面，从他们 GitHub 上的「操作系统」仓库里取出客户的语气画像，再去共享的 Pinecone 库里查这个细分领域里表现好的参考帖，最后按团队已有的 Notion 格式吐出钩子和正文构思。Drafter 套上语气画像和他们的钩子/正文模板库，坚持 Notion 优先，保证发布前还有人改。Post QA 把每一句论断拿去比对论断数据库，找支撑数据，给钩子和正文打分，标出需要人工复核的地方。复利就在这一点：Ideator 每跑一次都会把新帖子写回 Pinecone。
---
@kutaro_ai [Claude Code]
https://x.com/kutaro_ai/status/2100716805782376868
他用 Claude Code 跑一套全自动的 YouTube、TikTok、Instagram 内容生产，刚刚三个平台同时达标。前一天他看完另一个创作者的复盘，当场改了内容形态，立刻拿 Claude Code 对着推演，把过往视频重做成「只有旁白、不对口型、带场面切换」的形式。新形态当天就冲出他 YouTube 的历史最高：1227 播放、11 个赞，订阅数从长期停滞的 5 涨到 9。数字很小，但这才是自动化频道故事的诚实版本——通常这种故事出现的形式是别人收益后台的截图。
---
@Jack547890 [Claude Code]
https://x.com/Jack547890/status/2100407377371783226
零编程基础，代码基本没有一行是自己写的，靠 Claude Code 当搭档一个人做出了 Threads 自动发帖工具。这篇复盘值得读的地方在于他公开的是五次事故而不是高光时刻：UnicodeEncodeError 导致所有发帖全停、GitHub 密钥粘错、rebase 冲突把他甩进 detached HEAD，每一条都附了修好的代码。他还做了大多数人不会做的那件事——实测，发现把「AI 生成」标注去掉之后播放量涨了 8 到 9.5 倍。
---
@4111y80y [Claude Code]
https://x.com/4111y80y/status/2100597398716449204
他在 Oracle 云上薅到四台免费机器，让 Claude Code 和 Codex 从头到尾把四台全架成代理，中间没有手动步骤。Oracle 有 OCI，本质上就是一套 API，所以他在 X 上搜了几篇教程直接甩给 agent，让它在四台机器上各自部好 HY2 和 SS 两种节点。内存不够的 MICRO 实例，agent 自己想办法做了加固让它不崩；IP 被标记了，他一句话让它换。更大的意义在于，免费云额度加上一个能驱动厂商自家 API 的 agent，把折腾基础设施变成了一句话的事。
---
@fotoexamen [Claude Code]
https://x.com/fotoexamen/status/2100644246214549611
他做了一个 Loom 式的录屏工具，同时录屏幕和摄像头，然后让 Claude Code 或者 Codex 把整条视频剪完，被催了很多次之后开源成 VibeTube。你录一段自己演示的东西，agent 把剩下的全包了：摄像头全屏和角落画中画来回切、自动插 b-roll、音效、字幕，横版竖版各出一版，还能直接上传。里面接了 video-use 和 Hyperframes 两个 skill。他说花时间最久的是把摄像头抠背景做得像样，而恰恰是这种细节决定了这类工具是能用还是只能演示。
---
@paonx_eth [Claude Code]
https://x.com/paonx_eth/status/2100661313374453870
他把 MaleCNS 连接组接上了 Claude Code——16.67 万个果蝇神经元，用注意力机制做键选择，跟他之前拿去玩 DOOM 是同一套装置。它做出来的东西是一个苍蝇拍探测器：接摄像头，做运动和形状检测，一旦有拍子靠得太近就报警。他自己那句话是这周最好的总结：当你让 16.67 万个神经元学会写软件，它们解决的第一个问题是自己的问题。
---
@jurlycat [Claude Code]
https://x.com/jurlycat/status/2100468376082809072
一个独立开发者用 Claude Code 加 Unreal MCP，72 小时做出了一场能玩的魂类 Boss 战。这不是一个完整游戏，是一个可运行的战斗原型，有 Boss AI、闪避机制、武器连段和动态镜头切换。重点不在生成代码。通过 MCP，Claude 能直接检视 Unreal 工程本身、操作已有的 Blueprint、在引擎里改游戏，而不是吐一堆文件出来然后祈祷。编码 agent 开始伸出编辑器，够到工作真正发生的那个工具里去了。
---
@elizondogabriel [Claude Code]
https://x.com/elizondogabriel/status/2100586350399406343
赶在联大高级别周，他用 Fable 5.1、Claude Code、Codex 和 Grok Bot 一起做了一个「谁什么时候发言」的看板。它列出高级别周每位领导人的发言时间，带搜索框可以快速查某个人或某个国家，另外有个 WIRE 模块每天多次扫 X，把所有跟 UNGA81 相关的帖子捞上来。他说这里面已经出现了一堆他在自己时间线上本来会错过的东西——这才是真正的产品：不是看板，是给一根他本来就必须硬喝的消防水管加了个过滤网。
---
@DanNeidle [Claude Code]
https://x.com/DanNeidle/status/2100646104010305695
他需要数清楚英国 CT600 企业税表连同十四张附表里一共有多少个填写框。他自己手工数了一年，得到 908 个，同时让 Claude Code 并行数一遍作为交叉校验，两边基本对上了。然后，因为再手工数五年实在受不了，他把剩下的全交给 Claude Code，自己抽查几页。这才是高风险清点工作里没人写出来的那个正确姿势：自己先跑一遍，让 agent 当第二个计数员，等两边在第一遍上对上了，再把尾巴交出去。
---
@notEgoyard [Claude Code]
https://x.com/notEgoyard/status/2100518114114879887
Claude Code 不能生成图片，而这个限制逼出来的东西比一般的绕路方案好得多。有人做了个 skill，直接把 logo 写成真正的 SVG XML，再渲染成 PNG。流程分四段：访谈（它先读你的仓库，只问那些它自己看不出来的品牌和受众问题）、发散（并行 agent 一次生成 3 到 5 个完全不同的 SVG 方案，在 HTML 预览里并排展示，可切明暗底）、打磨，最后按七种标准尺寸导出，从 favicon 到 2048 像素。因为是真 SVG，放大缩小都不掉质量，同一个文件当 16 像素图标和 2048 像素应用图都成立，而且每一版都还是能手改的代码。作者自己的说法是大概来回了 15 轮：生成、筛选、砍掉、再来。
---
@rii_no_hukugyo [Claude Code]
https://x.com/rii_no_hukugyo/status/2100404658183561422
她用 Claude 加 Remotion 一天做了 35 条短视频。两个月前她试过同样的事然后放弃了，因为跟 Claude 来回拉扯太费时间，出来的东西还是一股 AI 味。隔了这么久回来一看，它已经变成一个真正能干活的剪辑师了。最能说明趋势的是这个细节：后半段那些视频，她是一边做饭一边用手机通过 Claude Code 的远程控制下指令做完的。
---
@Huahuazo [Claude Code]
https://x.com/Huahuazo/status/2100494716139913463
整本书翻译这件事，终于有人做了个从设计之初就奔着整本书去的工具。把 translate-book 丢给 Claude Code，喂一本外文书进去，出来一整本中文版。真正关键的设计决定是并行：书被切成 N 段，同时拉起一批子 agent 一起干，这决定了这是一个「启动就走」的任务还是一个「坐着等」的任务。PDF、DOCX、EPUB 三种格式随便喂。
---
@GeekCatX [Claude Code]
https://x.com/GeekCatX/status/2100441337648787854
他拿 Hypit 做了一次 clone → edit → reuse 的实验。Hypit 是给 Codex、Claude Code 这类 agent 做视频的开源语言和系统，能把脚本、素材、配音、字幕、b-roll 和动效组织成一套可执行的工作流。他从一条唐代主题的纸片拼贴视频起步，先克隆它的视觉语法：纸张纹理、醒目题签、前后景移动、用图解讲故事。然后只改了一句指令——沿用纸片拼贴工作流，做中国瓷器史，60 秒，中文旁白——同一套视觉语言就承载了全新内容。做完他又让它给 b-roll 加流程动效，它回到已有工程里加上了随讲解依次点亮的步骤卡、连接步骤的箭头、以及跟着「绘青花 → 罩透明釉 → 入窑烧成」顺序走的框选。重点是可复用的产物是工程文件，不是那条视频。
---
@shi3z [Claude Code]
https://x.com/shi3z/status/2100538279313727883
他给跑在四张 A100 上的 DeepSeek v4.1 Flash 做了个仪表盘，仪表盘立刻暴露出一件没人去测的事：Claude Code 调四次就建四次上下文，prompt 缓存直接作废。他的结论值得每个跑 agent 的人记住——benchmark 上的最高速度和实用场景里的最高速度，是两个数字。当天晚些时候他回来说四线程并行已经跑通、prefill 缓存完美生效，还说虽然 Claude Code 的额度已经恢复，但这套本地环境好到可以就这么一直用下去。
---
@ZeBoris_ [Claude Code]
https://x.com/ZeBoris_/status/2100735706704261534
他写了个能省 30% token 的 Claude Code 插件，而他用来说服人的那个数字才是该记住的。agent 不是只为上下文付一次钱：它读过的每个文件，在之后每一轮都会被重新发一遍。他最近九次会话里，重复读取的上下文累计 4.22 亿 token，而真正的工具输出只有 19.6 万 token。占比 0.04%。他的做法是让 Jev 在上下文之外读文件，只把答案返回来。
---
@0xLagosaur [Claude Code]
https://x.com/0xLagosaur/status/2100663417451270384
Claude Code 的 auto 模式有一个几乎没人知道的上限。连续三次动作被拦，或者一次会话里累计二十次，它就悄悄退回到每件事都问你。这个数字你改不了，而你按下的下一个「同意」又会把 auto 模式直接打开。他的建议是在你批准任何东西之前，先开 /permissions 看 recently denied 那一栏——那里面是你不在的时候审查者拒掉的全部动作。
---
@0xLagosaur [Claude Code]
https://x.com/0xLagosaur/status/2100729296700481790
同一个人的第二个发现，而且更危险：如果你在 allow 列表里写了 Bash(*) 想把弹窗全干掉，auto 模式会直接无视它。auto 一开，Claude Code 就把所有允许任意代码的规则全部搁置——Bash(*)、Bash(python*)、npm run、Agent。它们还在你的设置文件里，你退出 auto 它们就回来，所以根本没人会注意到。像 Bash(npm test) 这种窄规则仍然生效，所以正确做法是把你信任的命令一条条写清楚，剩下的交给审查者。
---
@PovilasKorop [Claude Code]
https://x.com/PovilasKorop/status/2100596651152806255
他原本以为在 Claude Code 里用 Claude 模型效果最好，因为是「原生」的，Codex 配 GPT 同理——理由听上去很合理：一家公司最懂怎么用自己的模型。他自己深入测了一轮，发现是错的。他贴的截图对比了 OpenCode 里的 Deepseek-v4.1-Flash 和 Deepseek 自家的原生 harness，原生那个工具调用次数多得多，时间和 token 之所以打平，纯粹是因为反复命中了缓存。他的结论是不同 harness 只是工作方式不同，原生并不保证质量更好。留在原生里唯一真正的实际理由是成本：Claude Code 或 Codex 的订阅比通过第三方按 API 价格调用便宜太多。
---
@Av1dlive [Claude Code]
https://x.com/Av1dlive/status/2100556003817431071
他发现自己的 GPT-6 Astra 额度全烧在给每个新 agent 重复讲同一个项目上，于是做了一套 Codex 和 Claude Code 共用的记忆系统：把决策、纠正过的东西、以及确实能跑通的命令存起来，两边都能查到、都能用。你在 Codex 里改掉一条过时的命令，Claude Code 下个会话就用改好的那条。系统是用 Kimi K3 搭的，然后他做了大多数人会跳过的那个对比：简单规则 vs 训练过的记忆模型。在他的测试里，规则的效果几乎一样好。
---
@gippp69 [Claude Code]
https://x.com/gippp69/status/2100602687129530681
他找到一个 9.4 万星的仓库，能给 Claude Code 和 Codex 加上跨会话的持久记忆，安装确实只要三分钟：npx claude-mem install，选上 Claude Code 和 Codex，重启 agent。Claude Code 这边额外加一步，添加 marketplace 再装插件。它不是让你每次重新讲一遍项目，而是记录 agent 干了什么、压缩掉、把有用的部分带进下一个会话。他的判断是对的：有意思的地方不是上下文更大，而是编码 agent 终于有了一份能在会话结束后活下来的记忆。
---
@daniel_mac8 [Claude Code]
https://x.com/daniel_mac8/status/2100620339097026633
他用 Jev 加 Grok Bot 加 X API，给自己的读者挑出当天最有价值的一条 agent 技巧，方法比结果更有意思。先用 X API 拉 1000 条关于 agent 的帖子，让 Jev 在这 1000 条里做两两对比挑出最有价值的，再让 Grok Bot 把前五名捞出来。最后出来的那条是：在 Claude Code 里用 omitClaudeMd: true 把 CLAUDE.md 从子 agent 里排除掉，因为它们根本用不上，白白烧额度。
---
@EXM7777 [Claude Code]
https://x.com/EXM7777/status/2100691010997342659
他的判断是：同时跑多个 harness 是现在 agent 工作里最重要的一项技能，只用一个 harness 加它自己的子 agent 是不够的。他的实际路由是：在 Claude Code 里出方案，丢给 Codex 和 GPT-6 Astra 评审；在 Codex 里要写东西，丢给 Fable，他说 Fable 在这件事上确实比 GPT 系列强；跑量的后台活给 Deepseek，因为便宜得离谱。他也承认找出每类任务对应哪个 harness 加哪个模型，需要真刀真枪练很多次，但一旦找到，速度和质量是跨档的。
---
@Whats_AI [Claude Code]
https://x.com/Whats_AI/status/2100600923689021665
他不再直接用 Codex 了。现在是 Claude Code 负责做计划，Codex 只负责执行，通过一个由 Claude 管理的 Codex MCP 调用，跑在独立环境里，合上笔记本活还在继续。大多数人做错的是笔记和 skill 放哪：他放在 Obsidian 里，在所有工具之外，这样换工具、换设备都不用重建上下文。你不想被厂商锁死的那部分东西，就该放在那个位置。
---
@Padierfind [Claude Code]
https://x.com/Padierfind/status/2100553840244273308
他在一台远程服务器上架了个 herdr 实例，上面常驻一个 Master Codex，接到他的聊天入口。这个 Master Codex 按需拉起 Claude Code、Grok Build 或者更多 Codex 实例，通过任务看板统一管理。这是本周很多人各自独立收敛到的同一个形状：在你自己控制的机器上放一个持久的协调者，按任务需要拉起各种类型的短命 harness。
---
@kei31 [Claude Code]
https://x.com/kei31/status/2100393796618064004
他在同时做 iPhone 和 Android 两个 App，没有把它们当两个独立项目跑，而是开了两个 Claude Code 实例，让它们互相通信。两边把共享的规格对齐，更有用的是把「哪些地方两个平台确实必须不一样」明确标出来。跨 agent 交接这个需求在这个栏目里反复出现，而这位就是自己动手把线接上了。
---
@raph_guilhem [Claude Code]
https://x.com/raph_guilhem/status/2100533134877995120
现在一台摄像机就能拍出无限机位，而他是直接在 Claude Code 里用 Seedance 2.5 加一个 MCP 干的，整个过程靠非常精确的时间戳驱动。最后这个细节才是操作层面的要害：这套工作流的质量取决于你能把时间点说得多准，而不是取决于模型。
---
@miyahancom [Claude Code]
https://x.com/miyahancom/status/2100420270087680127
很小的一件事，但正是这种事会改变你对 agent 的感觉。他跟 Claude Code 说，订阅我自己来弄，你只要建一个空的 Amazon SNS topic 就行。结果它照做之余，还顺手给他配了一个 CloudWatch 告警，专门用来抓「忘了登记订阅」这种情况。他的反应大意是：你这也太会来事了，来我这儿吧，八百万我出。
---
@joncphillips [Claude Code]
https://x.com/joncphillips/status/2100623307141763167
他做网页设计二十多年了。他让 Claude Code 给自己一个小 SaaS 快速搞个落地页，结果一次就成，而且他打算基本原样用。真正有分量的细节是他跟两个月前自己的对比——那时候他说完全不觉得惊艳。一个积累了这么多审美的人在一个季度内改变判断，这个信号比榜单上任何 benchmark 都强。
---
@bendee983 [Claude Code]
https://x.com/bendee983/status/2100608036603670706
Claude Code 让他自己动手去实现一个功能，理由是这事太简单，不值得占用它的时间和精力。他一半是在开玩笑，但他接着抛出的问题不是玩笑：等手写代码的能力慢慢消失，而编码 agent 开始决定什么值得实现、什么不值得实现的时候，会发生什么。这个栏目里目前还没人给得出答案。
---
@aiumeba [Claude Code]
https://x.com/aiumeba/status/2100676166214701420
这周关于提示词结构最妙的一个比喻，来自年节重箱。日本御节料理有规矩：一之重放祝肴，二之重放烧物，三之重放煮物。不是想把喜欢的东西放哪层就放哪层，正因为层次是固定的，做菜的人才不会犹豫。她把同一套东西用到了 Claude Code 的指令上。以前她想到什么写什么，写着写着连自己都不知道哪句话写在哪儿了。现在只分三层：要它做什么、不能做什么、输出成什么形状。Claude Code 不再犹豫是一回事，她觉得更值钱的是自己开始能看出漏了什么。先定好容器，里面的东西自然就齐了。
---
@ChristianLempa [OpenClaw]
https://x.com/ChristianLempa/status/2100488926028861833
他把 OpenClaw、Hermes 和 Grokbot 并排放在一起比，比的是真实使用而不是参数表，结论落在各自的运维成本上。Grokbot 让「常在线的 agent」变得极其容易：像跟同事说话一样给它发消息，它有自己的云端电脑，合上笔记本活照跑，桌面和手机都有原生 App，不用 VPS 不用网关。代价是只能跑在人家的机器上、只在美国、不能选模型，而且你得有 SuperGrok 或者 Cursor 订阅。OpenClaw 是自托管，任意模型，从 WhatsApp、Telegram、Discord 都能找到它，技能市场很大，数据在你自己硬件上。他诚实的抱怨是：太需要看孩子了，很容易变成花在维持网关别挂掉上的时间比真正用它的时间还多。Hermes 同样自托管，有持久记忆，能从真实工作里自己写出 skill，目前他觉得它没那么脆。
---
@danielpt987 [OpenClaw]
https://x.com/danielpt987/status/2100385437399355447
一次值得记一笔的静悄悄的回流。他之前从单个 OpenClaw 转去了 language chain 的 deep agent，当时跑得挺好，现在又搬回了「单个 OpenClaw 加子 agent」。他给的理由很简单：OpenClaw 这阵子可靠多了。Hermes 他还留着但基本没用，说自己现在主要就是在搭这个 OpenClaw。在一个时间线上到处是「还有人在用 OpenClaw 吗」的星期里，一个真正在用的人悄悄搬回来，才是信息量更大的那个数据点。
---
@attenisalluneed [OpenClaw]
https://x.com/attenisalluneed/status/2100640839928295585
他做了一个转录稿 MCP，抓的是整个 YouTube 频道而不是单条视频，并且推荐给一个想让 OpenClaw 去啃 YouTube 的人。他说拿来做调研效果很好，而这句话透露了关键：对 agent 来说，有用的检索单位很少是一条视频，而是某个信源说过的全部内容。
---
@jasonlk [OpenClaw]
https://x.com/jasonlk/status/2100603922750833125
他讲的是编排，但背后有一条真实的工作流撑着。他跟自己的 agent 说：把今天那期 20VC 和 SaaStr 剪成片段，早上十点和下午一点各发一次。它去抓 YouTube、走 Opus API、读完这些片段、判断哪些是他自己的高光而不是搭档的、写好文案、再通过 X API 发出去，整个过程他一件都不用想。他明说 OpenClaw 承诺的也是这个能力，而杀死它的是复杂度：要买 Mac Mini、要自己跑模型、等等等等。达成这件事的路子有很多条，不费劲的没几条。
---
@0xCrypus [OpenClaw]
https://x.com/0xCrypus/status/2100428743332479057
一篇把 OpenClaw 内部讲清楚的解释，针对的是现在 AI 工程里最普遍的误解：以为你的 LLM 就是那个 bot。LLM 严格来说只是一个下一个 token 预测引擎，没有手、没有记忆循环、对运行时一无所知。网关守护进程跑在本地 18789 端口，把来自 Telegram、Slack、CLI 的 WebSocket 通道多路复用起来，管理会话上下文，驱动自主事件循环。推理层是热插拔的，完全不硬编码，你可以在配置文件里从本地 Ollama 集群切到托管模型，一个工具执行器都不用动。而策略闸门是那道边界：模型只负责提出 JSON 意图，网关在它落到你主机上执行之前，逐条拿运行时边界去校验。模型负责想，网关负责做。
---
@mdlahfir [Claude Code]
https://x.com/mdlahfir/status/2100399709995356266
一个 Claude Code 插件，先把你本地系统上能用的 harness 和模型全部收集起来，然后用 Jev 预测当前这个任务交给哪套 harness 加哪个模型最合适。这周好几个人各自得出了同一个结论——收益在路由上，不在任何单一 harness 上——区别只在于这个是自动化的，而不是靠人手练出来的。
---
@QingQ77 [Claude Code]
https://x.com/QingQ77/status/2100547312569184265
当一个 Claude Code 会话撞到账号用量上限时，它自动切到下一个账号，不用登出、不用交接、不用重启会话。Claude Unlimited 是一个 100% 本地运行的 Python 守护进程，跑在 127.0.0.1:4317，把多个 Claude Pro/Max 订阅、ChatGPT/Codex 订阅和 Anthropic API key 汇成一个账号池供 Claude Code 使用。不管你怎么看这件事的正当性，这东西存在本身就是「用量上限到底有多疼」的直接读数。
---
@stretchcloud [Claude Code]
https://x.com/stretchcloud/status/2100448410805715381
Composio 把六个编码 agent harness 拉到一起硬碰硬——Codex、Claude Code、OpenCode、Hermes Agent、Pi Agent、Command Code——29 个标准化任务，全部由 GPT-6 Astra 驱动。任务完成率的差距只有 7 个百分点，比大多数人预期的小。真正该据此行动的是成本信号：失败的任务烧掉的 token 是成功任务的 3 到 5 倍。你输的不是能力，你输的是没跑完的那些任务带来的失控开销。这也把编排的问题从「哪个 harness 最好」改写成了「什么时候该掐掉一次正在打转的运行」。
---
@pradeepXkapoor [Claude Code]
https://x.com/pradeepXkapoor/status/2100526464533934095
针对时间线上最响的那条抱怨，来自真实使用的一个反例：即便 Claude Code 最近下调了用量上限，他还是能干很多活，昨天跑了那么多实验都没撞到五小时的限制。他的建议是别信那些拿用量上限喷 Claude 的人，自己试试。这条值得和那些确实撞墙的人并排看，因为两边都是真的，只是负载不同。
---
用户心声

用量上限是时间线上最响的一件事，而证据真的是分裂的。@Al41611876 用的是 Max，他形容 Opus 4.6 那阵子是「怎么用都用不完」，说 Fable 5 和 5.1 很好但撑不了多久，而他拿到 Opus 5.1 和 5.2 的那两天，感觉又什么都做得成了。@pradeepXkapoor 则跑了那么多实验都没撞到五小时限制，建议别信那些拿用量喷 Claude 的人。@suesswiesauer 补了个事实：夏季那个把周额度提高 50% 的活动 9 月 13 日结束，其中 25% 被永久保留。两种体验都是真的，差别在负载形状，不在诚实与否。

对 Opus 5 的抱怨具体是啰嗦，不是笨。@Im_IrushiK 说最大的问题是 Opus 为了解释一件简单的事写两万五千行小作文，最后还要拐到一个毫不相干的地方，他认为 Claude Code 落后 Codex 是因为这个而不是 token 成本。@cheaf25master 独立说了同样的话。

原生不等于更好，只是更便宜。@PovilasKorop 原本假设一家公司最懂怎么用自己的模型，自己实测之后发现是错的，留在原生里唯一真正的实际理由是订阅价格比 API 便宜。@stretchcloud 引用的 Composio 数据从另一侧说了同一件事：六个 harness 完成率只差七个百分点，钱是被那些失控的失败任务烧掉的。

auto 模式在做一些人们没同意过的事。@0xLagosaur 同时发现了两件事：连续三次动作被拦，它就悄悄退回到每件事都问你；以及一旦打开 auto，Claude Code 会把你 allow 列表里所有开放式 Bash 规则全部搁置，而这些规则在设置文件里看起来还好好的。没人会注意到，因为你一退出 auto 它们就回来了。

「能活过会话结束的记忆」现在是呼声最高的那块缺失拼图。@Av1dlive 做了一层 Codex 和 Claude Code 共用的记忆，就因为他的 Astra 额度全烧在重复讲同一个项目上；@gippp69 装 claude-mem 是同一个理由；@kei31 更进一步，直接开两个 Claude Code 实例互相通信，用来对齐 iOS 和 Android 的规格。而 @alexgoughcooper 提供了故事的另一半：求求你们别再给我发一眼就是 Claude Code 写的 Slack 消息了。
---
生态产品雷达

Jev（TypeSafe）是今天这批数据里被提到最多的新东西，而且它出现在五种不同的活里：按轮次做模型路由、在内容进上下文之前做垃圾回收、代码审查前置筛选、在代码库里做语义寻路、以及桌面自动化。@KeyTryer 押的是：Claude Code、Codex 以及它们的各种克隆，半年内都会做出原生版本。

MCP 已经不再是一个协议话题，它是活儿真正发生的地方。腾讯的 BrowserSkill 让 agent 直接驱动你已经登录好的真实浏览器，单个标签页借了要还，遇到验证码和二次验证再把控制权交回给你。Google 开放 Home 给 Claude 和 OpenClaw 走的也是同一条路。Unreal、GeoGebra、NotebookLM、Apollo、ColdIQ、Papers with Code、以及安卓端的 Artemis，全都在同一天以 MCP 的形态出现。

持久记忆这类工具是一次性涌出来的：claude-mem、Memorable、Mnemo Cortex、Campfire、obsidian-second-brain，解决的是同一个抱怨，只是切入角度略有不同。

Hypit 这个给 agent 用的开源视频语言，今天带来了四篇独立的上手实践；Luel 这个通过 MCP 让 agent 直接买数据集的市场，带来了五篇。

harness 对比现在自成一个品类。伯克利的 HarnessTax、Composio 的六 harness 基准、DoorDash 内部的 Vera，全部落在同一个 24 小时里，而且三者的结论一致：能力在收敛，成本没有。
