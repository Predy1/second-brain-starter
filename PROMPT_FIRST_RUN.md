# 🤖 FIRST-RUN PROMPT — paste this into Reasonix

> Copy-paste the whole block below into Reasonix (after it starts from `Start_Reasonix.bat`).

---

I'm on a Windows laptop, just installed Reasonix. Help me finish the setup correctly, without repeating the classic mistakes.

CONTEXT (read these first, in order):
1. TROUBLESHOOTING_PLAYBOOK.md — all already-solved errors + exact fixes
2. SETUP_GUIDE.md — Variant A (Gemini via LiteLLM) or Variant B (DeepSeek direct)
3. REPOPACK_CONTEXT.md — all the vault context

GOAL: Get me set up with a working AI (DeepSeek recommended — simple, one .bat), with a .bat that starts everything on double-click.

STEPS:
1. Check if I have an API key in .env or ask me for it (DeepSeek: platform.deepseek.com → API Keys → starts with sk-)
2. Copy Start_Reasonix.bat.template → Start_Reasonix.bat and put my key in it (NOT in the template!)
3. Verify Reasonix starts with: reasonix --model deepseek-v4-flash
4. Test each step before the next; at any error, stop and explain what I should do

RULES:
- New error? Look it up in TROUBLESHOOTING_PLAYBOOK.md first
- PowerShell: exe in quotes = `&` in front; `.ps1` blocked = use `.cmd` (e.g. npm.cmd)
- Never print API keys in output
- At the end: summary of what you configured + how I start everything with one click

---

## Note on variants

| Variant | AI | Cost | Complexity |
|---|---|---|---|
| **B (recommended)** | DeepSeek V4-Flash | ~$2-5 one-time top-up | Low — one .bat |
| A | Gemini (via LiteLLM) | 100% free | High — proxy + YAML config + FastAPI |

**Choose B** if you want fast and simple. Choose A only if you want strictly free and are OK with extra steps.
