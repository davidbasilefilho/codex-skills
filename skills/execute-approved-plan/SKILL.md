---
name: execute-approved-plan
description: Implement an already-approved software plan with focused changes and targeted tests, then stop. Use after plan review or explicit approval. Do not use for exploration or unapproved redesign.
---

# Execute Approved Plan

1. Identify approved plan and boundaries. If missing, state that and stop; do not invent broad implementation.
2. Read applicable `AGENTS.md` and repo instructions.
3. Do not spawn subagents.
4. Change required files only. Smallest complete patch wins.
5. Preserve architecture, behavior, naming, and style unless plan requires change.
6. Add no optional cleanup, refactor, dependency, feature, compatibility path, or formatting churn.
7. Run narrow relevant tests, type checks, linters, or builds. Fix only failures caused by patch; report unrelated failures without expanding scope.
8. Never commit, push, open PRs, or deploy unless requested.

Stop after implementation and targeted validation. Report changes, validation, and directly relevant unresolved issues. Skip optional polish.
