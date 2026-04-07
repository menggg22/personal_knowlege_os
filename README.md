# Personal Knowledge Operating System

A personal knowledge operating system powered by LLM. It ingests what you learn, synthesizes patterns over time, plans your week, and surprises you with what you can build.

## How It Works

The OS has two components: a **file structure** where knowledge lives, and **skills** — reusable LLM workflows that read and write that structure.

Together they form a loop:

```
  ┌──────────────────────────────────────────────────────────┐
  │                                                          ↓
Ingest                Synthesize             Act             Compound
/learn                /monthly-review        /journal plan   actions create
/innovate add         /write-blog            /journal review new knowledge
/journal log          /learning-quarterly    /innovate work  → back to Ingest
                                             /play
  │                         │                    │               │
  ↓                         ↓                    ↓               ↓
KNOWLEDGE/            JOURNAL/reviews/       JOURNAL/         KNOWLEDGE/
  learning-*          PUBLISHED/             FUN/sparks       new learning-*
  idea-*                                                      new project-*/
```

- **Ingest**: `/learn` a paper, `/innovate` an idea — knowledge enters the system
- **Synthesize**: `/monthly-review` finds patterns, `/write-blog` compresses insights
- **Act**: `/journal plan` generates your weekly plan, `/play` sparks creative exploration
- **Compound**: Actions generate new knowledge — the loop repeats

## Quick Start

```bash
git clone https://github.com/menggg22/personal_knowlege_os.git
cd personal_knowlege_os
```

Works with [Claude Code](https://docs.anthropic.com/en/docs/claude-code) or any LLM CLI that reads `CLAUDE.md`.

### Try it

```bash
# Capture a learning
/learn https://some-interesting-article.com

# Plan your week
/journal plan

# Explore something fun
/play
```

## Structure

```
KNOWLEDGE/                  # Topic-based knowledge
  _new/                     # Uncategorized (start here)
  example-topic/            # Create topics as you go
    learning-YYMMDD-*.md    # Readings and study notes
    idea-YYMMDD-*.md        # Innovation ideas
    blog-YYMMDD-*/          # Blog drafts
    project-*/              # Built things

JOURNAL/                    # Temporal structure
  2026/
    01-jan.md               # Monthly rolling log
  reviews/
    jan-2026.md             # Monthly review distillation

PUBLISHED/                  # Shipped writing

FUN/                        # Play sessions
  sparks.md                 # Quick idea capture
  sessions/                 # Play session notes

.claude/skills/             # The skills (LLM workflows)
CLAUDE.md                   # System instructions
```

### Naming Convention

The naming convention IS the database. The LLM searches for these patterns — no index needed.

- `learning-*` — readings, study sessions
- `idea-*` — innovation ideas
- `blog-*` — writing drafts
- `project-*` — developed projects

## Skills

| Skill | Phase | What it does |
|-------|-------|-------------|
| `/learn` | Ingest | Read an article, discuss it, file insights into the right topic |
| `/innovate` | Ingest | Evaluate an idea — feasibility, effort, market fit. Debate it. |
| `/journal log` | Ingest | Quick capture of a work session |
| `/monthly-review` | Synthesize | Read the month's data, find patterns, catch drift |
| `/write-blog` | Synthesize | Draft → iterate → feedback → publish |
| `/learning-quarterly` | Synthesize | 3-month strategic review — trajectory, alignment, correction |
| `/journal plan` | Act | Weekly plan from projects + learning gaps + last week's review |
| `/journal review` | Act | End-of-week review with git data + success criteria check |
| `/innovate work` | Act | Load project context, pick up where you left off |
| `/play` | Act → Compound | Random exploration — connect unrelated topics, follow curiosity |

### How skills connect

Skills read each other's output. That's what makes it an OS, not a collection of tools.

```
/learn → writes to KNOWLEDGE/
                ↓
/journal plan → reads KNOWLEDGE/ + JOURNAL/ → writes weekly plan
                ↓
/journal review → reads plan + git data → writes review
                ↓
/monthly-review → reads all reviews → finds patterns → writes synthesis
                ↓
/learning-quarterly → reads monthly reviews → strategic direction
                ↓
/journal plan → reads quarterly direction → next week's plan
```

## Customize

This is a template. Make it yours:

1. **Add topics** — create folders in `KNOWLEDGE/` for what you care about
2. **Modify skills** — edit `.claude/skills/*/skill.md` to match your workflow
3. **Change the rhythm** — weekly reviews too frequent? Make them biweekly. No quarterly needed? Remove it.
4. **Add work separation** — use a git submodule for employer-specific content on work-restricted infrastructure

The system works at any level of completeness. Use one skill or all of them.

## Philosophy

- The LLM maintains the knowledge, not you
- Knowledge should drive action, not just retrieval
- Learning compounds through temporal reviews
- Work and play belong in one system
- The best ideas come from curiosity with a safety net

## Blog Post

Read the full story: [Personal Knowledge Operating System with LLM](link)

## License

MIT
