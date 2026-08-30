---
title: "Cohere Parse 5：跑分认输，按页计价取胜"
date: 2026-08-29
lang: zh
source: https://clauday.com/zh/article/7ffad5d3-12bd-4776-95de-73509da29454
tags: ["Tool", "API", "Infrastructure"]
---

# Cohere Parse 5：跑分认输，按页计价取胜

来源 / Source: https://clauday.com/zh/article/7ffad5d3-12bd-4776-95de-73509da29454

Cohere这周发了Parse 5：一个2.3B参数的视觉语言模型，只干一件事——把PDF、幻灯片、图片变成结构化Markdown。表格还原成HTML，表单变键值对，图片带描述和坐标框，全部按阅读顺序输出。定价一刀切，每1000页1.5美元，每秒处理4.5页，API和Microsoft Foundry都能用。

VentureBeat给的定性在发布季里算少见的诚实：Parse 5跑分输了，按页成本赢了。Cohere没说自己是最准的解析器，说的是企业规模下最合理的成本能力配比——2.3B小到跑起来便宜，好到在每千页1.5美元的价位上那点误差无所谓。看了一年所有实验室在所有榜上宣称SOTA，一个用"够用、便宜得多"来定位的发布，居然让人觉得清爽。

对agent的意义：文档解析是每个企业agent的嘴。agent栽跟头很少栽在推理上，多数栽在上游某处一张表格被搅成了乱码汤。解析层已经悄悄变成兵家必争的基础设施——而把它按大宗商品定价、而不是按AI产品定价，大概率就是拿下这一层的打法。

详情：https://cohere.com/blog/parse
