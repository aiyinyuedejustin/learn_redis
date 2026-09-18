# PIPELINE（禁止跳步）

```
01_bootstrap     复制/连接 DB，写 L1 名册，RUNLOG 开工
02_rule_rubric   脚本反 slop → 更新 DB status + 报告
03_llm_judge     Judge 批审抽样/分层样本 → verdicts apply
04_calibrate     抽 50 条复核 → calibrate_sample.md（不达阈值则回 03 加严提示词再跑，最多 2 轮）
05_gap_expand    按缺口提案（URL 可选）→ import → 再跑 02 轻量去重
06_describe      全量 keep 刷 blurb+keywords → anti_slop 扫描描述
07_export_local  覆盖 exports/
08_github        新目录推送 learn_redis 并 merge main
FINAL            runlogs/FINAL.md 勾选 ACCEPTANCE 全项
```

未完成 ACCEPTANCE 任一项 → 不得进入 08 宣称成功；08 仅在 A–D+导出证明齐全后执行。
