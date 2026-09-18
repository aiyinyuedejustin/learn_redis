# rule_rubric_report

- updated: 2026-09-18T14:08:12
- round: `RULE_RUBRIC_R010` (+ light re-run after gap_expand)

## Pass 1 (pre-judge)
- before: 2106 → after restores/fixes: 2102
- reject final: 1 (template scaffold `…之外的Dwile`)
- merge final: 3 (HAB near-dup, ATV near-dup, ICAR山地救援)
- Latin-token disjoint guard added; craft EN tapestry/landscape allowed

## Pass 2 (light, post gap_expand)
- before import+rubric peak: 2254
- merge: 4 (see audit_apply_log)
- after: **2250**
- URL-missing alone: **never reject**

## Proof
- script: `scripts/rule_rubric_purge.py`
- audit: `audit_apply_log` round_id=RULE_RUBRIC_R010
- anti_slop prefs: `anti_slop/PREFERENCES.md`
