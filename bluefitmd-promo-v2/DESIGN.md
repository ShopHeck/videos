# BlueFitMD — Brand & Design System

Visual system for the Wolverine Stack promo, derived from the BlueFitMD logo and the
BPC-157 / TB-500 product vial. The brand reads **clinical + athletic**: vivid medical blue,
clean geometry, high contrast.

## Color Palette

| Token         | Hex       | Use                                             |
|---------------|-----------|-------------------------------------------------|
| Blue (primary)| `#2E7DF6` | Brand blue — vial cap, label accents, fills     |
| Blue light    | `#5BA0F8` / `#6BA8FA` | Gradients, glows, secondary accents |
| Blue ice      | `#BFE2FF` / `#BFD9FF` | Highlights, "MD", bright type       |
| Blue deep     | `#1657C8` / `#1A5BC4` | Background depth, gradient cores    |
| Navy base     | `#0A1E3C` → `#061528` | Scene backgrounds                   |
| Ink           | `#0B1322` | "Bluefit" wordmark on light surfaces            |
| White         | `#FFFFFF` | Primary type, label, CTA button                 |
| Mist          | `#DCE9FF` / `#EAF2FF` | Body copy on dark                   |
| Danger red    | `#FF4438` / `#FF6A60` | Injury/problem only — resolves to blue |
| Amber glass   | `#5a3010` → `#c98a3e` | Product vial glass gradient         |
| Metal crimp   | `#8f99a6` → `#f4f6f8` | Vial neck (brushed aluminum)        |

The **red → blue** color journey is intentional: red owns the pain/problem (Beats 1–2) and
hands off to blue the instant the solution appears, so blue == relief throughout.

## Typography

- **Anton** (`anton-latin-400`) — display / headlines. Tall, condensed, athletic; carries the
  scroll-stopping hooks and section titles.
- **Inter** (weights 600–900) — eyebrows, body, trust copy, labels, CTA. Clean and clinical.

Both vendored at `capture/assets/fonts/` so renders never depend on Google Fonts.

## Logo

Reproduced as inline SVG: two stacked blue "wing" blades (forward momentum) + the
`Bluefit` (white/ink) `MD` (light blue) wordmark in Inter 800. A blue→ice gradient on dark
scenes, solid blue on the white product label.

## Product Vial

Reproduced as layered SVG + an HTML label overlay so it animates as one unit:
- Blue flip-cap with a top highlight ellipse
- Brushed-metal crimp neck (multi-stop linear gradient)
- Amber glass body with a soft inner highlight and drop shadow
- White label: mini logo, `BPC-157 / TB-500` in Anton blue, `INJECTION`, and a blue
  `10mg+10mg/3ml` band — matching the real product packaging.
- A diagonal light **sheen** sweeps across the glass on reveal.

## Motion Principles

- **Slam, don't drift.** Headlines enter with scale-down + back/power3 easing for impact.
- **Everything breathes.** Subtle continuous push-ins, floats, and glow pulses keep frames alive
  (critical for watch-time on Meta).
- **Contrast the bars.** Beat 2's recovery bar crawls; Beat 5's snaps to 100% — same motif,
  opposite feel, selling the speed claim visually.
- **Crossfade scenes.** Each sub-composition fades its own root in/out across ~0.4s overlaps.

## Messaging Guardrails

Claims are limited to what the brand states: **pharmaceutical grade**, **third-party lab tested**,
**verified for purity**, **two recovery peptides (BPC-157 + TB-500) in one stack**. No medical
efficacy or outcome guarantees beyond the brand's positioning.
