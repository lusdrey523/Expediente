---
id: EMM-AUDIT-001
title: Auditoría de Integridad General y Cadena de Evidencias/Tiempos
version: 1.0.0
status: Active
jurisdiction: Chile
system: Expediente Maestro Migratorio (EMM)
created: 2026-08-17
last_updated: 2026-08-17
---

# Auditoría de Integridad General y Cadena de Evidencias/Tiempos

## 1. Propósito

Evaluar la integridad de la capa de trazabilidad actualmente incorporada en `lusdrey523/Expediente` y determinar si su diseño conserva una cadena auditable de cambios, verificaciones y estados, además de identificar los controles que deben existir antes de incorporar material sustantivo del expediente.

La auditoría es deliberadamente incremental: no sustituye la futura auditoría de cada evidencia ni certifica hechos jurídicos.

## 2. Alcance

Se revisó:

- estado actual del repositorio `main`;
- historial de commits desde el baseline inicial hasta PR #5;
- PR #1 a PR #5 y sus relaciones de base/head/merge;
- `PR_CONTROL_PROTOCOL.md`;
- `TRACEABILITY_REGISTER.md`;
- `VERIFICATION_REGISTER.md`;
- registros EMM-VER-002, EMM-VER-003 y EMM-VER-004;
- preservación de hashes SHA de commits y merges;
- continuidad entre estados pre-merge y post-merge;
- preparación de la arquitectura para cadena de custodia documental y cadena temporal.

Fuera de alcance: autenticidad material de documentos externos, verdad de hechos legales, elegibilidad migratoria, conclusiones jurídicas y exactitud de cualquier dato contenido en evidencias todavía no incorporadas.

## 3. Baseline auditado

| Elemento | Estado observado |
|---|---|
| Repositorio | `lusdrey523/Expediente` |
| Rama principal | `main` |
| Último estado auditado | PR #5 mergeado |
| Merge SHA PR #5 | `fdfd1e0a7d99f9566539be2ece3833640ddfb98d` |
| Baseline histórico inicial | `98691b7ca4578d9a2b4453a1953bdc9422db3abe` |
| Bootstrap merge | `b172d374785e062cf53cdb402650a5f211ec9954` |
| Governance layer merge | `3f6b5222b82ac88241096a7d08cd9fbc96361199` |
| Verification PR #3 merge | `c84ae649fd6afca59f25533ed073867cffe1a9f5` |
| Governance integrity PR #4 merge | `4b416ee6e00a1f08ecd08fda9fa47a05e01fbf5a` |
| Post-merge verification PR #5 merge | `fdfd1e0a7d99f9566539be2ece3833640ddfb98d` |

## 4. Resultado de integridad general

**PASS — para la capa de trazabilidad y control documental auditada.**

La secuencia PR #1 → PR #5 mantiene una cadena verificable de estados. Los PR registrados contienen referencias explícitas a ramas, SHA de head, SHA de base y SHA de merge. El repositorio conserva la continuidad histórica sin necesidad de reescribir los eventos anteriores.

El resultado PASS está limitado estrictamente a la infraestructura de trazabilidad y gobernanza existente.

## 5. Cadena de evidencias: estado actual

**PASS WITH CONDITIONS — capacidad preparada, cadena sustantiva todavía no constituida.**

El modelo actual declara correctamente que GitHub no sustituye la evidencia primaria. Sin embargo, antes de incorporar documentos o fotografías del expediente debe existir una cadena explícita, por elemento, al menos con:

1. identificador estable de evidencia;
2. nombre y tipo de fuente;
3. procedencia y método de adquisición;
4. fecha/hora de adquisición u observación cuando sea conocida;
5. zona horaria o indicación expresa de hora desconocida;
6. hash del archivo recibido cuando técnicamente sea posible;
7. estado de preservación del archivo original;
8. relación entre original, copia de trabajo y derivados;
9. transformación aplicada, si existe;
10. documento o hecho del expediente al que la evidencia se vincula;
11. verificaciones realizadas y resultado;
12. PR/commit mediante el cual el registro fue incorporado o modificado.

Ningún documento sustantivo debe considerarse plenamente trazado sólo por estar versionado en Git.

## 6. Cadena de tiempos: hallazgos

La infraestructura actual conserva timestamps de Git y fechas de los eventos de PR, lo que es suficiente para auditar la secuencia de cambios del repositorio. No es suficiente por sí solo para reconstruir la cronología jurídica o fáctica del expediente.

Se establece la siguiente separación obligatoria para la futura reconstrucción:

- **Tiempo del hecho:** cuándo ocurrió el hecho que la evidencia pretende demostrar.
- **Tiempo de emisión:** cuándo fue creado/emitido el documento por su fuente.
- **Tiempo de adquisición:** cuándo el expediente recibió o capturó el archivo.
- **Tiempo de observación:** cuándo una persona/proceso inspeccionó el elemento.
- **Tiempo de incorporación:** cuándo el elemento entró al repositorio controlado.
- **Tiempo de modificación:** cuándo se produjo una modificación documental controlada.
- **Tiempo de verificación:** cuándo se realizó la comprobación.

Estos tiempos no deben colapsarse en un único campo `date`.

## 7. Integridad temporal del repositorio

Los commits y PR observados muestran una progresión temporal coherente. Para fines probatorios internos se conservarán los timestamps exactos disponibles en GitHub, preferentemente en ISO 8601 UTC, sin reemplazarlos por fechas resumidas.

Cuando una fuente externa entregue una hora local, debe conservarse:

`fecha/hora original + zona horaria original + representación normalizada UTC`.

Si la fuente no permite determinar la hora, debe registrarse explícitamente como desconocida; no debe inferirse artificialmente.

## 8. Hallazgos de control

### H-001 — Control temporal sustantivo aún no formalizado

**Severidad: MEDIA / PREVENTIVA**

La capa actual controla la cronología Git, pero todavía no existe un registro específico que diferencie tiempo del hecho, emisión, adquisición, observación, incorporación y verificación.

**Acción:** crear ese control antes de la incorporación masiva de evidencia.

### H-002 — Cadena de custodia documental sustantiva aún no poblada

**Severidad: MEDIA / PREVENTIVA**

El repositorio está preparado para recibir identificadores y hashes, pero todavía no existe una población sustantiva de evidencias en el estado auditado.

**Acción:** incorporar evidencia de forma incremental, una unidad controlada por vez o mediante lotes formalmente identificados.

### H-003 — El estado PENDING de EMM-VER-004 requiere cierre explícito

**Severidad: BAJA / CONTROL DE CONTINUIDAD**

PR #5 fue mergeado correctamente, pero `EMM-VER-004` fue diseñado como registro pendiente que debe recibir un resultado posterior. El merge de PR #5 no debe confundirse con la aceptación final de su verificación.

**Acción:** este hallazgo se cierra mediante un evento posterior que verifique el estado `main` y cambie EMM-VER-004 a PASS si todos sus criterios están satisfechos.

## 9. Cadena controlada actualmente demostrable

`Baseline inicial → PR #1 → merge #1 → PR #2 → merge #2 → PR #3 → merge #3 → PR #4 → merge #4 → PR #5 → merge #5 → verificación post-merge de PR #5`

La cadena anterior es una cadena de control de cambios. La cadena de evidencia jurídica deberá acoplarse posteriormente sin alterar esta historia.

## 10. Criterio de continuidad

No se permite:

- sobrescribir silenciosamente una verificación histórica;
- sustituir un hash anterior por uno nuevo sin registrar el motivo;
- convertir una fecha desconocida en una fecha inferida sin marcarla como inferencia;
- confundir fecha de archivo con fecha del hecho;
- afirmar autenticidad material únicamente porque un archivo posee un hash;
- presentar un commit de Git como prueba de la ocurrencia del hecho jurídico subyacente.

Las correcciones, verificaciones posteriores y conclusiones supersedentes deben aparecer como nuevos eventos controlados.

## 11. Conclusión

La infraestructura de GitHub ha alcanzado un nivel suficiente para iniciar la reconstrucción documental incremental, pero la cadena de evidencia y la cadena temporal deben formalizarse antes de declarar íntegra una evidencia individual o un expediente sustantivo completo.

**Resultado global de esta auditoría:**

- Integridad de trazabilidad Git: **PASS**.
- Integridad de gobernanza documental: **PASS** dentro del alcance auditado.
- Preparación para cadena de evidencia: **PASS WITH CONDITIONS**.
- Cadena temporal jurídica/fáctica: **PASS WITH CONDITIONS — control preventivo pendiente de formalización**.
- Certificación de hechos o autenticidad externa: **FUERA DE ALCANCE**.
