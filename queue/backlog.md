# Backlog — external PR candidates for human review

## 2026-08-13
- **No confident external typo/doc target found this pass.** Swept openai-cookbook, langchain, langgraph, vllm, transformers, ollama, litellm, autogen, crewAI, llama_index, haystack, AutoGPT, pytorch, mcp/servers for common misspellings (recieve/seperate/compatability/occured/paramter/arguement/lenght/sucessful/existant/definately/occurence/retreive) in markdown — all clean. Well-maintained repos have already been swept by others.
- Lead worth a human pass: `crewAIInc/crewAI` returns 98 `the the` matches in .md — mostly sentence-boundary false positives ("...the. The...") but may hide 1-2 real duplicated-word typos. Needs eyeballing, not blind fix.
- Next time: target younger / fast-moving trending AI repos and their `examples/` (runnable snippets that drift out of date) rather than flagship docs; or filter GitHub `good first issue`+`documentation` more broadly instead of per-org.
## 2026-08-16 — fetchai/uAgents (~1.6k stars, verified, NOT yet PRed)
- Doc-vs-code mismatch in runnable README example.
- python/uagents-adapter/README.md:64 (LangChain adapter) prints result["agent_name"]/["agent_address"]/["agent_port"], but LangchainRegisterTool._run (langchain/tools.py:136-140,154) returns dict keyed name/address/port — never agent_* — so line raises KeyError.
- Control case: neighboring CrewAI tool _run (crewai/tools.py:635-642) DOES build agent_name/agent_address/agent_port, and identical print at README.md:117 works there. LangChain line was copy-pasted without adapting to different return contract.
- Fix: README.md:64 -> result["name"]/["address"]/["port"].
- Held today only because 2026-08-16 already shipped dynamiq#898 (1-PR cap). Good candidate for a future day.

