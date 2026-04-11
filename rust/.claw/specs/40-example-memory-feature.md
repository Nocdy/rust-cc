# Example Feature Spec: Memory Report

## Goal

- Provide a slash command that reports the current instruction-memory state for the workspace.

## Scope

- Include the current working directory.
- Include the number of discovered instruction files.
- Include a short preview of each discovered instruction file.

## Out of scope

- Editing instruction files.
- Introducing new persistence or caching behavior.

## User-visible behavior

- When the user runs `/memory`, the CLI prints the working directory and discovered instruction files.
- When no instruction files are found, the CLI prints a clear fallback message.

## Constraints

- Reuse the existing project-context discovery logic.
- Keep output aligned with the style of other slash-command reports.

## Acceptance criteria

- Given at least one `CLAW.md` or `.claw/specs/*.md` file, `/memory` lists the discovered files.
- Given no discovered instruction files, `/memory` prints a none-found message.
- Each listed file includes its path and a short preview.

## Verification

- Run targeted tests for prompt discovery and memory-report rendering.
