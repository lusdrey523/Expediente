---
id: EMM-REPO-ROADMAP-001
title: EMM Repository and Documentary Evolution Roadmap
version: 1.0.0
status: Active
jurisdiction: Chile
system: Expediente Maestro Migratorio (EMM)
created: 2026-08-18
last_updated: 2026-08-18
---

# EMM Repository and Documentary Evolution Roadmap

## 1. Purpose

Define the controlled sequence by which the EMM evolves from a Git/GitHub traceability nucleus into a complete, lawyer-facing documentary system, without mixing infrastructure controls with substantive case evidence and without rewriting historical events.

This roadmap is a planning and control document. A planned stage is not evidence that the stage has already been executed.

## 2. Foundational sequence

### Stage 0 — Source baseline and bootstrap
**Status: COMPLETED**

- Preserve the audited source package and its SHA-256 linkage.
- Establish the repository and initial controlled traceability.
- Preserve the initial repository state as historical context.

### Stage 1 — Minimum traceability and governance
**Status: COMPLETED**

- Establish the Pull Request control protocol.
- Establish verification and document-status models.
- Register controlled changes and post-merge verification.

### Stage 2 — Integrity and temporal-control audit
**Status: COMPLETED WITH CONDITIONS**

- Audit Git/PR integrity.
- Define evidence-chain requirements.
- Define the separation of fact time, emission, acquisition, observation, incorporation, modification and verification time.
- Record that substantive evidence and factual chronology remain to be reconstructed.

### Stage 3 — Infrastructure synchronization and architectural separation
**Status: COMPLETED**

- Keep `repository-governance/` explicitly separate from `docs/`.
- Maintain `README.md` and `CHANGELOG.md` as infrastructure representations.
- Reconcile the state after each controlled infrastructure change.
- Remove bootstrap-only artifacts once their historical existence is preserved by Git.

### Stage 4 — Documentary reconstruction of the audited case package
**Status: NEXT — NOT YET EXECUTED**

Execute incrementally from the audited baseline, not by importing an uncontrolled bulk state.

Initial controlled sequence:

1. Inventory and register the source documents/evidence.
2. Establish or reconcile the `EVIDENCE_REGISTER` and evidence manifest.
3. Preserve source hashes and provenance/receipt information.
4. Establish the next stable evidence identifiers and relationships.
5. Build the controlled evidence/document index.
6. Reconstruct the factual timeline using explicit temporal fields.
7. Build the FACT → EVIDENCE → DOCUMENT relationships.
8. Record legal questions/issues without prematurely converting them into definitive legal arguments.
9. Re-audit the integrated state and create a new persistent package/state snapshot when required by the operating procedure.

### Stage 5 — Legal review preparation
**Status: FUTURE**

- Produce lawyer-facing summaries and issue indexes from verified underlying records.
- Maintain explicit links from every conclusion or question to its supporting facts/evidence/documents.
- Prepare submission/PDF outputs only after documentary integrity gates are satisfied.

### Stage 6 — Lawyer-facing application layer
**Status: FUTURE — ARCHITECTURE ONLY**

The eventual interface may expose controlled case information through a web application suitable for direct lawyer interaction.

Requirements already established at architectural level:

- secure authentication and authorization;
- role-based access to case sections;
- clear separation between case data and repository governance;
- auditable interactions and document references;
- no exposure of secrets or private credentials through GitHub Pages;
- interface generated from controlled repository data rather than becoming the authoritative source itself.

GitHub Pages may serve a presentation layer where appropriate, but it is not itself the authentication/security boundary for sensitive case material.

### Stage 7 — Multicaso architecture
**Status: FUTURE — ARCHITECTURE ONLY**

Evolve the single-case model into a multi-case system in which each case has an isolated namespace, evidence set, facts, documents, verifications, legal analysis and access policy while sharing the same infrastructure control principles.

The architecture must support an arbitrary number of cases without requiring a redesign of the underlying traceability model.

### Stage 8 — Future interoperability
**Status: FUTURE**

Design conventions so that the system can later interoperate with broader institutional standards without creating present-day dependency, subordination or coupling to any external governance system.

## 3. Current gate

**Current controlled gate:** complete the documentary reconstruction foundation before building the application layer.

The immediate work is therefore documentary: evidence, facts, provenance, temporal controls, document relationships and lawyer-review questions.

The web application, authentication and multicaso capabilities are downstream architecture and must not be allowed to displace the evidentiary/documentary reconstruction.

## 4. Continuity rule

Every completed stage must be represented by controlled changes and, where applicable, verification. Planned stages must not be described as completed until their acceptance state is recorded.

Historical PRs and verification records remain immutable in meaning. Later corrections are represented as new controlled events.
