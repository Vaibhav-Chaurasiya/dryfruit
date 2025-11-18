<!-- .github/copilot-instructions.md - Project-specific guidance for AI coding agents -->

# Copilot / AI Agent Instructions for the `dryfruit` repo

Purpose: provide concise, actionable guidance so an AI coding agent can be immediately productive in this repository.

**Quick repo snapshot**
- Root contents: `index.html` (single static HTML file). No build system, no package manifests, no source folders.
- Git repo present (`.git/`). Default branch: `main`.

**Big picture (discoverable)**
- This is a minimal static site: one standalone page `index.html`. There are no backend services, no bundlers, and no tests to run or CI configuration to infer.
- Any structural decisions must be motivated by this simplicity — adding frameworks or build tooling requires explicit user approval.

**When making changes**
- Prefer small, focused edits to `index.html`. Keep modifications minimal and explain the user-visible impact.
- Do NOT introduce new top-level build tools (npm, webpack, etc.) unless the user explicitly asks.
- If adding assets (images, CSS, JS), place them under a new `assets/` or `static/` folder and update paths in `index.html`.

**Developer workflows (what an agent can run / assume)**
- There are no build or test commands discoverable in this repo. Treat edits as direct file updates.
- Use standard Git commands for changes: create branches, commit with clear messages, and open PRs if requested.

**Patterns & conventions (repo-specific)**
- Single-file site: favor in-place edits over splitting code into many files unless requested.
- Keep accessibility and small file size in mind — this repo looks intended for a small static page.

**Integration points / external dependencies**
- None discoverable. If an integration (CDN, analytics, payment, APIs) is required, ask the user for credentials, endpoints, and where to store configuration.

**Examples from this repo**
- To change the visible page title, edit the `<title>` element inside `index.html`.
- To add a stylesheet, create `assets/styles.css` and add `<link rel="stylesheet" href="assets/styles.css">` in `index.html`.

**AI-agent behavior rules (do not assume or do without consent)**
- Do not scaffold languages, frameworks, or CI pipelines without explicit user approval.
- Prioritize edits that preserve the current file layout and formatting.
- When a feature request would add new files or infrastructure (build, CI, DB, server), create a short plan and ask for confirmation before applying changes.

If anything in this file is unclear or you want the agent to follow alternate conventions (for example: split CSS/JS into separate files, introduce a build step, or add automated deployments), please tell me which direction to take.
