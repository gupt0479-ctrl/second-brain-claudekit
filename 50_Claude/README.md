# 50_Claude

AI-generated artifacts for this vault. Structured to make sessions searchable and reusable.

## Subfolders

| Folder | Contents |
|---|---|
| `Sessions/` | Structured logs from `/compress` or `/closeday`. One file per session. |
| `Summaries/` | Weekly and monthly rollups from `/review` and the `weekly-reviewer` agent. |
| `Patterns/` | Reusable prompts, frameworks, checklists, and mental models distilled from sessions. |
| `Templates/` | Session note templates, project review templates, idea distillation templates. |

## Naming Conventions

- Sessions: `YYYY-MM-DD-session.md`
- Edit logs: `YYYY-MM-DD-edits.md` (archived from `_today-edits.md`)
- Summaries: `YYYY-[W]WW-weekly-summary.md` or `YYYY-MM-monthly-summary.md`
- Patterns: descriptive slug, e.g. `idea-distillation-checklist.md`

## What Goes Here vs. Permanent Vault

| This folder | Permanent vault (`30_Knowledge/`, `10_Areas/`, etc.) |
|---|---|
| Raw session logs | Graduated evergreen notes |
| Weekly summaries | Project learnings promoted to project notes |
| Prompt drafts | Stable workflows that made it into `commands/` |
| Transient context | Durable rules that made it into `CLAUDE.md` |

Do not link from permanent notes into `50_Claude/`. The information flow is one-way: insights graduate **out** of here into the vault.
