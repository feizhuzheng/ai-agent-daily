# modelscope/evalscope top3 grind — backlog

Target: feizhuzheng into modelscope/evalscope Contributors top3. Bar 2026-09-22 = pass #3 git-jxj=26 (#4 Moenupa=14, #5 haoruilee=13 = early milestones). feizhuzheng=2 merged (#1751, #1755), #1752 ready-to-merge. Squash: 1 merged PR = 1 commit. Pace 1-2 REAL PRs/day, VARY module, clear impact only. WHY: gepa died; evalscope merges external daily (Yunnglin). WATCH: >10 days no external merge -> warn user.

## LESSON (#1752): Yunnglin rejects synthetic/defensive; demands reproduction on OFFICIAL/default data. Every PR issue-linked OR clearly reproducible on official data + regression test. He INDEPENDENTLY verifies. Be honest (concede wrong parts, prove real parts).

## Shipped
- #1751 MERGED 09-20: fix(metrics) Chinese multi-select parse. utils/multi_choices.py.
- #1755 MERGED 09-21: fix(ifbench) word-boundary keyword/person-name counting. benchmarks/ifbench/.
- #1752 READY-TO-MERGE (per Yunnglin): fix(mvbench) archive-member exact match, downscoped to MVBench-only w/ real 9741/209741 regression. benchmarks/mvbench/utils.py.
- #1761 OPEN 09-22: fix(ifbench) guard StopWordPercentageChecker ZeroDivisionError on word-less responses. benchmarks/ifbench/instructions.py.

## Next picks — MUST diversify away from ifbench (3 consecutive ifbench PRs #1755/#1761 + queued); prefer other modules
- **Scan for non-ifbench clear-impact bugs**: sweep open issues (bug label) + other benchmarks' eval/metric logic (mvbench frame-sampling #1708, audio ASR #1108 sglang 400, general_mcq, vlm adapters) for official-data-reproducible bugs. ifbench division-by-zero now all guarded (NGramOverlapChecker already had `if not ngrams`); no more same-class there.
- multi_choices.py 和/或 connector parity (答案：A和C truncates) — but frame with real impact per #1752 lesson; verify it bites on an official dataset before proposing.
- ifbench PronounCountChecker smaller-than-upstream pronoun set (undercounts) — judgment call, verify vs upstream; LOWER priority (ifbench fatigue).

## AVOID
- #930 (Yunnglin claimed it himself). #1040 (not-yet-supported, later). Synthetic/defensive-only. Consecutive same-module spam.

## Notes
Maintainers: Yunnglin (primary merger, independently verifies against real data), wangxingjun778. Conventional-commit fix(<module>):. tests/ ruff-format-excluded. eval-score-changing behavior needs evaluation_version bump (precedent #1676); pure crash->upstream-defined-return needs no bump (precedent #1756).
