# YouTube Clip Validation (Pass #10)

## Status
- Historical baseline run. Latest pool expansion is documented in `kb/materials/youtube_clip_validation_pass14.md`.

## Scope
- Objective: validate first 10 candidate clips against `kb/materials/youtube_channel_ladder.md`.
- Method: use `find_youtube.py` query packs and check duration/level fit first, then mark manual checks for audio clarity and speaker count.

## Validation results (10 candidates)
- 1) Target level `Y2` | `Simple Daily Routine English | Slow Listening & Speaking Practice for Beginners | Daily English` | 11:19 | `https://www.youtube.com/watch?v=ATc5ikVqank` | result: `provisional-pass` (topic fit, duration slightly above Y2 upper bound).
- 2) Target level `Y1` | `40 English Phrases You Need for Online Meetings` | 5:14 | `https://www.youtube.com/watch?v=PLhAzAymMsY` | result: `pass`.
- 3) Target level `Y3` | `A Simple Way to Break a Bad Habit | Judson Brewer | TED` | 9:25 | `https://www.youtube.com/watch?v=-moW9jvvMr4` | result: `pass`.
- 4) Target level `Y2` | `Top 5 Tips to Improve Communication Skills | Soft Skills For Beginners | Soft Skills | Simplilearn` | 5:55 | `https://www.youtube.com/watch?v=pJ7RgUCEd5M` | result: `pass`.
- 5) Target level `Y3` | `Every Political Ideology Explained in 8 Minutes` | 8:14 | `https://www.youtube.com/watch?v=9cz4ikFcwMY` | result: `provisional-pass` (topic density likely high).
- 6) Target level `Y3` | `Give me 9min, and I'll improve your storytelling skills by 176%` | 8:58 | `https://www.youtube.com/watch?v=hNuAv-42jzY` | result: `pass`.
- 7) Target level `Y4` | `REAL English Conversation | FAST English!` | 10:14 | `https://www.youtube.com/watch?v=jBUSWWM0JO4` | result: `pass`.
- 8) Target level `Y4` | `10 Minutes to Improve English Speaking Skills Efficiently | English Speaking Conversations` | 11:15 | `https://www.youtube.com/watch?v=aOLsQN98aI4` | result: `pass`.
- 9) Target level `Y2` | `Repeat-After-Me Speaking Practice with a fun little story` | 6:09 | `https://www.youtube.com/watch?v=6E7i_7Mr_5c` | result: `pass`.
- 10) Target level `Y4` | `English Listening Practice #1 - Real Native Conversation (B2-C1)` | 27:55 | `https://www.youtube.com/watch?v=6PJnEdbq8qc` | result: `fail` (duration far beyond Y4 range; reject for current ladder).

## Summary
- Pass: 7
- Provisional-pass: 2
- Fail: 1

## Decisions
- Keep clips #2/#3/#4/#6/#7/#8/#9 as candidate starter set.
- Keep #1 and #5 for conditional use (topic/pace check in live lesson).
- Reject #10 for now due excessive duration.

## Operational caveats observed
- `find_youtube.py` emits frequent yt-dlp JS runtime and ffmpeg warnings.
- One query path can raise console encoding issues on GBK terminals; `python -X utf8` avoids this.
