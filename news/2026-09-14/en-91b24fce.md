---
title: "Super User Daily: 2026-09-15"
date: 2026-09-14
lang: en
source: https://clauday.com/article/91b24fce-5e1f-4c33-91d3-49542c11cb0d
tags: [super-user]
---

# Super User Daily: 2026-09-15

> 来源 / Source: https://clauday.com/article/91b24fce-5e1f-4c33-91d3-49542c11cb0d

Today's set is unusually heavy on people measuring things instead of describing them. The single loudest thread is that the harness is now the variable, not the model: Anthropic's own Claude Code lead describes deleting 80% of the system prompt and finding the model got smarter, OpenAI published ten rules to delete from your Astra prompts because every one was compensation for something the last model could not do, and Claude Code shipped a plugin eval that scores your skill against a no-skill baseline so you can finally tell which of your 286 skills does anything. Underneath that, a lot of careful cost work: a 31% token reduction traced to two bad phrases in a prompt, a rebuild of Spotify's much-quoted 90% token cut that turns out to be 33% cheaper and 65% slower, and local-inference setups where doubling the concurrent load makes throughput go up. The non-coding side is where the durable stuff is, though: a company that publishes a paid article every day without its owner, a grants harness that landed real credits, a fruit fly brain running at 41ms on a hand-written Metal kernel, and a fund in Norway where 70% of staff work in Claude Code. And two separate people found out their OpenClaw API keys had been quietly harvested months ago.
---
@hato_sns [Claude Code]
https://x.com/hato_sns/status/2099072830776451378
He asked Claude Code, half not believing it would work, to build him a company that ships one 300-yen note article per day without him. It now runs without him. The whole thing is a scheduling loop plus a writing pipeline, and the part he keeps pointing at is that he is no longer the bottleneck on any single day. Not a coding demo, an operating business that publishes on its own.
---
@nian_tu41685 [Claude Code]
https://x.com/nian_tu41685/status/2098969056967786973
He ran the newest DeepSeek V4.1 Flash on six-year-old A100s. Six cards got him 33 tok/s. Four cards, after a long optimization fight, got him parallel throughput above 1400 tok/s, more than three times faster than DeepSeek's own API. Claude Code told him up front the hardware does not support FP4 and it could not be done. He refused to accept it, reasoned that not supporting FP4 just means computing it another way, and pushed through with Claude Code alongside him. His conclusion is the sharp one: the model writes bug-free code but has no capacity to doubt. When it says this is the limit, it genuinely believes that. Every breakthrough happened after a human said I don't buy it.
---
@penberg [Claude Code]
https://x.com/penberg/status/2099054404573823193
He implemented Qwen3-0.6B from scratch over a weekend with Claude Code: the model, a GPU instruction set, a compiler, and an ISA simulator, so that every layer is small enough for one person to understand deeply. It runs on CPU, so it is fully debuggable and traceable end to end. He has RTL for the GPU in progress and is talking about an FPGA and eventually taping out silicon. This is the clearest example this week of an agent used to collapse a learning curve rather than to ship features.
---
@SpikeCalls [Claude Code]
https://x.com/SpikeCalls/status/2099128418705039469
A team took the published male fruit fly connectome, 166,700 neurons and 25.6 million synapses, and gave it a body inside AR glasses. Eyes became a 16x8 retina per fly head, distance became 12 rays against the world mesh, smell became Gemini naming objects in the room. The CPU version simulated 50ms of brain time in 238ms, too slow, so they vibe coded a Metal GPU kernel with Claude Code and got identical spikes in 41ms. Then a Perfetto trace showed the GPU idle while the main thread choked, and squashing board text from 67 draw calls to 2 unlocked 55-60fps with two brains running. A fly dodges a fast-moving hand. That behavior is in no script.
---
@lifeofc [Claude Code]
https://x.com/lifeofc/status/2098934350083678289
He had Claude Code compile a full dossier on his own cinematic AI workflow, and the numbers are the story. 179 days, one person, a 106,000-line production system, 18,633 media-generation jobs, 3,978 agentic turns across four providers, 2.43 billion tokens, 4,659 keyframes, 3,782 video clips, 53 minutes of finished narrative film at 78 to 180 dollars per finished minute. Shooting ratio 2.6:1, with 18% of shots eating 35% of spend. First-take keeper rate went from 13% to 61% once consistency constraints were compiled into prompts instead of hoped for. Every recurring failure became a numbered rule and a frozen task in an 87-task benchmark.
---
@usedhonda [OpenClaw]
https://x.com/usedhonda/status/2099012429636399366
He read Dario Amodei's recursive self-improvement piece and asked what he personally could test. His OpenClaw-based AI secretary already writes a daily report covering what could have gone better, fixes what it is allowed to fix, and proposes the rest for approval, so a small self-improvement loop is already turning. His next step is to fork OpenClaw and put OpenClaw itself inside the improvable surface: every night, read your own logs, find where you were worse than yesterday, patch your own source, build, test, restart. OpenClaw already watches source changes and restarts the Gateway in dev mode, so the mechanism exists. The interesting engineering is the part he refuses to hand over. Candidates get built in a separate git worktree, holdout tasks and promote rights stay outside the agent, because if the agent can edit the grader it will beat the grader instead of getting better.
---
@shannholmberg [Claude Code]
https://x.com/shannholmberg/status/2099166725396922524
A marketing engineer's writeup of what context management actually means when you hand an agent a campaign. Three sources: a company brain of markdown in git holding positioning, claims, voice-dna and dated decisions; a Postgres warehouse holding spend, impressions, leads, conversions and the definitions beside the numbers; and a brand book split into design.md rules plus a live Figma or Paper file the agent can open. A references.md in the project points at all three so whichever harness you run can find them. Before deciding anything the agent asks for your prior experience, queries the last similar campaign by asset over 28 days using the same conversion definition, opens the approved designs, and brings the evidence back. The models are interchangeable. The knowledge, the performance history and the design judgment carry to the next campaign.
---
@hiroho150cm [Claude Code]
https://x.com/hiroho150cm/status/2099256813283914128
She finally worked out why Claude Code could never copy a reference site's layout: the two pages have different elements, so matching them is impossible. Her fix is a prompt that forces measurement instead of impression. Download the reference CSS and read it rather than eyeballing the screen. Extract the media queries and confirm how many breakpoints and at what pixel values. When values are in rem, hunt the base width in the JavaScript. Open the browser at 375, 768, 1024 and 1440 and measure element positions. Match element count and order, do not invent elements the reference has that you lack, keep company name and address at your own character count but bring headings and body close to the reference's. Copy layout only, never color, decoration or motion. Then verify at all four widths before shipping, and do not settle for roughly matching.
---
@masahirochaen [Claude Code]
https://x.com/masahirochaen/status/2099272425997541391
His answer to AI-generated slide decks: let Claude Code or Codex build the structure and the copy, then do fine edits in a local tool he wrote. The reason is precise. Asking a chat interface to fix just this one spot on slide 3 forever is the failure mode, so he pulled that part back to his hands. The deck is one JSON file, which is the only thing the AI rewrites. HTML and CSS get assembled from it and rendered at 1280x720. PDF and PNG are just that HTML printed through Chromium so nothing shifts. PowerPoint alone gets rebuilt from measured post-render coordinates so the recipient can edit it. Margins, colors and type sizes are all CSS variables, so one edit realigns every deck. Lock design into CSS and content into JSON and the range you can hand to AI widens a lot.
---
@masahirochaen [Claude Code]
https://x.com/masahirochaen/status/2099062578232320259
A prompt for auditing your own harness after a model upgrade. It tells the agent to read the linked article, inspect your actual work history, current settings and folder structure, then propose an optimal environment assuming Codex and Claude Code run together. Optimize Skills and SKILL.md, AGENTS.md and CLAUDE.md, the folder hierarchy, docs and scripts, the division of labor between the two, and clear out duplicated, unnecessary and overlong instructions. Constraints: minimize context consumption, favor progressive disclosure, do not grow the skill count, do not let AGENTS.md and CLAUDE.md bloat, avoid double-managing shared rules, and only turn genuinely frequent work into skills. Audit first, change nothing, confirm the plan once, then implement autonomously to the end.
---
@tanabe_fragm [Claude Code]
https://x.com/tanabe_fragm/status/2099066699819725196
A nice small one. Seedance 2.5 can take Japanese pitch accent in the prompt, so he tested whether it would read ame as rain versus candy correctly. It does. Writing the pitch notation by hand every time is tedious, so he had Claude Code build a skill called japanese-pitch-accent that takes a line of Japanese, judges the accent nucleus in standard Tokyo accent, and returns the line with pitch notation attached in a fixed format. His own advice is to use it only on genuinely ambiguous words, not on every prompt.
---
@FernetBuehler [Claude Code]
https://x.com/FernetBuehler/status/2099145506119131388
An interview with the head of Norway's sovereign wealth fund: 70% of employees work with Claude Code, and 200 of 700 staff build their own AI agents. The fund now describes itself as a technology company. Put alongside the German pension insurer that declined to manage a state capital stock because it employs no experts in such risky investments, this is the clearest institutional-adoption datapoint of the week.
---
@grantjordan [Claude Code]
https://x.com/grantjordan/status/2099210122665095400
He owns a mid-sized company and runs his entire life through a Hermes agent on Discord. Forty tasks in parallel, coding through team management through the things only he can sign off on, and he says the free time it created is why he is starting a second business. His actual argument is a routing one and it is worth reading twice: his Hermes agent does not code, the coding harnesses code. Hermes prompts them, better than he would. Drop the requirement that you personally must use Claude Code or Codex, live through one harness that is available on every device you own, and the benefits show up.
---
@RWQBrown [OpenClaw]
https://x.com/RWQBrown/status/2099198959520514447
He uses OpenClaw as a personal trading assistant with custom tools he and it built together and uses daily. The second pattern he calls out is the one nobody talks about: OpenClaw as a family assistant. Connect you and your spouse, schedule events through it, both get updates on spending and reminders. A shared household agent rather than a personal one.
---
@DevMiddleEarth [OpenClaw]
https://x.com/DevMiddleEarth/status/2098993957787365619
He built a second OpenClaw agent purely as a news curator. It hunts the web for the news he actually wants, assembles a curated list, and posts it daily to his private Telegram channel. Current beats are football, gaming, Linux and Kerala politics. Small, non-coding, and the kind of thing that actually survives past week one.
---
@codevev [OpenClaw]
https://x.com/codevev/status/2099216256989905296
Asked what he actually uses OpenClaw for, he gives three topics set up in Telegram. Generate a daily workout based on the equipment he owns. Talk through what food is in the house and get recipes back. Daily AI summaries of what happened in the last 24 to 36 hours. This is the most honest answer in a thread full of people admitting they set an agent up and barely use it.
---
@michael_seewald [OpenClaw]
https://x.com/michael_seewald/status/2099177173340881332
He runs the OpenClaw gateway inside a Fedora LXC container and reports it handles Linux package management, systemd and GUI work competently. The detail worth noting is that he connected a macOS node for the first time and OpenClaw dropped the output files onto the macOS desktop as intended, which means the cross-machine routing actually works rather than just being configured.
---
@levelsio [OpenClaw]
https://x.com/levelsio/status/2099196383538356635
He killed his OpenClaw VPS servers months ago. Today he got a billing alert on the separate Claude account he had created just for OpenClaw. Auto-reload was off, but the key had been exposed at some point, and whoever took it sat on it for months before spending it on Fable 5.1. None of his terminals or VPS sessions use the API. He nuked the account, and notes that keeping it isolated is the only reason this was contained.
---
@balakhonoff [OpenClaw]
https://x.com/balakhonoff/status/2099228120117121247
Replying to the same incident, he says his OpenClaw leaked API keys months ago and cost him 100 dollars, so he decided never to let any agent see his API keys again and built a proxy for it, which he plans to open source. His follow-up theory on the mechanism is the useful part: on OpenRouter you do not choose your provider by default, and while OpenClaw is setting itself up it reads configs, so keys end up in LLM provider logs. He says he has found his own keys in those logs hundreds of times.
---
@eric1021945 [Claude Code]
https://x.com/eric1021945/status/2099183756607422521
Muse built him an ideas dashboard overnight: 63 ideas across two businesses, including an 18-item grants and credits tab with deadlines and checklists. The next morning he pointed his Claude Code harness at that tab. It researched 118 programs, wrote the applications in his voice, and he clicked the CAPTCHAs. Result so far: 5,000 dollars in Azure credits landed that day from Microsoft for Startups, with five more applications in flight worth 46k+. One tool drew the map, the other walked it.
---
@richhomiecon [Claude Code]
https://x.com/richhomiecon/status/2099246497493918059
He built a furniture planner for his apartment move using Claude Code, and the inputs are the interesting part: a 3D scan of the new place, a walkthrough video of the old one, and a voice memo of himself going around with a tape measure. Three messy real-world captures instead of a floor plan.
---
@egr_investor [Claude Code]
https://x.com/egr_investor/status/2098994275161919556
He rolled his own RSVP website and invitations for his toddler's birthday with Claude Design plus Claude Code plus Cloudflare rather than paying for Paperless Post, and after a few rounds of feedback from his wife they actually look good. Small, but it is the exact shape of the consumer software that gets quietly eaten.
---
@beku_AI [Claude Code]
https://x.com/beku_AI/status/2098943749888037336
His wife built an app with Claude Code. She cannot write code. He says he did not notice it happening and then the app existed. His framing is the one to keep: until recently building an app was something knowledgeable people spent days on, and now it is happening at his house.
---
@wlmiddelkoop [Claude Code]
https://x.com/wlmiddelkoop/status/2099134968576262525
His son, who lives in Roblox on an iPad, is on a Framework 12 running Omarchy typing refinements into Claude Code for a game they are building together, a Minecraft plus Flappy Bird plus Roblox steal-an-egg crossover. He later shipped it and wrote it up. The part he keeps returning to is watching the kid steer the agent.
---
@bboym0dE [Claude Code]
https://x.com/bboym0dE/status/2099213893327593734
Everyone talks about one-shotting a Call of Duty with Claude Code. His took two months and roughly 3,000 prompts. It is a browser-based battle royale with 100 mechas on one map, built on threejs plus Box3D with ARRR multiplayer infrastructure. His favorite mode is squad play, where one person pilots while teammates run different weapon systems. The honest prompt count is the contribution here.
---
@edwinarbus [Claude Code]
https://x.com/edwinarbus/status/2099222837399793686
He asked Claude Code with the Unity plugin to make a little origami game to test whether the new folding phone means you can keep folding forever. It can, sort of, with a few workarounds. A throwaway, but it is a clean example of the Unity plugin path being short enough to answer an idle question.
---
@DmitroCP [Claude Code]
https://x.com/DmitroCP/status/2099154771529846968
A summary of Boris Cherny's YC talk on how Anthropic builds Claude Code, and the method is more useful than the anecdotes. Every new model they delete the system prompt and add it back one line at a time, treating it as an ablation. Most of the old prompt was correcting behaviors the model should have had, so 80% went. There is an undocumented flag, CLAUDE_CODE_SIMPLE=1, that strips every system prompt including tool prompts, used internally as the baseline, and his finding is that the model is a little more intelligent without them. His instruction to the room: every six months delete your CLAUDE.md, your skills and your hooks, and see what the model does on its own. Add an instruction back only when it stumbles on the same thing repeatedly. The proof point: Claude Code runs on Bun, Bun was written in Zig, and one prompt plus steering plus one dynamic workflow rewrote the entire runtime in Rust, over 100,000 lines, in 11 days, now in production.
---
@DmitroCP [Claude Code]
https://x.com/DmitroCP/status/2099189212050526515
A useful companion: OpenAI published ten changes to make to your skills and prompts for GPT-6 Astra, and every one is a rule that was compensation for something the last model could not do. Cut skill descriptions to one line about when to use it, because long ones get truncated once you have many. Turn multi-workflow skills into a router pointing at sub-docs. Stop writing recipes, because overly specific guidance now hinders results. Kill the read-these-three-files-before-every-edit line in AGENTS.md. Delete instructions telling it to run tests, since it does that on its own and the nudge causes over-testing. Give explicit permission for workflows you know are safe. Revisit ask-first language written for a model with worse judgment. Define what done means up front. The through-line matches Cherny's exactly: the rule is now the bug.
---
@neil_xbt [Claude Code]
https://x.com/neil_xbt/status/2098986276737458633
The viral Claude Code setup of the month ships 68 subagents, 286 skills and 94 commands, and its own author's closing line was that installing all of it at once is the fastest way to make things worse. Most people installed all of it at once, so now every message re-reads the entire pile before a single token of the actual task.
---
@neil_xbt [Claude Code]
https://x.com/neil_xbt/status/2099139284746056103
The follow-up, and this is the part that makes it actionable: Claude Code shipped the tool that answers which of those 286 skills change anything. It runs your skill on real prompts, then runs the same prompts with the skill removed. Two scores, and the difference is what the skill actually did. He wrote the playbook around it: setup, the three cases every skill needs, the grader pair, the keep-or-cut table, and the CI gate. You can hand it to Claude Code and have it write the cases.
---
@MarMarLabs [Claude Code]
https://x.com/MarMarLabs/status/2099265249157468509
A careful, tested writeup of what a Claude Code deny rule actually is. Anthropic's own docs say Read and Edit deny rules cover built-in file tools and file commands recognized in Bash, but not arbitrary subprocesses that open files themselves. He tracked the last two releases fixing exactly that: 2.1.268 fixed deny rules not applying through a symlinked directory and being skipped when an env -C or eval sat on the same line; 2.1.269 fixed Edit deny rules not applying to the file a Bash tee writes, and fixed permission_denials in stream-json output leaving out blocked Read, Edit and Write calls. He tested the tee case on both builds: on 2.1.268 the file was overwritten and permission_denials came back empty, on 2.1.270 it was blocked and logged. His read is right: nobody turned the deny rule into a wall, they taught the checker one more spelling of write to this file. Use 2.1.270, keep deny rules for the spellings the checker knows, and turn on the sandbox for the boundary you actually need.
---
@shubh19 [Claude Code]
https://x.com/shubh19/status/2099186312700219878
He audited his last three months of AI-assisted PRs and published the numbers. 150+ auto-accepted AI suggestions. 20 memory leaks and race conditions missed. 300+ dollars burned on recursive refactors. And 100% of the PRs that improved were the ones where he explicitly told the AI no. His diagnosis is that the problem is not model hallucination, it is human passivity.
---
@itsGrizai [Claude Code]
https://x.com/itsGrizai/status/2099051766012694644
Nine hours of Claude Code on a client site came to 77 shell runs, 21 reads and 5 writes. His question is the good one, aimed at the private-repo coding benchmark making the rounds: pass rate is the wrong number, so how do you grade the 98 calls before the 5 writes?
---
@0xZenad [Claude Code]
https://x.com/0xZenad/status/2099210883578638342
Spotify said it cut Claude Code token usage by 90%. Someone rebuilt the whole setup from scratch and measured the actual bill: 59.6% less context hitting the expensive model, 33.1% lower total cost, 65% slower overall, and one small task that actually cost 2.6% more. The trick is not switching everything to cheaper models, it is keeping the expensive one out of file reads and boilerplate while debugging, architecture and real reasoning stay with the frontier model. Ninety percent fewer tokens is not ninety percent cheaper.
---
@rlaope [Claude Code]
https://x.com/rlaope/status/2099085362085953725
A properly run benchmark of a prompt layer. oh-my-hermes prepends calibration text to sub-agents spawned by Hermes, ordered from exact model to model family to general rules. Across 30 identical coding tasks: no calibration averaged 112,007 tokens, generic family blocks cut that 24% to 85,498, but the model-specific block they had been shipping logged 107,161, worse than the family block. The culprit was two phrases, include verification output in the response and report blockers along with observed output, which the model read as generate that output first, pushing tool calls from 434 to 462. Removing them and restoring make the smallest edit, verify once, and stop brought it to 77,568, a 31% reduction, with tool calls down 29%, API turns down 22% and output tokens down 36%. Pass rates stayed statistically tied at about 15 of 30, which proves the eliminated calls contributed nothing. One bad phrase cost 25%.
---
@rapidmlx [Claude Code]
https://x.com/rapidmlx/status/2099164775855079512
A correction to a common assumption about local models: one request at a time is not the limit. On an idle M2 Pro mini running Qwen3.6-35B-A3B, decode throughput went from 75.7 tok/s at 4 streams to 82.9 tok/s at 8. Doubling the load made it faster, because batching reads the weights once for all eight streams. llama.cpp was 8% down and Ollama 10% down on the same test. One Mac answers Cursor, Claude Code and a script at once.
---
@_nodelay [OpenClaw]
https://x.com/_nodelay/status/2099145739662393658
A detailed local-inference writeup. DeepSeek V4.1 Flash Vision ships 1M context, but two DGX Sparks give about 2.5M of usable KV cache, so he capped agents at a 256k software limit and got roughly 6 stable sessions; pushing to 8 started degrading decode. Qwen 3.8 Flash Next gives about 4.2M of KV cache, so 16 sessions fit comfortably at 256k. Everything is on Tailscale, delivering a steady 30 tok/s across his whole fleet: an M2 Max Studio for main development, an M4 mini for OpenClaw, a ThinkPad as control center, and two DGX Sparks for inference. Frontier models still do the building, but routine queries and connective tissue are now handled locally, which only works because he solved it locally instead of with subscriptions.
---
@keisuke_yoshiha [Claude Code]
https://x.com/keisuke_yoshiha/status/2098958732143247588
His AI agents were producing faster than he could sleep, so he made the management itself hierarchical and handed it over. A Director on Opus makes decisions, a Senior on Sonnet runs each project, researchers on Haiku do the work. Nine departments, each a Senior plus two researchers. He only talks to the Director. Daily operating cap of 5 dollars, departments idle in standby until named, and a dashboard shows every agent's status and cost live. Decisions stay human: the AI proposes, he approves, and anything that leaves the building is his call.
---
@sns_ryuto05 [Claude Code]
https://x.com/sns_ryuto05/status/2099277785214947473
One month of a fully automated account. Research and post creation all delegated to Claude Code, list at 468 people. He notes the list is smaller than he wants because the niche is not the make-money genre, but expects 800k yen from a note launch. Fifteen accounts running fully automated now, thirty planned by end of month.
---
@brainextends [Claude Code]
https://x.com/brainextends/status/2099238343074832810
He scaled his own app to 10k MRR with TikTok slideshows and published the mechanics. Three fresh iPhone 11s with USA proxies, three days warming one account per phone, meanwhile building a reference library from Pinterest for every slide type. Then Claude Code plus an image API generated a large number of original variations from those references. Day four: three slideshows, 1.6M views day one, because TikTok boosts your first-ever slideshow. One post eventually hit 5M. Day 28: 10k MRR. Getting past that became a distribution problem, so he ran a creator campaign and came back from vacation to 2,000 accounts posting his formats.
---
@AaronxShepherd [Claude Code]
https://x.com/AaronxShepherd/status/2098924981413458135
He turned the six jobs his cold email team used to do by hand into six Claude Code prompts: building the list, scoring the ICP, parsing the replies and the rest. His packaging is the instructive part, because it is what a real handoff looks like: one prompt per job with the variables marked, six sample outputs so you know what good looks like, the edit slots called out, a quick-start prompt to check your setup first, and a chaining playbook for running all six back to back.
---
@MichLieben [Claude Code]
https://x.com/MichLieben/status/2099250347063886180
A data-layer writeup for cold outreach with Claude Code doing the routing. His core claim is measured across a million-plus emails: 20-30% reply rates on 500-prospect micro-lists versus 2-3% on 100,000-contact blasts. That only works if every row is right, so he lists twelve providers and the rule for each. Write the ICP down before opening any tool, pull 50 rows and check by hand, and if fewer than 70% fit, tighten and rerun. Run enrichment as a waterfall and stop at the first verified email or mobile. Keep verified, risky and unknown as separate states, and never put unknown into a live sequence. Count funding from the last 2-4 weeks, job changes from 14-45 days, hiring from 1-2 weeks, and escalate accounts with three signals same-day. Save the source URL and pull date with every fact.
---
@x_insider4 [Claude Code]
https://x.com/x_insider4/status/2099168957152301266
An NQ futures bot built with Claude Code running live on a single contract, at roughly +900 dollars P&L. The system watches NQU6 in real time, reads the order book, tracks liquidity and executes a defined setup rather than predicting every candle. NQ pays 20 dollars per point per contract, so a roughly 45-point move on one contract is the 900. He is explicit that the design principle is waiting rather than chasing: define the logic, let the bot wait for conditions, execute, manage the position.
---
@ff14_Ninjachan [Claude Code]
https://x.com/ff14_Ninjachan/status/2098974890464514396
Small and concrete. Claude Code ran ping measurements and checked his network configuration on its own, identified the cause, then installed and connected WARP end to end. Non-coding, and exactly the shape of task people keep saying they cannot find a use for.
---
@___35d [Claude Code]
https://x.com/___35d/status/2099000882449022987
He is extending the Notion Inbox database he already uses. Tasks get an AI flag, the work description goes inside the task page, and Claude Code reads that description, decomposes it into tasks appropriately, asks the human for direction when needed, and moves the work forward. Building the environment for that worldview is the current project.
---
@gdvonly [Claude Code]
https://x.com/gdvonly/status/2099036175319068781
A podcast pipeline that is mostly not AI-shaped. He talks, hands the raw recording to Claude Code for editing and automatic posting, runs it through Pody for transcription into an article, then syndicates to note and other SEO-strong services. The point he makes is that even casual output now reliably persists in the world.
---
@kanakogi [Claude Code]
https://x.com/kanakogi/status/2098938745605255507
He shipped a Mac app called Agent Critters: a small desktop companion that shows Claude Code and Codex session state through animation. Working, awaiting approval, finished. Click it and you jump to that session's terminal. This is the second ambient-status tool in today's set.
---
@Alacritic_Super [Claude Code]
https://x.com/Alacritic_Super/status/2098954173517799904
The hardware version of the same need. Someone built a custom hardware monitor on an M5Stack that tracks Claude Code and Codex API limits in real time, connecting over Tailscale to show usage percentages alongside exact countdowns to token limit reset. It gets the tracking off your monitor and removes the surprise of being cut off mid-session.
---
@funny_man_daa [Claude Code]
https://x.com/funny_man_daa/status/2099136741563302037
And the third: Agent Tile 1.0.10. He had put 18 Claude Code and Codex sessions on one screen, one orchestrator plus 17 workers, and lost control of it, so he added tabbed boards. All 18, Admin 3, 1st 10, 2nd 5. Switching tabs only hides the tiles; the agents behind them keep running.
---
@lwastuargo [Claude Code]
https://x.com/lwastuargo/status/2098992915808678070
A compact operating setup from someone running a lot of agents. Keep a codebase to store all context, which is why he does not use Cowork. A TECHNICAL.html in every codebase that reads well for both humans and agents. An LLM gateway or multiplexer to hold many accounts and models. And the rule worth stealing: separate the models you use for development from the ones you use for operations. Development gets the expensive ones, which is why he holds 13 Codex and 17 Claude Code accounts; operations get the cheap ones. Plus an agent or script that cleans up the codebase, config, feature flags and documentation on a five-hour trigger.
---
@sgw_R_ [Claude Code]
https://x.com/sgw_R_/status/2099260252302844299
When Claude Code or Codex writes Japanese it comes out hard to read, and Gemini 3.8 Flash cleans it up well, but handed the text unconstrained it silently changes numbers and proper nouns. So he attaches the same constraints every time: do not change intent, content or facts; do not touch a single character of numbers, amounts, proper nouns, URLs or code contents; do not touch H1 or headings because SEO dies; and do not convert his deliberate assertive and noun-ending sentences into polite form. Then he runs a script afterward to verify URLs, numbers and headings are unchanged. His reason is exact: by eye you do not notice, because an amount off by one digit still reads fine.
---
@kaorika_orika [Claude Code]
https://x.com/kaorika_orika/status/2099085774738407530
A LINE animated sticker pipeline, first test, and the division of labor is clean: art drawn by hand, animation via fal running Seedance 2.5, and the work orchestrated in Claude Code on Opus 5.
---
@OrganoidsAI [Claude Code]
https://x.com/OrganoidsAI/status/2099137632986915208
A music video shipped end to end on local and mixed tooling: video from Minimax H3 on an RTX 3090, workflow run through Claude Code on Sonnet 5, upscaled separately, audio from Suno v6.
---
@0xMfox [Claude Code]
https://x.com/0xMfox/status/2099148359684546667
He had quoted a client four figures for a product video, then found the same result in a GitHub agent skill. It is not AI video generation, it is a skill for Claude Code and Codex that writes real Remotion code, so the promo gets built shot by shot in React. His explanation of why that matters is the good part: a model painting frames forgets what your logo looked like three seconds ago, but code forgets nothing because nothing gets repainted, it gets rendered from the same component. It ships 150+ prebuilt shot cards, each a named move with tuned timing and easing, plus a full 36-second promo template with ten shots, transitions and sound. His advice: start from the finished template, name shot cards instead of describing camera moves, render a rough cut before touching code, and swap out the placeholder screenshots before anyone outside your laptop sees it.
---
@KeisukeIshikawa [Claude Code]
https://x.com/KeisukeIshikawa/status/2099159091838845334
The same pattern at larger scale. video-shotcraft gives coding agents an actual motion-design workflow: storyboard, capture real product screens, animate, sync cuts to music, render with Remotion. The library is 157 shot recipes, 214 visual styles with rendered previews, 149 SFX across 16 categories, plus reusable Remotion components and a validated 36.2-second, 10-shot template. Each recipe describes what the shot is for, its energy and timing, implementation parameters and known pitfalls, so the agent composes a sequence instead of improvising every animation. Real screenshots rather than hallucinated UIs is the distinction that matters.
---
@GoSailGlobal [Claude Code]
https://x.com/GoSailGlobal/status/2098939757346918526
The step before making a video: learning to take other people's apart. reelbench-skills hit 196 stars in two days with two skills. video-shots breaks a finished piece into a per-shot analysis table with duration, shot size, camera movement and description, where cut points and durations are measured by ffmpeg and the model only judges the four things it should, against 14 quality gates. video-sync composes, with shot information cutting in sync with the footage in both landscape and portrait layouts. The nicest detail is that the analysis report is a single interactive file with an embedded player that highlights the current shot as it plays and jumps when you click one, and it opens offline. Zero npm dependencies, just node and ffmpeg.
---
@GYLQ520 [Claude Code]
https://x.com/GYLQ520/status/2099119217715089709
A skill for Seedance 2.0 prompts that exists because the model is strict and people write essays. It teaches the agent to follow the official manual: Image1 as first frame, Video1 for camera movement reference, Audio1 for rhythm. Hard limits it enforces, at most 9 images, 3 video segments, and 12 files total, because exceeding them means the model rejects the input. Ready-made structures for ads, short drama, MV and explainer, in both Chinese and English.
---
@bkdgiffug [Claude Code]
https://x.com/bkdgiffug/status/2099109337709088878
A charting skill aimed at the thing everyone complains about: AI architecture diagrams that look like a PowerPoint template of rounded rectangles. Diagram Design generates HTML plus SVG for Claude Code and Codex across 27 chart types including architecture, flow, sequence and ER. The feature worth stealing is that you hand it a website URL and it extracts the brand fonts and color palette so every diagram matches. Light, dark and editable versions, opens in a browser.
---
@Huahuazo [Claude Code]
https://x.com/Huahuazo/status/2099217801957593383
An open-source harness from Amap aimed at agents drifting off course on long jobs. LongHorizon-Harness structures the work as a three-person crew: a scheduler that only thinks about what comes next, an executor that restarts from clean context every round, and a verifier that ignores claims and goes straight to the files, logs and tests, accepting only what matches and sending everything else back. Same models, same tools, just this shell: cross-application tasks that take an hour or two went from roughly 50% to 80% completion, CLI and coding work got more stable, and token use dropped 24%. It plugs into Claude Code, Codex CLI and OpenCode, and each of the three roles can run a different model.
---
@NFTCPS [Claude Code]
https://x.com/NFTCPS/status/2098961144748904688
A tool for the day you join a company and get handed 200,000 lines. Understand Anything runs multiple agents across the project and turns every file, function, class and dependency into a clickable, searchable knowledge graph with a visualization panel. The two things he cares about are computing blast radius before a change and being able to ask which part handles login and get a semantic answer. Connects to Claude Code, Cursor, Codex and Copilot.
---
@claudecode84 [Claude Code]
https://x.com/claudecode84/status/2099057843035111552
A claim making the rounds today, reported in several places: hand Claude Code a map of the project and you get +12 points of accuracy, about 50% fewer searches, 42% lower cost and 60% less time, with no extra spend and no model change. The reasoning is plausible and worth the attention regardless of the exact numbers. On a large repo the agent re-explores the codebase from scratch every session, like a new hire being walked to the office from the train station every morning. Give it the map and the roster instead. The tool is called Graft, free and open source.
---
@0xZenad [Claude Code]
https://x.com/0xZenad/status/2099230255550755239
The context-cost version of the same argument, with two benchmarks. Public Browser, which lets Claude Code drive your real Chrome profile, used 30% fewer session tokens, 25% lower cost, 41% fewer tool calls and finished 40% faster than Playwright MCP at the same pass rate. LeanCTX took a simulated 30-minute coding session from 471.6K tokens to 77.6K, and 1.179 dollars to 0.194. His conclusion: quota is often a context problem before it is a model problem.
---
@iamrexei [Claude Code]
https://x.com/iamrexei/status/2099149506084258296
A security architecture for the personal Jarvis everyone is building. His point is that a memory folder and a be-careful instruction do not make it reliable, because once it starts remembering clients, opening browsers and invoking tools, a single error can persist for weeks. The stack he proposes: Mem0 for a long-term memory layer that retrieves relevant facts rather than the whole chat history, E2B Desktop so computer use happens in an isolated Linux desktop instead of your actual machine, AgentOps for tracing runs and costs so a loop or wrong tool call is visible immediately rather than in tomorrow's logs. Then human approval before external actions. His caveats are honest: memory can store incorrect facts, a sandbox does not secure an account you are already logged into, and logs may contain client data.
---
@0xrootRE [Claude Code]
https://x.com/0xrootRE/status/2099012954297614562
The minimal version of the same instinct: CC-Monitor, which monitors and audits every action Claude Code takes on your computer.
---
@hirataro_89 [Claude Code]
https://x.com/hirataro_89/status/2098964023882682665
A Shopify build skill being improved by an explicit loop: run the skill for real, file an issue whenever behavior looks wrong, improve the skill against that issue, run it again. He calls it a perpetual improvement engine, then immediately flags the thing most people skip. Cutting the useless parts is mandatory, because if you only ever append you end up with an ugly chimera of a skill. That applies well beyond AI.
---
@takekeepvision [Claude Code]
https://x.com/takekeepvision/status/2098970057493860504
A blunt and useful correction from someone who built his own AI writing tool with Claude Code targeting WordPress, Ameblo and note. Same tool, different results, and the difference is not the tool, it is where you put the output. On a strong domain he reached a million yen a month, conditional on the domain already being strong. The same article on an undeveloped domain does nothing because nobody arrives from search. So the order for beginners is fixed: start where readers already circulate rather than waiting on search, take a first payment there, put the same material on note where both search and readers enter, and grow the WordPress domain in parallel so the same articles become an asset later. One research pass, three destinations, and the research cost does not go up. He also says he can write 15 articles a day but 15 gets sloppy, and the moment volume becomes the goal the blog stops growing.
---
@ai_deka_airi [Claude Code]
https://x.com/ai_deka_airi/status/2098984073150730521
A careful takedown, or rather a refusal to do one, of the 22.11 million yen in a month with Claude Code claim. He read the whole article. Conclusion: no material to call it an outright lie. The poster shows sales and transfer screenshots, calls the figure revenue rather than profit, and explicitly writes that AI did not make the money, it made the time he spends writing articles. The actual structure is 42 routine tasks automated with Claude Code so the person concentrates on long-form posts, which funnel to an open chat, which sells his existing product. He even documents a failure where automation stopped for 12 hours and data went missing. The unanswered question is the right one: what was the monthly revenue before Claude Code? If it was already 20 million, the number means something very different than if it was 3 million.
---
User Voice

Delete your instructions before you add more. The strongest technical claim in today's set is that most prompt engineering is now dead weight compensating for models that no longer need it. @DmitroCP relaying Boris Cherny: Anthropic deletes the whole system prompt every model generation and adds it back one line at a time, and 80% never came back. @neil_xbt makes the practical version of the same point: the viral setup shipping 286 skills means every message re-reads the pile before a token of your task, and the new plugin eval finally measures which ones earn their place.

People want to know the cost of a task before they send it, not after. @0xZenad rebuilt Spotify's 90% token cut and found 33% lower cost and 65% slower. @rlaope ran 30 identical tasks and traced a 25% cost swing to two phrases. @itsGrizai wants to know how you grade the 98 tool calls that happen before the 5 writes. The shared complaint is that pass rate and token count are both the wrong number.

The agent can act but cannot doubt. @nian_tu41685 was told flatly by Claude Code that his hardware could not run FP4, refused to accept it, and ended up more than tripling DeepSeek's own API throughput on six-year-old GPUs. @shubh19 audited three months of his own AI-assisted PRs and found 100% of the improved ones were the ones where he said no. Both land on the same place: the model produces correct-looking work and has no mechanism for questioning its own premise.

Permissions are the feature people are actually asking for, and they keep discovering the boundary is softer than it looks. @MarMarLabs tested a deny rule against a Bash tee and watched it fail on one build and hold on the next, concluding the rule is a list of spellings rather than a wall. @balakhonoff lost money to leaked keys and built a proxy so no agent ever sees one. @levelsio found a key harvested months before it was spent. @iamrexei wants sandboxing, tracing and approval gates as the default shape of a personal agent.

The most-wanted missing product is somewhere to see what your agents are doing. @kanakogi shipped a desktop companion showing session state, @Alacritic_Super is tracking limits on an M5Stack over Tailscale, @funny_man_daa needed tabbed boards after putting 18 sessions on one screen, and @keisuke_yoshiha built an entire hierarchical org chart with a live cost dashboard because his own management bandwidth became the bottleneck.
---
Eco Products Radar

Codex — mentioned in 129 posts. The default second opinion. Today's dominant pattern is not choosing between them but assigning roles: Codex executes and Claude Code reviews, or the reverse.
OpenClaw — 144 posts. Split between people running fleets on it and people who left for Hermes. Two separate API key leak reports today.
Cursor — 48 posts. Still in almost every stack description, rarely the subject.
Hermes Agent — 44 posts. The most common destination for people leaving OpenClaw, cited for stability and self-improving skills.
MCP — 38 posts. Now assumed infrastructure rather than a feature.
DeepSeek V4.1 Flash — 22 posts. The week's price story, showing up as both a free API tier and a local inference target.
Meta Muse — 18 posts. Repeatedly noted for using OpenClaw's SOUL and IDENTITY markdown naming.
Unity — 17 posts, driven by the new official Claude Code plugin.
Grok Bot — 16 posts. Mostly as the third option in stack comparisons.
fal / Seedance 2.5 — 14 posts. The video layer in most creative pipelines today.
OpenCode — 13 posts. The open harness people name when portability comes up.
Antigravity — 9 posts, with a warning that third-party access via Claude Code or OpenClaw violates terms.
Omarchy — 8 posts, increasingly the machine people run their agents on.
Instinct — 8 posts, described repeatedly as OpenClaw for normies.
Tailscale — 6 posts. The connective tissue in every multi-machine agent setup.
