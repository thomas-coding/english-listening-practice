# User Intent Map

## Purpose
- Keep interactions stable and predictable across future sessions.

## Supported intents
- `我来学一课` -> run one 30-minute adaptive lesson.
- `开始我的学习` -> auto-run today's teaching plan (assistant decides review-first or new lesson).
- `你自己学下` -> run mentor self-learning pass and update KB.
- `复习一下` -> run review-only lesson from review queue.
- `做个测试` -> run adaptive check from `kb/operations/adaptive_test_bank.md` (T3/T10/T20).
- `总结进度` -> output current stage, KPIs, weaknesses, next step.

## Auto-plan rule for `开始我的学习`
1. Load bootstrap files and recover current stage.
2. Check `days_since_last_lesson` and due items in `kb/learner/review_queue.json`.
3. Route mode automatically:
   - If `days_since_last_lesson >= 4` or overdue due-items >= 8 -> start with 8-12 min review reactivation block.
   - Else -> start directly with adaptive lesson.
4. Pick state (`low`/`normal`/`high`) from latest evidence + quick warmup performance.
5. Use confirm-before-playback flow for each segment.
6. In learner line, follow `kb/operations/dual_track_runtime.md` latency policy.
7. End with score + mandatory data writeback.

## Dual-track execution rule
- Learner line (`开始我的学习`): prioritize continuity and low waiting time.
- Teacher line (`你自己学下`): run heavy analysis/writeback and prebuild next lessons.
- Prebuilt queue reference: `kb/operations/prebuilt_lessons_queue.md`.

## Startup phrase (recommended)
- `加载导师知识库并进入教学模式`

## Expected assistant behavior
- Read bootstrap files first.
- Confirm current stage and pick lesson objective.
- Execute playback with script-based operations.
- End with scoring + data updates.
