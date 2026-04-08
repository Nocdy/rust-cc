# CLAW.md

This repository uses spec-driven coding.

## Instruction sources

- Treat `.claw/specs/*.md` as the primary project specification set.
- Load and follow every markdown file in `.claw/specs/` on each agent startup.
- When multiple spec files exist, read them in filename order.

## Working rule

- Keep implementation aligned with the active specs before adding new code.
- If code and spec conflict, update the code or ask to revise the spec instead of ignoring it.
