# modelscope/evalscope top3 grind — backlog

Target: feizhuzheng into modelscope/evalscope Contributors top3. Bar 2026-09-21 = pass #3 git-jxj=26 (#4 Moenupa=14 = early milestone). feizhuzheng=1 (#1751 merged). Squash: 1 merged PR = 1 commit. Pace 1-2 REAL PRs/day, no spam, VARY module. WHY: gepa died (only own PRs); evalscope merges external daily (Yunnglin merged #1751 in a day). WATCH: >10 days no external merge -> warn user.

## LESSON from #1752 (important)
Yunnglin rejects synthetic/defensive/theoretical fixes — demands the bug reproduces on OFFICIAL data or a supported real path. So every PR must be issue-linked OR clearly reproducible on official/default data. Prefer real logic bugs + regression tests + (for eval-affecting changes) an evaluation_version bump (precedent #1676).

## Shipped
- #1751 MERGED 09-20: fix(metrics) Chinese multi-select parse. Module utils/multi_choices.py. = feizhuzheng's 1st commit.
- #1752 OPEN (downscoping): archive-member match. Video-MME-v2 half conceded (synthetic); MVBench half is a REAL collision (action_antonym/ssv2_video.zip: 9741.webm vs 209741.webm). Awaiting Yunnglin's call on downscope-to-MVBench-only.
- #1755 OPEN 09-21: fix(ifbench) word-boundary keyword/person-name counting (art-in-start, Mia-in-Miami). Module benchmarks/ifbench/. + version bump + tests. Awaiting.

## High-value next picks (verified, clear-impact; vary module; space out same-module)
- ifbench StopWordPercentageChecker (ratio:stop_words): evalscope dropped upstream's `if num_words==0: return False` guard -> ZeroDivisionError on empty/whitespace model response (crashes metric; matches #1606's described 静默跳过). Clean one-line fix, clear impact. STRONG next pick (maybe links #1606).
- ifbench PronounCountChecker (count:pronouns): evalscope uses a smaller pronoun set than official IFBench (dropped demonstrative/interrogative/indefinite) -> undercounts vs official. Verify vs upstream first; judgment call.
- multi_choices.py follow-on (space out from #1751): Chinese connectors 和/或 without spaces (答案：A和C) truncate to first label; English handles "A and B". Extend parse_answers_zh to parity — but frame with real impact per the #1752 lesson.

## AVOID
- Issue #930 (prompt-template selection): Yunnglin claimed it himself ("I'll work on a PR"). Don't compete.
- Issue #1040 (text2image local /v1/images/generations): Yunnglin said not-yet-supported/later. Skip.
- Synthetic/defensive-only changes (see #1752 lesson).

## Notes
Maintainers: Yunnglin (primary merger, thorough reviewer — verifies against real data), wangxingjun778. Conventional-commit titles fix(<module>): . tests/ ruff-format-excluded. eval-behavior changes need evaluation_version bump (precedent #1676).
