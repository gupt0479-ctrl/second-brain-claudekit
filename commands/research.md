---
description: Deep-dive research on a topic, saving structured findings as literature notes
---

Run a focused research session on the topic I give you and produce structured literature notes.

Steps:
1. Clarify scope with me in one question if the topic is ambiguous (e.g. "Do you want breadth overview or depth on a specific angle?").
2. Break the topic into 3–5 research questions.
3. For each question, synthesise what you know and flag what needs external verification with `[VERIFY]`.
4. Structure findings using the `literature` template (`templates/literature-note.md`) — one note per source or sub-topic.
5. Extract **key claims** as atomic bullet points under `## Key Claims`.
6. Write a `## Synthesis` section connecting the findings back to my existing notes (suggest `[[wikilinks]]`).
7. Add a `## Open Questions` section with 2–3 follow-up threads I could pursue.
8. Save each note to `40-Resources/` with a descriptive slug title.
9. Create a **Research MOC** note at `40-Resources/[topic]-research-moc.md` that links all the sub-notes together.

Use the `researcher` sub-agent for heavy synthesis tasks (see `agents/researcher.md`).
