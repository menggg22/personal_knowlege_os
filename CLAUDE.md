# CLAUDE.md

Personal Knowledge Operating System.

## Directory Layout

```
KNOWLEDGE/           — Topic-based: learnings, ideas, blogs, projects
  _new/              — Uncategorized (land here first, organize later)
  <topic>/           — Create topics as you go
JOURNAL/             — Temporal: monthly logs + review distillations
  2026/MM-mmm.md     — Monthly rolling log (append-only)
  reviews/           — Monthly review outputs
PUBLISHED/           — Shipped writing
FUN/                 — Play sessions and sparks
  sparks.md          — Quick idea capture
  sessions/          — Play session notes
```

## Naming Convention

The naming convention is the database. Skills search for these patterns.

- `learning-YYMMDD-description.md` — readings, study sessions
- `idea-YYMMDD-description.md` — innovation ideas
- `blog-description/` — blog drafts (folder with outline, drafts)
- `project-name/` — developed projects (folder with README.md)

## Skills

| Skill | What it does |
|-------|-------------|
| `/learn [URL]` | Capture a reading → discuss → file insights |
| `/journal log "<what>"` | Log a work session → JOURNAL/ |
| `/journal plan` | Weekly plan from current context |
| `/journal review` | End-of-week review with success criteria |
| `/monthly-review` | Synthesize the month, catch drift |
| `/learning-quarterly` | 3-month strategic review |
| `/write-blog` | Blog drafts → iterate → publish |
| `/innovate` | Idea management — evaluate, track, develop |
| `/play` | Playful exploration, no pressure |

## Rules

- Keep entries concise. The monthly review synthesizes; individual entries just capture.
- Each skill reads other skills' output. That's what makes it compound.
- The system works at any level of completeness. Use one skill or all of them.
