---
description: Create or open today's daily journal note
---

Create or update today's daily note in `10-Daily/` using the daily note template.

Steps:
1. Determine today's date in `YYYY-MM-DD` format.
2. Check if `10-Daily/YYYY-MM-DD.md` already exists.
   - If it exists: load it and ask what I want to add (new entry, reflection, tasks).
   - If it does not: create it using `templates/daily-note.md`.
3. When creating fresh:
   - Pre-fill the date, day-of-week, and the `## Morning Intentions` section with a prompt: *"What is the one thing that would make today a success?"*
   - Pull in any incomplete tasks from yesterday's note (look for `- [ ]` items in the previous day's file).
   - Link back to yesterday's note with `[[YYYY-MM-DD]]`.
4. When I give free-form input (reflections, events, thoughts), append it to the `## Log` section with a timestamp prefix `HH:MM —`.
5. At end-of-day mode (if I say "close day" or "evening"), fill in `## Evening Review`: wins, energy level, one thing to carry forward.
6. Always save and confirm the note path.
