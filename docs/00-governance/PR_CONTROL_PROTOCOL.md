---
id: EMM-GOV-PR-001
title: EMM Pull Request Control Protocol
version: 0.1.0
status: Draft
authority: EMM traceability layer
jurisdiction: Chile
system: Expediente Maestro Migratorio (EMM)
created: 2026-08-17
---

# EMM Pull Request Control Protocol

## 1. Purpose

Define the minimum controlled workflow for documentary changes recorded in GitHub. This protocol is intentionally compatible with later governance expansion and does not attempt to replace legal review.

## 2. Controlled change rule

A substantive documentary change should not be accepted directly into `main` when it can be represented as a reviewable Pull Request.

Minimum chain:

`controlled branch → commit(s) → Pull Request → review/verification → merge → post-merge verification`

## 3. Naming

Branch names should identify the controlled work item, for example:

`traceability/<CONTROL-ID>`

or, for later substantive work:

`docs/<DOCUMENT-ID>`

Pull Request titles should begin with the same control identifier.

## 4. Commit discipline

Each commit must describe the actual controlled change. The final merge/squash commit message must be explicitly defined as part of the project record rather than relying on GitHub's automatic suggestion.

When the founder performs a manual merge or squash-merge, the project record must provide:

- exact commit title/message;
- exact PR number;
- expected PR head SHA before merge;
- merge method;
- resulting merge SHA after acceptance.

## 5. Evidence boundary

GitHub history demonstrates repository history and controlled change history. It does not independently establish the truth of a legal fact, authenticity of an external document, or legal validity of an immigration claim.

Those claims require source-linked verification records.

## 6. Verification before acceptance

Before a substantive PR is accepted, the reviewer/process should establish:

1. scope is limited to the stated purpose;
2. source references are identifiable;
3. hashes are preserved where applicable;
4. document identifiers and versions are coherent;
5. no unsupported legal conclusion is introduced as fact;
6. changed files are consistent with the declared scope;
7. the resulting state can be traced back to the PR.

## 7. Post-merge requirement

After merge, the resulting main-branch state should be checked and recorded where the change affects the controlled expediente. A merged PR alone is not the same as a completed verification record.

## 8. Incremental architecture

This protocol is a minimum viable control layer. Future governance may add approvals, roles, evidence classes, automated validation, release gates, or lawyer-review states without invalidating historical PR records.
