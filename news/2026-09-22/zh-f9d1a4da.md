---
title: "video-use 剪视频的办法，是让 agent 根本不去看视频"
date: 2026-09-22
lang: zh
source: https://clauday.com/zh/article/f9d1a4da-24cd-4b60-a53f-4f4e56f54665
tags: [Agents, Tool, Open Source]
---

# video-use 剪视频的办法，是让 agent 根本不去看视频

> 来源 / Source: https://clauday.com/zh/article/f9d1a4da-24cd-4b60-a53f-4f4e56f54665

browser-use 发了 video-use，让 Claude Code 之类的编码 agent 做视频后期。2.58 万星，MIT，最核心的那个设计决策很漂亮。

agent 不处理画面帧。每个素材调一次 ElevenLabs Scribe，拿回词级时间戳、说话人分离和音频事件，agent 对着这份转写稿剪。只有真需要看一眼才能做判断时，才生成视觉合成图。视频是所有媒介里对 token 最不友好的一种，这里的窍门是干脆不让它进上下文窗口——改文本，再把剪切点落到媒体上。

具体干的活：删口头禅和镜头之间的静默，分段自动调色，每个剪切点加 30 毫秒音频淡入淡出免得爆音，默认按两词一组全大写烧字幕，通过 HyperFrames、Remotion、Manim 或 PIL 生成动画叠层。它还会渲染出来，自己盯着剪切点做评估。会话状态存在 project.md 里，下一次开工知道上一次定了什么。

30 毫秒淡入淡出这个细节，是真剪过片子的人才写得出来的。这不是从第一性原理推出来的东西，是交付过一版满是咔哒声的成片之后加上去的。两词一组的字幕也一样，那是短视频行业为了可读性收敛出来的惯例。

安装方式是把一段 setup 提示词贴进 Claude Code，它负责克隆、装依赖、配密钥。需要 ffmpeg 和一个 ElevenLabs key，yt-dlp 可选。

https://github.com/browser-use/video-use
