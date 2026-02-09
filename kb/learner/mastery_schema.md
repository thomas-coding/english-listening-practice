# Mastery Tracker Schema

## Vocabulary item schema
- `term`: string
- `source`: material id/path + timestamp or episode
- `status`: `unknown | learning | known`
- `last_seen`: date
- `next_review`: date
- `correct_streak`: integer
- `error_note`: optional string

## Chunk item schema
- `chunk`: string
- `function`: e.g. opinion, transition, refusal, softening
- `source`: material id/path + timestamp or episode
- `status`: `new | building | stable`
- `last_seen`: date
- `next_review`: date
- `usage_success_count`: integer

## Error pattern schema
- `pattern_id`: string
- `type`: e.g. linking_miss, weak_form_miss, vocab_gap, inference_gap
- `examples`: list
- `count_total`: integer
- `count_last_30d`: integer
- `last_seen`: date
- `priority`: `high | medium | low`
