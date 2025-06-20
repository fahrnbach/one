---
title: "Sidebar Sync & Editor Devtool"
description: "DX idea: detect missing docs in the sidebar or manage them visually in dev mode."
tags: [meta, sidebar, DX, devtools, starlight]
---

## 🛠 Sidebar Sync & Editor Devtool (Future Feature)

> “Don’t fear the chaos — automate the order.”

### 🧭 Sidebar Check Utility
Create a small CLI script to scan `src/content/docs` and compare it against `sidebar.mjs`.

**Features:**
- Recursively list `.md` and `.mdx` files
- Compare with paths in `sidebar.mjs`
- Print out any missing or orphaned entries

**Prompt to build this:**
> “Write a Node.js script that walks `src/content/docs`, extracts valid doc paths, compares them to entries in `sidebar.mjs`, and logs any that are missing. Highlight orphaned files too.”

---

### 🧪 Sidebar Editor Devtool

In dev mode, spin up an internal page at `/dev/sidebar` with:

- A tree-view of `src/content/docs`
- Checkboxes for each file and folder
- Auto-save to `sidebar.mjs`
- (Optional) Live preview sidebar reload

**Prompt to build this:**
> “Create a local-only admin route `/dev/sidebar` in Astro that renders a tree-view of all markdown files in `src/content/docs`, and lets you check/uncheck which files appear in the sidebar. On save, rewrite `sidebar.mjs` to reflect changes.”

---

## 🌱 Status
- [ ] CLI Sidebar Sync Tool
- [ ] Sidebar Editor UI Devtool

## 🧘‍♂️ Impact
This is one of those tools that pays off *every time* you add a doc. Cleaner process, fewer forgotten pages, better DX.
