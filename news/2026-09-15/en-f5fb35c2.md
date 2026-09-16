---
title: "A Model That Can't Hallucinate, Because It Doesn't Write Words"
date: 2026-09-15
lang: en
source: https://clauday.com/article/f5fb35c2-fd03-4b36-b7a4-1ded3631d078
tags: [Agents, API, Infrastructure]
---

# A Model That Can't Hallucinate, Because It Doesn't Write Words

> 来源 / Source: https://clauday.com/article/f5fb35c2-fd03-4b36-b7a4-1ded3631d078

Typesafe AI came out of nowhere on September 15 with a model called Jev and a category name to go with it: System One Models. The pitch at https://typesafe.ai/blog/introducing-system-one-models-and-jev is that everything we call an LLM is built for a human reader, and the overwhelming majority of actual production calls are not a human reading anything. They are a piece of software asking a question and needing a typed answer back. Jev takes unstructured state in and emits typed probabilistic decisions out. It is a frontier-intelligence function call, not a chatbot.

The founder is Diogo Almeida, formerly of OpenAI. The technical claim that matters is that Jev cannot hallucinate or emit a type error — not "rarely does," but cannot, because the output is schema-constrained by construction and sampled in parallel rather than token by token. Every decision comes with a calibrated confidence score, which is the part builders should care about most. A calibrated number is what lets your code decide on its own when to act and when to escalate to a human, and right now most agent stacks fake that with a prompt and a vibe.

The numbers are absurd enough that you should want to see them reproduced. 70 to 500 milliseconds per call. Input at $0.042 per million tokens with output tokens free, which the site advertises as 238 times cheaper than Claude Fable 5.1. On their own workflow evals they claim up to 193.6x faster and 444.6x cheaper on production workloads. Parallel sampling explains the latency and the free output, since there is no long autoregressive tail to pay for.

Whether or not those exact multiples hold, the framing is the interesting part and I think it is correct. Most agent cost today is spent making a frontier model produce three tokens of JSON that decide a branch. That is a Ferrari idling in a drive-through. [Somebody spent $1,500 proving the advertised token savings in agent stacks aren't real](https://clauday.com/article/7d06a720-8150-4bd1-be47-1778c3923045), and this is the other end of the same problem — not compressing the context, but refusing to use a prose model for a decision that was never prose.

Caveats, and they are real ones. No open weights, no independent benchmark, early access by waitlist only, and "mathematically impossible to hallucinate" is a claim about format, not about being right. A schema guarantees you get a valid enum value back. It guarantees nothing about whether it is the correct enum value, and the calibration curve is the only thing standing between those two. Get on the waitlist, but grade it on calibration under distribution shift, not on the price tag.
