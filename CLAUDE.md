# CLAUDE.md

Agent instructions for working on this repository.

## What this is

**Furtune.DEV** — the static developer documentation site for the Furtune API.
Hosted via GitHub Pages. No build step, no framework — pure HTML/CSS/JS.

The site documents the public-facing Furtune API for Guardian-tier users (Nova Keys, completions endpoint, etc).

## Structure

```
index.html        # Nova Keys & completions API reference (current entry point)
docs/             # Additional reference pages (one HTML file per topic)
CLAUDE.md         # This file
```

## Adding a new page

1. Create `docs/<topic>.html` — copy the shell from `index.html` (styles, nav, layout).
2. Add a nav link in every existing page's `<nav>` sidebar so pages stay in sync.
3. Update the sidebar nav section headers if the new page introduces a new category.

## Tone & voice

All prose uses **Nova's voice**: confident, precise, futuristic — but never at the cost of clarity.
- Personality lives in intros, callouts, and section openers.
- Reference tables, code blocks, and error codes stay clean and scannable.
- Never expose internal terms to users: no "agent", "model", "token", "tool" — use "cat", "engine", "Aimo", "ability".

See [Furtune CLAUDE.md](https://github.com/threehua/facai) for full brand & lore reference.

## Style rules

- Dark theme — do not add light-mode styles unless explicitly asked.
- No external dependencies (no CDN fonts, no JS frameworks). Everything is self-contained.
- Use the existing CSS custom properties (`--accent`, `--surface`, etc.) for any new styles.
- Code tabs use the existing `switchTab()` JS function — no new tab libraries.

## Deployment

GitHub Pages serves from the `main` branch root. Pushing to `main` deploys automatically.
Configure in repo Settings → Pages → Source: `main` / `/ (root)`.
