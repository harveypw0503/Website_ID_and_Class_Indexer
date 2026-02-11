# Class & ID Indexer

**Find dead CSS classes, unused IDs, top-used selectors, and compound class combinations across your entire website codebase.**

**Put all .py files in the same folder and run gui.py**

**Originally created for and used by waltercreations.com**

This is a lightweight, offline Python tool that scans HTML, CSS, and JavaScript files to:

- Index every `.class` and `#id` and where they appear
- Detect **dead** (defined in CSS but never used) classes and IDs
- Show the **top 10** most-used classes and IDs
- Extract descriptions from CSS comments placed right before selectors
- List compound/multi-class usages (e.g. `btn.primary.large`)
- Generate a beautiful, clickable Markdown report
- Optionally export results as structured JSON

Comes with a simple **Tkinter GUI** for easy folder selection and output saving — no command line required.

Great for cleaning up legacy projects, reducing CSS bloat, improving page performance, or quickly understanding a new codebase.

## Features

- 🔍 Scans `.html`, `.css`, `.js` files (ignores `node_modules`, `.git`, etc.)
- 🧹 Detects **dead classes** and **dead IDs** (defined in CSS but unused)
- 📊 Shows top 10 most-used classes & IDs with usage counts
- 📝 Pulls descriptions from `/* comment */` placed immediately before selectors
- 🔗 Compound class detection (e.g. `.btn.btn-primary.active`)
- 📄 Generates rich Markdown report with file links and line numbers
- 💾 Optional JSON export for scripting / further analysis
- 🖥️ Simple desktop GUI built with Tkinter (no extra dependencies needed)

## Example output (Markdown excerpt)

```markdown
## 📊 Top 10 Most-Used Classes

- `.container` — 48 uses
- `.btn` — 37 uses
- `.text-center` — 29 uses
...

## 🧹 Dead Classes (Defined but Unused)

- `.old-banner`
- `.debug-grid`
...

## CSS Classes

### `.hero`

**Description:** Main landing page hero section with background image

**Used in HTML:**
- [index.html#L42](#L42)
- [about.html#L18](#L18)

**Used in CSS:**
- [styles/main.css#L120](#L120)
