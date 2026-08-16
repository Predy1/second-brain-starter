# 🛠️ TROUBLESHOOTING PLAYBOOK — Common problems + fixes

> The setup is intentionally simple: Obsidian + the Copilot plugin. If something misbehaves, the fix is usually one of these.

---

## 1. Obsidian says "Restricted mode" — plugins can't be enabled

**Cause:** Community plugins are off by default for safety.

**Fix:** Settings → **Community plugins** → **Turn on community plugins**. Then enable Copilot from the plugin list.

---

## 2. Copilot is enabled but no chat icon/sidebar appears

**Fix:**
1. Reload the vault: Ctrl+R
2. Open via Command Palette (Ctrl+P) → type **"Copilot: Open chat"**
3. If still missing → disable and re-enable the plugin, then reload again

---

## 3. Chat says the model is not available / "model not found"

**Cause:** The selected model isn't available on your plan or provider.

**Fix:**
- Copilot Plus models → check the Copilot Plus subscription is active in Copilot settings
- BYO key models → verify the provider actually offers that model (e.g. OpenRouter model list), and that the key has access
- Switch to a known-good model from the dropdown and retry

---

## 4. Error 401 / Authentication failed

**Cause:** The API key is invalid, expired, or was never entered.

**Fix:**
- Copilot settings → paste the key again (copy it fresh from the provider dashboard)
- Providers show the key **only once** at creation — if you lost it, generate a new one
- No key in the vault → you haven't configured a model; choose Copilot Plus or add a key

---

## 5. Error 429 / "quota exceeded"

**Cause:** The free tier or your balance ran out.

**Fix:**
- Free tier (e.g. Gemini): wait for the quota reset, or add a paid key
- DeepSeek/OpenRouter: top up the account
- Local Ollama model: no quota, works offline

---

## 6. Chat answers are weak / don't use the vault

**Cause:** The model doesn't have vault context, or an embedding model isn't configured for "chat with vault".

**Fix:**
- Make sure Copilot settings → embedding model is set (default: `gemini-embedding-001`)
- Reference the note in chat, or use the "chat with vault" mode so Copilot searches your notes
- Check the model chosen — small/cheap models answer weaker

---

## 7. Conversations/keys accidentally in git

**Cause:** `data.json` (Copilot settings, contains keys) or `copilot/copilot-conversations/` (chat history) got committed.

**Fix:**
- They are git-ignored in this repo (`.gitignore`) — if you changed it, restore that
- If already committed: remove them from tracking with `git rm --cached <file>`, add to `.gitignore`, then commit
- Rotate any key that was exposed — treat it as public

---

## 8. Windows hides file extensions

**Fix:** File Explorer → View → Show → **File name extensions** → check it.

---

## 9. Voice input (Win+H) doesn't type into Obsidian

**Fix:**
- Add your language + speech pack in **Settings → Time & Language**
- If Speech doesn't appear for your language → use [dictation.io](https://dictation.io) and paste

---

## Golden rules

1. **API keys go ONLY into Copilot settings** — never into notes, never into the repo.
2. **Each person makes their own account/key** — don't share keys with anyone.
3. **If a key was ever committed or shared → generate a new one** and delete the old.
4. **No internet?** Use an Ollama local model (weak but free).
5. **Anything weird → reload Obsidian (Ctrl+R) first**, then check the plugin list, then the model config.
