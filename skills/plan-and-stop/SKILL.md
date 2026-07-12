---
name: plan-and-stop
description: Inspect and plan a software task, then stop before editing. Use for planning, scoping, implementation design, or review checkpoints. Do not use when the user requests immediate implementation.
---

# Plan and Stop

1. Read applicable `AGENTS.md` and repo instructions.
2. Inspect only code, config, docs, and tests needed for task understanding.
3. Never edit/create files, spawn subagents, run destructive commands, commit, push, or open PRs.
4. State minor assumptions; record material uncertainty.
5. Produce concrete plan with outcome, current behavior/evidence, likely files/components, ordered steps, validation/tests, risks, assumptions, and open decisions.
6. Stop. Request feedback or approval. Tell user to load `review-plan` next. Never implement in same turn.
