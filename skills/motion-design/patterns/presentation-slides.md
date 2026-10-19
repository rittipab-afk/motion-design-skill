# Presentation Slides & One-Pagers

Motion for technical presentations: PowerPoint (and Google Slides) decks that walk an audience through
process data — PI trends, before/after improvements, control-loop performance, cost-saving results.
The goal is **comprehension, not decoration**. Every animation must answer: "What should the audience
look at next?"

## Context Overrides

Slides are not product UI. These rules override the general SKILL.md defaults:

| General rule | Slides override | Why |
|--------------|-----------------|-----|
| Always three motion layers | **Primary only.** No ambient motion, ever | Ambient motion pulls eyes off the data |
| Durations in ms (80-600ms) | Use **seconds** in PowerPoint; see table below | Audience reads at presenter pace, often on a projector |
| Personality: pick one | **Corporate**, always | Engineering/management audience |
| Overshoot allowed | **No overshoot, no bounce** | Data must feel exact and stable |
| Stagger budget < 500ms | Reveals are **On Click**, paced by the speaker | The speaker controls the story |

## Static vs Animated: Decide First

- **One-pager / report / PDF / printed** → **no animation.** Motion is lost on export. Use visual hierarchy
  instead: one headline takeaway, one hero chart, highlight color for the key series, callout box for the number.
- **Deck sent by email, read without a presenter** → minimal or none. Readers click through alone; builds
  hide information. Prefer one complete chart per slide.
- **Deck presented live** (meeting, shift handover, management review) → animation is useful for
  revealing a trend story step by step.
- **Deck that must also be shared as PDF** → build the reveal with **duplicated slides** (each slide adds one
  element) instead of animations, so the PDF keeps the step-by-step story.

## PowerPoint Duration Table

| Element | Effect | Duration | Start |
|---------|--------|----------|-------|
| Slide-to-slide (default) | Fade transition | 0.5 s | — |
| Same layout, data changes (zoom in on period, swap tag) | Morph transition | 0.7-1.0 s | — |
| Text / takeaway / callout box | Fade (entrance) | 0.4-0.5 s | On Click |
| Chart series (line / trend) | Wipe, From Left | 1.0-1.5 s | On Click |
| Bar / column chart | Wipe, From Bottom, By Category | 0.5 s each | After Previous, 0.1-0.2 s delay |
| Marker line (event, setpoint change, program ON) | Wipe, From Top | 0.4 s | On Click |
| Highlight region (shaded rectangle) | Fade to ~30% transparency | 0.5 s | On Click |
| Exit (remove distraction) | Fade (exit) | 0.3 s | With Previous |

**Easing in PowerPoint**: Animation Pane → Effect Options → *Smooth start / Smooth end*.
Entrances: Smooth end only (decelerate). Exits: Smooth start only (accelerate). Bounce end: always 0.

## Effects

**Use**: Appear, Fade, Wipe, Zoom (subtle, for a single callout), Morph transition.
**Avoid**: Bounce, Spin, Swivel, Boomerang, Fly In from off-slide, Pulse/Teeter loops, sound effects,
transitions other than Fade/Morph (Vortex, Origami, etc.).

## Chart Animation: Trend-Story Recipe (Before / After Improvement)

Use for PI trend slides showing the effect of a change (e.g. new Exapilot program, APC tuning, setpoint change).

1. **Headline takeaway** visible from the start (static title stating the result in one line).
2. **Chart frame**: axes, gridlines, legend, units — visible from the start so the audience orients first.
   (Chart animation *By Series* animates the background as its own first step; set it to appear with the slide.)
3. **Click 1 — Before period**: Wipe From Left, the baseline series / pre-change window.
4. **Click 2 — Event marker**: vertical line + short label (date, what changed). Wipe From Top.
5. **Click 3 — After period**: Wipe From Left, the post-change window.
6. **Click 4 — Callout**: the result number (Δ, %, variability reduction) in a box near the relevant area. Fade.
   Only use numbers the user provides — never invent or estimate results.

Variants:
- **Multiple tags on one chart** → Effect Options → Sequence → *By Series*; reveal hero tag last.
- **Variability reduction** → reveal shaded band (±σ or limit lines) before and after, so the narrowing is visible.
- **Zoom on an event** → duplicate slide, change the axis range, use **Morph** between the two slides.

## Choreography for Slides

- **One new thing per click.** If a click reveals two unrelated things, split it.
- **Reading order**: top-left → bottom-right, title → chart → callout.
- **Hero last**: the key series or result number is the final reveal on the slide.
- **Max ~5 clicks per slide.** More than that → split into two slides.
- **Direction carries meaning**: time series always Wipe From Left (time flows left to right); bars From Bottom
  (values grow up). Never reveal a time series from the right.

## Quality Checklist (Slides)

- [ ] Static first: does this slide need motion at all? (One-pager / PDF → no)
- [ ] Every animation reveals information in the order it should be read
- [ ] No ambient, looping, bounce or decorative effects
- [ ] Time series wipe left-to-right; bars bottom-to-top
- [ ] Transitions are Fade or Morph only, ≤ 1 s
- [ ] Hero data / result number is the last reveal
- [ ] Every number shown was provided by the user (no invented results)
- [ ] Deck still makes sense if exported to PDF (or a duplicated-slide build exists)
