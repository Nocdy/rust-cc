# Spec Coding Rules

## Purpose

- This directory stores the project-specific coding specifications for the agent.
- Every `*.md` file in `.claw/specs/` is loaded automatically at startup.

## Authoring rules

- Keep one concern per file when possible so specs stay reviewable.
- Use stable filenames with numeric prefixes such as `01-api.md` and `02-style.md`.
- Write requirements as explicit rules, constraints, and acceptance criteria.

## Agent behavior

- Read the relevant spec files before making code changes.
- Implement code to satisfy the specs first, then optimize or refactor if still consistent.
- If a requested change is not covered by the current specs, add or update a spec before making broad behavioral changes.
