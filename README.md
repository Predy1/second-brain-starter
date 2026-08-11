# 🧠 Second Brain Starter

A clean, ready-to-use **Obsidian Second Brain** with an AI assistant built in — a proven personal knowledge-management system, packaged as a starter for anyone.

## 📦 What's included

| Component | What it is | Cost |
|---|---|---|
| 📓 **Obsidian vault** | Second Brain structure (Dashboard, Journal, Memory, Thoughts, Inbox) | Free |
| 🧠 **Main AI** | **DeepSeek V4-Flash** (direct, simple .bat launcher) — or Google Gemini Flash via LiteLLM | ~$2-5 one-time top-up (DeepSeek) / free (Gemini) |
| 🏠 **Offline AI** (optional) | Ollama + `qwen2.5:1.5b` — when you have no internet | Free |
| 🤖 **Agent** | Reasonix — AI assistant with a specialized agent team (Skeptic, Debugger, Researcher, Verifier, Strategist) | Free |
| 🎤 **Voice input** | Win+H (Windows Voice Typing) + any language pack | Free |

## 🚀 Quick start

See **[SETUP_GUIDE.md](SETUP_GUIDE.md)** — steps 1-8, everything you need to install and configure.

Prefer a 3-step path? Go straight to **Variant B (DeepSeek direct)** in the setup guide — no LiteLLM, no YAML, just one `.bat` file.

## 📁 Vault structure

```
SecondBrain/
├── CLAUDE.md              → Router for the AI (what it reads first)
├── AGENTS.md              → Redirect to the real rules
├── IDENTITY.md            → Who your AI is (filled during BOOTSTRAP)
├── USER.md                → Who you are
├── SOUL.md                → What matters to you
├── SESSION.md             → Where you left off (resume point)
├── TOOLS.md               → Tools and skills
├── HEARTBEAT.md           → Periodic checks
├── _INBOX.md              → Quick capture
├── memory/                → Daily notes (YYYY-MM-DD.md)
├── 2_Wiki/                → Your content
│   ├── Dashboard.md       → Command center
│   ├── index.md           → Wiki index
│   ├── Navigate.md        → Quick navigation
│   ├── log.md             → Operations log
│   ├── Memory/            → Long-term memory
│   ├── Journal/           → Daily journal
│   ├── Inbox/             → Ideas / capture
│   └── Thoughts/          → Reflections
└── 3_System/              → AI rules and configuration
    ├── AGENTS.md          → AI behavior rules
    ├── AGENT_ROLES.md     → Specialized agent team
    ├── BOOTSTRAP.md       → First conversation with your AI
    ├── DAILY_STARTUP.md   → Daily ritual
    ├── STARTUP_CHECKLIST.md → Session discipline
    ├── SELF_IMPROVEMENT.md → Lessons learned
    └── VALIDATION_GATES.md → Fixed rules before decisions
```

## 🔌 Included plugins (12)

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

**Theme:** Tokyo Night · **CSS snippets:** 7 (folder colors, tag colors, note status, graph view, navigation buttons)

> Note: plugins are installed in `.obsidian/plugins/` but **not activated automatically** — on first open Obsidian asks permission to enable them.

## 🎨 Style

- Clean structure, most text neutral/plain
- **Agent team** (`3_System/AGENT_ROLES.md`): Skeptic, Debugger, Researcher, Verifier, Strategist — invoke them by name
- A bit of character: DAILY_STARTUP and Dashboard have a direct, action-first tone

## 🔒 About API keys

**Never put real API keys in this public repo.** Your key goes only into a local file — see SETUP_GUIDE.md (`.env` or `Start_Reasonix.bat`, both git-ignored).

## 🛠️ Troubleshooting

See **[TROUBLESHOOTING_PLAYBOOK.md](TROUBLESHOOTING_PLAYBOOK.md)** — real errors from real setups, with verified fixes (PowerShell `npm.ps1` blocks, LiteLLM/FastAPI conflicts, API-key issues, and more).

---

Built for anyone who wants a personal knowledge base with an AI brain, on Windows. Fork it, make it yours, bootstrap it in one conversation.
