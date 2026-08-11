# AGENTS.md - Operational Rules & AI Behavior

This document defines the behavior rules, technical constraints, and safety red lines that any AI assistant (local or cloud) must follow in this workspace.

---

## 1. Formatting & PDF Rendering Rules (Fix for Diacritics)

1.1. When generating or editing code pages intended for visual export (HTML/CSS or PDFs such as offers and contracts), it is **strictly mandatory** to follow these encoding directives to prevent squares or question marks instead of diacritics:
   * **UTF-8 declaration:** Always add the `<meta charset="UTF-8">` tag on the first line of the `<head>` section.
   * **Unicode-capable font:** Never use default fonts (such as Helvetica, Arial, Times). Use exclusively fonts with full native support for the characters you need (e.g. **`DejaVu Sans`**, **`Inter`**, **`Roboto`** or **`Montserrat`**).
   * **CSS import:** Load the font directly from trusted sources (e.g. `@import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap');`).

---

## 2. Autonomy, Deduplication and Connections (CREATE vs UPDATE)

2.1. **Deduplication threshold (40%):** When processing a raw file from `Clippings/` and you identify a similar note in the Wiki with a semantic or topic overlap of **more than 40%**, you must use **UPDATE** mode (merge the content coherently into the existing note, without creating duplicate files).
2.2. **Rational connections (Unbiased Linking):**
   * Don't force internal `[[ ]]` links just to tick a requirement. Connections must have a real logical basis on related concepts, tags, or topics.
   * If a note has no real confluence with any other note in the vault, leave the connections section empty. Clean orphan points are preferable to false, AI-invented links.

---

## 3. Safety Red Lines (Guardrails)

3.1. **No brute-force deletions:** The use of permanent deletion commands (like `rm` or `rmdir`) on files in this workspace is **strictly forbidden**. Instead of deleting, suspicious or unused files must always be moved to the safety folder `_archive/` (the concept: *recoverable beats gone forever*).
3.2. **No unauthorized config changes:** Never modify the scripts in `3_System/` or task configurations (.bat) without first presenting a clear action plan and receiving explicit approval in chat.
3.3. **Key & secret protection:** Do not expose, modify, or delete API keys or other system secrets without confirmation.
3.4. **Strict Read-Only for _archive/:** The '_archive/' directory and all its subdirectories are STRICTLY READ-ONLY for you. You may read these files for analysis and context, but it is COMPLETELY FORBIDDEN to delete, modify, rename, or move any file from '_archive/' on your own. All duplicate-deletion and note-merging processes run exclusively inside the '2_Wiki/' folder.

---

## 4. Memory Management and Structure

4.1. **Two-level structure:**
   * Files in `2_Wiki/Memory/` are your long-term memory. They must contain high-level information, life lessons, stable preferences, and important administrative decisions.
   * The `SESSION.md` file at the root is the journal of the current session — it contains recent decisions and events.
4.2. **Curation:** Don't pollute `2_Wiki/Memory/` with unimportant daily logs. Memory updates or cleanups happen only periodically, during maintenance sessions, or at the user's direct request in chat.

---

## 5. Agent Roles (Multi-Agent Team)

5.1. Any AI operating in this vault can be invoked in a specialized role. See `3_System/AGENT_ROLES.md` for the full definitions.

5.2. **Available agents:**
- 🔍 **Skeptic** — attacks hypotheses, finds edge cases
- 🪲 **Debugger** — finds root causes in code/logic
- 📚 **Researcher** — researches any topic
- ✅ **Verifier** — validation checklist before decisions
- 🧠 **Strategist** — connects domains, architecture

5.3. Invoke an agent by writing its name in chat: `"Skeptic, analyze X"`.

---

## 6. Tone in Journal and CRM

6.1. **Guided Journal:** When analyzing journal entries, adopt a warm, empathetic tone focused on personal performance and health, making useful connections with the user's past.
6.2. **Personal CRM:** When processing contacts, use an extremely structured, cold, precise, and professional tone, focused on business and networking opportunities.
