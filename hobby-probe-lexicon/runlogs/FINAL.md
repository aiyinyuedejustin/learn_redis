# FINAL — PROBE LEXICON v2

Completed: 2026-09-18 14:09 Asia/Shanghai (box clock)
Final active leaf count: **2254**

## Agent org map
| Role | id | Group |
|------|----|-------|
| 词表·门禁 | 4079867 | 探圈·审判庭 |
| Judge·反slop | 4079870 | 探圈·审判庭 |
| Judge·探针 | 4079873 | 探圈·审判庭 |
| 核对者 | — | 探圈·审判庭 |
| 缺口猎手 | 4079877 | 探圈·提案组 |
| 描述员 | 4079883 | 探圈·成片组 |
| 校准员 | 4079887 | 探圈·成片组 |

## ACCEPTANCE checkboxes

### A. 结构
- [x] ≥98% active 叶 path合法、is_leaf=1、层级≥2 — **2254/2254 = 100.00%** (`exports/dashboard.md`)
- [x] 无 L1 名称直接当叶子 — **0** (`runlogs/01_bootstrap.md`)
- [x] 导出存在：`exports/taxonomy.json`、`exports/taxonomy.md`、`exports/lexicon.csv`、`exports/dashboard.md`

### B. 反 slop
- [x] 规则扫描报告：`sources/derived/rule_rubric_report.md`
- [x] LLM judge 分层抽样 ≥200 — **280** in `rounds/R010/verdicts/llm_judge.jsonl`；报告 `sources/derived/llm_judge_report.md`；queue `rounds/R010/judge_queue/`
- [x] 抽检 50 条第二意见同意率 ≥75% — **50/50 = 100%** in `sources/derived/calibrate_sample.md`

### C. 探针效用
- [x] 随机 40 叶探针可解析 ≥80% — **40/40 = 100%** in `sources/derived/probe_eval.md`
- [x] 不要求 URL（全流水线未因缺 URL 淘汰）

### D. 描述
- [x] 100% keep 叶有 blurb + ≥3 keywords — **2254/2254**；`exports/lexicon_blurbs.jsonl`；`sources/derived/describe_report.md`
- [x] blurb anti-slop 扫描 residual=0（同 describe_report）

### E. 落盘与发布
- [x] 本地 `exports/` 覆盖完成
- [ ] 推送 `aiyinyuedejustin/learn_redis` → `hobby-probe-lexicon/` 并 merge main（见下方 PR）
- [x] 本文件列出每阶段证据

## Stage evidence
| Stage | Proof |
|-------|-------|
| 01_bootstrap | `runlogs/01_bootstrap.md`, `sources/derived/l1_names.json` |
| 02_rule_rubric | `sources/derived/rule_rubric_report.md`, `scripts/rule_rubric_purge.py` |
| 03_llm_judge | `sources/derived/llm_judge_report.md`, `rounds/R010/verdicts/llm_judge.jsonl` |
| 04_calibrate | `sources/derived/calibrate_sample.md`, `memory/judge_rubric_vNext.md` |
| 05_gap_expand | `sources/derived/gap_expand_report.md`, `sources/derived/diagnose_latest.md`, `sources/immutable/R010_GAP_proposals.jsonl` |
| 06_describe | `sources/derived/describe_report.md`, `exports/lexicon_blurbs.jsonl` |
| 07_export | `exports/*` |
| 08_github | PR URL below after merge |
