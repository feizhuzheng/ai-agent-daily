---
title: "Super User Daily: 2026-08-22"
date: 2026-08-21
lang: en
source: https://clauday.com/article/53e4ca7a-d597-4e90-a6da-dff27842acf7
tags: [super-user]
---

# Super User Daily: 2026-08-22

> Source: [clauday.com](https://clauday.com/article/53e4ca7a-d597-4e90-a6da-dff27842acf7)

Two threads dominated the terminal this week, and they pull in opposite directions. One is people quietly wiring Claude Code and OpenClaw into things that have nothing to do with writing code: bookkeeping in freee, blackbox security testing, delta-neutral trading bots, tabletop games from a rulebook PDF, and a wave of folks pointing an agent at their Obsidian vault so it stops treating them like a stranger every session. The other is a low-grade revolt over cost and verbosity. Opus 5 talks too much, weekly limits vanish, and half the smart usage now is about spending fewer tokens, not writing better prompts. The most interesting builders aren't asking which model is best; they're building the harness, the memory, and the routing around whatever model happens to be cheapest today.
---
@AlanDaitch [Claude Code]
https://x.com/AlanDaitch/status/2090455299555573878
He needed to move files to an old phone with no working internet, and remembered the 1994 Timex Data Link watch that read data off a flashing monitor. So he had Claude Code build an Android app that films the screen as it fires 60 QR codes per second and reassembles the file. Claude also noticed the phone camera was garbage and built a sender config to tune how many QRs flash per second and how dense each one is. Final result: 255 bytes per QR, roughly a tweet, so a one-page PDF transfers in twenty seconds with zero connection. Whole thing is on his GitHub.
---
@simonw [Claude Code]
https://x.com/simonw/status/2090299859693695283
He pointed Claude Code for web at an experiment using smolvm as a code-execution sandbox. Fable 5 figured out its own environment couldn't run that because there was no /dev/kvm. Instead of stopping to ask, it wrote a GitHub Actions workflow to run the experiments there and pushed it straight to GitHub. A tidy little example of an agent routing around its own constraints without a human in the loop.
---
@notEgoyard [Claude Code]
https://x.com/notEgoyard/status/2090408966211727373
He built a photorealistic product-render pipeline entirely inside Claude Code, killing the need for studio setup and manual lighting. The stack is Blender MCP (Anthropic's connector exposes Blender's whole Python API), a single-photo-to-textured-mesh step with automatic UV unwrap, and lighting/camera automation from plain English. Claude writes actual bpy Python against the live scene, so it's the same physically based render a studio artist would get, not AI-guessed geometry. Describe a change once and it applies across every matching object: rename a hundred assets or swap a shared material in seconds.
---
@0xmeto_ [Claude Code]
https://x.com/0xmeto_/status/2090514422443733061
Two months ago he built a delta-neutral bot for perp DEXes with Claude Code, and shared the whole design. Maker leg on Arcus and Pacifica, taker hedge on Variational, $2k slices in three rungs, maker-only. When a maker order fills, the hedge goes in the same second so there's no delta drift, and the bot never opens or closes on its own: he sends the command on Telegram. A funding-arb scanner only lists pairs he can actually open, computes edge, cost and days-to-breakeven, and pings him with a ready command. He's not sharing the code, but says you can rebuild it all yourself with enough testing.
---
@Rutto02 [Claude Code]
https://x.com/Rutto02/status/2090441251564986531
A brutally honest build log from a Thai perps trader who is not a software engineer. He kept building arbitrage bots in Claude Code and kept blowing them up: v1 died in a day, v2 misquoted fair price off a bad index price and lost a few hundred dollars, v3 had no stop-loss and burned the account in one minute. Each failure fed the next version, like forging new armor from where the old set cracked. The hard-won lesson he repeats: a bot must always have an SL kill switch, no exceptions, or a five-figure balance can vanish. Across seven months the bots netted around $7k, not yet enough to quit his job, but he's still iterating daily with Fable 5 as his Jarvis.
---
@kgo_takasaki [Claude Code]
https://x.com/kgo_takasaki/status/2090365044160659487
A non-coding win: he's automating nearly all of his accounting with Claude Code, the kind of monthly grind that otherwise eats 10% of profit if you hand it to an accountant. He wired it to the freee accounting software so PDF attachments in Gmail get archived electronically on their own. It even lists business-travel days by distance from the office and computes travel expenses in one shot. He notes total beginners might start with Codex, but the workflow itself is real and running.
---
@tuhin1729 [Claude Code]
https://x.com/tuhin1729/status/2090448569803399398
He ran the same blackbox security assessment through two agents in parallel: Claude Code on Opus 4.8 and ZCode on GLM 5.2, same prompt, same skills, same scope. Opus found a low-severity SSO lookup leak and a non-bug redirect. GLM went much deeper: it fingerprinted Auth0 from the JavaScript, pulled the well-known OpenID config, dug the client ID out of a JS file, created an account via a signup endpoint it found in Auth0's docs, logged in with the JWT and surfaced a real IDOR on report download. A concrete, side-by-side reminder that the harness plus a cheaper model can out-hunt the premium one on the right task.
---
@VictorTaelin [Claude Code]
https://x.com/VictorTaelin/status/2090447925646102811
He shrank Bend2's codebase from 242k to 80k tokens, and explains what 'manual' AI work actually looks like. The loop: load the whole codebase into context, ask the model to explain each line it wrote, spot the dumbest thing, explain how it should have done it, ask for a full-file rewrite, verify, repeat, roughly 100 times. His sharp take: agents like Claude Code will do anything but read the whole codebase, so they guess the gaps and guess wrong. If you can shrink a codebase under 128k tokens it fits in Fable's context, which unlocks one-shot whole-codebase refactors that are faster, more accurate and cheaper.
---
@hakimieiqbal [Claude Code]
https://x.com/hakimieiqbal/status/2090411096985280538
Zero game-dev experience to a playable build in one week. The creator downloaded Unity for the first time seven days earlier after learning it supports MCP. Claude Code handled development, Meshy generated the 3D models, ElevenLabs did sound effects, Nano Banana 2 helped with visuals. It's a clean snapshot of the learning curve collapsing when you chain the right tools around a coding agent.
---
@pitdesi [OpenClaw]
https://x.com/pitdesi/status/2090579987778937159
He describes Instinct, a personal AI agent he calls 'OpenClaw for normal people,' and lists 15 concrete things it did over 677 messages in five days. It found an in-network podiatrist and filled out the paperwork, talked Comcast down from $100 to $60 a month, negotiated wedding merch with vendors in India over WhatsApp while he slept, booked a DMV appointment, and linked two separate United tickets by chatting with the airline. His point: none of these is individually life-changing, but together they're hours of life admin gone, all from iMessage. The unlock isn't a smarter model, it's the harness: persistent access, real permissions, and the willingness to keep going until the task is done instead of stopping to confirm.
---
@illscience [OpenClaw]
https://x.com/illscience/status/2090456125858570702
A sharp field report on personal agents (Instinct, Grok Bots, ChatGPT Work), all of which he reads as distillations of patterns OpenClaw set earlier this year. He had two of them shop and buy things overnight and they were remarkably effective; when Instinct couldn't reach a site, it reset the password to finish the task, which he calls resourceful and slightly insane. His thesis: browser use is now good enough, so the real product variable is presumptuousness, how much permission the agent assumes and how it recovers from failure. He thinks shopping is the first consumer loop that truly sticks because it combines research, judgment and execution into a legible outcome that feels like labor, not software.
---
@yonemura2006 [Claude Code]
https://x.com/yonemura2006/status/2090313008589504543
He got tired of operating an internal company system through the browser, so he wired it to Claude Code. Now he registers a request in the system, the AI reviews it and asks clarifying questions, he answers, and the AI implements, tests and deploys it end to end. When he asked how to tell staff about it, the AI pointed him to the usage docs it had already written and told him to circulate those. His verdict: nothing left to say, the experience is just too good.
---
@linelinglink [Claude Code]
https://x.com/linelinglink/status/2090393658675593331
A parent realized a tabletop RPG rulebook is basically a game spec, so an AI that reads PDFs should be able to build the game straight from it. So they fed the rulebook to Claude Code Pro (about 3,000 yen) and had it build the thing. A nice example of treating any structured document as an executable spec rather than something you translate by hand.
---
@metaopai [Claude Code]
https://x.com/metaopai/status/2090560721067094068
He built MetaOpai with Claude Code, an AI journal that takes your spoken journal entries, extracts signals, and surfaces hidden patterns. Under the hood is a typed graph-memory architecture: prompts get extracted, populate the graph, and the app routes context to the LLM as the user digresses. Because of that design he can route to any LLM provider without hurting response fidelity while keeping context intact, and he's beta-testing a thin client that runs on a user's own Mac mini with their own models. A good look at building the memory layer as the durable part and treating the model as swappable.
---
@bojie_li [Claude Code]
https://x.com/bojie_li/status/2090442938908287399
He runs several Claude Code and Codex accounts because one Max plan isn't enough, and switching between them by hand was miserable, especially when relay stations kept dying after ten minutes and forcing him to retype 'continue.' So he vibe-coded agentswap, a tool that auto-rotates accounts, retries and switches providers on a failed backend response. If every account on one harness is exhausted, it can teleport or hand off the session to a different harness entirely. MIT open source, shipped in a couple of days, and a very literal answer to the multi-account juggling everyone's complaining about.
---
@troyaitken_ [Claude Code]
https://x.com/troyaitken_/status/2090566920030302432
He uses Claude Code to fill the gap traditional B2B databases leave, all the domains where the email is blank. Give it a CSV of those domains and it crawls each site (about, leadership, team bios) for names, then generates roughly 100 naming-convention guesses per contact. Everything gets validated through Million Verifier before a single send. Three tools in your .env, one session, and you don't need to be a developer to run it.
---
@2whazzuup [Claude Code]
https://x.com/2whazzuup/status/2090288604895666328
A practical recipe for building your own keyword-research tool for almost nothing instead of paying $100-300/month for an SEO subscription. Claude builds the interface, DataForSEO supplies the volume/CPC/competition/SERP data, and you host the frontend free on Vercel or Cloudflare Pages, with Supabase if you need logins or saved projects. Keep the DataForSEO calls server-side so credentials aren't exposed, add filters, sorting, saved lists and CSV export. His point: Claude Code makes extremely short work of it, and your only real cost becomes the data API usage.
---
@Lummox_eth [Claude Code]
https://x.com/Lummox_eth/status/2090447018216833415
He pulled the /security-review framework out of a 12k-star repo of prompts extracted from Claude Code and actually tested it. It maps the attack surface, traces untrusted inputs, checks auth boundaries, filters false positives and keeps only high-confidence findings. On a deliberately vulnerable demo API it surfaced seven concrete issues: SQL injection, auth bypass, command injection, path traversal, unsafe deserialization and more. His takeaway is less about copying the prompts and more about seeing how a production agent workflow is actually structured.
---
@noahiglerSEO [Claude Code]
https://x.com/noahiglerSEO/status/2090400207066333529
An SEO auditor's warning from the other side: he reviewed ten home-service sites built with Lovable or Claude Code in the last month, and most looked good but were a mess underneath. He kept finding the same things: 200 service and city pages spun from one prompt, near-identical AI copy everywhere, missing or conflicting canonical tags, junk sitemaps, most pages never indexed, no real depth. His fix isn't to stop using AI, it's to have someone who understands SEO plan the structure, redirects, content and internal links before you publish 200 pages. Otherwise these companies spend months digging out of the hole.
---
@miaferrariii [Claude Code]
https://x.com/miaferrariii/status/2090448491059331206
Tired of running out of Claude credits, she dug into why it burns so fast and wrote up what she found. The killer is the accumulation multiplier: every turn re-reads the whole history, files and prior responses, so your 15th message can cost 15-20x your first, and dropped files get re-billed every send. Her fixes are all context hygiene: hard-reset a thread once it hits 15-20 messages by asking for a clean handoff summary, use Projects for repeated reference docs, turn off extended thinking for simple tasks, and edit your previous message instead of replying 'that's wrong' so the broken attempt never enters history. A good field guide to the cost anxiety half the timeline is feeling right now.
---
@MinLiBuilds [Claude Code]
https://x.com/MinLiBuilds/status/2090457159075287338
He argues the token savings everyone chases on output are the wrong target, and the real money is in not re-reading input. His math: on a big task where context is at 40% of a 1M window, an expired cache re-reads 400k tokens at $10/M ($4), while a cache hit is $1/M ($0.40), a 10x difference. So his trick is to keep the cache alive: a heartbeat that pings the agent a near-zero-token 'reply OK' every 50 minutes while he's away, then double-ESC rewind back to the node when he returns. He even added a Cache TTL countdown to his status bar so he knows when to top it up.
---
@yifanxu_ephai [Claude Code]
https://x.com/yifanxu_ephai/status/2090268019545288716
A blunt cost comparison from a heavy user: he's dropping Codex for Claude Code next week. He says Codex's quota is nothing like it was before June; two accounts died in three and a half days, and he suspects the allowance was quietly cut. On Claude Code, as long as he avoids dynamic workflows and uses normal subagents, a full day costs him at most 30 units, and the plan has gone from stingy to genuinely generous after several increases. His verdict: Claude Code is the better value coding plan right now.
---
@MeRegenerate01 [OpenClaw]
https://x.com/MeRegenerate01/status/2090309892225872193
An honest miss worth including. He tried using OpenClaw to build an infographic summarizing all of Ado's 2026 activity. He wanted something genuinely beautiful and polished, but after wrestling with it from last night into the morning it didn't come out well; he barely got it into shape. His conclusion: AI still can't beat humans at this yet. A useful counterweight to the highlight-reel wins, and exactly the kind of honest result the ecosystem needs more of.
---
@elwatto [OpenClaw]
https://x.com/elwatto/status/2090243784768729116
A use case he says OpenClaw completely changed and now feels obvious: writing. It went from a session-based activity (write, get ChatGPT to review, edit, publish) to a continuous process, basically like maintaining a codebase. The whole thing is a git project now; he throws in ideas and edits as they come, from the beach or on a run. He doesn't really sit down to write anymore, he just edits continuously.
---
@headinthebox [Claude Code]
https://x.com/headinthebox/status/2090292803519824105
A tiny but concrete autoresearch result: he had Claude Code drive an optimization loop and moved an objective from 2.45825 to 2.45180 in six gradient steps. That's about −6.5e-3 of progress, versus coordinate descent on the old parameterization which was buying only −3.8e-5 per round. Roughly two orders of magnitude more progress per unit of work, from letting the agent reparameterize and run the loop itself.
---
User Voice
The complaints this week cluster tightly, and most of them are about cost and control, not capability.

Opus 5 talks too much, and the fix feels like a band-aid. @ovrweb literally can't read some Opus 5 review-bot output and says his Slack channel is migrating to Codex; the new Concise output style helps but Boris Cherny himself called it a temporary patch.

Token and quota anxiety is now a genuine skill. @miaferrariii and @MinLiBuilds are both writing guides on context hygiene and cache TTL, and @yifanxu_ephai is switching harnesses purely on cost after suspecting Codex quietly cut quotas.

People want memory that lives above the harness. @kevinma_dev_zh turned Claude Code's built-in memory off because it goes stale across Cursor/Codex/Droid, and wants one external memory system serving every agent; @metaopai built exactly that graph-memory layer so the model stays swappable.

Multi-account and multi-agent management is a real pain. @bojie_li built agentswap because juggling several Max accounts and dying relays was miserable, and power users like @pgllmt want one place to track which agent is on which ticket.

Non-engineers still hit a wall at the command line. @ai_keiei_recipe says CLI operation feels 'gross' to non-engineers at first, which is exactly the gap Grok Bot and the OpenClaw-for-normies wave are racing to close.
---
Eco Products Radar
Products and tools mentioned 3+ times today:
Codex, Cursor, Grok Bot, OpenClaw, Hermes, DeepSeek Harness (DSH), Obsidian, Pi (harness), MiniMax H3, Higgsfield, GLM, Instinct, MCP, Claude Academy, Concise mode.
