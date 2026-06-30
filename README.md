# docs-spec

**A practical open standard for structuring open-source project documentation.**

`docs-spec` defines a reusable documentation structure for open-source repositories. It standardizes where documentation lives, what files should exist, how docs should be organized, and how maintainers can keep project documentation usable over time.

This specification is part of the **Open Source Standards Initiative (OSSI)**.

## Purpose

Open-source documentation is often inconsistent across projects. Some projects place everything in a long README. Others scatter docs across wikis, websites, issue threads, markdown files, and generated reference pages.

`docs-spec` provides a lightweight baseline that projects can adopt without requiring a specific documentation generator, programming language, framework, or hosting platform.

## Goals

- Define a predictable documentation layout for open-source repositories.
- Improve discoverability for users, contributors, maintainers, and automated tools.
- Separate conceptual, task-based, reference, and governance documentation.
- Support both in-repository reading and published documentation sites.
- Provide a practical maturity model for adoption.

## Non-goals

This specification does not require:

- A specific static site generator.
- A specific markdown flavor beyond broadly compatible Markdown.
- A specific hosting provider.
- A specific programming language or package ecosystem.
- A large documentation team.

## Repository Contents

| Path | Purpose |
|---|---|
| `spec/docs-spec.md` | Main specification |
| `spec/maturity-model.md` | Adoption levels for projects |
| `spec/document-types.md` | Standard documentation categories |
| `spec/navigation.md` | Recommended navigation model |
| `schemas/docs-manifest.schema.json` | JSON Schema for `docs-manifest.json` |
| `templates/` | Reusable documentation templates |
| `examples/basic-project/` | Example implementation |
| `rfcs/` | Proposal process for future changes |
| `tests/` | Validation checklist |

## Core Layout

A compliant project SHOULD include:

```text
.
├── README.md
├── CONTRIBUTING.md
├── SECURITY.md
├── LICENSE
├── docs/
│   ├── README.md
│   ├── getting-started.md
│   ├── concepts/
│   ├── guides/
│   ├── reference/
│   ├── tutorials/
│   └── changelog.md
└── docs-manifest.json
```

## Specification Status

Current version: **0.1.0**

Status: **Draft**

This specification is intended for early implementation, review, and iteration.

## Who Should Use This

- Open-source maintainers
- Documentation teams
- Developer relations teams
- Standards groups
- GitHub organization owners
- Project governance leads
- AI/documentation tooling builders

## Adoption Levels

`docs-spec` defines four adoption levels:

1. **Level 0 — Unstructured**
2. **Level 1 — Basic Repository Docs**
3. **Level 2 — Structured Documentation**
4. **Level 3 — Maintained Documentation System**

See [`spec/maturity-model.md`](spec/maturity-model.md).

## Quick Start

1. Create a `/docs` directory.
2. Add `docs/README.md` as the documentation index.
3. Add `docs/getting-started.md`.
4. Add folders for `concepts`, `guides`, `reference`, and `tutorials` as needed.
5. Add `docs-manifest.json` using the included schema.
6. Use the templates in `/templates` to standardize new pages.

## License

This project is licensed under the MIT License.
