# modelscope/evalscope top3 grind — backlog

Target: feizhuzheng into modelscope/evalscope Contributors top3. Bar 2026-09-20 = pass #3 git-jxj=24 (#4 Moenupa=14 = early milestone). Squash: 1 merged PR = 1 commit. Pace 1-2 REAL PRs/day, no spam, prioritize issues, VARY module. WHY: gepa died (only merged own PRs); evalscope merges external real-person PRs daily. WATCH: if evalscope goes >10 days no external merge, warn user to switch.

## Shipped (open, pending merge)
- 2026-09-19: #1751 fix(metrics) Chinese multi-select answer parse (、 / /). Module utils/multi_choices.py + test. Awaiting.
- 2026-09-20: #1752 fix(benchmarks) archive-member exact match in mvbench + videomme_v2 (endswith false-match 2.mp4 vs 12.mp4). Modules benchmarks/mvbench/utils.py + videomme_v2/utils.py + new test. Awaiting.

## High-value next picks (verified; vary module; space out same-module)
- multi_choices.py follow-on (space out from #1751): Chinese connectors 和/或 without spaces (答案：A和C) still truncate to first label; English handles "A and B"/"A or B". Extend parse_answers_zh to parity.
- Issue #930 (enhancement, maintainer-friendly): allow selecting prompt template (SINGLE_ANSWER vs SINGLE_ANSWER_COT) via CLI/dataset-args without redefining adapter. Good small feature PR.
- Issue #1708 (open bug, HARDER): MVBench + Qwen3VL only extracts 1 video frame (frames_indices=[0] for an 82-frame clip) then VL processor 400s. Real frame-sampling/fps bug, needs deeper investigation into video frame extraction. NOT the archive-lookup bug (that was #1752).
- Issue #1108: Audio ASR (LibriSpeech/TORGO) 400 in sglang server mode; audio payload formatting; needs repro.
- Issue #1606 (7 comments): ifbench metric problem; investigate first.

## Notes
Maintainers: Yunnglin (primary merger), wangxingjun778. Conventional-commit titles fix(<module>): . tests/ is ruff-format-excluded. Contribution types: benchmark/dataset-mode/adapter/eval-bug/doc/test.
