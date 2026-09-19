# modelscope/evalscope top3 grind — backlog

Target: feizhuzheng into modelscope/evalscope Contributors top3. Bar 2026-09-19 = pass #3 git-jxj=24 (#4 Moenupa=14 = early milestone). Squash: 1 merged PR = 1 commit. Pace 1-2 REAL PRs/day, no spam, prioritize issues, vary module. WHY this repo: gepa died (maintainer only merged own PRs); evalscope actively merges external real-person PRs daily (Yunnglin/wangxingjun778). WATCH: if evalscope goes >10 days with no external merge, warn user to switch again.

## Shipped (open, pending merge)
- 2026-09-19: #1751 fix(metrics) parse Chinese multi-select answers separated by ideographic-comma / slash. Module evalscope/utils/multi_choices.py + test. Self-found parity bug. Awaiting.

## High-value next picks (verified; vary module)
1. multi_choices.py follow-on: Chinese connector words 和/或 without spaces (答案：A和C) still truncate to first label; English handles "A and B"/"A or B". Extend parse_answers_zh connector handling to parity. (Natural follow-on to #1751 — space it out a day or two.)
2. benchmarks/mvbench/utils.py find_archive_member: name.endswith(video_name) can false-match a suffix substring (1.mp4 matches x1.mp4); compare on basename equality. Related to open issue #1708 (fine_grained_pose subset).
3. Issue #1108: Audio ASR benchmarks (LibriSpeech/TORGO) return 400 in sglang server mode; likely audio payload formatting. Needs repro, concrete.
4. Issue #930 (enhancement): allow selecting prompt template (SINGLE_ANSWER vs SINGLE_ANSWER_COT) via CLI/dataset-args without redefining adapter. Maintainer-friendly small feature.
5. Issue #1606 (7 comments): ifbench metric problem; investigate before committing.

## Contribution types evalscope merges
new/fixed benchmark, dataset mode, model adapter, eval-logic/metric bug fix, doc-vs-code mismatch, test coverage. open issues few (~29) so also self-source bugs. Maintainers: Yunnglin (primary merger), wangxingjun778.
