# Sitcom Timestamp Micro-Tags (Pass #15)

## Scope
- Objective: add timestamp-level micro-tags (`start_end`) for sitcom starter entries.
- Sources: Fresh Off the Boat (S01/S02), Desperate Housewives (S01), Bob's Burgers (S06).
- Target output: routing-ready 90-second windows for lesson assembly.

## Method
1. Locate subtitle files (`.lrc`/`.srt`) for the 12 starter episodes.
2. Run subtitle-density scan on 90-second windows with 30-second step.
3. Keep top windows with stable line density and non-overlap.
4. Write selected windows into `kb/materials/sitcom_entry_microtags.md` using stable `clip_id`.

## Source subtitle files
- `D:\邬金平\初来乍到\3、初来乍到1-6季音频MP3\S01\S01E01.lrc`
- `D:\邬金平\初来乍到\3、初来乍到1-6季音频MP3\S01\S01E02.lrc`
- `D:\邬金平\初来乍到\3、初来乍到1-6季音频MP3\S01\S01E05.lrc`
- `D:\邬金平\初来乍到\3、初来乍到1-6季音频MP3\S02\S02E01.lrc`
- `D:\邬金平\绝望主妇\4  音频+LRC字幕\MP3\S01E01.lrc`
- `D:\邬金平\绝望主妇\4  音频+LRC字幕\MP3\S01E02.lrc`
- `D:\邬金平\绝望主妇\4  音频+LRC字幕\MP3\S01E03.lrc`
- `D:\邬金平\绝望主妇\4  音频+LRC字幕\MP3\S01E04.lrc`
- `D:\邬金平\汉堡店\burgers\8、字幕文件1-12季\英文字幕\S06\Bobs.Burgers.S06E01.1080p.WEB.h264-NOMA_track3_eng.srt`
- `D:\邬金平\汉堡店\burgers\8、字幕文件1-12季\英文字幕\S06\Bobs.Burgers.S06E02.1080p.WEB.h264-NOMA_track3_eng.srt`
- `D:\邬金平\汉堡店\burgers\8、字幕文件1-12季\英文字幕\S06\Bobs.Burgers.S06E03.1080p.WEB.h264-NOMA_track3_eng.srt`
- `D:\邬金平\汉堡店\burgers\8、字幕文件1-12季\英文字幕\S06\Bobs.Burgers.S06E04.1080p.WEB.h264-NOMA_track3_eng.srt`

## Output summary
- Timestamped clips added: `24` (`2 clips x 12 starter episodes`).
- Updated schema fields: `clip_id`, `start_end`.
- Main writeback file:
  - `kb/materials/sitcom_entry_microtags.md`

## Quality notes
- Windows are subtitle-density seeded (routing-ready), not full scene-semantic annotations.
- Next refinement should add communicative objective labels after first lesson evidence.
