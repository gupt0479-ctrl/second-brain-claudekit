# Hook: Daily Summary

**Trigger:** End of day (triggered manually with "close day" or "evening") OR start of a new day session.

**Purpose:** Automatically generate a summary of the day's activity in the vault and prime the next day.

## End-of-Day Actions

1. **Activity digest**
   - List all notes created or modified today, grouped by folder.
   - Highlight any notes that were promoted from inbox (significant progress signal).

2. **Task rollover**
   - Scan today's daily note for incomplete tasks (`- [ ]`).
   - Copy them to tomorrow's daily note under `## Carried Forward`.

3. **Evening review prompt**
   - Fill in the `## Evening Review` section of today's daily note with prompts:
     - "What was your biggest win today?"
     - "What drained your energy?"
     - "What one thing carries into tomorrow?"
   - Wait for my responses and save them to the note.

4. **Idea check**
   - If 3+ new ideas are sitting in `00-Inbox/` unprocessed, surface a reminder: *"You have N unprocessed ideas — want to run `/inbox-process`?"*

## Start-of-Day Actions

1. **Create today's daily note** (if not yet created) — automatically via `templates/daily-note.md`.
2. **Surface yesterday's carries** — show me the tasks and reflections I flagged from yesterday.
3. **Remind of stalled projects** — flag any `20-Projects/` note not touched in 7+ days.
4. **One question** — surface one open question from a recent note to prime thinking. Pick from notes tagged `#open-question`.

## Configuration

```yaml
hooks:
  daily_summary:
    enabled: true
    end_of_day_trigger: ["close day", "evening review", "wrap up"]
    start_of_day_trigger: ["good morning", "start day", "morning"]
    stale_project_threshold_days: 7
```
