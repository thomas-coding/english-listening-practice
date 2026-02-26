# AGENTS Handoff (OpenCode/Codex)

## Canonical Workspace
- Local working repo (single source of truth): `D:\邬金平\听力计划`
- Remote: `https://github.com/thomas-coding/english-listening-practice`
- Rule: do not maintain duplicate working copies; this directory is the only active local repo.

## Mission
- Build and operate a long-term English listening mentor system.
- End goal: smooth comprehension of normal YouTube videos without subtitles.

## Startup Protocol (Mandatory)
On every fresh session, read in this exact order before acting:
1. `README_START.md`
2. `kb/operations/session_bootstrap.md`
3. `kb/learner/progress_snapshot.json`
4. `kb/learner/learner_profile.md`
5. `kb/materials/materials_index.md`
6. `kb/qa/quality_guardrails.md`
7. `kb/qa/kpi_definitions.md`
8. `kb/mentor/stage_gate_framework.md`
9. `kb/mentor/learning_plan_todo.md`
10. `kb/operations/lesson_data_contract.md`
11. `kb/operations/gap_handling_rules.md`

Then explicitly confirm:
- current phase/stage,
- active next action,
- whether this session is Lesson mode or Mentor-learning mode.

## Session Modes
- Mode A: user intent like `我来学一节课` -> deliver one 30-minute lesson using `kb/operations/lesson_protocol_30min.md`.
- Mode A shortcut: user intent `开始我的学习` -> auto decide review-first or direct lesson, then run teaching flow.
- Mode B: user intent like `你自己学下` -> run mentor self-learning pass and write findings into KB.

## Dual-Track Runtime
- Follow `kb/operations/dual_track_runtime.md`.
- Learner line priority: low waiting time and continuity.
- Teacher line priority: heavy analysis/writeback and prebuild next 2-3 lessons.
- Prebuilt queue source: `kb/operations/prebuilt_lessons_queue.md`.

## Data Discipline (Non-negotiable)
After each lesson or mentor-learning pass, update all required artifacts:
- `kb/learner/lesson_log.jsonl`
- `kb/learner/progress_snapshot.json`
- `kb/learner/review_queue.json` (if applicable)
- `kb/learner/mastery_vocab.json` (if applicable)
- `kb/learner/mastery_chunks.json` (if applicable)
- `kb/learner/error_patterns.json` (if applicable)

Run integrity check via `kb/operations/data_integrity_check.md`.
If any required artifact is missing, set `data_integrity_pending=true` and repair first next session.

## Quality and Anti-Drift
- Keep fixed benchmark strategy active (`kb/qa/benchmark_suite.md`).
- Respect regression handling and stage-gate controls.
- Do not increase difficulty when regression recovery is in progress.

## Playback Operations (Preferred)
Use media-playback scripts documented in `kb/operations/playback_ops.md`:
- `C:\Users\wujin\.config\opencode\skills\media-playback\scripts\play_media.py`
- `C:\Users\wujin\.config\opencode\skills\media-playback\scripts\find_youtube.py`
- `C:\Users\wujin\.config\opencode\skills\media-playback\scripts\extract_segment_subtitles.py`

## Current Program State
- Phase: lesson data loop active (passes 1-17 and pass20 completed; lessons #1-#4 delivered).
- Lessons completed: 4.
- Immediate backlog:
  1. Deliver lesson #5 and accumulate stable KPI traces.
  2. Trigger review scheduler recalibration after lesson #5.
  3. Continue monthly benchmark tracking from BM2026M02 baseline.

## Git Operating Rule
- Work only in this repo directory.
- When user asks to push, commit relevant updates and push to `origin/main`.
- Do not amend history unless user explicitly requests it.
