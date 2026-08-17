---
id: EMM-GOV-VERIFICATION-001
title: EMM Verification Register
version: 0.1.0
status: Draft
jurisdiction: Chile
system: Expediente Maestro Migratorio (EMM)
created: 2026-08-17
---

# EMM Verification Register

## 1. Purpose

Provide a controlled location for recording verification events that connect source material, documentary changes, Git history and accepted states.

## 2. Verification record model

Each verification event should identify, where applicable:

| Field | Requirement |
|---|---|
| Verification ID | Unique stable identifier |
| Date | Date of verification |
| Scope | Exact files, evidence or state checked |
| Source | Source document, package, official record or prior state |
| Source hash | SHA-256 or other integrity identifier when available |
| Target | Commit, PR, document version or repository state |
| Method | Manual, automated, comparative or mixed |
| Result | PASS, PASS WITH CONDITIONS, FAIL or PENDING |
| Findings | Material observations |
| Action | Required correction or acceptance decision |
| Verifier | Person/process performing the check |

## 3. Initial registered events

| Verification ID | Scope | Target | Result | Notes |
|---|---|---|---|---|
| EMM-VER-001 | EMM GitHub traceability bootstrap | PR #1 / merge SHA `b172d374785e062cf53cdb402650a5f211ec9954` | PASS WITH CONDITIONS | Bootstrap establishes traceability infrastructure; it does not certify legal facts or source authenticity. |

## 4. Interpretation rule

A verification result applies only to the scope explicitly recorded. A PASS for repository structure or hash consistency must not be interpreted as a legal conclusion.

## 5. Pending population

Substantive evidence, facts, documentary interpretations and lawyer-facing outputs will be registered here as the EMM is reconstructed from the audited source package and later verified sources.

## 6. Continuity rule

Verification records are append-oriented. Historical verification entries should not be silently rewritten to reflect later conclusions. Corrections or superseding assessments must be recorded as new controlled events with explicit linkage to the prior record.
