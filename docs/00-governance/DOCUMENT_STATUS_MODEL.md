---
id: EMM-GOV-STATUS-001
title: EMM Document Status Model
version: 0.1.0
status: Draft
jurisdiction: Chile
system: Expediente Maestro Migratorio (EMM)
created: 2026-08-17
---

# EMM Document Status Model

## 1. Purpose

Define a small, unambiguous lifecycle for controlled EMM documents. The model is deliberately minimal so additional governance can be coupled later.

## 2. Statuses

### Draft

Work product under construction. It must not be represented as verified or final.

### Review

A defined version has been submitted for structured review. Changes should occur through the controlled workflow.

### Verified

The recorded verification scope has been completed successfully. Verified means verified against the stated scope and source, not legally adjudicated.

### Verified With Conditions

The verification identified bounded conditions that are explicitly recorded and do not prevent the document from being used for the stated limited purpose.

### Superseded

A later controlled version replaces this version. The superseded document remains historically traceable.

### Archived

Retained for historical or evidentiary reasons and no longer part of the active working set.

## 3. Prohibited interpretation

`Verified` does not mean:

- legally correct in every respect;
- accepted by a Chilean authority;
- authenticated by a court or government agency;
- equivalent to lawyer approval.

Where legal review exists, it must be separately recorded.

## 4. Versioning

A document version should change when its substantive controlled content changes. Status transitions should be traceable through commits, Pull Requests and verification records.

## 5. Historical preservation

A prior version must not be silently overwritten when its historical state is material to the expediente. A new controlled change should preserve the ability to reconstruct the prior accepted state.
