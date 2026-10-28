---
mode: agent
description: Generate a consistent  character reference sheet for any character character bible.
---
# Create Character Reference Sheet

Generate a consistent character turnaround / reference sheet for a character in character bible. Keep proportions, palette constant across every generation.

---

## Instructions (follow these steps)

1. **List all characters** from `workspace/output/storybook/document-c-character-bible.md`.
2. **Ask the user to select one** of the listed characters. Wait for their answer before continuing.
3. **Save the character reference sheet** into `./workspace/output/characters/` following the naming convention `{character-name}-reference-sheet.md` (lowercase, hyphenated).

---

## Reference Sheet Template

Fill this template using the selected character's details from `workspace/output/storybook/document-c-character-bible.md`. Replace the bracketed placeholders.

### Master Prompt

> Character reference sheet of **{character name}**, {build and posture}, head-to-body ratio {ratio}. {Hair}. {Face}. Wardrobe: {wardrobe}. Palette: {palette}.
>
> **Sheet layout:** full-body turnaround on a plain warm-paper background — **front · 3/4 front · profile · 3/4 back · back** — all at identical height on a shared ground line, consistent proportions across every view. Include a small **expression row** ({expression key}) and a **hands / signature gesture** inset ({signature gestures}).
>
> **Style:**: photorealism, delicate paper texture, gentle depth, melancholic and warm mood. No sharp contours, no neon, no chrome, no plastic. Even reference-sheet lighting, neutral pose, model-sheet clarity.

### Consistency Rules (must always hold)

- {Character-specific consistency rules from the character list.}
- Constant palette across every view.
- Keep proportions consistent across every view.
- Make character photorealism.

### Negative Prompt

> hard ink outlines, neon, chrome, plastic sheen, jewelry, heavy makeup, exaggerated expression, harsh shadows, busy background, 3D render, anime, glossy highlights.

### Suggested Settings

- **Aspect:** 3:2 or 16:9 (wide, to fit the full turnaround row).
