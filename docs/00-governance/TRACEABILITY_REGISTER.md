---
id: EMM-TRACE-REGISTER-001
title: EMM Traceability Register
version: 0.2.0
status: Active
jurisdiction: Chile
system: Expediente Maestro Migratorio (EMM)
ownership: Luis Fernando Breto Ruiz
created: 2026-08-17
---

# EMM Traceability Register

## 1. Purpose

This register establishes the auditable linkage between the Expediente Maestro Migratorio and the Git repository `lusdrey523/Expediente`.

Git history and Pull Requests are used as a traceability layer for controlled documentary changes. They do not replace primary evidence, official records, or legal review.

## 2. Bootstrap record

| Field | Value |
|---|---|
| Bootstrap identifier | EMM-BOOTSTRAP-001 |
| Repository | `lusdrey523/Expediente` |
| Default branch | `main` |
| Bootstrap branch | `traceability/EMM-BOOTSTRAP-001` |
| Initial repository commit observed | `98691b7ca4578d9a2b4453a1953bdc9422db3abe` |
| Initial commit date | 2026-08-17 |
| Initial commit content | `1.md` containing test content; retained as historical repository state |
| Bootstrap PR | PR #1 |
| Bootstrap merge SHA | `b172d374785e062cf53cdb402650a5f211ec9954` |

## 3. Source expediente baseline

The bootstrap process is linked to the previously audited EMM source package:

- Source package: `Legalbreto-main.zip`
- SHA-256: `26f599f89d7e546deb53ad316123f16cf6683015547a7f5bc5eb2c99f628435f`
- Reported inventory: 48 files
- Bootstrap assessment: `EMM_SYSTEM_ASSESSMENT_001`

This repository entry records the relationship to that source package; it does not assert that the ZIP itself is stored in this repository.

## 4. Traceability model

Each future controlled change should be represented through the following chain where applicable:

`Source evidence → Documentary interpretation → Controlled document → Git commit → Pull Request → Verification → Accepted state`

A Git commit proves that a repository state existed at a particular point in history. A Pull Request additionally records the proposed change, its rationale, review discussion and acceptance/rejection outcome.

## 5. Current governance layer

The following minimum controls are now incorporated through controlled change:

1. `EMM-GOV-PR-001` — Pull Request Control Protocol.
2. `EMM-GOV-VERIFICATION-001` — Verification Register.
3. `EMM-GOV-STATUS-001` — Document Status Model.

These controls are intentionally modular. They may be extended by later EMM governance without invalidating historical records.

## 6. Scope boundary

This traceability layer does not certify legal facts, evidence authenticity, immigration eligibility, or legal conclusions. Those matters require source-linked documentary verification and, where appropriate, independent legal review.

## 7. Continuity rule

Historical records should be preserved. Corrections and superseding assessments must be represented as new controlled changes rather than silently rewriting the historical record.
