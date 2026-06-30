# Standard Document Types

`docs-spec` defines standard documentation types to reduce ambiguity.

## Overview

| Type | Purpose | Typical Location |
|---|---|---|
| Overview | Explain what the project is | `README.md`, `docs/README.md` |
| Getting Started | Help users achieve first success | `docs/getting-started.md` |
| Concept | Explain ideas and architecture | `docs/concepts/` |
| Guide | Explain how to complete a task | `docs/guides/` |
| Tutorial | Teach through a step-by-step path | `docs/tutorials/` |
| Reference | Provide precise lookup material | `docs/reference/` |
| Governance | Explain project rules and processes | root files or `docs/governance/` |
| Release Notes | Explain project changes | `CHANGELOG.md` or `docs/changelog.md` |

## Recommended Metadata

Each document MAY include metadata:

```yaml
title: Configuration Reference
doc_type: reference
status: stable
owner: maintainers
last_updated: 2026-01-01
```

## Status Values

Recommended status values:

- `draft`
- `review`
- `stable`
- `deprecated`
- `archived`

## Audience Values

Recommended audience values:

- `user`
- `contributor`
- `maintainer`
- `operator`
- `integrator`
- `security-reviewer`
