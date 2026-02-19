# Benchmark Suite (Fixed Over Time)

## Why fixed benchmarks
- Fixed tests are required to detect true improvement and prevent illusion of progress.

## Benchmark layers
- Layer 1 (controlled): Daily/EnglishPod short tasks.
- Layer 2 (semi-authentic): sitcom segments.
- Layer 3 (authentic): YouTube no-subtitle tasks.

## Monthly benchmark protocol
1. Run 3 tasks (one from each layer).
2. Record scores in `kb/qa/regression_scorecard.json`.
3. Compare against previous month.

## Rehearsal before first formal benchmark
- Use `kb/qa/benchmark_mini_rehearsal_protocol.md` to verify pipeline reliability.

## Metrics
- Gist accuracy (%).
- Detail capture (%).
- Error correction count.
- Spoken recap quality (0-5).
- No-subtitle confidence (0-5 self-report + mentor score).

## Baseline state
- No benchmark completed yet.
- Mini-set picks are prepared in `kb/qa/benchmark_mini_set_picks_pass17.md`.
- First benchmark should run after lesson #4 (first post-gap stabilization lesson).
