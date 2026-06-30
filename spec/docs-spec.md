# Documentation Structure Specification

Version: 0.1.0  
Status: Draft  
Maintainer: Open Source Standards Initiative

## 1. Overview

The Documentation Structure Specification, known as `docs-spec`, defines a standard layout and content model for open-source project documentation.

The specification is designed to be simple enough for small projects and structured enough for larger projects with multiple contributors, releases, and governance requirements.

## 2. Terminology

The following terms are used throughout this specification:

- **MUST** means the requirement is mandatory for conformance.
- **SHOULD** means the requirement is strongly recommended but may be omitted with justification.
- **MAY** means the item is optional.
- **Project root** means the top-level directory of the repository.
- **Documentation root** means the primary documentation directory, usually `/docs`.
- **Document type** means a defined category of documentation such as guide, concept, reference, or tutorial.

## 3. Core Requirements

A project implementing this specification MUST provide a discoverable documentation entry point.

At minimum, the project SHOULD include:

```text
README.md
docs/README.md
docs/getting-started.md
```

A project MAY publish documentation to an external site, but the repository SHOULD remain readable on its own.

## 4. Required Root Files

The following files SHOULD exist at the repository root:

| File | Requirement | Purpose |
|---|---:|---|
| `README.md` | MUST | Primary project entry point |
| `LICENSE` | MUST | License terms |
| `CONTRIBUTING.md` | SHOULD | Contribution instructions |
| `SECURITY.md` | SHOULD | Security reporting instructions |
| `CODE_OF_CONDUCT.md` | MAY | Community conduct expectations |
| `CHANGELOG.md` | MAY | Release history if not kept in `/docs` |
| `docs-manifest.json` | SHOULD | Machine-readable documentation index |

## 5. Documentation Root

The documentation root SHOULD be named:

```text
docs/
```

Alternative names MAY be used when required by tooling, but `/docs` is the preferred default.

The documentation root SHOULD include:

```text
docs/
├── README.md
├── getting-started.md
├── concepts/
├── guides/
├── reference/
├── tutorials/
└── changelog.md
```

## 6. Documentation Categories

Projects SHOULD separate documentation into the following categories.

### 6.1 Getting Started

A getting-started document explains the fastest path from zero to a working project.

It SHOULD include:

- installation instructions
- basic configuration
- first successful run
- common setup problems
- links to deeper documentation

### 6.2 Concepts

Concept documents explain ideas, architecture, design models, terminology, and mental models.

Concept documents SHOULD answer: **What is this and why does it work this way?**

### 6.3 Guides

Guide documents explain how to complete practical tasks.

Guides SHOULD answer: **How do I do a specific thing?**

### 6.4 Reference

Reference documents provide complete, precise, and lookup-oriented information.

Reference documents MAY include:

- API references
- CLI references
- configuration keys
- environment variables
- error codes
- schemas

### 6.5 Tutorials

Tutorials provide step-by-step learning paths.

Tutorials SHOULD be beginner-friendly and outcome-oriented.

### 6.6 Changelog

A changelog records meaningful project changes over time.

Projects MAY keep changelogs at either:

```text
CHANGELOG.md
```

or:

```text
docs/changelog.md
```

The location SHOULD be linked from both the root README and documentation index.

## 7. Document Naming

Documentation files SHOULD use lowercase kebab-case.

Recommended:

```text
getting-started.md
configuration-reference.md
release-process.md
```

Not recommended:

```text
GettingStarted.md
configuration reference.md
release_process.md
```

## 8. Document Front Matter

Projects MAY use front matter when supported by their documentation tooling.

Recommended fields:

```yaml
title: Getting Started
description: Install and run the project for the first time.
doc_type: guide
status: stable
last_updated: 2026-01-01
```

Front matter SHOULD NOT be required for repository readability.

## 9. Documentation Index

`docs/README.md` SHOULD act as a human-readable documentation index.

It SHOULD include:

- a short introduction
- links to major documentation sections
- recommended reading paths
- contributor guidance for documentation updates

## 10. Machine-Readable Manifest

Projects SHOULD include a `docs-manifest.json` file at the repository root.

The manifest provides machine-readable documentation metadata.

Example:

```json
{
  "spec": "docs-spec",
  "version": "0.1.0",
  "documentation_root": "docs",
  "sections": [
    {
      "title": "Getting Started",
      "path": "docs/getting-started.md",
      "type": "guide",
      "status": "stable"
    }
  ]
}
```

## 11. Link Integrity

Projects SHOULD regularly check documentation links.

Internal links SHOULD use relative paths where possible.

External links SHOULD be reviewed during release or documentation maintenance cycles.

## 12. Versioning

Projects with versioned releases SHOULD document which versions their documentation applies to.

Documentation MAY be organized by version when needed:

```text
docs/
├── latest/
├── v1/
└── v2/
```

Small projects SHOULD avoid unnecessary version complexity.

## 13. Generated Documentation

Generated documentation MAY be included, but generated output SHOULD NOT replace human-authored overview, concepts, and usage guides.

Generated files SHOULD be clearly marked.

## 14. Accessibility and Readability

Documentation SHOULD use:

- clear headings
- short paragraphs
- descriptive links
- meaningful alt text for images
- code examples with explanations
- accessible diagrams where possible

## 15. Conformance

A project conforms to `docs-spec` when it:

1. Provides a root `README.md`.
2. Provides a discoverable documentation root.
3. Separates major documentation types.
4. Provides a documentation index.
5. Maintains documentation alongside project changes.

Conformance levels are defined in `spec/maturity-model.md`.
