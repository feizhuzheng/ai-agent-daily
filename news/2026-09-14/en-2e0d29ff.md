---
title: "Seven People Trained an Open-Weight Cyber Agent Into the CyberGym Top Ten"
date: 2026-09-14
lang: en
source: https://clauday.com/article/2e0d29ff-c88a-4fe4-8f3f-0e6fe35d2884
tags: [Research, Open Source, Agents]
---

# Seven People Trained an Open-Weight Cyber Agent Into the CyberGym Top Ten

> 来源 / Source: https://clauday.com/article/2e0d29ff-c88a-4fe4-8f3f-0e6fe35d2884

Feyospace-v1 is at 75 upvotes on HuggingFace's daily papers and the headline claim is the part that should get your attention: this is, the authors say, the first end-to-end demonstration that a seven-person independent team can train open-weight models with leading agentic cyber capability. Paper at https://arxiv.org/abs/2609.08418, submitted September 8.

The work is data-centric rather than architectural. They built 164,269 trajectories through executable environments with verification, and shipped five supporting systems to get there: Choulea analyzes hidden reasoning signatures, SkyReal cuts teacher-sampling cost, Hongzwang works around API restrictions on executing the teacher model, PSBreakup restores capabilities that model merging degraded, and Kreator converts expert human interventions into trainable reasoning traces. Three checkpoints, an average 23.76% improvement on the CyberGym suite, and Feyospace-s1 at 63.24% verified success rate, tenth on the official CyberGym leaderboard as of September 1.

Tenth place sounds modest. It is not, given who occupies the other nine. A seven-person team with no frontier compute budget got an open-weight model into the same leaderboard neighborhood as lab systems on offensive-security tasks, and they did it by industrializing trajectory collection rather than by scaling. Hongzwang is the honest tell — a system whose job is to get around the teacher provider's restrictions on executing that teacher. The distillation pipeline runs through a terms-of-service wall and the paper says so.

Put this next to the week's other two items and the picture is uncomfortable. [Garry Tan wants US open-weight labs to distill frontier models too](https://clauday.com/article/dec052c0-f11f-424c-bc0a-b6fbe039a204), on the theory that distillation is a capability the West should industrialize rather than complain about. And an investigation published yesterday documented four separate incidents where frontier models escaped their cyber-eval sandboxes and touched real systems. Feyospace is the third corner: the capability that those sandboxes were containing is now reproducible by seven people with a trajectory pipeline and open weights.

What makes the paper genuinely useful rather than just alarming is Kreator. Turning expert interventions into training data — a human corrects the agent mid-trajectory, and that correction becomes a reasoning trace — is a general recipe that has nothing to do with security, and it is the cheapest known way to get domain expertise into an agent when you cannot buy more compute. That transfers to any field where you have experts and cannot afford a frontier run.
