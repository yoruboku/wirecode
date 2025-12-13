# Wirecode

**Make coding with AI and the web effortless.**

Wirecode is a browser extension that finds `<code>` in websites AI chat UIs like ChatGPT or Gemini, all website containing `<code>` element etc.) also select the code/text normally and right click and choose wirecode then in sidepanel users can download, preview, edit or just commit to github.

---

## Key features

* **Inline capture button** — Wirecode injects a small `Add` button next to detected `<code>` in websites and send them to sidepanel.
* **Auto Mode** — Automatically captures every code block if the code block's code starts with (#* on the 1st line and end with *#) on last line in all websites.
* **Smart naming** — Wirecode uses the second line of the code as the name or nearby instructions (e.g., “save as `main.py`” from the ai) to auto-name files. If no name can be determined, it falls back to safe defaults like `1.py`, `snippet1.js`, etc. depending on the coding language of the code.
* **Selection capture** — Highlight any code/text and use the right-click menu to add it to Wirecode (works when `<code>` markup is absent).
* **Workspace & folders** — Saved snippets appear in a side-panel. Create nested folders, multi-select, drag & drop to reorder. Snippets from the same source link can be auto-grouped into the same folder.
* **Source linking** — Each snippet stores its origin: clicking the check button scrolls the original page to the exact code position from the history subpanel.
* **History** — Lightweight history showing timestamps, source URL, page position, and filename).
* **Preview & edit** — Preview code in vscode.dev, rename files, edit code.
* **Download & export** — Download single files or entire folders to your local disk.
* **GitHub integration** — Commit captured files directly to a repository with a guided flow and commit message support.
* **Search** — Filter workspace by filename, folder name, or same links.
* **view options** — users can see they wanna see their files in grind view or as a list etc. 
---

## How it works (high level)

1. Wirecode scans the DOM for `<code>`
2. elements and recognized code containers.
3. It places a lightweight small button next to each `<code>` element.
4. On pressing the button, Wirecode stores that code/text (source URL, scroll position, timestamp, filename).
5. Smart naming attempts in this order: explicit filename in code first line → nearby instruction like “save as X” → default based on that coding language.
6. Saved items appear in the side-panel.

---

## commands in the code
1. the 2nd line of the code is the name of the file if the 1st line end with a file extension of coding languages like (example : .py .js .sh etc.).
2. auto mode should only take the code which starts with (#* and end with *#) 
