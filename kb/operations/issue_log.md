# Issue Log

## Format
- Date:
- Issue:
- Impact:
- Workaround:
- Permanent fix:
- Status:

## Current issues

### 2026-02-09
- Issue: `mpv` not in PATH (but binary exists).
- Impact: direct `mpv` command may fail in some shells.
- Workaround: use media-playback skill script (`play_media.py`) which resolves Scoop mpv path.
- Permanent fix: optional PATH cleanup or keep script-based playback.
- Status: mitigated.

### 2026-02-09
- Issue: `find_youtube.py` may show yt-dlp warnings (JS challenge / ffmpeg in PATH hints).
- Impact: noisy output; occasional metadata quality degradation risk.
- Workaround: proceed with selected URL when returned; use direct `play_media.py` on known URLs.
- Permanent fix: tune yt-dlp runtime/config if warnings become blocking.
- Status: open.

### 2026-02-09
- Issue: `find_youtube.py` can hit terminal encoding errors on GBK when titles include special symbols.
- Impact: query command may crash before printing selected result.
- Workaround: run with `python -X utf8`.
- Permanent fix: enforce UTF-8 output mode in script wrapper.
- Status: mitigated.

### 2026-02-09
- Issue: selected YouTube candidate may exceed requested duration bounds in some queries.
- Impact: out-of-range clips can enter candidate list if not manually checked.
- Workaround: manual validation against ladder duration constraints and reject outliers.
- Permanent fix: tighten post-filter logic in `find_youtube.py` workflow.
- Status: open.

### 2026-02-18
- Issue: YouTube accessibility can be unstable during benchmark or lesson delivery.
- Impact: authentic-layer task may fail even when local pipeline is healthy.
- Workaround: use `authentic_proxy_local` fallback from benchmark picks file to keep pipeline test executable.
- Permanent fix: keep YouTube as primary target but maintain dual-path benchmark routing (online primary + local proxy fallback).
- Status: mitigated.

### 2026-02-19
- Issue: Very short repair clips can cut off target sentence endings.
- Impact: learner may miss key phrase even with subtitles and report false comprehension failure.
- Workaround: add +3 to +5 seconds tail buffer for repair replay windows.
- Permanent fix: standardize repair slice rule (`target sentence end + 4s`) in lesson assembly routine.
- Status: mitigated.

### 2026-02-20
- Issue: Requested English subtitle playback can occasionally display Chinese subtitles in some MKV files.
- Impact: repair tasks may become easier than intended and bias benchmark consistency.
- Workaround: when subtitle track is unreliable, switch repair mode to audio-only + explicit text anchors.
- Permanent fix: add subtitle-stream verification step before playback and lock English track index.
- Status: open.

### 2026-02-20
- Issue: Learner-line waiting can become too long if backend writeback/prep runs inline during live interaction.
- Impact: breaks learning continuity and increases cognitive drop-off.
- Workaround: enforce dual-track runtime; defer heavy tasks to teacher line.
- Permanent fix: prebuild next 2-3 lessons and keep learner-line latency contract active.
- Status: mitigated.

### 2026-02-26
- Issue: `extract_segment_subtitles.py` in `auto` mode may rely on Whisper for local MP3 and skip sidecar `.lrc`, producing noisy prep snippets.
- Impact: target-sentence anchors can drift, increasing repair mis-cut risk.
- Workaround: teacher line pre-extracts snippets from sidecar `.lrc` and writes them into lesson package files.
- Permanent fix: update extractor to prioritize sidecar `.lrc/.srt` before Whisper in `auto` mode.
- Status: open.
