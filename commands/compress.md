---
description: Write a structured session log to 50_Claude/Sessions/ so nothing is lost
---

Compress this session into a structured log and save it to `50_Claude/Sessions/`.

## Steps

1. Reflect on everything that happened in this Claude Code session:
   - What was worked on?
   - What decisions were made?
   - What was created, edited, or deleted?
   - What problems were encountered and how were they resolved?
   - What is still open or incomplete?

2. Write the session log using this structure:

```markdown
---
created: {{date:YYYY-MM-DD}}
session-start: {{approx time}}
type: session-log
tags: [session]
---

# Session Log — {{date}}

## Focus
(1-2 sentence summary: what was the main purpose of this session?)

## What Happened
(bullet list: concrete actions taken, in order)
- 
- 

## Decisions Made
(choices that affect future work)
- 

## State
(what is the current state of key things worked on this session — useful for /resume)
- [[note or project]]: current status

## Open Loops
(things started but not finished; questions raised but not answered)
- 

## Insights
(anything worth promoting to an evergreen note or preserving in CLAUDE.md)
- 

## Next Session Should Start With
(the first thing to pick up next time)
- 
```

3. Save to `50_Claude/Sessions/{{date}}-session.md`.
4. If there are insights worth preserving as rules, ask: *"Want to run `/preserve` for any of these?"*
5. Confirm: *"Session compressed to [[{{date}}-session]]."*
