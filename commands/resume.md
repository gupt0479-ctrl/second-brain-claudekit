---
description: Restore useful context from session logs to pick up where you left off
---

Load the most relevant past session context so we can pick up without re-explaining everything.

## Steps

1. List the 5 most recent files in `50_Claude/Sessions/` (by date in filename).
2. Read the most recent session log. Extract:
   - `## State` — current status of key notes/projects
   - `## Open Loops` — unfinished threads
   - `## Next Session Should Start With` — explicit carry-forward

3. Also check `CLAUDE.md` for any rules updated recently (look for comments with recent dates).

4. Output a **Resume Brief**:

```
## Resume Brief — picking up from {{last-session-date}}

### Last Session Focus
(what was the main thread)

### State of Key Things
- [[note/project]]: status

### Open Loops to Address
1. (most important)
2.
3.

### Suggested Starting Point
(the thing the last session said to start with next time)
```

5. Ask: *"Want to start with the suggested starting point, or something else?"*

## Advanced: Multi-Session Resume

If I say *"resume from [N] sessions ago"* or *"summarise the last week"*, read all session logs in the date range and synthesise a combined brief covering key decisions, state, and open loops across all of them.
