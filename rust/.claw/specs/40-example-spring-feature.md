# Example Feature Spec: Create Order API

## Goal

- Add an HTTP endpoint that creates an order and returns the created order summary.

## Scope

- Accept a create-order request through a REST controller.
- Validate required fields before business processing.
- Persist the new order and return a response DTO.

## Out of scope

- Payment processing.
- Asynchronous fulfillment workflows.
- Administrative reporting endpoints.

## User-visible behavior

- `POST /api/orders` accepts JSON input for customer identifier and order items.
- On success, the API returns `201 Created` with the created order summary.
- On invalid input, the API returns a validation error response.
- On duplicate or conflicting business state, the API returns a conflict response if the project uses that pattern.

## Constraints

- Keep the controller thin and delegate business logic to a service.
- Do not expose JPA entities directly in request or response bodies.
- Apply transaction management in the service layer.
- Reuse existing exception handling and error-response conventions.

## Data and validation

- `customerId` is required.
- `items` must contain at least one entry.
- Each item requires a product identifier and a positive quantity.
- The response includes the order id, status, created timestamp, and summarized items.

## Acceptance criteria

- Given a valid request, the API creates an order and returns `201 Created`.
- Given a missing `customerId`, the API returns a validation error.
- Given an empty `items` list, the API returns a validation error.
- Given a conflicting business condition defined by the domain, the API returns the expected conflict response.
- The persisted order data matches the accepted request.

## Verification

- Run controller tests for request validation and status codes.
- Run service tests for business rules.
- Run integration tests for persistence and transaction behavior when applicable.
