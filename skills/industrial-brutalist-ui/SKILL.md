---
name: industrial-brutalist-ui
description: Build raw mechanical interfaces combining Swiss industrial print or tactical CRT telemetry with rigid grids, extreme type contrast, utilitarian color, and analog degradation. Use for dense dashboards, portfolios, editorial sites, or blueprint-like systems.
---

# Industrial Brutalist UI

Choose one mode; never mix substrates.

## Modes

- **Swiss print:** off-white `#F4F4F0`/`#EAE8E3`, carbon `#050505`–`#111111`, only hazard red `#E61919`/`#FF2A2A`. Heavy asymmetric sans, visible blueprint grid, huge negative space/numerals.
- **Tactical CRT:** dark `#0A0A0A`/`#121212`, phosphor white `#EAEAEA`, same hazard red. Dense mono data, brackets/crosshairs/scanlines. Optional `#4AF626` for one functional indicator only.

No gradients, soft shadows, translucency, mixed light/dark sections, or rounded corners.

## Typography

- Macro: heavy neo-grotesk (Neue Haas Black, Archivo Black, Roboto Flex Heavy, Monument Extended), uppercase, `clamp(4rem, 10vw, 15rem)`, tracking `-0.03em` to `-0.06em`, line-height `0.85`–`0.95`.
- Micro: JetBrains/IBM Plex/Space Mono, VT323, or Courier Prime; 10–14px, tracking `0.05em`–`0.1em`, line-height `1.2`–`1.4`, uppercase metadata/nav/units.
- High-contrast serif only as rare degraded disruption.

## Structure

Use deterministic CSS Grid, visible 1–2px compartments/rules, alternating dense telemetry and vast negative space. Efficient line method: contrasting grid parent/children with `gap: 1px`.

Use semantic technical tags (`data`, `samp`, `kbd`, `output`, `dl`). Add restrained ASCII framing (`[ SYSTEM ]`, `>>>`, `///`), registration marks, crosshairs, barcodes, warning stripes, and believable revision/unit data.

Simulate physical media with low-opacity global SVG noise, halftone/1-bit dithering, or CRT repeating scanlines. Effects must reinforce chosen substrate, never become decoration noise.
