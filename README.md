# Wirecode

**Make coding with AI and the web effortless.**

Wirecode is a browser extension that finds `<code>` blocks across websites (GitHub, AI chat UIs like ChatGPT or Gemini, blogs, docs, etc.) and lets you collect, organize, preview, and manage them from a single workspace.

---

## Key features

* **Inline capture button** — Wirecode injects a small `Add` button next to detected `<code>` blocks. Tap to capture.
* **Auto Mode** — Automatically captures every code block on pages you visit (configurable per-site or per-domain).
* **Smart naming** — For AI-generated snippets, Wirecode uses the first line or nearby instructions (e.g., “save as `main.py`”) to auto-name files. For GitHub it uses the repository filename. If no name can be determined, it falls back to safe defaults like `1.py`, `snippet.js`, etc.
* **Selection capture** — Highlight any code/text and use the right-click menu to add it to Wirecode (works when `<code>` markup is absent).
* **Workspace & folders** — Saved snippets appear in a side-panel workspace. Create nested folders, multi-select, drag & drop to reorder. Snippets from the same source link can be auto-grouped into the same folder.
* **Source linking** — Each snippet stores its origin: clicking the source link scrolls the original page to the exact code position.
* **History** — Lightweight history showing timestamps, source URL, page position, and filename (does not duplicate full code unless explicitly saved).
* **Preview & edit metadata** — Preview snippets in-place, rename files, add notes or tags, and remove items.
* **Download & export** — Download single files or entire folders to your local disk; drag a folder from the workspace to a local file explorer to export it as a directory.
* **GitHub integration** — Commit captured files directly to a repository with a guided flow and commit message support.
* **Search** — Filter workspace by filename, folder name, or source domain.
* **Safety rules** — Built-in safeguards to avoid applying REPLACE blocks automatically (see `What Wirecode should NOT do`).

---

## How it works (high level)

1. Wirecode scans the DOM for `<code>` elements and recognized code containers.
2. It places a lightweight inline UI control next to each block.
3. On capture, Wirecode stores snippet metadata (source URL, scroll position, timestamp, inferred filename) and the snippet text.
4. Smart naming attempts in this order: explicit filename in code first line → nearby instruction like “save as X” → GitHub filename → fallback default.
5. Saved items appear in the side-panel workspace for organization and export.

---

## Quick start — user flow

1. Install the extension (Chrome/Firefox builds available). Grant required permissions during setup.
2. Open a page with code blocks. Use the `Add` button to capture a snippet, or enable Auto Mode to capture automatically.
3. Open the Wirecode side panel to preview, rename, tag, move to folders, or export.
4. Use right-click → `Add to Wirecode` to capture arbitrary selected text.
5. Use the source link on any saved snippet to jump back to the original page and exact position.

---

## Suggested system prompt for AI integrations

```text
always mention the code file name in the first line of the code block.
if the user must replace some code, write `REPLACE` on the second line and put the replacement code between `REPLACE` markers.
if the user must remove a block of code, wrap that block between `REMOVE` markers.
if the user must create a new file, write `CREATE` on the second line.
if the user must delete a file, write `DELETE` on the second line and place the filename to delete on the first line.
always include the target filename on the first line (even when not using `DELETE`).
```

> **Note:** Wirecode relies on these conventions to auto-name and process AI-generated snippets. The system prompt is a suggestion for AI prompts; Wirecode will still capture raw snippets when AI does not follow the format.

---

## What Wirecode should NOT do

* **Never** automatically apply or paste content that is wrapped with `REPLACE` markers into an existing code file. `REPLACE` blocks are treated as instructions that require explicit user confirmation.
* Avoid making destructive changes without explicit user consent (DELETE/REMOVE actions must always require manual confirmation).

---

## Privacy & security

* Wirecode stores snippet text and metadata locally by default. Cloud sync (optional) is opt-in.
* Source URLs and metadata are stored to enable history and source linking. You can delete history and snippets at any time.
* GitHub commits require explicit OAuth authorization; Wirecode never stores your GitHub password.
* Do not enable Auto Mode on sensitive sites (banking, health portals, private dashboards) — Wirecode provides per-site toggles.

---

## Permissions required

* Read and modify content on web pages (to detect and inject UI). Scope can be limited to specific domains.
* Access to local file system via download/drag-and-drop APIs.
* Optional: GitHub OAuth for committing to repositories.

---

## Installation

* Chrome: install the Chrome Web Store package (or load unpacked in Dev mode).
* Firefox: install from AMO (or load temporary extension in dev mode).

---

## Contributing

Contributions welcome. Please open issues or pull requests on the Wirecode GitHub repository. See `CONTRIBUTING.md` for coding conventions and the extension release process.

---

## License

MIT License — include LICENSE in the repo.

---

## Roadmap & ideas

* Selective cloud sync with encryption.
* Plugin system to add custom filename heuristics or post-processing hooks.
* Collaborative workspaces and snippet sharing.

---

*Created as a README template for the Wirecode browser extension.*
