# Folder Structure

The vault uses a numbered PARA-derived structure optimised for AI assistance. Numbers ensure consistent sort order across all tools and operating systems.

## Top-Level Folders

```
vault/
  .claude/           ← Claude Code project config (commands, agents, hooks, settings)
  00_Daily/          ← daily notes (YYYY-MM-DD)
  10_Areas/          ← ongoing responsibilities (no end date)
  20_Projects/       ← active, time-bounded projects
  30_Knowledge/      ← evergreen notes, literature, research
  40_Career/         ← career notes, professional development
  50_Claude/         ← AI-generated artifacts (sessions, summaries, patterns, templates)
  _attachments/      ← images, PDFs, all non-markdown assets
```

## Folder Definitions

### `.claude/`
Claude Code configuration for the vault project.
- `commands/` — vault-specific slash commands
- `agents/` — sub-agent configs
- `hooks/` — PowerShell automation hooks
- `settings.json` — hook bindings and project settings
- `settings.local.json` — machine-local overrides (gitignored)

### `00_Daily/`
One note per day, named `YYYY-MM-DD.md`. Weekly review notes also live here.
- Do not create subfolders. Obsidian search handles date navigation.

### `10_Areas/`
An area has an **ongoing standard** to maintain — no end date.
- Examples: Health, Finances, Career, Learning, Relationships.
- One note per area: `health.md`, `finances.md`, etc.
- Projects that serve an area link back to it; they do not live inside it.

### `20_Projects/`
A project has a **defined outcome** and a **finish line**.
- One folder per project: `20_Projects/project-name/`.
- Each folder contains a main note (`project-name.md`) and sub-notes.
- When complete, move the folder to an archive (or add `status: archived` frontmatter).

### `30_Knowledge/`
Long-term reference and evergreen knowledge.
- Evergreen notes graduated from daily captures or inbox.
- Literature notes (books, articles, research).
- Research MOCs and how-to references.
- Subfolders by domain are allowed: `30_Knowledge/neuroscience/`, `30_Knowledge/writing/`.

### `40_Career/`
Career-specific notes, separated for focus.
- Job search notes, interview prep, professional development, work reflections.
- Performance reviews, career goals, skill-building notes.

### `50_Claude/`
AI-generated artifacts. Information flows **out** of here into the vault, never in.
- `Sessions/` — structured logs from `/compress`. One file per session: `YYYY-MM-DD-session.md`.
- `Summaries/` — weekly and monthly rollups from `/review`.
- `Patterns/` — reusable prompts, frameworks, checklists distilled from sessions.
- `Templates/` — session, review, and distillation templates.

See `50_Claude/README.md` for the full conventions on what belongs here.

### `_attachments/`
All non-text assets. Configure Obsidian to default new attachments here.

## Notes at Vault Root

Keep the vault root clean. Acceptable files at root level:
- `CLAUDE.md` (Claude Code configuration)
- `README.md` or `Home.md` (vault entry point / dashboard)
- MOC notes that span multiple top-level folders

## Previous Structure Migration

If migrating from an older layout:
| Old folder | New location |
|---|---|
| `00-Inbox/` | Drop directly into `00_Daily/` or use the inbox in `30_Knowledge/` |
| `10-Daily/` | Rename to `00_Daily/` |
| `20-Projects/` | Rename to `20_Projects/` |
| `30-Areas/` | Rename to `10_Areas/` |
| `40-Resources/` | Rename to `30_Knowledge/` |
| `50-Archive/` | Add `status: archived` frontmatter instead, or keep as `_archive/` |
| `90-Templates/` | Move to `50_Claude/Templates/` (Claude templates) or Obsidian Templater folder |
