---
title: "video-use edits video by never letting the agent look at the video"
date: 2026-09-22
lang: en
source: https://clauday.com/article/8def25dc-b250-4fd1-9015-e6a67dd5392b
tags: [Agents, Tool, Open Source]
---

# video-use edits video by never letting the agent look at the video

> 来源 / Source: https://clauday.com/article/8def25dc-b250-4fd1-9015-e6a67dd5392b

browser-use shipped video-use, a tool that lets Claude Code and other coding agents do video post-production. 25.8k stars, MIT, and the design decision at the center of it is a good one.

The agent does not process frames. One ElevenLabs Scribe call per source returns word-level timestamps, speaker diarization and audio events, and the agent edits against that transcript. Visual composites get generated only when the agent actually needs to see something to make a decision. Video is the most token-hostile medium there is, and the trick here is refusing to put it in the context window at all — edit the text, apply the cuts to the media.

What it does with that: strips filler words and dead space between takes, auto color grades segments, adds 30ms audio fades at every cut so you do not get pops, burns in subtitles in two-word uppercase chunks by default, and generates animation overlays through HyperFrames, Remotion, Manim or PIL. It also renders, looks at its own cut boundaries, and evaluates them. Session state lives in a project.md so the next session knows what the last one decided.

The 30ms fade detail is the tell that a human who has actually edited video wrote this. That is not a thing you add from first principles; it is a thing you add after shipping a cut full of clicks. Same with two-word subtitle chunks, which is the convention short-form video converged on for readability.

Install is a setup prompt you paste into Claude Code, which clones, installs dependencies and wires up keys. Needs ffmpeg and an ElevenLabs key, yt-dlp optional.

https://github.com/browser-use/video-use
