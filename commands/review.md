---
description: Run a weekly or monthly review of the vault — surface, close, and synthesise
---

Guide me through a structured review of my second brain. Default to weekly; I can say "monthly" to expand scope.

## Weekly Review Workflow

### 1. Inbox Triage (run `/inbox-process` inline)
- List all files in `00-Inbox/`.
- For each, recommend: **keep as-is**, **process into a permanent note**, **archive**, or **delete**.
- Wait for my confirmation on each.

### 2. Daily Notes Review
- Summarise key themes from this week's daily notes (`10-Daily/`).
- Extract any uncompleted tasks (lines with `- [ ]`).
- Surface any ideas logged in the log sections that weren't captured as atomic notes.

### 3. Projects Check
- List all notes in `20-Projects/` and their `status` frontmatter field.
- Flag any project that hasn't been touched in 7+ days as **stalled**.
- Suggest closing, archiving, or re-scoping stalled projects.

### 4. Idea Connections
- Pick 3 recently added notes from `00-Inbox/` or `40-Resources/`.
- Run a mini connection analysis (like `/connect`) for each.
- Suggest the top link to add.

### 5. Weekly Synthesis
- Write a short (3–5 sentence) narrative summary of the week: what was learned, what moved forward, what's emerging.
- Save it as `10-Daily/[week-ending-date]-weekly-review.md`.

## Monthly Add-ons
- Review `30-Areas/` for any area that needs a new note, project, or archive.
- Check `50-Archive/` — nothing should be in both archive and active folders.
- Suggest one new MOC or structure note based on themes that have emerged.
