# Monthly Maintenance Protocol

## Checklist
1. Run benchmark suite and update `regression_scorecard.json`.
2. Compute KPI trends and compare with previous month.
3. Review top 10 recurring error patterns.
4. Prune stale review items (resolved > 60 days).
5. Refresh stage-gate status.
6. Archive monthly summary into lesson log.

## Output artifact
- Create one monthly summary entry in `kb/learner/lesson_log.jsonl` with:
  - benchmark scores
  - trend direction
  - next-month focus
