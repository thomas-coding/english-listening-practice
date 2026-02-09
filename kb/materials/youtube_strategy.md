# YouTube Transfer Strategy (Draft)

## Position in learning pipeline
- Final transfer target, not day-1 primary corpus.
- Decision: must be included in mentor self-learning and curriculum design from now on, but exposure is staged.

## Pass #6 writeback (channel/topic ladder)
- A channel/topic ladder with gating, query packs, and fallback protocol is now defined in:
  - `kb/materials/youtube_channel_ladder.md`
- This closes the previous gap where YouTube guidance was principle-level but not operational.

## Pass #10 writeback (first 10 clip validation)
- First 10 candidate clips were validated and recorded in:
  - `kb/materials/youtube_clip_validation_pass10.md`
- Structured pool tracking is recorded in:
  - `kb/materials/youtube_validated_pool.json`
- Current outcome: 7 pass, 2 provisional-pass, 1 rejected by duration.

## Pass #14 writeback (pool expansion to 30)
- Additional 20 candidates were validated and recorded in:
  - `kb/materials/youtube_clip_validation_pass14.md`
- Pool tracking now shows:
  - validated_count: 30
  - accepted_count: 29
  - rejected_count: 1
- New additions are level-balanced (`Y1=5, Y2=5, Y3=5, Y4=5`) to support stable routing.

## Integration stages
1. Controlled intro: 3-5 minute clips with English subtitles.
2. Mixed mode: first pass no subtitles, second pass with subtitles.
3. No-sub primary: first pass no subtitles as default.

## Practical gating for this learner
- Before regular YouTube blocks, keep controlled and semi-authentic sources as core.
- Trigger to enter regular mixed YouTube blocks:
  - 7-lesson moving average >= 74
  - short no-sub gist stability >= 55%
- Trigger to enter no-sub-primary YouTube blocks:
  - 7-lesson moving average >= 78
  - no-sub robustness >= 65

## Success criteria by stage
- Stage 1: can summarize gist + 3 details.
- Stage 2: no-sub first pass gist is stable (>60%).
- Stage 3: 8-12 minute normal videos, no-sub first pass >70%.

## Candidate topic ladder (to be expanded)
1. Daily routines / productivity / lifestyle vlogs.
2. Light explainer channels (history, tech basics, social topics).
3. Interview/discussion clips with moderate turn-taking.
4. Faster opinion channels and denser authentic content.

## Open tasks
- Add accent-mix policy (US/UK/mixed) based on benchmark trends.
- Add per-clip quality tags (`accent`, `speaker_count`, `subtitle_reliability`) for faster lesson assembly.
