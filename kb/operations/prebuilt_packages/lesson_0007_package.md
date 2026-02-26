# Lesson #7 Prebuilt Package (ready)

## Lesson intent
- State target: `normal`.
- Objective: stabilize long-sentence audio decode while keeping opening binding accurate.
- Priority carry-over: `e_long_sentence_decode_gap`, `c_i_guess_i_could_wait`, `c_looks_like_well_be_going_for_academic_scholarships`.

## Clip manifest
- Review R1 (4 min)
  - Source: `D:\邬金平\绝望主妇\4  音频+LRC字幕\MP3\S01E03.mp3`
  - Window: `14:28-14:38`
  - Goal: proper-name bind (`Have you met Ashley?`).
- Review R2 (4 min)
  - Source: `D:\邬金平\初来乍到\3、初来乍到1-6季音频MP3\S01\S01E02.mp3`
  - Window: `19:21-20:00`
  - Goal: reactivate recent chunks before new content.
- Main A (9 min)
  - Source: `D:\邬金平\初来乍到\3、初来乍到1-6季音频MP3\S01\S01E02.mp3`
  - Window: `14:38-15:46`
  - Goal: causal chain decode (`dine and dash` -> `comes out of our pocket`).
- Main B (7 min)
  - Source: `D:\邬金平\初来乍到\3、初来乍到1-6季音频MP3\S01\S01E02.mp3`
  - Window: `16:03-16:22`
  - Goal: polite contribution phrasing (`cover their check`, `chip in`).
- Sprint (3 min)
  - Source: `D:\邬金平\初来乍到\3、初来乍到1-6季音频MP3\S01\S01E02.mp3`
  - Window: `20:12-20:22`
  - Goal: one long rule sentence under no-sub pressure.

## Anchor sheet (timestamp-first, default padding +/-4s)
- `14:46.21` -> `You're gonna dine and dash.` -> play `14:42-14:50`.
- `14:59.96` -> `...run out on this check, it's gonna come out of our pocket.` -> play `14:56-15:06`.
- `15:41.13` -> `I talked to them the way that I would want to be talked to.` -> play `15:37-15:45`.
- `16:06.93` -> `...we'd like to cover their check.` -> play `16:03-16:11`.
- `19:45.74` -> `...but I guess I can wait.` -> play `19:42-19:50`.
- `19:59.96` -> `Looks like we'll be going for academic scholarships.` -> play `19:56-20:04`.

## Subtitle snippets (pre-extracted from sidecar LRC)
- Window `14:44-15:04`
  - `I know what you guys are doing here.`
  - `You're gonna dine and dash because you think it's fun and nobody gets hurt.`
  - `Look, if you guys run out on this check, it's gonna come out of our pocket.`
- Window `15:38-15:46`
  - `I took care of it.`
  - `I talked to them the way that I would want to be talked to, and they got it.`
  - `People are good.`
- Window `16:03-16:15`
  - `Excuse me, Mrs. Huang?`
  - `Um, we were just talking, and we'd like to cover their check.`
  - `...we want to chip in and pay their bill.`

## Fallback windows (same difficulty band)
- `D:\邬金平\初来乍到\3、初来乍到1-6季音频MP3\S01\S01E02.mp3` `03:35-04:05`
- `D:\邬金平\初来乍到\3、初来乍到1-6季音频MP3\S01\S01E02.mp3` `18:33-18:41`
- `D:\邬金平\绝望主妇\4  音频+LRC字幕\MP3\S01E03.mp3` `14:40-15:06`

## Correction guide
- Expected gist:
  - Main A: restaurant owner persuades potential dine-and-dash table by appealing to family impact.
  - Main B: staff volunteers to pay for the missing check.
- Target chunks:
  - `dine and dash`
  - `run out on this check`
  - `come out of our pocket`
  - `cover their check`
  - `chip in`
- Likely errors -> repair:
  - `run out` heard as `round out` -> force minimal pair with pause after `run`.
  - `cover their check` missed -> replay only `16:03-16:11` at `0.9x`.
  - long sentence collapse at sprint -> text anchor first, then no-sub replay.
