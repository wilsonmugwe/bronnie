# Contributing to BRONNIE

## Branching

Development should not normally occur directly on `main`.

Use short-lived branches.

Examples:

* `feature/email-ingestion`
* `feature/invoice-processing`
* `fix/duplicate-invoices`
* `infra/aws-networking`
* `docs/discovery-plan`
* `refactor/workflow-service`

## Commits

BRONNIE uses Conventional Commit-style messages.

Examples:

`feat: add enquiry classification`

`fix: prevent duplicate invoice processing`

`docs: add discovery plan`

`infra: add AWS networking module`

`test: add invoice extraction tests`

`refactor: separate workflow routing logic`

`chore: configure development tooling`

## Development Workflow

Issue
→ Branch
→ Implementation
→ Tests
→ Pull Request
→ Review
→ CI
→ Merge

## Pull Requests

Pull requests should explain:

* why the change exists,
* what changed,
* how it was tested,
* security implications,
* and relevant issues.

## Security

Never commit secrets or production-sensitive customer information.

## Documentation

Changes affecting architecture, behaviour, deployment, integrations, or important technical decisions should update the appropriate documentation.

Significant architecture decisions should receive an Architecture Decision Record.
