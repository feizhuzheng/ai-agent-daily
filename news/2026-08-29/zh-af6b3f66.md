---
title: "Scientific Agent Skills：165个技能，和一次值得琢磨的改名"
date: 2026-08-29
lang: zh
source: https://clauday.com/zh/article/af6b3f66-e376-4257-a402-2624848493c3
tags: ["Skills", "Research", "Open Source"]
---

# Scientific Agent Skills：165个技能，和一次值得琢磨的改名

来源 / Source: https://clauday.com/zh/article/af6b3f66-e376-4257-a402-2624848493c3

K-Dense的scientific-agent-skills今天涨了1600星，是它蹲守GitHub trending两周以来最猛的一天，总量37.9k。仓库里是165个验证过的skills，能把任何coding agent变成一个能干活的科研助理：PubChem、ChEMBL、UniProt等100多个科学数据库，RDKit、Scanpy等70多个Python包，还接了Benchling、DNAnexus这些科研平台。MIT协议，K-Dense号称19万科学家在用。

现在写它不只因为势头，是因为那次改名。这个仓库原来叫Claude Scientific Skills，现在叫Scientific Agent Skills，明确面向所有支持开放Agent Skills标准的agent。一次改名把生态的走向说透了：skills本来是Claude Code的一个功能，现在正悄悄变成一种厂商中立的专业知识打包格式——技能写一次，哪家agent赢了就跑在哪家上。

底下那个赌注值得挑明。模型能力在趋同，不趋同的是被编码成可执行形式的领域知识。一个知道怎么正确查询ChEMBL各种坑的skill，在Claude下有用，在Codex下有用，在明年随便哪个新agent下还是有用。做skill库的人赌的是护城河在模型之上——从具体厂商名改成标准名，就是把这个赌注喊出声了。

仓库：https://github.com/K-Dense-AI/scientific-agent-skills
