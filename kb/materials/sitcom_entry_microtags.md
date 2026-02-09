# Sitcom Entry Micro-Tags (v1.1)

## Purpose
- Speed up lesson assembly by mapping entry-safe episodes to reusable micro-tags.
- Unify selection across `初来乍到`, `绝望主妇`, and `burgers`.

## Tag schema
- `scene_type`: `family`, `work`, `school`, `service`, `conflict`, `social`.
- `speech_density`: `L` (low), `M` (medium), `H` (high).
- `speed`: `L` (slow), `M` (moderate), `H` (fast).
- `subtitle_reliability`: `R1` (full), `R2` (partial), `R3` (none).
- `recommended_state`: `low` / `normal` / `high`.
- `target_stage`: `S1` or `S2`.
- `start_end`: clip timestamp in `MM:SS-MM:SS` for lesson slicing.
- `clip_id`: stable identifier for logging and review queue links.

## Starter tagged entries

### Fresh Off the Boat (Tier A/B preferred)
- `S01E01` | `scene_type=family,school` | `speech_density=M` | `speed=M` | `subtitle_reliability=R1` | `recommended_state=normal` | `target_stage=S1`.
- `S01E02` | `scene_type=family,school` | `speech_density=M` | `speed=M` | `subtitle_reliability=R1` | `recommended_state=normal` | `target_stage=S1`.
- `S01E05` | `scene_type=family,social` | `speech_density=M` | `speed=M` | `subtitle_reliability=R1` | `recommended_state=normal` | `target_stage=S1`.
- `S02E01` | `scene_type=family,travel` | `speech_density=M` | `speed=M` | `subtitle_reliability=R1` | `recommended_state=high` | `target_stage=S1`.

### Desperate Housewives (S01-S02 entry)
- `S01E01` | `scene_type=family,social` | `speech_density=H` | `speed=M` | `subtitle_reliability=R1` | `recommended_state=normal` | `target_stage=S2`.
- `S01E02` | `scene_type=conflict,social` | `speech_density=H` | `speed=M` | `subtitle_reliability=R1` | `recommended_state=high` | `target_stage=S2`.
- `S01E03` | `scene_type=family,conflict` | `speech_density=H` | `speed=M` | `subtitle_reliability=R1` | `recommended_state=high` | `target_stage=S2`.
- `S01E04` | `scene_type=family,social` | `speech_density=M` | `speed=M` | `subtitle_reliability=R1` | `recommended_state=normal` | `target_stage=S2`.

### Bob's Burgers (subtitle-safe seasons)
- `S06E01` | `scene_type=family,work` | `speech_density=M` | `speed=M` | `subtitle_reliability=R1` | `recommended_state=normal` | `target_stage=S2`.
- `S06E02` | `scene_type=family,school` | `speech_density=M` | `speed=M` | `subtitle_reliability=R1` | `recommended_state=normal` | `target_stage=S2`.
- `S06E03` | `scene_type=family,conflict` | `speech_density=H` | `speed=M` | `subtitle_reliability=R1` | `recommended_state=high` | `target_stage=S2`.
- `S06E04` | `scene_type=family,work` | `speech_density=M` | `speed=H` | `subtitle_reliability=R1` | `recommended_state=high` | `target_stage=S2`.

## Pass #15 writeback: timestamp-level micro-tags (starter set)
- Method: subtitle-density scan on 90-second windows from episode subtitle files (`lrc/srt`) with overlap control.
- Note: these are routing-ready seed windows; scene-objective labels can be refined after first lesson evidence.

### Fresh Off the Boat clips (S1 bridge)
- `clip_id=fotb_s01e01_a` | `episode=S01E01` | `start_end=00:00-01:30` | `scene_type=family,school` | `speech_density=M` | `speed=M` | `subtitle_reliability=R1` | `recommended_state=normal` | `target_stage=S1`.
- `clip_id=fotb_s01e01_b` | `episode=S01E01` | `start_end=14:00-15:30` | `scene_type=family,school` | `speech_density=M` | `speed=M` | `subtitle_reliability=R1` | `recommended_state=normal` | `target_stage=S1`.
- `clip_id=fotb_s01e02_a` | `episode=S01E02` | `start_end=03:00-04:30` | `scene_type=family,school` | `speech_density=M` | `speed=M` | `subtitle_reliability=R1` | `recommended_state=normal` | `target_stage=S1`.
- `clip_id=fotb_s01e02_b` | `episode=S01E02` | `start_end=15:30-17:00` | `scene_type=family,school` | `speech_density=M` | `speed=M` | `subtitle_reliability=R1` | `recommended_state=normal` | `target_stage=S1`.
- `clip_id=fotb_s01e05_a` | `episode=S01E05` | `start_end=10:00-11:30` | `scene_type=family,social` | `speech_density=M` | `speed=M` | `subtitle_reliability=R1` | `recommended_state=normal` | `target_stage=S1`.
- `clip_id=fotb_s01e05_b` | `episode=S01E05` | `start_end=15:30-17:00` | `scene_type=family,social` | `speech_density=M` | `speed=M` | `subtitle_reliability=R1` | `recommended_state=normal` | `target_stage=S1`.
- `clip_id=fotb_s02e01_a` | `episode=S02E01` | `start_end=02:00-03:30` | `scene_type=family,travel` | `speech_density=M` | `speed=M` | `subtitle_reliability=R1` | `recommended_state=high` | `target_stage=S1`.
- `clip_id=fotb_s02e01_b` | `episode=S02E01` | `start_end=09:30-11:00` | `scene_type=family,travel` | `speech_density=M` | `speed=M` | `subtitle_reliability=R1` | `recommended_state=high` | `target_stage=S1`.

### Desperate Housewives clips (S2 transition)
- `clip_id=dh_s01e01_a` | `episode=S01E01` | `start_end=29:00-30:30` | `scene_type=family,social` | `speech_density=H` | `speed=M` | `subtitle_reliability=R1` | `recommended_state=normal` | `target_stage=S2`.
- `clip_id=dh_s01e01_b` | `episode=S01E01` | `start_end=39:30-41:00` | `scene_type=family,social` | `speech_density=H` | `speed=M` | `subtitle_reliability=R1` | `recommended_state=normal` | `target_stage=S2`.
- `clip_id=dh_s01e02_a` | `episode=S01E02` | `start_end=05:00-06:30` | `scene_type=conflict,social` | `speech_density=H` | `speed=M` | `subtitle_reliability=R1` | `recommended_state=high` | `target_stage=S2`.
- `clip_id=dh_s01e02_b` | `episode=S01E02` | `start_end=30:00-31:30` | `scene_type=conflict,social` | `speech_density=H` | `speed=M` | `subtitle_reliability=R1` | `recommended_state=high` | `target_stage=S2`.
- `clip_id=dh_s01e03_a` | `episode=S01E03` | `start_end=02:30-04:00` | `scene_type=family,conflict` | `speech_density=H` | `speed=M` | `subtitle_reliability=R1` | `recommended_state=high` | `target_stage=S2`.
- `clip_id=dh_s01e03_b` | `episode=S01E03` | `start_end=14:00-15:30` | `scene_type=family,conflict` | `speech_density=H` | `speed=M` | `subtitle_reliability=R1` | `recommended_state=high` | `target_stage=S2`.
- `clip_id=dh_s01e04_a` | `episode=S01E04` | `start_end=06:30-08:00` | `scene_type=family,social` | `speech_density=M` | `speed=M` | `subtitle_reliability=R1` | `recommended_state=normal` | `target_stage=S2`.
- `clip_id=dh_s01e04_b` | `episode=S01E04` | `start_end=17:30-19:00` | `scene_type=family,social` | `speech_density=M` | `speed=M` | `subtitle_reliability=R1` | `recommended_state=normal` | `target_stage=S2`.

### Bob's Burgers clips (S2 colloquial bridge)
- `clip_id=burg_s06e01_a` | `episode=S06E01` | `start_end=03:30-05:00` | `scene_type=family,work` | `speech_density=M` | `speed=M` | `subtitle_reliability=R1` | `recommended_state=normal` | `target_stage=S2`.
- `clip_id=burg_s06e01_b` | `episode=S06E01` | `start_end=06:30-08:00` | `scene_type=family,work` | `speech_density=M` | `speed=M` | `subtitle_reliability=R1` | `recommended_state=normal` | `target_stage=S2`.
- `clip_id=burg_s06e02_a` | `episode=S06E02` | `start_end=00:00-01:30` | `scene_type=family,school` | `speech_density=M` | `speed=M` | `subtitle_reliability=R1` | `recommended_state=normal` | `target_stage=S2`.
- `clip_id=burg_s06e02_b` | `episode=S06E02` | `start_end=17:00-18:30` | `scene_type=family,school` | `speech_density=M` | `speed=M` | `subtitle_reliability=R1` | `recommended_state=normal` | `target_stage=S2`.
- `clip_id=burg_s06e03_a` | `episode=S06E03` | `start_end=04:00-05:30` | `scene_type=family,conflict` | `speech_density=H` | `speed=M` | `subtitle_reliability=R1` | `recommended_state=high` | `target_stage=S2`.
- `clip_id=burg_s06e03_b` | `episode=S06E03` | `start_end=07:30-09:00` | `scene_type=family,conflict` | `speech_density=H` | `speed=M` | `subtitle_reliability=R1` | `recommended_state=high` | `target_stage=S2`.
- `clip_id=burg_s06e04_a` | `episode=S06E04` | `start_end=00:00-01:30` | `scene_type=family,work` | `speech_density=M` | `speed=H` | `subtitle_reliability=R1` | `recommended_state=high` | `target_stage=S2`.
- `clip_id=burg_s06e04_b` | `episode=S06E04` | `start_end=04:00-05:30` | `scene_type=family,work` | `speech_density=M` | `speed=H` | `subtitle_reliability=R1` | `recommended_state=high` | `target_stage=S2`.

## Assembly rules
1. Select by `target_stage` first, then by `recommended_state`.
2. Avoid `R3` entries in subtitle-dependent repair lessons.
3. Use `start_end` slices directly for first-pass clips (60-150 seconds), one scene objective per clip.
4. When learner state is `low`, prefer `_a` clips before `_b` clips in the same episode.

## Follow-up
- Expand starter entries from 24 timestamped clips to 40 clips.
- Add semantic objective labels (for example, `apology`, `request`, `conflict-repair`) after first 3 real lessons.
