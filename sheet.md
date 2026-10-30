# Workshop 4 - Plug in tools (one page)

**Question of the day: what happens when the chatbot acts outside?**
Full page: [README.md](README.md). Setup and common problems: [SETUP.md](SETUP.md).

| Score | When |
|---|---|
| **2** | Right, and it says where it comes from (7 and 9: saying "I don't know" or refusing is right; 8: "no official level today", with the source's sentence, is right when the file has no `live` level). |
| **1** | Honest but not enough: "I don't know" although the answer exists, no source, or partly right. |
| **0** | Wrong or invented. |

## 1. Welcome (20 min)

1. Open the Codespace: **https://codespaces.new/Youth-AI-Lab/yal-workshop-tools** → **Create codespace**.
2. Terminal 1: `workshop-login`, paste the key once, Enter → you see `Key OK`.
3. Drag `my-work.zip` into the file list. Terminal 1: `workshop-start 4 --from my-work.zip`.

## 2. Our tool (20 min)

1. `workshop D`, then `/mcp`: `fire-danger` and `time`. Enter on a server → **View tools**. **Esc**.
2. Question 8 → **Ctrl+O**: what the model asked the tool, what came back (`why_no_level`). **Ctrl+O**.
3. `mcp/fire-danger.json`: `"date"` = today (year-month-day). Antwerp, from its official page:
   `"status"` (`live`, `season-over` or `no-level-shown`), `"source_says"` (copied), and `"level"`,
   `"advice"` only if `live`. Save.
4. Question 8 again, **Ctrl+O**: what changed? `Ctrl+C` twice.

## 3. Servers that already exist (30 min)

1. Open `.mcp.json`: the program and the options of each server.
2. `workshop D`: `Has the Pla Alfa map of Catalonia already had its morning update today?` → **Ctrl+O**:
   was `time` called? Then the same, starting with `Use the time tool:`. `Ctrl+C` twice.
3. `WORKSHOP_WEATHER=1 workshop D`, then `/mcp`: `open-meteo   17 tools` (the model gets 2).
4. `Will it be windy tomorrow in La Rochelle?` → **Ctrl+O**: what was sent to Open-Meteo?
5. `Given the weather, what is the fire danger level today in La Rochelle?`: weather ≠ official level.
   Look at the gauge. `Ctrl+C` twice.

## 4. Read before you install (25 min)

1. `mcp/fire_danger_server.py`: the two `@mcp.tool()` and their descriptions; `DATA`, the file they read.
2. The five questions: who wrote it, what it reads, what it sends away, does it write, is its version fixed.
3. Watch the facilitator's page with a hidden sentence. Who wrote it? Who read it?
4. `mcp/fire-danger.json`: the entry of your territory (or a copy of one entry, with its own name,
   `scale`, `source` and `season`), with its source.
5. `workshop D`: `What is the fire danger level today in <your territory>?` → **Ctrl+O**: your source?
   `Ctrl+C` twice.

## 5. Closing (15 min)

1. `replay D`, then `score D 8 11 12`. Compare with column C.
2. `workshop-save` → right-click on `my-work.zip` → **Download...**. Bring it to [workshop 5](https://github.com/Youth-AI-Lab/yal-workshop-wiki).
3. Exit card: three answers, alone.

**Never make up a level**: only what the official source says, on the day. **Leave a
conversation:** `Ctrl+C` twice. **Copy / paste in the terminal:** `Ctrl+Shift+C` / `Ctrl+Shift+V`
(`Cmd+C` / `Cmd+V` on a Mac).
