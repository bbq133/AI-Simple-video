# QC Checklist

## Script and logic

- [ ] The user approved the full spoken script before voice generation.
- [ ] Every scene teaches one idea.
- [ ] Every bridge explains why the next scene follows.
- [ ] Spoken lines and on-screen components share the same order.

## Settled-frame composition

- [ ] The completed frame has a clear visual center.
- [ ] Label, visual, modules, and summary form a readable top-to-bottom path.
- [ ] No large meaningless blank region remains.
- [ ] Negative space has a purpose: focus, breathing room, or a documented motion path.
- [ ] The bottom summary is integrated, not stranded.
- [ ] No component is clipped, obscured, or touching unsafe edges.
- [ ] Text remains readable at 360 px preview width.

## Component animation

- [ ] The scene begins with only the first focus element.
- [ ] Components enter when their phrase is spoken.
- [ ] Entrances settle in 0.35–0.55 s.
- [ ] The final component is the summary/takeaway.
- [ ] The completed scene holds after the final spoken word.
- [ ] No duplicate HTML chip covers text already inside a keyframe.

## Transitions

- [ ] Completed scene fades out gently.
- [ ] Bridge appears after the scene is understandable.
- [ ] Bridge title is centered and large enough.
- [ ] Bridge has a stage kicker and one clear focus phrase.
- [ ] Next card fades in; no abrupt page flip.

## Narration

- [ ] Voice sample was approved or at least reviewed before full rerender.
- [ ] Speed is conversational, not artificially slow.
- [ ] Pauses vary naturally.
- [ ] Pronunciation glossary was applied.
- [ ] `AI` is spoken as `人工智能` unless explicitly overridden.
- [ ] Each file duration was measured.
- [ ] Picture timing was rebuilt from measured durations.

## Render

- [ ] H.264 video and AAC audio exist.
- [ ] Video and audio cover the intended duration.
- [ ] First and last frames decode.
- [ ] Width/height/FPS match the manifest.
- [ ] Final contact sheet has no black or incomplete frames.

## Preview

- [ ] JPEG preview is 540 px wide and lightweight.
- [ ] GIF is 320–360 px wide and lightweight.
- [ ] MP4 uses faststart and yuv420p.
- [ ] Progressive reveal strip is included.
- [ ] Full-resolution master remains available separately.
