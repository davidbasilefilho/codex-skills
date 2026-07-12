---
name: teach
description: Teach a skill or concept through a persistent workspace of mission-driven lessons, references, resources, practice, and learning records.
---

# Teach

Treat current directory as stateful teaching workspace.

## Workspace

- `MISSION.md`: learning purpose; use [MISSION-FORMAT.md](MISSION-FORMAT.md).
- `RESOURCES.md`: trusted sources and communities; use [RESOURCES-FORMAT.md](RESOURCES-FORMAT.md).
- `learning-records/NNNN-name.md`: durable insights and mission changes; use [LEARNING-RECORD-FORMAT.md](LEARNING-RECORD-FORMAT.md).
- `lessons/NNNN-name.html`: short, self-contained lessons.
- `reference/*.html`: printable cheat sheets, algorithms, syntax, poses, glossaries.
- `assets/*`: shared styles, quizzes, simulators, diagram helpers.
- `NOTES.md`: preferences and working notes.

## Principles

Ground every lesson in mission. If mission is unclear or absent, ask why user wants topic before teaching. Confirm mission changes; update `MISSION.md` and add learning record.

Use trusted external sources; never rely only on parametric memory. Build:

- knowledge from high-trust material;
- skills through relevant practice and tight feedback;
- wisdom through real-world communities/practitioners.

Optimize long-term storage, not temporary fluency. Use retrieval practice, spacing, and skill interleaving. For knowledge acquisition, reduce difficulty; for skill retention, add desirable difficulty.

## Lesson Workflow

1. Read mission, records, notes, resources, references, and reusable assets.
2. Choose one mission-relevant task in user's zone of proximal development. If user did not choose, infer from records.
3. Research trusted sources; update `RESOURCES.md`. Cite claims and recommend one primary source.
4. Create next numbered HTML lesson: beautiful, printable, quick, one tangible win, limited working-memory load, linked to related lessons/references, with invitation for questions.
5. Teach required knowledge, then interactive practice with immediate feedback. Quiz answers should have equal word and, when practical, character counts to avoid clues.
6. Open lesson when possible.
7. Capture non-obvious learning in next record; update concise reference material.

## Assets and References

Reuse `assets/` by default. First workspace component should be shared stylesheet. Extract anything a second lesson could reuse; do not duplicate inline code.

References are compressed long-term recall artifacts; maintain consistent glossary terms across every lesson.

For wisdom questions, answer provisionally and recommend a reputable online/offline community. Respect refusal to join.
