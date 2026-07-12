---
name: diagnosing-bugs
description: Diagnose hard bugs and performance regressions through a strict reproduce-minimise-hypothesise-instrument-fix loop. Use for broken, throwing, failing, flaky, slow, debug, or diagnosis requests.
---

# Diagnosing Bugs

Read `CONTEXT.md` and relevant ADRs first. Skip phases only with explicit reason.

## 1. Build Tight Feedback Loop

Create one command that catches user's exact symptom. Prefer, in order: failing test; HTTP script; CLI plus fixture/snapshot; headless browser assertion; trace replay; minimal harness; property/fuzz loop; `git bisect run`; old/new differential; last-resort human loop via `scripts/hitl-loop.template.sh`.

Tighten speed, specificity, and determinism. Pin time/randomness/network/filesystem. For flakes, raise measured reproduction rate through repetition, stress, parallelism, or timing control.

Phase ends only after running and showing one command/output that is:

- red-capable for exact bug, not generic failure;
- deterministic, or pinned to high measured flake rate;
- seconds-fast;
- agent-runnable, with humans only through HITL template.

No command, no hypothesis. If impossible, list attempts and request reproducing environment, captured artifact, or permission for temporary production instrumentation; stop.

## 2. Reproduce and Minimise

Run loop repeatedly. Confirm exact user symptom and capture error/output/timing. Remove inputs, callers, config, data, and steps one at a time; rerun after each cut. Continue until every remaining element is load-bearing.

## 3. Hypothesise

Write 3–5 ranked, falsifiable hypotheses before testing. Format: `If X causes bug, changing Y produces Z.` Discard unfalsifiable guesses. Show list to user, but proceed if unavailable.

## 4. Instrument

Map each probe to one prediction; change one variable. Prefer debugger/REPL, then targeted boundary logs. Never log everything. Tag temporary logs uniquely, e.g. `[DEBUG-a4f2]`.

For performance: establish baseline with timing harness, profiler, or query plan; then bisect. Measure before fixing.

## 5. Regression Test and Fix

Use correct seam reproducing real call-site pattern. Too-shallow test gives false confidence; if no valid seam exists, document architectural finding.

When seam exists:

1. Convert minimal repro into failing test; observe failure.
2. Apply fix; observe pass.
3. Rerun original unminimised loop.

## 6. Cleanup

Before completion:

- original repro passes;
- regression test passes, or missing seam documented;
- all `[DEBUG-...]` instrumentation removed;
- throwaway artifacts deleted or clearly isolated;
- correct hypothesis recorded in commit/PR message when one exists.

Then identify prevention. Recommend `improve-codebase-architecture` only after fix when poor seams, tangled callers, or hidden coupling contributed.
