---
name: define-goal
description: Define or refine a concrete, measurable goal before work starts. Use when asked to create/set a goal, use the goal tool, clarify success criteria, or quantify fuzzy intent. Do not use for ordinary implementation or durable plans, snapshots, logs, or execution artifacts.
---

# Define Goal

Turn intent into one verifiable, bounded objective. Do not force goal creation for ordinary work.

## Workflow

1. Restate outcome, target artifact/system/environment, verification, scope, exclusions, and stop/escalation condition.
2. Add meaningful numbers when possible: exact checks; latency, cost, quality, coverage, error, or reliability thresholds; paths/environments/deadlines; required evidence counts. Avoid decorative precision.
3. Repair activity goals (`make progress`, `investigate`, `improve`) into observable outcomes. Ask one short question only when missing scope or validator could change intent.
4. Call `get_goal` before creation:
   - No active goal: create only after quality check.
   - Matching active goal: reuse it.
   - Conflicting active goal: ask whether to finish it, mark complete if done, or use separate goal-backed thread.
5. Call `create_goal` with one concise objective containing evidence and material scope bounds. Include token budget only when explicitly requested.

Never create intermediate plans, snapshots, ledgers, decision logs, or resume files.

## Quality Check

Objective must answer:

- What becomes true?
- What exact evidence proves it?
- What binary or quantitative threshold defines success?
- What is in/out of scope?
- When must work stop for user input?

Domain hints:

- Bug: reproduce, fix, failing-then-passing validator.
- Test: exact command and pass condition.
- Performance: metric, threshold, method, run count.
- Quality: observable review or checks.
- Research: decision enabled, source scope, evidence standard.
- Operations: healthy state, monitoring window, failure threshold, rollback/escalation.

If no honest metric exists, propose a binary validator and ask for confirmation.
