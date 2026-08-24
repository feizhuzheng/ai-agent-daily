---
title: "Super User Daily: 2026-08-24"
date: 2026-08-23
lang: en
source: https://clauday.com/article/c0f2a4b3-f0a5-4e05-8466-75f6a23aa83b
tags: ["super-user"]
---

# Super User Daily: 2026-08-24

来源 / Source: https://clauday.com/article/c0f2a4b3-f0a5-4e05-8466-75f6a23aa83b

Today's standout theme: people are pointing these agents at everything except code. A construction crew turned a phone LiDAR scan into a truck-clearance simulator, an accountant is bolting features onto MoneyForward, someone runs their whole household budget through it, and another has it recreating the Matrix lobby shootout in Three.js from an empty repo. The center of gravity has clearly moved from writing functions to wiring up systems, and the loudest complaints are no longer about intelligence but about cost, context limits, and whether you own the harness at all.
---
@nakagomeco [Claude Code]
https://x.com/nakagomeco/status/2091192048959574207
A field engineer scanned a warehouse with an iPhone Pro LiDAR for a few minutes, then had Claude Code turn that raw point cloud into an app that drives a truck through the space to check whether it can get in without hitting anything. It shows overhead clearance, side clearance and slope in real time, turns red when the truck grazes the ceiling or a beam, and even judges overhang scraping at grade transitions. You can swap between measured 2-ton and 4-ton flatbeds pulled from the drawings. This is the kind of thing that used to need a dedicated 3D CAD workflow, done on-site in the time it takes to walk the room.
---
@rimuruafi [Claude Code]
https://x.com/rimuruafi/status/2091087986041688151
He told Claude Code to "build me a company that earns passively selling 500-yen notes" and says it actually produced a working one-person operation. The framing sounds like a joke, but it captures where a lot of people are: describing a business outcome rather than a feature and letting the agent assemble the plumbing. It got thousands of likes precisely because the ask was a business goal, not a coding task.
---
@jenixo0 [Claude Code]
https://x.com/jenixo0/status/2091166248533135407
He wired TTS into Claude Code and set a wake word so he can talk to it like Jarvis, giving orders lying in bed with his eyes closed. Unlike Alexa, it tracks his room's temperature and humidity and adjusts the AC and a circulator fan at the same time. He plans to feed it vitals from an incoming Fitbit Air next. This is Claude Code being used as a home-automation brain, not a coding tool at all.
---
@liebefactory [Claude Code]
https://x.com/liebefactory/status/2091157749363270124
She runs her monthly household budget and long-term financial plan entirely inside Claude Code, with tuition, income and expenses all linked, so changing one number that came in off-forecast cascades and fixes everything else. When she says "I want to spend on this," it pushes back with a blunt "that's tight" and then helps figure out how to make it work. The value is the honesty plus the live spreadsheet logic, not any code.
---
@creditship_dx [Claude Code]
https://x.com/creditship_dx/status/2091295600478237025
He recorded a staff meeting over Google Meet with transcript and screen capture, handed the files to Claude Code and just said "make a manual." Out came an Excel document with screenshots embedded, built from a normal conversation. Turning a meeting into a documented SOP with no manual authoring is exactly the kind of tedious office work that quietly eats hours.
---
@muramar_u [Claude Code]
https://x.com/muramar_u/status/2091032087956803973
An accounting firm is using Claude to build Chrome extensions that supercharge MoneyForward and freee, the accounting software their 500-plus clients live in. The demo feature highlights negative balances in a monthly trend view, but the same method extends to cash-flow statements, consolidated closes, and hooks into e-Tax, Gmail and Chatwork. Their whole pitch is that domain experts, not engineers, can now ship these tools in minutes by pasting a page URL and describing the feature.
---
@awilkinson [Claude Code]
https://x.com/awilkinson/status/2091178899749437580
He always admired a friend's book reviews but was too lazy and distracted to do his own, so he had Claude Code build a "Bookshelf" section on his personal site. It pulls all his most-highlighted Kindle books plus any commentary he'd posted publicly in newsletters or on X and lays them out automatically. A personal content project that would have sat undone forever, shipped because the friction dropped to a sentence.
---
@mstockton [Claude Code]
https://x.com/mstockton/status/2091283454881038686
He vibe-coded a CLI tool that pulls all his X data (tweets, likes, bookmarks) and embeds it into a vector database, which then becomes a search tool an agent can call. Now inside Claude Code he asks questions about his own Twitter history, and had it surface the top 20 long-form AI posts he'd starred over three months but never read. He notes the instruction was just him rambling into MacWhisper, and it still produced a clean reading list. This is the second-brain pattern done for real with a concrete artifact.
---
@jerryjliu0 [Claude Code]
https://x.com/jerryjliu0/status/2091231519293751458
LlamaIndex benchmarked Claude Code and Codex against specialized OCR tools and raw VLMs for schema-guided extraction from complex documents. The finding: on short documents the specialized OCR tools win on cost and accuracy, but on longer documents the coding agents move close to the Pareto frontier, because they can search snippets instead of loading the whole doc and lean on prompt caching. It reframes a coding harness as a general reasoning engine that happens to be good at document extraction. Worth reading in their ParseBench appendix.
---
@LegitSeanSmith [Claude Code]
https://x.com/LegitSeanSmith/status/2091232910208897444
He argues the tedious part of engineering isn't the code, it's the devops loop around it, and that's exactly what agents can now close. He attaches credentials to a sandbox with a scoped GCP service account, spins up Codex or Claude Code with approvals bypassed, and lets it test its own changes against real infrastructure: k8s rollouts, new protocol message types, whether a new image boots with nested virt. The open question he poses is how to scale that into a fleet of credential-scoped machines building and debugging against live infra in parallel.
---
@StephanFerraro [Claude Code]
https://x.com/StephanFerraro/status/2091296035192615160
He gave Claude Code with Opus 5 a single prompt: recreate the Matrix lobby shootout in Three.js from an empty repo. It generated all the textures, sound effects and music itself using OpenAI, ElevenLabs and Suno, then self-verified with screenshots. The result was a 62-second demo passing 31 of 31 tests with a single human intervention. A useful data point on how far one prompt plus self-verification can carry a multi-asset build.
---
@keitowebai [Claude Code]
https://x.com/keitowebai/status/2091067516483453232
With almost no hand-holding he had Claude Code set itself up to drive Seedance 2.5, then auto-generate a video from the context of his own existing content, titled around a real-and-unglamorous story about reaching a 10M-yen income. The point is the agent wired up the whole video-generation pipeline off his material rather than him prompting each clip. Non-coding creative production is becoming an agent orchestration problem.
---
@eijo_AIart [Claude Code]
https://x.com/eijo_AIart/status/2091005207958462920
He built a Seedance 2.5 prompt-generation app with Claude Code and Opus 5, then used it to output a 1080p clip, saying he wrote none of the prompts himself. Instead of prompting a video model directly, he had the agent build the tool that prompts it. That's a subtle but telling shift: the leverage moves up a level to building the machine that makes the thing.
---
@ruinolab [Claude Code]
https://x.com/ruinolab/status/2091310862372090213
For his first AI music video he generated each cut locally with MiniMax H3 in ComfyUI on his own RTX 4070 Ti, so the only cost was electricity, and he automated the whole generation loop with Claude Code. The agent handled prompt design, generation and inspecting the finished frames, while he did the initial concept, the accept/retake calls and the editing. A clean division of labor where the human keeps taste and judgment and the agent runs the grind.
---
@dan__rosenthal [Claude Code]
https://x.com/dan__rosenthal/status/2091163563570118742
He's scaling a company toward eight figures with a GTM automation layer running on ten tools, and Claude Code is the piece powering the company OS and the AI agents on top of it. Around it sit Supabase for internal datasets, a vector store of winning examples as RAG, plus Clay, HubSpot and the rest of the revenue stack. It's a concrete look at Claude Code as the orchestration brain of a real go-to-market operation, not a coding assistant.
---
@donnfelker [Claude Code]
https://x.com/donnfelker/status/2091269201402925352
He can close his laptop mid-task, drive across town, open his phone, and his agents are still working, for the cost of an old laptop and an afternoon. The recipe: grab an old PC, install Ubuntu Server, set BIOS to restore on power loss, install Tailscale and firewall everything off the tailnet, then install Claude Code, Codex and the rest and run them in tmux. SSH in over Tailscale from laptop or phone and the job is right where you left it. A tidy blueprint for a personal always-on agent server.
---
@borjaperfra [Claude Code]
https://x.com/borjaperfra/status/2091093015985369460
He connected Claude Code to Cloudflare Analytics and Search Console for his product helmcode and reports doubling July's traffic and tripling page views, with US visits climbing to 13 percent. A deep-dive piece on the DeepSeek harness drove much of the international traffic, and he's using Claude Code's read of the analytics to decide what to write and where to route readers next. Content strategy run off live first-party data, with the agent as analyst.
---
@mikefutia [Claude Code]
https://x.com/mikefutia/status/2091312553167106122
He points Claude Code at his Search Console and GA4 and has it run SEO end to end: find the keywords sitting at positions 4 to 20, ship the actual rewritten titles and headings rather than just naming the problem, turn redirect chains and slow pages into ranked dev tickets, and render a live health-score dashboard as one HTML file. His pitch is to cancel the $200-a-month Ahrefs subscription because the analysis now runs on your own data. Whether or not you buy the framing, it's a real vertical workflow, not a demo.
---
@JinjingLiang [Claude Code]
https://x.com/JinjingLiang/status/2091240309837729922
For a large PR he ran roughly 20 rounds of plan and review loops before writing any implementation, then used Claude Code's /ultracode mode, which ran on its own for 72 hours. He found Claude a much better harness than Codex for changes this large because Codex tended to get lost, and split the review across 5 to 10 agents each focused on one narrow area like backward compatibility or remote-host logic, orchestrated through Orca with a mix of Claude Code, Codex, Grok and OpenCode. He dogfooded a prod build from the branch to shake out bugs. This is what serious multi-agent engineering discipline actually looks like.
---
@Ninagawa123 [Claude Code]
https://x.com/Ninagawa123/status/2091017466726261005
He had Claude Code write an episode of the manga Kochikame set around Claude Code itself, from a one-line prompt: "read me the script of the Kochikame Claude Code episode." The post drew nearly two thousand likes and over a million views, largely on the strength of how well one line reconstructed the source material's voice. A reminder that the model's resolution on a niche cultural reference is doing as much work as the tooling.
---
@wickedguro [Claude Code]
https://x.com/wickedguro/status/2091244443995357464
He spent a day trying to let agents make purchases via a crypto-based payment protocol, and on paper everything worked, but when he asked Claude Code to actually buy, its auto-classifier refused because of the flood of crypto scams. Every alternative he tried added too much friction, so he gave up and went back to another task. A useful real-world data point on where the safety classifier draws a hard line, and the friction that creates for legitimate agent-commerce experiments.
---
@amuse [OpenClaw]
https://x.com/amuse/status/2091152460651847829
He walked the full migration path: started on OpenClaw pointed at ChatGPT, moved to Hermes on a local model, then had Hermes migrate everything to Grok Bot. What took a month to build on OpenClaw and three weeks on Hermes was running in a single weekend on Grok Bot. His local-model setup needed $10K of hardware versus $300 a month, a payback of nearly three years, so for now the managed option wins. A candid cost-and-effort comparison from someone who actually ran all three.
---
@ColdMorningGrit [OpenClaw]
https://x.com/ColdMorningGrit/status/2091261284813766829
A 52-year-old framer with no Cursor subscription and no IDE ran a one-prompt, one-shot pirate-ship coding challenge on Claude Sonnet 4.6 through OpenClaw, on his own machine at home. The result is a nice counter to the assumption that this all requires a developer setup: a self-owned agent stack in the house, driven by one prompt. The build-it-yourself, own-your-stack crowd keeps showing up in exactly these stories.
---
User Voice

Context and cost dominate the conversation far more than raw intelligence. The single most repeated complaint is token burn from bloated context, terminal output and MCP responses, and the fix everyone reaches for is delegation to subagents and aggressive /clear and /compact discipline (@itsharmanjot, @sairahul1). Right behind it is the usage-limit wall: the 5-hour cap keeps pushing people to Codex, to multiple Max accounts, or to free model routers, with several predicting the underpriced era ends abruptly (@zachmoskow, @masahirochaen). Model quality is a live sore spot, with users reporting Fable 5 and Opus 5 feeling dumber, verbose or prone to unrequested over-engineering, sharpened by confusion over the server-side effort remapping (@kimmonismus, @Prathkum). A strong own-your-harness sentiment is building: people want the Claude Code harness open-sourced and their skills portable across Codex, Pi and Hermes so switching costs disappear (@omarsar0, @rohit4verse). And a smaller but pointed one: Claude Code is verbose enough by default that some find it barely usable until forced into concise or ELI5 output, and a few say Codex simply follows written instructions more reliably (@ntkris, @ahmd3ssam).
---
Eco Products Radar

Codex — the constant comparison and load-balancing partner to Claude Code; many run both.
Cursor / OpenCode — alternative harnesses named repeatedly in the switch-cost debate.
Pi — open harness held up as the model-agnostic future; 5,000+ community extensions.
Hermes Agent — self-improving, always-on agent frequently paired against OpenClaw and Grok Bot.
Grok Bot — the "just works" managed agent people keep migrating to from OpenClaw/Hermes.
DeepSeek Harness — open, everything-is-a-plugin harness cited as the commoditization threat.
Obsidian + second-brain — the Karpathy vault pattern, driven by Claude Code, everywhere this cycle.
FreeToken — UC Berkeley local inference engine letting Claude Code point at frontier open models.
Seedance 2.5 / MiniMax H3 / Higgsfield — the video-generation stack agents are increasingly orchestrating.
Ox Alpha (0x Alpha) — anonymous frontier model people are running free through Claude Code harnesses.
ELI5 skill — Anthropic's internal one-line skill that renders explanations as HTML, widely shared.
