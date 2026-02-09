# Playback Operations (OpenCode CLI, Windows)

## Current environment findings
- Media playback skill exists at:
  - `C:\Users\wujin\.config\opencode\skills\media-playback`
- Verified from that skill:
  - `play_media.py` available and working (dry-run validated).
  - `find_youtube.py` available and working (search validated).
  - `extract_segment_subtitles.py` available.
- Runtime availability:
  - `mpv` binary exists at `C:\Users\wujin\scoop\apps\mpv\current\mpv.exe`.
  - `yt_dlp` Python module is installed.
  - `ffmpeg/ffprobe` exist at `D:\software_package\ffmpeg-8.0.1-full_build\bin\`.

## Preferred approach (use skill scripts)
- Use the skill scripts directly instead of manual `start` commands.
- Script root:
  - `C:\Users\wujin\.config\opencode\skills\media-playback\scripts`

## Local file playback (default app)
- Command pattern:
- `cmd /c start "" "D:\\path\\to\\file.mp3"`
- `cmd /c start "" "D:\\path\\to\\file.mkv"`

## Local/YouTube playback (recommended)
- Local clip, no subtitles:
  - `python "C:\Users\wujin\.config\opencode\skills\media-playback\scripts\play_media.py" "D:\path\video.mkv" --start 240 --end 300 --subtitle off`
- Audio-only, slowed speed:
  - `python "C:\Users\wujin\.config\opencode\skills\media-playback\scripts\play_media.py" "D:\path\audio.mp3" --audio-only --start 480 --end 510 --speed 0.8 --subtitle off`
- YouTube with English subtitles:
  - `python "C:\Users\wujin\.config\opencode\skills\media-playback\scripts\play_media.py" "https://www.youtube.com/watch?v=VIDEO_ID" --subtitle english`
- YouTube search + optional play:
  - `python "C:\Users\wujin\.config\opencode\skills\media-playback\scripts\find_youtube.py" --query "daily life english listening" --target-duration 60 --min-duration 45 --max-duration 80 --play --subtitle off`

## Optional player setup (recommended for stable control)
- Install mpv via scoop:
- `scoop install mpv`
- Then playback command:
  - `mpv "D:\\path\\to\\file.mp3"`
  - `mpv "D:\\path\\to\\file.mkv" --sub-auto=fuzzy --speed=1.0`

## YouTube playback options
- Option A: open in browser directly via URL.
- Option B: use `yt-dlp` for controlled local playback/download workflow.

## Subtitle extraction helper (segment transcript)
- Command:
  - `python "C:\Users\wujin\.config\opencode\skills\media-playback\scripts\extract_segment_subtitles.py" "D:\path\media.mkv" --start 240 --end 300 --mode auto`
- Output:
  - relative timeline starts from `00:00` (segment-relative), good for dictation review.

## Teaching control patterns
- No-sub first pass: play once without subtitle overlays.
- Repair pass: replay selected 15-60 second chunk.
- Speed tuning: `--speed=0.9` (if needed), return to `1.0` as soon as possible.

## Known caveats
- `find_youtube.py` may print yt-dlp warnings about JS challenges/ffmpeg in PATH.
- Current behavior is still usable for search and playback; warnings are not always blocking.
