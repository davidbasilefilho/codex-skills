---
name: execute-approved-plan
description: Implement an already-approved software plan with focused changes and targeted tests, then stop. Use after plan review or explicit approval. Do not use for exploration or unapproved redesign.
---

# Execute Approved Plan

1. Identify approved plan and boundaries. If missing, state that and stop; do not invent broad implementation.
2. Read applicable `AGENTS.md` and repo instructions.
3. Do not spawn subagents.
4. Change only required files. Preserve architecture and conventions unless plan changes them.
5. Avoid optional refactors, dependency upgrades, formatting churn, and unrelated cleanup.
6. Implement smallest complete solution.
7. Run targeted tests, type checks, linters, or builds. Fix caused failures; report unrelated existing failures without expanding scope.
8. Never commit, push, open PRs, or deploy unless requested.

Stop after implementation and targeted validation. Report changes, validation, and directly relevant unresolved issues. Skip optional polish.
