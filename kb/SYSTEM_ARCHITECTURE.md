# Knowledge Base Architecture v1

## Design goals
- Persistent across months/years.
- Fast recovery in a fresh AI session.
- Human-readable + machine-readable.
- Append-only logs for history traceability.
- Small snapshots for quick state loading.

## Folder layout
- `kb/learner/`: learner model and progress database.
- `kb/mentor/`: mentor methodology, rules, experiments, self-learning TODO.
- `kb/materials/`: material analysis and source metadata.
- `kb/operations/`: session startup, lesson delivery protocol, playback operations.
- `kb/qa/`: anti-drift quality controls, benchmarks, scorecards.
- `kb/templates/`: reusable templates.

## Data model
- Snapshot files (`*.json`, `*.md`): latest state, compact and quick to parse.
- Event logs (`*.jsonl`): append-only chronological records.
- Analysis docs (`*_analysis.md`): evolving qualitative knowledge per source.

## Update protocol (every lesson)
1. Append one line to `kb/learner/lesson_log.jsonl`.
2. Update `kb/learner/progress_snapshot.json` (scores, stage, next actions).
3. Update `kb/learner/review_queue.json` (items due for review).
4. Update mastery trackers (`mastery_vocab`, `mastery_chunks`, `error_patterns`).
5. If a new teaching insight appears, append to `kb/mentor/experiment_log.md`.

## Update protocol (mentor self-learning)
1. Pick one TODO item from `kb/mentor/learning_plan_todo.md`.
2. Analyze a bounded chunk of material (never full giant files at once).
3. Update the relevant `kb/materials/*_analysis.md` and `kb/materials/sources_summary.json`.
4. Mark progress percentage in `kb/mentor/learning_plan_todo.md`.

## Recovery protocol (new AI session)
1. Read `README_START.md`.
2. Execute `kb/operations/session_bootstrap.md` checklist.
3. Confirm current stage and ask user to start a lesson or continue mentor-learning.

## Anti-drift protocol
- Run monthly benchmark and regression checks from `kb/qa/`.
- Apply stage-gate controls from `kb/mentor/stage_gate_framework.md`.
- If regression alert appears, trigger correction cycle before difficulty increase.
