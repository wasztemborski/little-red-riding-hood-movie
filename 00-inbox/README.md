# 00-inbox — Sources

Raw source material. **Immutable** — never edit anything here; the vault treats
this folder as the record of what was actually received.

Sources arrive two ways:

- **Symlinks** to local folders (cloud storage, sibling projects). The link name
  is a kebab-cased alias; the target lives outside this repo.
- **Git submodules** for remote repositories. Refresh them with:

  ```bash
  git submodule update --init --recursive --remote
  ```

Everything here is read by the agent and distilled into `20-wiki/`.
