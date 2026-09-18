# RUNLOG — PROBE LEXICON v2
Started: 2026-09-18 22:03 Asia/Shanghai
Workspace: /workspace/hobby-probe-v2
GitHub target: aiyinyuedejustin/learn_redis → hobby-probe-lexicon/ then merge main

## Agent org map
- 词表·门禁 4079867 (gatekeeper) — 探圈·审判庭
- Judge·反slop 4079870 + Judge·探针 4079873 + 核对者 — dual/triple judge — 探圈·审判庭
- 缺口猎手 4079877 — 探圈·提案组
- 描述员 4079883 — 探圈·成片组
- 校准员 4079887 — 探圈·成片组

## Stages
- [x] 01_bootstrap — active leaves baseline 2106; `sources/derived/l1_names.json` (25 L1); `runlogs/01_bootstrap.md`
- [x] 02_rule_rubric — `sources/derived/rule_rubric_report.md`; script `scripts/rule_rubric_purge.py`
- [x] 03_llm_judge — sample 280; verdicts `rounds/R010/verdicts/llm_judge.jsonl`; queue for agents; after cleanup leaves ~2094
- [x] 04_calibrate — agree 50/50=100%; `sources/derived/calibrate_sample.md`
- [x] 05_gap_expand — +160 new; light rubric; active **2254**; `sources/derived/gap_expand_report.md`
- [x] 06_describe — 2254/2254 blurbs; `exports/lexicon_blurbs.jsonl`
- [x] 07_export_local — taxonomy.json/md, lexicon.csv, dashboard.md
- [x] 08_github — PR https://github.com/aiyinyuedejustin/learn_redis/pull/2 merged; folder hobby-probe-lexicon/
- [x] FINAL — `runlogs/FINAL.md` all ACCEPTANCE boxes ticked

## Counts trail
2106 (bootstrap) → 2102 (rubric+restore) → 2094 (judge) → 2254 (gap+restore) → **2254** (export)
