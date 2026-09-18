# 文件可见性矩阵（谁准读什么）

符号：R=只读 W=可写 —=禁止

| 路径 | 主控 | 提案* | 核对/Judge | 描述员 |
|------|------|-------|------------|--------|
| accept/ACCEPTANCE.md | R | R | R | R |
| anti_slop/PREFERENCES.md | R | R | R | R |
| orchestration/* | RW | R(本角色卡) | R(本角色卡) | R |
| sources/derived/diagnose*.md | R | R | R | — |
| sources/derived/*_report.md | RW | — | R | R |
| data/taxonomy.db | RW(编排脚本) | — | — | — |
| rounds/R010/private/<role>/ | RW | RW 仅自己 | — | — |
| rounds/R010/inbox/pool.jsonl | RW | StageB+ 只读 | R | — |
| rounds/R010/verdicts/ | RW | — | RW | — |
| exports/ | RW | — | — | R |
| 其他角色 private/ | — | — | — | — |
| sources/immutable/ | W仅归档脚本 | — | — | — |

## 阶段可见性
- **Stage 02 前提案隔离**：提案者不得读其他 `private/`，不得读 full taxonomy 叶列表（可读 L1 名册）
- **Stage 05**：可读 diagnose + 缺口清单 + 允许的 pool 摘要
- **Judge**：可读待审批次与 anti_slop；不可写提案
- **描述员**：只读 keep 清单；不改 status
