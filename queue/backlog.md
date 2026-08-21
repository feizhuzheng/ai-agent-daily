# Backlog — external PR candidates for human review

## 2026-08-13
- **No confident external typo/doc target found this pass.** Swept openai-cookbook, langchain, langgraph, vllm, transformers, ollama, litellm, autogen, crewAI, llama_index, haystack, AutoGPT, pytorch, mcp/servers for common misspellings (recieve/seperate/compatability/occured/paramter/arguement/lenght/sucessful/existant/definately/occurence/retreive) in markdown — all clean. Well-maintained repos have already been swept by others.
- Lead worth a human pass: `crewAIInc/crewAI` returns 98 `the the` matches in .md — mostly sentence-boundary false positives ("...the. The...") but may hide 1-2 real duplicated-word typos. Needs eyeballing, not blind fix.
- Next time: target younger / fast-moving trending AI repos and their `examples/` (runnable snippets that drift out of date) rather than flagship docs; or filter GitHub `good first issue`+`documentation` more broadly instead of per-org.
## 2026-08-16 — fetchai/uAgents (~1.6k stars) — PRed as #934, resolved
- Was verified KeyError in LangChain adapter README; shipped as fetchai/uAgents#934 on 2026-08-16. No longer a backlog item.

## 2026-08-16 — dynamiq-ai/dynamiq (~1.1k stars, verified, candidate for future)
- README.md async ReAct example ends with asyncio.run(...) (L142) but never imports asyncio (only imports at L101-104) -> NameError on copy-paste.
- Fix: add one line  to that snippet import block.
- Was opened as dynamiq#898 then closed same day to keep to a 1-PR/day cap (uAgents#934 took the slot). Branch feizhuzheng:docs/readme-add-missing-import-asyncio still has the change; can reopen/resubmit on a future day.

## 2026-08-21 · DeepSeek 官方 org 方向（已独立核实仓库真实、活跃、开 issues）
高价值目标，B 段优先考虑（拿"DeepSeek 官方/生态 merged PR"身份）：
- **deepseek-ai/awesome-deepseek-integration** ⭐38.8k（官方 deepseek-ai org，开 issues）——README 收录/格式/失效链接/typo 类，合一个=官方组织内 merged PR。**注意**：awesome 列表 PR 常要求按 CONTRIBUTING 的条目格式提交，先读它的规范。
- **anywhere-labs/deepseek-harness-desktop** ⭐16.5k（TS 桌面 harness，开 issues）——输出截断/filesize 格式化/显示宽度类 bug，跟 crush#16451、cline#11999 的 UTF-8/emoji 截断同型，命中率高。
- **awesome-dsh-plugin/awesome-dsh-plugin** ⭐10.6k（收录列表，开 issues）——docs/i18n 不一致。
- 主仓 deepseek-ai/deepseek-harness ⭐17万 **issues 关闭、不收外部 PR**，别在主仓浪费子弹；长线可在 Discussions 发高信号 bug 报告卡位。
（来源：一次生态调研，已用 GitHub API 逐个核实 star/issues/archived 属实。找到真问题再提，仍守质量门槛。）

## 2026-08-21 · sweep notes (B done: awesome-dsh-plugin#2495 shipped)
- **anywhere-labs/deepseek-harness-desktop** ⭐16.6k — swept src (truncation/byte-budget/format): exceptionally defensive (byteLength everywhere, Array.from for code-point-safe slicing, correct diagnostic byte-budget accumulation). No bug found this pass; 60 md files, 0 broken relative links. Low hit-rate for our usual truncation angle — deprioritize.
- **deepseek-ai/awesome-deepseek-integration** ⭐38.9k (official org, last push 2026-02-23) — README docs refs all resolve (53/53), no common typos. Clean; would need a dead external-link pass (network HEAD) to find anything, and it's heavily swept. 
- **awesome-dsh-plugin/awesome-dsh-plugin** ⭐10.7k — data-driven generated list; found+fixed a real data-integrity bug (plugin file missing .yml extension -> silently dropped) = PR #2495. Future angle here: run `node scripts/generate-readme.mjs --check` for staleness, and scan data/plugins/*.yml for unquoted ': ' in description.en (contributing.md's known parser trap).
