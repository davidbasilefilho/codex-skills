---
name: plan-and-stop
description: Inspect and plan a software task, then stop before editing. Use for planning, scoping, implementation design, or a requested review checkpoint. Do not use when the user explicitly wants immediate implementation without a planning pause.
---

# Plan and stop

Treat the user's prompt as the task to plan.

## Workflow

1. Read the applicable `AGENTS.md` files and repository instructions.
2. Inspect only the code, configuration, documentation, and tests needed to understand the task.
3. Do not edit or create files.
4. Do not spawn subagents.
5. Do not run destructive commands, create commits, push branches, or open pull requests.
6. Resolve minor ambiguity with clearly stated assumptions. Record material uncertainty in the plan.
7. Produce a concrete implementation plan containing:
   - the intended outcome;
   - relevant current behavior and evidence;
   - files or components likely to change;
   - ordered implementation steps;
   - validation and targeted tests;
   - risks, assumptions, and open decisions.
8. Stop after the plan and request the user's feedback or approval.

Do not begin implementation in the same turn, even when the plan appears straightforward.
