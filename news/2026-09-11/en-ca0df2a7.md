---
title: "Three People Built AI Filters for Hacker News on the Same Day"
date: 2026-09-11
lang: en
source: https://clauday.com/article/ca0df2a7-714a-4d25-9a63-f669999d9e00
tags: [Tool, Open Source, Monitoring]
---

# Three People Built AI Filters for Hacker News on the Same Day

> 来源 / Source: https://clauday.com/article/ca0df2a7-714a-4d25-9a63-f669999d9e00

On September 11, three separate front-page submissions did the same thing: strip AI content out of Hacker News. unslop.news by Ayden Diel, hcker.news with an ai=exclude toggle, and a reduced-priority-for-AI-content reranker on sprinklz.io. They landed within an hour of each other, took 160, 161 and 101 points, and none of the authors appear to have known about the others.

The most quotable number in the whole cluster is on unslop's own front page: 84 of 180 submissions survived the filter. Slightly under half of Hacker News, by one person's definition of AI content, is AI content. You can argue with the classifier all you want, and the comments did. The fact that three people independently shipped the same tool on a Friday is the actual signal, and it is not about the classifier's precision.

There is a fork in what these filters are for that nobody has resolved. Filtering AI-generated slop, meaning spam posts and machine-written blog filler, is uncontroversial and basically a moderation problem. Filtering AI as a topic is something else entirely, and on a site where a majority of the interesting engineering work right now involves agents, it is a deliberate choice to read a smaller internet. The submissions blur the two, which is why the threads are 70-plus comments of people talking past each other.

Same day, same front page: 25 Fields Medallists signed a declaration saying AI output is outrunning the human capacity to absorb it, a post called Feeling Sad About AI took 163 points, and a code-quality study found agent code is twice as eroded as human code. That is not a coincidence, it is a mood with four expressions. The builders' version of the mood ships a filter. Try them at https://www.unslop.news/ and https://hcker.news/?ai=exclude

Related reading: https://clauday.com/article/f1941f13-5e8d-44f5-8f2d-37c46264b4e6 and https://clauday.com/article/accb0b58-0840-482e-b574-40738256cd2d
