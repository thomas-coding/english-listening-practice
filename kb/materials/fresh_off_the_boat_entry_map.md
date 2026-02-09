# Fresh Off the Boat Entry Map (A/B/C + Subtitle Reliability)

## Scope
- Source: `D:\邬金平\初来乍到`.
- Objective: define season-level entry tiers and subtitle reliability for lesson assignment.

## Coverage validation
- Video episodes detected: 116.
- MP3 episodes detected: 116 (no missing against video set).
- LRC subtitle episodes detected: 79.
- Missing LRC against video episodes: 37.
- Key gap pattern: full-season LRC gaps in `S05` and `S06`.

## Season reliability map
- `S01`: videos 13, lrc 13 -> reliability `R1` (full subtitle support).
- `S02`: videos 24, lrc 24 -> reliability `R1` (full subtitle support).
- `S03`: videos 23, lrc 23 -> reliability `R1` (full subtitle support).
- `S04`: videos 19, lrc 19 -> reliability `R1` (full subtitle support).
- `S05`: videos 22, lrc 0 -> reliability `R3` (no subtitle support).
- `S06`: videos 15, lrc 0 -> reliability `R3` (no subtitle support).

## Difficulty entry tiers
- Tier A (entry bridge): `S01-S02` + reliability R1.
  - Use for first sitcom bridge lessons with subtitle-assisted repair.
- Tier B (stable transition): `S03-S04` + reliability R1.
  - Use after gist stability is reached on Tier A clips.
- Tier C (no-sub challenge): `S05-S06` + reliability R3.
  - Use only when no-sub robustness is stable enough.

## Lesson assignment rules
1. Start from Tier A with 60-120 second clips.
2. Promote to Tier B only after 2 consecutive passes on Tier A gist threshold.
3. Enter Tier C only after stable no-sub gist in Tier B.
4. If Tier C fails twice consecutively, step back to Tier B with one repair-focused lesson.

## Practical note
- Episode duration by season is stable around ~21 minutes, so difficulty control should rely on subtitle reliability and dialogue complexity, not duration.
