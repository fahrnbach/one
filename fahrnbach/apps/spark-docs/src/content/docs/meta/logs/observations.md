---
title: "Observations Log"
description: "A log of 'One-Liner' Observations for any Quirks, Issues, Errors etc we've run into along the way."
tags: [meta, sidebar, DX, devtools, starlight]
---

## 🔍 Observations Log
<div style="padding: 0 1rem; border-left: 4px solid #ccc; background-color: #202020;">

- **Folder naming matters**  
  Folder names under `/src/content/docs/` must be **lowercase** for sidebar routing to work (e.g. `futuredx`, not `futureDX`).  
  Astro/Starlight may lowercase slugs automatically — casing mismatches can break routing.

- **Sidebar & `_category_.json` behavior**  
  `_category_.json` **is ignored** at the top level if `sidebar.mjs` is active.  
  You **cannot override top-level group names** using `_category_.json` — use `sidebar.mjs` for that.  
  Subfolder `_category_.json` files **do work**, and can control local section order and labels — but only if `sidebar.mjs` is removed.  
  A **hybrid strategy** works best: use `sidebar.mjs` for high-level layout, `_category_.json` or frontmatter `title/place` for subfolder organization.  
  After updating `sidebar.mjs`, you must **restart the dev server** for changes to apply.

- **Frontmatter YAML quirks**  
  Use **double quotes (`"`)** for all frontmatter values to avoid YAML parsing errors, especially if the value contains apostrophes.  
  Bad indentation in frontmatter (e.g., mixed tabs/spaces) can result in cryptic errors like `bad indentation of a mapping entry`.

- **Astro behavior**  
  Astro auto-generates an **Overview section** in the ToC based on `##` headings — not file names or frontmatter.  
  `getStaticPaths()` router warnings can occur if slugs are misnamed, renamed, or improperly cased in sidebar/frontmatter.

- **Monorepo configs**  
  Use `.mjs` instead of `.ts` for config files in monorepos to avoid Node/ESM compatibility issues.

</div>

> ✨ Add these logs incrementally as you go — they’re a lifesaver for future debugging or onboarding contributors.