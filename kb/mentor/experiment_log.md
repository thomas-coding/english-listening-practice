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

### 2026-02-18 (Pass #17)
- Hypothesis: Preselected benchmark mini-set picks with explicit fallback routing will make first benchmark execution stable and comparable.
- Intervention: Added fixed mini-set picks for controlled/bridge/authentic layers and defined local proxy fallback for YouTube instability.
- Evidence: New picks file + rehearsal protocol updates now provide executable paths for both online and offline constraints.
- Decision: Run first benchmark mini-set after lesson #4 using this pick set and log scorecard baseline.

### 2026-02-20 (Pass #20)
- Hypothesis: Running the first benchmark mini-set after lesson #4 will expose true no-sub baseline and sharpen lesson #5 priorities.
- Intervention: Executed C1/B1/A1 mini-set with no-sub first pass and targeted repair.
- Evidence: Scorecard baseline recorded (`BM2026M02_first`), showing low first-pass robustness with consistent repair recovery.
- Decision: Route lesson #5 toward opening-turn binding and dialogue-only decode; keep benchmark continuity from this baseline.

### 2026-02-20 (Ops refinement)
- Hypothesis: Explicit dual-track runtime and prebuilt lesson queue will reduce learner waiting and improve session continuity.
- Intervention: Added learner-line latency policy, teacher-line heavy-task policy, and prebuilt queue for lessons #5-#7.
- Evidence: Runtime policy is now documented and linked by intent map/protocol/agents handoff.
- Decision: Keep this as default operating model and monitor learner-line wait-time friction in issue log.

### 2026-02-26 (Pass #23)
- Hypothesis: If teacher line prepares complete package assets before class, learner-line 30-minute sessions will stay smooth and avoid clip-cut mistakes.
- Intervention: Rebuilt upcoming lessons #7-#9 into package files with clip manifest, anchor timestamps (+/-4s), subtitle snippets, fallbacks, and correction guides.
- Evidence: Added `lesson_0007_package.md`, `lesson_0008_package.md`, and `lesson_0009_package.md`; updated queue to consume only `ready` packages.
- Decision: Keep package-first teacher-line flow as default and run Pass #19 recalibration before delivering lesson #7.
