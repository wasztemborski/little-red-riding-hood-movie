# Ludd Movie — Second Brain

A personal knowledge base maintained by an AI coding agent, based on the
[LLM Wiki pattern](https://github.com/karpathy/llm-wiki).

## Quick start

1. **Clone the repo** (with submodules — sources live in submodules):

   ```bash
   git clone --recurse-submodules <repo-url>
   cd ludd-movie
   ```

2. **Create a `.env`** if any source needs credentials:

   ```bash
   echo 'MY_TOKEN=<value>' > .env
   ```

3. **Update the inbox**:

   ```bash
   git submodule update --init --recursive --remote
   ```

4. **Ingest into the wiki** — start your agent in this folder and ask:

   ```
   Ingest 00-inbox/ into the wiki
   ```

5. **Ask a question** — the agent reads `20-wiki/index.md`, synthesises an
   answer from the relevant pages, and cites its sources.

## Structure

```
00-inbox/     — source documents (immutable — never modify)
10-context/   — context and background information
20-wiki/      — structured knowledge (AI-maintained markdown pages)
50-templates/ — reusable document templates
workspace/    — scratch / working area (not a source for wiki output)
```

| Folder | Purpose |
| --- | --- |
| `00-inbox/` | Entry point for raw source material: symlinked local folders and Git submodules. Never modified once added. |
| `10-context/` | Stable background: goals, stakeholders, assumptions, environment. |
| `20-wiki/` | Evergreen pages curated by the agent, organised by entity type. |
| `50-templates/` | Reusable document templates. |
| `workspace/` | Scratch area — never used as a source for wiki output. |
| `AGENTS.md` | Instructions for the AI agent (ingest workflow, page format, citation rules). |

### `20-wiki/` organisation

Organised **by entity type** into folders — never collapsed into a flat directory:

| Path | Contents |
| --- | --- |
| `index.md` | Table of contents for the whole wiki, grouped by folder. |
| `log.md` | Append-only record of all operations. |
| `decision/` | Decision records with context and rationale. |
| `place/` | One page per place. |
| `century/` | One page per century. |
| `character/` | One page per character. |

Pages are interlinked with `[[wiki-links]]` that reference a page by its
filename only (without `.md`), regardless of folder.

## How it works

1. New sources go into `00-inbox/`.
2. The agent reads the source, discusses key takeaways, then creates/updates
   pages in `20-wiki/` — one file per entity, in the correct folder.
3. Pages are interlinked with `[[wiki-links]]` and follow a consistent format.
4. `20-wiki/index.md` and `20-wiki/log.md` are updated after every change.

## Key rules

- Never modify files in `00-inbox/`.
- Keep `20-wiki/` organised by entity type; one file per entity.
- Always update `20-wiki/index.md` and `20-wiki/log.md` after changes.
- Every factual claim must cite its source.
