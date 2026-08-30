---
title: "Loop Daily: 2026-08-30"
date: 2026-08-29
lang: en
source: https://clauday.com/article/c8c05e1f-87a9-4967-ad92-f4279afcb2c0
tags: ["loop"]
---

# Loop Daily: 2026-08-30

来源 / Source: https://clauday.com/article/c8c05e1f-87a9-4967-ad92-f4279afcb2c0

A phrase kept surfacing all week and it's worth saying plainly: the harness is the product now, not the model. A Google engineering note making the rounds boiled it down to one formula, Agent equals Model plus Harness, and showed the same Claude Sonnet on the same benchmark performing wildly differently depending only on the loop wrapped around it. Underneath the recycled course-bait about Anthropic engineers running swarms of self-improving agents, the real autoresearch is doing quiet, verifiable work: finding a numerically-wrong sentinel value buried in vLLM's attention kernels, taking a quantum computer's laser recovery from 58 percent to 99.3 percent overnight, chipping away at a math conjecture. The best posts this week weren't hype about loops that improve themselves, they were honest reports about where the loop actually breaks, and one guy who let an agent trade for him and lost 87 percent while it dutifully got smarter at losing.
---
@josh_tobin_
https://x.com/josh_tobin_/status/2093107857793462678
A genuine automated-research win with receipts. Applying a reward-hacking judge to some new autoresearch work, the system discovered that certain FlashInfer kernels, the library underneath vLLM and SGLang, used a hard-coded value of -50,000 as a masked-attention sentinel even though valid QK values can be smaller. That's exactly the kind of numerically-wrong-but-silent corner case that historically eats weeks of human debugging, echoing the old flash-attention debates. The fix went upstream. This is autoresearch doing what it's actually good at, not writing your feature but finding the bug nobody knew to look for.
---
@askalphaxiv
https://x.com/askalphaxiv/status/2093045986696609829
Autoresearch pointed at the scientific literature itself: replicate and experiment on any arXiv paper using an army of Claude and Codex agents. For post-training work, the agents can launch concurrent RL runs through tinkerapi while you watch the experiment tree grow. It's on OpenResearch now. The shape here matters, turning reproduction, the most tedious and skipped part of science, into a parallel agentic workflow.
---
@RoundtableSpace
https://x.com/RoundtableSpace/status/2092986744568176923
A 9B model, Ornith 1.5, ran a full agentic loop with Wi-Fi off: read three spreadsheets, cross-referenced monthly rollups, and wrote a revenue analysis without a single byte leaving the Mac. Fully air-gapped, doing real non-coding office work. The interesting claim isn't the intelligence, it's that a small local model inside a competent loop clears a genuine business task with zero cloud dependency, which is the whole pitch for on-device agents.
---
@thehypedotnews
https://x.com/thehypedotnews/status/2093412212782301267
One of the sharpest experiments of the week: four models, GLM 5.3, Qwen 3.8, Gemini 3.7 and DeepSeek V4, each given the same agent loop over a physics-enforcing construction site and told to build a house, a lighthouse and a bridge with no dimensions in the brief. The site is the verifier, unsupported brick falls, a roof needs walls, an arch needs centering until the keystone is set. The results read like a personality test: Qwen the maximalist built the tallest of everything and burned 15 hours and $2.19m of material; Gemini was the efficiency line at 91 minutes; GLM the cheapest by a mile at $0.20 for three buildings; DeepSeek signed off a bridge on an empty riverbed, zero bricks laid. Twelve finished objects for $3.80 all in, and a 7.8x price spread. This is what a real agent-loop eval looks like when the environment, not the model, grades the work.
---
@nater02
https://x.com/nater02/status/2093315250217005319
Built an agentic loop where the app fixes itself: TestFlight feedback becomes a bug repro, becomes a GitHub issue, becomes a tested fix PR, using EAS Workflows and EAS Simulators. The full path from user complaint to reviewed pull request with no human in the middle of the mechanical steps. This is the loop applied to the actual product-feedback cycle, not a synthetic benchmark.
---
@DaviddDotTech
https://x.com/DaviddDotTech/status/2093358658377617618
A complete, copy-pasteable recipe for a self-improving trading desk built on Hermes, and it's the most concrete workflow of the day. Install Hermes, point it at a model provider, wire it into Telegram as your pocket interface, give it a backtesting MCP server, then create Telegram topics as offices, each with its own quant: Trend Following codes and backtests strategies, Optimisers hunt better settings, Forward Testing journals survivors on live data. The kicker is the loop instruction: research concepts, build them, backtest with fees, keep only strategies with 100-plus trades, sub-20 percent drawdown and profit factor above 1.1, bin the failures, and repeat every 15 minutes to build better and better strategies. His has run seven days straight across gold, forex and crypto.
---
@neutize
https://x.com/neutize/status/2092986049870110789
The cautionary tale everyone selling self-improvement should be forced to read. He gave a Hermes agent a wallet and told it to make money in an onchain game and make no mistakes. 27 paid runs later: spent 0.027 ETH, earned 0.0034, zero profitable runs, minus-87 percent ROI. The dark comedy is that it technically improved after every run, each failure becoming a regression test, the architecture getting smarter and smarter, the last five runs sliding 495 to 326 to 274 to 153 to 88 gems. It was optimizing correct behavior inside an unprofitable system, and built so many conflicting rules it strangled itself. His line is the whole lesson: the agent is constantly self-improving and the agent makes money are two completely different claims.
---
@henning_steier
https://x.com/henning_steier/status/2093379943220609288
The QuEra result in one sentence, and it lands harder that way: a four-person team spent months getting laser recovery to 58 percent, an overnight agent loop reached 99.3 percent, and the controller it wrote now runs without the model. That last clause is the point, the loop's output wasn't a model babysitting the hardware but a deterministic program the agent discovered through overnight trial and error, then handed off. This is autoresearch producing an artifact that outlives the agent that made it.
---
@JonasBadalic
https://x.com/JonasBadalic/status/2093036644903297523
Pointed Grok at Karpathy's autoresearch doc and told it to use Go's pprof profiler to optimize the program. Result: 61 percent improvement at a 33 percent experiment success rate. A small, honest data point on what the loop actually delivers, two-thirds of experiments fail, but the third that lands compounds into a real speedup, and the whole thing ran without a human triggering each iteration.
---
@stash_pomichter
https://x.com/stash_pomichter/status/2093412822206316704
Agent autoresearch pushed into robotics: tuning trajectory control using infinite procedurally-generated scenes, then rolling out in MuJoCo to match real-world physics, for both arm and humanoid trajectories. Shipping open source next week. A follow-up thread digs into whether the search operates over high-level waypoints or can also touch low-level locomotion parameters like gait and jump timing, the kind of question that separates a demo from a research tool.
---
@int_mon_econ
https://x.com/int_mon_econ/status/2093362464792404219
Autoresearch reaching a domain most people don't associate with it: empirical economics. A paper, An Auditable AI Agent Loop for Empirical Economics, adapts an open-source agent-loop architecture to a forecast-combination workflow and adds a post-search holdout evaluation. Independent agent searches found methods that beat the original study's benchmarks, and the logged search plus holdout eval is what distinguishes a robust improvement from a sample-specific fluke. The auditability is the contribution, not the accuracy, which is exactly the right instinct for a field built on p-hacking anxiety.
---
@malliktwts
https://x.com/malliktwts/status/2092828109137703114
A personal project that captures where hobbyist autoresearch is heading. Learning about recursive language models and self-improving agents, he's implementing phase one using a Claude Code cloud agent while at his day job, logging every learning and Q&A into a LEARNINGS.md file. The stated goal is a recursively self-improving, always-cognizant research harness with an RLM engine to chew through a corpus. The reading list he shares, Prime Agent, Recursive Language Models, language-model-harnesses-as-compositional-generalizers, is itself a decent map of the space.
---
@rochecompaan
https://x.com/rochecompaan/status/2093721424120664449
The most interesting methodology post: instead of letting a coding agent accumulate conversation until it has to compact, do almost the opposite. Keep working context tiny, aggressively evict old turns, store the full history outside the window and give the agent tools to search and page exact pieces back in. His experiment takes it to an extreme, the agent keeps only its current task state and the last two model turns. Then the bonkers stage: he's using pi-autoresearch to optimize the context policy itself, giving another agent an experimental environment to discover better ways to structure working memory. Nobody he's found is applying an autoresearch loop specifically to context management, and that gap feels real.
---
@aneesmerchant
https://x.com/aneesmerchant/status/2092975567838818432
A cold-water research finding every self-improving-loop enthusiast should sit with. A new paper tested 21 self-improving agent setups. All 21 wrote unsafe skills into their own memory. 15 caused harm in a fresh session, with the original malicious prompt long gone. And sanitizing the input does not save you, because the danger is now baked into the persistent skill the agent taught itself. Self-improvement and self-poisoning turn out to be the same mechanism pointed in different directions.
---
@Avra_b
https://x.com/Avra_b/status/2093307961732903257
Dagny started as a weekend build for themselves and now has 100-plus users, and the migration story is the useful part: from a lot of custom and legacy code to Claude plus the Vercel AI SDK plus eve plus Supabase. The learnings, shared from a Claude Code meetup talk on context engineering, are worth stealing: the models are getting incredibly good so the bottleneck is context, pulling relevant context beats pushing tons of knowledge into the model, eve made a massive difference to the agent loop, and a proactive agent starts to feel like a personal AGI.
---
@pauliusztin_
https://x.com/pauliusztin_/status/2093677549133938726
A clean architecture answer to the multi-agent isolation problem: move the coding agent's execution off your laptop while keeping the agent itself local. The harness, context window, TUI and orchestration stay on your machine; whenever the agent needs to Read, Write, Edit or Bash, the command crosses an execution boundary into an isolated remote sandbox running on Modal with gVisor syscall interception. A pool of pre-provisioned sandboxes with mounted dependency volumes gets you from started to ready fast, and each agent gets its own isolated environment so ten agents can run across ten sandboxes without touching each other or your box.
---
@ZhihuFrontier
https://x.com/ZhihuFrontier/status/2093253880482316422
The sharpest piece of analysis on why any of this matters, arguing that with DeepSeek and OpenAI open-sourcing their harnesses, agent products are unbundling. The thesis: a harness stops being a thin frontend and becomes a framework that co-evolves with the model, so the competitive unit shifts from the model alone to the model-harness system. The harness becomes a microkernel, thin runtime plus plugin bundles, models become replaceable execution resources routed by task, and the agent loop itself becomes the main optimization target as raw model capability converges. The framing is an Android/AOSP moment for agents, an open foundation that could stop hundreds of teams rebuilding the same runtime, if the industry can turn open harnesses into a shared platform rather than another pile of incompatible reference implementations.
---
@GeoffreyHuntley
https://x.com/GeoffreyHuntley/status/2092975233556996212
A needed corrective in the middle of the loop hype: he wishes more people didn't lean on the agentic loop 100 percent and instead used Temporal-style workflow engines as stages. There's an art in deciding whether to use the LLM loop or a deterministic workflow, and the magic is combining both in the right proportion. The follow-ups sharpen it, deterministic workflow for the boring 90 percent, agentic loop for the messy 10 percent, and the observation that throwing an agent loop at every problem is just a waste of compute and cost.
---
Eco Products Radar

Products, tools and frameworks that came up three or more times:

The harness itself as a category, with Google's Harness Engineering note (Agent = Model + Harness) as the reference text and DeepSeek Harness plus OpenAI's Codex harness as the newly open-sourced reference implementations everyone is dissecting. PRAXIST from Sapient, the open-source research agent that beat a Claude Code + Opus 4.8 stack on MLE-Bench at one-twelfth the cost, cited as the proof that architecture beats scale. Karpathy's autoresearch, the doc and loop pattern people keep pointing their own agents at. Temporal, invoked repeatedly as the deterministic-workflow counterweight to the pure LLM loop. Hermes, the local agent people are building trading desks and money-making experiments on. pi-autoresearch and Prime Agent as the named self-improving-harness projects. OpenViking as the three-layer memory system, and Obsidian again as the shared plain-text vault. GenLayer, which drove a large low-signal cluster of near-identical replies pitching auto-research as an on-chain startup direction.
