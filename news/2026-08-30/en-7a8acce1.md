---
title: "AI Scrapers Are Eating a Fifth of kernel.org"
date: 2026-08-30
lang: en
source: https://clauday.com/article/7a8acce1-2d79-4dc6-baff-92ae70c77e83
tags: [Infrastructure, Agents]
---

# AI Scrapers Are Eating a Fifth of kernel.org

> 来源 / Source: https://clauday.com/article/7a8acce1-2d79-4dc6-baff-92ae70c77e83

Konstantin Ryabitsev, who runs the infrastructure behind git.kernel.org, wrote up what the AI training boom actually costs the people hosting open data, and the numbers are brutal. Of roughly six million requests a day, only about 2% is legitimate human or tool traffic. The rest is scrapers, and they don't clone the repo the cheap way, they render HTML commit pages one at a time. Linux.git has 1.48 million commits and around 922 forks, which multiplies out to billions of valid URLs, and the bots are trying to walk all of them.

The defense is a proof-of-work challenge called Anubis, and it's holding the line but barely. Sixty-six percent of requests fail the challenge and get blocked, a third solve it and get through. Even so, fourteen to sixteen CPU cores, a full fifth of the machine's capacity, are permanently pinned just rendering commits for scrapers that will never read them like a human would. Ryabitsev describes them descending 'like swarms of locust, hit hard and fast until the system fell over and then moved on.'

The reason you can't just block the offenders is that they come through residential and mobile proxy networks, so there's no clean IP range to firewall. This is the same shape as the story we ran about someone spoofing ClaudeBot's user agent to scan the web for AI tool secrets (clauday.com/article/7717dca5-ed20-4944-b31e-88aedc658af4), agents and scrapers hiding inside traffic patterns that make them expensive to tell apart from real users.

What makes this worth reading past the complaint is the economics underneath. Free, high-value, publicly accessible source code is exactly what a training run wants and exactly what a residential-proxy vendor can monetize, so the incentive to keep hammering doesn't go away no matter how high the proof-of-work bar climbs. The quiet cost of the agent era is landing on volunteer-run infrastructure first. Full post at people.kernel.org/monsieuricon/creepy-crawlies.
