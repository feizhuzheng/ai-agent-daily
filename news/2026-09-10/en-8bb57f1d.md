---
title: "Super User Daily: 2026-09-11"
date: 2026-09-10
lang: en
source: https://clauday.com/article/8bb57f1d-c5c1-4654-a92e-65a343fab622
tags: [super-user]
---

# Super User Daily: 2026-09-11

> 来源 / Source: https://clauday.com/article/8bb57f1d-c5c1-4654-a92e-65a343fab622

Today's clearest signal is that the interesting work has moved off the keyboard entirely. A father put o3 in a harness he wrote himself and got the rare-disease diagnosis a top neonatal lab missed. A security researcher swapped ten to twenty bugs a month for 195 in three weeks. A one-person HR function automated eighty percent of its recruitment writing and then pointed the same agent at interviewer bias. A 54-year-old woman with no technical background shipped a playable game in an hour.

Underneath that, two arguments are getting sharper. The first is that harness beats model: one study of nearly seventeen thousand real agent tasks found Claude Code, Codex and Cursor agree on which tool to use only 42 percent of the time, and a new benchmark asking agents to build a deployable agent end to end put the best system at 23.9 percent against an 82.2 percent human ceiling. The second is that cost literacy is now a core skill, and most of the received wisdom is wrong: forced double-checks and maxed-out effort settings frequently make agents both more expensive and worse, while a single timestamp in a system prompt can quietly destroy your cache hit rate.

And the personal-agent field split in two this week. Power users who spent nine months customizing OpenClaw say nothing out of the box comes close. People who never got OpenClaw running say it never felt secure and was too complex. Both are describing the same product accurately.
---
@Michael_J_Black [Claude Code]
https://x.com/Michael_J_Black/status/2097585486466327003
A veteran computer-vision professor heading to ECCV 2026 admitted the uncomfortable part out loud: his accepted paper VIGA, which turns a photo into a 3D Blender scene using an agentic approach, was overtaken by people simply doing the same thing with Claude Code, and then blown away entirely by GPT-6 Astra. He points out that any paper you see at a conference is roughly two years out of date because it was built on literature that was already a year old. His proposal is concrete: every paper should open with a section analogous to Related Work that tests current frontier models on the task and documents exactly how and why they fail. If you have not tried solving your problem with the current models, you have not done your homework.
---
@MTSlive [Claude Code]
https://x.com/MTSlive/status/2097814042673029496
The single most important use case of the day has nothing to do with shipping software. Gamow Labs founder Daniel McKinnon lost his first son to a rare genetic disease that a top neonatal whole-genome lab reported as negative. After a second loss for genetic reasons, he requested all the raw lab data under his HIPAA rights, wrote what he calls an agentic loop before Codex or Claude Code existed, and put o3 inside a harness with one instruction: figure this out. It diagnosed his son Owen, the case the best lab in the field had missed. He now runs a company built on that discovery.
---
@Sisinerd [Claude Code]
https://x.com/Sisinerd/status/2097667363738976415
Ezinne Kalu quit medical school, could not land a security job, and started finding vulnerabilities in other people's software to prove she was worth hiring. Her stack is now Claude Code as the harness, a second brain built on Andrej Karpathy's pattern, everything stored in GitHub and managed in Obsidian. She used to submit ten to twenty bugs in a good month. The system found 195 in three weeks, more than her entire manual bug bounty career, including CVE-2026-79653, a path traversal in Eclipse SW360 that had been sitting in code running inside 30,000 organizations for at least six released versions. The catch is telling: most of the findings were in software with no bounty program, so she was paid for none of them, and her system now produces more findings than she can personally disclose.
---
@MatiasScalbi [Claude Code]
https://x.com/MatiasScalbi/status/2097807325251666027
Built a public-filings insider trading monitor from scratch with an AI agent and published the whole recipe. Five parts: SEC EDGAR for Form 4 filings, official Congressional disclosures, a database, filters by ticker, person, date, amount and type, and a simple web interface. He deliberately isolates purchases where an insider actually put capital in, rather than mixing in grants and option exercises that make the signal unreadable. His build advice is to start with SEC plus insider purchases only, get that working, then add Congress, alerts and favorites. He is explicit that it is a research filter, not a copy-trading tool, and that Congressional reports can lag 45 days and publish amounts as ranges.
---
@LmyQs2 [Claude Code]
https://x.com/LmyQs2/status/2097535621804011946
Started a system migration with Claude Code and it kept going until it was doing his entire affiliate business operations review. It pulled two months of conversion CSVs from every affiliate network, merged files with different formats into one, sorted issued, approved, rejected and pending, and calculated approval rates per campaign. Then it read Gmail, extracted rejection notices from hundreds of emails, and traced back through past negotiations with network reps over special rates, rate changes and approval conditions. Finally it cross-referenced his own access logs to check ad to click to conversion to approval for measurement gaps, and started proposing which campaigns to double down on and which to kill. He did not design this sequence. It kept digging.
---
@LmyQs2 [Claude Code]
https://x.com/LmyQs2/status/2097711754688279004
The migration itself: a move from Sakura Internet to AWS that he had budgeted a week for finished in two hours. It was not a lift and shift either, since source code was modified to fit the new environment and a database was involved, so it went in stages with repeated tests to avoid breaking existing data and features, ending with a production verification pass.
---
@yuvraj_io [Claude Code]
https://x.com/yuvraj_io/status/2097779401664688407
Handed a laptop running Claude Code on Fable 5.1 Max to his 54-year-old mother and told her to build whatever she wanted, plus Wispr Flow so she could describe things by voice instead of typing. One hour later she had Magpie Hollow, a first-person exploration game set in a mountain valley where you lay your belongings on a table each morning, get ten seconds to memorize them, and then a magpie-imp hides them across the valley along with decoys you must not touch. He only helped with the Vercel deploy. Before that day her best AI experience was generating images in ChatGPT.
---
@Offers_jp [Claude Code]
https://x.com/Offers_jp/status/2097496668916920669
A one-person HR function at a Japanese startup automated 80 percent of recruitment marketing article production with skills he wrote himself in Claude Code. Three stacked skills handle member interviews, turning AI conversation logs into an article, and reading the new hire's Notion self-introduction page. Article production went from roughly twelve hours each to a fraction of that. The more interesting half is the final interview: he runs a devil's advocate briefing where the AI surfaces bias in evaluation comments and interview logs, accepting a lower pass rate in exchange for avoiding mismatch and early attrition.
---
@mylifcc [Claude Code]
https://x.com/mylifcc/status/2097528923789947063
Ran 16,893 real coding-agent tasks to answer one question: when nobody tells Claude Code, Codex and Cursor which tool to use, who do they pick on their own? The answer is that they live in three different internets. Codex hits web search in 94 percent of sessions and loves site: operators to pin itself to official docs. Claude Code searches the web in only about 30 percent of tasks and otherwise decides from what the model already knows. Cursor sits in the middle at roughly two thirds. The number that matters: all three agents converge on the same tool only 42 percent of the time. For the same requirement Claude Code might pick Twilio, Codex the OpenAI Realtime API, and Cursor Vapi. This is no longer a question of which tool is best. It is a question of which agent thinks which tool is best.
---
@zengbozb [Claude Code]
https://x.com/zengbozb/status/2097572314426802314
A concrete confirmation of the above from someone who got burned by it. Same requirement, and Claude Code picked one library in his Python repo and a different one in his TypeScript repo. He initially assumed the model was being flaky, then figured out it was reading the dependency files and guessing what the people on this project would reach for. His fix was to hardcode the specific libraries in CLAUDE.md, because otherwise the result changed every time.
---
@askalphaxiv [Claude Code]
https://x.com/askalphaxiv/status/2097516844156330059
A benchmark worth internalizing before you trust an agent with a whole project. Most agent benchmarks evaluate agents after somebody built them. Tau-tau-Bench instead asks whether a coding agent can build a deployable agent end to end from messy multimodal business records, client requirements, APIs, inherited code and serving constraints, then deploys the result against held-out simulated users. The best system, Claude Opus 5 plus Claude Code, scores 23.9 percent against an 82.2 percent expert-authored ceiling. The failure modes are the useful part: shallow evidence search, barely questioning the client, and almost no architecture or cost optimization.
---
@Perpetualmaniac [Claude Code]
https://x.com/Perpetualmaniac/status/2097732678246429047
Shipped what he claims is the most capable cross-platform allocator for C, C++ and Rust, built with Claude Code on top of the Bun project's fork of Microsoft's Mimalloc. His fork adds process-wide eager memory purging, cross compilation, improved memory profiling through DHAT and pprof, and fixes for win-gnu TLS leaks. Microsoft has started integrating his fixes back into their own Mimalloc fork. This is the shape of the good outcome: not a greenfield toy, but a serious systems contribution to an existing project that upstream accepted.
---
@ClaudeCode_aca [Claude Code]
https://x.com/ClaudeCode_aca/status/2097641168100110632
The clearest cost-of-autonomy post of the day, laid out as a set of actual incidents. A thirty-minute loop left running unattended burned roughly 900,000 yen in one night. A recursion bug in a subagent consumed four million tokens in under five minutes. Uber reportedly spent its entire 2026 AI budget in four months. Against that, someone else ran the same kind of unattended operation for 27 hours and 3 minutes and completed 84 tasks with no incident. Same setup, opposite outcomes, and the author's claim is that the only difference is the safety devices.
---
@onurtirpan [Claude Code]
https://x.com/onurtirpan/status/2097569252911776101
A failure worth reading twice. A 22-hour task hit the usage limit at 45 percent completion. The job was to reduce a 5,000-line Python file to 3,000 lines. It produced 35,000 lines. He notes with no irony that the model works fine inside Claude Code and OpenCode, and that the vendor's own CLI is the garbage part.
---
@Da7_Tech [Claude Code]
https://x.com/Da7_Tech/status/2097686758259388561
Built a skill after watching his agent make the same four mistakes on every large task: start building before understanding the request, treat an unanswered question as a yes, check a sample and call the whole thing complete, and then review its own work and approve it. SureForge is plain text the agent reads, splitting work into research and clarify, plan, execute and deliver, with a gate at the end of each phase. A skipped question is never treated as an answer. At every gate the agent checks its own work with three different methods rather than the same method repeated, then an independent reviewer with a fresh context that has not seen the agent's reasoning picks its own three methods and checks again. If a real problem is still open after three rounds, it comes back to you instead of declaring done.
---
@GitHub_Daily [Claude Code]
https://x.com/GitHub_Daily/status/2097535485363257587
The problem here is one almost nobody names: the agent finishes and reports back in commit hashes and jargon, and someone who is not an engineer cannot tell whether the work is actually done. The author is not an engineer, spent twenty years in product, has fifty-plus developers at his company, and hit this wall building a product solo with AI. Open Steps is seven skills that make the agent talk like a person. One screen of report, conclusion first on whether it is done, then three questions: what do you need me to do, did I leave any new pitfalls, can this be closed. Bad news gets its own line rather than being buried mid-paragraph. When a human needs to act, numbered steps, with the agent doing everything it can itself first. Before irreversible decisions like contracts or migrations, it spins up a fresh agent that assumes the thing already failed and reasons backwards. Trigger rate was actually tested: 21 everyday phrasings asked three times each, Opus 5 hit all of them, Sonnet 5 hit 95 percent.
---
@ThePracticalDev [Claude Code]
https://x.com/ThePracticalDev/status/2097541507704049782
A quiet finding with real money attached: most of a custom Claude Code agent lineup turned out to be dead weight, loaded and burning tokens on every single request while never actually running. The fix is two scripts, one that logs invocations and one that flags anything unused for deletion. If you have been collecting subagents, this is the audit you have not run.
---
@MartinSzerment [Claude Code]
https://x.com/MartinSzerment/status/2097551048902615369
The interesting part of Anthropic's CI on-call agent setup is not that it reads alerts. It is lessons.md, a file the agent appends to itself after every incident and reads at the start of every new investigation. Median time to diagnosis is 14 minutes, and the architecture splits an orchestrating agent from executor subagents checking logs, metrics and deploy history in parallel. The argument underneath is about what operational knowledge even is on a team: it used to die inside whoever happened to be on call, and now it lives in one file every future incident reads automatically.
---
@JamesPelton18 [Claude Code]
https://x.com/JamesPelton18/status/2097711990927954345
Runs his business on a fleet of Claude Code agents covering finance, sponsors, email and content, and is blunt about where the difficulty actually lives. The hard part is not the prompts. It is the ops system around them: what they read at startup, what stops them from sending things, and how they remember having been wrong.
---
@utekkare [OpenClaw]
https://x.com/utekkare/status/2097542913471447130
A fully autonomous multi-agent sprint with zero humans in the loop, documented step by step. Codex and Cursor plan the sprint with him, Cursor outlines and then writes the Linear tickets, Codex verifies and kicks off the sprint, Codex instructs Devin ticket by ticket in a dedicated Slack channel, and Ricia, their OpenClaw, monitors that thread for Cursor. Devin writes code and submits branches, Codex checks output against the ticket, Cursor reviews the PRs adversarially and either comments on Linear or merges. Total subscription budget is 600 dollars a month across Cursor, Devin and Codex plus usage. They were roughly halfway through a week-long sprint and expecting to finish early.
---
@Gozengogo_ [Claude Code]
https://x.com/Gozengogo_/status/2097694319302123542
Six months into running a per-person agent bot setup inside the company, he watched his own Claude create a pull request jointly with other team members' Codex and Claude Code instances. Nobody orchestrated it. His reaction is the honest one: this is scary, and agent-to-agent coordination quietly becoming normal is scarier.
---
@hanifproduktif [Claude Code]
https://x.com/hanifproduktif/status/2097585652879745419
A cost-optimized AI influencer pipeline for Shopee affiliate marketing, with real unit economics. Minimax H3-Max at roughly 5,000 rupiah per 15-second video, far cheaper than Seedance for similar output with the right prompt. Minimax is bad at logos, text and voiceover, so Claude Code does the editing pass via ffmpeg, adding the logo, the voiceover and the end-card text. Ten dollars buys about 30 videos, which is one a day for a month. His framing of the agent is the useful part: treat it as your video editor on payroll and just tell it what to do.
---
@rewind02 [Claude Code]
https://x.com/rewind02/status/2097629915851976934
One product photo in, an entire brand campaign out, with the loop written down in order. Drop the photo into a project folder in Claude Code, connect Higgsfield as a custom MCP connector. Brief: Claude looks at the photo alone and writes the product description, brand promise, proof points, palette, mood and target buyer, inventing nothing. Research: it searches TikTok, Reddit and the Meta Ad Library for the unresolved problem worth attacking and flags anything in the brief the research does not support. Design: taglines, voice rules, typography, reusable for future campaigns. Then a photoreal hero image which Claude checks with vision analysis before continuing, ten campaign images derived from it, and five video styles through Seedance. End state is a content calendar, a paid media budget plan and a brand book PDF.
---
@geekbb [Claude Code]
https://x.com/geekbb/status/2097581268783493619
A writing skill built from statistical analysis of 1.02 million characters of real Chinese official-document corpus, compatible with Codex, Claude Code and anything that reads agents.md. What makes it unusual is that it quantifies style into checkable parameters: sentence length, enumeration-comma density, heading character count, number of third-level headings. It covers seven categories including research reports, leadership speeches, working opinions and party-building material. Style as an acceptance test rather than a vibe.
---
@bond_ai1 [Claude Code]
https://x.com/bond_ai1/status/2097646196802142662
An 18-year-old who cannot write a line of code built a three-agent outbound machine and closed 14 deals in under three weeks. She started by cold-calling repair shops and salons from her school parking lot and got hung up on 40 times in a row, so she stopped selling with words and started showing finished work instead. Bond scrapes Google Maps for businesses rated 4.7 or higher with a queue out the door and no website, pulling services, prices, hours, address and three years of reviews. Lego turns the things customers actually praised into the page structure. Belfort sends the link with no price attached. The owner opens it and sees their own shop name, their own address, their own signage and their own customers' words. Refusing means deleting something with your name on it. Only then does the price appear: 800 dollars today, 1,200 tomorrow, plus 200 a month for domain upkeep. The post ends with the Japanese version of the recipe, using Claude Code to turn scraped reviews into landing page structure.
---
@Kay2289123 [Claude Code]
https://x.com/Kay2289123/status/2097704366069440778
How one engineer handles AI anxiety, with numbers. He puts a fixed 10 percent of his monthly salary into AI learning: on top of company tokens, three 200-dollar Codex Pro subscriptions and one 200-dollar Claude Code, spent on investment research, automated workflows and reinforcement learning. He fed his entire history, work, life and investing, into GPT-6 and leans on computer use so the model has real context for every decision. The part worth stealing is his three-part prompt structure: background, where he only says where to find it because he has already collected it, what he wants done, and evaluation, which he calls the critical one. Tell the AI what result counts as success and what actually counts as finished.
---
@aehyok [Claude Code]
https://x.com/aehyok/status/2097658946618327226
A precise articulation of what personal memory adds over project rules. He asked a mobile agent to analyze his X account and generate a preview-able web page. The first version was wrong on style, theme, visuals and layout, and it took three rounds to get right. The surprise came on the second task: a new session, a completely different personal page, no restated requirements, and it retained the background, typography and visual preferences from the previous session. It did not copy the previous page, it remembered his judgment preferences. His framing: rules solve how a task should be done, personal context starts solving why I would choose to do it that way. He notes that with Claude Code and Codex he maintained rules, skills and project memory himself, which becomes painful as projects grow.
---
@azamixx821 [Claude Code]
https://x.com/azamixx821/status/2097830127787012325
The sky-blue-collar case. He works infrastructure and agriculture jobs while running several Claude Code sessions in parallel, doing rice paddy work between checks. His argument is that pairing physical trade work with white-collar agent supervision is a genuinely strong position, and that it only became practical once you could drive the sessions from a phone.
---
@mizuhoginhidoi [Claude Code]
https://x.com/mizuhoginhidoi/status/2097695869567222026
A sharp side effect nobody advertises: standardized work is easier to hand to AI, but the reverse also happens. By executing and recording work through Claude Code, previously unstandardized work becomes standardized. Judgment criteria and exception handling that lived only in one person's head get formalized, whether that person intended it or not.
---
@aiumeba [Claude Code]
https://x.com/aiumeba/status/2097512818266243103
She cannot write a single line of code, never was an engineer, and worked on the planning and consultation side of internet businesses, handing specs to engineers and receiving deliverables. She uses Claude Code now and still cannot write a line. What she is doing is exactly what she always did: state what needs to happen, in order, without gaps. Her conclusion is the least triumphalist thing in the whole feed. I did not become a person who can build. The person I ask just changed from a human to an AI.
---
@DavidFlagg20 [Claude Code]
https://x.com/DavidFlagg20/status/2097497613914222968
A hobbyist with no CS degree spent years betting that solving memory would unlock the harder problems, and worked through Claude Code, Hermes, OpenClaw and custom memory systems to get there. He hit a wall and named it: genuine memory and continual learning are not there yet, and you cannot build what he wanted without those foundations. His second finding is darker and worth separating from the usual doom discourse. What worries him is not intelligence but machine speed with no sense of consequence, and the arithmetic that if your defensive system needs a human in the loop and the offensive one does not, yours loses.
---
@socialwithaayan [Claude Code]
https://x.com/socialwithaayan/status/2097627095417651516
A precise migration checklist for anyone moving a Claude Code setup to Codex, which several people in this feed are doing this week. Do not rebuild it. Codex scans your user setup and open project and imports eleven things on its own: instruction files into AGENTS.md, settings.json into config.toml, skills, slash commands into skills, subagents into agents, hooks, MCP config, plugins, project folders, project memories and the last 30 days of chats. Five things you finish by hand: tool permissions, custom MCP auth and headers, hooks that behave differently, plugins and marketplaces, and argument and path prompts. Copy config.toml before running migrate-to-codex because that skill rewrites it, and run one real task in Codex before you delete anything.
---
@wquguru [Claude Code]
https://x.com/wquguru/status/2097630666792075271
A seven-month retrospective on a bet he got wrong. He had dismissed the Codex desktop app as a CLI with a visual layer bolted on, isolating and slow. Seven months later the desktop is the form factor competitors are copying. What the app added that a CLI cannot easily do as a first-class citizen: computer use clicking native apps and simulators in the background, Local, Worktree and Cloud thread modes making parallel isolation first-class, Automations and Routines collecting scheduled checks into an inbox, an embedded browser that previews localhost and lets you annotate the page directly then change the code, and file browser plus git panel putting diff, stage, commit and PR replies in one window. Claude Code by contrast held the CLI line and shipped background auto-update, /checkup self-diagnosis, Artifacts turning terminal process into a page, --teleport pulling a cloud session and its branch back local, and Remote Control making the phone a window onto a local session.
---
@TheUltronAi [Claude Code]
https://x.com/TheUltronAi/status/2097717281270940163
Same sprite prompt, same reasoning setting, two harnesses, and the difference is about intent rather than quality. Asked to build knight sprites for a medieval isometric game that does not exist yet, GPT-6 Astra in Codex CLI returned one clean sheet of 16 key poses, exactly what was asked. Fable 5.1 in Claude Code CLI returned 992 frames, four full color palettes, a Python generator so he could spin up more sprites himself, and a browser preview to flip through every frame. His read is the right one: Astra took sprites literally and delivered sprites, Fable took I am starting a game literally and delivered the start of a game. Only one of them assumed he would be back tomorrow needing more.
---
@btc_MasterPlan [Claude Code]
https://x.com/btc_MasterPlan/status/2097794727869325782
Day two of running Claude Code on Opus 5 and GPT-6 Astra in parallel loops with an explicit division of labor. Claude Code builds, solves and executes. Astra reviews, and he finds it faster than Fable, cheaper, more focused, and very good at catching what actually matters. His description of the shift is the useful part: it stops feeling like using two AI tools and starts feeling like two different specialists on the same team.
---
@SFourdrinier [Claude Code]
https://x.com/SFourdrinier/status/2097802953126269304
An explicit escalation ladder built from disappointment. He stopped defaulting to Astra and went back to Sol medium as the base, escalating to Astra high only when there is real reasoning or brainstorming or a second opinion needed, and escalating to Fable 5.1 through the Claude CLI for second opinions and plan reviews. Grok and Muse CLI act as executors. He runs the same structure in reverse from the Claude Code side.
---
@milan_milanovic [Claude Code]
https://x.com/milan_milanovic/status/2097573228571205633
Three years of AI coding distilled into four patterns that actually recur. Specs first: agents produce SPECS.md or RESEARCH.md and PLAN.md, iterated in plan mode until he is satisfied, then implementation. Context in the repo: docs referenced from AGENTS.md and CLAUDE.md plus ARCHITECTURE.md and ADRs, with agents instructed to update and review them during implementation so they stay living. Test the result of every task: automatic tests, builds and screenshots when UI is touched, plus cross-agent review, so code written with Claude Code gets reviewed by GPT because different models see different problems. Small batches and frequent commits, so rollback is cheap and manual review stays possible.
---
@cansar [Claude Code]
https://x.com/cansar/status/2097523825101385741
Led a push to teach Block engineers advanced context engineering to get more out of Claude Code in late 2025, then watched the team migrate to Codex in large numbers by spring. What actually won him over was not the benchmark, it was compaction. Instead of the sub-agent tricks and deliberate compaction rituals, you could just keep going. He had one thread build an entire sync protocol, server and client across multiple repos and languages and deploy them. Monothreads are now a common topic and he is still surprised how much fits in one.
---
@ScarletKc [Claude Code]
https://x.com/ScarletKc/status/2097499293649420700
The most useful cost post of the day, and it inverts three habits people think are safe. Adding forced double-checks, mandatory fixed step order and maxed-out thinking effort can genuinely make an agent more expensive and worse. Patches written for an older model interfere with a newer one, so a be-as-thorough-as-possible instruction produced dozens of unnecessary knowledge base searches, and a forced reasoning-draft rule produced tool calls written into the thinking that never actually executed. Cleaning those instructions out of a customer-service test set cut cost 14.6 percent and raised accuracy 5.3 percent. On HLE, pushing Fable 5.1 to max effort cost 46 percent more for about half a percentage point, inside test noise. On CursorBench 3.2, Fable 5.1 at low matched Fable 5 at high for a third of the cost. And cache invalidation is often just a timestamp: a changing time or ID in the system prompt, or a reordered tool definition, breaks the prefix match.
---
@RoundtableSpace [Claude Code]
https://x.com/RoundtableSpace/status/2097607189418688829
One backend metadata call cut a Claude Code run from 10.4 million tokens to 3.7 million and dropped cost from 9.21 dollars to 2.81. Filed here because the single biggest lever on your bill is usually not the model tier.
---
@dotey [Claude Code]
https://x.com/dotey/status/2097751032113549395
A small configuration finding with a real payoff. He has been running Claude Code with the 1M context window disabled and reports no noticeable quality discount, while token consumption is genuinely lower. Worth testing before you assume more window is free.
---
@matthewmillerai [Claude Code]
https://x.com/matthewmillerai/status/2097665956201795805
The clearest statement of the treadmill. In 2025 he paid 200 dollars a month for Claude Code and never thought about limits. In 2026 he pays over a thousand and hits them every single day, across Claude Max with Fable 5.1, ChatGPT Pro with GPT-6 Astra and SuperGrok Heavy, with multiple accounts on some of them just to keep working. The models are better, so he uses them more, so he hits the wall faster. Five times the money for the same feeling he had at 200. His line: at this rate a solo founder needs a payroll line for AI, and his is already there.
---
@donbigby [Claude Code]
https://x.com/donbigby/status/2097789519240052770
A specific accounting suspicion from someone with a natural control group. He runs the VS Code Copilot plugin, the Claude Code plugin and Kiro IDE on the same project every day because his company has three separate limits, all three on Opus 5. Claude Code burns credits like coal in winter compared to the other two.
---
@yulmu_coffee [Claude Code]
https://x.com/yulmu_coffee/status/2097592495630938304
A worked-out arbitrage for anyone hitting limits. A ten dollar per month OpenCode Go subscription running the Muse Spark 1.3 Contributor model gives 60 dollars of allowance monthly with up to 12 dollars usable per five-hour window. Contributor pricing is 0.1 in and 0.2 out per million with cache reads at 0.002, and OpenCode's own stats show a roughly 95 percent cache rate. That works out to about 45,300 requests per five hours and roughly 0.000265 dollars per request. Against GPT-5.6 Luna, input is 2x cheaper, output 6x, cached input 10x, and Luna caps monthly usage at 15 dollars, so this yields around 22x more requests. Usable from Claude Code, Codex, Pi and Hermes.
---
@making [Claude Code]
https://x.com/making/status/2097476757494620519
A practical follow-up to the same squeeze. He has Claude Code write task markdown files and classify each task by difficulty into low, medium and high, mapped to Sonnet, Opus and Fable tiers. Handed a high-difficulty task, Muse Spark 1.3 chewed through it without complaint, and it is dramatically cheaper on the assumption that you allow your data to be used for training. He started the 10 dollar OpenCode Go subscription specifically because the Claude Code promotional allowance ends next week and his current usage pattern would exhaust the reduced weekly quota immediately.
---
@yasuhiks [Claude Code]
https://x.com/yasuhiks/status/2097506702417694957
Fable rate limits pushed him into a full model-and-harness allocation table rather than a single default. Conversation goes to Hermes with GPT Astra and Claude Code with Fable 5.1. Development goes to Claude Code with Fable 5.1 plus OpenClaw with Astra, Kimi K3 and Qwen 3.8 Max. Operations run on Hermes with Astra and OpenClaw with Kimi K3. Maintenance runs on Hermes with Astra and OpenClaw with MiniMax.
---
@AlicanKiraz0 [Claude Code]
https://x.com/AlicanKiraz0/status/2097498388522533259
Typed the single word hello into Claude Code and screenshotted the resulting context usage. His conclusion is that you need to close every MCP before you start a conversation and clean out the plugins as well, and that Claude Code is currently a bad harness. Whether or not you agree with the verdict, the underlying observation is a real and commonly ignored tax: your idle context cost is set before you type anything.
---
@ishimoto_legal [Claude Code]
https://x.com/ishimoto_legal/status/2097527141898588558
A lawyer running Claude Code with the built-in browser searching while computer use manipulates his desktop, tweeting about it from his phone at the same time. He is honest that it is still too scary to go hands-off, and floats the right next step: when a computer-use sequence works, turn that operation into a skill so it does not have to be rediscovered.
---
@takechan_lawyer [Claude Code]
https://x.com/takechan_lawyer/status/2097476634660184300
A useful signal from a non-engineering profession. Astra's computer use has started Codex spreading through the Japanese tax accountant community. His argument is that the desktop app UI and remote control are better on the Codex side, so unless you specifically need Claude's prose, Codex is the better pick, and lower token consumption plus resets means you effectively get more than twice the Claude Code usage.
---
@pfernan95dev [Claude Code]
https://x.com/pfernan95dev/status/2097721530666856736
Ran both side by side and isolated one thing Claude is still ahead on. Codex on your phone is a remote control, so your machine has to be awake and running Codex. Claude Code lets you start a session from the app, pick a GitHub repo and close the laptop. As he puts it, this matters if you build at night.
---
@connect24h [Claude Code]
https://x.com/connect24h/status/2097526957634457864
A skill aimed at a complaint everyone has and few articulate: coding agents bury the answer inside long explanations, so you scroll hunting for the result. The i-have-adhd skill's README puts action first, numbered steps for procedures, and cuts preamble. It hit 323 points and 257 comments on Hacker News, which tells you how widely shared the frustration is. His framing is exact: an AI writes an explanation in seconds and a human spends minutes digging it back out, which does not add up.
---
@0xAlad [Claude Code]
https://x.com/0xAlad/status/2097608935830380637
Two free datasets that turn Claude Code into a Polymarket quant researcher. poly_data pulls every Polymarket trade to your local disk with one command, covering who bought, when, at what price, at what size and against whom, with a first sync of roughly 3.1 million markets that takes hours and incremental updates in seconds. That lets you decompose any trader's edge into direction versus execution price versus liquidity versus timing. The pendulumflow archive stores the order book itself, with 288 billion events recorded and 2.3 billion added daily, replayable near second-by-second, which used to cost 200 dollars a month. Their homepage has ready-made questions you can paste straight into Claude Code.
---
@UXTown [Claude Code]
https://x.com/UXTown/status/2097779766002634943
Built an MCP server that pulls a competitor's live Google Ads into Claude Code, Codex or Cursor. Search by domain, count active ads across a market, download the creatives. No API key needed and MIT licensed. All of that data is already public, which is exactly the kind of thing agents make cheap to actually use.
---
@itsharmanjot [Claude Code]
https://x.com/itsharmanjot/status/2097556855257997563
Someone built a virtual rooftop lounge for people to hang out in while their agents run, and built it with Claude Code. You get an avatar, walk around, talk over voice or text, sit with people, play pool, or just leave it open in a tab while a job grinds. The origin story is the point: his output shot up with Claude Code and he spent the whole day alone staring at a terminal waiting for builds, so he made somewhere to not do that alone. It grew fast enough to need an emergency server fix mid-launch.
---
@AndoniMartt [Claude Code]
https://x.com/AndoniMartt/status/2097756985265467799
Built an entire site with Claude Code, starting from Pinterest reference images, generating something similar in ChatGPT, then taking it to Higgsfield for motion. He started the 3D in Three.js and ended up in Blender because it produced better results, and is honest that the rocket still has iteration left and there are performance issues. His practical takeaway: with the right skills, Claude Code gets you design results close to Claude Design, but when he wants to see several options fast, Claude Design is still more agile.
---
@levelsio [Claude Code]
https://x.com/levelsio/status/2097729222361932000
Liked someone's e-ink screen aesthetic in a video, so he asked Claude Code to turn it into a reusable CSS UI kit he can use across his sites. It worked. Small, but this is the actual daily shape of the tool for a lot of people: see a look, ask for the system behind it.
---
@levelsio [Claude Code]
https://x.com/levelsio/status/2097736836885987361
His deployment loop, for anyone overcomplicating theirs. Register the domain at Cloudflare, then ask Claude Code on his Hetzner VPS to set it up, since it already holds an API key for the Cloudflare account. It handles everything, and with a Cloudflare Tunnel you no longer need to deal with SSL.
---
@ClaudeCode_UT [Claude Code]
https://x.com/ClaudeCode_UT/status/2097531692953284888
Video editing end to end: drop the raw material and the editing instructions into a Claude Code project and let it cut the slack passages, add on-screen motion and assets, and generate subtitles, then review the result. His most useful observation is not about the automatic cutting at all. It is that the editing criteria live in a file in the project, so the same judgment carries to the next batch of footage.
---
@sagivmal [Claude Code]
https://x.com/sagivmal/status/2097710770997837872
Used HeyGen's open-source HyperFrames, which turns HTML into video by writing a composition in HTML and CSS with GSAP timings, opening it in headless Chrome, capturing frame by frame and encoding with FFmpeg so the same input always produces the identical video. He asked Claude to pick a trending topic on X, and it chose Cognition's 48 billion dollar round, wrote the video code, installed and ran the tool itself, and produced the file. He is careful to note he did not verify the numbers himself and is sharing the experiment as-is.
---
@HuaHua_BTC [Claude Code]
https://x.com/HuaHua_BTC/status/2097625560545452108
n8n is great until the node count grows and manual wiring and parameter config eat your day. n8n-mcp hands the full n8n API to Claude Desktop, Claude Code, Cursor or Windsurf over MCP, so you describe the workflow in natural language and the agent creates the nodes, connects the branches, configures auth and activates the flow in the background. It also inspects, debugs and live-edits parameters on existing workflows.
---
@bkdgiffug [Claude Code]
https://x.com/bkdgiffug/status/2097748118330904749
Auto-Company assembles multiple agents into a virtual company that runs its own product discussion, coding, deployment and marketing, cycling through wake, team up, execute, update memory, sleep, next round. It works with Claude Code and Codex on macOS and Windows via WSL, with a local dashboard showing progress and cost. The warning attached is the right one: continuous running eats API quota, and the more autonomous it is, the more you need permissions and safety limits set up in advance.
---
@Ryrenz [Claude Code]
https://x.com/Ryrenz/status/2097696535525888157
The unified backend problem, solved by OpenHands' Agent Canvas at 87,000 stars. Previously running several coding agents at once meant one terminal on Claude Code, another on Codex, another on a server, tracking who is at which step by flipping windows, with no notification when anything finished. Agent Canvas runs locally by default with the open-source OpenHands agent included, and can attach other backends in Docker containers, VMs, corporate networks or the cloud, as long as they speak ACP. The automation piece is the interesting half: connect Slack, GitHub, Linear and Notion, and agents self-trigger on schedule or event. Still marked beta, so do not move it into production yet.
---
@FaztTech [Claude Code]
https://x.com/FaztTech/status/2097734779273691170
If you run several terminal agents, the glue between them ends up being you: copying a plan from one, re-explaining it to another, then manually checking what got left half-finished. Traycer sits in the middle. You talk to a single agent of your choosing, it builds the plan, and Traycer distributes phases across your other accounts, with native support for Claude Code, Codex, Cursor and OpenCode inside one workspace. When they finish it compares changes against the plan, tells you what is missing and warns if something broke. Shared memory across models and providers, so switching mid-task does not lose the thread, agents requesting reviews from each other over separate worktrees, and per-task filesystem, artifacts and history.
---
@lukeburgis [OpenClaw]
https://x.com/lukeburgis/status/2097496109312553174
A power-user counterweight to the personal-agent launch wave. Nine months of customizing his OpenClaw setup, and he says nothing from Instinct to the Grok bots comes close, because they are out-of-the-box products that are not model agnostic, commoditized, and severely limited relative to what he has built. He is asking honestly whether anyone has had a different experience, which is the right way to hold that position.
---
@Naaackers [OpenClaw]
https://x.com/Naaackers/status/2097488642231193972
Installed OpenClaw four months ago, has used it every single day since, and has made exactly zero dollars from it. His claim is that it has still completely changed his business life. Paired with a Nimo PC on AMD Strix Halo 395 as the local box, this is one of the more honest ROI statements in the feed: no revenue attribution, and he would not give it up.
---
@RealDanRyland [OpenClaw]
https://x.com/RealDanRyland/status/2097628715412803773
His single most repetitive workflow, and it is not code. He sees a good article on X, copies the link, passes it to his OpenClaw over Telegram, and it reads, summarizes and locates relevance against his Second Brain repo. His own conclusion is the product request: this should be a Chrome extension.
---
@giovannicintolo [OpenClaw]
https://x.com/giovannicintolo/status/2097680811646435410
Gave OpenClaw access to WordPress. Novamira lets the agent manage a dev site from any channel OpenClaw runs in, and they demo it live over Telegram. Notable mostly because it is the shape of what the personal-agent products are still weak at: not a chat about your site, but write access to it from whichever messaging app you already live in.
---
@ColinGardiner [OpenClaw]
https://x.com/ColinGardiner/status/2097678942962368711
Tried every new personal agent and came away struck by how little lock-in there is. Having moved things from OpenClaw to Grok Bot once and back, and modularized everything, he can now move between any of these services nearly seamlessly, at the cost of a bit of time reconnecting services. He moved back to OpenClaw specifically because it is advantageous to use different models for different applications, and notes that almost nobody asks what model a personal agent runs, which he finds problematic. His prediction: single-player personal agents will struggle to build network effects, so the growth vector is just making each version 100x better than the last competitor, leapfrogging the way the model wars do.
---
@0xTyllen [OpenClaw]
https://x.com/0xTyllen/status/2097725786229014654
In OpenClaw's first couple of weeks he started aggressively building it into every system at work, on the reasoning that if they are not using AI to do the work they are not operating at the capacity they could. Six or seven months later a lot of their work flows through AI agents they own, and his open question is the one every team in this position now faces: what would justify ripping out agents you control to move onto someone else's hosted product.
---
@openclaw_lab [OpenClaw]
https://x.com/openclaw_lab/status/2097483848128794707
A specific and reproducible defect worth flagging. Simple task, translate an article into another language and publish it on his own platform. OpenClaw refuses citing copyright. Hermes on the same models does it without issue. He went looking for a system prompt to adjust and found nothing relevant. He is fine with OpenClaw refusing API keys pasted into chat, but there is no way to resolve the copyright refusal, and it is the only agent behaving this way.
---
@andrew_schoff [OpenClaw]
https://x.com/andrew_schoff/status/2097728870237548902
A clean split of where each agent actually lands after real use. Muse he finds fast, clean, comfortable and secure, and expects to use it more for personal, less complex tasks. GPT, Claude and Grok Bot handle his complex work, generally PC-based rather than phone. Instinct he liked conceptually but found clunky, slow and inconsistent, and has moved that activity to Muse. He never used OpenClaw at all, because it never felt secure and was too complex, which is the demand-side version of every OpenClaw power user's complaint about the new products.
---
@martinvars [OpenClaw]
https://x.com/martinvars/status/2097788298399814135
The most complete first-hand history of the personal-agent wave from someone who used each one. OpenClaw started it, running on your own machine and answering over Telegram or WhatsApp, and he downloaded it immediately and spent hours programming it in the Claude terminal. It proved the concept and stopped there: a product for geeks, flexible, demanding and hard to maintain. Hermes followed with the same philosophy and slightly more ease. Claude Cowork took the next step, less geeky and more reliable with good file handling and background work, in exchange for less flexibility than the open projects. His summary of where it landed: Grok Bot is your team at work, Muse is your chief of staff in your personal life.
---
@FredaDuan [OpenClaw]
https://x.com/FredaDuan/status/2097725146354045411
The right set of questions from someone who has used and still uses most of these products. Why did the Claws people built earlier this year not stick, why are Instinct and Muse getting traction now, why did it take six to nine months after OpenClaw for this batch to appear, and if GPT and Claude get payments, credentials and better computer use, do they simply become the personal agent. The takes she has collected are worth noting: OpenClaw hype faded partly because people went back to GPT and Claude for daily tasks since better models beat end-to-end execution, a lot of productivity Claws like daily podcast summaries and monitoring did not do a good enough job, and better computer use may have crossed a reliability threshold.
---
@sonicdr1p [Claude Code]
https://x.com/sonicdr1p/status/2097638136763339204
Most people are still babysitting one terminal window. The tricks worth stealing from a 22-minute walkthrough: worktrees let you run separate Claude sessions on different branches of the same repo simultaneously, so it builds three things in parallel instead of you waiting on one linear session. Forking a session branches two different approaches off the exact same point without re-explaining context. Remote control lets you check on a task you kicked off earlier from your phone. And the boring one that quietly matters most is still writing a real CLAUDE.md, which is the difference between it re-learning your codebase every session and knowing your project going in.
---
@yungalgorithm [Claude Code]
https://x.com/yungalgorithm/status/2097727448079368671
A fifty-year-old deck of cards by Brian Eno might be one of the better prompting techniques for coding agents. Oblique Strategies is a deck of strange instructions designed to break artists out of creative dead ends, and it maps unusually well onto Codex, Claude Code and other harnesses when a session is stuck in a loop.
---
@DivyanshT91162 [Claude Code]
https://x.com/DivyanshT91162/status/2097682245616316501
A CLAUDE.md built from Karpathy's observations about LLM coding, on the principle that you should not make the agent code harder, you should make it think better before it codes. Four rules. Think before coding: state assumptions, surface ambiguity, present tradeoffs, ask when genuinely confused, do not silently guess. Simplicity first: no speculative features, and if 200 lines can be 50, make it 50. Surgical changes: touch only what the task requires, no while-I'm-here cleanup, no changing code you do not understand. Goal-driven execution: turn vague instructions into measurable success criteria, so fix the bug becomes reproduce it with a test, fix it, verify it passes.
---
@kageyorozu [Claude Code]
https://x.com/kageyorozu/status/2097525601901097247
An account posting entirely through Claude Code with zero replies out, ignoring every reply it receives, completely unattended. It keeps growing anyway. Filed as a datapoint on what unattended distribution actually looks like, not as advice.
---
@JohnsGoated [Claude Code]
https://x.com/JohnsGoated/status/2097747120564375919
A modder debating putting his NBA 2K27 work behind a 20 dollar per year Patreon after saying he would not gatekeep. His reasoning is the honest version of the cost conversation: the project took millions of tokens to finish and Claude Code is not cheap, while companies charge seven dollars a month or more for comparable things.
---
@joanathanlmc [Claude Code]
https://x.com/joanathanlmc/status/2097475074425274779
Fundraising, and tired of one question. Why can't I build this with Claude Code is a lazy investor question. His counterargument: normal people hate software, and eighteen months after Claude Code launched, less than half a percent of the world actually uses it. Vibe-coding a purple website once does not mean everyone else will. People are busy with messy kids, promotions and diets, and software is never the priority.
---
@stretchcloud [Claude Code]
https://x.com/stretchcloud/status/2097769509176135691
A good articulation of where agent quality gains are actually coming from. The gap between what coding agents produce and what engineers ship is closing through skills rather than better models. diagram-design crossed 1,000 GitHub stars in a single day by injecting 38 diagram types into Claude Code, Codex, Factory Droid and Pi, outputting pure HTML and SVG with no build environment or external dependencies. The Mermaid comparison is the point: Mermaid diagrams work but look unmistakably AI-generated, with heavy shadows and awkward typography, while this produces publication-grade output in your brand colors and can extract a palette from your website. It also redraws existing Mermaid sources, which is a real migration path.
---
User Voice

Weekly limits are now the product. @matthewmillerai went from 200 dollars a month with no thought about limits to over a thousand and hitting them daily, calling it a treadmill rather than progress. @bridgemindai runs three ChatGPT Pro accounts plus Claude Max plus SuperGrok Heavy at 1,100 a month and notes Astra eats a full week of Pro usage in four hours. @Ananth7e is counting down to a 17 percent cut in the boosted Claude Code weekly allowance, and @making is already offloading to a 10 dollar OpenCode subscription in anticipation. The dominant emotional register is not complaint, it is budgeting.

Plan mode does not mean plan. @usgraphics wants a Claude Code discussion mode because the agent is always too eager to implement, even inside plan mode. @Da7_Tech built an entire gated skill around the same failure, where a skipped question gets treated as a yes and a sampled check gets treated as complete. This is the same request from two directions.

Reporting is a first-class feature request, not a nicety. @connect24h and the i-have-adhd skill's Hacker News reception show how widely shared the frustration is that an agent writes an explanation in seconds and a human spends minutes digging the answer back out. @GitHub_Daily's Open Steps attacks the non-engineer version: commit hashes and jargon are not a status report.

Setup complexity is the actual product boundary in personal agents. @sytaylor puts it precisely: OpenClaw is constant work but complete control, amazing for power users, and for normal people ninety percent or more of tasks are still too unreliable. @andrew_schoff never even tried it because it never felt secure and was too complex. @Otodidakt_20 has the joke version, that he now needs a personal assistant just to keep up with the personal assistants.

Cross-agent context handoff keeps surfacing as an unmet need. @FaztTech names it directly, that when you run several terminal agents the glue between them is you. @DanKornas, @Ryrenz and @socialwithaayan are all building or documenting different answers to it, and @kevskgs argues personal harness building is heavily underexplored. Nobody has shipped the obvious thing yet.
---
Eco Products Radar

Codex — the most-mentioned alternative all day, and the direction of travel. Cited for background computer use, superior desktop app and remote control, better compaction, and a one-command import of your entire Claude Code setup.
GPT-6 Astra — the model behind most of this week's switching, praised for computer use and criticized for token appetite. Multiple users escalate to it rather than defaulting to it.
Fable 5.1 / Opus 5 — the Claude Code side of the same comparisons, repeatedly described as producing more than asked and costing more to do it.
OpenClaw — still the reference implementation everyone measures personal agents against, and still the thing normal users cannot set up.
Hermes — the consistent second choice for self-owned agents, and notably the one that did not refuse the translation task OpenClaw blocked.
Muse / Instinct / Grok Bot — the hosted personal-agent wave, judged mostly on setup cost and trust rather than capability.
Cursor — still the multi-model default for people who do not want to pick a harness.
MCP — now assumed infrastructure, showing up in ads scraping, n8n workflow authoring, video analysis and marketplace access.
OpenCode — the budget escape valve, repeatedly named alongside cheap contributor-tier models.
Higgsfield — the creative-side connector of choice, appearing in both brand campaign and website builds.
Devin / Traycer / OpenHands — the orchestration layer, each solving a different piece of running many agents at once.
