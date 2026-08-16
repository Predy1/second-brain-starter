# 🚀 SETUP GUIDE — Second Brain + Copilot (Obsidian)

> Total time: ~15 minutes. Cost: **~$0** — you bring your own model key, or use Copilot Plus built-in models.

---

## How it works

```
You (voice/keyboard)
   ↓
Copilot chat (inside Obsidian)
   ↓
Model: Copilot Plus (built-in)  OR  your own key (OpenRouter / OpenAI / DeepSeek / Gemini / local Ollama)
```

- **Obsidian = the memory** (your vault)
- **Copilot = the chat brain** (plugin, inside Obsidian)
- **Model = the reasoning** (cloud by default, local via Ollama if you want offline)

---

## Step 1 — Install Obsidian + open the vault (5 min)

1. Download from [obsidian.md](https://obsidian.md)
2. Install
3. Rename the project folder to **`Second Brain`** (two words, with a space — same as the original vault)
4. On first open: **"Open folder as vault"** → select the `Second Brain` folder
5. Done — the vault with the full structure is ready. The Files sidebar should look exactly like the original layout: `00_MASTER.md`, `2_Wiki/`, `3_System/`, `memory/`, `Projects/`, `Resources/`, `Private/`, `Clippings/`, `_archive/`, the Bases, etc.

> ⚠️ If you rename the folder after opening it in Obsidian: close Obsidian first, rename, then reopen the folder as vault.

---

## Step 2 — Enable plugins + Copilot (3 min)

1. In Obsidian: **Settings → Community plugins**
2. If it says **Restricted mode** is on → click **Turn on community plugins** (Obsidian asks you to trust the plugins — they are all from the official Obsidian community list)
3. The included plugins (Copilot, Dataview, Templater, Smart Connections, etc.) are installed but **not activated**
4. Activate **Copilot** (the most important one) — the toggle next to it in the plugin list
5. Optional: activate the others (Dataview, Templater, QuickAdd, Smart Connections, Omnisearch...)
6. Reload Obsidian if prompted (Ctrl+R)

> Only Copilot is required. The rest are quality-of-life: Dataview (queries), Templater (templates), QuickAdd (fast capture), Omnisearch (fast search), Smart Connections (note links).

---

## Step 3 — Choose your AI model (5 min)

Open the **Copilot chat** (ribbon icon on the left, or Command Palette → "Copilot: Open chat").

### Option A — Copilot Plus (easiest, no keys)
- Models like **copilot-plus-flash** come built-in
- Requires a Copilot Plus subscription (enabled in Copilot settings)
- Nothing to configure — just pick the model from the chat dropdown

### Option B — Your own API key (free-to-cheap, recommended)
One key from any provider, pasted into **Copilot settings → Model** (or the chat model dropdown → add API key):

| Provider | Cost | Notes |
|---|---|---|
| **OpenRouter** | Free models exist, others pay-per-use | One key gives access to hundreds of models (Gemini, Claude, GPT, DeepSeek...) |
| **DeepSeek** | ~$1-3 one-time top-up, lasts weeks | [platform.deepseek.com](https://platform.deepseek.com) → API Keys |
| **OpenAI** | Pay-per-use | GPT models |
| **Google AI Studio** | Free tier | [aistudio.google.com](https://aistudio.google.com) → Get API key |

**Rule: the key goes ONLY into Copilot settings — never into a note, never into this repo.**

---

## Step 4 — First conversation: bootstrap (5 min)

1. Open **Copilot chat** in Obsidian
2. Paste the whole prompt from **[PROMPT_FIRST_RUN.md](PROMPT_FIRST_RUN.md)** as your first message
3. Copilot reads your vault structure, asks you a few questions, and fills in:
   - `3_System/USER.md` → who you are
   - `IDENTITY.md` → who your AI is
   - `SOUL.md` → what matters to you
   - `3_System/BOOTSTRAP.md` → your first session plan
4. Done — from now on you just chat with Copilot inside Obsidian. It knows the vault.

---

## Optional — Voice input (5 min)

1. **Settings → Time & Language → Language & region**
2. **Add a language** → pick yours → Install
3. Click on the language → **Language options** → under **Speech** click **Download**
4. To dictate: press **Win + H** anywhere in Obsidian → speak → text is typed

> ⚠️ If "Speech" doesn't appear, use [dictation.io](https://dictation.io) in the browser and copy-paste.

---

## Optional — Offline AI with Ollama

> Only if you want AI without internet. Local models are weaker — don't use them for complex thinking.

1. Download from [ollama.com](https://ollama.com)
2. Pull a model: `ollama pull qwen2.5:1.5b` (or any model you like)
3. In Copilot settings → **Local models** → pick your Ollama model

---

## 🎯 Summary

| Step | What you get |
|---|---|
| 1 | Obsidian with the full Second Brain structure |
| 2 | Copilot plugin enabled |
| 3 | A working AI model (Copilot Plus or your own key) |
| 4 | Vault bootstrapped (USER, IDENTITY, SOUL) |

Total: **~15 minutes, ~$0** (plus whatever model you choose).
