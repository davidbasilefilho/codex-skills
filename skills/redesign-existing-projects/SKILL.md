---
name: redesign-existing-projects
description: Upgrade existing websites/apps to premium quality without breaking behavior or replacing their stack. Use for redesigns, design audits, removing generic AI patterns, or targeted visual and UX polish across any CSS approach.
---

# Redesign Existing Projects

## Workflow

1. Scan framework, styling system, dependencies, components, routes, states, and existing visual language.
2. Audit issues below; report evidence and priorities.
3. Apply focused upgrades in current stack. Never rewrite from scratch, migrate frameworks, or add unchecked dependencies. Check Tailwind version before config edits.
4. Test behavior after each change. Keep diffs reviewable; remove debug/dead code.

## Audit

### Type and Content

- Replace browser defaults or monotonous Inter with fitting characterful type; use serif/sans pairing when editorial.
- Give headings presence: fluid scale, tight tracking/leading, balanced wrapping. Limit body width near 65 characters; use 500/600 weights for hierarchy.
- Use tabular/monospace numerals for data; positive tracking for labels; avoid all-caps everywhere.
- Replace lorem ipsum, clichés, title-case overload, fake brands/names/round numbers, repeated avatars/dates, “Oops!”, passive errors, and empty links with specific credible content.

### Palette and Surface

- Use off-black instead of pure black; one restrained accent; one warm or cool gray family.
- Remove generic purple-blue AI gradients, harsh black shadows, inconsistent lighting, random light/dark section jumps.
- Add controlled texture, ambient image, radial/mesh treatment, tinted shadows, or grain where flat sections lack depth. Keep palette coherent.

### Layout

- Replace repetitive centered symmetry and equal three-card rows with justified asymmetry, mixed spans, zig-zag, masonry, or horizontal flow.
- Use `min-height: 100dvh`, max-width container (roughly 1200–1440px), CSS Grid for complex columns, responsive relative units, generous optical spacing.
- Align repeated card titles, feature starts, prices, and CTAs; allow varied heights when appropriate. Use optical 1–2px corrections.
- Avoid universal radius, forced sidebars, flat depth, and accidental overlaps. Mobile must remain clear and touch-safe.

### Components and States

- Use cards only when grouping/elevation matters. Avoid default border-shadow-white cards, paired filled/ghost CTAs, pill badges, FAQ accordions, dotted testimonial carousels, three-tower pricing, modal overuse, avatar-only circles, sun/moon switches, and footer link farms.
- Add hover, pressed, focus, active-nav, loading, empty, error, validation, smooth anchors, back navigation, 404, skip link, legal links, and required consent.
- Animate `transform` and `opacity`, 200–300ms or context-appropriate springs; never layout properties.

### Assets and Code

- Use one consistent icon family/stroke; avoid default Lucide/Feather and cliché metaphors where differentiation matters. Add favicon and meaningful alt text.
- Prefer real/candid or coherent illustrated imagery. When assets are absent, use stable contextual placeholders such as `https://picsum.photos/seed/{name}/1920/1080`.
- Use semantic HTML and project styling conventions. Remove inline-style mixing, arbitrary `z-index`, import hallucinations, and missing title/description/social metadata.

## Upgrade Order

1. Font and type hierarchy.
2. Palette cleanup.
3. Interaction states.
4. Grid, spacing, and alignment.
5. Generic component replacement.
6. Loading/empty/error completion.
7. Final typographic and motion polish.

Use advanced techniques only when concept supports them: broken grid, deep whitespace, parallax stacks, split scroll, staggered or scroll-driven reveals, spring motion, refractive glass, spotlight borders, and grain. Accessibility, performance, function, and project coherence outrank novelty.
