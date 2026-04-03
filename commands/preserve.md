---
description: Update CLAUDE.md with a new stable rule or preference discovered this session
---

Distil something we learned this session into a durable rule in `CLAUDE.md`.

## When to Use

Use `/preserve` when:
- We discover a preference I want Claude to remember permanently
- A workflow turns out to work better with a specific pattern
- I correct Claude's default behaviour and want it fixed going forward
- A vault convention is clarified or changed

## Steps

1. Ask: *"What stable rule or preference do you want to preserve?"* (if not already stated).
2. Assess where it belongs in `CLAUDE.md`:
   - **Behavioral Rules** — how Claude should act generally
   - **Vault Structure** — conventions about the vault layout
   - **Workflow Rules** — how specific commands or agents should behave
3. Draft the new rule as a concise, actionable bullet point. Show it to me first.
4. Wait for confirmation before editing `CLAUDE.md`.
5. Add the rule under the right section. Never delete existing rules — append or refine.
6. Confirm: *"Preserved: '{{rule}}' added to CLAUDE.md under {{section}}."*

## What NOT to Preserve

- Session-specific context (that goes in `/compress` logs)
- Insights about specific notes (those belong in the notes themselves)
- Temporary workarounds (preserve only durable patterns)

Keep `CLAUDE.md` lean. If a section grows beyond 10 rules, suggest consolidating.
