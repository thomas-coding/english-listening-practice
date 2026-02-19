# Benchmark Mini-Set Picks (Pass #17)

## Purpose
- Prepare a stable first benchmark mini-set using real lesson evidence from `L0001-L0003`.
- Keep one task per layer (controlled / bridge / authentic) with explicit fallbacks.

## Evidence used for selection
- Current weak tags: `opening_segment_decode_gap`, `audio_only_decode_lag`, `fixed_expression_gap`.
- Current strength trend: fixed expressions improve after short repair loops.
- Constraint: YouTube access may be unstable; local fallback is required.

## Selection rules
1. Controlled task must be easy enough to verify no-sub decode baseline.
2. Bridge task must use sitcom turn-taking but avoid overfamiliar windows.
3. Authentic task keeps YouTube first, with one local proxy fallback when network is unavailable.
4. All clips use first-pass no-sub + one repair replay, aligned with KPI scoring.

## Mini-set v1 picks

### Task C1 (Controlled layer)
- Primary: `englishpod 0023 (Making an Appointment)` | window `00:35-01:45` (~70s) | tier `E1`.
- Fallback: `daily 0012 (Small Talk About the Weather)` | window `00:40-01:50` (~70s) | tier `D1`.
- Why: checks whether core gist and service-intent details can be captured without visual cues.

### Task B1 (Bridge layer)
- Primary: `FOTB S01E02` | window `03:00-04:20` (from `fotb_s01e02_a`) | ~80s.
- Fallback: `FOTB S01E01` | window `14:00-15:20` (from `fotb_s01e01_b`) | ~80s.
- Why: evaluates multi-speaker sitcom decoding on a less-rehearsed segment.

### Task A1 (Authentic layer)
- Primary (online): `yt_017` (`https://www.youtube.com/watch?v=uDVoZ39mONk`) | window `01:15-03:05` (~110s).
- Fallback (online): `yt_019` (`https://www.youtube.com/watch?v=dzA7nL6cicY`) | window `00:50-02:30` (~100s).
- Fallback (offline proxy): `DH S01E03` | window `14:00-15:20` (from `dh_s01e03_b`) | tag `authentic_proxy_local`.
- Why: keeps authentic intent while guaranteeing executable flow if network is unstable.

## Scoring focus by task
- C1: `gist + detail precision` (controlled decode baseline).
- B1: `opening turn decode + scene binding` (bridge bottleneck check).
- A1: `no-sub robustness + recap coherence` (transfer readiness probe).

## Pass #17 outcome
- Benchmark mini-set picks are now ready for first run after lesson #4.
- Pipeline can proceed even with intermittent YouTube access.
