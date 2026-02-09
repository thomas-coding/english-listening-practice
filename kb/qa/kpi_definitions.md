# KPI Definitions

## Core KPIs

1. First-pass gist accuracy (%):
- Definition: correct gist tasks / total gist tasks in lesson.

2. Detail capture rate (%):
- Definition: correctly captured key details / total target details.

3. Error recurrence rate (%):
- Definition: repeated prior error patterns / total detected errors.

4. No-subtitle robustness score (0-100):
- Composite of gist accuracy + detail capture on no-sub tasks.

5. Recap quality (0-5):
- 0 none, 1 fragmented, 3 coherent basic narrative, 5 coherent with precise details.

## Rolling indicators
- 7-lesson moving average total score.
- 30-day no-sub robustness trend.
- Monthly benchmark delta vs previous month.

## Regression trigger
- If monthly benchmark has >=2 KPI declines beyond threshold, set `regression_alert=true`.
