# Pedagogy Notes (Living Document)

## Core framework
- Phase A: Controlled decoding (podcasts with transcripts).
- Phase B: Semi-authentic transition (sitcom audio + optional subtitles).
- Phase C: Authentic robustness (YouTube no-subtitle first-pass).

## Skill stack to build
1. Acoustic decoding (connected speech).
2. High-frequency spoken lexicon and chunks.
3. Pragmatic language (idioms/slang/discourse markers).
4. Real-time meaning integration under imperfect understanding.

## Typical bottleneck map
- If words look familiar but audio is unclear -> decoding training.
- If sentence is clear but meaning still vague -> chunk and discourse training.
- If short clips are fine but long clips collapse -> endurance and attention pacing.
- If scripted media is fine but YouTube fails -> authenticity gap bridging.

## Review principles
- Spaced recall for error patterns, not only vocabulary lists.
- Recycle material by function: comprehension, dictation, retell, no-sub pass.

## ESL listening expert loop (operationalized)
1. Diagnose bottleneck (decoding, lexical, integration, endurance, transfer).
2. Assign a minimal effective task (45-180 seconds) at the right difficulty.
3. Force retrieval output (gist/details/recap) before showing support text.
4. Run targeted repair (one confusion segment, one reason, one fix).
5. Log reusable chunks + error pattern for spaced return.

## Technique-to-problem map
- If learner misses function words or reductions -> micro-dictation on 10-20 second spans.
- If learner knows words but cannot parse meaning flow -> chunk segmentation + discourse markers.
- If learner collapses on long clips -> split into 2-4 minute blocks with recap checkpoints.
- If learner performs well on scripted content but fails on YouTube -> add accent/speed variability in mixed mode.

## Daily source usage note (seed phase)
- In first-10 lessons, use Daily as controlled precision training with short no-sub segments.
- Sequence principle: service/daily-life -> workplace/social judgement -> negotiation/formal register.

## EnglishPod triad usage note (seed phase)
- Treat `pb` as diagnostic input, `rv` as targeted repair, and `dg` as retrieval reinforcement.
- Keep segment-level focus; do not consume full `rv` unless the error hotspot truly needs it.

## Progression safety rule
- When moving from D1 to D2 material, require gist stability for 2 consecutive lessons.
- If two D2 lessons fail in a row, schedule one D1 recovery lesson before retrying D2.

## EnglishPod scaling rule
- For triad-total duration >22 minutes, cap first-pass PB segment to 120 seconds and route remaining time to output/retrieval.
- Use one explicit topic tag per lesson to keep cross-source transfer tracking consistent.

## YouTube transfer rule
- Select clip by ladder level first, then by topic relevance; never invert this order.
- If YouTube first-pass gist fails twice in a row, execute one controlled recovery lesson before next YouTube attempt.

## Benchmark routing rule
- For benchmark mini-set, keep YouTube as authentic primary but predefine one local proxy fallback.
- If network blocks YouTube execution, run local proxy for pipeline check and mark benchmark status as `pending_online_authentic`.

## YouTube pool routing rule
- Keep at least 5 validated candidates per ladder level (Y1-Y4) to avoid repeated exposure fatigue.
- In each level, route with a 3:1 mix of `pass` to `provisional_pass` clips so challenge stays controlled.

## Sitcom subtitle-reliability rule
- If subtitle reliability is low (R3), treat material as challenge mode only and shorten first-pass segment.
- Use high-reliability seasons first when building bridge confidence.

## Micro-tag assembly rule
- Select clips using `target_stage` and `recommended_state` before selecting by topic preference.
- Keep one dominant scene objective per clip to protect recap quality.

## Timestamp slice rule
- Use predefined `start_end` windows first to reduce setup overhead and cross-session variance.
- For `normal` state, start with `_a` windows; use `_b` windows as same-episode repair/follow-up.
- For repair replay, keep a tail buffer of 3-5 seconds after the target sentence to avoid truncating key line endings.

## Subtitle reliability fallback rule
- If requested English subtitles are not reliably rendered, switch repair to audio-only with explicit text anchors.
- Mark that segment as `subtitle_reliability_warning` in log/notes to protect benchmark comparability.

## Dual-track prebuild-first rule
- Teacher line should finish package assets (manifest, anchors, snippets, fallbacks, correction map) before learner line starts.
- Learner line only does minimal unblock operations; heavy extraction/prep should be backfilled in teacher line.

## Anti-memorization switching rule
- If learner reports "I remembered it, not heard it", immediately rotate to same-band unfamiliar fallback within the same lesson.
- Keep one known-line confidence check, then spend remaining time on unfamiliar decoding to protect transfer quality.
