# Benchmark Mini-Set Rehearsal Protocol

## Purpose
- Rehearse benchmark execution flow before formal monthly benchmark cycles start.
- Ensure controlled/bridge/authentic layers are all testable in current workflow.

## Mini-set composition (3 tasks)
Use preselected picks from:
- `kb/qa/benchmark_mini_set_picks_pass17.md`

1. Controlled layer (S0 style)
   - Source: `daily` or `englishpod` E1/E2.
   - Clip length: 60-90 seconds.
2. Bridge layer (S1 style)
   - Source: `初来乍到` Tier A/B or subtitle-safe `burgers` starter episode.
   - Clip length: 60-120 seconds.
3. Authentic layer (S2/S3 transition)
   - Source: YouTube validated pool (`kb/materials/youtube_clip_validation_pass10.md`).
   - Clip length: 90-150 seconds.
   - If YouTube is unavailable, use one local `authentic_proxy_local` fallback and mark it in scorecard notes.

## Rehearsal steps (single run)
1. Run no-sub first pass for each task.
2. Collect gist and detail outputs immediately.
3. Run one repair replay for each task.
4. Score with KPI dimensions (gist, detail, error repair, recap).
5. Record results in `kb/qa/regression_scorecard.json` as rehearsal-only note if needed.

## Pass condition
- Workflow pass if all 3 tasks can be executed and scored end-to-end.
- Content score is secondary in rehearsal; pipeline reliability is primary.

## Failure handling
- If any task cannot be delivered due material/ops issues:
  - log issue in `kb/operations/issue_log.md`,
  - swap to fallback material from same layer,
  - rerun rehearsal within next mentor-learning pass.
- If authentic YouTube task fails only because of network instability:
  - run local proxy fallback to complete pipeline check,
  - keep official benchmark run pending until YouTube task is executable.

## Notes
- Rehearsal does not replace official monthly benchmark tracking.
- First formal benchmark remains scheduled after first 3 real lessons.
