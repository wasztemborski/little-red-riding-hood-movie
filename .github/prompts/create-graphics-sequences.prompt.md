# Create storybook illustration prompts for a Sequence (AI prompt)

Purpose

Generate a `graphics-sequence-N.md` file containing one self-contained storybook **illustration prompt** for every scene in a given sequence. The prompts must be ready to paste directly into an image generator.

Inputs (fill these in when running)

# Instructions

1. Analyze `production/storybook/B-story-structure.md` to identify the sequences and their scene ranges.
2. Propose granularity level basd on hierachy: **BOOK → PARTS → SECTIONS → CHAPTERS → SEQUENCES**) and ask user for confirmation. The  storyboard with generate, up to to keep 6 images per storyboard for that selection. 1 image per scene on one storyboard image
3. Save output into `production/sequences/graphics-sequence-N.md` (N = sequence number).

## Guidelines

- 
- Follow the `production/storybook` project's style and formatting conventions.
- Path: `production/sequences/graphics-sequence-N.md` (N = sequence number).
- Language: English. Markdown only. No commentary outside the file structure below.
- Exactly one prompt per scene in the range — no more, no fewer.
- Each blockquote must be self-contained (end with the full style suffix) so it works standalone.
- Keep descriptions faithful to the storyboard's Image/Camera notes; do not invent contradicting content.
- Resolution Aspect 16:9 for each image in storyboard
- Storyboard is organized as a set of equally distributed images in a grid

## format

```md
1. **H1 title:** 
2. **Intro line:** "Storybook illustration prompts, one per scene. Each prompt is self-contained and carries the full style so it can be pasted directly into an image generator."
3. **Global style suffix block (bold label + italics):**
   *hand-painted watercolor and gouache, Scandinavian storybook illustration, pastel palette, soft diffuse light, rounded organic shapes, delicate paper texture, gentle depth, melancholic and warm mood, no photorealism, no sharp contours, no neon, no chrome, no plastic. Aspect 16:9.*
4. **Context line(s)** relevant to the sequence: the correct **palette + light** for the location(s), plus any **character consistency** note needed (see below).
5. `---` divider.
6. One block **per scene**, in order:
   - `## S0XX — <scene-slug>` (use the storyboard's scene slug)
   - A single blockquote `>` paragraph: a vivid scene description **followed by the full global style suffix appended inline** (so each prompt stands alone).
```
