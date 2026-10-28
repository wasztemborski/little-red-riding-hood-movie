# Ludd Movie — LLM Wiki

A personal knowledge base maintained by an AI coding agent, based on Andrej
Karpathy's LLM Wiki pattern.

## Purpose

You are my operating-system assistant. Help me run my work through this vault.
Be proactive, check your own work before showing it to me, and always cite the
notes you used.

The agent maintains the wiki. The human curates sources, asks questions, and
guides the analysis.

## Folder structure

```
00-inbox/     -- source documents (immutable -- never modify)
10-context/   -- context and background information
20-wiki/      -- pages maintained by the agent, organised BY ENTITY TYPE
50-templates/ -- reusable document templates
workspace/    -- scratch; never a source for wiki output
```

`20-wiki/` is split into one folder per entity type. This layout is required —
do not put entity pages back into a flat directory:

```
20-wiki/
  index.md   -- table of contents for the entire wiki (grouped by folder)
  log.md     -- append-only record of all operations
  decision/    -- Decision records with context and rationale.
  place/       -- One page per place.
  century/     -- One page per century.
  character/   -- One page per character.
```

Wiki-links `[[page-name]]` reference a page by its **filename only** (without
`.md`), regardless of which folder it lives in — so pages may be moved between
folders without breaking links, provided basenames stay unique.

## Sources in `00-inbox/`

Sources arrive two ways:

- **Symlinks** to local folders (cloud storage, other projects). The target is
  owned by something outside this vault; treat it as read-only.
- **Git submodules** for remote repositories. Refresh with
  `git submodule update --init --recursive --remote`.

If a symlink dangles or a submodule is empty, say so rather than silently
ingesting nothing.

## Ingest workflow

When the user adds sources to `00-inbox/` and asks you to build or update the wiki:

1. Read the relevant source markdown; include `10-context/` as background.
2. For a large batch, map the landscape first (entities, types, owners) before
   writing anything, and show that map to the user.
3. Write pages **by entity**, into the correct folder, one file per entity.
4. Link entities to each other with `[[wiki-links]]`.
5. Update `20-wiki/index.md`, grouped by folder.
6. Append an entry to `20-wiki/log.md` with the date, source, and what changed.
7. Lint before finishing: 0 broken wiki-links, 0 orphan pages.

A single source batch may touch many pages across several entity folders. That
is normal.

## Page format

```markdown
# Page Title

**Summary**: One to two sentences describing this page.

**Sources**: List of raw source files this page draws from.

**Last updated**: YYYY-MM-DD

---

Main content. Clear headings, short paragraphs.

Link to related entities using [[wiki-links]] throughout the text.

## Related pages

- [[related-page-1]]
- [[related-page-2]]
```

## Citation rules

- Every factual claim references its source file.
- Use the format `(source: filename.pdf)` after the claim.
- If two sources disagree, note the contradiction explicitly.
- If a claim has no source, mark it as needing verification.

## Question answering

1. Read `20-wiki/index.md` first to find relevant pages.
2. Read those pages and synthesise an answer.
3. Cite specific wiki pages in your response.
4. If the answer is not in the wiki, say so clearly.
5. If the answer is valuable, offer to save it as a new wiki page.

Good answers should be filed back into the wiki so they compound over time.

## Lint

When asked to lint or audit the wiki:

- Check for contradictions between pages.
- Find orphan pages (no inbound links).
- Identify concepts mentioned in pages that lack their own page.
- Flag claims that may be outdated based on newer sources.
- Check that all pages follow the page format above.
- Report findings as a numbered list with suggested fixes.

## Rules

- Never modify anything in `00-inbox/`.
- Organise `20-wiki/` by entity type into folders. Never collapse them.
- One file per entity. Aggregate related raw items into the relevant entity page.
- Record relationships explicitly: each page names its owner(s) and links out.
- Always update `20-wiki/index.md` and `20-wiki/log.md` after changes.
- Don't use `workspace/` as a source for generated output.
- Keep page names lowercase with hyphens (e.g. `machine-learning.md`).
- Write in clear, plain language; cite sources.
- When uncertain how to categorise something, ask the user.
