# Journal

Track your work with temporal structure.

## Usage

- `/journal log "<what>"` — log a work session
- `/journal plan` — generate weekly plan
- `/journal review` — end-of-week review

## Log Mode

Append to `JOURNAL/2026/MM-mmm.md` (create if needed):

```markdown
## YYYY-MM-DD (Day, ~Xh)
[What was worked on. Project name, what happened, insights.]
```

## Plan Mode

1. Read last week's review (if exists)
2. Read recent `JOURNAL/` entries
3. Scan `KNOWLEDGE/` for active projects and learning gaps
4. Ask user for priorities and context
5. Write weekly plan with:
   - What to focus on
   - Success criteria (checkboxes)
   - Time allocation

## Review Mode

1. Read this week's plan
2. Read `JOURNAL/` entries for the week
3. Check git log for activity: `git log --since="7 days ago" --oneline`
4. Ask user reflection questions:
   - What are you most proud of?
   - What didn't go as planned?
   - One thing you learned?
5. Write review with:
   - Accomplishments
   - Success criteria assessment
   - Patterns noticed
   - Next week recommendations
