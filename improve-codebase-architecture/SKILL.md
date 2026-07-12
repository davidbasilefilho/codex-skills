---
name: improve-codebase-architecture
description: Find codebase deepening opportunities, present a visual HTML review, then guide selected design. Use for architectural friction, shallow modules, weak seams, poor locality, or testability-driven refactoring.
---

# Improve Codebase Architecture

Seek deep modules: small interfaces hiding substantial implementation, improving testability and AI navigation.

Use `codebase-design` vocabulary exactly: **module**, **interface**, **depth**, **seam**, **adapter**, **leverage**, **locality**. Apply deletion test and principles: interface is test surface; one adapter is hypothetical seam, two are real. Use `CONTEXT.md` domain terms and respect `docs/adr/`.

## 1. Explore

Read domain glossary and relevant ADRs. Explore organically for:

- understanding scattered across small modules;
- interfaces nearly as complex as implementations;
- pure functions extracted for tests while call-site bugs remain;
- coupled modules leaking across seams;
- untested or hard-to-test interfaces.

Deletion test: would removing candidate concentrate complexity rather than move it? Only then treat as strong deepening opportunity.

## 2. Report

Create self-contained `<temp>/architecture-review-<timestamp>.html`; never write report into repo. Resolve `$TMPDIR`, `/tmp`, or `%TEMP%`. Open with platform command and provide absolute path.

Use Tailwind CDN, Mermaid CDN for graph-shaped relationships, and CSS/SVG for editorial visuals. Follow [HTML-REPORT.md](HTML-REPORT.md). Every candidate card needs:

- files/modules;
- friction;
- proposed change in plain language;
- locality, leverage, and test benefits;
- side-by-side before/after visual;
- `Strong`, `Worth exploring`, or `Speculative` badge.

End with top recommendation and reason. Use domain vocabulary. Mark worthy ADR conflicts explicitly; omit theoretical conflicts. Do not design interfaces yet. Ask which candidate user wants to explore.

## 3. Design Selected Candidate

Run `grilling` for constraints, dependencies, deepened module shape, hidden implementation, seam, and surviving tests.

Keep artifacts current as decisions form:

- New/sharpened domain concept: update `CONTEXT.md`; create lazily.
- Rejection with durable, load-bearing reason: offer ADR; skip temporary/self-evident reasons.
- Alternative interfaces: run `codebase-design` and its design-it-twice parallel pattern.
