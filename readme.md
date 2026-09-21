# NABCO — Al Nukhba Al Barraq Company · Design System

Design system for **NABCO (نابكو · شركة النخبة البراق)**, a Jeddah-based group operating across logistics, fleet and transport, contracting and facilities in Saudi Arabia, built to carry future sub-brands (divisions). The identity is built around a lightning bolt driven forward by five speed lines: speed, efficiency, momentum.

## Sources
- `D:/NABCO/Branding/NABCO_Brand_Source_Package` — client-approved master logo (SVG/EPS/PDF), core colours.
- `D:/NABCO/Brand-System` — the full identity system derived from it: generators (`_src/`), tokens, 180+ logo/element/application assets, and the guidelines document preserved here at `guidelines/nabco-design-system-reference.html`.
- No website codebase exists yet; components here are the reference implementation, not ports.

## CONTENT FUNDAMENTALS
- **Bilingual, written natively.** Arabic is never a translation of the English; lead with the audience's language (Arabic first for domestic/government, English first for international).
- Voice is **provisional** (no approved copy guide yet): short, confident, concrete — "Speed. Scale. Certainty.", "Moving the Kingdom forward." Name real services and real figures; no unattributed claims.
- Sentence case for body and headings; eyebrows UPPERCASE tracked (English only — Arabic is never letter-spaced). No emoji.
- The company names are fixed: "NABCO", "Al Nukhba Al Barraq Company", "شركة النخبة البراق", "نابكو".

## VISUAL FOUNDATIONS
- **Colour**: navy `#104060` (primary — ink, grounds, structure), Electric Gold `#F2C230` (accent only — rules, fills, speed lines, ~10% of a layout), sand `#F7F4EF` (light ground), ink `#111111` (mono). Proportion ~60% ground / 30% neutral / 10% gold.
  - **Gold is never text on a light ground**: 1.53:1 on sand, 1.68:1 on white. Gold type on light uses `--gold-800` `#8B6500` (4.83:1). Gold on navy is 6.51:1 — use freely. Gold buttons carry ink or navy text, never white.
  - Neutrals are the warm **sand** ramp, never default greys. Body text stops at `--sand-600` (5.05:1).
  - On navy grounds gold becomes the action colour (`.on-dark` swaps the semantic tokens).
  - Six **division accents** (`--accent-*`) at equal OKLCH lightness, all AA with white text — for sub-brand tabs, rules, charts; never inside the logo. Status colours are functional only.
- **Geometry — the two angles**: every angled edge uses **Rake 3°** (velocity: speed lines, patterns, shallow edges) or **Strike 52°** (the bolt stroke: panel cuts, chevrons, corners). Nothing else. On small formats keep strike diagonals in a corner so they never cross type.
- **Type**: IBM Plex Sans for all Latin (headings bold, −0.02em, `text-wrap: balance`); IBM Plex Sans Arabic for ALL Arabic, set ×1.08 with line-height 1.35 display / 1.75 body, tracking 0; IBM Plex Mono only for specs, IDs, tabular figures. Scale `--size-xs`…`--size-6xl`.
- **Space**: 4px base (`--space-*`); sections 80px (48px compact); max-width 1240px; prose 66ch; lay out with `gap`.
- **Corners**: small radii only — 2px buttons/inputs/badges, 4px cards, 8px overlays. The brand's corner is the **52° strike cut** (`.card-strike`), not a big radius.
- **Elevation**: navy-tinted `rgba(6,46,72,α)` shadows, never neutral black.
- **Focus**: 2px ground + 2px navy-600 ring; gold ring on dark grounds.
- **Graphic elements** (`assets/elements/`): Rake Array (the mark's own speed lines — fleet/hero device), Velocity Field (tileable speed-line texture at 8–12%, never behind body copy), Strike Cut panel, Bolt Mask (photo clip), Chevron (always points right). **One device per composition.**
- **Motion**: always left to right. Rake sweep 320ms `cubic-bezier(.4,0,.1,1)`; strike reveal 560ms `cubic-bezier(.2,.8,.2,1)`; UI 150–200ms. Honour `prefers-reduced-motion`.
- **RTL**: mirror the layout (logical properties, `.icon-directional` on arrows) — **never the logo**.

## LOGO
Use the `<Logo>` component (outlined artwork, inlined) or files in `assets/logo/`. Never draw, re-type, recolour, stretch, rotate or mirror it.
- Pick by width: **horizontal** (bilingual + descriptors) ≥360px/60mm · **compact** (no descriptors) ≥160px · **minimal** (icon + NABCO) ≥110px · **stacked** for square/portrait · **badge** (navy square, bolt + gold lines) ≥48px · **badge-micro** (bolt only) ≥16px.
- `tone="reverse"` on navy/dark: artwork goes white, speed lines stay gold.
- Clear space = one cap height of "NABCO" on every side. The icon sits LEFT in every lockup, Arabic-only included.
- Sub-brands: branded house — the division name replaces the descriptor line; icon, wordmark and gold rule never change.

## ICONOGRAPHY
No icon set has been chosen. Use a single stroke icon family (e.g. Lucide, 2px stroke) consistently; directional icons point right and mirror in RTL via `.icon-directional`. No emoji.

## Index
- `styles.css` — global entry (imports `tokens/`).
- `tokens/` — `fonts.css`, `tokens.css` (all custom properties), `base.css`, `components.css`.
- `assets/logo/` — lockups, icon, badges, square formats (SVG). `assets/elements/` — graphic elements (SVG).
- `guidelines/cards/` — specimen cards. `guidelines/nabco-design-system-reference.html` — full identity guidelines.
- `components/brand/` — Logo, VelocityField. `components/core/` — Button, Card, Badge, SectionHeader, Stat, Field.
- `SKILL.md` — agent skill entry point.
