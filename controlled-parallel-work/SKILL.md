---
name: controlled-parallel-work
description: Complete a software task with tightly limited parallel subagents, then synthesize and implement centrally. Use only when the user explicitly requests parallel work, subagents, an explorer, or an independent reviewer. Do not use for small or sequential tasks.
---

# Controlled parallel work

Use parallelism only when it provides clear value for the user's task.

## Limits

1. Use at most two subagents in total.
2. Never allow nested delegation.
3. Tell every subagent explicitly not to spawn additional agents.
4. Keep subagents read-only unless the user explicitly requests independent implementations.
5. Do not create duplicate investigations or assign overlapping scopes.

## Roles

Use only the roles that are useful:

- **Explorer:** inspect relevant code and return evidence, file paths, constraints, and a recommended approach.
- **Reviewer:** independently examine the task or proposed change for correctness, regressions, missing tests, and scope violations.

One subagent may be enough. Use zero when the task is not meaningfully parallel.

## Workflow

1. Read the applicable `AGENTS.md` files and repository instructions.
2. Define a narrow, non-overlapping assignment for each selected subagent.
3. Spawn no more than the necessary agents.
4. Wait for all selected agents to finish.
5. Verify and synthesize their findings; do not copy conclusions uncritically.
6. Make the final implementation in the parent agent.
7. Keep changes within the user's requested scope.
8. Run targeted validation and fix failures caused by the changes.
9. Do not create commits, push branches, open pull requests, or deploy unless explicitly requested.

## Completion

Stop after the implementation and targeted tests are complete.

Return a concise summary of:
- subagents used and their scopes;
- the synthesized decision;
- changes made;
- validation results;
- directly relevant unresolved risks.

Do not start optional follow-up work.
