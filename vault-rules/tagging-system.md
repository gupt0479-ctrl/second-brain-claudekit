# Tagging System

Tags in Obsidian complement links — they group notes by property rather than by concept. Use both; do not substitute one for the other.

## Tag Taxonomy

### Type Tags (always present via frontmatter `type`)
These are set automatically by templates. Do not add manually.

| Tag | Meaning |
|---|---|
| `#daily` | Daily journal note |
| `#project` | Active project note |
| `#area` | Area of responsibility note |
| `#literature` | Book, article, podcast, or research note |
| `#idea` | Raw or developing idea |
| `#meeting` | Meeting notes |
| `#person` | Contact / person note |
| `#moc` | Map of Content index note |

### Status Tags
Track where a note is in its lifecycle.

| Tag | Meaning |
|---|---|
| `#raw` | Unprocessed, straight from inbox |
| `#developing` | Being actively worked on |
| `#mature` | Stable, well-linked, unlikely to change much |
| `#stale` | Hasn't been touched in 90+ days, review needed |
| `#open-question` | Contains an unanswered question worth pursuing |
| `#orphan` | No links yet — needs connecting |

### Domain Tags
Apply relevant domain tags to make cross-cutting searches possible.

Examples (adapt to your interests):
- `#learning` `#memory` `#cognition`
- `#productivity` `#focus` `#habits`
- `#writing` `#communication`
- `#tech` `#ai` `#software`
- `#health` `#fitness` `#sleep`
- `#finance` `#career`
- `#philosophy` `#psychology`

### Source Tags
For literature notes — where did this come from?

| Tag | Meaning |
|---|---|
| `#book` | From a book |
| `#article` | From an article or blog post |
| `#paper` | Academic paper |
| `#podcast` | From a podcast |
| `#video` | From a video or talk |
| `#conversation` | From a conversation |

## Tagging Rules

1. **Maximum 5 tags per note.** More than 5 = not selective enough.
2. **No tag for concepts that have their own note.** Use a `[[wikilink]]` instead.
3. **Tags are facets, not folders.** A note can have `#learning` and `#writing` — it doesn't need to choose.
4. **Review tags during `/inbox-process`.** Inbox notes get minimal tags; permanent notes get considered tags.
5. **Nested tags are allowed** (Obsidian supports `#domain/subdomain`): e.g., `#tech/ai`, `#health/sleep`.
