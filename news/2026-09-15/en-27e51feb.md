---
title: "Gemini Can Now Say “Let Me Check That” and Actually Go Check"
date: 2026-09-15
lang: en
source: https://clauday.com/article/27e51feb-e16b-4a99-8776-993a7d357a98
tags: [Agents, API, Benchmark]
---

# Gemini Can Now Say “Let Me Check That” and Actually Go Check

> 来源 / Source: https://clauday.com/article/27e51feb-e16b-4a99-8776-993a7d357a98

Google shipped Gemini 3.8 Live and Gemini 3.8 Live Extended Thinking on September 15 at https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-3-8-live-gemini-3-8-live-extended-thinking/. One is tuned for scale and cost, the other for multi-step reasoning. Both do near real-time voice with visual grounding and automatic language detection across 97 languages. The feature that actually matters is buried: background tool execution.

That is the whole trick, and it is worth spelling out. Voice agents have always had a structural problem that text agents don't. If a tool call takes four seconds, a text agent shows a spinner and nobody minds. A voice agent goes silent for four seconds and the human on the other end assumes the call dropped. The Extended Thinking variant handles this by running the tool in the background and filling the gap verbally — saying "let me check that" the way a person would, then coming back with the answer. Conversational filler as a latency-hiding mechanism is a genuinely good piece of interface design.

The numbers back it up where it counts. 82.6 on Artificial Analysis speech-to-speech quality, which is first place. 97.7% on Big Bench Audio. Second on Speech Agent Arena. But the agentic ones are the honest ones: 68.6% task completion on τ-Voice and 35.1% on Sierra's τ-Voice-banking. That banking number is the one to remember. Two out of three banking tasks still fail, on a benchmark built by the people who sell voice agents, with a model that just took first place on speech quality. Sounding human and completing a transaction remain very different problems.

Availability is immediate across Gemini API and AI Studio for developers, private preview in Gemini Enterprise, and it is already live behind Search Live, Gemini Live and Workspace. Pricing is described as competitive without a number attached, which is Google's usual way of saying check the pricing page later.

This is the fourth Gemini release in the 3.x line in about seven weeks, after [3.8 Flash and Flash Cyber at the start of the month](https://clauday.com/article/59b9da60-f8ba-4d25-a47a-4a45982a48a8). The cadence is starting to say something on its own. Google is shipping narrow, task-shaped variants faster than anyone is evaluating them, and picking the right one is becoming a real engineering decision rather than a default. [The same week Apple built a socket to let a competitor's model drive Siri](https://clauday.com/article/986b310a-1798-4672-a49d-281a3e456fb0), voice stopped being a feature and became a market.
