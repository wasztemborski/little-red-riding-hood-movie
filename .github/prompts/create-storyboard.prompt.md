# Create storybook illustration prompts for a Sequence (AI prompt)

Purpose

Generate a storyboard file markdown for a sequence in the storybook, based on the source material and the specified style. Each scene in the sequence will have a corresponding illustration prompt, formatted for use with an image generator.


# Instructions

1. Analyze `production/storybook/B-story-structure.md` to identify the sequences and their scene ranges.
2. Propose granularity level basd on hierachy: **BOOK → PARTS → SECTIONS → CHAPTERS → SEQUENCES**) and ask user for confirmation. The storyboard with generate, up to to keep 6 images per storyboard for that selection. 1 image per scene on one storyboard image
3. Save output into `production/storyboard.md`.

## Guidelines

- Follow the `production/storybook` project's style and formatting conventions.
- Each scene entry **must include all fields** from the example template below, even if field is empty or marked N/A.
- Extract and populate the following fields explicitly for each scene:
  - **Scene ID & Title** (from story structure)
  - **Timecode/Runtime** (from story structure)
  - **Image description** (from location bible + character continuity notes)
  - **Camera direction** (from cinematic storybook, Document E)
  - **Aspect ratio** (always 16:9)
  - **Character animation notes** (poses, expressions, continuity marks)
  - **Narration** (if applicable to sequence)
  - **Dialogue** (character names and exact lines)
  - **Sound effects** (SFX, ambient, music cues)
  - **Illustration prompt** (ready for AI image generator, includes full style suffix)
  - **Animation prompt** (timing, motion, technical notes)

## Format

Example template for one scene entry:

```md 

## SEQUENCE I — CITY OF ANSWERS (S001–S010)

### S001_City_dawn · 0:00–0:10

- **Scene ID:** 1.1.1.1.1
- **Title:** Cold Open: A Spot of Red
- **Runtime:** 1:30
- **Image:** Aerial over misty valley; folded-paper roofs of a town emerge among trees.
- **Camera:** Slow high drift forward.
- **Aspect:** 16:9
- **Char. anim.:** None; drifting mist, faint smoke from chimneys.
- **Narration:** *W pewnym mieście wszyscy nosili zegarki, ale nikt nie miał czasu.*
- **Dialogue:** Character 1: "Wszyscy spieszą się, ale nikt nie wie dokąd."
- **SFX:** Soft wind, faint layered ticking rising.
- **Illustration prompt:** Watercolor Scandinavian storybook valley at dawn, misty blue town of folded-paper roofs among trees, soft diffuse light, rounded shapes, no sharp contours.
- **Animation prompt:** 10s slow aerial push forward, drifting mist, subtle chimney smoke, gentle parallax.

```
