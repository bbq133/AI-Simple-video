---
name: ai-knowledge-sketch-video
description: Use this skill when the user asks to create or refine a vertical AI/product knowledge explainer in a fresh sketch, paper-cut, doodle, or light educational style; requests 9:16 knowledge cards, narration-synced component reveals, logical card transitions, natural Chinese female voice-over, mobile-friendly previews, or asks to update the workflow after feedback.
version: 1.0.0
---

# AI Knowledge Sketch Video

Turn an AI/product knowledge topic into a clear, attractive 9:16 sketch explainer whose visual focus moves with the narration. Deliver a reproducible project, not only prompts.

Resolve `<SKILL_DIR>` to this folder. Keep project assets outside the skill folder.

## Required outcome

1. Approved spoken script and scene-to-line map.
2. Locked 9:16 visual system.
3. Finished keyframes with balanced final compositions.
4. Separately animatable scene components.
5. Narration-driven component timing.
6. Logical, gentle transitions.
7. Natural Chinese narration with verified terminology.
8. Valid H.264/AAC MP4 plus lightweight chat previews.
9. Feedback rules appended to this skill when the user refines the workflow.

## Default visual direction

Use **清新剪纸简笔** unless the user selects another direction:

- warm ivory paper field with subtle texture;
- charcoal sketch lines;
- pale mint atmosphere;
- coral-red focus accents;
- paper modules with restrained shadows;
- one round-headed guide character;
- short, large Chinese text;
- clear component spacing for later animation.

Avoid purple-neon AI clichés, dark dashboards, generic corporate MG, glossy 3D, dense walls of cards, and decorative clutter.

## Hard gates

### Gate 1 — research before style claims

If the user asks for popular/high-engagement styles, compare at least 10 relevant market styles and distinguish sourced observations from assumptions. Extract interaction mechanisms, not copied artwork.

### Gate 2 — script approval before voice

Present the complete scene script and spoken lines. Do not generate or write narration into the video until the user explicitly approves it.

### Gate 3 — one style anchor before a full set

Generate 2–4 distinct style samples using the same knowledge point. After selection, lock the palette, line, shadow, character, type hierarchy, and spacing.

### Gate 4 — end-frame composition check

Before animation, inspect every fully assembled frame at mobile size. Reject frames with:

- large meaningless blank areas;
- all content compressed into one corner;
- a caption stranded at the bottom;
- weak visual center or no clear reading path;
- components touching edges or overlapping;
- small text that becomes unreadable at 360 px preview width.

Negative space is allowed only when it directs attention or reserves a deliberate motion path. It must not look unfinished.

## Production workflow

### 1. Lock the brief

Define topic, audience, platform, aspect ratio, target duration, teaching goal, required facts, CTA, and pronunciation glossary.

Default to 9:16 for short-form feeds. Use 3:4 only for a static carousel explicitly targeting that format.

### 2. Write the knowledge arc

Use a five-beat structure when appropriate:

1. Hook: a concrete question or misconception.
2. Myth: show the wrong mental model.
3. Structure: reveal the correct sequence.
4. Experience: demonstrate the principle.
5. Takeaway: leave one memorable sentence.

Each scene carries one idea. Transition cards must advance logic: `question → correction → structure → application → takeaway`.

### 3. Design for animation from the start

Do not animate a flattened keyframe as one object when the user expects focus guidance.

For every scene define:

- background field;
- scene label;
- character;
- individual keywords/cards/icons;
- connector/arrow;
- final summary;
- their narration cue and entrance order.

Use real HTML/SVG/transparent PNG layers. Keep each component independent and leave motion-safe spacing around it.

### 4. Reveal components with the narration

The settled frame is the destination, not the first frame.

Example opening:

`01 label → character + question mark → AI → 大模型 → 风口 → summary`

Map every reveal to a spoken phrase. Use 0.35–0.55 s paper-settle entrances. Show only the elements needed for the current phrase. Hold the completed scene long enough to understand it.

Do not add duplicate overlay chips on top of already flattened keyframe content; this causes obstruction.

### 5. Transition logically and gently

Default transition:

`completed scene → 0.7–1.0 s fade out → centered bridge card → 0.7–1.0 s fade in`

Do not use fast page flips, abrupt lateral slides, or simultaneous cross-screen motion unless the story requires it.

Bridge hierarchy:

1. small stage kicker, e.g. `02 → 03 拆解`;
2. large focus sentence with one coral keyword;
3. optional quiet next-page hint.

Never place a tiny bridge caption at the bottom edge.

### 6. Narration

Read `references/narration.md`.

Generate one voice file per main scene and bridge. Measure actual durations, then derive picture timing from speech:

`scene duration = fade-in + spoken duration + 0.7–1.2 s tail + fade-out`

Use normal conversational pauses. Avoid slow broadcast cadence, exaggerated emotion, and mechanical punctuation.

Maintain a pronunciation glossary. In this project:

- on-screen `AI` is allowed;
- spoken `AI` defaults to **“人工智能”**, not letter-by-letter `A-I`, unless the user explicitly chooses otherwise.

Offer a short first-line sample before a costly full rerender when changing voices.

### 7. Visual quality control

At minimum inspect:

- early, middle, and settled frame of every scene;
- midpoint of every transition;
- final contact sheet at 360 px card width;
- the last completed frame for visual balance and blank-space quality.

Read `references/qc-checklist.md`.

### 8. Render and preview

Render H.264 video and AAC audio. Verify dimensions, duration, frame count, full video/audio coverage, and decoding of first/last frames.

For mobile/chat preview:

- MP4: `-movflags +faststart`, H.264 Main/Baseline, yuv420p, no B-frames when maximum compatibility is needed;
- JPEG: 540 px wide, roughly 30–80 KB;
- GIF: 320–360 px wide, reduced palette;
- always provide a progressive reveal strip when video preview is unreliable.

Never rely on a large GitHub MP4 as the only review method.

## Feedback-driven skill maintenance

When the user corrects the workflow or quality bar:

1. apply the correction to the current deliverable;
2. decide whether it is reusable beyond the current scene;
3. if reusable, update `references/learned-rules.md`;
4. update the relevant rule in this `SKILL.md` if it changes a hard gate or default;
5. append a dated entry to `CHANGELOG.md`;
6. keep the user's exact intent, but generalize away project-specific filenames;
7. never weaken an earlier accepted rule without explicit user direction.

At the start of every task using this skill, read `references/learned-rules.md`.

## Delivery layout

```text
project/
  brief.md
  script.md
  STYLE_LOCK.md
  manifests/
    storyboard.json
    voice-durations.json
    sync-timeline.json
  assets/
    keyframes/
    layers/
    voice-final/
    audio/
  renders/
    scenes/
    final.mp4
    preview.mp4
    preview.gif
    contact-sheet.jpg
    progressive-reveal.jpg
```

## Final acceptance

- Understandable without audio.
- Spoken script matches the visual reveal order.
- One focus at a time.
- No obscured components.
- No meaningless end-frame whitespace.
- No tiny transition captions.
- No fast/uncomfortable page turns.
- Chinese terminology is pronounced correctly.
- Preview opens quickly on mobile or has GIF/JPEG fallbacks.
- Reusable user feedback is recorded back into the skill.
