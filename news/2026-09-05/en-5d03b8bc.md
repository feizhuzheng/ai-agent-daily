---
title: "Claude Formalized Fermat's Last Theorem. All of It. In 11 Days"
date: 2026-09-05
lang: en
source: https://clauday.com/article/5d03b8bc-acfb-4947-bbbf-9437f1980986
tags: [Research, Agents]
---

# Claude Formalized Fermat's Last Theorem. All of It. In 11 Days

> 来源 / Source: https://clauday.com/article/5d03b8bc-acfb-4947-bbbf-9437f1980986

Anthropic published the first complete computer-checked proof of Fermat's Last Theorem on September 4 (https://www.anthropic.com/research/formalizing-fermats-last-theorem). Claude agents did it autonomously in 11 days: 13 million lines of Lean — more than five times the size of Mathlib, the entire accumulated library of formalized mathematics — proving 30,300 theorems, of which 29,500 made it into the final proof. Total spend: about six billion output tokens, from an internal research model Anthropic describes as roughly comparable to Fable 5.1.

For calibration on how absurd that timeline is: Kevin Buzzard, the Imperial College mathematician leading the human FLT formalization effort, launched his community project expecting it to take many years. FLT is the Everest of proof formalization, resting on decades of modern number theory. Anthropic partnered with Buzzard and with Columbia researchers who built Prove2Me, an open collaborative platform that organizes the work as directed theorem graphs. Buzzard's verdict: "If the automatic formalization of FLT is possible now, then we have taken a big step towards automatic formalization of the modern mathematical literature."

The most honest number in the post is worth more than the headline: failed attempts account for about 7% of the non-boilerplate lines. The agents wandered, hit dead ends, backed out — and still converged, because Lean is a perfect verifier. Every one of the 13 million lines passes a compiler that cannot be sweet-talked, which is why an artifact no human team could hand-check is trustworthy anyway.

That is the transferable lesson for anyone building agents outside mathematics. Where a hard verifier exists, agent autonomy scales to eleven unsupervised days and six billion tokens. Where one does not, you get a German wiki full of agents trading exam answers. Both stories, same week.
