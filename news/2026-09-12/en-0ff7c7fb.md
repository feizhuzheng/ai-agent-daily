---
title: "Predict the Concept, Not the Token"
date: 2026-09-12
lang: en
source: https://clauday.com/article/0ff7c7fb-8453-4a7c-9d03-4c26eee5cb6e
tags: [Research, Open Source]
---

# Predict the Concept, Not the Token

> 来源 / Source: https://clauday.com/article/0ff7c7fb-8453-4a7c-9d03-4c26eee5cb6e

Top of Hugging Face's daily papers with 231 upvotes: NCP-ArchPreview, from the Intern-NCP team, 27 authors, submitted September 9. Paper at https://arxiv.org/abs/2609.10715 . The pitch is that next-token prediction is not the only objective a language model should be trained on, and they built an 8.9B model on 5.73 trillion Dolma-3 tokens to argue it.

The mechanism is next concept prediction, running alongside ordinary next-token prediction rather than replacing it. They build a concept vocabulary by product-quantizing the model's own hidden states, so a concept is a discrete code derived from what the network already represents, not a human-labelled category. Then a dedicated Concept Module predicts the next concept, which means the model is explicitly being asked to guess a multi-token chunk of what's coming, not just the immediately next symbol.

The numbers are the reason this is at the top of the board. It reaches OLMo-3-7B's final pretraining loss using 51.3 percent of the tokens. Half the data for the same loss. It then beats OLMo-3-7B by 2.45 points on the downstream macro-average, and by 5.99 points on GSM8K specifically, which is the kind of gap that suggests the concept objective is buying something structural on multi-step reasoning rather than just smoothing perplexity. They also report matching an 8.9B baseline with about 85 percent of the compute.

The two spin-off results are the ones an engineer will actually use. A 17M-parameter VQ module on top of the learned latent space does lightweight domain adaptation, which is a very cheap knob compared to any form of fine-tuning. And feeding concept representations into speculative decoding improves mean accepted length by 4.17 percent, which is free inference throughput on an existing serving stack. That second one is notable because it is a latent-space idea cashing out as a plain systems win.

Worth being calm about it. This is an architecture preview from a team reporting its own results at 8.9B, and half-the-tokens claims have a long history of shrinking when someone else runs them at a different scale with a different data mix. But the objective is a real structural idea rather than a tuning trick, and if the data efficiency holds anywhere near 51 percent, that's the sort of thing that changes what a pretraining budget buys. Worth watching who reproduces it.
