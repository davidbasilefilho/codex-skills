---
name: tdd
description: Apply test-driven development for features or fixes. Use when the user requests test-first work, red-green-refactor, or integration tests.
---

# Test-Driven Development

Read `CONTEXT.md` when present; match domain terms and respect relevant ADRs. See [tests.md](tests.md) and [mocking.md](mocking.md).

## Test Surface

Test behavior through public interfaces, never internals. Tests must read as specifications and survive refactors.

A seam is a public boundary where behavior is observed. Before testing, list proposed seams and confirm them with user. Write no test at an unconfirmed seam.

## Reject

- Implementation-coupled tests: private methods, internal mocks, side-channel verification.
- Tautologies: expected value recomputed like production code. Use independent literals, worked examples, or spec facts.
- Horizontal slicing: all tests before all code. Use vertical tracer bullets.

## Loop

1. Pick one confirmed seam and behavior.
2. Write one failing test; observe red.
3. Add only enough implementation for green. Avoid speculative behavior.
4. Repeat one vertical slice at a time.

Keep refactoring outside red-green cycles; perform it during review after tests pass.
