# 🛠️ TROUBLESHOOTING PLAYBOOK — Common problems + verified fixes

> Every error below appeared REAL during actual setups and was solved. If you see one, the fix is here.

---

## 1. `npm : File ...npm.ps1 cannot be loaded because running scripts is disabled`

**Cause:** PowerShell blocks scripts (execution policy = Restricted). Node is installed correctly, but PowerShell refuses `npm.ps1`.

**Fix (works instantly):**
```
npm.cmd i -g reasonix
```
Or (permanent, once):
```
Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned
```
Or just open classic CMD (type `cmd` in Start) — there `npm` works directly.

---

## 2. `The '--' operator works only on variables... Unexpected token 'config'`

**Cause:** PowerShell, command with a quoted path without `&` at the start.

**Fix:**
```
& "C:\full\path\program.exe" --config config.yaml
```
In PowerShell, any exe with a quoted path needs `&` in front.

---

## 3. `Error: Option '--port' requires an argument`

**Cause:** The command was cut off at `--port`, without the value `4000` on the same line.

**Fix:** Whole command on ONE line, `4000` before Enter:
```
litellm --config litellm_config.yaml --port 4000
```

---

## 4. `ImportError: cannot import name 'get_flat_dependant' from 'fastapi...'`

**Cause:** FastAPI too old, incompatible with newer LiteLLM (version conflict).

**Fix:**
```
python -m pip install --upgrade --force-reinstall "litellm[proxy]"
```
This reinstalls everything clean (FastAPI, uvicorn, pydantic to compatible versions).

---

## 5. `litellm is not recognized`

**Cause:** The exe is installed but not on PATH (especially with Python from the Microsoft Store).

**Fix — find the exact path:**
```
python -c "import sysconfig; print(sysconfig.get_path('scripts'))"
```
Then run with the full path:
```
& "C:\path\from\above\litellm.exe" --config litellm_config.yaml --port 4000
```
Or add the Scripts folder to PATH (System Properties → Environment Variables → Path → New).

---

## 6. `python -m litellm` → `No module named llm.__main__`

**Cause:** LiteLLM does NOT run with `python -m`. Only the direct exe works.

**Fix:** Never use `python -m litellm`. Use `litellm --config ...` directly (or with the full path).

---

## 7. `! provider "deepseek-v4-flash" requires DEEPSEEK_API_KEY` / `Authentication failed (HTTP 401)`

**Cause:** The API key isn't reaching Reasonix. The `/config` and `/reasonix-guide sk-...` commands DON'T work (they're not key-configuration commands).

**Fix (the correct one):**
1. Exit the chat: `exit`
2. Run in terminal: `reasonix setup` → choose DeepSeek → paste your key
3. Or create a `.env` file in the root with a single line:
```
DEEPSEEK_API_KEY=sk-...your_key...
```
4. Restart `reasonix --model deepseek-v4-flash`

**Verify:**
```
echo %DEEPSEEK_API_KEY%
```
If you see the key → all good.

---

## 8. Key doesn't show up after `setx` / environment variable

**Fix:** Close and reopen the terminal — `setx` writes permanently, but it only loads in a new terminal. Or use the .bat which sets the key automatically on every start.

---

## 9. Windows hides extensions (.bat not visible)

**Fix:** File Explorer → View → Show → **File name extensions** → check it.

---

## 10. The difference between `.template` and the real file

- `Start_Reasonix.bat.template` → the model, DON'T edit it
- `Start_Reasonix.bat` → the real copy, HERE you put the key

**Steps:** copy the template → rename without `.template` → Notepad → put your key → save.

---

## Golden rules

1. **In PowerShell:** exe in quotes = `&` in front. Use `.cmd` commands if `.ps1` is blocked.
2. **Never use `python -m litellm`** — only the direct exe.
3. **Never put keys in slash commands** — keys go into `reasonix setup` or `.env`.
4. **Personal key = your own account** — don't share keys with anyone; everyone makes their own account.
5. **After any PATH/environment change** → close and reopen the terminal.
