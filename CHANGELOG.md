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
- Sincronización del README con el estado real inmediatamente anterior a PR #10.
- Reconciliación del registro de trazabilidad hasta PR #10 sin reescribir los eventos anteriores.
- Confirmación de que la siguiente etapa es la reconstrucción documental incremental del expediente, antes de la capa de aplicación.
- La futura interfaz para abogado, autenticación segura y arquitectura multicaso permanecen como arquitectura posterior; no forman parte de esta PR.

## PR #11 — EMM-CASE-FOUNDATION-001

**Hito:** entrada controlada a Stage 4 mediante la fundación de intake documental.

- Creación de `docs/case-foundation/` como punto de entrada para la reconstrucción sustantiva.
- Definición del control de intake, preservación y condiciones de bloqueo para F-01.
- Actualización de `README.md` para reflejar PR #10 como último hito integrado y F-01 como siguiente ejecución controlada.
- Actualización del roadmap para distinguir con precisión entre la fundación de intake ya definida y la incorporación sustantiva aún bloqueada por la disponibilidad verificable del paquete fuente.
- No se incorpora evidencia sustantiva ni se inventan o reconstruyen archivos fuente a partir de memoria, prompts o nombres de archivo.

## Regla de continuidad

Cada nueva evolución de infraestructura debe preservar la cadena histórica existente y documentar de forma explícita qué cambia, por qué cambia y mediante qué evento controlado se incorpora.

Las etapas planificadas no deben presentarse como completadas hasta que exista un cambio controlado y, cuando corresponda, una verificación de aceptación.
