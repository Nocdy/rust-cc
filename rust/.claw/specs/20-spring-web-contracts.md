# Spring Web Contracts

## API contract rules

- Treat public HTTP endpoints, request payloads, response payloads, status codes, and error bodies as contracts.
- Do not change observable API behavior without a spec that explicitly describes the change.
- Preserve backward-compatible behavior unless the spec declares a breaking change.

## Controller rules

- Keep controllers focused on transport concerns: request mapping, validation, authentication context, and response shaping.
- Do not place core business logic in controllers.
- Use explicit request and response DTOs for public APIs.

## Validation and error handling

- Use Bean Validation for request validation when appropriate.
- Return consistent status codes for validation, not-found, conflict, and server-error cases.
- Keep error response structure consistent across endpoints when the project already has an error format.

## Persistence and transaction rules

- Keep transaction boundaries in the service layer unless there is a strong reason not to.
- Avoid leaking persistence-specific details into controller contracts.
- Be explicit about create, update, delete, and query semantics when repository behavior affects correctness.

## Compatibility rules

- Prefer additive response changes over removing or renaming existing fields.
- If contract behavior is used by tests or clients, update those surfaces in the same change.
