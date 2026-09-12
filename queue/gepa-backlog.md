# gepa-ai/gepa top3 grind — backlog

Target: feizhuzheng into gepa-ai/gepa Contributors top3. Bar 2026-09-12 = pass #3 (mwildehahn 27) -> ~28 merged commits. Squash: 1 merged PR = 1 commit. Pace 1-2 REAL PRs/day, no spam, prioritize open issues, VARY the module.

## Timeline note
- gepa merge-froze 09-01 -> 09-11 (11 days, maintainer away). Thawed 09-12 (LakshyAAAgrawal merging again). Held B=0 during freeze on purpose (anti-flooding); resumed 09-12. Do NOT panic-switch target on short lulls.

## Shipped (open, pending merge)
- #449 fix(code_execution) kill orphaned child processes on subprocess timeout — CLEAN/mergeable. Module utils/code_execution.py.
- #450 feat(api) warn when max_metric_calls too low, Fixes #375-item1 — blocked (awaiting approval). Module api.py.
- #455 fix(rag) honest hybrid-search capability + warn on silent fallback — Module generic_rag_adapter. Awaiting.

## High-value next picks (verified; vary module)
- lancedb_store.py:207 — hybrid_search does real hybrid (query_type="hybrid") but ignores alpha; thread alpha via LanceDB LinearCombinationReranker (needs lancedb to test).
- evaluation_metrics.py evaluate_retrieval — precision/recall computed on dedup set()s not ranked lists (loses rank/dup semantics of precision@k); defensible correctness cleanup.
- code_execution follow-up: _execute_in_process in-process timeout double-check wrongly gated behind kill_child_processes; on no-SIGALRM (Windows) an overrun with kill_child_processes=False silently reports success=True. (space out from #449)
- doc/impl: code_execution.py says "MD5 hash" in 3 docstrings but uses sha256. Pair with another small fix.
- minor: subprocess results loader except (EOFError, Exception) redundant.

## AVOID (taken or high-conflict)
- #357 (parent re-eval) & #316 (cached-eval budget): real but sit in maintainer's actively-redesigned cache/budget area (#4/#301/#369) = high merge-conflict risk. Avoid until that settles.
- Taken by others' open PRs: #281->#282, #390->#435, #440->#445, #375->#376 (we did #375 item1 as #450; check #376 overlap before more #375 items).

## Notes
- gepa gates first-contributor PRs behind maintainer 'approve & run workflows'. Once engaged (as with #449 now clean), later PRs flow faster. C-priority = respond to LakshyAAAgrawal reviews instantly.
