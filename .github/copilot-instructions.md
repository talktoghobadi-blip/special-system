## Quick context

This repository is currently a minimal static project. At the time of writing it contains at least:

- `index.html` — root HTML file for the site
- `README.md` — short repo description

No build system (no `package.json`, `pyproject.toml`, `Makefile`, or CI workflows) or tests were found in the repository root.

## Goal for an AI coding agent

Be minimally invasive and evidence-driven: prefer small, well-documented changes. When adding new tooling or language ecosystems, create the associated manifest (example: `package.json` for Node) and update `README.md` describing how to build/run/test.

## What to read first

1. `index.html` — UI and static content lives here; small frontend changes should target this file.
2. `README.md` — any project-level notes or usage instructions should be kept here.

If you plan to add code in a new language or framework, list the new files added in your commit and update README with the required dev commands.

## Discovered repository patterns (explicit)

- Flat structure: top-level static files (no src/ or lib/ directories yet).
- No automated tests or CI detected in the current tree.

## How to be productive (explicit, actionable rules)

- Before making changes: search the repo for `package.json`, `pyproject.toml`, `Makefile`, or `.github/workflows/` to confirm whether to add tooling or integrate with existing CI.
- For HTML/CSS edits: keep changes scoped to `index.html` unless introducing assets; add new assets under an `assets/` or `static/` folder.
- When introducing JavaScript or Node tooling: add `package.json`, include `scripts` for `start`, `build`, and `test`, and document usage in `README.md`.
- When adding tests: prefer a top-level `tests/` folder and include one minimal test that demonstrates the expected behaviour. Document how to run tests in the README.

## Integration points & external deps

None discovered in the repository root. If you add external services (APIs, CDNs, or backend integrations), document required environment variables and request access details in `README.md`.

## Commit & PR guidance for the agent

- Keep commits focused and atomic (one feature/fix per branch).
- Include a short summary line and a few bullet points in the body explaining what changed and why.

## Examples (from this repo)

- To change the page title edit the `<title>` element in `/index.html`.
- To add a stylesheet, create `assets/styles.css` and link it from `/index.html`; add the asset folder to commits.

## If something is ambiguous

- Ask a human: open an issue or add a PR comment requesting product/acceptance criteria before making large structural changes.

---
If you want, I can (a) run a quick repo scan for any other hidden files, (b) create a small `README` expansion with common dev commands, or (c) add a starter `package.json`+`scripts` if you plan to use Node. Which would you like next?
