# Daily First-30 Progression Map (Seed v1)

## Scope
- Purpose: expand Daily mapping from first 10 lessons to a first-30 progression pool.
- Source: `D:\邬金平\pod\daily`.
- Data note: durations for episodes `0001-0030` were validated via `ffprobe`.

## Tag schema
- Topic tags: `routine`, `commute`, `work`, `service`, `social`, `media`, `finance`, `health`, `travel`, `culture`, `negotiation`, `formal`.
- Tier tags:
  - `D1`: concrete daily-life content, lower inference load.
  - `D2`: mixed daily/workplace content, moderate inference load.
  - `D3`: abstract/workplace judgement or denser reasoning.

## Episode tags (0001-0030)
- `0001` (21.6m) | D1 | `social` | Introducing Yourself.
- `0002` (22.0m) | D1 | `routine` | Getting Up.
- `0003` (24.7m) | D2 | `routine` | Cleaning Up.
- `0004` (23.5m) | D2 | `routine` | Eating Breakfast.
- `0005` (19.6m) | D1 | `routine`,`work` | Getting Dressed & Ready for Work.
- `0006` (23.0m) | D2 | `commute`,`work` | The Commute to Work.
- `0007` (22.0m) | D2 | `work` | At My Desk, on Break, and at Lunch.
- `0008` (21.6m) | D2 | `commute`,`service` | Commute Home and Running Errands.
- `0009` (21.3m) | D1 | `routine` | Making Dinner, Eating Dinner.
- `0010` (17.8m) | D1 | `routine`,`media` | Relaxing, Reading the Mail, and the Trash.
- `0011` (20.2m) | D1 | `routine` | Getting Ready for Bed and Going to Sleep.
- `0012` (17.3m) | D1 | `social` | Small Talk About the Weather.
- `0013` (22.9m) | D2 | `service`,`health` | Going to the Drugstore.
- `0014` (20.8m) | D1 | `service` | Going to the Post Office.
- `0015` (19.2m) | D2 | `work` | Problems at the Office.
- `0016` (19.5m) | D2 | `commute`,`travel` | Driving on the Freeways.
- `0017` (18.4m) | D1 | `media` | Reading the Newspaper.
- `0018` (17.2m) | D1 | `social` | Seeing Old Friends.
- `0019` (22.0m) | D3 | `work`,`negotiation` | Tough Negotiations.
- `0020` (16.5m) | D3 | `work`,`formal` | Formal Emails.
- `0021` (17.3m) | D2 | `work` | Getting an Interview.
- `0022` (15.4m) | D2 | `work`,`social` | Making a Good Impression.
- `0023` (25.3m) | D3 | `health`,`service` | A Visit to the Doctor.
- `0024` (22.0m) | D3 | `work`,`social` | Taking Credit.
- `0025` (21.3m) | D2 | `travel` | A Trip to New York City.
- `0026` (21.0m) | D2 | `culture`,`social` | At the Movies.
- `0027` (20.7m) | D2 | `service`,`travel` | Car Trouble.
- `0028` (16.2m) | D2 | `finance`,`service` | Cashing a Check.
- `0029` (18.3m) | D1 | `routine`,`social` | Staying In.
- `0030` (17.4m) | D2 | `culture`,`social` | At the Art Exhibit.

## Suggested lesson expansion after first 10 lessons
- L11-L16: prioritize D1 reinforcement with occasional D2 probes.
- L17-L24: run D2 as core and insert one D1 recovery slot every 3 lessons.
- L25-L30: introduce D3 once no-sub gist remains stable for 2 consecutive lessons.

## Control rules
- If two consecutive lessons fail gist on D2, temporarily return to D1 for one recovery lesson.
- For episodes longer than 22 minutes, keep first-pass clip <= 120 seconds.
- Keep one reusable chunk list per lesson and recycle in the next 2 lessons.
