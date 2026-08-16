# 🧠 Second Brain Starter

A clean, ready-to-use **Obsidian Second Brain** with an AI assistant built in — a proven personal knowledge-management system, packaged as a starter for anyone.

## 📦 What's included

| Component | What it is | Cost |
|---|---|---|
| 📓 **Obsidian vault** | Second Brain structure — same layout as the original (Dashboard, Master, Journal, Memory, Thoughts, Inbox, Projects, Resources, Private, Clippings, Bases) | Free |
| 🧠 **Main AI** | **Copilot** — chat AI built into Obsidian. Copilot Plus flash models (built-in, no keys) or bring your own key (OpenRouter / OpenAI / DeepSeek / Gemini) | Free (BYO key) / Copilot Plus optional |
| 🏠 **Offline AI** (optional) | Ollama — local models, when you have no internet | Free |
| 🤖 **Agent team** | Built into the AI via `3_System/AGENT_ROLES.md` — Skeptic, Debugger, Researcher, Verifier, Strategist (invoke by name) | Free |
| 🎤 **Voice input** | Win+H (Windows Voice Typing) + any language pack | Free |

## 🚀 Quick start

See **[SETUP_GUIDE.md](SETUP_GUIDE.md)** — 4 steps, everything you need to install and configure (~15 minutes).

## 📁 Vault structure

```
Second Brain/            ← name the vault folder exactly like this
├── 00_MASTER.md         → Master context (current goal, plan, key facts)
├── 00_DASHBOARD.canvas  → Dashboard hub (visual map of the vault)
├── CLAUDE.md            → Router for the AI (what it reads first)
├── AGENTS.md            → Redirect to the real rules
├── IDENTITY.md          → Who your AI is (filled during BOOTSTRAP)
├── USER.md              → Who you are
├── SOUL.md              → What matters to you
├── SESSION.md           → Where you left off (resume point)
├── TOOLS.md             → Tools and skills
├── HEARTBEAT.md         → Periodic checks
├── HOTCACHE.md          → Session context (distilled, updated often)
├── MEMORY.md            → Long-term memory (curated)
├── _INBOX.md            → Quick capture
├── Projects.base · Tasks.base · Books.base · Papers.base · Youtube.base
├── memory/              → Daily notes (YYYY-MM-DD.md)
├── 2_Wiki/              → Your content
│   ├── Dashboard.md · index.md · Navigate.md · log.md · Kanban.md
│   ├── Attachments/ · Inbox/ · Journal/ · Memory/ · Thoughts/
│   ├── Business/ · CRM/ · Freelancing/ · Gaming/ · Health/
│   ├── PC_Optimization/ · Personal/ · Second_Brain/ · Trading/
├── 3_System/            → AI rules and configuration
│   ├── AGENTS.md        → AI behavior rules
│   ├── AGENT_ROLES.md   → Specialized agent team
│   ├── BOOTSTRAP.md     → First conversation with your AI
│   ├── DAILY_STARTUP.md → Daily ritual
│   ├── STARTUP_CHECKLIST.md → Session discipline
│   ├── SELF_IMPROVEMENT.md → Lessons learned
│   └── VALIDATION_GATES.md → Fixed rules before decisions
├── Projects/            → Project notes (visible in Projects.base)
├── Resources/           → Books/ · Papers/ · Youtube/ (visible in the bases)
├── Private/             → Personal notes, not for sharing
├── Clippings/           → Raw web clips to process
├── _archive/            → Old/unsorted notes (read-only for the AI)
└── copilot/             → Copilot conversations (auto-created, git-ignored)
```

## 🔌 Included plugins (14)

| Plugin | What it does |
|---|---|
| **Copilot** | Chat AI directly in Obsidian |
| **Claude Sidebar** | Claude assistant in the sidebar |
| **Dataview** | Query notes (tables, dynamic lists) |
| **Templater** | Advanced templates |
| **Smart Connections** | Smart links between notes |
| **Various Complements** | Autocomplete while typing |
| **Omnisearch** | Fast search everywhere |
| **QuickAdd** | Quick capture (Ctrl+Alt+I → inbox) |
| **Custom Frames** | Web panels in Obsidian |
| **Kanban** | Kanban boards |
| **Persistent Graph** | Graph position persists |
| **HTML Plugin** | Import HTML files |
| **Supercharged Links** | Styled/iconed links based on note tags |
| **Style Settings** | Adjust themes and snippets from the settings UI |

**Snippets:** 9 (folder colors, tag colors, note status, graph view, navigation buttons, bookmarks buttons, ewan theme, clipping cards, supercharged links) — same colors and filters as the original vault.

> Note: plugins are installed in `.obsidian/plugins/` but **not activated automatically** — on first open Obsidian asks permission to enable them.

## 🎨 Style

- Clean structure, most text neutral/plain
- **Agent team** (`3_System/AGENT_ROLES.md`): Skeptic, Debugger, Researcher, Verifier, Strategist — invoke them by name
- A bit of character: DAILY_STARTUP and Dashboard have a direct, action-first tone

## 🔒 About API keys

**Never put real API keys in this public repo.** Your key goes only into the Copilot settings inside Obsidian (stored in `.obsidian/plugins/copilot/data.json`, git-ignored). Never write a key into a note.

## 🛠️ Troubleshooting

See **[TROUBLESHOOTING_PLAYBOOK.md](TROUBLESHOOTING_PLAYBOOK.md)** — common problems and fixes (plugins not enabled, model/API-key errors, indexing, and more).

---

Built for anyone who wants a personal knowledge base with an AI brain, on Windows. Fork it, make it yours, bootstrap it in one conversation.
