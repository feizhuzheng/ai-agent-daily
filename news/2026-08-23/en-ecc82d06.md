---
title: "Somebody Finally Wrote Down What a Harness Actually Is"
date: 2026-08-23
lang: en
source: https://clauday.com/article/ecc82d06-f5e4-42ab-b05c-d8e0f036f74e
tags: ["Agents", "Framework", "Open Source"]
---

# Somebody Finally Wrote Down What a Harness Actually Is

来源 / Source: https://clauday.com/article/ecc82d06-f5e4-42ab-b05c-d8e0f036f74e

We have been saying the word harness for months on this site without ever nailing down what it means. Earendil, the small team behind the open-source Pi coding agent, just fixed that with the cleanest definition going around. Agent equals model plus harness. The model is the raw brain. The harness is the software it lives inside, and that software is the part almost nobody talks about but everybody depends on.

They break the harness into four pieces. A system prompt, which is the model's onboarding doc telling it who it is and how to behave. Tools, the actual code it can call to search the web, run a script, send an email. An agentic loop, the machinery that lets it call a tool, look at what came back, and decide what to do next instead of answering in one shot. And a translation layer, so the same harness can drive Fable today and GLM tomorrow without a rewrite. That last one is the sleeper. It is what turns a harness from a wrapper around one lab into something model-agnostic.

The name comes from climbing, and the analogy does real work. A climbing harness holds you up, keeps you on route, and catches you when you slip. An agent harness does the same for a model that would otherwise wander off a cliff. But the punchline is political, not technical. If you can own and run your own harness on your own machine, you keep your agency. You are not renting your workflow from whichever lab controls the app. You can swap the brain, keep your logs, and set your own rules.

This lands the same week NVIDIA showed a custom harness dragging Claude Opus 5 from 30 percent to 100 percent on ARC-AGI-3, and Google's EnvHarness argued the environment matters more than the agent. The whole field is converging on one idea: the unit of capability is not the model, it is model plus harness. Earendil's contribution is to say the quiet part out loud, that of those two, the harness is the half you can actually own. Read it at earendil.com/posts/what-is-a-harness.
