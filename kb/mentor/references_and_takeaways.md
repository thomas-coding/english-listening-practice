# References and Takeaways (for system design)

## Consulted references (2026-02-09)
1. The Learning Scientists - Retrieval Practice.
2. The Learning Scientists - Spaced Practice.
3. Victoria University (Paul Nation resources page and linked resource ecosystem).
4. SLA overview references (interlanguage, variability, cognitive + sociocultural factors).
5. Deliberate practice literature summary references.

## Practical takeaways integrated into KB
- Retrieval + feedback must be mandatory in each lesson.
- Spaced review must be built into data model (review queue + due dates).
- Learner errors are developmental signals, not random noise -> error pattern tracker.
- Expertise growth needs deliberate weak-point focus -> stage-gate and adaptive rules.
- Long-term system needs anti-drift checks -> benchmark suite + regression scorecard.

## Caution
- Some web sources are broad summaries. Use them for system principles, not as sole empirical evidence.

## Pass #1 material-intelligence takeaways (2026-02-09)
- Desperate Housewives has effectively full transcript support for detected video episodes, so it is suitable for transcript-assisted repair loops.
- Burgers subtitle support is strong in S01-S12 (except S08E11-12) but drops sharply in S13-S15, so season-level filtering is mandatory.
- For this learner stage, sitcom usage should prioritize short clip cycles (no-sub -> repair -> chunk extraction -> recap), not full-episode exposure.
- YouTube remains the final transfer target and must be prepared early through staged gating, not postponed indefinitely.

## Pass #2 Daily takeaways (2026-02-09)
- A concrete first-10-lesson Daily seed map is now available with tier progression (D1 -> D2 -> D3).
- Episode-level duration checks improve lesson feasibility; clips from longer episodes can still be used if chunk size is controlled.
- For this learner, transition from daily-life topics to workplace abstraction should happen within the first 10 lessons to avoid plateau.

## Pass #3 EnglishPod takeaways (2026-02-09)
- EnglishPod early episodes show strong PB/RV/DG completeness in sampled `0001-0030`, enabling reliable triad-based lesson design.
- PB/RV/DG timing can be standardized into a 30-minute template, reducing lesson variance while preserving adaptation room.
- Output after RV is mandatory; otherwise learners can become explanation-dependent without improving first-pass decoding.

## Pass #4 Daily progression takeaways (2026-02-09)
- Topic-tagged first-30 mapping helps avoid random episode hopping and keeps difficulty progression controllable.
- Recovery controls (fallback to D1 after repeated D2 failures) are important to prevent confidence collapse.
- Duration-aware clipping is non-negotiable for episodes over 22 minutes.

## Pass #5 EnglishPod progression takeaways (2026-02-09)
- PB/RV/DG completeness in early EnglishPod allows stable triad-based lesson engineering at scale.
- Topic-tagged first-30 mapping improves transfer planning from controlled dialogue to workplace/finance themes.
- High-load triads (>22 minutes total) should always use selected segments to protect output quality.

## Pass #6 YouTube ladder takeaways (2026-02-09)
- YouTube transfer becomes actionable only after adding level gates, query packs, and fallback rules.
- Topic progression (routine -> work -> commentary -> interview) reduces authenticity shock.
- No-sub first pass remains mandatory; subtitle use belongs to repair only.

## Pass #7 Fresh Off the Boat takeaways (2026-02-09)
- Subtitle reliability is the primary control variable here: `S01-S04` are suitable for subtitle-assisted bridge lessons; `S05-S06` are no-sub challenge only.
- Because episode duration is stable across seasons, tiering should depend on subtitle availability and dialogue complexity, not length.

## Pass #8 state-based blueprint takeaways (2026-02-09)
- State-aware lesson blueprints reduce both overtraining risk on fatigue days and undertraining risk on momentum days.
- Output floors should scale by state so quality remains measurable even when lesson intensity changes.

## Pass #9 adaptive test-bank takeaways (2026-02-09)
- A short T3 pulse check is enough to route most sessions into low/normal/high blueprint safely.
- T10 and T20 provide objective hold/recover decisions and reduce subjective difficulty jumps.

## Pass #10 YouTube validation takeaways (2026-02-09)
- Query-pack based candidate selection is workable for fast curation, but manual checks remain necessary for audio clarity and speaker count.
- Duration filtering is critical: some selected clips can exceed target bounds and must be explicitly rejected.

## Pass #11 sitcom micro-tagging takeaways (2026-02-09)
- A shared micro-tag schema across sitcom sources significantly reduces lesson assembly friction.
- Tagging by `target_stage`, `recommended_state`, and `subtitle_reliability` improves consistency in clip selection.

## Pass #12 review scheduler takeaways (2026-02-09)
- A baseline spaced-review scheduler can be defined before real lesson volume arrives, but must include a fixed recalibration trigger.
- Error-pattern items need tighter intervals than generic vocabulary to reduce recurrence.

## Pass #13 benchmark rehearsal takeaways (2026-02-09)
- Benchmark reliability should be rehearsed as an operational pipeline (material -> playback -> scoring), not only as a scoring rubric.
- Layer-balanced mini-set design (controlled/bridge/authentic) reduces blind spots before formal benchmark cycles begin.
