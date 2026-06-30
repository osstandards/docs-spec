# Documentation Navigation Standard

Documentation SHOULD be easy to navigate from both the repository and a published documentation site.

## Required Entry Points

Projects SHOULD provide links to documentation from:

- root `README.md`
- `docs/README.md`
- release notes or changelog
- contribution documentation

## Recommended Navigation Order

1. Overview
2. Getting Started
3. Tutorials
4. Guides
5. Concepts
6. Reference
7. Changelog
8. Contributing
9. Security

## Documentation Index Example

```markdown
# Documentation

## Start Here

- [Getting Started](getting-started.md)
- [Installation](guides/installation.md)

## Learn

- [Core Concepts](concepts/core-concepts.md)
- [Architecture](concepts/architecture.md)

## Use

- [Configuration Guide](guides/configuration.md)
- [CLI Reference](reference/cli.md)
```

## Linking Rules

- Prefer relative links for internal docs.
- Use descriptive link text.
- Avoid “click here.”
- Link to canonical documents rather than duplicate explanations.
- Avoid orphan pages.
