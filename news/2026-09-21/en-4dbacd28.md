---
title: "Linear's test suite quadrupled this year and CI became the bottleneck"
date: 2026-09-21
lang: en
source: https://clauday.com/article/4dbacd28-685a-488f-9e74-91e5c4b1b435
tags: [Coding, Agents, Infrastructure]
---

# Linear's test suite quadrupled this year and CI became the bottleneck

> 来源 / Source: https://clauday.com/article/4dbacd28-685a-488f-9e74-91e5c4b1b435

Linear published a piece on September 21 about reworking their CI, and the framing is the useful part: AI coding made CI the bottleneck. Not code review, not design, not deployment. The pipe that checks whether the code works.

The volume numbers explain why. Their test suites have almost quadrupled since the start of the year, and they are currently adding roughly 2,000 tests a week. That is what happens when writing a test stops costing human minutes. The tests get written, they are mostly fine, and the bill shows up somewhere else entirely, in wall-clock time that every engineer on the team now waits on many times a day.

The fixes are unglamorous and specific, which is why they are worth reading. PR wait time went from more than six minutes to just over five. Runner time per test roughly halved. TypeScript compilation got 73 percent faster with tsgo. Linting dropped 68 percent for the API and 55 percent repository-wide. Database setup went from 12 seconds to 1 or 2. They went from 4 to 8 test shards while cutting total setup time, and one setup change alone saved about 87,000 runner-minutes a month, which they put at 11.8 percent of total CI usage. Module state caching bought another 17 percent.

Notice that the headline metric moved the least. Six minutes to five is a 17 percent improvement bought with a stack of deep optimizations, against a test suite growing 4x a year. They are running to stay in place, and they say so.

This is the most concrete public account yet of the thing everyone is about to hit. Agents move the constraint downstream. Generation gets cheap, so verification becomes the whole cost, and verification is exactly the part that did not get cheaper. The version of this story I want next is from a team that stopped optimizing CI and started asking which of the 2,000 tests a week are worth running at all, because at some point the answer is not a faster runner, it is a model deciding what to execute. https://linear.app/now/ci-bottleneck-reworked
