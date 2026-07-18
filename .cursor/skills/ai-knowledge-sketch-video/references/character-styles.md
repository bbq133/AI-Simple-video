# Character Style Library

Choose one character family after choosing the component design system. Do not mix character families inside one video.

All styles use five canonical poses: `思考 / 指引 / 携带 / 拒绝 / 行走`.

## P1 — 圆豆向导 Bean Guide

Best match: System A / B.

Feeling: soft, confident, friendly, contemporary.

- Head: `112 × 104 px`, slightly oval.
- Torso: one rounded bean shape, `132 × 176 px`.
- Arms/legs: `14 px` rounded limbs, not skeletal lines.
- Face: two `8 px` eyes + one `20 px` mouth curve.
- Hands/feet: simple rounded ends, no fingers.
- Accent: one coral cuff, notebook, or pointer.
- Character height: `360–430 px`.
- Do not use a stick spine.

Motion: body squash `0.96 → 1`, 6 px settle; arms rotate from shoulder anchors.

## P2 — 软线漫步 Softline Walker

Best match: System A / B.

Feeling: editorial, elegant, human, light.

- Head: open hand-drawn circle, diameter `96 px`.
- Body: one continuous curved contour, not a straight stick.
- Stroke: `7 px`, rounded, slight pressure variation.
- Torso includes a subtle shoulder/hip curve.
- Face: optional eye dots only; expression comes from posture.
- Character height: `380–460 px`.
- Accent: coral scarf/marker stroke, maximum one.

Motion: line draws on in `0.3 s`; posture eases with small arm/torso rotations.

## P3 — 剪纸胶囊 Paper Capsule

Best match: System A / B.

Feeling: designed, tactile, clean, easiest to animate.

- Head: paper circle, diameter `104 px`, with `6 px` offset shadow.
- Torso: rounded capsule `126 × 184 px`.
- Arms/legs: separate rounded paper strips, `24–30 px` thick.
- No facial features by default; optional two ink dots.
- Character height: `380–440 px`.
- Palette: ivory body, mint torso tab, coral active prop.
- Each limb is a separate layer.

Motion: paper pieces arrive independently, then lock into the pose; no rubber morphing.

## P4 — 编辑部角色 Editorial Figure

Best match: System B / C.

Feeling: smart, stylish, more mature, suitable for product opinions.

- Head: `96 × 108 px`, slightly rectangular-rounded.
- Neck: visible short line/shape.
- Torso: tapered jacket-like silhouette `150 × 190 px`.
- Legs: two simple tapered shapes rather than sticks.
- Face: eyebrows + eyes, no detailed nose.
- Character height: `400–480 px`.
- Accent: one colored collar, sleeve, or folder.
- Hair is optional but must be one simple shape.

Motion: head/eyebrow reaction, hand gesture, and 8–12 px body shift; avoid bouncing.

## P5 — 几何助手 Geo Helper

Best match: System C.

Feeling: precise, modern, technical, not robotic.

- Head: `96 px` circle.
- Torso: rounded trapezoid `144 × 172 px`.
- Joints: `18 px` circles.
- Limbs: `16 px` rounded bars.
- Character height: `370–440 px`.
- Face: two navy dots; active joint/prop may use tomato.
- Geometry uses the same radius and stroke logic as technical modules.
- Do not add antennas, robot ears, or metallic effects.

Motion: joints rotate cleanly; active node pulses once; body moves on 8 px grid.

## Selection recommendation

| Goal | Pick |
|---|---|
| Most attractive and friendly | P1 圆豆向导 |
| Most hand-drawn and editorial | P2 软线漫步 |
| Best for paper-cut layer animation | P3 剪纸胶囊 |
| Most mature/product-opinion oriented | P4 编辑部角色 |
| Best for technical explainers | P5 几何助手 |

## Approval gate

Before full production:

1. render all five families in the same three poses;
2. review at 360 px preview width;
3. select one family;
4. create a character turnaround/pose sheet;
5. record `characterFamily` in `STYLE_LOCK.md`.
