# Linking Strategy

Links are the connective tissue of the second brain. A note without links is a dead note.

## Core Principle

**Link on concepts, not keywords.** Ask: *"Is this reference meaningful? Would following this link teach me something relevant to the current note?"* If yes, link. If it's just a word that happens to match, don't.

## When to Link

| Situation | Action |
|---|---|
| You mention a concept that has its own note | Add `[[note-slug]]` inline |
| You reference a person | Link to their `[[person-note]]` |
| You reference a project | Link to the `[[project-note]]` |
| A note raises a question another note answers | Link with a comment: `[[answering-note]] answers this` |
| You're building an argument from multiple notes | Create a MOC and link all of them to it |

## When NOT to Link

- Do not link common English words that happen to match note titles.
- Do not link the same note more than once per section (once per note is ideal).
- Do not create links just to increase link count.

## Bidirectional Links

Obsidian tracks backlinks automatically, but be intentional:
- If note A links to note B, ask: should note B link back to A?
- If the relationship is **mutual** (both notes benefit from the connection): yes, link both ways.
- If the relationship is **hierarchical** (A builds on B but B doesn't need to know about A): one-way is fine.

## Maps of Content (MOC)

A MOC is an index note — it links to a cluster of related notes but does not itself contain core ideas.

- Create a MOC when 3+ notes share a theme and no parent note exists.
- Name MOCs with the suffix `-moc`: `[[productivity-moc]]`, `[[neuroscience-moc]]`.
- Store MOCs in `40-Resources/` or at the root of a relevant folder.
- MOCs should list notes with a one-line description of each link.

## Alias Links

Use aliases when a note's full slug is unwieldy in prose:
```markdown
[[spaced-repetition-improves-long-term-recall|spaced repetition]]
```
