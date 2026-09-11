# 07 Speckit Fundamentals

[← Back to Index](index.md)

Spec Kit (or `speckit`) is a professional toolkit that operationalizes Spec-Driven Development. Instead of relying on scattered chat logs, Spec Kit treats specifications as **first-class citizens** within your code repository.

## Core Concept: Specs as Code

In a Spec Kit project, the "spec" is not just a document in a wiki; it is a set of artifacts stored directly in your repository (typically under a `.specify/` or `specs/` directory).

This allows you to:
- **Version your specs**: Your requirements evolve alongside your code in Git.
- **Provide context to agents**: Any agent entering the project can read the specs to understand the intended behavior.
- **Audit changes**: You can see exactly when a requirement changed by looking at the git history of the spec file.

## Getting Started

### Installation
Spec Kit is installed via the `specify-cli`. It is recommended to use `uv` for package management:

```bash
uv tool install specify-cli
```

### Initialization
To turn a directory into a Spec Kit project, run:

```bash
specify init my-project --integration <agent-name>
```

This command creates the necessary scaffolding and integrates the Spec Kit slash commands into your chosen AI agent (e.g., Copilot, Claude, or OpenCode).

## The Project Constitution

The first step in any Spec Kit project is establishing the **Constitution**. This is done via:

`/speckit.constitution`

The Constitution defines the governing principles of the project—such as coding standards, UX guidelines, and performance requirements. This ensures that every single feature the AI builds follows the same overarching rules without you having to repeat them in every prompt.
