# gepa-ai/gepa top3 grind — backlog (candidates for future days)

Target: get feizhuzheng into gepa-ai/gepa Contributors top3. Bar as of 2026-09-07 = pass #3 (mwildehahn 27) -> ~28 merged commits. Squash repo: 1 merged PR = 1 commit. Pace: 1-2 REAL PRs/day, no spam, prioritize open issues, VARY the module (don't hammer one file).

## Shipped (open, pending merge)
- 2026-09-06: #449 fix(code_execution) — kill orphaned child processes on subprocess timeout (real bug + tests + uv.lock psutil). Module: utils/code_execution.py. Awaiting first-contributor workflow approval.
- 2026-09-07: #450 feat(api) — warn when max_metric_calls too low (Fixes #375 item 1). Module: api.py + tests/test_budget_warning.py. Awaiting approval.

## High-value next picks (verified, space out & vary module)
- **#375 remaining items (same issue, 2-3 more independent PRs)**: (item2) add a `min_proposals` param to control the floor; (item3) promote num_proposals_attempted/accepted/num_validations to first-class GEPAResult fields + print a one-line run summary; (docs) new "Choosing max_metric_calls" budget guide under docs/docs/guides/.
- **#357**: reflective_mutation.py execute_proposal does two adapter eval calls; when parent already evaluated it's a redundant re-eval wasting runtime/budget — check whether the cache path can be reused. Module: proposer/reflective_mutation/.
- **#316**: cached eval still counts toward metric budget (sparse body, 2 comments, maintainer cc'd; needs investigation of cache vs budget-counting interaction).
- **code_execution follow-up (space out from #449)**: `_execute_in_process` in-process timeout double-check wrongly gated behind kill_child_processes — on no-SIGALRM platforms (Windows) an overrun with kill_child_processes=False is silently success=True. Harder to unit-test on Linux CI.
- **doc/impl mismatch (easy)**: code_execution.py says "MD5 hash" in 3 docstrings but impl uses hashlib.sha256. Pair with another small fix.
- **RAG alpha ignored (doc/impl mismatch)**: qdrant_store.hybrid_search delegates to similarity_search; lancedb_store.hybrid_search doesn't weight by alpha though VectorStoreInterface documents alpha semantics. Needs real DBs to test.
- **minor cleanup**: subprocess results loader `except (EOFError, Exception)` redundant.

## Already claimed — skip
- #390 (overgoy), #440 (dhairya2006-del "PR shortly").

## Notes
- gepa gates first-contributor PRs behind maintainer 'approve & run workflows' — CI (ruff/pyright/pytest across 3.10-3.14) won't run until LakshyAAAgrawal approves. Once he engages on the first PR, later PRs should flow faster. C-step priority = respond to his reviews instantly.
