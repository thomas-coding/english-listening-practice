# Material Analysis: Bob's Burgers (汉堡店)

## What it is
- Very large mixed-format corpus (mp4/mkv/mp3/srt/pdf).
- MP3 set: 285 episodes, average ~22 minutes.

## Coverage validation (Pass #1 writeback)
- Video episodes detected by season/episode pattern: 285.
- Subtitle files detected by season/episode pattern (SRT): 235.
- Missing subtitle coverage against detected videos: 50 episodes.
- Confirmed missing pattern:
  - S08: missing `E11`, `E12`
  - S13: subtitle coverage missing for full season
  - S14: subtitle coverage missing for full season
  - S15: subtitle coverage missing for full season
- Interpretation: S01-S12 are mostly usable for subtitle-assisted training; S13-S15 are no-sub challenge only.

## Pedagogical value
- Strong for colloquial and humorous conversational English.
- Good authenticity bridge toward YouTube-style informal speech.
- Episode length is suitable for 30-minute lessons after clip slicing.

## Risks
- Humor and cultural references can reduce comprehension clarity.
- Data volume is huge; must pre-filter by teachability.

## Entry strategy (for this learner)
- Priority starter pool: S05-S07 and S09-S12 (clean subtitle support and mature conversational density).
- Avoid S13-S15 in early bridge stage due subtitle gaps.
- Use S08 with episode-level filtering (exclude E11/E12 in subtitle-dependent lessons).

## Recommended role in curriculum
- Mid/late-stage source for informal expression and speed tolerance.
- Use curated episodes with clean subtitle support first.

## Lesson recipe (high-yield)
1. 60-120 second no-sub first pass.
2. Subtitle-assisted repair pass on same segment.
3. Extract humor-neutral daily chunks (family, school, work).
4. 45-second recap with one opinion sentence.

## Pass #11 writeback (micro-tags)
- Starter episode micro-tags are now included in:
  - `kb/materials/sitcom_entry_microtags.md`
- Use subtitle-safe seasons first (for example, S06 starter episodes).

## Pass #15 writeback (timestamp micro-tags)
- Timestamp-level starter clips (`start_end`) were added for S06E01-S06E04 in:
  - `kb/materials/sitcom_entry_microtags.md`
- This gives direct colloquial bridge slices for S2 lessons.

## Open tasks
- Expand curated timestamped starter list from S06E01-04 to 10 subtitle-safe episodes.
- Build expression bank from recurring family/school/work contexts.
