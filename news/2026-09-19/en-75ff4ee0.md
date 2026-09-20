---
title: "Anthropic Open-Sourced Eleven Job Descriptions"
date: 2026-09-19
lang: en
source: https://clauday.com/article/75ff4ee0-9be8-4c76-aefc-b7a4835161a2
tags: [Skills, Agents, Open Source]
---

# Anthropic Open-Sourced Eleven Job Descriptions

> 来源 / Source: https://clauday.com/article/75ff4ee0-9be8-4c76-aefc-b7a4835161a2

anthropics/knowledge-work-plugins is trending today, 280 stars in a day on 25,100 total. What is in it is eleven plugins that turn Claude into a specialist for a specific job function, built for Claude Cowork and usable in Claude Code. Productivity, Sales, Customer Support, Product Management, Marketing, Legal, Finance, Data, Enterprise Search, Bio-Research, and one for building your own.

The structure is the same every time and it is worth looking at, because it is Anthropic's own answer to a question the ecosystem has been arguing about for months. Each plugin is a manifest, an .mcp.json that declares which tools it connects to, a commands directory of slash commands, and a skills directory of domain knowledge. That is it. No framework, no orchestration layer, no graph. Connections, commands, knowledge.

The connector lists are the tell for who this is aimed at. Sales wires into HubSpot, Close, Clay and ZoomInfo. Legal into Box, Egnyte and Microsoft 365. Finance and Data go straight at Snowflake, Databricks and BigQuery. Product Management reaches Linear, Figma, Amplitude and Intercom. These are not developer tools with an agent bolted on. This is the software that runs a company, and Anthropic has published a map of how to reach all of it from one assistant.

The plugin I would read first is Bio-Research, which wires into PubMed, BioRender, Benchling and ChEMBL. It shipped the same week Anthropic confirmed it is running a wet biology lab in the Bay Area. Those two facts are the same strategy seen from two angles, and the plugin is the cheaper half: they are publishing the tool graph a life sciences researcher works in, and the skills file is their opinion about how that work is actually done.

That is the part that is genuinely new here, and it is not the code. A skills directory is a written claim about what a job consists of, committed to a public repo, versioned, and open to pull requests. Anthropic has now published eleven of those. Whether or not you use Cowork, somebody at a frontier lab wrote down what they think legal review or pipeline review or reconciliation is, and you can go read it and disagree in a diff. Repo at github.com/anthropics/knowledge-work-plugins.
