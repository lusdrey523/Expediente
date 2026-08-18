# CHANGELOG — Expediente Maestro Migratorio

Registro histórico de evolución de la infraestructura documental y de trazabilidad.

## Principio

Cada entrada describe cambios de infraestructura o control incorporados mediante eventos Git/PR. El CHANGELOG no sustituye los registros de verificación ni la evidencia primaria.

## PR #1 — EMM-BOOTSTRAP-001

**Hito:** establecimiento de la primera capa controlada de trazabilidad.

- README mínimo y principio operativo.
- Registro de trazabilidad inicial.
- Vinculación con el baseline inicial y el paquete `Legalbreto-main.zip` mediante SHA-256.
- Preservación del principio de evolución incremental.

## PR #2 — EMM-TRACE-LAYER-002

**Hito:** establecimiento de la capa mínima de gobernanza documental.

- Protocolo de control de Pull Requests.
- Registro de verificaciones.
- Modelo de estados documentales.
- Actualización del registro de trazabilidad.

## PR #3 — EMM-TRACE-VERIFY-002

**Hito:** cierre controlado de la verificación post-merge de PR #2.

- Registro EMM-VER-002.
- Actualización de registros de gobernanza y trazabilidad.
- Conservación explícita de la condición histórica `PASS WITH CONDITIONS`.

## PR #4 — EMM-VER-003

**Hito:** verificación de integridad de la capa de gobierno/control.

- Verificación EMM-VER-003.
- Distinción entre control de infraestructura y certificación de hechos/evidencia externa.
- Preservación de verificaciones históricas.

## PR #5 — EMM-VER-004

**Hito:** cierre de la verificación post-merge de PR #4.

- Registro EMM-VER-004.
- Actualización de registros de trazabilidad y verificación.
- Cierre mediante el estado integrado de PR #5.

## PR #6 — EMM-AUDIT-001

**Hito:** auditoría general de integridad y cadena de evidencias/tiempos.

- Auditoría de la capa Git/PR.
- Definición de controles necesarios para procedencia, hashes, preservación y relaciones de evidencia.
- Definición de clases temporales diferenciadas.
- Confirmación de `PASS` para trazabilidad Git y `PASS WITH CONDITIONS` para cadena sustantiva de evidencia/tiempo.

## PR #7 — EMM-REPO-STATUS-001

**Hito:** sincronización de la representación de infraestructura y creación del CHANGELOG permanente.

- README actualizado después de PR #6.
- Principios explícitos de trazabilidad, integridad histórica, separación de capas, preservación temporal, evolución incremental e interoperabilidad futura.
- CHANGELOG permanente.

## PR #8 — EMM-REPO-ARCH-002

**Hito:** separación arquitectónica explícita entre gobierno del repositorio y documentación del caso.

- `00-governance/` → `repository-governance/`.
- `docs/00-governance/` → `docs/case-governance/`.
- Incorporación de `repository-governance/REPOSITORY_ARCHITECTURE.md`.
- Preparación de dominios futuros dentro de `docs/` sin afirmar que su contenido sustantivo ya exista.

## PR #9 — EMM-REPO-STATUS-002

**Hito:** sincronización menor del estado arquitectónico después de PR #8.

- README actualizado para representar PR #8 como último hito integrado.
- Cadena PR representada hasta PR #8.
- Aclaración de que los registros de nombres similares en `repository-governance/` y `docs/case-governance/` pertenecen a capas distintas y no son intercambiables.
- Sin incorporación de hechos, evidencia sustantiva o análisis jurídico.

## PR #10 — EMM-REPO-RECON-003

**Hito:** reconciliación de estado, roadmap y limpieza del artefacto bootstrap.

- Retiro de `1.md`, archivo auxiliar utilizado durante el bootstrap inicial.
- Preservación de su existencia histórica mediante Git y los registros PR #1/PR #10.
- Incorporación de `repository-governance/ROADMAP.md` para separar explícitamente etapas completadas, pendientes y futuras.
- Reconciliación del registro de trazabilidad hasta PR #10 sin reescribir los eventos anteriores.
- Confirmación de que la siguiente etapa es la reconstrucción documental incremental del expediente, antes de la capa de aplicación.

## PR #11 — EMM-CASE-FOUNDATION-001

**Hito:** entrada controlada a Stage 4 mediante la fundación de intake documental.

- Creación de `docs/case-foundation/` como punto de entrada para la reconstrucción sustantiva.
- Definición del control de intake, preservación y condiciones de bloqueo para F-01.
- Actualización del roadmap para distinguir la fundación de intake ya definida de la incorporación sustantiva aún bloqueada por la disponibilidad verificable del paquete fuente.
- No se incorpora evidencia sustantiva ni se inventan o reconstruyen archivos fuente a partir de memoria, prompts o nombres de archivo.

## PR #12 — EMM-CONST-001

**Hito:** integración de la Constitución Documental y del núcleo de gobernanza normativa.

- Integración de la Constitución Documental y de Gobernanza.
- Integración del estándar común de metadatos.
- Integración del modelo de autoridad y separación de funciones.
- Actualización de los cuatro instrumentos de continuidad dentro del mismo PR.
- Merge efectivo en `main` mediante commit `67d540bfcc00db3413432da334545bdf4204fb13` el `2026-08-18T18:08:57Z`.
- La verificación pre-merge histórica permanece registrada como `PASS`; la activación normativa se registra como evento posterior en PR #13.

## PR #13 — EMM-GOV-OPS-001

**Hito:** activación del gobierno documental y del control operativo.

- Activación efectiva de la Constitución, el estándar de metadatos y el modelo de autoridad.
- Incorporación de `DOCUMENT_CONTROL_PROTOCOL.md` como protocolo operativo.
- Incorporación de `CONSTITUTION_ACTIVATION_RECORD.md` como registro de activación posterior a PR #12.
- Definición de `Active` como estado vinculante de un instrumento normativo vigente; `Approved` no es un estado documental independiente.
- Integración efectiva en `main` mediante commit `2233cb6f2c80ba474a171a467feab278906480a5` el `2026-08-18T19:18:15Z`.

## PR #14 — EMM-F01-SOURCE-INTAKE-001

**Estado:** propuesta en ejecución; pendiente de merge.

**Hito previsto:** preparar el recibo controlado y la representación exacta del gate de F-01 antes de incorporar evidencia sustantiva.

- Sincronizar el estado real de `main` después de PR #13.
- Incorporar un registro de recepción de fuente que distinga identidad declarada, verificación independiente y disponibilidad efectiva.
- Mantener bloqueada la incorporación sustantiva mientras el paquete fuente exacto no esté disponible como input verificable en el proceso de intake.
- No reconstruir ni alterar archivos fuente a partir de memoria, prompts, nombres de archivo o registros históricos incompletos.
- Actualizar los cuatro instrumentos de continuidad dentro del mismo PR.
- Mantener separadas la infraestructura de gobierno y la documentación sustantiva del caso.

## Regla de continuidad

Cada nueva evolución de infraestructura debe preservar la cadena histórica existente y documentar de forma explícita qué cambia, por qué cambia y mediante qué evento controlado se incorpora.

Los PR abiertos pueden registrarse expresamente como `Proposed` o `Pending`; nunca deben representarse como integrados antes de su aceptación y merge efectivo.

Las etapas planificadas no deben presentarse como completadas hasta que exista un cambio controlado y, cuando corresponda, una verificación de aceptación.
