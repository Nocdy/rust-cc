# Feature Spec Template

## Goal

- State the user-facing outcome in one or two sentences.

## Scope

- Define what is included in this change.
- Define what is explicitly out of scope.

## User-visible behavior

- Describe the expected behavior from the user's perspective.
- Include API behavior, request and response examples, persistence effects, or workflow changes when relevant.

## Constraints

- List implementation constraints that must be preserved.
- Reuse existing modules or flows where possible instead of duplicating logic.
- State expected controller, service, repository, DTO, and validation boundaries when relevant.

## Data and validation

- Define request fields, optional fields, default values, and validation rules.
- Define response fields and any fields that must be hidden or transformed.
- Define idempotency, uniqueness, or transactional requirements when relevant.

## Acceptance criteria

- Given a valid input or action, the expected result occurs.
- Given an invalid input or edge case, the expected failure behavior occurs.
- Existing related behavior continues to work unless this spec intentionally changes it.

## Verification

- List the commands, tests, or checks required to prove the spec is satisfied.
- Prefer naming unit tests, controller tests, repository tests, and integration tests separately when applicable.
