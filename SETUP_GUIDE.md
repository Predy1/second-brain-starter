# 🚀 SETUP GUIDE — Second Brain + AI

> Total time: ~30 minutes. Cost: **~$0** (see Variant B — DeepSeek has a small one-time top-up).

---

## 🅰️ Variant A — Gemini (100% FREE) | 🅱️ Variant B — DeepSeek (simpler, small cost)

**Recommendation: Variant B.** It's much simpler (no LiteLLM, no FastAPI, no version conflicts). DeepSeek V4-Flash is cheap: ~$1-2 lasts for weeks of conversation.

| | A: Gemini (LiteLLM) | B: DeepSeek (direct) |
|---|---|---|
| Complexity | High (proxy + YAML config) | **Low (one .bat)** |
| Cost | 100% free | One-time top-up (~$2-5) |
| Steps | 5-8 | **3 steps** |
| Risks | FastAPI/LiteLLM can break | Almost zero |
| Romanian | Excellent | Good |

---

## Step 1 — Install Obsidian (5 min)

1. Download from [obsidian.md](https://obsidian.md)
2. Install
3. On first open: **"Open folder as vault"** → select the `SecondBrain` folder
4. Done — vault with full structure is ready

---

## Step 2 — Install Node.js (required for Reasonix) (5 min)

1. Download from [nodejs.org](https://nodejs.org) (LTS version)
2. Install with default settings
3. Verify in terminal: `node --version` → should show `v20+`

---

## Step 3 — Get your FREE Gemini key (2 min) ⭐ IMPORTANT

This is your AI brain. **Free, no card, 1M context.**

1. Go to [aistudio.google.com](https://aistudio.google.com)
2. Log in with your Google account
3. Click **"Get API key"** → **"Create API key"**
4. Copy the key (starts with `AIza...` or `AQ.Ab...`)
5. **Save it in `GEMINI_KEY.txt`** in the `3_System/` folder (not in git!)

---

## Step 4 — Install LiteLLM (the proxy to Gemini) (10 min)

LiteLLM lets Reasonix talk to Gemini.

1. Open a terminal (cmd)
2. Install Python: [python.org](https://python.org) → version 3.11+
3. Run:
   ```
   pip install litellm
   ```
4. Copy `litellm_config.template.yaml` → rename it `litellm_config.yaml`
5. Open it in Notepad and put your key instead of `YOUR_GEMINI_API_KEY`

---

## Step 5 — Install Reasonix (10 min)

1. `npm install -g reasonix` (or follow the instructions on the Reasonix site)
2. Verify: `reasonix --version`

---

## Step 6 — Install Ollama (OPTIONAL — offline only) (10 min)

> Only if you want AI even without internet. It's weak (1.5B) — don't use it for complex thinking.

1. Download from [ollama.com](https://ollama.com)
2. Run in terminal: `ollama pull qwen2.5:1.5b`

---

## Step 7 — Voice input (5 min)

1. **Settings → Time & Language → Language & region**
2. **Add a language** → pick yours → Install
3. Click on the language → **Language options** → under **Speech** click **Download**
4. To dictate:
   - Press `Win + Space` → select your keyboard
   - Press `Win + H` → dictation bar appears
   - Speak → text is typed

> ⚠️ If "Speech" doesn't appear, use [dictation.io](https://dictation.io) in the browser and copy-paste into the terminal.

---

## Step 8 — Start everything (2 min)

1. Open a terminal
2. Start the proxy:
   ```
   litellm --config litellm_config.yaml --port 4000
   ```
3. Open a SECOND terminal, go to the vault folder:
   ```
   cd SecondBrain
   set GEMINI_API_KEY=your_key_here
   reasonix
   ```
4. Done! The AI starts with your structure. On first run it guides you through BOOTSTRAP (name, vibe, SOUL).

---

## 🅱️ VARIANT B — DEEPSEEK DIRECT (RECOMMENDED, just 3 steps)

> Skip steps 3-7 above. Just do this:

### Step B1 — Create a DeepSeek account (5 min)
1. Go to [platform.deepseek.com](https://platform.deepseek.com)
2. Create account → **Top Up** (minimum — ~$2-5)
3. **API Keys** → **Create** → copy the key (starts with `sk-`)

### Step B2 — Put the key in the launcher (1 min)
1. In the `SecondBrain\` folder you'll find **`Start_Reasonix.bat.template`**
2. **Copy it** and rename it **`Start_Reasonix.bat`**
3. Open in Notepad → replace `YOUR_DEEPSEEK_API_KEY` with your real key
4. Save

### Step B3 — Double-click `Start_Reasonix.bat`
- Terminal opens → Reasonix starts with DeepSeek → talk to it
- **Done!** No LiteLLM, no YAML config, no `--port 4000`

---

## 🎯 Architecture summary

```
You (voice/keyboard)
   ↓
Reasonix (the agent, in terminal)
   ↓
DeepSeek V4-Flash (cloud — direct, no proxy)
```

- **DeepSeek = the brain** (cloud, cheap)
- **Obsidian = the memory** (your vault)
- **Ollama/Qwen = offline plan B** (only if you have no internet)
