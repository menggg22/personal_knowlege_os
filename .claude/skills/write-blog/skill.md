# Write Blog

Draft, iterate, and publish blog posts.

## Usage

- `/write-blog` — show blog dashboard (drafts in progress, ideas)
- `/write-blog "topic"` — start a new draft

## Execution

### New Draft

1. Create folder: `KNOWLEDGE/<topic>/blog-YYMMDD-description/`
2. Start with `outline.md` — structure the argument
3. Iterate to `draft-v1.md`, `draft-v2.md`
4. When ready, move final version to `PUBLISHED/`

### Dashboard

Scan for `KNOWLEDGE/*/blog-*` across all topics. Show:
- Drafts in progress (have outline but no published version)
- Ideas (mentioned in sparks.md or idea files but no draft started)
- Published (in PUBLISHED/)
