---
class: MOC
status: evergreen
tags: ["trading", "moc"]
---

# 🗺️ Trading Hub

> The central map for your trading research. The edge is **yours** — this system only gives you the process to develop, validate, and track it.

## 🔄 The Pipeline

1. **Capture** — dump any idea into [[IDEA_LOG]] (tag `#idea`)
2. **Research** — ask the Researcher agent; save findings as atomic notes in `2_Wiki/Trading/`
3. **Formalize** — turn a promising idea into a strategy with [[Template_Strategy]]
4. **Backtest** — run the numbers, fill in the Backtest section
5. **Validate** — Skeptic + Verifier attack it (see [[3_System/VALIDATION_GATES]])
6. **Forward test** — small size, strict rules, log every trade with [[Template_Trading_Log]]
7. **Review** — weekly debrief: what works, what doesn't, what's next

## 🎯 Where Things Live

| Content | Where / Template |
|---|---|
| Ideas (raw) | [[IDEA_LOG]] or a note tagged `#idea` |
| Strategies | `2_Wiki/Trading/` using [[Template_Strategy]] |
| Trade journal | Notes using [[Template_Trading_Log]] |
| Lessons | Atomic notes tagged `#lesson` |
| Daily debrief | [[Template_Debrief]] |
| Weekly review | [[Template_Weekly_Review]] |

## 📌 Conventions

- Tag everything: `#trading`, plus `#idea` / `#strategy` / `#lesson` / `#backtest` / `#forward-test`
- Connect every note to at least one other note — linked mentions build your web
- Agent conclusions get the tag `#agent-insight`

## 🧠 Agents at Work

- **Researcher** — "Research how professional X is done"
- **Skeptic** — "Attack my strategy before I backtest it"
- **Verifier** — "Verify this backtest for lookahead bias"
- **Vault Agent** — "Organize my trading notes"
- **Efficientizer** — "Speed up my review workflow"
