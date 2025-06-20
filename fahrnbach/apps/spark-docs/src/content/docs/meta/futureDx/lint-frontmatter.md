---
title: "Lint Frontmatter Quote Consistency"
description: "DX idea: Lint Frontmatter Quote Consistency."
tags: [meta, sidebar, DX, devtools, lint]
---

## 🛠️ Future DX: Lint Frontmatter Quote Consistency

We’ve run into YAML parsing errors when using **single quotes** (`'`) in frontmatter values — particularly when those strings also contain apostrophes (e.g., `description: 'Jacob's blog post'`). YAML interprets this as a malformed mapping.

To avoid this, we’ve adopted a **best practice** of always using **double quotes** (`"`) around frontmatter values. This allows us to safely include apostrophes within strings without breaking the frontmatter.

### 🚧 TODO: Frontmatter Lint Rule

Eventually, we want to **automatically enforce** this quoting rule across all `.md`/`.mdx` content files. Options include:

- ✅ **Build a custom lint rule** using [`remark-lint`](https://github.com/remarkjs/remark-lint) and [`remark-frontmatter`](https://github.com/remarkjs/remark-frontmatter`)
  - Pros: Integrates directly into our content pipeline, can be run in CI
  - Cons: Requires writing a plugin that parses and validates YAML nodes

- ✅ **Write a standalone script** that scans frontmatter blocks and flags:
  - Any single-quoted (`'`) values
  - Any unquoted values (barewords)
  - Optionally, values missing quotes altogether

- ✅ Optionally integrate into a `pre-commit` hook using [`lint-staged`](https://github.com/okonet/lint-staged)

```bash
# Example: Pre-commit hook
pnpm lint:frontmatter
```
This will help us avoid subtle formatting bugs and ensure our markdown is always safe and predictable — especially as the number of contributors grows.