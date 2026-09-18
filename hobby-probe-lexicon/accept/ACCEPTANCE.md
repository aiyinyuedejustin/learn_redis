# ACCEPTANCE — 探圈词表 v2（事前契约，未勾完禁止宣称完成）

## 目标（一句）
产出一张 **L1→L2→L3(→L4) 探圈词表**：叶子是具体爱好/圈子名，可拿去问别的 AI「这圈子干什么」；每条最终带一句人话介绍 + leading keywords。**不是**网页标本库，也不是刷数量竞赛。

## AI slop（本任务定义）
不只是英文腔。包括：
- 套话/翻译腔/排比/“不仅…更是…”/空洞升华
- **假搜索技术名词**：听起来很专业、像 SEO/论文关键词、但真人圈子不这么自称的标签
- 换皮同义、空壳大类、平台名冒充爱好、为凑数切的微片

反参考：Wikipedia “Signs of AI writing”；blader/humanizer、kill-slop、antislop 等 skill 的检测思路（见 `anti_slop/PREFERENCES.md`）。

## Done-when（全部满足才算完成；禁止提前收束）

### A. 结构（脚本，硬）
- [ ] ≥98% active 叶：`path` 合法、`is_leaf=1`、层级≥2
- [ ] 无 L1 名称直接当叶子
- [ ] 导出存在：`exports/taxonomy.json`、`exports/taxonomy.md`、`exports/lexicon.csv`、`exports/dashboard.md`

### B. 反 slop（脚本 + judge，硬/半硬）
- [ ] 规则扫描报告：`sources/derived/rule_rubric_report.md`；平台名/空壳/明显模板名已 reject 或 merge
- [ ] LLM judge 至少覆盖 **min(500, 全部 active)** 条，或分层抽样 ≥200 条含过热 L1
- [ ] 抽检 50 条「换皮/假技术词」：第二意见同意率 ≥75%（记入 `sources/derived/calibrate_sample.md`）

### C. 探针效用（半硬）
- [ ] 随机 40 叶：用固定探针提示问「这圈子主要干什么/聊什么」；可解析回答 ≥80%（`sources/derived/probe_eval.md`）
- [ ] **不要求 URL**；有 URL/具名社群只作弱加分记录

### D. 描述（后置，不进 A–C 分数）
- [ ] 100% keep 叶有 `blurb`（≤40字中文或等价）+ ≥3 `keywords`
- [ ] blurb 经 anti-slop 规则扫描：无禁用词表命中超标（报告附）

### E. 落盘与发布
- [ ] 本地 `exports/` 覆盖完成
- [ ] 推送到 `aiyinyuedejustin/learn_redis` 的 **新目录**（非覆盖旧 hobby-taxonomy 也可并存）并 **merge 进 main**
- [ ] `runlogs/FINAL.md` 列出每阶段证据路径与勾选证明

## 明确非目标
- 穷尽人类一切爱好
- 无 URL 就淘汰
- 用叶子数量当主 KPI
- 未完成 Done-when 就宣称成功 / 提前结束

## 主控纪律（给主agent）
不允许：偷懒短提示、跳过阶段、用「差不多」勾选、无证据勾选、提前收束。
失败条件：任一 Done-when 无对应文件证明。
