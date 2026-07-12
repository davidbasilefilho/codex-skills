---
name: execute-approved-plan
description: Implement an already-approved software plan with focused changes and targeted tests, then stop. Use after plan review or explicit approval. Do not use for exploration or unapproved redesign.
---

# Execute Approved Plan

1. Read plans in `.agents/plans/`. If none exist, stop. If one exists, use it. If multiple exist, ask user which plan to use and stop.
2. Read selected approved plan and boundaries. Do not invent broad implementation.
3. Read applicable `AGENTS.md` and repo instructions.
4. Do not spawn subagents.
5. Change required files only. Smallest complete patch wins.
6. Preserve architecture, behavior, naming, and style unless plan requires change.
7. Add no optional cleanup, refactor, dependency, feature, compatibility path, or formatting churn.
8. Run narrow relevant tests, type checks, linters, or builds. Fix only failures caused by patch; report unrelated failures without expanding scope.
9. Never commit, push, open PRs, or deploy unless requested.

Stop after implementation and targeted validation. Report changes, validation, and directly relevant unresolved issues. Skip optional polish.
