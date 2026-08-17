# Repository Architecture

## Purpose

This document defines the structural distinction between **repository governance** and **case documentation** within the Expediente Maestro Migratorio (EMM).

## Architectural decision

The repository separates two different concepts that previously shared the same `00-governance` name:

- `repository-governance/` — governance, integrity, traceability, verification and lifecycle controls for the repository as infrastructure.
- `docs/` — substantive case documentation, organized by case-oriented domains.

The separation is intentional. Repository governance describes **how the repository is controlled**; case documentation describes **what the case contains**.

## Current structure

```text
/
├── repository-governance/
│   ├── INTEGRITY_AUDIT_EMM-001.md
│   ├── POST_MERGE_VERIFICATION_*.md
│   ├── TRACEABILITY_REGISTER.md
│   └── VERIFICATION_REGISTER.md
├── docs/
│   └── case-governance/
│       ├── DOCUMENT_STATUS_MODEL.md
│       ├── PR_CONTROL_PROTOCOL.md
│       ├── TRACEABILITY_REGISTER.md
│       ├── VERIFICATION_REGISTER.md
│       └── VERIFICATION_*.md
├── README.md
└── CHANGELOG.md
```

The similarly named registers under `repository-governance/` and `docs/case-governance/` are **layer-scoped records** and must not be treated as interchangeable. The former concerns repository infrastructure; the latter concerns governance of case documentation.

## Intended evolution

The `docs/` layer may grow into clearly separated case domains such as:

- `docs/case-foundation/` — foundational case context and scope.
- `docs/case-governance/` — rules and lifecycle controls specific to case documentation.
- `docs/evidence/` — evidence records, manifests and provenance information.
- `docs/facts/` — structured factual records and fact identifiers.
- `docs/documents/` — documentary inventory and document-level records.
- `docs/verifications/` — case-level verification records where appropriate.
- `docs/legal-analysis/` — legal analysis and lawyer-facing working material, when incorporated.

These are target architectural domains, not claims that their substantive contents already exist.

## Boundary rule

Repository governance MUST NOT be confused with case evidence, and case evidence MUST NOT be treated as repository governance merely because it is stored in Git.

A Git commit, Pull Request, hash or verification record can establish a repository event and its recorded integrity properties. It does not, by itself, establish the truth of an underlying legal fact or the material authenticity of an external document.

## Compatibility principle

The architecture is intentionally modular and standards-oriented so that future institutional interoperability can be introduced without requiring structural reconstruction or retrospective rewriting of the historical chain.

This compatibility is architectural only. It does not create present subordination, dependency or legal incorporation into any external institutional system.

## Change control

Structural changes to this architecture must be introduced through the repository's controlled Pull Request process and recorded in the CHANGELOG. Historical verification events must not be rewritten merely to conform to a later architecture.
