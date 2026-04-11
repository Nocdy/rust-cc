# Spec-Driven Development Process

## Core rule

- All non-trivial code changes must start from a spec.
- If a requested feature is not covered by an existing spec, create or update a spec before implementation.
- Implementation must satisfy the accepted spec and should not add extra behavior without explicit approval.

## Required workflow

1. Read the relevant spec files before editing code.
2. Restate the requested behavior as explicit acceptance criteria.
3. Identify the smallest set of files and modules that must change.
4. Implement only what is required to satisfy the spec.
5. Run the relevant verification commands.
6. Report which spec was implemented and whether verification passed.

## Change control

- Prefer updating code to match the spec.
- If the spec is ambiguous, contradictory, or incomplete, stop and clarify it before continuing.
- Avoid unrelated refactors unless they are required for correctness or to satisfy the spec cleanly.

## Acceptance criteria rules

- Write requirements as observable, testable behavior.
- Prefer concrete input/output and when/then statements over vague goals.
- Capture edge cases and failure behavior when they affect correctness.
