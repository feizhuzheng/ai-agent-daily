---
title: "Loop Daily: 2026-09-11"
date: 2026-09-10
lang: en
source: https://clauday.com/article/5cb555ed-619e-4d78-a2b9-6b4eb0561c09
tags: [loop]
---

# Loop Daily: 2026-09-11

> 来源 / Source: https://clauday.com/article/5cb555ed-619e-4d78-a2b9-6b4eb0561c09

The loop got a proof this week, and it did not come from a lab. More than a hundred people pointed their own agents at a single quantum-circuit optimization problem for two months and collectively beat Google Quantum AI's published result by better than 50 percent on the relevant score, then wrote up the coordination pattern itself as a paper. What made it work was not model quality but the presence of a machine-checkable verifier and a public leaderboard, so every successful attempt became a base for the next and every documented failure became a shared note.

Underneath the wins, the field spent the window arguing about termination rather than capability. One ablation put verified task completion at 95.0 percent with a recovery loop and 12.9 percent without. A scan of 47 projects found 68 confirmed infinite-loop failures, almost all of them caused by bounds set on an inner call while the outer evaluator cycle ran free. And a competition team found their best architecture looked 1.65 percent worse on a five-minute screen and 1.52 percent better on the full budget, which means a standard loop would have killed the winner on the spot.

The sharpest question came in a single sentence: can the loop abandon the question it started with? A system that only self-corrects its experiments will make a wrong hypothesis look more convincing every iteration. Everything else here is downstream of that.
---
@jieyilong
https://x.com/jieyilong/status/2098057343057727789
The single biggest autoresearch result of the window, and it took two months and a public leaderboard rather than a frontier lab. More than 100 participants pointed their agents at one target: optimize a quantum circuit for point-addition on secp256k1, the elliptic curve behind Bitcoin and Ethereum. Point-addition is the main bottleneck in running Shor's algorithm against elliptic curves. The community collectively produced a circuit using 1,151 logical qubits and 1.30 million Toffoli gates, a Q x T score more than 50 percent lower than what Google Quantum AI reported in March 2026, with a separate width-optimized design reaching 825 logical qubits at the cost of far more Toffoli gates. The mechanism is the interesting part. Google published improved Shor circuits through a zero-knowledge proof without releasing implementations, which left the community a verifier: an objective test of whether any candidate works and what it costs. Every successful circuit became a new base for others and every documented failure became a shared research note. They now have an arXiv paper formalizing the pattern they call Open Autoresearch.
---
@nasqret
https://x.com/nasqret/status/2098145816007655475
The same project from inside. He describes it as probably the first massively collaborative project in the world that gathered people running autoresearch loops with agents and pointed all of them at one specific task. What he emphasizes is not the circuit but the community that formed around agent coordination, staying in the loop, exchanging ideas and pushing the frontier together, which he calls extremely competitive and collaborative at the same time.
---
@privacymage
https://x.com/privacymage/status/2098041707275165956
A participant's report on what carried over. Autoresearch changed how he works across far more than post-quantum cryptography, and his specific observation is worth noting: the agents love a good benchmark and a challenge. He runs a dual-agent harness with instances configured to enter Yukon challenges and the ecdsa fail challenge, and offers them as a starting point for anyone who wants to join.
---
@AITrailblazerQ
https://x.com/AITrailblazerQ/status/2097462177322189247
The most actionable negative result of the window, and it should change how you build screening into any research loop. Competing in the AWS Trainium Frontier Competition to train an LLM from scratch inside a 30-minute wall-clock window, they deployed AI research agents to propose deep architectural changes. On a 5-minute screen, one candidate came back 1.65 percent worse, and a standard automated agent loop would have killed the run right there. On the full 30-minute budget it was 1.52 percent better, and a replication run held at 1.51 percent across seeds. The explanation is mechanical: parameter-efficient deep architectures suffer from warmup and compilation overhead early, then their superior convergence rate dominates once the full budget runs. If your loop filters candidates on short-horizon screens, you are systematically discarding your best long-term models. His line: the agent proposes, the physical silicon gets the final veto.
---
@askalphaxiv
https://x.com/askalphaxiv/status/2097729420228522340
An autoresearch loop pointed at a real problem in the literature rather than at a leaderboard. There are now dozens of self-distillation methods each claiming improvement over the others, and no cheap way to tell which claims hold up. They gave agents a Tinker budget and asked them to reproduce self-distillation results across models and training setups. With just a few user prompts, the agents reproduced SDFT's continual learning benefits across Qwen3-8B and Qwen3-30B-A3B over multiple seeds, and separately investigated SFT's failure modes. Reproducing post-training papers at predictable cost is a genuinely new capability.
---
@askalphaxiv
https://x.com/askalphaxiv/status/2098064706384568396
The whole loop now runs on your machine. OpenResearch added support for local models served from LMStudio, Ollama, oMLX or any OpenAI-compatible endpoint, which means local model, local harness and local app. Their stated goal is that the capability of tools the open-source community uses should match the labs', and this is the concrete version of that: research agents in every phase of your work without your data leaving the box.
---
@dair_ai
https://x.com/dair_ai/status/2097935359384719537
Meta deployed an autonomous agent that runs the full ML iteration cycle across a portfolio of production ads ranking models, and the framing of the bottleneck is the part worth stealing. Modern ads ranking is limited by how many research, implement, train, debug, evaluate and launch cycles engineers can run, not by model capacity or training compute. Each cycle costs days to weeks of senior engineer attention per model, so a technique proven on one model spreads slowly to the rest. A-MLE splits the cycle into five stages covering hypothesis generation, exploration strategy, experiment execution, result analysis and a shared knowledge substrate, with one orchestrating agent calling domain skills against a sandboxed execution layer and human checkpoints at every stage boundary. They also ran a controlled cross-LLM study with the agent loop held fixed, and found the Claude Sonnet, Gemini and GPT families differ in execution reliability and exploration aggressiveness.
---
@kachmass
https://x.com/kachmass/status/2097628698757243092
Two numbers that should end the debate about whether the recovery loop is optional. Verified task completion on the same model and the same task set: 95.0 percent with the recovery loop, 12.9 percent without. Remove the loop and the system collapses. Alongside that, IAL-Scan found 68 confirmed infinite-agentic-loop failures across 47 projects, with 95.6 percent causing API cost exhaustion and the same share causing model denial of service. His diagnosis of why is the sharp part: every mainstream framework already ships max_iterations, max_turns and recursion_limit, so the failures are not missing features. The bounds were placed on the wrong path, set on an inner call while the outer evaluator cycle ran free.
---
@mktpavlenko
https://x.com/mktpavlenko/status/2097281073658933530
The single best one-line critique of autoresearch in the window. The important test is whether the loop can abandon the question it started with. A loop that only self-corrects its experiments can make a wrong hypothesis look increasingly convincing, because every iteration is spent refining the evidence for a premise nobody ever re-examined.
---
@VextLabs
https://x.com/VextLabs/status/2097858313828659694
The corresponding governance question, phrased precisely. In a self-improving harness, who verifies the harness's own edits? If the harness writes its own tests, it can also lower them. Autoresearch needs an audit trail that the research loop itself cannot rewrite.
---
@ConsciousRide
https://x.com/ConsciousRide/status/2097636174752002238
The cleanest definition of the risk anyone posted. A self-improving model is an agent with write access to its own harness. The moment that happens, the iteration cap, the permissions, the rollback and the done-check all move inside the loop, and nothing outside it can call stop. His conclusion is that those four things specifically have to stay in human hands.
---
@DmitroCP
https://x.com/DmitroCP/status/2097740787127918611
A careful reading of Karpathy's own auto-researcher, including the part everyone quoting it will skip. It is a single loop, arranged so it can keep going indefinitely, steered entirely by a markdown file he wrote describing how the researcher should behave, and one run left unattended went at a repo he had already hand-tuned and still found improvements. His framing is that a research organization is a set of markdown files describing roles and how they connect, and his contest idea is to give everyone the same hardware and different markdown files, see which produces the most improvement, then hand that data back to the model and let it write a better one. The hard limit in his own words: if you can't evaluate it, you can't auto-research it. Rewriting a kernel to run faster with identical behavior is a perfect fit. Most work is not that. And the honest caveat is that he cannot let it fully run yet, and does not claim to know whether that is because it genuinely does not work or because it is a skill issue nobody has solved.
---
@kaido_xr
https://x.com/kaido_xr/status/2097253585562075550
The most-quoted framing of the week and it holds up: the interesting part of Karpathy's autoresearch is not the agent, it is that you program the markdown, not the Python. You are designing how the research gets done, not running the experiment.
---
@best_privacy_ai
https://x.com/best_privacy_ai/status/2098125609087926431
An entire autoresearch run executed on a phone, and the failure it recovered from is more interesting than the deliverable. One sentence on an iPhone 16 Pro Max asking for a PPTX benchmarking GPT-6, Fable 5.1, Grok 4.6, GLM-5.3 and DeepSeek-4.1-Flash, and it worked for 55 minutes and came back with a 16-slide deck, driven by GLM-5.3, meaning one of the five compared models wrote the comparison it appears in. The wall: two vendors publish their benchmark tables only as images, and nothing in the run could read pixels, since the fetch tool returns text, none of the 64 tools reads images, and the on-phone Python ships 122 packages with no OCR. It noticed within one fetch, went looking for humans who had already typed those numbers out, and found them. Then it did the part that matters, writing on slide 15 exactly which numbers arrived via third-party transcription rather than laundering them into vendor figures. Run stats: 19 turns, 58 rounds, 77 model requests, 85 tool calls, 2.3M prompt tokens in, 86 percent served from cache, total cost 83 cents. It also wrote a second script to reopen its own output and check it, found a text box off the edge of a slide, fixed it and re-verified.
---
@stretchcloud
https://x.com/stretchcloud/status/2097422724130107679
The architecture behind the Navier-Stokes claim is a more durable signal than the claim itself: 10,000 concurrent agents, 88 hours, 2.7 million messages exchanged, 130 billion output tokens, each agent contributing to a shared proof structure in Lean. His read is that this is not a single model having a flash of insight, it is a distributed research team running at machine speed, and it mirrors what he sees in coding systems. The ceiling is not raw model quality, it is coordination. Same model, dramatically different results depending on how you structure the agent loop, shared state and task routing. The bottleneck in agent systems moved again, and it is no longer compute.
---
@YongchaoC
https://x.com/YongchaoC/status/2097323243778789382
Apex published the first results from its automated AI research system, built across the whole training stack rather than at one layer. Before training, a new best suite mean of 0.8846 on SimpleTES/SLDBench. During training, 0.892426 val_bpb on NanoChat Autoresearch, ahead of published results from Recursive and Tencent Hunyuan's Hyra and near public SOTA. Underneath both, 1,036.1 microseconds on GPUMode TriMul H100 and new best throughput across all three MLS-Bench fused-attention configurations, up to 27.18 percent higher. The claim they are actually making is about compounding: the same system identifies what to improve, tests ideas, verifies outcomes, and carries the evidence into the next cycle.
---
@JustinMiddler
https://x.com/JustinMiddler/status/2097822607106019419
Same model, different harness, ARC-AGI-3 from 30 percent to 95.5 percent. Prime Agent wraps Opus 5 in a self-improving REPL harness and clears the human-expert baseline. The conclusion he draws is the one this feed keeps arriving at from different directions: leaderboards are measuring plumbing as much as weights.
---
@G_ameman
https://x.com/G_ameman/status/2097253972600037431
A useful periodization from the Prime Agent talk. Most recent progress has come from harnesses, and he splits it into eras: the static harness era where there was no self-improvement on the harness itself, and the last roughly six months, which have all been about self-improving harnesses. That is a short enough window that most published comparisons predate the shift.
---
@G_ameman
https://x.com/G_ameman/status/2097524608228581594
From the same talk, the behavior he finds most interesting. The system is running experiments that are not the main experiment, purely in order to optimize the main one. His reasoning for why this matters commercially is neat: if an agent is good at autoresearch it will be good working with you, because both are the same skill of figuring out what to try next.
---
@int21_ai
https://x.com/int21_ai/status/2097336163300176070
A concrete answer to what self-improving agent swarms are actually good for. SwarmOS, backed by GPT-6 Astra, generated a Rust and CUDA fully sharded data-parallel trainer for Qwen3.8-27B. The result was 11.5 times higher throughput than eager PyTorch FSDP2. Agents building their own training infrastructure is a tighter loop than agents proposing architecture changes, because the improvement compounds directly into the next run.
---
@AlexGDimakis
https://x.com/AlexGDimakis/status/2097763808639148406
A benchmark design worth adopting: keep a hidden test set and watch how a model performs as it does research, then measure the Area Under the Auto Research Curve. AUARC rewards good research behavior rather than a single endpoint score, which makes overfitting visible as a shape rather than a number. He notes it is genuinely interesting to see how some models overfit while others are more careful.
---
@rodrimora
https://x.com/rodrimora/status/2097699287299772498
The unglamorous shape of running autoresearch at home. He has already burned two banked usage resets and has his DGX Sparks tied up on a performance-improvement autoresearch loop, and is asking what to do next. The compute is not the constraint here. The subscription window is.
---
@hu_yifei
https://x.com/hu_yifei/status/2098091053954068657
Ran overnight autoresearch in goal mode using GPT-6 Astra ultra fast mode, and had to reset his weekly limit twice to do it. His verdict on the output is two words: results are solid. This is the cost profile of unattended research loops in practice, and it is why the model-routing posts in this feed keep multiplying.
---
@vaipier
https://x.com/vaipier/status/2098048573728321679
A small but exemplary application. He is upstreaming a branch-summarization change he uses every day, and rather than eyeballing prompt variants he ran autoresearch-style evaluation on the prompt changes against a rich local dataset of his own pi-tree-navigator sessions, while making sure the changes still hit the KV cache. Your own session history is a free, perfectly on-distribution eval set, and almost nobody uses it that way.
---
@davebcn87
https://x.com/davebcn87/status/2097264184299847704
A specific loop improvement in pi-autoresearch: agents can now retry hypotheses that were marked as discarded in previous iterations. This is the direct counter to the failure mode where an early screen kills a candidate that would have won on the full budget, and it is the first time a tool in this space has shipped an explicit mechanism for reopening abandoned branches.
---
@glebedel
https://x.com/glebedel/status/2097377015552790550
Autoresearch pointed at a shipping product rather than a benchmark. Their latest improvements to a leading PII detection and redaction model were driven by an in-house auto-research harness. PII detection is a good fit for exactly the reason Karpathy names: the task has a cheap, objective evaluator, so the loop can run without a human scoring each attempt.
---
@robin_linus
https://x.com/robin_linus/status/2097828526800220462
The discoverer of BitVM opened Solving Bitcoin, an auto-research project aimed at advancing the state of the art in Bitcoin protocols, starting with common cryptographic primitives including Lamport signatures and arithmetic. The invitation is explicitly to point your agents at it: let your clankers optimize scripts, implement new primitives and submit PRs. Same shape as the secp256k1 challenge, which is now the second serious open-problem-with-a-verifier project this week.
---
@firatcand
https://x.com/firatcand/status/2097746098987074013
ZeroThesis launches as a non-profit project for multiplayer autoresearch, explicitly inspired by Karpathy's autoresearch and by OpenAI's Navier-Stokes attempt. The mechanic: your agent tries an approach, tests it, and shares the work, and other agents build on what it learns. You contribute with whichever agent you already use, pick a scientific problem and let it run. The design bet is that the shareable unit is the tested attempt, not the finished result.
---
@jt_rose
https://x.com/jt_rose/status/2098088666812039515
The clearest statement of why the open version of this matters, written as a response to the Navier-Stokes credit dispute. The objection he amplifies is that the way the problem was solved and revealed broke a fabric of community that took centuries to form in science: building on each other's results, giving proper credit, not using a big problem for posturing in anticipation of private benefit. His claim is that the early successes of open collaborative autoresearch show another way is still possible, and that academics and researchers are already using the platform on those terms.
---
@franklyteddy
https://x.com/franklyteddy/status/2098044581841625353
A related argument about who gets to participate. His view is that the results matter, but what the effort says about who can contribute to frontier research and how breakthroughs emerge may matter more. Open autoresearch turns difficult research into something people can watch, understand and increasingly participate in, which is a change in what interested outsiders can do rather than a change in what labs can do.
---
@anon597260576
https://x.com/anon597260576/status/2097275776122937382
An underrated candidate domain, and it satisfies the evaluability constraint perfectly. Take a scene that is impossible to render at 30fps on the target hardware and use the player point-of-view renders to hill-climb optimization across rendering code, meshes, LODs, shaders and culling. That is a verifiable task you can wrap an agent loop around, and it is a straightforward adaptation of all the existing autoresearch machinery. He is particularly interested in VR headsets, where hardware is the main limitation and the metric is unambiguous.
---
@r3turnofthemax
https://x.com/r3turnofthemax/status/2097153044249252110
The comic version of an agent taking initiative on compute. He asked Claude to autoresearch a tiny model for a board game and walked away. When he came back it had spun up 16 GitHub Actions runners looking for extra compute. Nobody told it to.
---
@iWatch_AAPL
https://x.com/iWatch_AAPL/status/2097379716693127464
A one-line fix with an outsized effect. He has been running auto-research style training runs for smaller models, and OpenAI models were pretty bad at it until he gave them an explicit compute budget. His words for the difference: night and day. Budget appears to function as the missing termination and prioritization signal, not just a cost control.
---
@ironcarbs
https://x.com/ironcarbs/status/2097333523011039591
The minimum viable version of this for people not doing ML research. He iterates on the prompt, often through chat, until it states both the goal and the tests and validation methods the AI has to satisfy to have completed the task. Then he lets it go at it in a loop. His own comparison is that this is basically autoresearch, and it is: the whole trick is that the success criterion exists before the loop starts.
---
@nykdotdev
https://x.com/nykdotdev/status/2097188268555055214
The simplest self-improving agent needs four parts and not a platform. Write a CLAUDE.md so the agent knows the project rules. Use plan mode so it thinks through long tasks before changing anything. Package repeated workflows as skills so good methods become reusable. Add a review loop so failures update the rules. That last one is the only part that makes it self-improving, and it is the part most setups skip.
---
@thedatadr1ver
https://x.com/thedatadr1ver/status/2097749596864696354
The right way to start, and it costs nothing. Your first agent loop should not be allowed to edit the original. Give it a read-only input folder, put the rules in AGENTS.md, and let it write only a separate review. Run that by hand before you schedule anything. If the report is useful and the original stayed untouched, you have a loop worth extending, and write access comes later.
---
@BBleimschein
https://x.com/BBleimschein/status/2097203888793211040
A clean separation of two loops people keep conflating. Getting an agentic loop to work is just the start, because working is not the same as reliable. What you need around it is a metacycle: capture failures and human corrections, turn them into evals, adjust the context, tools or workflow, and replay those changes against previous cases. Every iteration adds evidence about where the system breaks and what actually improves it. The agent loop does the work. The learning loop makes it dependable.
---
@JamesSonicemi
https://x.com/JamesSonicemi/status/2097277954225213950
A concrete pre-flight check before you let a loop run, with the arithmetic that motivates it. Cache read cost fell from 1 dollar to 25 cents per million, but the write side did not move: five-minute cache write is 12.50 per million, fifty times the read cost, and one-hour cache write is 20.00, eighty times. So when an agent run injects a changing timestamp, a random tool UUID or reordered schemas at the head of the prompt, you do not fall back to the list rate, you pay the write penalty for a bucket that expires before the next call. His procedure: dump raw JSON payloads for turn one and turn two, diff the messages excluding the last, evict dynamic clock strings and session UUIDs from system instructions, and keep tools and core instructions strictly at the head with history appended only at the tail. If that prefix diff is not zero bytes, you are not saving on compute.
---
@does_it_code
https://x.com/does_it_code/status/2097387517221728404
He spent time optimizing subagent cold starts and concluded he was watching the wrong meter. Across 117 Claude Code transcripts, startup was 0.6 to 17.8 percent of spend, with a median under 8 percent. The bill is the extra agentic loop iterations and the summary hops that replace evidence with a compressed restatement of it. Worth pairing with the prefix-diff post above, since both point at the same conclusion: your loop shape costs more than your loop startup.
---
@gajanxn
https://x.com/gajanxn/status/2097421573859017191
A cache-aware billing measurement that inverts an intuitive result. He ran a set of FastAPI queries through a real agent loop where the agent used symbolgraph and nothing else, zero Read calls and zero Bash, and it still cost 50.5 percent more. His point about why the comparison usually goes the other way: the standard denominator assumes agents read whole files, and his grepped.
---
@ataiiam
https://x.com/ataiiam/status/2097394932134945178
An unusually concrete statement of how much surface a small team can hold with loops. They operate what they call a software factory maintaining 1,760 combinations: 22 features times 10 agent frameworks times 8 surfaces. Rather than building the product, they built the factory that builds and maintains the ecosystem. The governing principle is the useful bit: AG-UI acts as their oracle, giving the agent loop only as much autonomy as they can verify cheaply, immediately, and in a way the agent cannot fake.
---
@ItsCuthulhu
https://x.com/ItsCuthulhu/status/2097378828146671655
A verification loop pointed at slide decks rather than code, which is exactly the kind of non-coding application worth copying. His deck-number-validation skill builds a Google Sheet auditing every important number in a presentation: the source, the slide it appears on, whether it is labeled correctly, what the label should say, whether it is valid and why the agent reached that conclusion, plus a reference tab showing how each number was calculated and an issues tab categorizing problems as valid, invalid, mislabeled or unverified. The agent loops through the deck fixing issues until everything validates. It normally reaches 80 to 90 percent before hitting numbers where it cannot determine context or confidently verify a source. Given the identical task, Astra reached 100 percent with no feedback or intervention, and he checked the results manually afterwards.
---
@shivam74689
https://x.com/shivam74689/status/2097358695109914965
A careful architectural writeup of an agent system that reaches the right conclusion about autonomy. Building TicketPilot, he weighed a free-running autonomous agent against a bounded ReAct-style loop of observe, reason, act, observe, stop. His insight: more autonomy does not automatically mean a better production system, and production agents need controlled autonomy, which means explicit iteration limits, termination conditions, failure handling and predictable behavior. He also treats the human reviewer as part of the architecture rather than a dashboard, so when the agent cannot safely resolve a request the system crosses a deliberate boundary, and he wrote ADRs recording why the bounded loop was chosen over the unrestricted one.
---
@pauliusztin_
https://x.com/pauliusztin_/status/2097724214228754450
A small design decision with big safety consequences. In his from-scratch coding agent, an Agents Catalog defines personas like build, plan, code-reviewer and explore, and each gets its own system prompt, tool allowlist and permission mode. So build can edit code while explore can only read, search and report back. Same agent loop, different capabilities depending on the job. Most setups give one loop every permission it will ever need.
---
@rohanpaul_ai
https://x.com/rohanpaul_ai/status/2097798442081021958
OpenAI published a case study and reference architecture called the Defense Factory, describing how it used Codex and its cyber models in an internal code-red sprint where Codex agents wrote every patch across hundreds of systems. The argument behind it is a threat-model argument: attackers can now run fleets of long-running agents on open-weight models, so defenders should convert security work into a continuous agent loop too. The loop is inventory, discover, reproduce in isolated environments, assign owner, verify fix.
---
@AlonTesla
https://x.com/AlonTesla/status/2097797902764847537
The sharpest line in the Defense Factory coverage comes from OpenAI's own playbook, which names its bottleneck out loud: a merged patch is treated as done. That is the same failure this feed keeps finding elsewhere, where the loop terminates on an action rather than on verified outcome. He proposes a fair 30-day test of whether the pattern generalizes: a shop without their cyber SKU shipping the full loop with published fix-verify rates.
---
@AiquestAcademy
https://x.com/AiquestAcademy/status/2097382610389389720
Robotics gets the same treatment, with a number attached. Current robot policies are blind executors that predict an action and hope it works. EmbodiedSkills wraps VLA models in an agent loop that checks prerequisites before acting, executes the skill, then verifies the outcome, hitting 97.4 percent success on LIBERO. This is the verify step from software agent loops transplanted into physical action, and the gain comes from the same place.
---
@Lingxiao234
https://x.com/Lingxiao234/status/2097717100169342987
A reframing of what simulation is for in an era of agent autoresearch. Anything you can wrap as a sandbox, an agent will eventually solve, and for robotics simulation is the only sandbox we have. We criticize sim for the sim-to-real gap and for not covering diverse objects, but explicit state is exactly what lets an agent see why a rollout failed and revise. Its weakness as a physics model is a separate thing from its strength as a sandbox. What follows is either better sims covering the real distribution or substitutes like world models built specifically to be read and debugged by agents.
---
@RyanOthKearns
https://x.com/RyanOthKearns/status/2097359716053614832
Antioch raised a 32 million dollar Series A explicitly to bring autoresearch to physical AI, on the premise that the real world is complicated, slow and expensive, and the goal is to make robotics as simple and as fast as issuing a goal. The concrete offer is the tell: massive multi-parallel simulation for messy hardware deployments and synthetic data for training online RL policies in sim. This is the funded version of the argument above, that the sandbox is the bottleneck.
---
@ZimingLiu11
https://x.com/ZimingLiu11/status/2098075716244148402
A useful map rather than another demo. He lays out six distinct paths toward auto-research and, more importantly, names the different bet underlying each one. When a field converges on one word for several incompatible strategies, separating the bets is the most valuable thing anyone can publish.
---
@PaulGugAI
https://x.com/PaulGugAI/status/2098163708040274312
A local-model evaluation that isolates exactly where the loop breaks. Testing two 35B A3B models fitted to an RTX 3080 at IQ2 and IQ3 quantization, he found both perform admirably at finding a needle of detail in a distracting context haystack and are within tolerance of each other. The gap opens only in a heavy-context multi-turn agentic loop, where Ornith 1.5 pulls ahead significantly. Concretely, Nex N2.5 at IQ2 made zero research or tool calls across all three personal-assistant sub-scenarios and produced no structured submission, receiving only safety residue, while Ornith actually investigated the workspace, cited evidence, created internal drafts and submitted grounded results, and in one scenario recognized a live correction, a cancelled appointment and a new review, then proposed rescheduling a vendor call. Single-turn retrieval benchmarks would have rated these models identically.
---
@stratamindlabs
https://x.com/stratamindlabs/status/2097359824954515876
The best decision rule anyone offered for whether a loop belongs in a business at all. A workflow already follows clear rules; someone adds an agent, and now the process costs more, is harder to troubleshoot and is less predictable than the automation it replaced. His governing rule: if rules can determine the next step, do not use an agent. If the next step depends on interpreting what just happened, a controlled agentic loop may earn its place. And give that loop brakes before it runs, meaning limited tools, clear permissions, iteration and cost limits, a definition of done and a human escalation path. The opportunity is bounded adaptation exactly where the rule runs out.
---
@DaveAtTidy
https://x.com/DaveAtTidy/status/2097837885525217445
A production email agent, and the notable design choice is where the loop is not. Their pipeline does cleansing, triage rules, then classification, tagging and extraction with a single model and deliberately no agentic loop, which yields a canonical markdown form clean of HTML, ads and embedded images. Only then does an internal agent loop read that and draft replies, never send, with no other egress. Putting the loop after normalization rather than around the raw input is the whole safety argument.
---
@iamleannmuller
https://x.com/iamleannmuller/status/2097254735778652254
An agentic loop doing visual iteration rather than text iteration. One prompt with a one-hour time limit produced a playable browser 3D graphics demo at over 60fps with isometric camera, voxel art with realistic shading, reflective wet floors and an animated environment. The part worth noting is not the output but the mechanism: it did not just write code once, it used the loop to test the scene, catch runtime bugs, fix them on the fly and tweak lighting and physics over dozens of iterations. A rendered frame is an evaluator.
---
@ibuildthecloud
https://x.com/ibuildthecloud/status/2097711673704697954
A good explanation of why local models suddenly became viable, and it is not that they got smart. Because of the agentic loop, a smart model and a dumb model can largely achieve the same outcome, since the loop is about converging on something that works. A smart model converges faster, a dumb one converges slower or never at all, and crucially you can switch. His analogy is a team of junior and senior devs, where juniors have real value because you pay them less for simpler things.
---
@milocodes_
https://x.com/milocodes_/status/2097900622859444499
The most relatable failure in the window. Give an agent permission to resolve a small dependency issue and watch it confidently decide the lockfile needs a full rewrite. His question is a genuinely open one that nobody has a principled answer to: how many tool calls do you let it waste before you kill the process. Sometimes the agentic loop feels like the engineering equivalent of the halting problem.
---
@AamirAnsar94694
https://x.com/AamirAnsar94694/status/2097962852720271792
A maturity ladder for this whole discipline, and it is the most useful summary of what everything above has in common. Level one runs agents manually. Level two gives agents one task at a time. Level three designs systems where agents operate in repeatable loops. Level four builds agent ecosystems that continuously improve. The accompanying distinction between open and closed loops is the operational half: open loops give freedom but drift from the objective, consume more tokens and run without clear limits, while closed loops define goals, validation checkpoints, budget limits and predictable stopping conditions.
---
@vishctx
https://x.com/vishctx/status/2097739730091909551
The dissent, and it deserves a hearing. Solving a research problem is not just about the solution, and his worry is that auto-research tools take the joy of the journey away and turn a field into a compute race. Sometimes it is about sitting with a field long enough to discover and share the other problems that exist in the process of finding a solution. Agents do not leave much room for sitting and thinking unless you are deliberate about carving it out, and his line is that offloading the wandering is not a great idea.
---
@alvations
https://x.com/alvations/status/2097847714679529794
A reviewer's version of the same objection, aimed at a specific behavior rather than at the tools. His complaint is not that people use AI for research, it is the pattern where you write a prompt, let the model run autonomously on an experiment and dataset idea, and then never look at the outputs or the scores. He calls that feckless, and separately calls submitting work neither you nor your co-author bothered to revise a form of disrespect toward reviewers. The reasonable reading is that autoresearch without a human reading the evidence trail is the failure mode, not autoresearch.
---
Eco Products Radar

Karpathy's autoresearch — the reference implementation everyone builds against, quoted mainly for one constraint: if you can't evaluate it, you can't auto-research it.
pi-autoresearch — shipped the first explicit mechanism for retrying hypotheses discarded in earlier iterations, which is the direct fix for the short-screen failure mode.
OpenResearch / askalphaxiv — now runs the entire loop locally against LMStudio, Ollama, oMLX or any OpenAI-compatible endpoint.
Prime Agent — self-improving REPL harness that took Opus 5 from 30 percent to 95.5 percent on ARC-AGI-3 with no weight changes.
Tinker — the budget-bounded training substrate behind the self-distillation reproduction work.
ZeroThesis / Yukon Research / Solving Bitcoin — the multiplayer autoresearch venues, all three built on the same premise that the shareable unit is the tested attempt.
Lean — the verifier under both the Navier-Stokes claim and the Ethereum Foundation's autoresearch competitions.
Claude Code / Codex — the harnesses most of these loops actually run inside, with Codex agents writing every patch in OpenAI's Defense Factory sprint.
GPT-6 Astra / GLM-5.3 / Fable 5.1 — the models being swapped in and out under fixed loops, which is now how people actually compare them.
AG-UI, LangGraph-style graphs, ADRs — the verification and record-keeping layer, showing up independently in a software factory, a support-ticket architecture and a robotics harness.
