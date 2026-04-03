---
description: Surface conceptual connections between notes across the vault
---

Analyse the note or concept I specify and find meaningful connections to other notes in the vault.

Steps:
1. Read the source note (or the concept I describe).
2. Identify the 3–5 most meaningful conceptual links — not just keyword matches, but genuine idea overlaps, contrasts, or progressions.
3. For each connection, explain *why* the link is meaningful in one sentence.
4. Suggest the exact `[[wikilink]]` syntax to add to the source note.
5. Check whether the linked notes should also link back (bidirectional links) and suggest those additions.
6. If a cluster of 3+ notes share a strong theme, suggest creating a **Map of Content (MOC)** note that sits above them.
7. Output a connection map in this format:

```
## Connections for [[note-title]]

### Strong Links
- [[linked-note-1]] — reason for link
- [[linked-note-2]] — reason for link

### Tangential Links
- [[linked-note-3]] — reason for link

### Suggested MOC
- Consider creating [[topic-moc]] to tie together: note-1, note-2, note-3
```

Never fabricate note titles. Only reference notes I have confirmed exist or that I create during this session.
