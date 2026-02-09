# Session Bootstrap Checklist

## Step 1: Load context quickly
Read in this order:
1. `README_START.md`
2. `kb/learner/progress_snapshot.json`
3. `kb/learner/learner_profile.md`
4. `kb/materials/materials_index.md`
5. `kb/qa/quality_guardrails.md`
6. `kb/qa/kpi_definitions.md`
7. `kb/mentor/stage_gate_framework.md`
8. `kb/mentor/learning_plan_todo.md`
9. `kb/operations/lesson_data_contract.md`
10. `kb/operations/gap_handling_rules.md`

## Step 2: Confirm mode with learner
- Mode A: "我来学一节课" -> deliver one 30-minute lesson.
- Mode B: "你自己学下" -> run mentor self-learning pass and update KB.
- Reference: `kb/operations/user_intent_map.md`.

## Step 3: Before ending session
- Append event to `kb/learner/lesson_log.jsonl`.
- Update `kb/learner/progress_snapshot.json`.
- Update `kb/learner/review_queue.json` if needed.
- Update mastery trackers (`mastery_vocab`, `mastery_chunks`, `error_patterns`).

## Step 4: Data integrity check
- If required lesson artifacts are missing, mark `data_integrity_pending=true` and repair first next session.
- Follow `kb/operations/data_integrity_check.md` quick checklist.
