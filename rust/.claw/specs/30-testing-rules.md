# Testing Rules

## Verification policy

- Every implemented spec must have verification.
- Do not claim completion if the relevant verification was not run.
- If verification cannot run, report that explicitly with the reason.

## Test selection

- Prefer targeted tests for the modules changed by the spec.
- Run broader workspace checks when the spec affects shared behavior, contracts, or cross-crate flows.
- Add or update tests when behavior changes in a way that should remain stable.

## Reporting

- Separate spec failures from unrelated pre-existing failures.
- State which commands were run and whether they passed.
