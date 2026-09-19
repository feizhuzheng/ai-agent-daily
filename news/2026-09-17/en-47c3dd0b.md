---
title: "Bend Makes the Agent Prove It Didn't Break Your Rules"
date: 2026-09-17
lang: en
source: https://clauday.com/article/47c3dd0b-fdcc-42fd-9f2f-69b6539cff84
tags: [Coding, Framework, Agent-Operable]
---

# Bend Makes the Agent Prove It Didn't Break Your Rules

> 来源 / Source: https://clauday.com/article/47c3dd0b-fdcc-42fd-9f2f-69b6539cff84

Bend describes itself as a fast language that blocks AI mistakes via proof, which sounds like three unrelated pitches stapled together until you see how it works. Site at https://bend-lang.com/ , source at github.com/bendlang/bend, and it took 139 points on Hacker News overnight.

The mechanism is simple enough to explain in a sentence. You write your invariants into a file called LAWS.bend: the properties that must never break, stated formally. Before code merges, the agent has to run bend PROOF.bend and produce a machine-checked, Lean-style proof that its changes do not violate them. Their demo is a game with a law stating that winning is impossible, and the system refuses any implementation change that would break that proven invariant. Not flagged. Not warned about. Refused, because the proof does not close.

This is the enforcement-over-instruction argument in its purest available form, and that argument has been piling up evidence all month. You cannot write "never break the invariant" in a system prompt and mean it, because a prompt is a request and a proof obligation is a wall. The interesting design consequence is what it does to review: instead of a human reading a diff and trying to imagine what it might break, the machine either produces the proof or it does not, and the human's job moves up a level to deciding which laws are the right laws. Your understanding of the problem becomes the artifact. The code becomes negotiable.

The other half is performance, and it is the reason this is not just a verification toy. Bend claims C-level speed, compiles to a parallel runtime, and runs the same binary across CPU cores or GPU kernels without anyone hand-writing kernel code or managing threads. Proof-carrying code has historically been where your throughput goes to die, so pairing the guarantee with CUDA-class parallelism is the bet that makes it worth trying.

Temper accordingly. The project says outright that it is still evolving and that bugs are expected, the page carries no version number and no explicit license, and there is no named organization behind it, only a repo and a Discord. There is also a very hard unanswered question underneath the whole idea, which is who verifies that LAWS.bend says what you actually meant. The proof is only as good as the laws, and writing correct formal specifications is the part of this that has defeated people for forty years.
