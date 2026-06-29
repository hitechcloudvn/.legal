# Pull Request Process

This document defines the expected review and merge workflow.

## 1. Pull request scope

Prefer pull requests that stay within one main concern:

- legal document updates
- policy corrections and clarifications
- documentation improvements
- licensing and compliance updates
- dependency or workflow maintenance

If a pull request crosses areas, explain why the changes must land together.

## 2. Review expectations

### Legal documents

- include a summary of what changed and why
- identify affected documents and cross-references
- verify English is primary, Vietnamese follows

### Documentation

- identify the synchronized files updated together
- note any reviewer risk where behavior could not be exercised directly

### Governance and policy

- identify affected policy area
- verify consistency across all related documents
- note any legal or compliance implications

## 3. Branch protection recommendation

Recommended protection for `main`:

- require pull requests before merge
- require at least one approval
- require code owner review
- dismiss stale approvals on new commits
- require conversation resolution before merge
- block force pushes
- block branch deletion

## 4. Labels and ownership

Recommended labels:

- `documentation`
- `governance`
- `licensing`
- `security`
- `dependencies`

`CODEOWNERS` should remain aligned with the repository structure so reviewers are requested automatically.

## 5. Automation and dependency updates

- keep dependency pull requests small and reviewable
- refresh stale dependency branches before merge
- keep workflow permissions minimal
- use [`maintenance.md`](./maintenance.md) when touching repository automation

Repository workflows run automatically when their path and event filters match. Dependabot remains active with bounded pull request limits.

## 6. Related document review

When changing legal, licensing, or policy content, review and update as needed:

- [`README.md`](../README.md)
- [`NOTICE`](../NOTICE)
- [`LICENSE`](../LICENSE)
- [`COMMERCIAL-LICENSE.md`](../COMMERCIAL-LICENSE.md)
- [`docs/licensing.md`](./licensing.md)
- [`docs/legal-notice.md`](./legal-notice.md)
- [`docs/legal-vi.md`](./legal-vi.md)

## 7. Merge guidance

Prefer squash merge for routine changes unless preserving commit history is important for audit or release reasons.
