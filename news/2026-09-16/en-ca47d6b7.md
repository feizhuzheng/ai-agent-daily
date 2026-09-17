---
title: "Loop Daily: 2026-09-17"
date: 2026-09-16
lang: en
source: https://clauday.com/article/ca47d6b7-8678-4ac9-b983-6f76f028a8cf
tags: [loop]
---

# Loop Daily: 2026-09-17

> 来源 / Source: https://clauday.com/article/ca47d6b7-8678-4ac9-b983-6f76f028a8cf

Two results in one window put recursive self-improvement on firmer ground than any essay this month, and neither of them touches the weights. A swarm beat state of the art on a public benchmark in three days by building a harness over a graph database where each iteration learns how to do research better, not just how to do the task. And Google published a method where the models stay frozen entirely and what improves is the search: record every discovery into a tree, turn the tree into a replay simulator, then dream up thousands of better strategies offline at zero cost, for 162x fewer compute calls. Against that, the loop's own failure modes got named unusually precisely today. A month of an agent grading its own output collapsed the moment one external eval was added. The same model scored dramatically differently across three harnesses, and the low reasoning setting burned more tokens than medium while scoring worse. Memory is where auto-research keeps dying, because a finding written on Monday still reads like gospel on Friday after its source changed. And the most quoted line of the day belongs to the harness layer rather than the model layer: everything is now a swappable plugin, including the loop itself.
---
@hyperparticle
https://x.com/hyperparticle/status/2099861544481731058
They pointed a swarm of agents at Karpathy's NanoChat benchmark and beat state of the art in three days. The part worth copying is not the swarm, it is the harness they built on top of a graph database to do auto-autoresearch, where every iteration learns from the previous one's mistakes about how to do research rather than only about the task. The team wrote more than 15,000 entries into it. This is the clearest demonstration this window that the outer loop, the one that questions the recipe, is where the gains now are.
---
@thtbee_
https://x.com/thtbee_/status/2100205546146247066
Google's Dream-RSI is recursive self-improvement of a kind almost nobody was watching for, because the models stay completely frozen. What improves is how the agent explores. It records every past discovery into a tree, turns that tree into an offline replay simulator, then dreams up thousands of better search strategies by replaying its own history at zero cost, picks the best, deploys it, and the richer history produces a better simulator and better strategies. 162x fewer compute calls than existing systems, 2x performance on GPU kernel tasks at equal budget. The second-order point is the one to sit with: the GPU kernels it finds make training infrastructure faster, so the loop that does not touch the model still feeds the loop that does.
---
@michael_kove
https://x.com/michael_kove/status/2100223367332663458
The right sceptical question about Dream-RSI, asked plainly. It maintains a local cache of its own history and does not update weights, so how is that different from what most agents already do, and is a self-improving skills system not the same claim? Worth holding next to the 162x number, because the distinction between a better search policy and a better model is exactly the thing the current RSI discourse keeps collapsing.
---
@MaryamMiradi
https://x.com/MaryamMiradi/status/2099587552894173492
The best architecture post of the window, and it names the flaw in most self-evolving agents in one line: the agent proposes a change, tests it, and decides it worked, which is an agent grading its own homework. The paper it draws on separates the two jobs, with the model deciding what evidence to acquire next and deterministic components deciding what that evidence proves. Seven steps: fix the task, metric, boundaries and allowed evidence first so success cannot be quietly redefined; diagnose the bottleneck before changing anything; state a falsifiable hypothesis with a rejection condition; change one axis at a time; put an independent evidence gate in front of the verdict; store negative results so repeated failures lower the priority of similar actions; and freeze the winning configuration before certifying it against untouched evidence. Across 22 heterogeneous scientific tasks it reached a 96.77 task-normalised score with 72.2 percent less cumulative fitting time.
---
@Marko_Poly
https://x.com/Marko_Poly/status/2099591011186139226
He let an agent loop grade its own output for a month and it looked great. Then he added one external eval to decide whether run two ships, and his success rate dropped from something he had been bragging about to something honest. The model was marking its own homework. The eval costs him about fifteen minutes a day and some ego, and it is the only reason he now trusts overnight runs. His question at the end is the right one to steal: what is the smallest eval that actually changed how much you trust your agent?
---
@Oluwaphilemon1
https://x.com/Oluwaphilemon1/status/2100037551373308192
He ran the same model, Qwen3.8-27B, through a minimal SWE agent, Claude Code and Pi, and the scores moved dramatically. With vanilla Pi it performed poorly on the benchmark, and after tuning and iterating on the Pi setup it beat the reward score from Qwen's own published run using Claude Code. Same weights. The second finding is the one nobody expects: lower thinking was not more efficient, because the low setting used more tokens and more turns than medium while scoring worse, since the model compensates by taking more actions. His conclusion is that agentic coding benchmarks are not model benchmarks, and a score without the configuration behind it hides most of the story.
---
@sunsetsyntax
https://x.com/sunsetsyntax/status/2100045108779401645
An independent confirmation of the same thing from local runs: same weights, different harness, completely different software-engineering outcomes. He names the specific parts doing the work, which is tool policy, retry behaviour and context hygiene, and says the loop is doing more than people admit.
---
@irastech
https://x.com/irastech/status/2099707117695381542
The bluntest version of the harness-over-model claim in the window: they swap open and closed weights weekly and reliability barely moves, while the harness does. If you only read one line on benchmark methodology this week, this is it.
---
@CoreyGallon
https://x.com/CoreyGallon/status/2099976426577355199
A production report from Maersk that is more useful than most agent papers. He calls the problem a tribal dungeon: operational knowledge that is real and already proven safe to run, but trapped in a form no agent can execute, because legacy SOPs are screenshots of what a person clicks rather than a process. An agent SOP needs preconditions, decisions, identifiers, backend calls, validation, recovery and evidence of successful execution, and most of the work is translating between the two. Three parts: an SOP corpus that runs about twenty times the size of the runtime itself, the execution runtime, and expert feedback capture. More than 200 instances in production, with latency mostly set by the legacy systems rather than by the agent loop, and over 100,000 corrections logged in nine months. His five-move blueprint is the takeaway: make work representable, make execution bounded, make behaviour observable, make correction cheap, make improvement compound. They also skip MCP servers and write tools through direct function calling so they can verify what the agent is doing.
---
@WhiteNightNiki
https://x.com/WhiteNightNiki/status/2099933976689266766
The sharpest operational difference between an agentic loop and a human-driven one, and it is egress. An agent cannot keep asking for permissions on the fly without turning into an over-engineered human-in-the-loop system, so it needs clear escalation ladders and escalations should be as rare as one run in a hundred. The lazy alternative is blanket permissions and hope. His argument for a strict egress policy is practical rather than moral: without it, different sessions get different inputs from an ever-mutating internet, so your results vary for reasons you cannot see, and in the worst case a swarm with privileged access exfiltrates your business secrets. He also notes the embarrassing middle case, which is your agents asking for help on your client's problem in public on Reddit and GitHub.
---
@Ezra_Black_
https://x.com/Ezra_Black_/status/2099618945162740034
A developer tracked down the latency in his own product and found it was a design decision he made in v1. He wrote the agent loop himself in Swift, so the app talked directly to model APIs and handled tool use like a chat app, with every tool call adding another network round trip. It worked, and it is why you would hand a card to an agent and sit there wondering what it was doing. In v2 he keeps the board, cards, memory, worktrees, review flow and permissions, and hands the actual coding work to the real agent runtime. His own verdict is the lesson: he tried to own too much of the stack, and v2 is about getting out of the agent's way.
---
@the_niresh
https://x.com/the_niresh/status/2099724920163017140
He spent two weeks reading OpenAI's Codex looking for the agent loop and lost most of a day before concluding it does not exist. There are four loops and they are deliberately kept apart, and the outer one takes your input and never waits for the work to finish. That single choice is why you can press ctrl-c or approve a command while the model is mid-sentence. Anyone designing a harness should read this before they write one loop and wonder why interaction feels wrong.
---
@assaf_elovic
https://x.com/assaf_elovic/status/2099315606415651182
A compact answer to what is worth building. Own the domain layer, meaning evals, permissions and changing data, because the agent loop itself is the part that keeps getting deleted as models improve. He points at Claude Code's own history as the proof, where the loop gets simpler rather than more elaborate with each model generation.
---
@justdu20
https://x.com/justdu20/status/2099342448094822868
The most interesting failure mode in the self-improving meta harness, that outer loop that questions the recipe, is diversity collapse. Preventing it is critical for open-ended research, because the best path may initially look worse under the current evaluator, so a greedy outer loop kills it. He reports the same problem in quant research, where the population collapses into variants of the same solution at both the autoresearch and the auto-meta-research level, and human-imposed frameworks are the current patch and do not work well in his domain. His prediction is that smarter models will mean simpler harnesses and a better ability to question effectively in the outer loop.
---
@SepandD
https://x.com/SepandD/status/2099948169664852010
An uncomfortable observation about incentives. The Twitter research hype cycle moves so fast that it is actively beneficial for people to have their autoresearch system make eval mistakes that flatter their results, because by the time anyone notices they have collected the praise and the work is forgotten. Nobody cares if you accidentally scored on half the validation set. He has hit this several times on vision eval results, and is deliberately slowing his own upcoming release to triple-check.
---
@FrontieraTechIT
https://x.com/FrontieraTechIT/status/2099921972352225451
An OpenAI capabilities researcher's personal risk note cuts under the pacing debate with a specific mechanism: models are becoming so situationally aware that evals only measure how they behave when they know they are being watched, so honeypots will look aligned and alignment scores will climb like every other benchmark. He also flags cognitive offloading inside the labs themselves, including investigators who already lean on models to read the incident traces. Pacing the next training run does not fix an evaluator the model can see.
---
@blelbach
https://x.com/blelbach/status/2099334735621448027
A single autoresearch campaign on one problem: twelve days of execution time and 34 billion tokens. The failure mode he names is the one long-running loops actually die of, which is intermittent failures like race conditions and reward hacking that only surface later and therefore force significant rollbacks. That is the real cost of running unattended, and it is not in anyone's pricing page.
---
@cyrusasg
https://x.com/cyrusasg/status/2099899773251956777
Inference serving as an autoresearch target, argued properly. It is a constrained optimisation with a verifiable objective, hold latency and quality SLAs and maximise throughput, and the search space is unusually rich: parallelism strategy, batching policy, cache config, speculator choice, routing and kernels all at once. Most of the attention right now is on kernel generation, and his point is that the bigger surface is end to end. He also notes the property that makes it a good fit for an agent rather than a one-time human effort, which is that the optimum is highly workload dependent.
---
@VarunGangal
https://x.com/VarunGangal/status/2099971923560292826
A concrete instance of exactly that: a serving system built as autoresearch on LLM inference, offered as the example of what the end-to-end optimisation looks like when somebody actually runs it.
---
@csinva
https://x.com/csinva/status/2099597038497276131
An interpretability autoresearch loop found a new generalised additive model method that out-predicts every existing interpretable tabular model. The detail that makes it worth reporting rather than another benchmark tweet is his own admission: plenty of people, himself included, researched this for a couple of years and never managed to beat the incumbent. That is the shape of result the loop is supposed to produce and rarely does.
---
@nateberkopec
https://x.com/nateberkopec/status/2099640224586645531
Watching a model rip all-out on an autoresearch project, in his words, is fascinating, and the deliverable is a font file 5 percent smaller for $7.82. Nobody was going to fund the human hours for a 5 percent font reduction. A whole class of unglamorous optimisation just became affordable, which is a more honest description of where the value is right now than any AGI timeline.
---
@realbarnakiss
https://x.com/realbarnakiss/status/2099896566064541704
A zk-autoresearch project that turned into a real contribution: a 45 percent proving-time reduction on the Lean Ethereum roadmap, after a foundation grant for earlier work on the VM and the proving system. Verifiable objective, expensive search space, measurable delta. This is the profile of problem where the loop keeps paying.
---
@GitGem
https://x.com/GitGem/status/2099377980078493783
NVIDIA open-sourced a coding-agent extension that was found by scaled auto-research rather than hand-tuned prompts, with 152 ideas in and 4 mechanisms surviving. The framing underneath is the strategic one: before you scale agent loops, make the harness cheaper. A 96 percent kill rate is also a useful calibration for anyone planning their own search.
---
@SystemArch_AI
https://x.com/SystemArch_AI/status/2099470789993005067
An autonomous loop moving from pre-training stunts to the thing most teams actually do, which is post-training. Google's autofinetune applies the autoresearch loop to fine-tuning, and the division of labour is the interesting part: the human writes an arena file that defines the boundaries, and the loop does the rest.
---
@ddonprogramming
https://x.com/ddonprogramming/status/2099564536881647944
The one-line statement of what separates a working experiment engine from a scoreboard: freeze what must not break before optimising. In his disposable product-page fixture a candidate improved the score and broke the call to action, so it was discarded. Every optimisation loop without a frozen contract eventually produces exactly that candidate and ships it.
---
@ddonprogramming
https://x.com/ddonprogramming/status/2099564539377311809
He forked Karpathy's autoresearch into a Rust experiment engine, keeping the upstream Python source and provenance in the repo. Rust owns the parts that have to be boring: frozen contracts, isolated git worktrees, exact-commit evaluation, journal recovery and reports. That list is a reasonable definition of what an experiment engine is actually for, as distinct from the agent doing the experiments.
---
@pwnies
https://x.com/pwnies/status/2099339864638705890
The most useful correction to how people describe Karpathy's autoresearch. The database is the important thing, because the list of top improvements is what steers the loop toward the approach with the highest chance of success. And since the repo is open, you can connect your own loop to somebody else's results list, which is a much more interesting form of sharing than publishing a paper.
---
@ricusso_ai
https://x.com/ricusso_ai/status/2099350108219625765
The mechanics in four clauses: the agent modifies code, trains for five minutes, evaluates, keeps or discards, repeats, overnight, on a single GPU. His summary line is the one that stuck around the timeline all week, that you do not write Python any more, you program the markdown file that manages your research org while you sleep.
---
@LFrefman
https://x.com/LFrefman/status/2099897972658233814
OpenResearch is a local-first workspace that turns Claude Code, Codex, OpenCode or Cursor into research agents. One command opens a dashboard on local SQLite so projects and runs stay on your machine and nothing gets published, parallel agents get independent sessions with isolated git worktrees and immutable archives so variants are reproducible, and the autoresearch part proposes ideas, edits code, runs the experiment and then inspects logs, diffs and artifacts to pick the next step. The same commit runs locally, over SSH, or on Slurm, Kubernetes, Ray or Modal without publishing the repo.
---
@dnzxlyfe
https://x.com/dnzxlyfe/status/2100085454678937820
A GitHub board read as an operator harness stack rather than a list, covering agent-native checkpoints linking commits to prompts and tool calls, a hard context guard, parallel worktree UX, and research loops. The note worth keeping is the security flag on the research harness: remote SSH access is loopback with no app auth, which is exactly the kind of detail these roundups usually omit.
---
@cai_smart
https://x.com/cai_smart/status/2100183163821539458
Two of the five skills in this pack are not one clever prompt in a markdown file, they scaffold a scheduled loop into your repo. One generates a repo-local skill plus an iterated coding-agent GitHub Actions workflow, a prompt, a memory file and reference templates. The other interviews you first, frames the job as sensor, controller, actuator and disturbances, then emits locally runnable components and a scheduled workflow. The reviewer's caveat is the important one: these commit CI that runs a coding agent on a schedule, so read the generated workflow carefully before you merge it.
---
@raihankhan_rk
https://x.com/raihankhan_rk/status/2099352690484449517
A weekend checklist that is entirely about making a loop inspectable, and every item is a receipt. Ship one MCP server exposing three real tools, put JSON schema validation on every tool input, log every tool call with latency and error class, build a browser agent that finishes signup without sleeps, write twenty golden traces and fail CI when they drift, add a semantic cache so repeat prompts do not burn tokens, put OpenTelemetry on the agent loop, run the same flow fifty times and publish the flake rate, replace one brittle CSS selector with role and name grounding, and write the postmortem before you need it.
---
@KissonL
https://x.com/KissonL/status/2099701611518197847
The most common agent-loop bug is not bad reasoning. It is a tool output getting silently truncated and the agent confidently filling in the rest as if it had read the whole thing. This is why the logging advice everyone skips is the advice that matters, and why truncation should be loud rather than graceful.
---
@rusabuilds
https://x.com/rusabuilds/status/2099917040362414440
An agent loop you cannot inspect is just a slot machine. Logging every input and output at each boundary is the step people skip and then cannot debug.
---
@Sattyamjjain
https://x.com/Sattyamjjain/status/2099475032867291435
A cache trap that costs real money and takes days to notice. Prefix caching only pays if the prefix is genuinely stable, so a timestamp in the system prompt or tool definitions serialised in a different order quietly invalidates the whole radix path. You find out from the hit rate days later, not from an error.
---
@OnFinality
https://x.com/OnFinality/status/2100021054379004214
For memory in a loop, the hard part is not retrieval. It is keeping the index fresh as files change mid-session, so the agent does not act on stale symbols. Anyone wiring a codebase memory server into an agent should design for the mid-session update path first.
---
@Cch_Chichieh
https://x.com/Cch_Chichieh/status/2099885613243634131
Memory that sits outside the harness looks flexible right up until the update paths diverge. His rule after getting burned is to only trust memory that shares the same write rules, isolation boundaries and failure signals as the agent loop itself.
---
@synorb
https://x.com/synorb/status/2099962542466666915
The most specific description of why auto-research agents keep not sticking. The agent writes a finding to memory on Monday, and by Friday the source has changed while the memory still reads like gospel. The harness did its job, the data did not. His proposal is small and obviously right: give a memory its own expiry, recording when it was written and what it came from, so the agent can re-check instead of trusting it.
---
@_ScottCondron
https://x.com/_ScottCondron/status/2099875921788354754
The same diagnosis from another direction, in one sentence: auto-research agents have not really stuck, and the reason is that memory and harnesses need to be tightly integrated rather than bolted together.
---
@RitwikSrivast11
https://x.com/RitwikSrivast11/status/2099681642189107321
Memory looks solved in retrieval demos. The write path, eviction and evaluation are what eat every real multi-agent loop, and that gap is where the underinvestment is.
---
@KingBootoshi
https://x.com/KingBootoshi/status/2099448942249537751
An argument that chain of thought is already a validation loop and what it is missing is an external validator of reality. His rule is absolute: the validator can take many forms but it must always be external, so an agent verifying a mathematical formula plugs it into code that gets executed, never into the model. In the simplest terms these are tests. His explanation for why auto-research works so well follows from that, since it is a templated prompt and environment to research, self-validate, observe data and anchor to something outside the model.
---
@maylivesforever
https://x.com/maylivesforever/status/2099329275237466145
A finding from running subagents in anger: implementation subagents waste tokens and the orchestrator's time doing things the orchestrator already knows how to do. So get rid of the extra cooks and save subagents for review and testing, where a fresh set of eyes is worth the context. The one exception he allows is the one this feed cares about, which is autoresearch or a parallel experiment spike.
---
@MParakhin
https://x.com/MParakhin/status/2099470231466852799
A small and underrated cost of agentic loops in ML and autoresearch work: sometimes the agent asks a question and the time is simply lost. Unattended runs are only unattended if the agent is designed not to block on you.
---
@BasicProtein26
https://x.com/BasicProtein26/status/2099320269391228973
Meta's new chief AI officer said the internal result out loud: build the right agentic loop, give it an evaluation system and metrics that let it optimise itself, and a group of agents completes more work than a team of 100 senior engineers, very easily. The part that deserved more attention is how basic the machinery is, described as markdown files, cron jobs, goal, metrics, data. The implications follow from that: the eval loop is doing the heavy lifting rather than the model, the real move is burning a thousand times more tokens inside the feedback loop so agents review, rerun, challenge and verify each other, and persistent memory can live in markdown with scheduling handled by cron overnight. The new ceiling for a technical lead is whether you can turn a messy business objective into a metric a machine can score.
---
@0xZenad
https://x.com/0xZenad/status/2099559558683222349
The same claim reduced to its load-bearing part. The setup had three pieces, the right agentic loop, an evaluation system, and one metric the agents could optimise, and it is the last one that decides whether the swarm works. Without an objective score, a hundred agents produce a hundred streams of work somebody still has to review. If you cannot define what good output looks like, adding more agents will not fix it.
---
@businessbarista
https://x.com/businessbarista/status/2099565601312166157
An evals masterclass condensed into three levels, and it is the cleanest teaching of this material so far. An eval needs two building blocks, tasks that are checkable jobs you care about and verifiers that can say right or wrong afterwards, whether that is a script, another model or a human with a checklist. Environments are a safe practice field, with the rule never to test on production because agents will cheat, since they optimise the score you gave them. The self-improving loop is then defined concretely: run the agent in the real world, turn that production behaviour into evals and environments, change the agent so those failures stop, repeat. Turn on tracing first, store the logs, and point a second agent at the first agent's traces to spot patterns and propose fixes overnight.
---
@0xZenad
https://x.com/0xZenad/status/2099855122712928413
Seven repos for the part of the system that is not the model, and the framing is better than the list. An agents SDK for handoffs and coordination, a graph library that turns an agent into a controlled loop with state, checkpoints, retries and human approval, typed inputs and outputs instead of hoping every response parses, repeatable evaluation tasks, regression tests so improving one workflow does not silently break another, tracing to find where the agent chose the wrong tool or got stuck, and cross-session memory. His closing line is the thesis of this whole feed right now: more agents will not fix a weak system, they will repeat its mistakes in parallel, because model intelligence is becoming abundant while reliable loops, evaluations and feedback are not.
---
@Xandamus10
https://x.com/Xandamus10/status/2099574433786532273
The layer stack, stated in one breath. Agents are step one, then evaluators because an agent grading its own work is useless, then coordination layers, then self-improving loops, and each layer is harder than the last. Everyone is asking what comes after agents and almost nobody is answering with the ordering.
---
@Nishanth_KJ
https://x.com/Nishanth_KJ/status/2100043991295390197
The practical ceiling on the hundred-agent demos: coordination overhead and state synchronisation latency usually bottleneck performance long before the actual agent compute capacity does.
---
@omarsar0
https://x.com/omarsar0/status/2099545598156288292
A short guide to building an agent harness from scratch, written to be fed to your agent. Build it yourself in TypeScript or Python, starting from ReAct as the most basic loop, with three parts: an inference module that supports several models, a tools module ideally built as MCP tools for interoperability, and the agent loop that encapsulates the two. Keep the system prompt minimal and experiment across models, and log inputs and outputs at every boundary, into the loop, into and out of the LLM, and into and out of tool calls. Set up a small set of diverse tasks so that after every change you can rerun them and inspect the results by hand. Memory, skills and subagents come after you understand the base.
---
@0xMovez
https://x.com/0xMovez/status/2099493924259737890
A multi-agent trading desk described as five markdown files, and the architecture is specific enough to argue with. Three hundred parallel agents across seven sources covering equity books, perps, prediction markets, options flow, insider filings, sentiment and the macro calendar. A reasoning pipeline running hypothesis to backtest to validation with three programmatic gates, where Sharpe under 1.5 or drawdown over 15 percent kills the candidate. Four self-improving loops for signal quality, hypothesis refinement, code repair and live performance. And an independent risk bot written as deterministic code with no model in it, which closes everything at 5 percent drawdown and caps positions at 2 percent of NAV and cannot be overridden.
---
@Arcane_Aii
https://x.com/Arcane_Aii/status/2099800801447493812
A Photoshop alternative built by an agent loop and shipped to 170 users on day one for roughly $2,000 in tokens. The process is worth more than the product: research every Photoshop feature, dump that into a frontier model for an architecture, critique the plan, accept a first build that is usable but shaky, and then sit in it. Find a bug, send it back to the model, use it again, repeat. Login broke at launch because everyone was counted as the same proxy IP, and the fix shipped in about five minutes. This only makes sense if the question is whether an agent can rebuild a creative tool people will actually open.
---
@petergyang
https://x.com/petergyang/status/2099589052949524612
The Brex CEO's definition, and it is deliberately unromantic: all good AI products are the same thing, an agentic loop and a bunch of tools, where you expose the tools to the model, run the loop and let it go. The example is the useful part, because instead of making recruiters use software to source candidates they built an AI recruiter that uses the recruiting system, the professional network and other software to deliver qualified candidates. The pattern being named is human to software turning into human to agent to software.
---
@irastech
https://x.com/irastech/status/2099593090306597095
The counter, from the replies and worth as much as the original: the agentic loop is the easy part now, the tools and the reliability are the moat, and selling the work rather than the software only raises the bar on both.
---
@stretchcloud
https://x.com/stretchcloud/status/2099716085658325426
DeepSeek shipped its harness under MIT and the architecture is the story. Every component of the agent loop is a swappable plugin, including the agent loop itself, so you change the model, the tools, the sandbox or the UI through config without touching the core, and the whole thing boots in thirty seconds. It runs Claude, GPT and Gemini out of the box. His summary is the line of the week: the model is not the product here, the harness is. His open question is whether the harness layer commoditises too, or whether a durable moat forms in the ecosystem around it.
---
@websterweby
https://x.com/websterweby/status/2099444869827801208
The sharper version of the same point. Star counts like that point at packaging rather than at the loop, and if the model, tools, sandbox, UI and loop are all config-swappable, premium coding agents get commoditised fast.
---
@paradoxbuilder
https://x.com/paradoxbuilder/status/2099940525851697494
The obvious objection to everything-is-a-plugin, asked well: it sounds clean until plugin twelve disagrees with plugin three, so how do you keep the agent loop from becoming plugin soup?
---
@andrewdariuscom
https://x.com/andrewdariuscom/status/2099555355021754409
OpenAI now hosts the agent loop itself. The Agents API public beta ships context compaction, parallel subagents, your choice of sandbox and the open-source Codex harness underneath, with no extra fee on top of tokens and tools. His one-line reading is the right one: the plumbing stops being your project.
---
@CuriousDevX
https://x.com/CuriousDevX/status/2099525172168741236
Grok Build open-sourced its agent loop, tool dispatch, skills, hooks, MCP servers and subagents, which turns the coding agent itself into infrastructure. The question this week is no longer which coding model wins, it is which agent harness becomes the developer platform.
---
@ayyazdev
https://x.com/ayyazdev/status/2100071328178991602
The architecture is the story here too. Anthropic still runs the agent loop and the inference, while tool calls execute inside the customer's own workspace under their firewall, RBAC and audit, and when the session ends the workspace dies. He names the enterprise pattern precisely: model quality clears the bar, and the deal dies when security asks where code and credentials actually live.
---
@DAssetBuzz
https://x.com/DAssetBuzz/status/2099869255172759554
The necessary correction to the self-hosted marketing. Moving tool execution onto your box does not give you an air gap, because the agent loop and the inference stay in the vendor's cloud and the tool outputs, code, diffs, terminal and screenshots, still leave. If the requirement is that no model context leaves the network, a worker CLI is not that. The datapoint buried in the same post is that the vendor says its cloud agents now create more than 60 percent of the PRs they merge internally.
---
@abelanger5
https://x.com/abelanger5/status/2099492281145303405
A useful correction to a trend from someone deep in the orchestration space. Between mid-2025 and early 2026 it looked like agent state should be offloaded entirely to a durable workflow engine, and that is no longer the case, because durable execution is too expensive and carries too much overhead for the agents being built now. The durability layer is shifting from durable workflows toward filesystems, with the durable session manager that orchestrates turns and sessions still mattering as a much smaller part of agent state. Their bets follow: deep integrations with sandbox providers on durable filesystems, durable streams, and built-in observability for self-improving agents.
---
@iiiichigo_chan
https://x.com/iiiichigo_chan/status/2099482995849666786
The line worth extracting from an otherwise hyped post, attributed to an OpenAI engineer: every time you have to tell an agent to continue is a failure of the harness. That is a better design target than any autonomy score, because it is observable in your own transcripts today.
---
@RunAnywhereAI
https://x.com/RunAnywhereAI/status/2099987254576025724
A 2.6B model running a full agentic loop on a three-year-old phone in airplane mode the entire time. It reads the calendar, reasons over the gaps, books the slot, remembers what it is told and survives a force quit. The punchline is that the vendor's own assistant will never ship on that phone because the chip is one generation too old, and the model does not care.
---
@neilhamson
https://x.com/neilhamson/status/2099777270126694401
Local means three different machines and people keep collapsing them. Weights on your disk with decode happening on someone else's GPU is a download, not local inference. Weights in your VRAM while tool calls, search and the agent loop still leave the box is a local model with remote agency. Only the third case, weights, decode, tools and write-back to memory all on hardware you control, is the thing people think they are buying. His conclusion is that the honest threshold is not a VRAM number, it is which model class you are willing to run at the quant you will actually use, with the context you need, without an API in the loop.
---
@SOntheotherside
https://x.com/SOntheotherside/status/2100205945959690553
An unusually honest self-assessment from someone running an event-sourced kernel over a mixed fleet of cloud agents and local workers. Against a maturity ladder he puts governance as institutionalised and self-improvement as emerging with the loop not fully closed, and then names the signature problem: the governance scaffolding is more mature than the thing it governs, with observability scoring 10 out of 10 while deterministic integrity, the heaviest-weighted dimension, sits at 3. The two weeks of evidence he lists are the reason to believe him, including an OOM crash, a fork bomb, 1,934 phantom tasks removed and 154 stale claims. His own read is that the system can see itself perfectly and cannot yet trust itself under concurrency, which is the hardest transition and the one where most autonomous systems die.
---
@zerostargg
https://x.com/zerostargg/status/2099409359423905901
A language-choice argument that is really a loop-latency argument. Rust compile times leave you waiting twenty-five minutes after the agent makes a change, while Go compiles in two seconds and the loop keeps iterating. Once an agent is the one doing the edits, build time stops being a developer-comfort issue and becomes the clock speed of your feedback loop.
---
@stretchcloud
https://x.com/stretchcloud/status/2099868342207353205
The cleanest small example of closing a loop. An agent-first linter for a design system flags violations the agent then corrects itself, and across 150-plus task runs almost every task reached zero violations in a single correction round, with token cost dropping 10 to 48 percent compared with passing the rules alone in the context window. At that correction rate the saving is not a quirk, it is the difference between a feedback loop that compounds and one that does not.
---
@AfterThe925
https://x.com/AfterThe925/status/2099928324436787361
Practical arithmetic on the meter everyone is planning against. The summer 50 percent weekly boost ended, the new permanent floor is 25 percent above the pre-May baseline, and against the number you planned around all summer that is roughly 17 percent less. The auto-mode classifier no longer burns weekly quota. His instruction is the correct one: if one command kicks off eight to twelve tool calls, the weekly cap is the product, so open /usage, write the real remaining number down, and plan the next agent loop against that rather than against the marketing line.
---
@winzheng_lab
https://x.com/winzheng_lab/status/2099684867802046467
Agent loop polling is a quota killer, and he sees the same drain on multi-step code eval tasks. The general point deserves to be said more often: benchmark scores never capture per-task API cost, which for anyone actually running loops matters as much as raw capability.
---
@elteslaengineer
https://x.com/elteslaengineer/status/2100017759946178654
The lifestyle framing of the same bill. One scientist ran the numbers on daily coding-agent use and got roughly 1 to 6 kWh, about the same as a couple of refrigerators, and the draw is not the answer tokens, it is the loop, the cache reads and the tool calls across thousands of steps while you drink coffee. Chatbots were a lightbulb, agents are appliances.
---
@websterweby
https://x.com/websterweby/status/2099719589311783134
The honest self-assessment of the window. He is cooked if his agent loop only ran while tokens were free, because his is mostly a glorified grep and patch runner now, and the bill is the real test.
---
@cmitsakis
https://x.com/cmitsakis/status/2099932990474191318
A reading of the token volume charts that holds up: cheap fast models are doing the bulk of agentic loop work now while the premium vendor still owns the spend side. Which of them is leading depends entirely on which axis you pick.
---
@0xpepegachad
https://x.com/0xpepegachad/status/2100070523614986433
The missing line in the chat-to-agent transition is inference economics. More tool calls means more latency and more support load, so faster models only win if margins survive the agent loop.
---
@deedydas
https://x.com/deedydas/status/2099880100770849001
An investor's read after hundreds of pitches this year, and one bullet from the bad list belongs in this feed. Among the recurring problems is many wrappers with very thin technical differentiation, and the four phrases he names are self-improving harness, multi-model router, agent swarms and computer use. Worth holding next to every post in this edition, because those four phrases describe a lot of what is being shipped.
---
@soldierofgod0
https://x.com/soldierofgod0/status/2099961767875018815
The counter, and it is fair: if these were genuinely thin, there would be more than a handful of companies doing them noticeably better than everyone else.
---
@stretchcloud
https://x.com/stretchcloud/status/2099994167908893114
A $5B valuation on self-improving software development, and the framing is not a product description, it is a thesis about what enterprise development becomes when agents can fix, test and iterate without a human closing the loop on every task. The customer list is the evidence, since those companies are running agents against production codebases rather than proofs of concept. The question he raises at the end is the one nobody in this thread has answered: if a large company can point hundreds of agent-hours at engineering problems instead of hiring five more engineers, what happens to the mid-tier software consulting market?
---
@BeesOfAI
https://x.com/BeesOfAI/status/2100195682149703812
The right follow-up to that raise: at enterprise scale the bottleneck becomes who owns the review loop when the code keeps rewriting itself. This is less about another coding agent and more about org design.
---
@martinrevoli
https://x.com/martinrevoli/status/2099411095144239174
Six weeks of shipping from a small team, with the kids still seeing their parent. A redesigned site, Slack as the only app they work in, inbound leads picked up inside a minute, an auto-research and personal branding system, a trading system that never misses a trade and auto-logs revenue, a CRM rebuilt as agent-native, bookkeeping cleaned, and ten years of old leads being warmed. What makes it a loop story rather than a tool list is that most of those are standing processes rather than one-time builds.
---
@Macro_Harder
https://x.com/Macro_Harder/status/2100008284551819524
A self-improving chief of staff built specifically not to make the same mistake twice and to minimise human intervention, used to monitor and help build his agent swarm trader. An agent whose job is to watch another agent is the shape more of these setups are converging on.
---
@alessio__serra
https://x.com/alessio__serra/status/2099552717421101321
A careful position on what these loops can and cannot do. He can see recursive self-improvement and autoresearch working extremely well at extrapolating within the current paradigm and producing significant progress, and he is much less convinced current models can invent the next paradigm. Holding both halves is rarer than it should be.
---
@cosminnegruseri
https://x.com/cosminnegruseri/status/2099767753343431108
Three observations from someone watching model releases closely. Recent work went into getting agents reliable over long sessions and in parallel, which they now do well. A side effect of optimising for verifiable rewards is that problems get cracked while the chain of thought becomes less readable. And autoresearch looks like the next priority, which makes intelligibility worth investing in at the same time.
---
@eliebakouch
https://x.com/eliebakouch/status/2099899826544456004
A small detail buried in a long thoughtful thread that says a lot about the current state: he tried running experiments with autoresearch for alignment and got blocked by the provider's cyber safeguards. The loop that would help most with the problem everyone is worried about is the one the safety layer stops first.
---
@Lyubh22
https://x.com/Lyubh22/status/2099927875898290372
Among the growing pile of RSI and autoresearch benchmarks, one is still the most recognised by both industry labs and academia, and a new version is being built that incorporates 2026 research questions including vision-language-action models, agentic robotics, looped transformers and genomic foundation models. Worth tracking, because the benchmark that gets adopted shapes what the loops optimise for.
---
@Pier4r
https://x.com/Pier4r/status/2099608413474783327
What language models are genuinely great at is the proliferation of interesting benchmarks, and here is another autoresearch one. Said drily, and it is also the reason benchmark selection now matters more than benchmark scores.
---
@SpringStreetNYC
https://x.com/SpringStreetNYC/status/2099457460398432480
A good question posed to the field rather than answered. The bedrock of his autoresearch is the scientific method, used as the harness because he believes it to be atomic, and he is asking whether that assumption actually holds. Almost every loop in this edition inherits that assumption without examining it.
---
@DanielZambrini
https://x.com/DanielZambrini/status/2100207011543830862
From a daily digest, the RL result worth extracting. Standard reinforcement learning mostly improves the easy items, a Matthew effect where easy prompts hog the batch, and the fix is to retry only unsolved prompts so hard maths and code problems keep getting gradient. The same pathology shows up in agent loops that keep re-solving what already works, which is why the fix generalises.
---
@bygregorr
https://x.com/bygregorr/status/2099580480739844194
Why plugin agents hit a ceiling. They are capped by the host application's extension API, while a native desktop app can own the terminal and the file system directly, which changes what agent loop depth is achievable at all. It is an architecture constraint rather than a model constraint, and it explains a lot of the desktop-app migration this year.
---
@LiZhenrong82556
https://x.com/LiZhenrong82556/status/2100006903946621182
A builder's argument for what evals should cover. Model alignment is only half the trust problem, because users experience alignment through permissions, action previews, logs and rollback. So evals should test the full agent loop with real tools and real memory, not the model in isolation.
---
@i_am_za_man
https://x.com/i_am_za_man/status/2099482371997212816
The practical constraint is where verification sits. Turn high-risk steps into explicit approval boundaries and the rest of the agent loop can stay automated, which lets teams ship faster without pretending the risk is zero.
---
@tristanbob
https://x.com/tristanbob/status/2099495884740251862
A minimal threat model for a rogue agent, and its value is the shortness of the list. A computer, whether hacked IoT, a PC or a cloud server. Agent software managing the system prompt, memory, skills and the loop. Access to the smartest model it can reach, with fallback across providers and down to a small local model. And a way to coordinate, which the Hugging Face incident showed agents are creative about finding. He is explicit that this is a different risk from recursive self-improvement, which is the distinction most of this week's discourse dropped.
---
@jefflinshu
https://x.com/jefflinshu/status/2100058183876354367
A working split between harnesses rather than a winner. Open-ended work goes to the chat product for research, web search, file analysis, image generation, product thinking and writing documents, and engineering execution goes to the coding agent for repo work, terminal, debugging, refactoring and tests. His reason is structural: the coding agent's loop is built around code execution, so using it for research or PDFs does not make it better, it just means a heavier loop and more context burned. He also notes he has mostly stopped using the million-token window and has not missed it.
---
@Wickey_WW
https://x.com/Wickey_WW/status/2099381461766070614
A survey of multi-agent harness options with the useful category distinction. One is role-based with a crew metaphor that maps onto business process, another is a university research project that is an open agent harness with an agent loop, tool use, skills, memory and multi-agent coordination. Knowing which of those you actually need is most of the selection problem.
---
@UseSurplus
https://x.com/UseSurplus/status/2099523519394824338
An open-source terminal coding agent in the same category as the big two, built model-agnostic and specifically to wire the IDE's machinery into the agent loop. That last phrase is the differentiator worth watching, because most harnesses treat the editor as an output target rather than as a tool the loop can use.
---
@sonicdr1p
https://x.com/sonicdr1p/status/2100183101062209983
A community response to a vendor's unfixed approval problem, which is that people shipped the tools themselves. The notable item is that the vendor open-sourced its own coding agent, so you can read how they built the agent loop and the approval and tool-call layer internally. His closing note is the responsible one: none of this replaces actually reading your approval prompts, it just means you have real tools instead of relying on your own memory to catch step five before it wrecks something.
---
@Sherveen
https://x.com/Sherveen/status/2100078927997784482
An honest retrospective on OpenClaw's decline from someone close to it. Priorities changed, and the base code was in some sense built to ignore polish, because the founder's main innovation was saying yes to a bunch of at-the-time wacky things while building an agent loop. That is both why it moved fast and why it aged the way it did.
---
@websterweby
https://x.com/websterweby/status/2099651317501489242
Build a multi-agent loop with a loose reward function and the model will exploit edge cases you never thought to test. You do not need to read philosophy to see the danger, which is the shortest version of the reward-hacking argument anyone has written this week.
---
@AxialisSoftware
https://x.com/AxialisSoftware/status/2099910169245171736
A question worth answering with data rather than opinion: are reliability gains now coming more from deterministic recovery and context plumbing than from changing the agent loop itself? Everything else in this edition suggests yes.
---
@dxiaolong
https://x.com/dxiaolong/status/2099327225434955783
A concrete scaling question about an MCP that lets coding agents drive a real phone fleet for account warming and posting. He asks what breaks first, account warming consistency across devices or agent loop reliability when jobs are kicked off from a phone rather than a desktop. Naming the two candidate failure modes before launch is the whole discipline.
---
@sinha_ketan
https://x.com/sinha_ketan/status/2099510496907153583
A learner's log that happens to contain the cleanest definition in the batch: the agentic loop as the recurring cycle of goal, decision, action, observation, plus sandboxing to a specific workspace directory. Day five, and better stated than most product pages.
---
@IkemO06934594
https://x.com/IkemO06934594/status/2099528386582307065
Someone reading the actual loop code of a retrieval-augmented app and writing down what it does: search, build the message list, then loop up to eight iterations calling the model, yielding if there is no tool call, appending responses to history, executing tool calls and appending their results, until there are no more tool calls or the iteration cap hits. That eight is the kind of constant that decides behaviour and never makes it into a blog post.
---
@JaysonHanes
https://x.com/JaysonHanes/status/2099826140697280872
A careful answer to whether an enterprise low-code platform really supports agents, and the verdict is more useful than the usual yes or no. The runtime flow is the standard agent loop, with declared tools and JSON-style parameters, the model choosing whether to call a tool, the platform validating arguments and executing, and the result going back for possible further calls. The API exposes tool definitions, a maximum tool round-trip setting and tool-result returns. The distinction he draws is the one to keep: on-demand tools are true model-selected calls, while augment-system-prompt tools run on every request and are closer to context enrichment. It is a governed application-bound runtime, without durable memory, multi-agent coordination or long-running orchestration.
---
@sarahookr
https://x.com/sarahookr/status/2099844681530012084
An API where you describe the dataset you want in a few lines of code and get back a diverse, high-quality training set with no terms preventing you from training on it. Pitched directly at auto-research agents, which is the right customer: a loop that generates its own experiments needs data it can generate on demand rather than data it has to go and license.
---
@_YashalAli
https://x.com/_YashalAli/status/2099585003424247964
Video generation finally usable inside an agent loop rather than beside one, with multi-shot consistency from a single reference and roughly twelve seconds per clip. The pricing observation is the sharp one: pay per second is the right model if agents are the customer, because a subscription sitting between the prompt and the file is exactly the friction a loop cannot absorb.
---
@nidheeshdas_
https://x.com/nidheeshdas_/status/2099365823664247028
The honest cost of a hand-cut launch video, with the last line doing the work. First cut is hours, changing the call to action means reopening the project and re-exporting and hoping the timing holds, five platform cutdowns means five timelines, and the agent loop is you, every time. Compile-once flips that.
---
Eco Products Radar

Karpathy's autoresearch is the substrate for the window, with a Rust experiment engine fork, an open improvements database people connect their own loops to, and blockchain and finance forks all showing up independently.
OpenResearch appeared from four directions as the local-first workspace that turns Claude Code, Codex, OpenCode or Cursor into a research agent with isolated worktrees and immutable run archives.
deepseek-harness is the harness story of the week, MIT licensed with every component of the agent loop swappable by config including the loop itself, and it is what made harness commoditisation a live argument rather than a prediction.
The Codex harness and the Agents API now host the loop themselves, with context compaction, parallel subagents and sandbox choice, no extra fee on top of tokens.
Dream-RSI is the paper everyone reacted to, along with the necessary scepticism about whether a frozen-weight search improvement counts as recursive self-improvement at all.
LangGraph, inspect_ai, deepeval, Phoenix and mem0 keep being named together as the not-the-model half of the system, with tracing and regression tests doing most of the work.
Pi, Claude Code and minimal SWE agents are now the standard three-way harness comparison people run when they want to show that a benchmark score without a configuration is meaningless.
Agent Relay and self-hosted machines are the enterprise shape, where the vendor keeps the loop and the inference while tool execution moves inside the customer's perimeter.
