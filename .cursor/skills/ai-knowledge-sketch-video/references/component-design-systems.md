# Component Design Systems

Choose exactly one system per video. Do not mix characters, corner radii, shadows, icon strokes, or title hierarchies from different systems.

All values target a 1080×1920 canvas. Scale proportionally for previews.

## Shared foundation

### Canvas and grid

- Canvas: `1080 × 1920`, 9:16.
- Safe area: `64 px` left/right, `72 px` top, `96 px` bottom.
- Base grid: `8 px`.
- Standard vertical gaps: `24 / 32 / 48 / 64 px`.
- Components must remain independently animatable.
- Completed-frame content should occupy roughly `68–82%` of the useful vertical field.
- Empty regions larger than `320 px` high require a documented focus or motion purpose.

### Shared type scale

| Role | Size | Weight | Line height |
|---|---:|---:|---:|
| Cover hook | 76 | 900 | 1.16 |
| Scene focus title | 64 | 900 | 1.24 |
| Module title | 48 | 800 | 1.28 |
| Summary | 44 | 800 | 1.38 |
| Body/support | 34 | 600 | 1.5 |
| Scene kicker | 30 | 700 | 1.2 |
| Hint/meta | 26 | 500 | 1.35 |

Use at most three text levels in one frame. Use one highlighted phrase, not many.

### Character-family override

Character design is selected separately from the surrounding component system. Read `character-styles.md` and lock one family (`P1–P5`). The chosen family inherits the system palette but keeps its own body proportions and motion grammar. Its specification overrides the fallback character notes under each system.

### Shared motion contract

- Scene label enters first.
- Character/context enters second.
- Knowledge components enter in spoken order.
- Summary enters last.
- Component entrance: `0.35–0.55 s`.
- Final hold: at least `0.8 s` after narration.
- Transition: fade out → centered bridge → fade in.

---

## System A — 薄荷剪纸 Mint Paper

Best for: general AI/product knowledge, misconceptions, product thinking, workflow explanations.

Personality: fresh, friendly, precise, light.

### Color tokens

| Token | Hex | Use |
|---|---|---|
| `paper` | `#FBF8F1` | main field |
| `paper-card` | `#FFFCF7` | cards/chips |
| `ink` | `#242525` | text/line |
| `ink-muted` | `#6E706D` | secondary text |
| `mint-100` | `#EEF8F2` | soft module fill |
| `mint-500` | `#72B894` | positive/flow |
| `coral-500` | `#E35D4B` | single focus |
| `sand` | `#E8DED0` | borders/background detail |

Maximum: paper + ink + mint + coral. Coral should occupy less than 12% of the frame.

### Shape tokens

- Main card radius: `32 px`.
- Keyword chip radius: `22 px`.
- Scene label radius: `18 px`.
- Border: `2 px solid rgba(36,37,37,.12)`.
- Shadow: `0 12px 24px rgba(90,70,40,.14)`.
- Paper cut offset: `4–8 px`, never thick/extruded.

### Character

- Round head diameter: `92–112 px`.
- Body height: `300–430 px`.
- Stroke: `4 px`, round cap/join.
- Face: two dots + one short curve; maximum three facial marks.
- Hands/arms use one continuous gesture line.
- Five standard poses: think, point, carry, reject, walk.
- Do not add clothes/details unless required by the lesson.

### Symbols and icons

- Stroke: `4 px`, charcoal.
- Bounding box: `72 / 96 / 128 px`.
- Corners round; no filled glossy icons.
- Error: coral X inside a circle.
- Correct: coral or mint tick.
- Process: mint arrow with a `4 px` shaft.
- Question: standalone charcoal `?`, never emoji.

### Numbers and levels

- Scene number: coral, two digits (`01`).
- Sequence number: circled `① ② ③` in coral.
- Level card: left-aligned number, title, optional one-line support.
- Standard level card: `800 × 180 px`.
- Level spacing: `60 px`.

### Titles and cards

- Scene label: `01 / 开场`; coral number + ink category.
- Keyword chip: one phrase, 2–6 Chinese characters.
- Summary card: maximum two lines, centered, `44 px`.
- Bridge: small mint kicker + `64 px` center title + optional gray hint.

### Motion signature

Paper-settle: rise `34 px`, scale `0.88 → 1`, rotate `-2° → 0°`, `back.out(1.5)`.

---

## System B — 杏色手账 Apricot Journal

Best for: creator education, AI habits, prompt tips, personal workflows, approachable tutorials.

Personality: warm, editorial, human, lightly playful without becoming childish.

### Color tokens

| Token | Hex | Use |
|---|---|---|
| `cream` | `#FFF7EA` | field |
| `paper` | `#FFFDF8` | notes |
| `ink` | `#30312E` | text/line |
| `sage` | `#A9BDA6` | calm support |
| `apricot` | `#F4BA8A` | section grouping |
| `terracotta` | `#D96E55` | focus/error |
| `dust-blue` | `#AFC3CC` | neutral structure |

Use two soft fills plus one terracotta focus. Avoid full pink palettes.

### Shape tokens

- Note radius: `18 px`.
- Feature card radius: `28 px`.
- Tape corner: `72 × 26 px`, `8%` opacity texture.
- Border: `2 px solid rgba(48,49,46,.1)`.
- Shadow: `0 9px 18px rgba(86,68,48,.12)`.
- Optional irregular paper edge amplitude: `3–5 px`.

### Character

- Head: slightly oval, `96 × 88 px`.
- Body height: `310–420 px`.
- Stroke: `5 px`, subtly imperfect.
- One warm accent object per pose: pencil, note, folder, or pointer.
- Standard poses: listen, write, compare, peel-note, celebrate.
- Keep eyes and mouth minimal; no kawaii blush or oversized anime eyes.

### Symbols and icons

- Stroke: `5 px`.
- Use hand-drawn enclosure: loose circle, underline, bracket.
- Highlight: semi-transparent apricot marker swipe.
- Correct/error: hand-drawn tick/cross, not UI icons.
- Arrow: curved, slightly asymmetrical.
- Icon labels may sit on small paper tabs.

### Numbers and levels

- Scene number: terracotta handwritten-style numerals.
- Steps use `1 / 2 / 3` inside `64 px` irregular circles.
- Level title uses a colored top tab: `基础 / 进阶 / 应用`.
- Standard note: `760 × 190 px`.
- Alternate notes shift horizontally by `32–48 px` to feel collected, not grid-rigid.

### Titles and cards

- Cover title can use one marker underline.
- Body cards use left-aligned title + one concise note.
- Summary uses a “torn note” shape, maximum two lines.
- Bridge uses a journal divider: chapter label + one centered sentence.

### Motion signature

Note placement: rotate `-4°/+3° → 0°`, y `44 → 0`, `0.5 s`; optional tape appears `0.12 s` after note.

---

## System C — 雾蓝墨线 Mist Blueprint

Best for: model concepts, RAG/Agent systems, comparisons, architecture, mechanisms, more technical AI education.

Personality: clear, intelligent, calm, premium, but not corporate dashboard-like.

### Color tokens

| Token | Hex | Use |
|---|---|---|
| `fog` | `#F3F7F6` | field |
| `white` | `#FFFFFF` | cards |
| `navy-ink` | `#24323A` | text/line |
| `blue-100` | `#E4F0F2` | structure fill |
| `blue-500` | `#6198A4` | connector/data |
| `tomato` | `#DD6654` | focus/warning |
| `graphite` | `#8A969A` | secondary |

No neon, gradients, glassmorphism, or dark “AI cockpit” treatment.

### Shape tokens

- Main module radius: `16 px`.
- Secondary module radius: `12 px`.
- Border: `2 px solid #C9D7D8`.
- Shadow: `0 8px 20px rgba(36,50,58,.10)`.
- Optional guide grid: `1 px`, `#DCE7E6`, 48 px spacing, max 18% opacity.

### Character

- Head diameter: `84–96 px`.
- Body height: `290–380 px`.
- Stroke: `4 px`, navy ink.
- Character acts as analyst/guide, not mascot.
- Standard poses: inspect, connect, sort, test, conclude.
- A single tomato accent may mark the active hand/object.

### Symbols and icons

- Stroke: `4 px`, geometric but with round caps.
- Standard icon boxes: `80 / 112 px`.
- Connector lines: `4 px`; active route blue, error route tomato.
- Nodes: `20 px` filled circles.
- Use bracket, flow, funnel, layer, and comparison symbols.
- Avoid generic robot heads and sparkles.

### Numbers and levels

- Scene numbers: `01`, navy; active digit block in tomato.
- Architecture levels use `L1 / L2 / L3` plus Chinese titles.
- Comparison columns use `A / B`, not decorative badges.
- Standard technical module: `820 × 168 px`.
- Connector gap: `48–72 px`.

### Titles and cards

- Scene kicker: uppercase-like compact label, `30 px`.
- Focus title: left aligned, `60–64 px`.
- Technical term may appear in a blue capsule; one capsule per frame.
- Summary uses a full-width bottom band integrated with the diagram.
- Bridge uses `阶段 / 结论` kicker and one large sentence.

### Motion signature

Trace-and-lock: connector draws first (`0.35 s`), module fades/rises `20 px` (`0.4 s`), active node pulses once. Never keep nodes pulsing continuously.

---

## Selection guide

| Content | Recommended system |
|---|---|
| General AI/product education | A — 薄荷剪纸 |
| Creator tips and approachable tutorials | B — 杏色手账 |
| Technical mechanisms and architecture | C — 雾蓝墨线 |

Once selected, record the system name and version in `STYLE_LOCK.md`.
