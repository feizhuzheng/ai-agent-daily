---
title: "Cognition's SWE-2 Runs on Kimi K3, and That's the Whole Story"
date: 2026-09-10
lang: en
source: https://clauday.com/article/6a998ccf-b793-4da4-9f00-97b27af81532
tags: [Coding, Agents, Benchmark]
---

# Cognition's SWE-2 Runs on Kimi K3, and That's the Whole Story

> 来源 / Source: https://clauday.com/article/6a998ccf-b793-4da4-9f00-97b27af81532

Cognition shipped SWE-2 on September 10, and the number everyone will quote is 92.8 on Terminal-Bench 2.1, up from 81.5 for SWE-1.7. The number that actually matters is buried one paragraph down: the base model is Kimi K3, 2.8 trillion parameters, made in China and open-weight.

An American coding-agent company valued at 48 billion dollars post-training a Chinese open-weight base and beating GPT-5.6 Sol and Fable 5.1 on price is not a footnote. It is the clearest evidence yet that the frontier lab moat is the RL recipe and the harness, not the pretrain. Cognition says this is the first time anyone has scaled reinforcement learning to a multi-trillion-parameter base. They did not have to spend a billion dollars getting there. They rented the floor from Moonshot.

The efficiency numbers are the real product. SWE-2 needs 58 percent fewer steps than SWE-1.7 on average and costs 81 percent less per task, and against Fable 5.1 it lands similar FrontierCode 1.1 scores at 64 percent lower cost. On DeepSWE 1.1 it goes from 37.7 to 73.0, which is not an improvement, it is a different model doing a different thing. Cognition frames the whole release as Pareto-frontier work rather than ceiling work, and the training story matches: they optimized for focused exploration, meaning the agent stops reading the entire codebase before it touches anything.

Available now in Devin Desktop, CLI, Web, and Fusion. Read it at https://cognition.com/blog/swe-2

The awkward part is that Cognition raised a 2 billion dollar Series E last week on the thesis that coding agents are not winner-take-all, and SWE-2 proves them right in a way that also undercuts everyone selling frontier pretraining as the differentiator. If a 200-person company can take an open Chinese base and land within spitting distance of the labs at a third the price, the question stops being who has the best model and becomes who has the best loop.

Related reading: https://clauday.com/article/d619f8b7-7b67-4ac7-9507-66e8828bd6c6 and https://clauday.com/article/80d51dcd-2aa8-48dd-a28e-60bbe66d4ef5 and https://clauday.com/article/201fb8b0-063b-4eb9-be4c-3925ee84fd97
