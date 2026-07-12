---
name: controlled-parallel-work
description: Complete software work with the explorer and forge custom agents under tight scope. Use only when user explicitly requests subagents, parallel work, exploration, or delegated implementation. Avoid small or sequential tasks.
---

# Controlled Parallel Work

Use only configured `explorer` and `forge` agents.

## Rules

- Use at most one `explorer` and one `forge`; one or zero may suffice.
- Forbid nested delegation.
- Give narrow, non-overlapping scopes. Never duplicate work.
- `explorer`: read-only evidence, paths, symbols, constraints, risks.
- `forge`: implement one approved plan with smallest complete patch. Never use without approved plan.

## Workflow

1. Read applicable `AGENTS.md` and repo instructions.
2. Spawn `explorer` only when focused investigation helps. Verify returned evidence.
3. Confirm approved plan before spawning `forge`. Give exact scope, constraints, and checks.
4. Wait for each required result. `forge` owns implementation; parent owns synthesis and final verification.
5. Inspect patch. Run narrow checks. Fix only caused failures.
6. Never commit, push, open PRs, or deploy unless requested.

Stop after implementation and targeted checks. Report agent scopes, changes, validation, unresolved risks. Skip optional work.
