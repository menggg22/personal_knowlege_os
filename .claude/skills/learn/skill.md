# Learn

Capture and discuss a reading.

## Usage

- `/learn` — show learning dashboard (recent entries, topics)
- `/learn [URL]` — read an article, discuss it, file insights
- `/learn "topic"` — start or resume a deep learning series

## Execution

### URL Mode

1. Fetch and read the article
2. Summarize key insights (3-5 bullets)
3. Discuss with user — what's interesting? What connects to existing knowledge?
4. Determine topic folder (scan `KNOWLEDGE/` for best fit, or `_new/`)
5. Write `learning-YYMMDD-description.md` with:
   - Source URL
   - Key insights
   - Connections to existing knowledge
   - Open questions

### Dashboard Mode

Scan `KNOWLEDGE/*/learning-*` across all topics. Show:
- Recent learnings (last 2 weeks)
- Topics by depth (count entries per topic)
- Active deep studies (folders with multiple sessions)
