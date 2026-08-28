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

## 2026-08-22 · mem0ai/mem0 — pr-gate `isDocs` too narrow (real 2nd bug, future target)
- `.github/workflows/pr-gate.yml` L56: `isDocs = (filename) => filename.startsWith('docs/') || rootDocs.has(filename)`. Only `docs/**` + root README/CONTRIBUTING/CODE_OF_CONDUCT/SECURITY count as docs. Markdown docs living under `skills/**`, `examples/**`, `cookbooks/**` (e.g. our #7061 edit to `skills/mem0/references/integration-patterns.md`) are NOT recognized, so genuine documentation-only PRs get auto-closed even though policy states "Documentation-only changes skip this gate entirely."
- Fix idea: broaden `isDocs` to also treat `*.md`/`*.mdx` files (or add `skills/`, `examples/`, `cookbooks/` prefixes) as docs. BUT this edits a workflow (non-docs) so it would itself be gated -> needs an `accepted` issue first. Don't blind-PR; note for when we're a vouched/accepted contributor.
- #7061 (relative-link fix) currently auto-closed by this same gap; commented asking for reopen.

## 2026-08-25 · livekit/agents top-level README — ~8 dead example links (verified, NOT PR'd)
Verified against livekit/agents default branch: the README "Examples" section links to files deleted by the July examples-revamp (PR #5523 "remove redundant files", merged 2026-07-13). None exist anywhere in the repo now:
- L149 `examples/voice_agents/multi_agent.py` (revamp reason: "favor examples and restaurant agent")
- L257 `examples/voice_agents/push_to_talk.py`
- L267 `examples/voice_agents/background_audio.py` (revamp: now docs-only)
- L274 `examples/voice_agents/dynamic_tool_creation.py`
- L291 `examples/voice_agents/structured_output.py`
- L335 `examples/voice_agents/restaurant_agent.py`
- L308 `examples/other/text_only.py`
- L325 `examples/avatar_agents/` (revamp: documented on plugin pages)
Why not PR'd this round: no verifiable 1:1 replacement — the examples were consolidated into docs / removed, and are NOT in the external `livekit-examples/python-agents-examples` repo (code-searched: 0 hits for push_to_talk/structured_output/dynamic_tool_creation/multi_agent/restaurant). Repointing each link (to docs URL vs external repo vs section removal) is maintainer-judgment, so a mass-rewrite would be guesswork = spam risk. Better handled as a GitHub issue, or a PR only after confirming intended targets with maintainers. High visibility (main README, ~13k-star repo) so worth doing once targets are known. Repo has NO PR title-lint/changeset gate; CLA bot on first PR (feizhuzheng already opened #6972 there this run).

## 2026-08-26 · pipecat sweep (B done: pipecat-ai/pipecat#5439 shipped)
- **B shipped**: pipecat-ai/pipecat#5439 — examples/README.md linked `./thinking-and-mcp/` (dead dir); examples were split into `examples/thinking/` + `examples/mcp/` (both exist). Split the stale section into two resolving entries. Docs-only → no changelog fragment (CONTRIBUTING exempts docs); no PR-title lint. New repo (not in prior skip list), new type (stale doc link to split/renamed example dir).
- **Secondary pipecat finding, NOT PR'd (same run, keep 1-PR/day)**: `examples/flows/assets/hold_music/README.md` links `[warm transfer example](../warm_transfer.py)` → from `assets/hold_music/` that resolves to `examples/flows/assets/warm_transfer.py` (missing); real file is `examples/flows/warm_transfer.py`, i.e. link should be `../../warm_transfer.py`. Trivial one-char-family fix but it's the SAME broken-relative-link type as mem0#7061, so deferred to avoid repeating a type. Good easy future pickup.
- **camel-ai/camel**: docs/mintlify/reference/index.mdx etc. use Mintlify absolute paths (`/reference/...`, `/images/...`) — filesystem-broken but Mintlify-served, FALSE POSITIVES, do not "fix". Typos clean. browser-use clean. Deprioritize link-audits on Mintlify-based docs.

## 2026-08-28 · VoltAgent sweep (B done: VoltAgent/voltagent#1408 shipped)
- **B shipped**: VoltAgent/voltagent#1408 — new repo (10.4k stars, active) + reused dead-link type but a different sub-case (removed example, not renamed): examples/README.md listed `[SDK Trace Example](./sdk-trace-example)` but that dir was deleted in 5aa84b5b (feat: add evals #674), 404s on GitHub, no replacement example → removed the stale line. Gates: commitlint (config-conventional) = used `docs(examples):`; Biome doesn't lint md; no changeset gate for non-package examples doc. First-time-contributor CI awaits maintainer workflow-approval (normal).
- **Secondary VoltAgent, NOT PR'd (kept 1-PR/day)**: same dead `sdk-trace-example` ref also in `website/blog/2025-10-21-ai-agent-examples/index.md:265` (full GitHub tree URL, 404). Left alone — dated blog post, point-in-time content; noted in PR body. Future micro-fix if maintainers want it.
- **fast-agent (evalstate/fast-agent, 3.9k stars) codespell**: only weak hits, all FALSE POSITIVES — config.py `SHTTP` (intentional Streamable-HTTP abbrev), oauth_client.py `asend` (real async-gen method), plugins.py `unparseable` (valid word). Docs are Docusaurus (trailing-slash route links) → link-audit = false positives, deprioritize. No clean target found.
- **VoltAgent guardrails/defaults.ts `cunt`** = intentional profanity blocklist, NOT a typo. Do not "fix".
