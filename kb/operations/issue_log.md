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
