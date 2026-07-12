---
name: controlled-parallel-work
description: Complete a software task with at most two tightly scoped subagents, then synthesize and implement centrally. Use only when the user explicitly requests parallel work, subagents, exploration, or independent review. Avoid for small or sequential tasks.
---

# Controlled Parallel Work

Use parallelism only for independent work with clear value.

## Rules

- Use at most two subagents total; one or zero may suffice.
- Forbid nested delegation explicitly.
- Keep agents read-only unless user requests independent implementations.
- Give narrow, non-overlapping scopes; never duplicate investigation.
- Use explorer for evidence, paths, constraints, approach. Use reviewer for correctness, regressions, tests, and scope.

## Workflow

1. Read applicable `AGENTS.md` and repo instructions.
2. Assign only useful roles and scopes; tell each agent not to spawn agents.
3. Wait for results. Verify evidence; synthesize critically.
4. Implement centrally within user scope.
5. Run targeted validation; fix failures caused by changes.
6. Never commit, push, open PRs, or deploy unless requested.

Stop after implementation and targeted tests. Report agent scopes, synthesized decision, changes, validation, and relevant unresolved risks. Skip optional follow-up.
