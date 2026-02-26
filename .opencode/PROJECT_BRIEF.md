# Project Brief - listening_plan

## Goal
- Long-term: smooth understanding of normal YouTube videos without subtitles.
- Near-term: stable lesson data loop (lesson delivery + KPI/review writeback + anti-drift benchmark checks).

## Stable Rules (Project-level)
- Work only in canonical repo `D:\邬金平\听力计划`.
- On every restart, run the startup read order and reconfirm `phase/stage`, `next action`, and session mode.
- After every lesson, complete required learner artifact writeback and run data integrity check.
- Keep stage-gate and anti-drift controls active; do not increase difficulty during regression recovery.
- In learner mode, always ask a short prompt first and wait for explicit `ok` before any media playback.
- For segment playback, anchor the target sentence first, then apply lead/trail padding (default +/- 4s) to avoid clipping key words.
- Keep dual-track flow: teacher line prebuilds lesson assets first (clips, timestamp anchors, subtitle snippets, fallback windows), learner line focuses on smooth 30-min delivery.

## Important Paths
- `README_START.md`
- `AGENTS.md`
- `.opencode/SESSION_STATE.md`
- `kb/operations/lesson_data_contract.md`
- `kb/operations/data_integrity_check.md`
- `kb/operations/lesson_protocol_30min.md`

## Done Definition
- Lesson done: lesson delivered, required artifacts updated, integrity check passed.
- Phase done: >=5 real lessons logged, review scheduler recalibrated, monthly benchmark tracking active.
- Program done: Stage S3 target met (no-sub robustness >=75 on 8-12 minute videos, no regression alert).

## Maintenance
- Keep this file stable and brief; only update when goals/rules change.
- Update `.opencode/SESSION_STATE.md` for moving status and next action.
