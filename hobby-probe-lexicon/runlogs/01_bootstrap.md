# 01_bootstrap baseline

- time: 2026-09-18 14:04:01 Asia/Shanghai (box UTC shown via date)
- db: `data/taxonomy.db` (copied from prior project)
- active leaves: **2106**
- active nodes: **3055**
- all nodes: **3954**
- status dist: `{'active': 3055, 'merged': 117, 'rejected': 782}`
- active leaf by level: `[<sqlite3.Row object at 0x7f5a1a8d3a60>, <sqlite3.Row object at 0x7f5a1a8d3af0>]`
- L1-as-leaf (should be 0): **0**
- active leaves with path containing `/`: **2106** / 2106 (100.00%)
- L1 list: `sources/derived/l1_names.json` (25 L1s)
- scripts: copied/adapted under `scripts/` from `scripts_seed/`

## Agent org map (v2)

| Role | Agent id | Group |
|------|----------|-------|
| 词表·门禁 (gatekeeper) | 4079867 | 探圈·审判庭 |
| Judge·反slop | 4079870 | 探圈·审判庭 |
| Judge·探针 | 4079873 | 探圈·审判庭 |
| 核对者 (existing) | — | 探圈·审判庭 |
| 缺口猎手 | 4079877 | 探圈·提案组 |
| 描述员 | 4079883 | 探圈·成片组 |
| 校准员 | 4079887 | 探圈·成片组 |

Judge queues land in `rounds/R010/judge_queue/`; verdicts in `rounds/R010/verdicts/`.
