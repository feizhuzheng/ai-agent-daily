---
title: Loop Daily: 2026-08-13
date: 2026-08-12
lang: en
source: https://clauday.com/article/ab6a0f14-e246-410a-b294-d8d63d64e449
tags: loop
---

# Loop Daily: 2026-08-13

> 来源 / source: [clauday.com](https://clauday.com/article/ab6a0f14-e246-410a-b294-d8d63d64e449) · 2026-08-12

The most useful thing posted today was a receipt. Someone spent real money benchmarking the idea everyone repeats casually, put Claude Code in a loop and let it improve your agent, against Karpathy-style autoresearch and a purpose-built optimizer, and the answer is that all three beat the baseline, all three found their best solution almost immediately, and then all three flatlined while the meter kept running. That result rhymes with everything else worth reading today: a fine-tuning agent that post-trained two production models with no human in the loop, a self-improving solver that broke a fifteen-year-old packing record on its first two dollars of compute, an Amazon agent loop that quietly ran 860 percent over budget for five months, and a growing pile of people pointing out that the keep-or-discard step at the heart of autoresearch has no statistics in it at all.

---

@jeremytian_
https://x.com/jeremytian_/status/2087222707415130335
The benchmark of the day, and it cost about $67,000 to run. He took a production-deployed enterprise AI agent, before optimization, and pitted three auto-optimizers against each other on the same starting configuration, the same dataset and the same judge, optimizing precision with a recall floor. Baseline was 0.734. Claude Code in a loop reached 0.818, Karpathy-style AutoResearch reached 0.843, and AutoAgent reached 0.877. The finding that matters more than the ranking: even with tens of thousands of dollars of compute, all three found their best solution very early and then capped out. Auto-optimizers pick low-hanging fruit and then burn money hoping to break a ceiling they cannot see. Consistent improvement needs strategic test scheduling, escaping local minima and deciding which candidates deserve continuation, not more budget.

---

@george_onx
https://x.com/george_onx/status/2087191914760098115
Two open-weight domain models shipped today where no human did any post-training. Both were built end to end by an autoresearch agent that ran the full pipeline itself: task research, data curation, eval construction, parallel training experiments and deployment. The finance model improved FinQA execution accuracy by 43.37 points, from 15.86 percent to 59.23 percent, and gained 7.81 points on BizFinBench. The healthcare model gained 11.32 points on MEDEC flag accuracy, putting it ahead of Claude Opus 4.6 and past Muse Spark on the MedHELM leaderboard. Both are Apache 2.0 on Hugging Face. This is autoresearch producing artifacts other people will actually deploy, not a benchmark demo.

---

@cognizantailab
https://x.com/cognizantailab/status/2087238121809166762
A self-improving agent broke a math record standing since 2011. A coding agent built on Claude was set loose to write and rewrite its own optimization solver with almost no human guidance beyond a benchmark to test against, and Packomania has accepted its new 27-circle packing as the record. The cost breakdown is the interesting half: the agent's very first solver, at $2.48, could already reach the record. The next $12 of self-improvement bought consistency, not capability. That distinction, capability versus reliability, is exactly the axis auto-optimizers keep collapsing.

---

@DavidFSWD
https://x.com/DavidFSWD/status/2086999880799748557
The grassroots version, running continuously in someone's room. DeepSeek Flash with pi-autoresearch, 24 hours a day for about a week, at roughly two dollars a day to find discoveries. He has also distilled DeepSeek Flash into a Qwen 3 4B model, which is now 500 steps in without a mistake. Two dollars a day is the number to sit with, because it moves autoresearch out of the category of things you need a lab to try.

---

@aintonio_dev
https://x.com/aintonio_dev/status/2087064221670314384
The sharpest methodological criticism of the day. Karpathy's autoresearch lets an agent edit a training script forever and keep whatever happens to work; Shopify's pi-autoresearch brought that loop to the terminal. Both share the same weakness: keep or discard with no science behind it. No fitness ladder, no significance test, no lineage. His skill fixes exactly that, applying genetic programming over deep learning pipelines with gated candidates, cheap fidelity runs to prune early, full fidelity only to crown champions, and permutation tests on every keep decision. He also packaged it as an agent plugin so any agent can install it.

---

@bygodgiven
https://x.com/bygodgiven/status/2087094945916035419
Explains precisely why your agent loops forever, using Codex's goal command as the worked example. Every turn, the harness injects a continuation prompt carrying your objective back in, and it keeps doing that until the model calls the update-goal tool and declares it achieved. There is no timer and no judge behind it. The finish line is a sentence the model has to be able to check. "Refactor the auth module cleanly" never terminates. "All tests in auth pass" does. Rewrite your next goal as a condition, not an essay.

---

@shmidtqq
https://x.com/shmidtqq/status/2087267062813220880
A personal assistant where the entire agent loop is 95 lines of Python on one screen, no framework in the way. The design detail worth stealing is the gate: ask a normal assistant what 17 times 23 is and it wakes the memory store, drags eight chunks of context into the prompt and bills you for all of them. This one puts a gate in front that looks at the question and declines to retrieve. Memory is three layers, facts, events and skills, in one SQLite file plus a MEMORY.md you can read like a diary. A local dashboard shows every iteration, every token and the real money spent rather than an estimate. Evals are kept separate: pytest answers whether it worked, an LLM judge answers whether it was any good.

---

@dnagabut
https://x.com/dnagabut/status/2087209735967883521
Per internal documents reported by the Financial Times, an AI project inside Amazon generated a $1.8 million bill, roughly 860 percent over budget, running undetected for five months. Two smaller ones came in $541,000 and $134,000 over. His framing is the important part: a runaway server costs the same today as it did yesterday, but a runaway agent loop calls a model priced per token, retries on failure, and spawns more calls precisely when it is stuck. The unit is small enough to feel free and the loop is fast enough that it is not. Nobody had an alert because nobody had a mental model yet for what normal looks like. Set the alarm before you set the agent loose.

---

@AlcidesTicllaCh
https://x.com/AlcidesTicllaCh/status/2087242908579557521
Kernel Forge, out of the University of Michigan, is an agent harness that stops optimizing CUDA kernels in isolation and starts optimizing the ones that actually run inside your PyTorch model. You hand it an unmodified model and example inputs. It runs the model, captures the real operators with their real shapes and arguments, groups them into concrete variants, and optimizes each variant with an agent loop: generate CUDA, compile with nvcc, run on the captured inputs, check against eager outputs, repair on failure. Validated candidates grow a Monte Carlo tree that deliberately keeps slow kernels, because a dead-end-looking candidate can seed a good revision. The output is a guarded package that swaps in generated CUDA only where it is valid and actually faster, and falls back otherwise. Honest headline: 14 kernels beat eager, up to 2.83x on softmax, but those wins land on small runtime operators while matmul and attention are already mature vendor paths.

---

@helenamy
https://x.com/helenamy/status/2087273025427079575
A worked economic argument for splitting where your agent loops run. Hosted coding products give you a whole harness around the model, repository awareness, shell access, patching, test execution, context management, and that is genuinely valuable, but you are also working inside rate limits and quotas designed around hosted frontier inference. Her split: frontier models for architecture, hard implementation decisions, audits and security-sensitive work; open-weight models on rented GPUs for bulk implementation, repetitive refactoring, test generation, long-running agent loops, cleanup and migrations. Her numbers on RunPod: an A6000 at roughly $0.53 an hour, so a five-hour session is about $2.65 and 250 hours a month lands around $132. The point is not that the cheap model is as smart. It is that some jobs need a competent model to sit there for eight hours running tests, and that job should not be billed at frontier economics.

---

@awa_omg
https://x.com/awa_omg/status/2087324110296662402
Ran Ling-3.0-tiny as an agent on an Android phone, CPU only, no GPU, no model-specific runtime, Q8_0 GGUF at about 3.2 tokens per second. The finding that generalises beyond phones: 8K context worked but 4K was better, not because reasoning got worse at 8K but because more context made every subsequent iteration of the agent loop more expensive to process. His fix was to have the harness compact what matters into a Markdown file and continue from that state, turning part of the conversation into external memory. The limiting factor is not how much context you can store, it is how much you can afford to reprocess every turn.

---

@testingham
https://x.com/testingham/status/2087323635958817214
The useful skeptic. Six months of workable autoresearch and there is no notable acceleration in algorithmic efficiency visible on public leaderboards. He is asking, genuinely, for counterexamples he might be missing. Worth holding next to the Fastino and Packomania results above, because both of those are real and neither of them shows up as leaderboard movement, which suggests either the gains are landing somewhere other than benchmarks or the loop is better at grinding known problems than at moving frontiers.

---

@YoussefHosni951
https://x.com/YoussefHosni951/status/2087075716890263934
Separates three things that keep getting mashed together, and makes the separation diagnostic rather than academic. Harness is what environment the model runs inside: tools, state, permissions, sandboxes, approvals, tracing, retries, recovery. Loop is how the agent makes progress: act, inspect evidence, update state, decide whether to continue, retry, replan or stop. Graph is how the workflow is structured: which nodes run, in what order, where branches happen, what runs in parallel, which cycles are allowed. Then the payoff: if the model cannot reach the capability or state it needs, look at the harness; if it keeps declaring success without evidence, look at the loop's verification and termination logic; if steps run out of order or branching becomes uncontrollable, look at the graph.

---

@andriibidochko
https://x.com/andriibidochko/status/2087142588256027017
Names the failure mode behind most disappointing self-improving loops: Goodhart's Law. The agent optimizes a proxy metric so hard it degrades actual task execution. Unless the evaluation harness includes out-of-band signals and execution-trace inspection the agent cannot directly manipulate, self-improvement quietly turns into automated reward hacking. His related point is that this shifts the developer's job from writing prompts to designing robust evaluation harnesses, because if your metrics are shallow the loop just accelerates the cheating. The harness is the product.

---

@butchsonic
https://x.com/butchsonic/status/2087143936313712778
The reading list behind self-evolving agents, posted in order of use: the Survey of Self-Evolving Agents; MINJA, on memory injection through conversation alone; Sakana's Darwin Godel Machine; work on self-preference in LLM judges; Who Validates the Validators on criteria drift; Manheim and Garrabrant's four flavours of Goodhart's law; LiveBench and FrontierMath; Letta's sleep-time compute; ACE with its generator, reflector and curator; SICA, the Self-Improving Coding Agent; SSGM on governance for evolving agent memory; and the 25-researcher interview study on automating AI research. If you want the actual literature rather than the thread summaries, this is the map.

---

@antpalkin
https://x.com/antpalkin/status/2087179419517354098
Frames the difference between asking a chatbot for a trading strategy and running a real loop: it writes, tests, kills and re-runs until almost nothing survives, testing 1,262 and handing back the 14 that deserve money. The more useful half is his catalogue of where each loop architecture breaks. Multi-agent debate: bull, bear and risk agent converge on the same wrong answer and hand it to you sounding certain. Maker and checker: the checker learns to agree, so you now trust output nobody really checked. Generate, verify, revise: the loop stops terminating and one strategy burns more compute than it can ever earn. Planner with workers: fifty agents, one orchestrator, and your parallel system runs in a line. Swarm with weighted voting: forty opinions, one data source underneath, all wrong at the same second. Memory: the thing that makes it improve is the thing that rots it, one bad lesson repeated forever.

---

@LukaTheFounder
https://x.com/LukaTheFounder/status/2087260938789626170
A small working multi-agent loop rather than an architecture diagram. Three bot agents: coding, QA and personal content. The QA agent ran QA on his repos, found bugs, told the coding agent to fix them, then examined the resulting pull requests and merged them if clean. The content agent is still looking for a job. This is the shape most people should be attempting first, because the QA-to-coding handoff has a natural verification step built into it.

---

@_bugmaker
https://x.com/_bugmaker/status/2087318232155722065
A routine one level up from the work: he asks a coordinator agent to audit the agent loop itself, fix the bugs in the loop and fill the gaps. The point is that over iterations the model context and behaviours drift out of date, and this keeps them current. He does not run it on a schedule; it is triggered by an observation about how the loop is behaving, or by a tool or framework upgrade. He thinks even that trigger could be automated: a technical requirement issue gets created, the coordinator fires the loop and agent restructuring, then messages running agents about the update.

---

@dakebu_cityu
https://x.com/dakebu_cityu/status/2087019152431362387
The auto-research target for formal mathematics, stated plainly: human gives high-level ideas and proof strategies, the harness retrieves the relevant formal knowledge, decomposes the proof, writes and repairs Lean, and returns a Lean-verified proof. The eventual goal is a system that proposes new ideas itself. Worth noting that verification here is free and total, which is why formal math keeps being the cleanest environment for autoresearch.

---

@sebinsua
https://x.com/sebinsua/status/2087257687713071478
One sentence with a lot in it: test-first survives inside the agent loop as valid experiment design. Before changing code, the agent writes the simplest test that demonstrates the bug, and you review that test. If it passes, its assumption about the bug was wrong. If it fails, that same test has to pass after the fix. This turns the loop's termination condition into something falsifiable rather than something the model asserts.

---

@aeterna_agent
https://x.com/aeterna_agent/status/2087061296973787525
An open-source harness you can run in a couple of commands, with the full loop wired against a toy market and a paper broker: research, reason, signal, risk, execute, observe, remember, adapt. Model choice is swappable without touching the harness, and market data, broker, memory and inference provider are all pluggable. TypeScript, MIT. Useful mainly as a legible reference implementation of a full sense-act-remember cycle rather than as a trading system.

---

@malekoo
https://x.com/malekoo/status/2087288153698648316
A concrete tool-use loop on a 30B open model that fits on a 24GB GPU. One prompt, research a newly released model and produce a technical summary as a PDF, and it handled the whole loop itself: live web search through an API, cited answers, then a PDF generation tool producing a multi-page summary. The claim being tested here is not reasoning quality, it is whether a local model can chain tools reliably enough for an agent loop to complete without babysitting.

---

@cozybearlog
https://x.com/cozybearlog/status/2087278069036052527
Notes a quiet shift in how teams pick models. Six months ago every evaluation was a leaderboard race, SWE-bench this, GPQA that, with teams swapping models monthly chasing numbers. Now the questions are about latency under load, how the model behaves after 200 turns in an agent loop, and failure modes that only appear in production. Nobody asks about the leaderboard, they ask about the tail. His read is that the benchmarks were never wrong, they were measuring something that stopped mattering, because intelligence was never the bottleneck and reliability, cost and operational predictability were.

---

@dejavucoder
https://x.com/dejavucoder/status/2087088839215263979
Running his own autoresearch blog alongside the one everyone is reading, and reports something worth checking against your own runs: Claude Opus 5 gives up fairly fast even on realistic tasks. Persistence under a long loop is a different property from raw capability, and it is the one that decides whether autoresearch converges or stalls.

---

@omsharmadev
https://x.com/omsharmadev/status/2087259982630965351
Built his own coding agent CLI from scratch specifically to understand what happens under the hood of tools like OpenCode and Claude Code: the agent loop, tool calling, provider and model management, and working with a codebase. Not a product pitch. The pattern of building the toy version to understand the real one is showing up a lot as harnesses stop being black boxes.

---

@jdjohnson
https://x.com/jdjohnson/status/2087302868067836036
The domain nobody mentions in these threads: genealogy. He points at an autoresearch project for family history as where all his expiring tokens go. Archival research is close to an ideal autoresearch target, since it is unbounded search over messy sources with cheap human verification at the end.

---

@tom_doerr
https://x.com/tom_doerr/status/2087068602948108643
A curated list of autonomous improvement loops, research agents and self-improving coding tools built in the wake of Karpathy's autoresearch. Useful as a survey of what the loop-shaped corner of the ecosystem actually contains right now, rather than what the threads about it claim.

---

Eco Products Radar

prime-agent - self-improving RLM agent for long-running coding tasks, +2,642 stars in 24 hours and #3 on GitHub trending
pi and pi-autoresearch - the terminal-native autoresearch loop, also the harness winning the cost-per-task comparisons
Claude Code - the default thing people put in a loop, and the thing being benchmarked against purpose-built optimizers
Codex - the goal command is the reference implementation everyone dissects for loop termination
Hermes Agent - the self-improving loop people report actually working on client projects
Muse Glimmer - Apache 2.0 30B agentic model running the full loop on a 24GB consumer GPU
DeepSeek V4 Flash - the cheap execution layer under most of today's 24/7 loops
AutoResearch and AutoAgent - the two optimizers that beat Claude-Code-in-a-loop on the day's benchmark
loopx - loop engineering state kernel, agent-loop agnostic across Codex and Claude Code, 4.0K stars
