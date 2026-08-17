# CHANGELOG — Expediente Maestro Migratorio

Registro histórico de evolución de la infraestructura documental y de trazabilidad del repositorio.

> Este archivo registra cambios de infraestructura y control. No constituye por sí mismo una certificación de hechos jurídicos ni sustituye los registros de trazabilidad o verificación correspondientes.

## Estado inicial observado

- Repositorio: `lusdrey523/Expediente`
- Rama principal: `main`
- La infraestructura comenzó con un bootstrap mínimo y se amplió mediante Pull Requests controladas.

## PR #1 — EMM-BOOTSTRAP-001

**Hito:** establecimiento de la primera capa de trazabilidad documental.

- Creación del README inicial y principio operativo.
- Creación del registro de trazabilidad.
- Registro del commit baseline observado.
- Vinculación del paquete fuente previamente auditado mediante SHA-256.
- Definición de una arquitectura incremental para futuras capas.

## PR #2 — EMM-TRACE-LAYER-002

**Hito:** establecimiento de controles mínimos de gobernanza documental.

- Protocolo controlado de Pull Requests.
- Registro de verificaciones.
- Modelo de estado del ciclo de vida documental.
- Actualización del registro de trazabilidad.
- Confirmación de que la nueva capa no reemplaza ni reescribe el bootstrap histórico.

## PR #3 — EMM-TRACE-VERIFY-002

**Hito:** cierre de la primera brecha de verificación post-merge.

- Registro formal de la integración de PR #2.
- Incorporación de la verificación correspondiente.
- Extensión de la cadena de trazabilidad y verificación.

## PR #4 — EMM-VER-003

**Hito:** verificación de integridad de la capa de gobernanza y control.

- Verificación PASS de la capa de control dentro de su alcance explícito.
- Preservación de resultados históricos anteriores sin reescritura retroactiva.
- Mantenimiento de la frontera entre trazabilidad del repositorio y afirmaciones jurídicas o probatorias externas.

## PR #5 — EMM-VER-004

**Hito:** cierre del ciclo de verificación post-merge de PR #4.

- Registro de PR #4 como incorporada.
- Registro de la verificación post-merge correspondiente.
- Consolidación de la continuidad de la cadena de control.

## PR #6 — EMM-AUDIT-001

**Hito:** auditoría general de integridad con foco en cadena de evidencias y cadena temporal.

- Auditoría de la capa Git y de gobernanza.
- Confirmación PASS dentro del alcance auditado.
- Formalización de controles para separar tiempo del hecho, emisión, adquisición, observación, incorporación, modificación y verificación.
- Definición de requisitos preventivos para la futura cadena de custodia documental.
- Registro de la verificación post-merge correspondiente a PR #5.

## PR #7 — EMM-REPO-STATUS-001

**Hito:** actualización de la representación institucional de la infraestructura del repositorio.

- Actualización del README para representar el estado real de la infraestructura después de PR #6.
- Incorporación de principios explícitos de arquitectura incremental, separación de capas, integridad histórica, preservación temporal e interoperabilidad futura.
- Creación de este CHANGELOG para conservar una vista cronológica de la evolución de la infraestructura.
- La actualización no modifica los documentos históricos del caso ni altera retrospectivamente verificaciones anteriores.

## PR #8 — EMM-REPO-ARCH-002

**Hito:** separación arquitectónica explícita entre gobierno del repositorio y documentación sustantiva del caso.

- Renombrado conceptual y estructural de la capa raíz `00-governance/` a `repository-governance/`.
- Renombrado conceptual y estructural de `docs/00-governance/` a `docs/case-governance/`.
- Incorporación de `repository-governance/REPOSITORY_ARCHITECTURE.md` como definición formal de la arquitectura.
- Actualización del README para reflejar la estructura vigente y la evolución modular prevista.
- Preservación de los contenidos y SHAs de los documentos trasladados; el cambio es estructural y no reescribe su contenido histórico.
- Definición de dominios futuros de `docs/` sin afirmar que sus contenidos sustantivos ya estén incorporados.
- Mantenimiento de la separación entre infraestructura de control y evidencia/documentación del caso.

## Regla de continuidad

Cada nueva evolución de infraestructura debe preservar la cadena histórica existente y documentar de forma explícita qué cambia, por qué cambia y mediante qué evento controlado se incorpora.
