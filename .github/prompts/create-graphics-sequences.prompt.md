# Create storybook illustration prompts for a Sequence (AI prompt)

Purpose

Generate a `graphics-sequence-N.md` file containing one self-contained storybook **illustration prompt** for every scene in a given sequence, matching the exact format of the existing `workspace/output/graphics-sequence-1.md`. The prompts must be ready to paste directly into an image generator.

Inputs (fill these in when running)

- **Sequence number & title** — e.g. `SEQUENCE II — QUESTIONS`.
- **Scene range** — e.g. `S011–S018`.
- **Source of truth** — read the matching scenes in `workspace/output/storyboard.md` (fields: Image, Camera, Char. anim., Narration, SFX, illustration prompt) and honor the bibles: `world-description.md`, `character-list.md`.

Reference sequences and ranges

- Sequence I — City of Answers (S001–S010)
- Sequence II — Questions (S011–S018)
- Sequence III — Klara / Answer Office (S019–S028)
- Sequence IV — The Question Swells (S029–S038)
- Sequence V — The Three Offices (S039–S050)
- Sequence VI — Sitting With It & Return (S051–S060)

Output file

- Path: `workspace/output/graphics-sequence-N.md` (N = sequence number).
- Language: English. Markdown only. No commentary outside the file structure below.

Required file structure (match `graphics-sequence-1.md` exactly)

1. **H1 title:** `# KLARA & THE QUESTION — Illustration Prompts: <SEQUENCE TITLE> (<range>)`
2. **Intro line:** "Storybook illustration prompts, one per scene. Each prompt is self-contained and carries the full style so it can be pasted directly into an image generator."
3. **Global style suffix block (bold label + italics):**
   *hand-painted watercolor and gouache, Scandinavian storybook illustration, pastel palette, soft diffuse light, rounded organic shapes, delicate paper texture, gentle depth, melancholic and warm mood, no photorealism, no sharp contours, no neon, no chrome, no plastic. Aspect 16:9.*
4. **Context line(s)** relevant to the sequence: the correct **palette + light** for the location(s), plus any **character consistency** note needed (see below).
5. `---` divider.
6. One block **per scene**, in order:
   - `## S0XX — <shortslug>` (use the storyboard's scene slug)
   - A single blockquote `>` paragraph: a vivid scene description **followed by the full global style suffix appended inline** (so each prompt stands alone).

Palettes & light (use the right one per scene)

- **City:** misty blue · stone grey · pale olive · wood beige — cool, diffuse light.
- **Office:** cream · paper · brass · light oak — even, controlled light.
- **Home:** amber · honey · linen · warm white — soft golden light.
- **Anxiety Workshop:** clinical white · pale grey · faint brass — cold even light.
- **Trainer's room:** bright cream + muted light-blue accent — airy light.
- **Office of Prediction:** dark/dim + soft amber blinking machine lights (never neon).
- **Crisis/swelling scenes:** slightly more contrast with soft shadows.

Character consistency (include when characters appear)

- **Klara:** calm adult woman, ash-brown hair loosely tied, cream blouse + muted olive cardigan, exactly **one brass wristwatch**; emotes through breath, hands, gaze, pace — never exaggerated mimicry.
- **The Question:** grey soft fur, **mismatched ears (one up, one folded)**, big listening eyes, **tail like an unfinished sentence**; swelling is smooth and balloon-like, never violent; identity constant across all states.
- **Answers:** deliberately **too-finished and glossy**, fur of tidy declarative sentences, tails of neat conclusions; **Service Answers** have engraved brass collars (Wdrożono / Zamknięto / Zoptymalizowano / Brak dalszych działań).

Rules

- Exactly one prompt per scene in the range — no more, no fewer.
- Each blockquote must be self-contained (end with the full style suffix) so it works standalone.
- Keep descriptions faithful to the storyboard's Image/Camera notes; do not invent contradicting content.
- Do not include animation prompts here (those live in `animation-sequence-N.md`).

Example invocation

> Create storybook graphics for SEQUENCE II — QUESTIONS (S011–S018). Add one illustration prompt for each scene in the range, following the established style guidelines, and save to `workspace/output/graphics-sequence-2.md`.

Companion prompts

- After generating illustration prompts, optionally generate the matching `animation-sequence-N.md` (one motion prompt per scene) using the same scene range and the calm-camera motion style.