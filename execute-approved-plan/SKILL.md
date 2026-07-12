---
name: execute-approved-plan
description: Implement an already-approved software plan with focused changes and targeted tests, then stop. Use after a plan has been reviewed or when the user explicitly identifies a plan as approved. Do not use for exploration-only work or broad unapproved redesigns.
---

# Execute an approved plan

Implement the approved plan from the current task or conversation.

## Preconditions

1. Identify the approved plan and its boundaries.
2. If no approved plan is available, do not invent a broad implementation. State that the approved plan is missing and stop.
3. Read the applicable `AGENTS.md` files and repository instructions before changing code.

## Execution

1. Do not spawn subagents.
2. Change only files required by the approved plan.
3. Preserve existing architecture and conventions unless the plan explicitly changes them.
4. Avoid optional refactors, dependency upgrades, formatting churn, and unrelated cleanup.
5. Implement the smallest complete solution that satisfies the plan.
6. Run the most targeted relevant tests, type checks, linters, or build commands.
7. Fix failures caused by the changes. Report unrelated pre-existing failures without expanding scope.
8. Do not create commits, push branches, open pull requests, or perform deployment unless explicitly requested.

## Completion

Stop when the implementation and targeted validation are complete.

Return a concise summary containing:
- what changed;
- validation performed and its result;
- any unresolved issue or follow-up that is directly relevant.

Do not continue into optional polish or additional work.
