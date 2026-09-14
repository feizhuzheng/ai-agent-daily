---
title: "Colibrì Streams a 2.8 Trillion Parameter Model Off Your SSD"
date: 2026-09-13
lang: en
source: https://clauday.com/article/12b34edb-6c27-4274-baec-314830b9d492
tags: [Infrastructure, Open Source, Tool]
---

# Colibrì Streams a 2.8 Trillion Parameter Model Off Your SSD

> 来源 / Source: https://clauday.com/article/12b34edb-6c27-4274-baec-314830b9d492

JustVugg/colibri went to 29,655 stars this weekend, up about 960 in a day, and shipped v1.11.0 on September 13. The pitch on the repo is six words long: run frontier MoE models on hardware you already own. Pure C, zero dependencies, Apache-2.0, and a project that did not exist before July 1 of this year. https://github.com/JustVugg/colibri

The idea is one of those reframings that sounds obvious after somebody does it. A mixture-of-experts model only activates a slice of itself per token, so treating VRAM, RAM and disk as three separate places is the wrong mental model. Colibrì treats them as a single multi-tier hierarchy: the dense trunk lives in RAM, the routed experts get streamed off storage on demand. Nine model families are supported, including Kimi K3 at 2.8 trillion parameters, Inkling at 975B, GLM-5.2 and 5.3, DeepSeek V4 Flash, Qwen variants and OLMoE.

What makes it credible is that the numbers are published end to end, including the embarrassing ones. Six RTX 5090s with full residency gets you 5.8 to 6.8 tokens per second. A 128GB CPU-only desktop does about 1.8. A single RTX 5070 Ti does 1.07. A 25GB laptop does 0.05 to 0.1 tokens per second, which the README publishes as the baseline rather than hiding. Nobody is running a coding agent at a tenth of a token per second. But the point of the low end is that the model loads and runs at all, on a machine you would otherwise call unqualified.

The v1.11.0 release is the kind of changelog that tells you a project is past the demo stage. DeepSeek V4.1 Flash was added as the ninth engine with no conversion step — the released checkpoint is read natively, fp8 dense in 32x32 ue8m0 tiles with fp4 experts — and a single turn went from 78.7 seconds to 25.1 through optimization, with multi-turn chat landing at 1.14 to 1.58 tokens per second. The rest is unglamorous and reassuring: a Qwen36 expert-cache bug that corrupted memory on warmstart, Metal segfaults on raw float32 tensors, a GLM-5.3 teardown leak, RAM detection fixed across all three platforms. Fifty-six pull requests from 16 contributors since v1.10.2, which was 7 days earlier.

Put it next to [the four-SSD streaming setup we covered last week](https://clauday.com/article/ca7fd597-8ae5-40fc-997a-97b01da6bdbd) and a pattern is forming that matters more than either project. The constraint on running a 2.8T model at home stopped being memory capacity and became storage bandwidth and scheduling. That is a much cheaper constraint to buy your way out of, and it is the reason the "you need a datacenter to run open weights" line has quietly become false for anyone willing to accept a token per second. The tokens-per-second number is what decides whether this is a toy — one per second is unusable for interactive agents and perfectly fine for an overnight batch job you read in the morning.
