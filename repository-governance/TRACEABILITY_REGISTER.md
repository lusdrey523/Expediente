---
id: EMM-TRACE-REGISTER-001
title: Registro de Trazabilidad del EMM
version: 1.1.0
status: Active
language: es-CL
jurisdiction: Chile
system: Expediente Maestro Migratorio (EMM)
document_type: register
owner_role: Repository Administrator
created_at: 2026-08-17
last_updated_at: 2026-08-20
---

# Registro de Trazabilidad del EMM

## 1. Propósito

Este registro establece el vínculo auditable entre el Expediente Maestro Migratorio y el repositorio `lusdrey523/Expediente`.

Git y los Pull Requests constituyen la capa de trazabilidad para cambios documentales controlados. No sustituyen evidencia primaria, registros oficiales ni revisión jurídica.

## 2. Registro bootstrap

| Campo | Valor |
|---|---|
| Identificador bootstrap | EMM-BOOTSTRAP-001 |
| Repositorio | `lusdrey523/Expediente` |
| Rama principal | `main` |
| Rama bootstrap | `traceability/EMM-BOOTSTRAP-001` |
| Commit inicial observado | `98691b7ca4578d9a2b4453a1953bdc9422db3abe` |
| Timestamp inicial | `2026-08-17T18:33:10Z` |
| Contenido inicial | `1.md`, contenido de prueba; conservado como estado histórico del repositorio |
| PR bootstrap | PR #1 |
| SHA de merge bootstrap | `b172d374785e062cf53cdb402650a5f211ec9954` |

El retiro posterior de `1.md` no elimina este registro histórico. Su existencia anterior permanece recuperable mediante Git y PR #1/PR #10.

## 3. Baseline del expediente fuente

El bootstrap está vinculado al paquete fuente EMM previamente auditado:

- Paquete fuente declarado: `Legalbreto-main.zip`
- SHA-256 declarado: `26f599f89d7e546deb53ad316123f16cf6683015547a7f5bc5eb2c99f628435f`
- Inventario reportado: 48 archivos
- Evaluación asociada: `EMM_SYSTEM_ASSESSMENT_001`

Esta entrada registra la relación histórica con el paquete fuente. No afirma que el ZIP esté almacenado en este repositorio ni que haya sido re-recibido y re-hasheado durante PR #14 o posteriores.

## 4. Historial controlado

| Etapa | Identificador | Registro Git | Estado |
|---|---|---|---|
| Bootstrap | `EMM-BOOTSTRAP-001` | PR #1 → `b172d374785e062cf53cdb402650a5f211ec9954` | Incorporado |
| Capa mínima de gobernanza | `EMM-TRACE-LAYER-002` | PR #2 → `3f6b5222b82ac88241096a7d08cd9fbc96361199` | Incorporado |
| Verificación post-merge | `EMM-VER-002` | PR #3 → `c84ae649fd6afca59f25533ed073867cffe1a9f5` | PASS WITH CONDITIONS |
| Integridad de control | `EMM-VER-003` | PR #4 → `4b416ee6e00a1f08ecd08fda9fa47a05e01fbf5a` | PASS |
| Verificación post-merge | `EMM-VER-004` | PR #5 → `fdfd1e0a7d99f9566539be2ece3833640ddfb98d` | PASS |
| Auditoría integridad/evidencia-tiempo | `EMM-AUDIT-001` | PR #6 → `e2f4442de7d77f9d217b1668c0f58a5765cfa8e3` | Incorporado |
| Verificación post-merge | `EMM-VER-005` | PR #6 / estado resultante | PASS |
| Estado y CHANGELOG | `EMM-REPO-STATUS-001` | PR #7 → `b8269471d5c6258f6fe9aff0b7e57102e67a41ba` | Incorporado |
| Separación arquitectónica | `EMM-REPO-ARCH-002` | PR #8 → `87d48732e12fb04d0e1bd6e615a67f414c0231c7` | Incorporado |
| Sincronización de infraestructura | `EMM-REPO-STATUS-002` | PR #9 → `b06badf304aaf8e1cf12af18538976fb57f84b0e` | Incorporado |
| Reconciliación de infraestructura | `EMM-REPO-RECON-003` | PR #10 → `3cd9ba12c03d4c0a5b54d8ec6ddaf1159ae314b6` | Incorporado |
| Fundamento de intake documental | `EMM-CASE-FOUNDATION-001` | PR #11 → `0a94b0c19826ee3028c2e24ab46c304d488ca1c9` | Incorporado |
| Constitución y gobierno documental | `EMM-CONST-001` | PR #12 → `67d540bfcc00db3413432da334545bdf4204fb13` | Incorporado |
| Activación de gobierno documental | `EMM-GOV-OPS-001` | PR #13 → `2233cb6f2c80ba474a171a467feab278906480a5` | Incorporado |
| Preparación de intake F-01 | `EMM-F01-SOURCE-INTAKE-001` | PR #14 → `b60e055d91846f746d4eb063f1248e3101bcc940` | Incorporado |
| Sincronización post-merge PR #14 | `EMM-POSTMERGE-014` | PR #15 (este cambio) | Propuesto |

PR #12 quedó integrado en `main` el `2026-08-18T18:08:57Z`.

PR #13 quedó integrado en `main` el `2026-08-18T19:18:15Z`, produciendo el SHA `2233cb6f2c80ba474a171a467feab278906480a5`.

PR #14 quedó integrado en `main` el `2026-08-18T19:52:58Z`, produciendo el SHA `b60e055d91846f746d4eb063f1248e3101bcc940`.

## 5. Modelo de trazabilidad

Cada cambio controlado debe poder representarse, cuando corresponda, mediante:

`Fuente → Interpretación documental → Documento controlado → Commit Git → Pull Request → Verificación → Estado aceptado`

Un commit demuestra que un estado del repositorio existió en un punto de la historia. Un Pull Request añade la propuesta de cambio, su justificación, revisión y resultado de aceptación/rechazo.

## 6. Regla de sincronización

Cada PR que incorpore una modificación relevante debe actualizar dentro del mismo PR los cuatro instrumentos de continuidad:

1. `README.md`
2. `CHANGELOG.md`
3. `repository-governance/TRACEABILITY_REGISTER.md`
4. `repository-governance/VERIFICATION_REGISTER.md`

En un PR abierto, estos instrumentos pueden describir el estado propuesto. Después del merge, el siguiente evento controlado debe reflejar el SHA real de `main` sin reescribir la historia anterior.

## 7. Alcance actual

La capa `repository-governance/` contiene los controles de PR, verificación, estado documental, trazabilidad, auditoría de integridad, arquitectura, roadmap, intake y gobernanza constitucional activa. La capa sustantiva permanece separada bajo `docs/`.

La futura aplicación multicaso puede acoplarse a esta infraestructura, pero la interfaz no adquiere autoridad sobre los registros por el hecho de presentarlos.

## 8. Límite

Este registro no certifica hechos jurídicos, autenticidad material de evidencia, elegibilidad migratoria ni conclusiones legales. Es una representación controlada de la historia documental y técnica del proyecto.

## 9. Continuidad

Los eventos históricos se preservan. Correcciones y evaluaciones posteriores deben representarse como nuevos cambios controlados, no como reescritura silenciosa de la historia anterior.
