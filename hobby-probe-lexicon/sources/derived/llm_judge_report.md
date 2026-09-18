# llm_judge_report

- time: 2026-09-18T14:06:06
- stratified sample: **280** (≥200), hot L1 overweight
- sample verdicts: `{'keep': 277, 'drop': 2, 'demote': 1}`
- targeted full-set actions applied: `{'demote': 3, 'drop': 5}`
- active leaves after: **2094**
- queue: `rounds/R010/judge_queue/batch_*.jsonl` (for 4079870/4079873/核对者)
- verdicts: `rounds/R010/verdicts/llm_judge.jsonl`
- criteria: human hobby feel; mount OK; not paraphrase; probe-useful; URL optional
- dual/triple: Judge·反slop + Judge·探针 + 核对者 (executor sim + targeted misparent/dup pass)

## Sample non-keep
- [drop] `语言与人文/哲学文学阅读/补洞阅读/哲学咖啡馆业余主持` — scaffold_in_name_or_path
- [drop] `户外运动/水上与潜水/补洞水/皮艇翻滚EskimoRoll` — scaffold_in_name_or_path
- [demote] `竞技游戏/格斗与对抗竞技/再平衡/马里Kora科拉琴演奏` — misparented_under_fighting_rebalance

## All targeted actions
- [demote] `竞技游戏/格斗与对抗竞技/再平衡/马里Kora科拉琴演奏` — misparented_under_fighting_rebalance
- [demote] `竞技游戏/格斗与对抗竞技/再平衡/伊朗Tar与Setar练习` — misparented_under_fighting_rebalance
- [demote] `竞技游戏/格斗与对抗竞技/再平衡/阿拉伯语书法业余练习` — misparented_under_fighting_rebalance
- [drop] `社群志愿/开源与知识共享/知识库补洞/公共领域乐谱扫描` — scaffold_in_name_or_path
- [drop] `语言与人文/哲学文学阅读/补洞阅读/哲学咖啡馆业余主持` — scaffold_in_name_or_path
- [drop] `户外运动/水上与潜水/补洞水/皮艇翻滚EskimoRoll` — scaffold_in_name_or_path
- [drop] `科学业余研究/生物与生态记录/南非Big_Five之外的公民观鸟清单` — scaffold_in_name_or_path
- [drop] `社群志愿/本地兴趣俱乐部/全球南节庆与社群实践/哈贾勒朝觐之外的开斋节市集志愿` — scaffold_in_name_or_path
