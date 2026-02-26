# Dual-Track Runtime Policy

## Purpose
- Keep learner-side interaction fast and continuous.
- Move heavy preparation and system maintenance to mentor-side runs.

## Track definitions
- Learner line: live teaching interaction (`开始我的学习`, lesson/review/test mode).
- Teacher line: mentor self-learning and backend maintenance (`你自己学下` or post-lesson writeback stage).

## Learner-line latency contract
1. First actionable teaching response should be immediate (no long backend wait before giving next step).
2. After learner confirms `ok`, launch playback first, then continue with short prompts.
3. During learner line, avoid long scans/transcriptions unless strictly needed for the current question.
4. If a playback setup might take longer, send a short status line first, then execute.

## Learner-line allowed operations
- Segment playback.
- Short repair prompts and scoring.
- Minimal lookup needed to unblock the current segment.

## Learner-line deferred operations
- Large transcript extraction.
- Multi-file benchmark analysis.
- Bulk KB rewrites and integrity checks.
- Git staging/commit/push tasks.
- On-the-fly batch subtitle extraction for non-critical clips.

## Teacher-line responsibilities
1. Complete deferred writebacks and integrity checks.
2. Prebuild at least the next 2-3 lessons (materials, clips, fallback options).
3. Prepare one benchmark/assessment package ahead when relevant.
4. Update issue log and pedagogy notes from learner-line friction points.

## Teacher-line prebuild package (required)
For each upcoming lesson in queue, prepare a reusable package before learner entry:
1. Clip manifest: primary/repair/sprint windows with fixed `start/end` and objective.
2. Anchor sheet: target sentence timestamps and default context padding (usually +/-4s).
3. Subtitle snippets: pre-extracted text for each planned repair window.
4. Fallback set: at least 2 alternate short windows in same difficulty band.
5. Correction sheet: expected gist, key chunks, and likely error-to-correction mapping.

## Queue readiness rule
- Mark a lesson as `ready` only when the prebuild package is complete.
- Learner line should consume `ready` lessons first to keep the 30-minute flow continuous.

## Handoff rule
- End learner line with concise result + next planned entry point.
- Start next learner line from prebuilt queue first; only re-plan if learner state changes sharply.
