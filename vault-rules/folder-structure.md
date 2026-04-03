# Folder Structure

The vault uses a modified PARA (Projects, Areas, Resources, Archive) structure with explicit numbering for reliable sort order.

## Top-Level Folders

```
vault/
  00-Inbox/          ← raw, unprocessed captures (temporary home)
  10-Daily/          ← daily notes, indexed by date
  20-Projects/       ← active, time-bounded projects
  30-Areas/          ← ongoing responsibilities (no end date)
  40-Resources/      ← reference material, research, literature notes
  50-Archive/        ← completed, dormant, or deprecated notes
  90-Templates/      ← Obsidian Templater templates (never link to these)
  _attachments/      ← images, PDFs, all non-markdown assets
```

## Folder Definitions

### `00-Inbox/`
The capture landing zone. Nothing lives here permanently.
- Every note here is **unprocessed** — no links required, minimal frontmatter.
- Run `/inbox-process` regularly to empty it.
- Target: empty inbox weekly.

### `10-Daily/`
One note per day, named `YYYY-MM-DD.md`. Weekly review notes also live here.
- Do not create subfolders (e.g., by month). Obsidian search handles this.

### `20-Projects/`
A project has a **defined outcome** and a **finish line**.
- One folder per project: `20-Projects/project-name/`.
- Each project folder contains: a main project note (`project-name.md`) and any sub-notes.
- When a project is complete, move the folder to `50-Archive/`.

### `30-Areas/`
An area has an **ongoing standard** to maintain — no end date.
- Examples: Health, Finances, Career, Learning, Relationships.
- One note per area at the root level: `30-Areas/health.md`.
- Projects that serve an area link back to it; they do not live inside it.

### `40-Resources/`
Reference material you want to keep regardless of active projects.
- Subfolders by domain are allowed: `40-Resources/neuroscience/`, `40-Resources/writing/`.
- Literature notes, research MOCs, and how-to references live here.

### `50-Archive/`
Anything no longer active but worth keeping.
- Do not edit archived notes.
- If an archived project becomes active again, move it back to `20-Projects/`.

### `90-Templates/`
Template files for Obsidian Templater.
- Never link to template files from regular notes.
- Keep in sync with `templates/` folder in this kit.

### `_attachments/`
All non-text assets. Obsidian settings should point attachment default here.

## Notes at Vault Root

Keep the vault root clean. The only acceptable files at root level:
- `README.md` or `Home.md` (vault entry point / dashboard)
- `MOC` notes that span multiple top-level folders
