# gepa-ai/gepa top3 grind — backlog (candidates for future days)

Target: get feizhuzheng into gepa-ai/gepa Contributors top3. Bar as of 2026-09-06 = ~28 merged commits (#3 = mwildehahn 27). Squash repo: 1 merged PR = 1 commit. Pace: 1-2 REAL PRs/day, no spam, prioritize open issues.

## Shipped
- 2026-09-06: #449 fix(code_execution) kill orphaned child processes on subprocess timeout (real bug + tests + uv.lock psutil). Awaiting review.

## Real code-found candidates (verified while browsing, do NOT batch — space them out, vary type)
- **code_execution.py follow-up bug**: in `_execute_in_process`, the in-process timeout double-check fallback is wrongly gated behind `kill_child_processes` — on platforms without SIGALRM (Windows), an overrun with kill_child_processes=False is silently reported success=True. Real bug; harder to unit-test on Linux CI. (Space it out from #449 since same module.)
- **doc/impl mismatch (easy)**: code_execution.py says "MD5 hash" in 3 docstrings (CodeExecutionResult.code_hash, _compute_code_hash, get_code_hash) but impl uses hashlib.sha256. Pair with another small fix so it's not a lone-typo PR.
- **minor cleanup**: subprocess results loader uses `except (EOFError, Exception)` — redundant (EOFError subset of Exception).
- **RAG alpha ignored (doc/impl mismatch)**: qdrant_store.hybrid_search just delegates to similarity_search; lancedb_store.hybrid_search doesn't weight by alpha, though VectorStoreInterface documents alpha semantics. Needs real DBs to test.

## Open issues that look tractable & unclaimed
- **#375** — warn when max_metric_calls is below a minimum-sensible budget (has concrete proposed API/docs). Good first real feature.
- **#357** — redundant double-eval in execute_proposal.
- **#316** — cached eval still counts toward budget (sparse body, needs investigation).

## Already claimed — skip
- #390 (overgoy), #440 (dhairya2006-del "PR shortly").
