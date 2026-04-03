# Hook: Post Note Create

**Trigger:** Immediately after any new note is created in the vault.

**Purpose:** Ensure every new note is born well-formed — with frontmatter, at least one tag, and a connection attempt.

## Actions

1. **Frontmatter check**
   - Verify the note has `created`, `type`, and `tags` fields.
   - If any are missing, fill them in automatically:
     - `created`: current date in `YYYY-MM-DD` format
     - `type`: infer from folder (`10-Daily` → `daily`, `20-Projects` → `project`, `40-Resources` → `literature`, `00-Inbox` → `idea`, etc.)
     - `tags`: suggest 1–2 tags based on content and wait for confirmation

2. **Orphan prevention**
   - Run a lightweight connection scan (see `agents/connector.md`).
   - Suggest the single most relevant `[[wikilink]]` to add.
   - If no connection is found, add a `#orphan` tag as a reminder to revisit.

3. **Title validation**
   - Warn if the filename uses spaces (prefer hyphens), uppercase (prefer lowercase), or special characters.
   - Suggest a corrected slug if needed.

4. **Inbox routing**
   - If the note was created outside `00-Inbox/` but has no template applied, ask whether to apply one.

## Configuration

```yaml
# Add to your Claude Code project settings or CLAUDE.md
hooks:
  post_note_create:
    enabled: true
    auto_fill_frontmatter: true
    suggest_links: true
    warn_on_bad_filename: true
```
