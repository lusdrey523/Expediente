---
id: EMM-GOV-VERIFICATION-001
title: Registro de Verificaciones del EMM
version: 0.7.0
status: Active
language: es-CL
jurisdiction: Chile
system: Expediente Maestro Migratorio (EMM)
document_type: register
owner_role: Verifier
created_at: 2026-08-17
last_updated_at: 2026-08-18
---

# Registro de Verificaciones del EMM

## 1. Propósito

Proporcionar una ubicación controlada para registrar eventos de verificación que conecten fuentes, cambios documentales, historial Git y estados aceptados.

## 2. Modelo de registro

Cada evento de verificación debe identificar, cuando corresponda:

| Campo | Requisito |
|---|---|
| Verification ID | Identificador único y estable |
| Fecha | Fecha de verificación |
| Alcance | Archivos, evidencia o estado exacto comprobado |
| Fuente | Documento fuente, paquete, registro oficial o estado previo |
| Hash fuente | SHA-256 u otro identificador de integridad cuando exista |
| Objetivo | Commit, PR, versión documental o estado del repositorio |
| Método | Manual, automatizado, comparativo o mixto |
| Resultado | PASS, PASS WITH CONDITIONS, FAIL o PENDING |
| Hallazgos | Observaciones materiales |
| Acción | Corrección o decisión requerida |
| Verificador | Persona/proceso que ejecuta la comprobación |

## 3. Eventos registrados

| Verification ID | Alcance | Objetivo | Resultado | Notas |
|---|---|---|---|---|
| EMM-VER-001 | Bootstrap de trazabilidad GitHub del EMM | PR #1 / `b172d374785e062cf53cdb402650a5f211ec9954` | PASS WITH CONDITIONS | Establece infraestructura de trazabilidad; no certifica hechos jurídicos ni autenticidad material de fuentes. |
| EMM-VER-002 | Verificación post-merge de la capa mínima de gobernanza | PR #2 / `3f6b5222b82ac88241096a7d08cd9fbc96361199` | PASS WITH CONDITIONS | Confirmó los cuatro controles iniciales y su incorporación en `main`. |
| EMM-VER-003 | Integridad de la capa de gobierno/control | PR #4 / `4b416ee6e00a1f08ecd08fda9fa47a05e01fbf5a` | PASS | Confirmó coherencia interna, preservación histórica y límites probatorios. |
| EMM-VER-004 | Verificación post-merge de PR #4 | PR #4 / `4b416ee6e00a1f08ecd08fda9fa47a05e01fbf5a`; verificado mediante PR #5 | PASS | Cerrado mediante el estado controlado de PR #5. |
| EMM-VER-005 | Verificación post-merge de PR #5 y estado resultante de `main` | PR #5 / `fdfd1e0a7d99f9566539be2ece3833640ddfb98d` | PASS | Confirma integración de PR #5 y continuidad de la cadena de control. |
| EMM-VER-006 | Verificación post-merge de PR #11 / fundación de intake documental | PR #11 / `0a94b0c19826ee3028c2e24ab46c304d488ca1c9` | PASS | Verificación de integración de infraestructura y coherencia con Stage 4/F-01. No certifica la disponibilidad o autenticidad del paquete fuente sustantivo. |
| EMM-VER-007 | Verificación pre-merge de PR #12 / Constitución, metadatos, autoridad y sincronización | PR #12 / head `cb90898ce8ec0413777f512b0c6ee92ae59fff79` | PASS | Confirma coherencia interna de la propuesta y presencia de los cuatro instrumentos de continuidad. La verificación se limitó a la rama antes del merge. |
| EMM-VER-008 | Verificación post-merge de PR #12 / integración constitucional | PR #12 → `67d540bfcc00db3413432da334545bdf4204fb13` | PASS | Confirma que PR #12 quedó efectivamente integrado en `main` el `2026-08-18T18:08:57Z`. La activación normativa se documenta como evento posterior en PR #13. |
| EMM-VER-009 | Verificación pre-merge de PR #13 / activación y control documental | PR #13 / rama `governance/EMM-OPS-001` | PASS | Confirma coherencia de la propuesta de activación, protocolo de control documental, registro de activación y sincronización de los cuatro instrumentos de continuidad. No representa todavía integración en `main`. |

## 4. Regla de interpretación

Un resultado de verificación aplica únicamente al alcance expresamente registrado. Un PASS sobre estructura, control o consistencia de hashes no constituye una conclusión jurídica.

Una limitación de alcance no es por sí misma un fallo. Cuando una verificación está completa dentro de su alcance declarado, puede recibir PASS conservando explícitamente sus límites.

## 5. Regla de sincronización con PR

Cada PR que incorpore una modificación relevante debe actualizar dentro del mismo PR los cuatro instrumentos de continuidad:

- `README.md`
- `CHANGELOG.md`
- `repository-governance/TRACEABILITY_REGISTER.md`
- `repository-governance/VERIFICATION_REGISTER.md`

Antes del merge, el registro puede contener una verificación de la rama propuesta. El resultado de esa verificación no debe confundirse con la aceptación del merge. La integración efectiva se acredita mediante el evento Git correspondiente.

Cuando una propuesta normativa haya sido integrada pero requiera que su estado documental pase de `Proposed` a `Active`, la corrección puede incorporarse en el siguiente PR sustantivo junto con su registro de activación; no se requiere un PR de mera limpieza.

## 6. Continuidad

Los registros de verificación son orientados a anexado. Las entradas históricas no deben reescribirse silenciosamente para reflejar conclusiones posteriores. Correcciones o evaluaciones supervinientes deben registrarse como nuevos eventos vinculados al registro anterior.

El cambio de estado de una verificación debe conservar su identificador, objetivo y contexto histórico originales.
