# Material Analysis: Fresh Off the Boat (初来乍到)

## What it is
- Sitcom corpus with mkv/mp3/lrc/script documents.
- MP3 average ~21 minutes.

## Pass #7 writeback (A/B/C entry map)
- A season-level entry map with subtitle reliability is now defined in:
  - `kb/materials/fresh_off_the_boat_entry_map.md`
- Coverage finding: `S01-S04` have full LRC support, while `S05-S06` have full-season LRC gaps.
- This closes the entry-tier and subtitle-reliability gap for this source.

## Pass #11 writeback (micro-tags)
- Entry-safe episode micro-tags are now defined in:
  - `kb/materials/sitcom_entry_microtags.md`
- This enables faster lesson assembly by state (`low`/`normal`/`high`) and stage (`S1`/`S2`).

## Pass #15 writeback (timestamp micro-tags)
- Timestamp-level starter clips (`start_end`) were added for S01E01/S01E02/S01E05/S02E01 in:
  - `kb/materials/sitcom_entry_microtags.md`
- This enables direct clip slicing without per-lesson manual scan.

## Pedagogical value
- Strong bridge from textbook-like speech to authentic conversational flow.
- Good for subtitle control progression: full -> partial -> none.

## Risks
- Some episodes lack aligned auxiliary subtitle files in certain formats.
- Dialogue density can spike; can overwhelm early-stage lessons.

## Recommended role in curriculum
- Mid-stage transition corpus.
- Use selected easier episodes first, then increase speed density.

## Teaching use constraints
- Keep `S05-S06` out of subtitle-dependent lessons.
- Use `S01-S04` as core for repair loops and chunk extraction.

## Open tasks
- Expand timestamped starter clips from S01/S02 into S03/S04 transition episodes.
