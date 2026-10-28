# Graphics Sequences Overview

**Created**: 2026-10-29  
**Project**: THE RED CAP (Little Red Riding Hood movie storybook)  
**Format**: Storybook illustration prompts for image generation

---

## Granularity Decision

The storybook is organized as follows:

| Level | Count | Usage |
|-------|-------|-------|
| **Parts** | 4 | Major narrative division (Errand, Off the Path, Cottage, Forester) |
| **Sequences** | 12 | Groups of related scenes |
| **Scenes** | 34+ | Individual cinematic moments |

**Chosen granularity for graphics sequences**: **Sequences** (groups of 6 related scenes per storyboard image set)

This breaks the film into 6 illustration sets, each containing 4–7 prompts per sequence, allowing:
- 1 storyboard image per scene (or per moment)
- Contextual grouping that maintains narrative flow
- Manageable scope for image generation (4–7 images per graphics file)
- Clear thematic/spatial coherence within each sequence

---

## Sequence Breakdown

### Part I — The Errand (5 scenes)
- **graphics-sequence-01.md**: Introduces home, rule, departure
- Scenes: 1.1.1.1.1–1.1.1.2.3
- Key themes: Warm family cottage, promise-making, the gate as first threshold
- Palette: Yellow ochre, warm light, the red cap as sole saturation

### Part II — Off the Path (7 scenes)
- **graphics-sequence-02.md**: The temptation and the wolf
- Scenes: 2.1.1.1.1–2.2.2.1.2
- Key themes: Path discipline vs. meadow beauty, reasoning, the drift, predator arrival
- Palette: Progression from friendly birch → shadowed columnar trunks → hazy meadow → disorientation → wolf
- Character: Introduction of both path-rule (visual grammar) and wolf (politeness masking predation)

### Part III — The Cottage (8 scenes)
- **graphics-sequence-03.md** (Section 1): Wolf's planning and execution
  - Scenes: 3.1.1.1.1–3.1.2.2.2
  - Themes: Politeness wins trust, information volunteered, grandmother in danger, disguise
  - Wolf character locked: grey-brown, polite, sly, efficient
  
- **graphics-sequence-04.md** (Section 2): Climax — the three questions and leap
  - Scenes: 3.2.1.1.1–3.2.2.2.2
  - Themes: Arrival, unease, naming the truth, the leap, predator undone by sleep
  - Light: Dim backlit interior where disguise works until it doesn't
  - Character consistency: Girl notices everything; wolf is exhausted by his satisfaction

### Part IV — The Forester & Return (6 scenes)
- **graphics-sequence-05.md**: Rescue
  - Scenes: 4.1.1.1.1–4.1.2.1.3
  - Themes: Ordinary attentiveness (forester notices what is wrong), decisive action, restoration
  - Palette: Late afternoon moving to dusk, golden light
  - Introduces forester character (who was planted in background of 2.1.1.1.2)
  
- **graphics-sequence-06.md**: Return home
  - Scenes: 4.2.1.1.1–4.2.2.1.2
  - Themes: Task completion, choice, the path now freely chosen, safety at home, the coda
  - Palette: Deep golden dusk transitioning to blue evening, warmth of lit cottage
  - Closing image: Child and mother at threshold, hand in hand, the forest now seen clearly

---

## Style Consistency Across All Sequences

**Global style suffix** (all prompts end with):
*Hand-painted watercolor and gouache, Scandinavian storybook illustration, pastel palette, soft diffuse light, rounded organic shapes, delicate paper texture, gentle depth, melancholic and warm mood, no photorealism, no sharp contours, no neon, no chrome, no plastic. Aspect 16:9.*

**Character consistency notes**:
- **Red Riding Hood**: Red cap tied under chin (never removed until cottage), pale linen dress, dark pinafore, red thread continuity, grass stains from meadow (2.2.1.2.1 onward), damp hem from stream (2.1.1.1.2 onward), touches knot of cap when uncertain
- **The Wolf**: Grey-brown, bulky, polite register, sly smile when alone, dressed in grandmother's nightcap and spectacles (sits wrong), enormous teeth, snores
- **The Forester**: Man in green-brown coat, axe, moves through forest with attentiveness, planted in background of scene 2.1.1.1.2 (unremarked), essential in Part IV
- **Mother**: Warm, hesitant, careful with instruction and medicine
- **Grandmother**: Elderly, kind, collected, grateful

**Location consistency notes**:
- **Family Cottage (L1)**: Yellow ochre, worn timber, cluttered but orderly, dawn-lit at start, lamplit at dusk
- **The Path (L2)**: Pale ribbon of packed earth, continuous vanishing point, visible while on path (2.1.1), absent from 2.2.1.1.1 through 4.2.2.1.0, returns in 4.2.2.1.1
- **The Forest (L3)**: Three registers — near (birch, friendly), middle (columnar, quiet), deep (enormous trunks, no horizon). Becomes less friendly across Part II
- **The Meadow (L4)**: Blown-out warm light, haze, shallow focus, painterly, no clear far edge, visible but untaken in coda (4.2.2.1.1)
- **Grandmother's Cottage (L5)**: Dim, backlit from one window and open door, dried flowers on shelves, bed against back wall facing door, the staging reason the girl cannot tell

---

## Usage Instructions

1. Each `.md` file is self-contained and ready for image generation
2. Paste each blockquote `>` prompt directly into your image generator
3. Each prompt carries the full style suffix, so it works standalone
4. Prompts follow the storyboard's cinematic blocking and lighting notes
5. Use the "Character consistency" and "Palette & Light" sections as reference for maintaining style across sequences
6. All prompts maintain Aspect ratio 16:9 as specified

---

## Total Scene Count

- Part I: 6 scenes (graphics-sequence-01)
- Part II: 8 scenes (graphics-sequence-02)
- Part III Section 1: 7 scenes (graphics-sequence-03)
- Part III Section 2: 8 scenes (graphics-sequence-04)
- Part IV (Rescue): 5 scenes (graphics-sequence-05)
- Part IV (Return): 4 scenes (graphics-sequence-06)

**Total: 38 illustration prompts across 6 sequence files**
