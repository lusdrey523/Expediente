---
id: EMM-REPO-ROADMAP-001
title: Hoja de Ruta de Evolución del Repositorio y Documentación EMM
version: 1.4.0
status: Active
language: es-CL
jurisdiction: Chile
system: Expediente Maestro Migratorio (EMM)
document_type: roadmap
owner_role: Project Owner
created_at: 2026-08-18
last_updated_at: 2026-08-18
---

# Hoja de Ruta de Evolución del Repositorio y Documentación EMM

## 1. Propósito

Definir la secuencia controlada mediante la cual el EMM evoluciona desde un núcleo de trazabilidad Git/GitHub hacia un sistema documental completo y posteriormente hacia una interfaz para abogado y una arquitectura multicaso, sin mezclar controles de infraestructura con evidencia sustantiva ni reescribir eventos históricos.

Esta hoja de ruta es un documento de planificación y control. Una etapa planificada no constituye evidencia de que ya haya sido ejecutada.

## 2. Secuencia fundacional

### Stage 0 — Baseline de fuente y bootstrap
**Status: COMPLETED**

- Preservar el paquete fuente auditado y su vínculo SHA-256.
- Establecer el repositorio y la trazabilidad inicial controlada.
- Conservar el estado inicial como contexto histórico.

### Stage 1 — Trazabilidad y gobernanza mínima
**Status: COMPLETED**

- Establecer el protocolo de Pull Requests.
- Establecer los modelos de verificación y estado documental.
- Registrar cambios controlados y verificaciones post-merge.

### Stage 2 — Auditoría de integridad y control temporal
**Status: COMPLETED WITH CONDITIONS**

- Auditar integridad Git/PR.
- Definir requisitos de cadena de evidencia.
- Separar tiempo del hecho, emisión, adquisición, observación, incorporación, modificación y verificación.
- Registrar que la evidencia sustantiva y la cronología fáctica todavía deben reconstruirse.

### Stage 3 — Sincronización de infraestructura y separación arquitectónica
**Status: COMPLETED**

- Mantener `repository-governance/` separado explícitamente de `docs/`.
- Mantener `README.md` y `CHANGELOG.md` como representaciones de infraestructura.
- Reconciliar el estado después de cada cambio controlado.
- Retirar artefactos exclusivos del bootstrap una vez preservada su existencia histórica mediante Git.

### Governance activation layer — PR #13
**Status: COMPLETED / ACTIVE**

- Activar la Constitución integrada por PR #12.
- Activar el estándar de metadatos y el modelo de autoridad.
- Establecer el Protocolo de Control Documental.
- Registrar la activación como evento posterior a PR #12 sin reescribirlo.
- Mantener sincronizados los cuatro instrumentos de continuidad dentro del mismo cambio.

PR #13 quedó integrado en `main` mediante `2233cb6f2c80ba474a171a467feab278906480a5` el `2026-08-18T19:18:15Z`.

### Stage 4 — Reconstrucción documental del paquete auditado
**Status: IN EXECUTION**

Ejecutar incrementalmente desde el baseline auditado, no mediante una importación masiva no controlada.

#### F-01 — Evidence register foundation
**Status: INTAKE CONTROL ESTABLISHED — SOURCE RECEIPT REQUIRED**

- Controlar el límite de entrada documental.
- Identificar exactamente el paquete fuente presentado.
- Calcular y registrar independientemente su SHA-256.
- Preservar el paquete exacto como input de referencia.
- Inventariar sus archivos sin modificar el contenido fuente.
- Crear el primer registro controlado de evidencia solamente después de verificar el input.

PR #14 establece la capa de recibo y el gate operativo. No afirma que el paquete fuente haya sido recibido, re-hasheado o verificado dentro de esta PR.

**Blocking prerequisite:** el paquete fuente auditado exacto debe estar disponible como input reproducible y verificable. El repositorio no debe inferir ni reconstruir artefactos fuente a partir de memoria, prompts o nombres de archivo.

#### F-02 — Reconciliación histórica de evidencia/manifiesto
**Status: NOT STARTED**

Reconciliar registros EML/manifiestos/recibos históricos con el registro controlado sin reescribir silenciosamente los registros históricos.

#### F-03 — Normalización de metadatos y procedencia
**Status: NOT STARTED**

Normalizar metadatos mínimos para identificar fuente, adquisición, preservación, hash y timestamps relevantes, conservando explícitamente los valores desconocidos.

#### F-04 — Identificadores estables y relaciones
**Status: NOT STARTED**

Establecer identificadores de evidencia/documentos y sus relaciones con el paquete fuente, hechos y documentos controlados.

#### F-05 — Índice y capa de control
**Status: NOT STARTED**

Construir el índice controlado que conecte evidencia, documentos, hechos, verificaciones y eventos del repositorio.

#### F-06 — Reconstrucción temporal
**Status: NOT STARTED**

Construir la línea temporal factual/documental con campos separados para:

- tiempo del hecho;
- tiempo de emisión;
- tiempo de adquisición;
- tiempo de observación;
- tiempo de incorporación;
- tiempo de modificación;
- tiempo de verificación.

#### F-07 — Modelo FACT → EVIDENCE → DOCUMENT
**Status: NOT STARTED**

Establecer vínculos explícitos entre afirmaciones fácticas, evidencia de soporte y artefactos documentales. Un vínculo no constituye por sí mismo una conclusión jurídica.

#### F-08 — Preparación de preguntas jurídicas y entrega al abogado
**Status: NOT STARTED**

Registrar preguntas jurídicas, vacíos documentales y asuntos que requieren revisión profesional sin convertirlos prematuramente en argumentos jurídicos definitivos.

#### Reconstruction gate

Después de F-01 a F-08 debe ejecutarse una reauditoría controlada y producirse el estado/paquete persistente requerido por el procedimiento operativo. La finalización de los ocho pasos no constituye automáticamente certificación de cada elemento de evidencia.

### Stage 5 — Preparación para revisión jurídica
**Status: FUTURE**

- Producir resúmenes para el abogado e índices de asuntos a partir de registros verificados.
- Mantener vínculos explícitos entre cada conclusión/pregunta y sus hechos/evidencia/documentos de soporte.
- Preparar salidas PDF o de presentación únicamente después de satisfacer los gates documentales.

### Stage 6 — Capa de aplicación para abogado
**Status: FUTURE — ARCHITECTURE ONLY**

La interfaz futura podrá exponer información controlada mediante una aplicación web adecuada para interacción directa del abogado.

Requisitos ya definidos a nivel arquitectónico:

- autenticación y autorización seguras;
- acceso por roles a secciones del caso;
- separación entre datos del caso y gobierno del repositorio;
- interacciones auditables y referencias documentales;
- ningún secreto o credencial privada en GitHub Pages;
- interfaz generada desde datos controlados, sin convertirse en fuente autoritativa por sí misma.

GitHub Pages puede servir como capa de presentación cuando corresponda, pero no es por sí mismo la frontera de autenticación/seguridad para información sensible.

### Stage 7 — Arquitectura multicaso
**Status: FUTURE — ARCHITECTURE ONLY**

Evolucionar el modelo de un caso a múltiples casos, con namespace, evidencia, hechos, documentos, verificaciones, análisis jurídico y políticas de acceso aislados por caso, compartiendo los principios de control de infraestructura.

La arquitectura debe admitir un número arbitrario de casos sin rediseñar el modelo de trazabilidad subyacente.

### Stage 8 — Interoperabilidad futura
**Status: FUTURE**

Diseñar convenciones para permitir interoperabilidad posterior con estándares institucionales más amplios sin crear dependencia, subordinación o acoplamiento actual.

## 3. Gate actual

**Current controlled gate:** Stage 4 / F-01 — Evidence register foundation.

La infraestructura de intake y gobierno está establecida. El recibo y la verificación del paquete fuente exacto siguen siendo el bloqueo material antes de la incorporación sustantiva.

PR #14 no declara completado F-01; establece el control necesario para recibir y verificar el input antes de incorporar evidencia.

## 4. Relación con la secuencia de auditoría histórica

El programa de auditoría previamente definido conserva fases para baseline/inventario, estructura/metadatos, cronología, análisis evidencia-afirmación, evidencia primaria, controles EML, consistencia documental, revisión red-team, handoff al abogado y gate final de presentación.

Esta hoja de ruta no descarta esa secuencia. Separa el prerrequisito de infraestructura de la ejecución documental. F-01 a F-08 constituyen el puente controlado inmediato hacia esa secuencia más amplia.

## 5. Regla de continuidad

Cada etapa completada debe estar representada por cambios controlados y, cuando corresponda, verificación. Las etapas planificadas no deben describirse como completadas hasta registrar su estado de aceptación.

Los PR históricos y los registros de verificación conservan su significado histórico. Las correcciones posteriores se representan como nuevos eventos controlados.
