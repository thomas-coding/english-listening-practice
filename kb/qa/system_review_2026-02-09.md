# System Design Review (2026-02-09)

## Review objective
- Validate whether current mentor system can improve over long time horizons (months/years) toward the vision: smooth no-subtitle YouTube comprehension.

## Reference principles consulted
- Retrieval practice: learning improves when recall is effortful and followed by feedback.
- Spaced practice: distributed review beats cramming for long-term retention.
- Deliberate practice: specific goals, immediate feedback, and weak-point targeting are key.
- SLA variability/interlanguage: learner errors are systematic and should be tracked as developmental signals.

## Evaluation dimensions

### 1) Persistence and continuity
- Status: pass.
- Evidence: snapshot + append-only logs + bootstrap order already implemented.
- Risk: medium if data integrity checks are skipped.

### 2) Personalization depth
- Status: partial pass.
- Evidence: learner profile and competency model exist.
- Gap found: mastery updates need strict contract and lesson-gap handling.

### 3) Anti-drift safeguards
- Status: pass (baseline).
- Evidence: fixed benchmark suite + regression scorecard + guardrails created.
- Gap found: KPI formulas and monthly maintenance cadence needed.

### 4) Operational reliability
- Status: pass (with caveats).
- Evidence: media-playback script workflow validated.
- Gap found: backup/restore protocol should be explicit.

### 5) Pedagogical progression control
- Status: partial pass.
- Evidence: adaptive rules exist.
- Gap found: formal stage-gate promotion/demotion rules needed.

## Decisions from this review
1. Add KPI definition and health scoring.
2. Add stage-gate framework for progression control.
3. Add gap-handling rules for irregular attendance.
4. Add backup/restore and monthly maintenance protocol.

## Review result
- Architecture quality: improved from v1 to v1.1 (anti-drift reinforced).
- Confidence: medium-high for 1-year continuity, contingent on strict per-lesson data updates.
