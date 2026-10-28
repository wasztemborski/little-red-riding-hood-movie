# Operations log

Append-only record of every operation on this vault. Newest entries at the
bottom. One entry per ingest, lint, or structural change.

Format:

```markdown
## YYYY-MM-DD — Short title

**Source**: what was read (files, submodules, symlinks)
**Changed**: pages created / updated / removed
**Notes**: anything surprising, contradictory, or left unresolved
```

---

## 2026-10-28 — Vault created

**Source**: n/a
**Changed**: initial folder structure scaffolded
**Notes**: entity folders created; no pages yet.

## 2026-10-28 — First ingest: Perrault's Czerwony Kapturek

**Source**: `00-inbox/story.md` (Polish text of Perrault's Little Red Riding Hood)
**Changed**: created 5 character pages (red-riding-hood, wolf, grandmother, mother, woodcutter), 3 place pages (forest, flower-meadow, grandmother-cottage), 1 decision page (leave-the-path); regenerated `index.md`
**Notes**: single source, no contradictions found. Story is the Perrault version (no harvesters/mother's second errand, ends with the moral about staying on the path). Pages written in English with Polish terms noted.
