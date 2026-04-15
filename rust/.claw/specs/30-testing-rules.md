# Testing Rules

## Verification policy

- Every implemented spec must have verification.
- Do not claim completion if the relevant verification was not run.
- If verification cannot run, report that explicitly with the reason.

## Test selection

- Prefer targeted tests for the modules changed by the spec.
- Run broader project checks when the spec affects shared behavior, contracts, or cross-module flows.
- Add or update tests when behavior changes in a way that should remain stable.

## Java and Spring test guidance

- Test business rules in service-layer unit tests.
- Test endpoint contracts with controller tests such as `@WebMvcTest` or the project equivalent.
- Use integration tests for persistence behavior, transaction behavior, and full request-to-database flows when correctness depends on wiring.
- Cover validation failures, not-found cases, conflict cases, and happy paths for externally visible endpoints.

## Verification commands

- Prefer the project's Gradle or Maven commands as declared by the repository.
- For Gradle projects, typical checks include `./gradlew test` and targeted test tasks.
- For Maven projects, typical checks include `mvn test` and targeted module tests.

## Reporting

- Separate spec failures from unrelated pre-existing failures.
- State which commands were run and whether they passed.
