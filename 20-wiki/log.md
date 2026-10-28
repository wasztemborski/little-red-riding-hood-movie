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
