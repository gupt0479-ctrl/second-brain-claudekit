# Hook: Auto-Link

**Trigger:** When a note is saved or when `/connect` is run.

**Purpose:** Continuously weave the knowledge graph by detecting and suggesting new connections as notes evolve.

## Actions

1. **Mention detection**
   - Scan the note content for any mentions of titles or key concepts from other notes (even without `[[]]` syntax).
   - For each detected mention, suggest converting it to a proper `[[wikilink]]`.
   - Example: if the note mentions "spaced repetition" and `[[spaced-repetition-strengthens-memory]]` exists, flag it.

2. **Backlink suggestion**
   - After adding a link `[[target-note]]`, check whether `target-note` should also link back.
   - If the relationship is bidirectional (most are), suggest adding the return link.

3. **MOC update**
   - If the note's tags or content match an existing MOC's scope, suggest adding the new note to that MOC's index.

4. **Orphan resolution**
   - Notes tagged `#orphan` are priority targets. On each vault save cycle, attempt to find one connection for each orphan note.
   - Remove `#orphan` once at least one link is established.

## Excluded Paths

The following paths are excluded from auto-link scanning:
- `00-Inbox/` (notes are unprocessed; linking happens at inbox-process time)
- `_attachments/`
- `90-Templates/`

## Configuration

```yaml
hooks:
  auto_link:
    enabled: true
    scan_on_save: true
    exclude_paths:
      - "00-Inbox"
      - "_attachments"
      - "90-Templates"
    backlink_suggestions: true
    moc_update_suggestions: true
```
