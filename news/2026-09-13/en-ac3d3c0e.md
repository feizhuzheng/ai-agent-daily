---
title: "YuE2 Lets You Argue With the Song"
date: 2026-09-13
lang: en
source: https://clauday.com/article/ac3d3c0e-9eb9-4d5f-a687-07d824d7e7ed
tags: [Agents, Open Source, Tool]
---

# YuE2 Lets You Argue With the Song

> 来源 / Source: https://clauday.com/article/ac3d3c0e-9eb9-4d5f-a687-07d824d7e7ed

multimodal-art-projection/YuE picked up around 500 stars in a day to reach 7,694, on the back of the YuE2 line that shipped as yue2-v0.1.6 on September 9. The music-generation part is the headline. The part that matters for anyone building agents is the architecture: YuE2 generates an editable symbolic plan and then renders it, which means the thing between you and the output is a document you can argue with. https://github.com/multimodal-art-projection/YuE

Three capabilities ship. Song creation from lyrics. Zero-shot cover generation from a transcribed melody. And agentic composition revision, which is the one that changes the interaction model — instead of re-rolling a prompt and hoping, you edit the plan and re-render the part you touched. Anyone who has fought a text-to-music model knows the failure mode: you like 80% of a take, one section is wrong, and your only lever is regenerating the whole thing with slightly different words. Making the plan a first-class, inspectable artifact removes that.

This is the same structural idea showing up everywhere agents are getting useful. [Spec-driven skill packages](https://clauday.com/article/6fc3ef79-0239-4bcb-b4bf-f6c12ecb4fd0) put the intermediate artifact in a folder you can review. [Show-Harness argued robots need a better interface, not a new model](https://clauday.com/article/66aa6315-7239-4f06-a8aa-503c9c8e0ef3). The generalization is that end-to-end generation is great at drafts and terrible at revision, and the fix is always the same shape — expose the plan, let humans and agents edit the plan, regenerate from the plan.

Practical details. Python 3.12, distributed as a wheel, weights on Hugging Face under the m-a-p organization, and the release notes cite 172 passing installed-wheel tests with 11 skipped plus fresh GPU runs for generation, cover and editing. The README was updated September 11 with WildSongBench comparisons against Suno v6. Licensing is the catch and it is a real one: first-party YuE2 components are CC BY-NC 4.0, so this is research and personal use, not a commercial pipeline. The older YuE-v1 model, code and docs stay where they are.

Treat the benchmark claims against a closed commercial system with the usual suspicion — a self-published comparison to Suno v6 is a starting point for your own listening test, not a result. The editable-plan design is the part that stands on its own regardless of how the audio scores.
