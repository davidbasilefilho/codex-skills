---
name: review-plan
description: Review an implementation plan against repository evidence, fix concrete planning failures, then stop before implementation. Use after plan-and-stop or whenever a plan needs correctness, scope, sequencing, or validation review.
---

# Review Plan

Review plan only. Never implement.
Load `caveman` and use it to review and rewrite the plan minimally.

1. Read applicable `AGENTS.md` and plans in `.agents/plans/`.
2. If user names a plan, use it. If exactly one exists, use it. If none exist, stop. If multiple exist and none is named, ask user which plan to review and stop.
3. Read selected plan and only files needed to verify it.
4. Find common failures:
   - wrong current behavior, file, symbol, API, or dependency assumptions;
   - vague steps lacking target or outcome;
   - missing prerequisites or wrong order;
   - scope creep, optional cleanup, speculative abstraction;
   - behavior, compatibility, migration, data, security, or failure-path gaps relevant to task;
   - missing targeted tests, checks, or acceptance evidence;
   - unresolved decisions disguised as assumptions.
5. Fix every evidenced failure. Preserve valid scope and decisions. Make smallest correct plan.
6. Edit selected `.agents/plans/` file in place.
7. Report key fixes and remaining user decisions. Stop. Do not edit implementation files, spawn agents, commit, push, or open PRs.
