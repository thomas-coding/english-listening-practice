# 30-Min Lesson Protocol

## Entry shortcut
- If user says `开始我的学习`, assistant must auto-select review-first or direct lesson using:
  - `kb/operations/user_intent_map.md` (auto-plan rule)
  - `kb/operations/gap_handling_rules.md`
- User does not need to provide stage/state/material choice.

## Runtime policy
- Learner line must follow `kb/operations/dual_track_runtime.md`.
- Prefer prebuilt lesson assets from `kb/operations/prebuilt_lessons_queue.md` to reduce wait time.
- Defer heavy backend tasks to teacher line unless they are required to unblock the live segment.
- Before playback starts, load a prebuilt package (clip manifest + anchor sheet + subtitle snippets + fallbacks).
- If package is incomplete, do only minimal unblock actions in class and record missing prep for teacher-line backfill.

## Step 0: Pick lesson state blueprint
- Before starting, select `low` / `normal` / `high` using:
  - `kb/operations/lesson_blueprints_state_based.md`
- Then run the matching 30-minute structure.

## Default structure
- 0-3 min: objective and attention target.
- 3-10 min: first-pass listening (no pause).
- 10-18 min: second-pass repair (targeted replay).
- 18-24 min: focused extraction (errors + chunks).
- 24-29 min: spoken recap (45-90 seconds).
- 29-30 min: score + next action.

## Required outputs
- One-sentence gist.
- Corrected errors and reusable chunks must meet state floor.
- One spoken recap (length by state floor).

## State-specific output floor
- `low`: gist + 2 errors + 3 chunks + short recap.
- `normal`: gist + 3 errors + 5 chunks + recap.
- `high`: gist + 4 errors + 6 chunks + extended recap.

## Pass/fail decision
- Pass: gist clear + error correction complete + recap done.
- Borderline: gist weak but corrected with replay.
- Fail: gist missing and no usable recap.
