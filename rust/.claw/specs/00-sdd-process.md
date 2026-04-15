# Spec-Driven Development Process

## Default stack

- Assume the target project is a Java application unless the repository says otherwise.
- For Web projects, assume Spring Boot conventions are preferred.
- Favor simple, maintainable layered design over framework-heavy indirection.

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

## Java implementation rules

- Keep responsibilities explicit across controller, service, repository, and configuration layers.
- Prefer constructor injection and avoid field injection.
- Keep controller classes thin; put business logic in services.
- Do not expose JPA entities directly as external API contracts unless the spec explicitly allows it.
- Prefer DTOs, request objects, response objects, and mapper logic when crossing API boundaries.
- Keep method and class names aligned with domain behavior instead of framework mechanics.

## Change control

- Prefer updating code to match the spec.
- If the spec is ambiguous, contradictory, or incomplete, stop and clarify it before continuing.
- Avoid unrelated refactors unless they are required for correctness or to satisfy the spec cleanly.

## Acceptance criteria rules

- Write requirements as observable, testable behavior.
- Prefer concrete input/output and when/then statements over vague goals.
- Capture edge cases and failure behavior when they affect correctness.
- For Spring Boot features, include request format, validation rules, status codes, response shape, transaction behavior, and persistence effects when relevant.
