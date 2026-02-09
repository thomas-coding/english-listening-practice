# Review Scheduler Rules (v0, pre-lesson baseline)

## Purpose
- Turn lesson outputs into spaced review actions with predictable workload.
- Keep review sustainable before and after real lesson data starts accumulating.

## Item types
- `vocab` (single words in context)
- `chunk` (multi-word expressions, discourse patterns)
- `error_pattern` (repeatable decoding/inference mistakes)

## Default spacing ladders
- `vocab`: D0 -> D1 -> D3 -> D7 -> D14 -> D30.
- `chunk`: D0 -> D2 -> D5 -> D10 -> D21 -> D45.
- `error_pattern`: D0 -> D1 -> D4 -> D8 -> D16 -> D32.

## Promotion/demotion rules
- Promote item to next interval when recall quality >= 3/5.
- Hold interval when recall quality = 2/5.
- Demote one interval when recall quality <= 1/5.
- Archive as stable when two consecutive recalls >= 4/5 at interval >= D21.

## Daily workload caps
- Max new items per lesson:
  - vocab: 8
  - chunk: 6
  - error_pattern: 3
- Max review items per day: 25 (soft cap), 35 (hard cap).
- If hard cap exceeded, defer lowest-priority vocab items by +1 day.

## Priority order
1. `error_pattern` due items
2. `chunk` due items
3. `vocab` due items
4. new items from current lesson

## Gap-aware adjustment
- If `days_since_last_lesson >= 11`, run reactivation review first:
  - 2 error patterns + 3 chunks + 5 vocab items.
- Freeze new-item intake for one lesson when overdue queue > 35.

## Logging contract
- For each reviewed item, store:
  - `item_id`, `item_type`, `recall_quality`, `next_due_date`, `status`.
- Scheduler action should be reflected in:
  - `kb/learner/review_queue.json`
  - `kb/learner/mastery_vocab.json` / `kb/learner/mastery_chunks.json` / `kb/learner/error_patterns.json`

## Calibration plan
- This is a pre-lesson baseline (v0).
- Recalibrate intervals and caps after first 5 real lessons.
