# Backup and Restore Protocol

## Backup policy
- Weekly backup of `kb/` folder.
- Keep at least last 8 weekly backups.
- Optional monthly frozen snapshot for long-term trend analysis.

## Minimal backup set
- `kb/learner/*`
- `kb/mentor/*`
- `kb/materials/*`
- `kb/operations/*`
- `kb/qa/*`

## Restore checks
1. Ensure `progress_snapshot.json` loads.
2. Ensure `lesson_log.jsonl` is readable.
3. Ensure benchmark scorecard is intact.
4. Run session bootstrap order.

## Corruption fallback
- If latest snapshot is corrupt, recover from latest valid backup then replay lesson logs.
