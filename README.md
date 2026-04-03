# second-brain-claudekit

A Claude Code kit for building and operating a powerful second brain with Obsidian + Claude. Designed to minimise prompting friction so you can focus on thinking and content.

## Structure

```
second-brain-claudekit/
  CLAUDE.md           ← root config: how Claude operates in this vault
  commands/           ← slash commands (/capture, /journal, /connect, etc.)
  agents/             ← sub-agent configs (researcher, writer, connector, reviewer)
  hooks/              ← automation hooks (post-note-create, auto-link, daily-summary)
  templates/          ← Obsidian note templates (daily, project, idea, etc.)
  vault-rules/        ← vault conventions (naming, linking, folder structure, tags)
```

## Quick Start

1. **Copy to your vault root** (or use as a Claude Code project in WSL/Windows):
   ```
   cp -r second-brain-claudekit/.  your-vault/.claude-kit/
   ```
2. **Place `CLAUDE.md`** at the root of your Claude Code project (or vault root).
3. **Copy `commands/`** to `.claude/commands/` to enable slash commands in Claude Code.
4. **Copy `templates/`** to your Obsidian vault's `90-Templates/` folder.
5. Open Claude Code in your vault directory and start with `/capture` or `/journal`.

## Commands

| Command | Purpose |
|---|---|
| `/capture` | Dump a raw idea into inbox |
| `/journal` | Create or open today's daily note |
| `/connect` | Find connections between notes |
| `/summarize` | Progressive-summarise a note |
| `/research` | Deep-dive research, saved as literature notes |
| `/brainstorm` | Ideation session, auto-saves atomic notes |
| `/review` | Weekly/monthly vault review |
| `/inbox-process` | Process inbox one note at a time |

## Vault Layout

The kit assumes and enforces this folder structure in your Obsidian vault:

```
vault/
  00-Inbox/       ← raw captures
  10-Daily/       ← daily notes (YYYY-MM-DD)
  20-Projects/    ← active projects
  30-Areas/       ← ongoing areas of responsibility
  40-Resources/   ← literature notes, research
  50-Archive/     ← completed/dormant
  90-Templates/   ← Obsidian Templater templates
  _attachments/   ← images, PDFs
```

See `vault-rules/folder-structure.md` for the full conventions.
