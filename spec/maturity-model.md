# docs-spec Maturity Model

The maturity model helps projects adopt `docs-spec` gradually.

## Level 0 — Unstructured

Documentation exists, but it is scattered, incomplete, or difficult to navigate.

Common signs:

- README is the only documentation.
- Setup instructions are incomplete.
- Important information lives only in issues or discussions.
- No clear documentation index exists.

## Level 1 — Basic Repository Docs

Minimum practical documentation exists.

Requirements:

- Root `README.md`
- License file
- Basic installation instructions
- Basic usage example
- Contribution instructions or link to them

Recommended files:

```text
README.md
LICENSE
CONTRIBUTING.md
SECURITY.md
```

## Level 2 — Structured Documentation

Documentation is organized by purpose.

Requirements:

- `/docs` directory
- `docs/README.md`
- `docs/getting-started.md`
- at least two document categories, such as `guides` and `reference`
- links from root README to documentation index

Recommended layout:

```text
docs/
├── README.md
├── getting-started.md
├── guides/
├── reference/
└── changelog.md
```

## Level 3 — Maintained Documentation System

Documentation is treated as part of project quality.

Requirements:

- all Level 2 requirements
- `docs-manifest.json`
- documented ownership or review process
- release documentation workflow
- link checking or documentation validation
- changelog or release notes
- documentation templates

Recommended additions:

```text
docs-manifest.json
templates/
tests/docs-checklist.md
```

## Adoption Recommendation

Most projects should aim for Level 2 first.

Level 3 is recommended for projects with:

- frequent releases
- multiple maintainers
- external users
- security-sensitive deployments
- ecosystem or standards role
