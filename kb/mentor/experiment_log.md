# Mentor Experiment Log

## Format
- Date:
- Hypothesis:
- Intervention:
- Evidence:
- Decision:

## Entries

### 2026-02-09
- Hypothesis: A persistent hybrid KB (snapshot + append logs) will improve cross-session continuity.
- Intervention: Created v1 architecture and bootstrap documents.
- Evidence: New session can restore state by reading 5 files in fixed order.
- Decision: Keep this architecture and start filling with real lesson evidence.

### 2026-02-09 (Pass #14)
- Hypothesis: A Y1-Y4 balanced 30-clip YouTube pool will improve clip routing stability and reduce random topic drift.
- Intervention: Expanded validated pool from 10 to 30 clips using fixed duration windows and query packs.
- Evidence: Added 20 new entries with balanced level distribution (`Y1=5, Y2=5, Y3=5, Y4=5`) and updated structured pool JSON.
- Decision: Keep this pool as v1.1 baseline and move to timestamp micro-tagging for faster lesson assembly.

### 2026-02-09 (Pass #15)
- Hypothesis: Timestamped sitcom micro-tags will reduce lesson assembly latency and stabilize first-pass clip quality.
- Intervention: Added 24 timestamp-level starter clips across FOTB/DH/Burgers using subtitle-density windows.
- Evidence: Each starter episode now has direct `start_end` clip slices and stable `clip_id` tags for logging.
- Decision: Use these clips to launch trial lesson #1 and collect first real KPI traces.
