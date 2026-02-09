# Lesson Data Contract

## Required data artifacts after each lesson
1. Append one JSON line to `kb/learner/lesson_log.jsonl`.
2. Update `kb/learner/progress_snapshot.json`:
   - total_lessons_completed
   - latest_lesson_score
   - rolling_7d_avg_score
   - top_weakness_tags (if known)
3. Update `kb/learner/review_queue.json`:
    - add new items (unknown chunks/words, repeated error patterns)
    - update due dates
   - follow `kb/operations/review_scheduler_rules.md`
4. Update mastery trackers:
   - `kb/learner/mastery_vocab.json`
   - `kb/learner/mastery_chunks.json`
   - `kb/learner/error_patterns.json`
   - Follow `kb/learner/mastery_schema.md`

## Why this matters
- Prevents forgetting across sessions.
- Ensures personalization improves over time.
- Enables spaced review and regression checks.

## Enforcement
- If any required artifact is missing, next session must start with a repair step.
