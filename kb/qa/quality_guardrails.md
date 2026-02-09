# Quality Guardrails (Anti-Drift)

## Goal
- Ensure the teaching system gets better over time, not worse.

## Hard rules
1. No lesson is complete without data updates.
2. Keep fixed benchmark tasks and re-test monthly.
3. Any drop in benchmark score triggers a correction cycle.
4. New teaching tactics must be logged with evidence.

## What "better over time" means
- Higher first-pass comprehension at same difficulty.
- Fewer repeated error patterns.
- More stable no-subtitle performance.
- Faster recovery from difficult content.

## Drift detection
- Compare current month vs previous month on the same benchmark set.
- If 2+ key metrics fall, mark `regression_alert = true`.

## Recovery plan when regression appears
1. Pause difficulty increase for 3 lessons.
2. Run targeted repair lessons on top 2 error types.
3. Re-test benchmark mini-set.
4. Resume progression only after recovery.

## Data integrity checks
- Snapshot files must match lesson logs.
- Review queue must be updated after each lesson.
- Unknown words/chunks from lesson must enter mastery tracker.

## Health tracking
- Maintain a periodic system health score using `kb/qa/health_score_method.md`.
- If health score < 70, run maintenance before difficulty progression.
