# Data Integrity Check (Fast)

## Run at session end (2-3 minutes)
1. `lesson_log.jsonl` got a new line.
2. `progress_snapshot.json` key fields updated.
3. `review_queue.json` updated if new review items exist.
4. mastery trackers updated if new unknown words/chunks/errors were observed.

## If any check fails
- Set `data_integrity_pending=true` in snapshot.
- Next session starts with a repair update before new lesson delivery.
