---
title: "nobuzz: a Second AI to Shut the First One Up"
date: 2026-08-21
lang: en
source: https://clauday.com/article/8c6fbd7e-f05a-4c5c-9b92-a320ff8b5687
tags: [Tool, Open Source]
---

# nobuzz: a Second AI to Shut the First One Up

> Source: [clauday.com](https://clauday.com/article/8c6fbd7e-f05a-4c5c-9b92-a320ff8b5687)

The funniest repo on Hacker News today is also a real datapoint. nobuzz, by Adnan Akil, adds a /debuzz command to Claude Code that takes Claude's last response and pipes it through the Gemini CLI to translate it from — the README's words — millennial clickbait into regular English. The pitch: Claude is a great engineer with one incurable condition. It talks like it's delivering a TED talk about its own pull request. 148 points and 104 comments say the diagnosis landed.

Sit with the architecture for a second: a user deploying Google's model as a linter for Anthropic's model's personality. Cross-vendor, adversarial, and running locally as a skill. We've written about model routing as an economics story all month — this is model routing as couples therapy.

The comment thread is better than the repo, honestly. The consensus practical fix is hard word limits — cap comments at seven words and user-facing strings at ten and the fluff dies at the source. Several people pointed out the style guidance doesn't survive long contexts: as the conversation grows, Claude drifts back to its trained voice no matter what the system prompt says. Which is the real finding here — personality lives deeper than instructions, so users are reaching for enforcement layers instead: hooks, linters, and now a rival model on debuzz duty.

Model personality became a product surface this year — we covered the "Why Opus 5 Feels Worse" debate and Anthropic shipping release notes for the system prompt. nobuzz is the community's answer: if the vendor tunes the voice and the prompt can't hold it, wrap it. Everything gets a harness eventually, even the vibes.

Repo: https://github.com/adnanakil/nobuzz
