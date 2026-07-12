---
name: gpt-taste
description: Create high-variance editorial UI with AIDA structure, wide heroes, gapless bento grids, advanced GSAP motion, varied assets, and strict preflight verification. Use for motion-rich premium React/Tailwind pages that must avoid common generated layouts.
---

# GPT Taste

No emojis. Before code, emit `<design_plan>` using deterministic prompt-derived selection: one hero, one font stack (Satoshi, Cabinet Grotesk, Outfit, Geist; never Inter), three component architectures, two GSAP paradigms. Do not repeat default combination.

## Page System

Follow AIDA: premium nav; Attention hero; Interest bento/features; Desire scroll/media; Action CTA/footer. Separate chapters with `py-32 md:py-48`.

Hero:

- Select cinematic center, artistic asymmetry, or editorial split.
- H1 uses wide `max-w-5xl`/`max-w-6xl`, responsive `clamp`, maximum 2–3 lines.
- Maintain perfect button contrast. No stamp icons, pill tags, or raw stats.

Bento: 3–5 intentional cards, `grid-flow-dense`, spans proven to fill every cell. Mix imagery, typography, and CSS effects; no dead corners.

Components may include inline heading images, horizontal expanding accordion, infinite partner marquee, or restrained testimonial carousel.

## Motion

Use real GSAP with `@gsap/react` and `ScrollTrigger`. Select two: pinned title/gallery split, image scale/fade scroll, scrubbed word reveal, stacked cards. Interactive images/cards need slow contained scale hover. Static interface fails.

Wrap page with `<main className="overflow-x-hidden w-full max-w-full">` to contain animated overflow.

## Assets and Bans

Use contextual `https://picsum.photos/seed/{keyword}/1920/1080` when needed; art-direct with coherent grayscale/blend/contrast/opacity. Use subtle radial blur, grain mesh, or dark overlays.

Ban cheap meta-labels (`SECTION 01`, `QUESTION 05`, `ABOUT US`), invisible button text, empty bento cells, narrow multi-line heroes, repeated left/right sections, flat backgrounds, and stock-feeling imagery.

## Required `<design_plan>`

1. Three-line deterministic selection output for hero, font, three components, two GSAP motions.
2. AIDA map.
3. H1 max-width and 2–3-line proof; confirm no stamps/tags.
4. Grid span math and `grid-flow-dense` proof.
5. Meta-label sweep and button contrast check.

Only then output UI code.
