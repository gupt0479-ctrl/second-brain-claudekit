# second-brain-claudekit

A Claude Code kit for building and operating a powerful second brain with Obsidian + Claude. Designed to minimise prompting friction so you can focus on thinking and content.

---

## Structure

```
second-brain-claudekit/
  CLAUDE.md                   ← root config: stable rules, vault layout, CPR session pattern
  .gitignore

  .claude/                    ← Claude Code project config (copy to your vault root)
    commands/                 ← vault-specific slash commands
    agents/                   ← sub-agent configs
    hooks/                    ← PowerShell automation hooks
    settings.json             ← hook bindings, autoCompact: false
    settings.local.json       ← machine-local overrides (gitignored)

  commands/                   ← global commands (copy to ~/.claude/commands/)
  templates/                  ← Obsidian Templater note templates
  vault-rules/                ← vault conventions (naming, linking, folders, tags)

  00_Daily/                   ← daily notes (YYYY-MM-DD)
  10_Areas/                   ← areas of responsibility
  20_Projects/                ← active projects
  30_Knowledge/               ← evergreen notes, literature, research
  40_Career/                  ← career notes
  50_Claude/                  ← AI-generated artifacts
    Sessions/                 ← session logs from /compress
    Summaries/                ← weekly/monthly rollups
    Patterns/                 ← reusable prompts and frameworks
    Templates/                ← session, review, pattern templates
```

---

## Quick Start

### 1. Set up Claude Code in your vault

```sh
# Copy the .claude/ folder to your Obsidian vault root
cp -r .claude/ ~/your-vault/.claude/

# Copy CLAUDE.md to your vault root
cp CLAUDE.md ~/your-vault/CLAUDE.md
```

### 2. Install global commands

```sh
# Global commands work in any Claude Code project
mkdir -p ~/.claude/commands/
cp commands/*.md ~/.claude/commands/
```

### 3. Install Obsidian templates

Copy `templates/` to your vault's `90-Templates/` folder and configure Obsidian Templater to point there.

### 4. Create the vault folder structure

Create these folders in your vault if they don't exist:
`00_Daily/`, `10_Areas/`, `20_Projects/`, `30_Knowledge/`, `40_Career/`, `50_Claude/Sessions/`, `50_Claude/Summaries/`, `50_Claude/Patterns/`, `50_Claude/Templates/`

Copy `50_Claude/Templates/*.md` into your vault's `50_Claude/Templates/`.

### 5. Start a session

```
/context   ← loads vault state into Claude's working memory
/today     ← opens or creates today's daily note
```

---

## Commands

### Global (install to `~/.claude/commands/`)

| Command | Purpose |
|---|---|
| `/preserve` | Update CLAUDE.md with a new stable rule from this session |
| `/compress` | Write a structured session log to `50_Claude/Sessions/` |
| `/resume` | Load context from last session log to pick up where you left off |
| `/capture` | Dump a raw idea into the inbox |
| `/brainstorm` | Ideation session, auto-saves atomic notes |
| `/connect` | Find conceptual links between notes |
| `/research` | Deep-dive research → literature notes + MOC |
| `/review` | Weekly/monthly vault review |
| `/summarize` | Progressive-summarise a note |
| `/inbox-process` | Process inbox one note at a time |

### Vault-specific (live in `.claude/commands/`)

| Command | Purpose |
|---|---|
| `/context` | Load vault context into Claude's working memory |
| `/today` | Create or open today's daily note |
| `/trace` | Trace an idea's evolution across the vault |
| `/graduate` | Promote a mature idea to an evergreen note |
| `/closeday` | End-of-day: review, task rollover, session log |
| `/emerge` | Surface latent patterns from recent notes |
| `/ghost` | Free-write mode — no formatting or judgment |
| `/challenge` | Steelman and stress-test an idea |
| `/ideas` | Fast ideation sprint, saves atomic notes |
| `/drift` | Find stale, orphaned, or superseded notes |
| `/schedule` | Build a schedule from tasks across the vault |

---

## Agents

Three sub-agents, each with a focused mandate:

| Agent | Purpose |
|---|---|
| `vault-curator` | Keeps notes linked, clean, and deduplicated |
| `research-distiller` | Turns rough notes into compact evergreen notes |
| `weekly-reviewer` | Runs end-of-week review, creates weekly summary |

---

## Hooks

Two hooks run automatically via `.claude/settings.json`:

| Hook | Trigger | Effect |
|---|---|---|
| `after-edit-log.ps1` | After any file edit | Appends a log entry to `50_Claude/Sessions/_today-edits.md` |
| `session-wrapup.ps1` | Session end | Reminds you to run `/compress` if no session log was written |

Both are PowerShell scripts — compatible with Windows and WSL (pwsh).

---

## Session Memory: CPR Pattern

The kit uses a **Compress → Preserve → Resume** loop:

1. **`/compress`** — at session end, writes a structured log to `50_Claude/Sessions/`
2. **`/preserve`** — updates `CLAUDE.md` with any new durable rule from the session
3. **`/resume`** — at session start, loads context from the last log

`autoCompact` is disabled in `settings.json` so you control exactly when compression happens.

**Three layers of memory — use each for the right thing:**

| Layer | What goes here |
|---|---|
| `CLAUDE.md` | Stable rules, durable preferences |
| `50_Claude/Sessions/` | What happened in sessions |
| Vault evergreen notes | Insights worth long-term reuse |

---

## Vault Layout

| Folder | Purpose |
|---|---|
| `00_Daily/` | Daily notes (`YYYY-MM-DD.md`) |
| `10_Areas/` | Ongoing responsibilities |
| `20_Projects/` | Active, time-bounded projects |
| `30_Knowledge/` | Evergreen notes, literature, research |
| `40_Career/` | Career and professional development |
| `50_Claude/` | AI artifacts (sessions, summaries, patterns, templates) |

See `vault-rules/folder-structure.md` for full conventions.

