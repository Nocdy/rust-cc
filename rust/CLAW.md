# CLAW.md

This repository uses Spec-Driven Development (SDD).

## Instruction sources

- Treat `.claw/specs/*.md` as the primary project specification set.
- Load and follow every markdown file in `.claw/specs/` on each agent startup.
- When multiple spec files exist, read them in filename order.

## Primary domain

- Use these specs primarily for Java development, especially Spring Boot and common Web application work.
- Default to conventions that fit layered Java services unless a project spec says otherwise.

## SDD rule

- Start non-trivial changes from a spec instead of implementing directly from an informal request.
- Keep implementation aligned with the active specs before adding new code.
- If no relevant spec exists, create or update a spec before making broad behavioral changes.
- If code and spec conflict, update the code or ask to revise the spec instead of ignoring it.
