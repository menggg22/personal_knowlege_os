# Monthly Review

End-of-month synthesis. Read everything, find patterns, catch drift.

## Usage

- `/monthly-review` — run at end of month

## Execution

1. **Gather data**:
   - `JOURNAL/2026/MM-mmm.md` — this month's log entries
   - `KNOWLEDGE/*/learning-*` — learnings created this month
   - `KNOWLEDGE/*/blog-*` — blog activity
   - `KNOWLEDGE/*/project-*` — project progress
   - `PUBLISHED/` — anything shipped
   - `git log --since="[MONTH_START]" --until="[MONTH_END]"` — activity

2. **Ask user**:
   - What are you most proud of this month?
   - What didn't go as planned?
   - What surprised you?

3. **Write review** to `JOURNAL/reviews/MMM-YYYY.md`:
   - Summary (2-3 sentences — what defined this month)
   - What was built / shipped / learned
   - Patterns noticed ("You started 3 projects but finished 1")
   - Drift check ("Stated goal was X, actual focus was Y")
   - Next month recommendations
