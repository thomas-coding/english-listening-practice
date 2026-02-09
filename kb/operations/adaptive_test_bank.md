# Adaptive Test Bank (3/10/20-Min)

## Purpose
- Provide fast, repeatable checks for placement, recovery, and progression control.
- Support intent `做个测试` without replacing the monthly fixed benchmark suite.

## Check types

### T3: Pulse Check (3 min)
- Input: one 45-60s clip.
- Tasks:
  1) one-sentence gist,
  2) one key detail.
- Score (0-10): gist 6 + detail 4.
- Use when: lesson start state is uncertain.

### T10: Mini Diagnostic (10 min)
- Input: two clips (60-90s each), usually one controlled + one semi-authentic.
- Tasks:
  1) gist for each clip,
  2) total 3 key details,
  3) one corrected listening error,
  4) 30-45s recap.
- Score (0-30): gist 10 + details 8 + repair 6 + recap 6.
- Use when: after long gap or after 2 weak lessons.

### T20: Stress Check (20 min)
- Input: one 3-5 minute clip with no-sub first pass and repair pass.
- Tasks:
  1) gist,
  2) 5 details,
  3) 3 corrected errors,
  4) 60-90s recap.
- Score (0-50): gist 15 + details 15 + repair 10 + recap 10.
- Use when: promotion/demotion decision points.

## Routing rules
- `T3 < 4` -> choose `low` blueprint.
- `T3 4-7` -> choose `normal` blueprint.
- `T3 >= 8` and recent stable passes -> choose `high` blueprint.
- If `T10 < 16`, pause difficulty increase for next 2 lessons.
- If `T20 < 28`, step down one difficulty tier and run recovery lesson.

## Stage-aware source routing
- S0: controlled sources only (`daily`, `englishpod` E1/E2).
- S1: controlled + bridge sitcom clips (`初来乍到` Tier A/B).
- S2: bridge + selected YouTube Y1/Y2 clips.
- S3: YouTube Y2/Y3/Y4 and mixed authentic clips.

## Logging contract
- Each test event in `lesson_log.jsonl` should include:
  - `test_type` (`T3`/`T10`/`T20`)
  - `test_score`
  - `source_layer` (`controlled`/`bridge`/`authentic`)
  - `decision` (`low`/`normal`/`high` or `promote`/`hold`/`recover`)

## Guardrail note
- Adaptive checks are formative controls.
- Monthly fixed benchmark protocol in `kb/qa/benchmark_suite.md` remains mandatory for anti-drift tracking.
