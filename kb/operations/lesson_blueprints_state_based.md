# 30-Min Lesson Blueprints by Learner State

## Purpose
- Keep lesson quality stable under variable energy, focus, and attendance gaps.
- Avoid over-pushing on low-state days and under-challenging on high-state days.

## State selection (before minute 0)
- `low` if any two signals are true:
  - learner self-report energy/focus <= 2/5,
  - `days_since_last_lesson >= 11`,
  - previous lesson result was `fail`.
- `high` if all signals are true:
  - learner self-report energy/focus >= 4/5,
  - previous two lessons were `pass`,
  - no active regression alert.
- `normal` for all other cases.

## Blueprint A: Low-state recovery (30 min)
- 0-2 min: set one narrow objective (only one confusion type).
- 2-7 min: short first pass (45-90s, no pause).
- 7-14 min: targeted repair with support text only on hotspot.
- 14-20 min: extract minimum set (2 corrected errors + 3 chunks).
- 20-27 min: guided recap (30-60s, scaffold allowed).
- 27-30 min: score, recovery note, and easy carry-over task.

## Blueprint B: Normal-state standard (30 min)
- 0-3 min: objective and attention target.
- 3-10 min: first-pass listening (no pause).
- 10-18 min: second-pass repair (targeted replay).
- 18-24 min: focused extraction (errors + chunks).
- 24-29 min: spoken recap (45-90s).
- 29-30 min: score + next action.

## Blueprint C: High-state stretch (30 min)
- 0-3 min: stretch objective with one additional challenge.
- 3-11 min: longer no-sub first pass (120-180s).
- 11-19 min: repair with reduced support (text delayed).
- 19-25 min: second clip or contrast segment for transfer.
- 25-29 min: recap + one opinion sentence (60-120s).
- 29-30 min: score and progression decision.

## Output minimum by state
- `low`: gist + 2 corrected errors + 3 chunks + short recap.
- `normal`: gist + 3 corrected errors + 5 chunks + standard recap.
- `high`: gist + 4 corrected errors + 6 chunks + extended recap.

## Safety rules
- If two consecutive low-state lessons fail, run one controlled-source repair block next session.
- If high-state lesson fails gist threshold, immediately return to normal blueprint.
- Never promote difficulty during regression recovery window.

## Logging requirement
- Every lesson log must include:
  - `state_selected` (`low`/`normal`/`high`)
  - `state_reason_tags` (e.g., `long_gap`, `fatigue`, `momentum`)
