# Lesson #8 Prebuilt Package (ready)

## Lesson intent
- State target: `normal` (can downshift to `low` with shorter windows).
- Objective: train unfamiliar long-sentence decoding in colloquial school/family context.
- Priority carry-over: `e_long_sentence_decode_gap`, `audio_only_decode_lag`.

## Clip manifest
- Review (4 min)
  - Source: `D:\邬金平\初来乍到\3、初来乍到1-6季音频MP3\S01\S01E02.mp3`
  - Window: `19:42-20:00`
  - Goal: keep `I guess I can wait` + `academic scholarships` active.
- Main A (10 min)
  - Source: `D:\邬金平\初来乍到\3、初来乍到1-6季音频MP3\S01\S01E05.mp3`
  - Window: `10:48-11:12`
  - Goal: conditional/offer sentence tracking in fast comedic lines.
- Main B (9 min)
  - Source: `D:\邬金平\初来乍到\3、初来乍到1-6季音频MP3\S01\S01E05.mp3`
  - Window: `14:38-15:00`
  - Goal: follow a 3-step information chain (`trace cause` -> `epidemic` -> `action plan`).
- Sprint (3 min)
  - Source: `D:\邬金平\初来乍到\3、初来乍到1-6季音频MP3\S01\S01E05.mp3`
  - Window: `17:01-17:24`
  - Goal: catch intention/constraint sentence under no-sub mode.

## Anchor sheet (timestamp-first, default padding +/-4s)
- `10:48.83` -> `The workplace is filled with inappropriate characters.` -> play `10:45-10:53`.
- `10:57.18` -> `If you select me on Friday night, I'll select you for the promotion.` -> play `10:53-11:01`.
- `14:38.08` -> `We traced this video back to your son.` -> play `14:34-14:42`.
- `14:42.09` -> `It's just a sexual harassment training video from my restaurant.` -> play `14:38-14:46`.
- `14:55.83` -> `We're planning a sex Ed assembly.` -> play `14:52-15:00`.
- `17:21.94` -> `Look, I don't want you to go out and have sex tomorrow.` -> play `17:18-17:26`.

## Subtitle snippets (pre-extracted from sidecar LRC)
- Window `10:53-11:08`
  - `Here we have the persistent Romeo.`
  - `If you select me on Friday night, I'll select you for the promotion.`
  - `How about Saturday? Sunday? Monday?`
- Window `14:38-14:59`
  - `We traced this video back to your son.`
  - `It's caused an epidemic.`
  - `It's just a sexual harassment training video from my restaurant.`
  - `We're planning a sex Ed assembly.`
  - `...have the talk with their sons.`
- Window `17:18-17:24`
  - `Look, I don't want you to go out and have sex tomorrow.`

## Fallback windows (same difficulty band)
- `D:\邬金平\初来乍到\3、初来乍到1-6季音频MP3\S01\S01E05.mp3` `11:48-12:13`
- `D:\邬金平\初来乍到\3、初来乍到1-6季音频MP3\S01\S01E05.mp3` `18:25-18:56`
- `D:\邬金平\初来乍到\3、初来乍到1-6季音频MP3\S01\S01E05.mp3` `19:43-19:59`

## Correction guide
- Expected gist:
  - Main A: workplace training video uses exaggerated characters and repeated pitch lines.
  - Main B: school staff traces problem source and asks parents to start sex-ed talk.
- Target chunks:
  - `inappropriate characters`
  - `select you for the promotion`
  - `traced this video back to your son`
  - `caused an epidemic`
  - `have the talk`
- Likely errors -> repair:
  - `select` heard as `sick/sex` -> isolate `select` in 2-second micro-repeat.
  - `epidemic` dropped -> force shadowing after text anchor once.
  - long chain collapse -> split into 2 clauses before full replay.
