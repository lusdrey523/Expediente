---
id: EMM-STD-META-001
title: Estándar de Metadatos Documentales del Proyecto EMM
version: 1.0.0
status: Proposed
language: es-CL
jurisdiction: Chile
system: Expediente Maestro Migratorio (EMM)
document_type: standard
owner_role: Repository Administrator
created_at: 2026-08-18
last_updated_at: 2026-08-18
---

# Estándar de Metadatos Documentales del Proyecto EMM

## 1. Objetivo

Establecer un esquema único de metadatos para los documentos controlados del proyecto y eliminar la divergencia de nomenclatura, idioma y campos entre capas.

## 2. Campos obligatorios

Todo documento normativo, de gobierno, protocolo, registro, auditoría o modelo controlado debe incluir YAML front matter con:

- `id`
- `title`
- `version`
- `status`
- `language`
- `jurisdiction`
- `system`
- `document_type`
- `owner_role`
- `created_at`
- `last_updated_at`

## 3. Campos condicionales

Según la naturaleza del documento podrán añadirse:

- `effective_date`
- `supersedes`
- `superseded_by`
- `related_pr`
- `related_commit`
- `baseline_sha`
- `source_sha256`
- `evidence_id`
- `fact_id`
- `document_id`
- `verification_id`
- `classification`
- `retention`

Los campos no aplicables no deben inventarse. Deben omitirse o utilizar el valor explícito definido por el modelo correspondiente.

## 4. Valores controlados

### status

`Proposed`, `Active`, `Superseded`, `Deprecated`, `Archived`.

### language

El valor normativo por defecto es `es-CL`. Puede utilizarse `en` o `en-US` cuando un artefacto técnico, fuente externa o requisito operativo lo justifique.

### document_type

Los tipos mínimos son: `constitution`, `policy`, `standard`, `protocol`, `register`, `record`, `audit`, `model`, `case-document`, `evidence-record`, `fact-record`, `legal-analysis`.

## 5. Fechas y horas

Las fechas estructurales usan ISO 8601 (`YYYY-MM-DD`). Los timestamps que representen eventos concretos deben usar ISO 8601 con zona horaria explícita, preferentemente UTC (`YYYY-MM-DDTHH:MM:SSZ`).

No debe utilizarse una fecha de creación del archivo como sustituto del tiempo del hecho documentado.

## 6. Identidad y versionado

El `id` es estable y no debe cambiar cuando el documento evoluciona. `version` sigue SemVer cuando el tipo de documento lo permita.

Un cambio sustantivo debe aumentar la versión y quedar relacionado con el evento de cambio correspondiente.

## 7. Migración histórica

La ausencia de metadatos en un documento histórico no autoriza a inventar datos. La normalización histórica debe preservar el contenido y registrar cualquier valor derivado como tal.

Los documentos históricos no se reescriben simplemente para que parezcan haber cumplido desde el principio el estándar actual.

## 8. Idioma documental

El español es el idioma normativo principal. La nomenclatura técnica puede conservar nombres internacionales cuando ello facilite interoperabilidad o exactitud técnica.

Los títulos y cuerpo de nuevos documentos normativos deben redactarse en español salvo excepción documentada.

## 9. Validación

Antes de aceptar un documento controlado deben comprobarse como mínimo: YAML válido, campos obligatorios presentes, valores controlados válidos, identificador estable, versión coherente y ausencia de afirmaciones de estado no verificadas.
