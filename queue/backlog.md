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
