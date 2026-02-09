# YouTube Channel/Topic Ladder (Seed v1)

## Purpose
- Build a controllable bridge from semi-authentic materials to normal-speed YouTube comprehension.
- Keep YouTube training aligned with stage-gate control, not random browsing.

## Gating before ladder entry
- Enter regular YouTube mixed-mode only when:
  - 7-lesson moving average >= 74
  - short no-sub gist stability >= 55%
- Enter no-sub-primary YouTube mode only when:
  - 7-lesson moving average >= 78
  - no-sub robustness >= 65

## Ladder levels
- Y1 (controlled authenticity): 3-5 minute clips, single speaker or clean dialogue, strong subtitle support.
- Y2 (bridge): 4-7 minute clips, moderate turn-taking, common daily/work topics.
- Y3 (normal pace): 6-10 minute clips, denser argument structure and faster delivery.
- Y4 (robustness): 8-12 minute unscripted interviews/discussions with minimal support.

## Topic ladder
1. Daily routine and productivity.
2. Work and communication habits.
3. Lifestyle explainers and social commentary.
4. Multi-speaker interviews and opinion content.

## Candidate source types (examples)
- Y1: learning-oriented channels and clear explainers (for stable caption quality).
- Y2: practical lifestyle/how-to explainers with moderate speed.
- Y3: mainstream explainer channels (business, society, tech basics).
- Y4: interview/podcast-style clips with natural turn-taking.

## Selection constraints (hard rules)
- Audio clarity must be good (no heavy background music/noise).
- Speaker count <= 2 for Y1-Y2.
- Avoid topic-heavy jargon in first two levels.
- Keep first pass no subtitles; subtitles only for repair pass.

## Query packs for `find_youtube.py`
- Y1 queries:
  - `english listening daily routine slow clear`
  - `english conversation workplace basic clear audio`
- Y2 queries:
  - `english lifestyle tips clear explanation`
  - `english communication skills short video`
- Y3 queries:
  - `english explainer social issue 8 minutes`
  - `english business explainer clear narration`
- Y4 queries:
  - `english interview full conversation natural speed`
  - `english discussion podcast clip 10 minutes`

## Execution template (per clip)
1. First pass: no subtitles, no pause.
2. Repair pass: one hotspot segment with subtitles.
3. Output: one-sentence gist + 3 details + 45-90 second recap.
4. Log: top confusion type and 5 reusable chunks.

## Fallback protocol
- If two consecutive YouTube clips fail gist threshold:
  - step down one ladder level,
  - use shorter clip (<=5 minutes),
  - run one controlled-source recovery lesson before retry.
