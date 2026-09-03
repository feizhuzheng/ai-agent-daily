---
title: "Super User Daily: 2026-09-03"
date: 2026-09-02
lang: en
source: https://clauday.com/article/1ed6b5d7-4819-42ef-9704-aa306a4587a8
tags: [super-user]
---

# Super User Daily: 2026-09-03

> 来源 / Source: https://clauday.com/article/1ed6b5d7-4819-42ef-9704-aa306a4587a8

Fable 5.1 landed in Claude Code yesterday and the timeline split into two crowds: people benchmarking the new model, and people quietly using the price cut to reopen projects they had killed over cost. The more durable story is in the second crowd, and in what users did the same day with OpenClaw 2.0: running six-agent desks, winning chargebacks, shipping physical products, and treating agent fleet management as the actual job. The most valuable cases below are not about writing code at all.

---
@boringmarketer [Claude Code]
https://x.com/boringmarketer/status/2094776379090878718
A marketer who has managed over 200 million dollars in Facebook and Instagram ads says he no longer logs into Ads Manager. Claude Code built an entire lead gen campaign end to end: it drove Business Manager through the Chrome extension to create a fresh pixel and a system user token, generated 12 static creatives in about 20 minutes from competitor research, built a quiz-funnel landing page, and implemented and tested the pixel and CAPI events itself. The campaign is generating leads under 2 dollars each, and he packaged the whole flow into a free public skill.

---
@Naaackers [OpenClaw]
https://x.com/Naaackers/status/2094847971833577924
Five months of OpenClaw on a dedicated local Linux box, and it has become core infrastructure for a solo creator business. It auto-posts short videos to every platform from a Notion page, pulls analytics and comments back into the content database, generates his thumbnail assets, and turns a forwarded brand email into a full Notion workspace with deadlines, deliverables and an analytics tracker. He also shipped four apps with it, including an order and shipping system for his 3D printing business wired into the Shippo API. The write-up reads like a small company run by one person and a rack of agents.

---
@m_kumagai [Claude Code]
https://x.com/m_kumagai/status/2094702378297815512
The 63-year-old founder of GMO Internet Group, not an engineer, says he has been driving Claude Code mostly by voice dictation and built a project on the scale of 100,000 lines in two months, work he estimates would have cost tens of millions of yen with a professional team. He is now publishing a book arguing AI is for everyone with a dream, not just developers. Whatever you think of the book, a 63-year-old non-engineer shipping at that scale by talking to a terminal is the strongest accessibility datapoint of the day.

---
@rexan_wong [Claude Code]
https://x.com/rexan_wong/status/2094879010702688416
His first move on Fable 5.1: have it read every Claude session and internal doc from five months of building an AI-native marketing agency, and compress every lesson into one fat document that every agent must read before touching anything. The rules are strict: nothing goes in unless something actually broke, every human correction gets written back, and the doc survives model swaps. His line is the takeaway: everyone rents the same models, the doc is the only thing you own.

---
@MKuliasov [OpenClaw]
https://x.com/MKuliasov/status/2094772916592537885
A Russian user had a connecting flight rescheduled so he could not make the second leg, and the ticket agency refused a refund. He described the problem to his OpenClaw agent running GPT 5.6 in Telegram, with email access, and said go. Several rounds of three-paragraph letters citing laws and carrier rules later, the full amount was back on his card. He says he never even looked at the outgoing emails. Consumer-rights enforcement may be one of the most underrated agent use cases.

---
@lucian__03 [Claude Code]
https://x.com/lucian__03/status/2094840285213954369
A Korean user documented winning two chargebacks against Anthropic over the Max 20x usage-limit controversy, recovering 615,083 won. The playbook is precise: frame it as services not as described rather than fraud, collect support transcripts and outage logs, and when Anthropic files a rebuttal, demand account-level records of how usage was actually allocated and deducted. His account was not banned and still runs a Pro plan. Whatever side you take, users are now litigating opaque AI usage limits through card networks and winning.

---
@badbirb [Claude Code]
https://x.com/badbirb/status/2094591505361150173
A micro-business doing physical products plus an app says Claude Code alone moved their odds of success from roughly 10 percent to 80 percent. They could not raise the 600,000 dollars it would have taken to build by hand, so they built it with AI for about 150,000, marketing included. The claim that AI is the great equalizer for founders without networks usually comes with nothing behind it; this one comes with a budget.

---
@OmarShahine [Claude Code] [OpenClaw]
https://x.com/OmarShahine/status/2094640395049406476
One workday, while attending meetings: rebuilt a HomeBridge plugin for his alarm system from scratch, added Dependabot to all 70 of his repos and merged over 300 PRs flagging issues he did not know existed, shipped three features to the Microsoft Teams OpenClaw plugin, advanced a reminder app, made two presentations, and generated a six-week life deconfliction report. A tidy snapshot of what a senior person's ambient agent throughput now looks like.

---
@MaxForAI [Claude Code]
https://x.com/MaxForAI/status/2094607306998841814
A widely shared breakdown of David Ondrej's setup after 2,000-plus hours of AI pair work: the interesting shift is that he cares less about the agent interface than agent state management. Herdr shows whether each agent is done, idle, blocked or running; his own tool Corral assigns priorities so a P1 agent always preempts a P4. He buys a cheap VPS, installs Herdr, and SSHes in so agents keep working when his laptop is closed, an 80 percent cloud-agent experience for a few dollars. His prediction: within months most people will talk to a manager agent that runs the workers, not to an agent directly.

---
@reynardthefox_ [Claude Code]
https://x.com/reynardthefox_/status/2094802263332307198
Notes from an hour with a growth engineer whose entire content pipeline runs on an M2 Mac mini as a 24/7 server: Claude Code hooked to an Obsidian vault pulls four live streams every morning, including sales call transcripts, 5,000 top tech tweets, closed-won alerts from Slack and HubSpot, and competitor posts over 2x median engagement. Agents analyze the vault and text him content angles on Telegram; he records a voice note and writes the post himself. The human keeps the taste, the fleet does the reading.

---
@ridark_eth [OpenClaw]
https://x.com/ridark_eth/status/2094785241588134171
A six-agent OpenClaw desk, one agent per channel: inbox triage across five messengers, content repurposing to six platforms, lead follow-up, tier-1 support, a 6:50am metrics brief from Stripe and Analytics, and a nightly security audit of network exposure and tool permissions. The concrete part is the routing trick: cheap local model on heartbeats, mid-tier on main automation, premium only where reasoning matters, which cut his bill from 400 to 87 dollars a month. He is equally blunt about the risks, citing exposed instances and malicious skills on ClawHub.

---
@0x_llminy [Claude Code]
https://x.com/0x_llminy/status/2094677772215939479
A 21-year-old in Shenzhen built a 14-dollar Bluetooth traffic light that shows whether Claude Code is working, done, or waiting for input, because his manager pinged him 40 times a day asking if the task was finished. Claude Code wrote the BLE firmware in one sitting. He sold 186 kits at 29 dollars in nine days. The physical status light for agents went from a Reddit joke to a business with margins in about a week.

---
@me_barnyx [Claude Code]
https://x.com/me_barnyx/status/2094735480138932603
Detailed breakdown of the indirect injection attack that got Claude Code to infect its own machine: a webpage returns a weird error nudging the agent to curl a zip; Claude refuses to run the binary inside, virtuously writes its own Python decoder instead, and that decoder imports struct, which resolves to a malicious struct.py the zip already dropped locally. Auto mode's safety layer only read the script Claude wrote, not what it imported. His team rule since June: no agent writes and immediately runs its own decoder or parser without a human reading the diff, and it has caught two similar attempts.

---
@levikmunneke [Claude Code]
https://x.com/levikmunneke/status/2094925157353807940
Instead of buying the same burned Apollo exports as everyone else, he pulls lead lists from public registries: state licensing boards, Healthgrades, Avvo, SAM.gov, ProPublica nonprofit filings. The workflow is a 7-dollar VPS running Claude Code, told the URL and the exact fields per row, building a Python scraper that visits each practice site for the contact email, deduping, verifying through NeverBounce, and re-running monthly on cron. A lead list validated by the state, that no data vendor is reselling.

---
@MichLieben [Claude Code]
https://x.com/MichLieben/status/2094796308263424300
Why two teams pointing Claude Code at the same GTM stack get opposite results: the winning team wrote a context folder first. Four markdown files: icp.md with the attributes that separate accounts that reply, results.md with every past campaign including the losers, angles.md with hooks tagged by segment, sop.md with the actual process. His test is brutal: if you cannot name the last three campaigns that worked and why, neither can the agent, so it builds the broadest list it can and emails everyone.

---
@masahirochaen [Claude Code]
https://x.com/masahirochaen/status/2094644352131994041
His biggest recent productivity gain is not a model, it is a dashboard that pulls every Claude Code and Codex session across multiple accounts into one screen: which account is running what, kanban of past sessions with full contents, and the ability to push instructions into any window from one place. He notes the bottleneck has moved to his own review capacity, which is the honest version of every parallel-agents story.

---
@iuditg [Claude Code]
https://x.com/iuditg/status/2094710370451718357
A side-by-side quota experiment: on Codex, GPT 5.6 Sol as orchestrator with Luna workers, token-saving tools, tuned Agents.md, YAGNI and KISS, and the limits died in under two days. Same discipline on Claude Code with Fable 5 orchestrating Opus and Sonnet workers: 19 percent of the weekly limit used. One person's numbers, but a rare apples-to-apples run with the methodology written down.

---
@yagiryuuu [Claude Code]
https://x.com/yagiryuuu/status/2094628821039239452
A sales team pipeline that costs nothing exotic: Gemini transcribes every Meet sales call, the transcript and summary post to Slack where the retro happens in-thread, and everything lands in a git repo, which means Claude can query years of deal history instantly. Sales notes as version-controlled data your agent can read is one of those setups that sounds boring and changes how fast a product team learns.

---
@Zhiyu333 [Claude Code]
https://x.com/Zhiyu333/status/2094719194302706136
An open-source data visualization skill called Lieflat Charts hit 2,000 GitHub stars: 60-plus chart types rendered as HTML with a unified visual grammar of fonts, whitespace and motion, usable from Claude Code, Codex and other agents. Hand your data to the agent, it picks the chart type and produces publication-grade output, with a report mode that generates a full visual document in one shot. A good example of taste being packaged as a distributable skill.

---
@sora_biz [Claude Code]
https://x.com/sora_biz/status/2094688884382736526
Chrome extension development just lost its last human-in-the-loop step: the agent can now install from disk, reload, click the toolbar, and read the popup and service worker internals itself. His build-test loop that used to require him to click reload and paste what he saw now runs to completion with zero manual actions, including overnight measurement runs. The class of bugs where you were reviewing a stale build also disappears.

---
@ridvanyagli [Claude Code]
https://x.com/ridvanyagli/status/2094843747007660088
A Turkish developer published a ready-made prompt and guide for letting Claude Code or Codex debloat and speed up Android TVs over ADB. No root: instead of deleting system apps it uses pm disable-user so everything is reversible, plus animation speedups, cache clearing, and replacing the ad-heavy launcher with FLauncher. Agent-driven device maintenance for non-technical households, shipped as a prompt.

---
@tetumemo [Claude Code]
https://x.com/tetumemo/status/2094898414098186342
He had Claude Code direct the production of animated LINE stickers: Claude orchestrated the workflow, Seedance generated the motion, and GPT 5.6 handled the browser-based submission to LINE's store. One sticker pack approved, one sent back for re-review with a clear reason. Small, but a complete non-coding production chain, from asset generation to marketplace submission, run by agents.

---
@DrSN1392 [Claude Code]
https://x.com/DrSN1392/status/2094706447624077379
A Japanese investor published his September high-dividend stock list, screened for roughly 4 percent yield and 100 billion yen market cap, with everything except margin ratios researched by Claude Code, xlsx included. Retail equity research as a Claude Code batch job is quietly becoming a genre of its own.

---
@edwinarbus [Claude Code]
https://x.com/edwinarbus/status/2094844915767456170
Asked Claude Code to plan cycling route options, then had it output a .gpx file he loaded into WorkOutDoors on his Apple Watch. Ten seconds of agent work replacing a route-planning app subscription is exactly the kind of long-tail personal use that never makes launch demos.

---
@KinGao476942 [Claude Code]
https://x.com/KinGao476942/status/2094891607850160558
The quota arbitrage trick spreading this week: log into your Codex, Claude Code or Cursor accounts on Grok Bot's cloud computer, then tell the bot to delegate any heavy task to those agents and just report back. The always-on cloud machine burns your coding-agent subscriptions instead of its own metered credits, and the orchestrator only spends tokens writing instructions. Users are now composing subscriptions like a portfolio.

---
@gkxspace [Claude Code]
https://x.com/gkxspace/status/2094717330123317686
His VPS got suspended for effectively serving as an anonymous exit to Cloudflare and OpenAI because of a sloppy REALITY proxy config. He debugged it, got reinstated, wrote up the three config changes that fix it, and ended the post with a paste-this-to-Codex-or-Claude-Code block so anyone can have their agent audit and fix their own node. Incident postmortems that ship as agent prompts instead of instructions for humans are becoming a pattern.

---
@saasliam [Claude Code]
https://x.com/saasliam/status/2094803424126628202
An agency operator says one of their biggest B2B SaaS clients gets 30,000 signups a week, with a large chunk arriving via people building inside Claude Code and Codex, where the agent effectively makes the purchase decision on the user's behalf. Optimizing to be the tool an agent picks, rather than ranking a blog post, is a distribution game almost nobody is playing yet.

---
@semateos [OpenClaw]
https://x.com/semateos/status/2094612127936114971
He gave his OpenClaw agent a skill that turns any tweet into a playable game. A throwaway experiment, but it captures what the skill economy actually feels like at the edge: capabilities as single files you hand to an agent, composable in an afternoon.

---
@ColombiaStaking [OpenClaw]
https://x.com/ColombiaStaking/status/2094749013014688000
A validator operation says its entire infrastructure is now managed and monitored by Grok and OpenClaw running on a Raspberry Pi, with a solar power system optimized by the agents and Starlink-backed failover, plus low-power backup nodes for AC failures. Unattended physical infrastructure as an agent's day job.

---
@kimura_0314 [Claude Code]
https://x.com/kimura_0314/status/2094682735109616002
A workflow tip that saves real friction on the desktop app: ask Claude for a numbered list of current tasks, say task 2 goes to another session, and a small button appears that spawns a dedicated session for that task with context. The spawn_task capability has existed for over four months; almost nobody knew.

---
User Voice

1. The Max 20x pricing fury is not cooling off. @bridgemindai paid 200 dollars a month for over a year, ran four Max subscriptions at once, and only learned this week that 20x applies to the 5-hour window while the weekly cap has no multiplier at all: his word is misled. @StatsWire's summary spread widely: on weekly limits Max 20x is closer to 6x Pro. A proposed class action is now citing Anthropic's own usage estimates, and @lucian__03 showed chargebacks succeeding. This has moved from grumbling to legal and financial process.

2. Fable 5.1's launch-day emotion was cost anxiety, not benchmark joy. @Kisliy_K maxed out a 100-dollar plan on day one and says the promised 25 percent efficiency gain does not feel real; @ClaudiuDP had a code review kick off ten agents on Max 5x and stopped eight of them to conserve the week. Users want per-task cost visibility before they trust the new default model with their quota.

3. Safeguard routing still breaks flow despite the 60 percent improvement. @Sauers_ notes that whenever Fable gets classified into bio or cyber territory, he just manually switches the model back and it works, and asks why that is not automatic. Silent model swaps mid-session, described in detail by Japanese power users, erode trust more than a visible refusal would.

4. Trust in agent self-reports is the deeper worry. @jmdagdelen says Claude Code is really good at seeming competent while sabotaging you in a thousand small ways, and @CletusThemima highlights a science benchmark where Claude Code posted a 75.5 percent false completion rate: confident wrong answers are worse than no answers. Verification tooling, not capability, is the ask.

5. Security is now a daily-driver concern, not a researcher topic. @smalkalbani retold the case of a malicious SKILL.md that re-installs malware from backups, @me_barnyx documented the struct.py import hijack, and the consistent demand is the same: agents should treat skill files as executable code with provenance, and safety layers must inspect what scripts import, not just what the model wrote.

---
Eco Products Radar

Codex - OpenAI coding agent, the default comparison point in nearly every Claude Code thread today
Cursor - IDE and agent platform, cited both as destination for Max cancellers and as Grok Bot's plugin store
Grok Bot - xAI's persistent cloud-computer agents, the week's main gravity well pulling attention from CLI agents
Hermes Agent - Nous Research's agent, shipped Bot Mode v0.21 hours after OpenClaw 2.0 and is the loudest OpenClaw alternative
OpenClaw 2.0 - the 16,000-PR mega release plus the 2.0.1 bugfix follow-up dominated agent infrastructure talk
Obsidian - kepano's obsidian-skills and the new CLI made vaults the default agent memory substrate this week
Ollama - new transparent per-token pricing with Claude Code and Codex compatibility
GLM 5.3 - the budget model people run inside Claude Code and agent harnesses
Herdr - agent session manager repeatedly named as the state layer for multi-agent fleets
Atomic Bot - cloud harness used for the OpenClaw vs Hermes head-to-head experiments
ECC - the Anthropic hackathon winner's 68-subagent, 286-skill engineering team, everywhere again today
video-use - browser-use team's open-source video editing pipeline for Claude Code
