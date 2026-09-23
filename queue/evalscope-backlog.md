# modelscope/evalscope top3 grind — backlog

Target: feizhuzheng into modelscope/evalscope Contributors top3. Bar 2026-09-23 = pass #3 git-jxj=26 (#4 Moenupa=14, #5/#6=13 = near milestones). feizhuzheng=2 merged (#1751,#1755); #1752 ready-to-merge, #1761 + #1769 open. Squash: 1 merged PR=1 commit. Pace 1-2 REAL PRs/day, VARY module, clear impact only. WHY: gepa died; evalscope merges external daily. WATCH: >10 days no external merge -> warn user.

## LESSON (#1752): Yunnglin rejects synthetic/defensive; demands reproduction on OFFICIAL/default data + he INDEPENDENTLY verifies. Every PR: issue-linked OR provably reproducible on official data, + regression test. Be honest.

## Shipped
- #1751 MERGED 09-20: fix(metrics) Chinese multi-select parse. utils/multi_choices.py.
- #1755 MERGED 09-21: fix(ifbench) word-boundary keyword/person-name counting.
- #1752 READY-TO-MERGE: fix(mvbench) archive-member exact match (downscoped, real 9741/209741 regression).
- #1761 OPEN 09-22: fix(ifbench) StopWordPercentageChecker ZeroDivisionError guard.
- #1769 OPEN 09-23: fix(hallusion_bench) fAcc/qAcc grouping vs official (category key + skip VS figure_id==0). NON-ifbench.

## Next picks (clear-impact, verified; KEEP diversifying modules)
- **BBH dyck_languages target corruption (STRONG next)**: bbh/bbh_adapter.py:124 `target.replace('(','').replace(')','').strip()` runs UNCONDITIONALLY, corrupting free-form dyck_languages gold (e.g. "] ) )" -> "]"), systematically scoring correct answers 0 on a default subset. Fix = only strip parens for multiple-choice subsets. Verify shipped lukaemon/bbh target format first. Different module (bbh).
- multi_choices.py 和/或 connector parity (答案：A和C) — verify it bites official data first.
- audio ASR #1108 (LibriSpeech/TORGO sglang 400) — needs repro, deeper.
- mvbench frame-sampling #1708 (Qwen3VL 1-frame) — deep, hard to unit-test.

## AVOID
- #930 (Yunnglin claimed it). #1040 (later). #1100/BFCL-v4 memory (deep integration, not unit-testable). Synthetic/defensive-only. 3+ consecutive same-module.

## Notes
Maintainers: Yunnglin (primary merger, independently verifies vs real data), wangxingjun778. Conventional fix(<module>):. tests/ ruff-format-excluded. eval-score-changing => evaluation_version bump (precedent #1676); pure crash->upstream-return => no bump (#1756).
