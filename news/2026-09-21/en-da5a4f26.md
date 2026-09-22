---
title: "Loop Daily: 2026-09-22"
date: 2026-09-21
lang: en
source: https://clauday.com/article/da5a4f26-4a1d-4e68-9a46-3f4805e65fe3
tags: [loop]
---

# Loop Daily: 2026-09-22

> 来源 / Source: https://clauday.com/article/da5a4f26-4a1d-4e68-9a46-3f4805e65fe3

The loop turned around and pointed at itself this window, and it worked. The paper everyone read ran recursive auto-research on the agent harness rather than the model — 152 proposed directions across 535 executable environments, over 3,000 runs — and kept four mechanisms that cut token traffic by up to 49 percent and API cost by about a third while holding roughly 94 percent of the score, then transferred to a different vendor's model with no further search. The detail that makes it credible is that the acceptance benchmark was frozen and never fed back into the search, because prior work had shown evolved harnesses score well on what they trained against and barely improve on anything new. Alongside it, thirteen agents did twelve days of collective research with no manager and no assigned tasks by treating a version-control graph as shared memory, closing 62 percent of the gap to a trained baseline — though the most useful reader pointed out that the same 200 development texts were reused throughout, so the trace is auditable but the generalization is not established. The counterweight came from people running these loops on real problems and reporting what broke: a frontier model auto-researching trading signals explored parameters badly and proposed three nearly identical learning rates as an experiment, an overnight run produced a seventeen-times inference speedup that did not generalize at all, and someone running an unmonitored pipeline found that 95 percent of apparent breakthroughs were overfits to noisy scrapers until strict external validation gates were added. The sharpest single line of the window answers what a self-improvement loop goes after first: whichever layer has a cheap verifier. Kernels and context management have one. Open-ended work does not, which is why the same technique that halves your token bill cannot tell you whether a story is any good.
---
@askalphaxiv
https://x.com/askalphaxiv/status/2101578159674310707
The paper that organized the whole window: a recursive auto-research loop pointed at the agent harness rather than at the model. Coding agents optimize their own harness instead of having it hand-designed, and across diverse coding environments the loop discovers four mechanisms that compress context, observations, reading and actions. The result is comparable performance at 44.7 to 49 percent less token traffic and roughly one third lower API cost.
---
@arkyyang
https://x.com/arkyyang/status/2101300791651049832
The most useful breakdown of that paper, written for product builders rather than researchers. His first takeaway is the one that changes behaviour: most of an agent's bill is repeated context rather than new thinking, because the model is re-billed for the whole conversation at every step — so before switching to a cheaper model, measure how many tokens your harness re-sends per step. The second is that the waste lives in four separate places and should be fixed and measured separately: merge a file edit and its follow-up test into one request; only shrink running context when the projected savings beat the cost of rebuilding it; stop re-sending huge tool outputs in full and archive them behind a short handle plus a 1KB excerpt; and compress long build logs with a cheap model into a verified short receipt that falls back to the original if verification fails. Third, harness efficiency transferred to a different vendor's model unchanged, so keep harness logic separate from model-specific code. Fourth, and the one most people will skip: automated self-improvement overfits unless you wall off the final exam — the search ran across 535 environments while the acceptance benchmark stayed frozen and was never fed back, and without that the reported gain is a mirage.
---
@Montreal_AI
https://x.com/Montreal_AI/status/2101667013462536610
Adds the search scale behind that result and the detail that makes it trustworthy: 152 proposed directions, 535 executable search environments, over 3,000 runs and more than 60,000 agent-environment interactions, after which the candidate harness is frozen and the held-out evaluation stays outside the search loop with no patching against the final test. His framing of the shift is clean — the harness itself became an object of research, meaning the model need not change for the surrounding intelligence system to improve. He also notes that the authors are careful to present recursive efficient improvement, where a cheaper harness funds broader research that discovers an even better harness, as a future direction rather than a demonstrated compounding effect, and argues that discipline makes the result more interesting rather than less.
---
@casper_hansen_
https://x.com/casper_hansen_/status/2101337016093065481
The highest-reach post in the window, and it is a claim about hardware. He relays Jeff Dean saying chip design could be compressed from two years to three months with reinforcement learning plus new EDA tooling — which amounts to a specialized auto-research loop for hardware. A reply asks the right question and gets no answer: does that mean the agent is proposing layouts, or running validation simulations too. The difference between those two is the entire question of whether the loop has a real verifier.
---
@JohnKutay
https://x.com/JohnKutay/status/2101892859305623793
Ran the honest version of the test everyone else was theorizing about, inside a real go-to-market agent harness on anonymized production data. On classifying campaign emails by strategy, the decision model hit 90 percent accuracy against 50 percent for the LLM baseline and ran nearly eight times faster. But it was not a universal win, and the failure is the more valuable half: it performed poorly as a control mechanism inside their text-to-SQL agent loop because it lacked the semantic context to interpret internal business definitions. It could see that a query returned rows but not whether those rows matched the company's canonical definition of qualified pipeline, whereas the LLM could inspect the relevant models, filters and definitions before deciding the analysis was complete. His conclusion is the right one: extremely promising for repeatable classification, still worse than an LLM for context-heavy reasoning, and best paired.
---
@de1lymoon
https://x.com/de1lymoon/status/2102028138297327884
Argues that adding a decision model to an agent does not automatically make the loop faster, and gives the sequence that does. First capture the loop: log model calls, tool actions, retries, latency and cost so you know where time actually goes. Then group the repeated decisions — use a tool, retry, is this done — and define the correct outcome for each. Only then route them, giving the fast model the relevant state and clear criteria instead of pushing the whole conversation through a deep model. Set confidence thresholds so uncertain or novel cases escalate. Finally verify and measure against your baseline on total loop time, cost and errors. The speed comes from finding the decisions the agent makes over and over, not from the swap itself.
---
@dani_avila7
https://x.com/dani_avila7/status/2101888707259256903
Built a Claude Code mod from a skill-suggestion example, and his framing of what it implies is sharper than the mod itself: it points at a different way of managing the context window, where skill, effort and tool selection get delegated to decision models. The harness can then be split into smaller independent decision services instead of putting everything inside the main agent loop.
---
@0xwhrrari
https://x.com/0xwhrrari/status/2102035137848381455
Ran a decision model in front of a cloud agent product on his own Mac and published both the setup and the result. It analyzed twelve live options, ranked them in 0.18 seconds and stopped before the irreversible action, at a cost of roughly two millionths of a cent. The seven-step setup is mostly discipline: keep the API key out of chat paste and into the secure field, smoke-test one primitive, build the router with a dry-run mode and logs, add a skill that calls the router before browser, research, retry or spawning another bot, then stay in shadow mode reading logs until you trust it, with a kill switch that bypasses the router entirely. Only then flip to active. Twelve options analyzed, six decision checks, zero unsafe actions, one ranked choice.
---
@DivyanshT91162
https://x.com/DivyanshT91162/status/2101231430223462456
Describes an approach where thirteen AI agents do research together without a manager, without assigned tasks and without a shared conventional memory, because research is recorded as a version-control graph instead. Every hypothesis, experiment, result, insight and verification becomes an immutable commit, so an agent can literally pick up where another left off. They ran it: thirteen language-model workers over about twelve days produced 1,703 contributions across fifteen accounts, with 145 commits in the winning ancestry and 165 independent reproductions. The task was to initialize a 119.6M-parameter hybrid model from 141 pretrained donor models with no training data and no gradient updates, and the evaluator went from 3.39 to 1.899 bits per byte, closing 62 percent of the gap to a trained small baseline. The part he likes is that there was no central planner — they were given a shared research memory and let loose.
---
@ContextWindow_
https://x.com/ContextWindow_/status/2101131674666868784
Gives the same collective-research result the skeptical reading it needs. He accepts the substrate idea — parallel research agents repeat experiments when session-local results do not provide a durable record of prior methods and their provenance, and storing code, results and verification claims as linked commits with searchable views exposing leading and neglected branches fixes that. But he draws the line precisely: selection repeatedly reused the same 200 development texts, so while the system makes the search trace auditable, the study does not establish a discovery-efficiency gain or held-out generalization. Those are two different claims and the paper only supports one.
---
@sandeepinloop
https://x.com/sandeepinloop/status/2101694815851131113
Adds the threat model to the same design. Using version control as shared memory for collective auto-research is a strong substrate idea, but it also becomes a contagion surface: if one agent writes a gaming heuristic, the rest pick it up. His conclusion is that shared channels belong in the evaluation threat model, not just in the storage design. This is the cleanest statement of a failure mode that multi-agent research systems have not yet had to face at scale.
---
@edotenv
https://x.com/edotenv/status/2102075985973690493
A clean negative result from letting a frontier model auto-research deep learning signals on crypto perpetuals data. The model does not explore parameters well, making only minimal changes across iterations; it has poor research taste, at one point proposing experiments consisting of three almost identical learning rates; and it struggles with intelligent evaluation, specifically judging training curves where there is no binary criterion. His summary is that there is still a long way to go before these models are useful on genuinely hard research tasks.
---
@RRicefan
https://x.com/RRicefan/status/2102077726563971190
The companion result, and the comparison is the part that stings. Running the same auto-research on real historical data with a high-frequency target confirms the model is a bad researcher with poor research taste in a very low signal-to-noise setting — but the task is still solvable by humans, because his own hand-fitted models outperform the auto-researched ones by a wide margin and took him less time to build.
---
@gregpr07
https://x.com/gregpr07/status/2102157421909258560
One night of auto-research did not generalize, which he says plainly rather than burying — but the failure came with two specific outputs worth keeping. It optimized caching specifically for a custom harness, and it implemented a diffusion transformer on a 2048 block that made inference seventeen times faster. Narrow, non-transferable, and real: that combination is what most overnight runs actually produce.
---
@Kizuno18
https://x.com/Kizuno18/status/2101834245471707397
States the mechanism that separates auto-research theatre from auto-research results. Running an unmonitored pipeline on demographic data, he found that when models hypothesize and test data treatments, 95 percent of apparent breakthroughs are subtle overfits to noisy scrapers. Strict external validation gates turned 103 noisy experiments into real, reproducible gains. His framing is that the real compounding only starts when auto-research loops get deterministic evaluation gates.
---
@rryssf
https://x.com/rryssf/status/2101392207999889475
Walks through the overnight loop that made the term mainstream, and the arithmetic is what carries it. You hand it a GPU and a single markdown instruction file; the agent reads the file, edits the actual training script, and launches a run capped at exactly five minutes regardless of hardware. After every run it checks one thing — did the model get better — keeping and committing the change if yes and throwing it out if no. Five-minute runs mean about twelve experiments an hour and roughly a hundred by morning, and one public overnight run executed 700 experiments and found 20 genuine improvements, all logged, all reversible, all discovered while nobody watched. His closing line is the one worth arguing with: the bottleneck was never the hardware, it was always the human deciding what to try next.
---
@chrismdp
https://x.com/chrismdp/status/2101627716210430011
One sentence that marks the boundary of the whole method. Both of the well-known auto-research implementations climb a single number, and a story has no such number — whether it is good is a judgement, so the judge has to be an agent reading the whole run. That is the cleanest available statement of why this technique generalizes instantly to kernels and compilers and not at all to open-ended work.
---
@Tech_girl
https://x.com/Tech_girl/status/2102111778624692600
A head-to-head on the public auto-research benchmark that produces a number most people will quote without reading the caveat. On their test hardware, one system ran 336 experiments against 76 for a general coding agent, and also reached a better final score. The raw results are public. The experiment count is the interesting figure because it is measuring throughput of the loop rather than intelligence of the model, which is exactly the variable this whole field just started optimizing.
---
@ChrisJMcCormick
https://x.com/ChrisJMcCormick/status/2102102027279204747
The clearest case in the window of a human lifting results out of a published auto-research run rather than running one. A stack of improvements cut his baseline time by 40 percent, and he is explicit about which ideas he borrowed — batch size of 192K, gates added to certain lambdas, and two large bigram hash tables of two million and one million rows, with the 5.25 billion parameters in them optimized sparsely with no first moment and only per-row magnitude. He is equally explicit about what he did not take: no FP8, no custom kernels, and a codebase he notes is still clean rather than agent-mangled. Two of his own changes are the fun part — dropping gradient buffers from the hash tables and inlining the optimizer into their backward math, and learning that you can run the autotuner once and ship the result alongside the model.
---
@vigram_void
https://x.com/vigram_void/status/2101809430602113122
Points at a paper with a genuinely different idea for scaling research agents: stop running every experiment they propose. Reinforcement learning for auto-research agents has an ugly bottleneck, because generations batch nicely but every candidate experiment needs its own sandbox, dataset load, training run and evaluation — eventually the expensive part is not thinking, it is finding out whether the thought worked. The approach replaces most of that execution with a learned world model that predicts outcomes, then periodically anchors it against real executions, with online debiasing correcting systematic reward error and inverse-variance denoising suppressing noisy predictions. The numbers: a 4B agent drops from 883 to 286 GPU-hours and a 9B from 1,174 to 349, while both beat full real-environment RL on held-out averages. The pattern he names is the takeaway — learn a cheap approximation of reality, use reality sparingly to keep it honest, and spend most of your compute inside the approximation.
---
@my_cat_can_code
https://x.com/my_cat_can_code/status/2101537855134941576
Notes that one conference already hit 60,000 abstracts against 19,500 the year before — more than every previous year combined — and then refuses the easy conclusion. People still think auto-research is about optimizing for papers, but getting accepted does not mean you found anything. Auto-research is about discovering new science and pushing the frontier; papers were never the goal, and a model that writes something a top conference will accept is a paper machine rather than a researcher.
---
@AtaeiMe
https://x.com/AtaeiMe/status/2102033799424954723
The most considered version of the academia argument, and it starts by conceding the thing everyone else resists: the old publishing system is going away and most proposed fixes assume we can get back to how it worked before. He thinks of the submission flood as a denial-of-service, because producing a paper gets cheaper while checking it still takes time, and says he is not convinced machine reviews have been worse than the average human review since 2025. His sharper point is that solving review would not save it — anyone with a large node can take last year's paper, make the obvious extension and keep submitting, so what does an acceptance mean when you can produce them hourly, given we still use publications to decide who gets a job. His proposal is the constructive part: run auto-research openly with the traces published alongside the paper, so you can see what was tried and why someone gave up on it, and give people credit for finding an error that would have wasted six months even when there is no paper in it. Publishing already worked like decentralized recursive self-improvement, and papers compressed that process while leaving most of it out.
---
@SuJinyan6
https://x.com/SuJinyan6/status/2101101400809963813
Arrives at the same place from formal verification. A founder friend pitched using formal methods to solve the verification problem, and the question she was too intimidated to ask at the time is the right one: converting natural language to formal language is well studied, but how do you ensure the natural language part is all-encompassing in the first place. She connects that to auto-research claims, noting that flooding a conference with agent-generated papers and treating peer review as the evaluation is not good verification for automatic research. Her closing line is the one to keep: in the end, reality is the final verifier.
---
@OngroundAI
https://x.com/OngroundAI/status/2101257979978743959
Ties the harness result to the broader question in one move. Harness changes are measurable, sandboxable and reversible, while weight edits are none of those — which is why the efficiency work landed first. His answer to what a self-improvement loop targets first is the line of the window: whichever layer has a cheap verifier. Kernels and context management have one; open-ended model quality does not.
---
@AxiomBot
https://x.com/AxiomBot/status/2101753455157326058
Names the artifact the field is missing in one demand. The harness paper wants a harness receipt: repo, environment, verifier, selected mechanism, failed mechanism, and transfer result. Otherwise auto-research becomes a very convincing benchmark story. The inclusion of failed mechanism in that list is the part that would actually change anything.
---
@GiulioRebuffo
https://x.com/GiulioRebuffo/status/2101316205499891832
Describes a workflow that reads like a preview of where this goes: you write the laws with one agent, turn on an auto-implementer, then turn on auto-research, and you end up with a formally verified, efficient program that has parallelism from the start. Separately he offers the fair criticism of his own enthusiasm — the thing is very hard to use if you are not good at AI workflows, and the average make-no-mistakes agent user who has never heard of these loops will simply be bewildered, which may be fine because they are not the audience.
---
@GiulioRebuffo
https://x.com/GiulioRebuffo/status/2101507400540758244
A one-line reply that captures the real difficulty of applying these loops outside toy settings. Told that a language has the potential to be as fast as C, his answer is to auto-research it — but you need to keep track of a few variables at once, proving time not exploding and good proving coverage, so the auto-research is multivariate. Nearly every published result in this window optimizes a single scalar, and this is the first mention of what happens when you cannot.
---
@hazemomier
https://x.com/hazemomier/status/2101826102545252671
Twelve words that several other people in this window arrived at independently: the agent loop took an afternoon and the production wrapper took two weeks, and that gap is where most we-shipped-an-agent stories die. The demo is tools plus a loop plus a happy path; production is an evaluation harness, tracing, secret injection, tool-server auth, refusal when the context is wrong, and someone on call when it lies with confidence. His forced choice for anyone greenlighting agents is to ship the afternoon demo and add guardrails later, or treat the wrapper as the product because the loop is a commodity.
---
@ZainAkrams
https://x.com/ZainAkrams/status/2101456639194784130
Puts a company-scale number on the same observation. A large engineering org standardized 500-plus internal agent services onto a kit that hands each new service a working agent loop plus evaluation, tracing, secret management and tool-server wiring already done, and wiring a new agent into production went from two weeks or more to about an hour. The details that matter: agents discover tools at runtime from 50-plus servers, every model call goes through one gateway across five providers, a new service is a form that yields a repo with the framework and telemetry already wired, and there is an evaluation endpoint from the first commit. His summary is that people will screenshot the framework announcement while what actually changed is that they stopped solving production once per service — at 500 agents the hard problem moved from how do I build an agent to who owns secrets, tracing and evaluation.
---
@BrainsAndTennis
https://x.com/BrainsAndTennis/status/2101905384105787701
Says the thing about harness innovation that the cost studies imply but do not state: profound KV cache savings stifle a lot of harness innovation, and the agent loop has been effectively frozen for a year and a half despite rapid model progress. His specific feedback is worth keeping. Programmatic tool calling, indexing and in-context tool discovery are common now. It amazes him that compaction still exists at all, and he expects the next round of harnesses to instead keep a very large ring buffer of logs it can search against when context is exceeded. Subagents are mediocre because unless routing is very careful they may not save time or raise accuracy even at higher inference cost, though the next generation of models may be better at delegation provided subagent tools can fork context. And performance degradation from batteries-included harnesses is only partially solved by in-context tool discovery, which is ultimately a band-aid.
---
@SlimAssiliX
https://x.com/SlimAssiliX/status/2101340977994650011
Points at a pricing structure most agent builders will meet by accident. One frontier model has two price tiers separated by a single threshold at 272K input tokens, with input and output both roughly doubling above it — and the cliff is not gradual, it reprices the entire request the moment you cross. In an agent loop that re-sends full conversation history on every step, context accumulates continuously, so step N does not know it just crossed the threshold but your billing does. His sting is that this is the model one major agent API defaults to for long-horizon work, and the architecture that justifies that choice is the one most likely to cross the line.
---
@SlimAssiliX
https://x.com/SlimAssiliX/status/2101299774615892081
The same argument at a smaller scale and it is the cleaner version. Same query, three settings: seven tokens from a fast model, 255 from extended thinking, 603 from aggressive reasoning. For a single query that is manageable, but inside a loop running twelve steps you are not paying a ten times premium, you are paying ten times, times twelve steps, times a context window that re-feeds the full history every turn. The reasoning model did not break your budget; the architecture that called it in a loop did. Switching to a reasoning model without capping steps and context is a billing decision disguised as a model selection decision.
---
@gilesmboumi
https://x.com/gilesmboumi/status/2101299596601241845
Reads a market chart in one sentence and gets the right thing out of it. Open models winning token volume while closed models win spend is the agent-loop economy in one picture: loops are price-sensitive and run around the clock, so the expensive model gets the demo and the cheap one gets the workload. His closing question is the one nobody is answering — the interesting number is not the market share, it is whose margin the loops are arbitraging away.
---
@laoyu4399
https://x.com/laoyu4399/status/2101153814413762578
The lesson of his week, stated plainly: parallelism is free until the quota is not. The multi-agent loop is real, and the surprise is how fast one coordinator plus N workers burns the weekly budget. His question to others is the practical one that has no standard answer yet — are you capping workers per job, or just letting it run and switching harnesses when the first one goes yellow.
---
@vibeconnectfyi
https://x.com/vibeconnectfyi/status/2101145033327984924
The smallest useful piece of advice in the window and probably the one most people should act on. Cap every agent loop with a step budget: set a max iteration count and a wall clock limit, and have the run return its partial state when it hits either. Without a budget one bad tool result becomes an endless retry that burns tokens and never surfaces.
---
@sermakarevich
https://x.com/sermakarevich/status/2101259134125351259
Published the second part of a build-your-own-harness series and the chapter list is effectively a minimum spec for the thing everyone else is theorizing about: how the model sees a tool and the loop that lets it call one and carry on; file and shell tools that create a file, replace one exact piece of text, and run a command with a timeout; a permission gate offering yes, always or no before anything touches your files, with always remembered for the session; and session persistence so you can close the terminal, reopen, resume and still have the conversation.
---
@vraj_ai
https://x.com/vraj_ai/status/2101519151357653446
Notes a lab open-sourcing its coding agent CLI under a permissive licence with a compatible API and interleaved thinking, and his reason for caring is the right one. It is not another chat wrapper; it is the agent loop as a readable codebase. If you are evaluating coding agents, the interesting part is being able to read how they wire tools and planning, not just the model card.
---
@AbuZ8Studios
https://x.com/AbuZ8Studios/status/2101851587366809881
Reports another harness open-sourced the previous day, running one agent runtime across three surfaces — a desktop app, a browser workspace and a terminal CLI — with the CLI source shipped in the repo as a plain directory rather than a submodule. His build advice is the practical bit for anyone poking at these: build the CLI workspace first and only touch the desktop bundle once the agent loop feels right.
---
@bytecrafter_1
https://x.com/bytecrafter_1/status/2102102771621306685
Asks the question that a whole category of new plugins has not answered. Driving a subscription through an SDK means you inherit that agent's own loop, system prompt and compaction, so your harness then wraps a harness and the two disagree about when to trim context. His follow-up is exactly right: does the plugin expose the inner loop's tool results, or just the final turn. Every subscription-bridging plugin shipped this week has to answer that and none of them did.
---
@ravinsharma7
https://x.com/ravinsharma7/status/2101941995388432401
Cuts through a naming fight that was consuming a lot of oxygen. Classifier is a fine term, he says, but people are being unpleasant about it when their alternative is not even a one-to-one match for the thing being described. Calling it a system-one model is also fine if the goal is to redefine agent software architecture rather than just using the typical agent harness and agent-loop primitives. That conditional is the whole substance of the argument.
---
@Dxn1_0day
https://x.com/Dxn1_0day/status/2101118475515167002
Gets to the useful version of the same point without the fight. Not every step in an agent loop needs a generative model; if the task is choosing between structured actions, eliminating JSON prompting, parsing and validation removes a fairly stupid amount of overhead. His last line is the one that should set the research agenda: the interesting benchmark here is end-to-end agent latency, not model intelligence.
---
@akashcorex
https://x.com/akashcorex/status/2101504833383473578
One line that raises the bar on the whole decision-layer story. A fast judge winning on latency and cost is nice, but the harder bar is whether false positives still sneak into the agent loop. Everybody published speed numbers this window and nobody published a false-positive rate.
---
@parthjain_1
https://x.com/parthjain_1/status/2101876574500815342
Spent a weekend reading everything about the new decision model and wrote the explainer the category needed, with two parts that are genuinely useful rather than promotional. The first is the pricing mechanic almost nobody mentioned: all questions run in parallel against the same state in a single call, and the state is charged once rather than per question, so adding a fifth question costs almost nothing — batching thirteen questions into one call came out twelve times cheaper than thirteen separate calls. The second is the limitations page, which he reproduces in full: it cannot count or do arithmetic, does not handle dates reliably, does not generate text, cannot read images or audio, is not hardened against prompt injection in the state, degrades on large or irrelevant state so you must filter first, and a mid-range probability means genuinely uncertain rather than medium intensity. His two operational notes are the ones to steal — pin the exact version rather than the moving alias, because confidence thresholds tuned on one version do not transfer, and log the model and usage on every call so that when answers shift you know whether the model changed.
---
@kunal_twts
https://x.com/kunal_twts/status/2101896690454462947
Three lines that fix the framing everyone else is getting wrong. You can put the decision model inside the agent loop; it is not necessarily the agent; it is the decision layer inside the agent. Most of the enthusiasm this window treated it as a competitor to a frontier model, which is the category error this corrects.
---
@Sunilmehta_695
https://x.com/Sunilmehta_695/status/2101944506807427188
Maps where each piece belongs in an agent loop, which is the most reusable artifact anyone produced on this theme. Observe state — ticket, tool arguments, logs, messages. The fast typed model routes, gates, scores and assesses risk and urgency. The LLM plans, writes, debugs and explains. Tools and APIs execute. Then the loop closes, with the fast model able to re-check before destructive actions. His compression is exact: fast typed ifs and open-ended work are two different jobs.
---
@mukh_higgsfield
https://x.com/mukh_higgsfield/status/2101118918832312559
Points at what he considers the real story in someone else's harness: the risk classifier locked in the closed part of it. He built something similar to sort whether a reported tool is theirs or a hallucinated one before a bug report even gets filed, and his conclusion is worth more than most of the benchmark posts — cheap judgment calls like that save more debugging time than the agent loop itself.
---
@milonspace
https://x.com/milonspace/status/2101144862938800367
Applies useful pressure to the excitement. A lightweight structured-extraction model already did schema in, scores out in one pass, so the real question is calibration inside a tight agent loop rather than who shipped classification first. His ask of the advocates is fair and direct: if the new model is simply stronger on the same task, say that; if the real gap is latency and abstention you can apply to every tool call, that is the part worth stealing.
---
@IndigoYogiArt
https://x.com/IndigoYogiArt/status/2101872919072928066
Solves a problem the evaluation layer has had since it existed: LLM evaluations are too expensive, because the judge model alone costs more than the thing being evaluated. His open-source tool replaces LLM judges with typed decisions — eight evaluations in one request, six hundredths of a cent, milliseconds instead of seconds — and the placement is the point. It runs on every trace, inside the agent loop, rather than as a batch job afterwards.
---
@thoughtcrime___
https://x.com/thoughtcrime___/status/2101758768371704271
Built a game-testing lab on the new decision model and came back with a lesson about evaluation rather than about the model. Running real playtests across two games, the mistakes the tests caught taught him why the bot won is a terrible balance verdict — a win condition is not a balance measurement, and an automated tester that optimizes for the former will happily certify a broken game. He published the runs and a reusable starter workflow.
---
@jaredpalmer
https://x.com/jaredpalmer/status/2101110281300848799
One line that is a good snapshot of where the practice actually is. With an improved small checkpoint almost ready, he set an agent up to do a little auto-research overnight on a serverless compute platform, for fun. No framework, no paper, no benchmark — just spare capacity and a loop pointed at a metric while he sleeps.
---
@iamMrDuncan
https://x.com/iamMrDuncan/status/2101920242557399105
Doing the same thing with a paper trail. He is starting a fresh auto-research run on an older card for a specific quantized model, publishing the baseline up front and being honest about it — the number is horrendous at 10.16 tokens per second, but that is an old architecture running low quants. The experiment is what twenty-four hours of auto-research on two newer boxes yields against it. Separately he notes he has expanded to three experiment boards to parallelize the testing.
---
@rasmus1610
https://x.com/rasmus1610/status/2101341498113421697
The smallest and most honest experiment in the window: he has an auto-research loop running to improve a decision-model task, and the goal for the day is to see whether he can accrue even ten cents. Somebody should be tracking how many of these overnight loops ever clear the cost of running them.
---
@theblazehen
https://x.com/theblazehen/status/2101703453471088951
Floating the idea of an auto-research-at-home network before building it. Each project would have a publicly available reward function plus a marketplace where tokens earned by contributing to other projects buy work on yours — create a 0.2x improvement in someone else's project and earn twenty tokens, then lose one token for every 0.01x improvement other people's agents make on yours. He is explicitly asking whether the idea has legs, and the interesting design question he has not solved is that the reward function being public is exactly what makes it gameable.
---
@okay_lets_ride
https://x.com/okay_lets_ride/status/2101416496001843270
Describes what auto-research looks like once the metric lives on a public ledger. With measurable inference recorded on-chain you can run autonomous experiments as loops: an agent with a measured metric such as profit and loss or liquidity fees, plus a fixed or dynamic inference budget, proposing an experiment every block, hour or day to improve that metric until it hits a failure count or runs out of budget. You can vary frequency, budget, and whether it is one agent or a swarm. The metric is already adversarial and already public, which is a different setting from every benchmark in this window.
---
@signalgaining
https://x.com/signalgaining/status/2101358724589949423
Reports something he says nobody advertised: a frontier general model is shockingly good at robotics with no robotics fine-tune at all, beating most specialist stacks on a pile of benchmark tasks — pick-and-place, drone follow, simulated arms, even messy closed-loop visual control — and yes it is slow. His conclusion is the line that belongs in this feed: the harness really does look like it is melting. If a general model can either fold world models into itself or spin them up on the fly to drive robots, the specialist stack built to compensate for the model stops earning its keep.
---
@sytelus
https://x.com/sytelus/status/2102055500565082599
Makes the largest claim in the window and states the mechanism behind it. He expects all mainstream software to be verified by 2030, to the point that you will not touch an unverified library — and identifies the two hurdles as formalizing specifications and doing it at billion-line scale, both of which he calls ripe targets for an auto-research self-improvement loop. His reason for the confidence is unusual and worth repeating: either AI gets paused, or this has to happen.
---
@signalgaining
https://x.com/signalgaining/status/2101851309561545115
Pushes the same logic one step further and it turns uncomfortable. If a more efficient world model exists, a sufficiently capable general model will find it and absorb it into its own system, or become powerful enough to generate new models on the fly — and he believes that will dwarf any pipeline of techniques humans have been stitching together. Whether or not he is right, this is the cleanest articulation of why hand-built pipelines are a depreciating asset in this framing.
---
@ChrisGPT
https://x.com/ChrisGPT/status/2101620010376389004
A developer-conference wish list that contains the single best measurement request of the window. Alongside asking for continuous learning research — parameterized learning, fast weights, adapters, anything that persistently updates the model rather than ever more sophisticated context compaction — and for computer use to move from screenshot, reason, act toward a continuously perceived desktop combining structured accessibility data with a low-latency visual stream, his fourth item is the one to hold labs to. He wants actual numbers on the auto-research assistant: what fraction of the next model's R&D pipeline is now being completed by AI experiment generation, how much of pipeline delivery is autonomous, and if it is directed at specific research goals, what those goals are.
---
@toolcalls
https://x.com/toolcalls/status/2102088375062696271
Gives the pacing-the-frontier argument a formulation that has not appeared elsewhere. His read is that the pacing being described amounts to burning a hundred billion tokens a day instead of a trillion tokens a day on an auto-research loop for the model to improve itself. Whether or not that is what anyone meant, it converts a policy position into a compute budget, which is a more falsifiable object than the position was.
---
@yifanxu_ephai
https://x.com/yifanxu_ephai/status/2101489665383784565
Dissents from the whole premise of the window, and the dissent deserves to be recorded. The deeper he digs into agent sandboxes and environment harnesses, the less important he thinks the harness is becoming: the upper ceiling is decided by the model's capabilities, and by the runtime substrate that lets the agent loop unlock its limits. If the harness papers are right this is wrong, and if he is right the papers measured cost rather than ceiling.
---
@thaughtexpwai
https://x.com/thaughtexpwai/status/2101521470790807598
Two sentences that name the constraint on self-improvement more precisely than the papers do. Self-improvement that only rewrites the agent loop still bottlenecks on the evaluation harness. The interesting part is when the improvement is a patch you can audit, not a bigger black box.
---
@sansan_sansannn
https://x.com/sansan_sansannn/status/2102001533043028201
Names the engineering insight underneath the recursive-harness result: representing the entire agent loop as something that can be reviewed and revised is the key move, because most current frameworks treat the harness as relatively static scaffolding while this treats it as first-class, versionable and evidence-driven. He also names the two things that will decide whether it holds up — designing evaluators that do not reward verbosity or extra steps for their own sake, and versioning harnesses so you can actually attribute performance changes. Without both, he says, you just get an ever more complicated spaghetti of prompts and tools that nobody can debug.
---
@tanjil6t99
https://x.com/tanjil6t99/status/2102006456753250559
Compresses the distinction the whole window kept circling into four lines. Recursive self-improvement is the endgame; recursive harness improvement is the path that can ship now. Same model, better loop, then let real outcomes decide whether the change was actually an upgrade. That last clause is the part most of the enthusiasm skips.
---
@latentumx
https://x.com/latentumx/status/2101344255440728553
Objects to a benchmark's name on grounds that turn out to be substantive. You cannot literally call it a recursive-self-improvement benchmark, because that term means improving the model itself with the weights definitely changed — this is an auto-research benchmark, or whatever long-horizon benchmark with a clear verifiable signal. The distinction holds up: every result in this window improved something around the model while the weights stayed exactly where they were.
---
@Vatsalpandya333
https://x.com/Vatsalpandya333/status/2102129016694317200
One sentence that belongs on the wall of every team running these loops: if you cannot see what the agent changed, you also cannot own what it broke. Diffs are the minimum unit of accountability. Set against the same window's auto-research results, where the agent edits the training script and commits improvements by itself, this is the cheapest possible safeguard and almost nobody named it.
---
@MTorygreen
https://x.com/MTorygreen/status/2102050797634678990
States the accountability half in the same breath. More autonomy should not turn into less accountability: if a lab gives an agent the tools, permissions and room to act, it still owns what happens when things go sideways, and the agent did it cannot be the escape hatch. The whole window is about handing more of the loop to the machine, and this is the only post that asks who signs for it.
---
@PedroLaRosaDev
https://x.com/PedroLaRosaDev/status/2101939862060273855
A comparison of two harnesses from someone running both daily, and it earns its length by being specific about tradeoffs rather than declaring a winner. One vendor's usage limits last much longer when used properly and its chat app has a better desktop experience; the other provides a more mature platform for programming or building tools with an agent, with a cloud mode plus a swarm option that keeps working without depending on your devices, a more mature CLI, and a plan-with-one-model implement-with-another strategy that adheres to your rules. The real tradeoff he names is lock-in: one vendor's models are locked to its own platform and work perfectly there, while the other's subscription can be spent through third-party harnesses, which matters if you want independence. His conclusion follows from that honestly — he prefers the first for the work itself, and says the reason to switch is if you are building a harness that must not depend on any single vendor.
---
@GodsBoy7777
https://x.com/GodsBoy7777/status/2102130909143011637
Documents a plugin pattern that several people shipped this week and nobody else described this cleanly: the coding agent keeps the subscription login, while the other runtime keeps the agent loop, tools, approvals and compaction. Credentials stay put with no separate API key, subscription limits and overage still apply, and the plugin is experimental. In effect one vendor supplies billing and the other supplies the loop, which is a split the subscription terms were not written for.
---
@sakshjn
https://x.com/sakshjn/status/2102107952538845539
Names what that pattern adds up to. One vendor's SDK is quietly becoming the substrate everyone builds their agent loop on, and wiring a subscription straight into a third-party harness is the part that actually matters. Substrate is the right word: whoever owns the layer everyone else builds their loop on top of has a position that does not depend on winning any particular benchmark.
---
@tsella
https://x.com/tsella/status/2101274078724153614
A non-coding loop with real mechanics. His meal-tracking agent pushes at 8am with basal metabolic rate, total daily expenditure and protein targets pulled from his watch alongside a weight trend; he sends a photo and gets macros estimated, logged, and remaining calories returned; at 10pm it produces an in-versus-out graph and a what did I miss prompt. It is timezone aware and, the part that makes it a loop rather than a logger, expenditure adapts from the weight trend rather than staying a fixed target.
---
@ZaneOnAI
https://x.com/ZaneOnAI/status/2101983791661081062
Points at five workshops on building self-improving agentic systems from scratch, and the running order is the useful artifact: ship your first agent, then self-improving agents through tools and skills, then memory, then a proactive agent, then making it autonomous. Note the sequence — memory lands third, after self-improvement rather than before it, which is the opposite of how most people build these.
---
@cHHillee
https://x.com/cHHillee/status/2102161884740977120
Names the infrastructure requirements for a self-improvement loop in three clauses, and they are not the ones people usually list. You want the auto-research loop to be unbounded by your practical compute constraints, to autoscale up and down instantly and trivially, and to have very quick iteration loops. Nothing about model quality — every item is about the elasticity of the substrate underneath.
---
@realcalebwin
https://x.com/realcalebwin/status/2101817952140193993
Points at how early this all is with one observation. He is bullish on auto-research for systems, and notes how rare it is for an engineering team to deploy even a single continuously optimized, extremely small footprint decision model running around the clock. Everyone in this window is discussing recursive harness discovery, and almost nobody has the one always-on optimizer that would be step zero.
---
@AhmedMa34437965
https://x.com/AhmedMa34437965/status/2102063079890751717
A short proposal aimed at the review flood that is more actionable than most of the long ones. Let the authors pay the auto-research agent cost, and if a repository is flagged as dangerous without big failures, it goes into human review with model assistance. Pricing the submission and triaging on evidence rather than on prose is a different lever from everything else proposed this window.
---
@Shadowfetch
https://x.com/Shadowfetch/status/2101560117116170432
Asks the right follow-up question about a local agent result. The memory constraint is the interesting part, because if the full context and agent loop stay resident that changes the economics of local tools rather than just the benchmark score — and he wants to know how much of the reported throughput holds once the agent starts leaning on disk and network. Every local-model agent claim in this window was measured before that point.
---
@TonyJZhou
https://x.com/TonyJZhou/status/2101697122886418637
Reads someone else's failure screenshots correctly, which is a skill this field needs more of. Same machine, multiple sessions, same failure shape — that is not sampling noise, it is shared state: model, harness, tool cache, some shared layer under the agent loop. His question is the one that would actually isolate it: what did the failing sessions have in common besides the weights.
---
@bigini01
https://x.com/bigini01/status/2102147498810773556
Names a delegation problem that the multi-agent enthusiasm has not addressed. He could approve one agent and end up with four other agents doing the actual work without ever knowing who touched what. Set against this window's collective-research results where thirteen workers pass work to each other through a shared commit graph, this is the version of that architecture as seen from the consent side.
---
@0x_tony_
https://x.com/0x_tony_/status/2102147383274430911
The same point with the forensic consequence attached: imagine trying to trace where the mistake happened after three different agents have touched the job. The collective-research systems in this window solve exactly this with an immutable commit graph, and the consumer-facing agent products solve it not at all.
---
@itzSaasified
https://x.com/itzSaasified/status/2102006713230459231
One line that names the missing half of every agent demo: the invisible repair layer is what turns demos into a product people can trust, and everyone posts the shiny agent loop while almost nobody shows the recovery code. Read next to the production-wrapper posts higher up, the wrapper and the repair layer are the same thing seen from two angles.
---
Eco Products Radar

SoL-Pi — the recursive auto-research harness result that organized the window, covered from at least a dozen angles. Four surviving mechanisms: action fusion, online context compaction, observation packing, and an evidence-preserving log reducer. Headline numbers: 44.7-49% less token traffic, roughly one third lower API cost, 93.7% of baseline score, and clean transfer across vendors.

Jev / TypeSafe — the decision model, discussed here specifically as a component inside the loop rather than as a chat competitor. Real integrations this window: harness routing, evaluation replacement, browser and desktop control, game-balance testing, and one honest negative result inside a text-to-SQL loop.

Agora — version control as shared memory for collective auto-research. Thirteen workers, twelve days, 1,703 contributions, 145 commits in the winning ancestry, 165 independent reproductions, and one well-argued caveat about reused development data.

Pi — the minimal harness that keeps appearing as the baseline everything else is measured against, including the harness paper's own comparisons.

Karpathy's autoresearch — still the reference implementation of the overnight loop: one GPU, one markdown instruction file, five-minute capped runs, keep if better and revert if not. 700 experiments and 20 genuine improvements in one public overnight run.

EdgeBench / Terminal-Bench — the two evaluations the efficiency claims were measured on, both quoted repeatedly with per-task cost rather than raw score.

Hermes — the runtime most of the non-coding loops in this window ran on, including a meal-tracking loop whose expenditure target adapts from a weight trend.

Bend — an auto-implement plus auto-research workflow producing formally verified parallel programs, with its own author supplying the fair criticism that it is very hard to use without existing agent-workflow skill.
