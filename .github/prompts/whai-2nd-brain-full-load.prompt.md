---
description: >
  Full maintenance pass over this Second Brain vault: refresh 00-inbox/
  (submodules + symlinks), rebuild 20-wiki/ from whatever changed, then lint
  the result. Use this whenever sources may have moved on and the wiki needs
  to catch up in one go.
---

Act as a useful AI agent maintaining this Second Brain vault. Follow `AGENTS.md`
for the page format, ingest workflow, and lint rules. Do the following, in
order, and report what happened at each stage before moving to the next:

## 1. Refresh `00-inbox/`

- Pull the latest submodules:

  ```bash
  git submodule update --init --recursive --remote
  ```

- Verify every source resolves:

  ```bash
  .github/skills/whai-2nd-brain/scripts/link-source.sh --project . --verify-only
  ```

  If any entry comes back `BROKEN` or `EMPTY`, stop and tell me before
  continuing — rebuilding the wiki against a source that silently vanished
  just bakes the gap in as stale pages instead of catching it.

## 2. Rebuild `20-wiki/`

- Read every source in `00-inbox/` and the background in `10-context/`.
- Map the landscape first — list the entities you can see and their types —
  and show me that map before writing anything, so I can catch a
  miscategorised entity early.
- Write or update one page per entity, in the correct entity folder, following
  `assets/wiki-page.md.tmpl`'s structure (Summary, Sources, Last updated, then
  content with `[[wiki-links]]`).
- Prefer updating existing pages over creating duplicates — check `index.md`
  for an entity before assuming it's new.
- Regenerate `20-wiki/index.md`, grouped by entity folder.
- Append one dated entry to `20-wiki/log.md` summarising what changed and why.

## 3. Lint

Run the lint checks `AGENTS.md` defines and report the results as a numbered
list with suggested fixes:

- Zero broken `[[wiki-links]]`
- Zero orphan pages (no inbound links)
- Every page follows the standard page format
- Every factual claim carries a source citation
- Concepts mentioned repeatedly but lacking their own page
- Claims that look outdated given what just arrived in `00-inbox/`

Finish with a short summary: what was refreshed, what was written or updated,
and what the lint pass found.
