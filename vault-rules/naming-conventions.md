# Naming Conventions

Consistent filenames make the vault navigable, searchable, and portable across systems.

## File Names

- **Always lowercase.** No uppercase letters. `spaced-repetition.md`, not `Spaced-Repetition.md`.
- **Hyphens, not spaces.** `my-idea-about-sleep.md`, not `my idea about sleep.md`.
- **No special characters.** Avoid `/ \ : * ? " < > | # ^ [ ]` — these break links and sync tools.
- **No dates in filenames** (except daily notes). Dates belong in frontmatter `created` field, not in the title.
- **Exception — daily notes:** `YYYY-MM-DD.md` format exactly. Example: `2025-03-14.md`.
- **Exception — weekly reviews:** `YYYY-[W]WW-weekly-review.md`. Example: `2025-W11-weekly-review.md`.

## Title Style

File names should be **noun phrases** describing the core concept:
- ✅ `spaced-repetition-improves-long-term-recall`
- ✅ `focus-requires-friction-reduction`
- ❌ `my thoughts on spaced rep` (vague, personal)
- ❌ `2025-notes-about-learning` (date in name, vague)

## Folder Names

- Lowercase, hyphenated. Prefix with two-digit sort order: `20-Projects`, `40-Resources`.
- Do not create subfolders beyond one level deep inside `20-Projects` or `30-Areas`.
- Resource subfolders by domain are allowed: `40-Resources/neuroscience/`, `40-Resources/productivity/`.

## Frontmatter Required Fields

Every permanent note must have:
```yaml
created: YYYY-MM-DD
type: [daily | project | area | literature | idea | meeting | person | moc]
tags: [at-least-one-tag]
```
