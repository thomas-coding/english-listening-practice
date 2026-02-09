# User Intent Map

## Purpose
- Keep interactions stable and predictable across future sessions.

## Supported intents
- `我来学一课` -> run one 30-minute adaptive lesson.
- `你自己学下` -> run mentor self-learning pass and update KB.
- `复习一下` -> run review-only lesson from review queue.
- `做个测试` -> run quick benchmark check (short form).
- `总结进度` -> output current stage, KPIs, weaknesses, next step.

## Startup phrase (recommended)
- `加载导师知识库并进入教学模式`

## Expected assistant behavior
- Read bootstrap files first.
- Confirm current stage and pick lesson objective.
- Execute playback with script-based operations.
- End with scoring + data updates.
