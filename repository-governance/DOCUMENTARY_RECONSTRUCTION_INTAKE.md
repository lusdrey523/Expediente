---
id: EMM-RECON-INTAKE-001
title: Documentary Reconstruction Intake Control
version: 1.0.0
status: Active
jurisdiction: Chile
system: Expediente Maestro Migratorio (EMM)
---

# Documentary Reconstruction Intake Control

## Objective

Control the transition from the infrastructure-only stage into substantive documentary reconstruction.

## Mandatory intake sequence

1. Identify the exact source package presented for reconstruction.
2. Calculate and record its SHA-256 independently.
3. Preserve the source package as the immutable input reference.
4. Inventory files without changing source contents.
5. Map existing identifiers and registers from the audited baseline.
6. Detect discrepancies before creating or updating controlled records.
7. Create the first controlled evidence-register layer.
8. Record unknown, missing or unverifiable attributes explicitly rather than inferring them.

## Preservation rules

- Original source content is not silently normalized in place.
- Normalized representations must remain distinguishable from source artifacts.
- Historical timestamps are preserved with their source and precision.
- Hashes are calculated over the exact preserved artifact used as the reference.
- Any correction after incorporation is represented as a new controlled event.

## Blocking conditions

The reconstruction must stop before substantive incorporation if:

- the source package cannot be identified;
- its integrity cannot be independently verified;
- the baseline used for reconstruction differs from the declared audited baseline without explanation; or
- a proposed change would require rewriting an historical verification event.

## Output of F-01

The minimum F-01 output is a controlled evidence-register foundation and source receipt that can be independently checked against the declared baseline.
