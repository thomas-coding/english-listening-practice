# YouTube Clip Validation (Pass #14)

## Scope
- Objective: expand validated YouTube pool from 10 to 30 clips with Y1-Y4 balance.
- Inputs: query packs from `kb/materials/youtube_channel_ladder.md` + duration windows per level.
- Tooling: `find_youtube.py` with `python -X utf8` and duration constraints.

## Validation method
1. Run query packs per level and tune `--target-duration` to diversify picks.
2. Keep clips matching level duration windows:
   - Y1: 180-300s
   - Y2: 240-420s
   - Y3: 360-600s
   - Y4: 480-720s
3. Mark `pass` when topic + duration are stable for lesson routing.
4. Mark `provisional_pass` when lexical density/topic abstraction may require guided repair.

## New validated candidates added (20)

### Y1 additions
- `yt_011` | `My Morning Routine | Slow English Listening Practice for Beginners (A2)` | 3:23 | `https://www.youtube.com/watch?v=bRysNHKSxDo` | `pass`.
- `yt_012` | `Business English Conversations | ESL Business Meeting Conversation` | 3:25 | `https://www.youtube.com/watch?v=z-8o9sp8YIA` | `pass`.
- `yt_013` | `A1 English Listening Practice - Language Learning` | 3:43 | `https://www.youtube.com/watch?v=erjMgola4fQ` | `pass`.
- `yt_014` | `A2 English Listening Practice - Travel` | 3:32 | `https://www.youtube.com/watch?v=gOMypAhVaXE` | `pass`.
- `yt_015` | `What do you do every day? Easy English Conversations Episode 4` | 4:57 | `https://www.youtube.com/watch?v=bq6GBbh3uhU` | `pass`.

### Y2 additions
- `yt_016` | `How the food you eat affects your brain - Mia Nacamulli` | 4:52 | `https://www.youtube.com/watch?v=xyQY8a-ng6g` | `provisional_pass` (concept density watch).
- `yt_017` | `The Easiest Way to Improve Your English Listening Skills` | 5:39 | `https://www.youtube.com/watch?v=uDVoZ39mONk` | `pass`.
- `yt_018` | `The 3-2-1 Speaking Trick That Forces You To Stop Rambling!` | 5:28 | `https://www.youtube.com/watch?v=5m-C5mwpmxU` | `pass`.
- `yt_019` | `English Conversation At the Office - Speaking English at Workplace` | 5:46 | `https://www.youtube.com/watch?v=dzA7nL6cicY` | `pass`.
- `yt_020` | `English Rewind - 6 Minute English: Self help` | 6:30 | `https://www.youtube.com/watch?v=5rlC_oUe3zo` | `pass`.

### Y3 additions
- `yt_021` | `CYBER SECURITY explained in 8 Minutes` | 8:08 | `https://www.youtube.com/watch?v=zYLkdT731x8` | `pass`.
- `yt_022` | `Love Explained in 9 Minutes` | 9:08 | `https://www.youtube.com/watch?v=_KOpLEcN2-g` | `pass`.
- `yt_023` | `Supply and Demand in 8 Minutes` | 7:51 | `https://www.youtube.com/watch?v=kIFBaaPJUO0` | `provisional_pass` (term density watch).
- `yt_024` | `Every Networking Concept Explained In 8 Minutes` | 8:03 | `https://www.youtube.com/watch?v=vtUHgkTKju0` | `provisional_pass`.
- `yt_025` | `Every Level of Intelligence Explained in 9 Minutes` | 9:19 | `https://www.youtube.com/watch?v=9_cC-zt5yhc` | `provisional_pass`.

### Y4 additions
- `yt_026` | `How I Learned To Speak Clearly (English is my 3rd Language!)` | 9:10 | `https://www.youtube.com/watch?v=BAJMNQXzrgg` | `pass`.
- `yt_027` | `Learn English Small Talk to use at Work and with Friends, Family and Strangers` | 8:52 | `https://www.youtube.com/watch?v=4zXys7i8Zrc` | `pass`.
- `yt_028` | `Why you can't understand native English speakers.` | 10:30 | `https://www.youtube.com/watch?v=5TBvIfvUTGs` | `pass`.
- `yt_029` | `The secrets of learning a new language | Lydia Machova | TED` | 10:46 | `https://www.youtube.com/watch?v=o_XVt5rdpFY` | `pass`.
- `yt_030` | `Social Media Corrupts Human Interactions | Jack Symonds | Part 1 of 6` | 11:00 | `https://www.youtube.com/watch?v=5hCq0V_edbY` | `provisional_pass`.

## Pass #14 outcome
- Pool size: `10 -> 30` validated entries.
- Level balance for new 20 clips: `Y1=5, Y2=5, Y3=5, Y4=5`.
- Aggregate status after expansion (all 30 entries): `pass/provisional_pass=29`, `reject=1`.

## Operational notes
- `find_youtube.py` still emits yt-dlp runtime warnings in this environment unless stderr is suppressed.
- For repeatability, use `python -X utf8` and fixed duration windows per level.
