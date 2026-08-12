# Backlog — external PR candidates for human review

## 2026-08-13
- **No confident external typo/doc target found this pass.** Swept openai-cookbook, langchain, langgraph, vllm, transformers, ollama, litellm, autogen, crewAI, llama_index, haystack, AutoGPT, pytorch, mcp/servers for common misspellings (recieve/seperate/compatability/occured/paramter/arguement/lenght/sucessful/existant/definately/occurence/retreive) in markdown — all clean. Well-maintained repos have already been swept by others.
- Lead worth a human pass: `crewAIInc/crewAI` returns 98 `the the` matches in .md — mostly sentence-boundary false positives ("...the. The...") but may hide 1-2 real duplicated-word typos. Needs eyeballing, not blind fix.
- Next time: target younger / fast-moving trending AI repos and their `examples/` (runnable snippets that drift out of date) rather than flagship docs; or filter GitHub `good first issue`+`documentation` more broadly instead of per-org.
