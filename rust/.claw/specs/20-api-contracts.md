# API And Command Contracts

## Contract rules

- Treat public CLI behavior, slash-command output, config keys, and persisted data as contracts.
- Do not change observable contract behavior without a spec that explicitly describes the change.
- Preserve backward-compatible behavior unless the spec states a breaking change is intended.

## Output stability

- Keep report and command output structurally consistent when extending existing commands.
- Prefer additive output changes over destructive formatting changes.
- If output is consumed by tests or tools, update those surfaces in the same change.

## Reuse rules

- Reuse runtime discovery and prompt-building logic instead of reimplementing it in the CLI layer.
- Keep contract shaping close to the owning module so behavior stays coherent.
