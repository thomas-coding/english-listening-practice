# Prebuilt Lessons Queue (Local-First)

## Purpose
- Keep learner sessions smooth by preloading upcoming lesson assets.
- Use local materials first to avoid network instability.

## Per-lesson package checklist
- Clip manifest ready: review/main/repair/sprint windows with exact timestamps.
- Anchor sheet ready: target sentence timestamps plus default +/-4s context padding.
- Subtitle snippets ready: extracted text for each planned repair window.
- Fallback windows ready: at least 2 alternates in same difficulty band.
- Correction guide ready: expected gist, target chunks, likely confusion points.

## Delivery history (completed)
- Lesson #5: completed on 2026-02-26.
- Lesson #6: completed on 2026-02-26.

## Upcoming ready packages
- Lesson #7 (`ready`)
  - Objective: consolidate long-sentence decode and opening binding.
  - Package: `kb/operations/prebuilt_packages/lesson_0007_package.md`
  - Primary sources: `FOTB S01E02` + `DH S01E03` short reactivation.
- Lesson #8 (`ready`)
  - Objective: unfamiliar long-chain decoding in colloquial school/family lines.
  - Package: `kb/operations/prebuilt_packages/lesson_0008_package.md`
  - Primary source: `FOTB S01E05`.
- Lesson #9 (`ready`)
  - Objective: S1->S2 bridge with DH social binding and idiom decoding.
  - Package: `kb/operations/prebuilt_packages/lesson_0009_package.md`
  - Primary source: `DH S01E04` with `DH S01E03` quick review.

## Usage rule
- Learner line should consume this queue first.
- If learner state is `low`, reduce each window to 20-45 seconds and increase repair density.
- During learner line, avoid rebuilding package assets unless required to unblock the current turn.
- Missing assets discovered in class must be logged and backfilled in teacher line before next lesson.
