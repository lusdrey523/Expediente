# Expediente

Repositorio de infraestructura documental y trazabilidad del Expediente Maestro Migratorio (EMM).

## Propósito

Este repositorio proporciona una capa controlada para registrar, preservar y verificar la evolución documental del expediente mediante historial Git, Pull Requests, verificaciones y registros de control.

GitHub funciona como infraestructura de trazabilidad y control de cambios. No sustituye la evidencia primaria ni certifica por sí mismo la verdad de hechos jurídicos, la autenticidad material de documentos externos, la elegibilidad migratoria ni conclusiones legales.

## Estado actual de la infraestructura

- **Repositorio:** `lusdrey523/Expediente`
- **Rama principal:** `main`
- **Último hito integrado antes de PR #10:** PR #9 — `EMM-REPO-STATUS-002`
- **PR #10:** reconciliación de infraestructura en curso; incluye la eliminación del artefacto bootstrap `1.md`.
- **Estado de la capa Git y de gobernanza auditada:** PASS dentro del alcance definido por `INTEGRITY_AUDIT_EMM-001.md`.
- **Cadena PR integrada:** PR #1 → PR #9.
- **Cadena de evidencia sustantiva:** preparada a nivel de control, todavía pendiente de reconstrucción documental incremental.
- **Cadena temporal:** control preparada a nivel de infraestructura; la cronología fáctica debe reconstruirse separando tiempo del hecho, emisión, adquisición, observación, incorporación, modificación y verificación.

## Arquitectura

La infraestructura distingue explícitamente dos capas:

- **`repository-governance/`**: gobierno, integridad, trazabilidad, verificaciones, roadmap y controles de la infraestructura del repositorio.
- **`docs/`**: documentación sustantiva del caso, organizada progresivamente en dominios como `case-foundation/`, `case-governance/`, `evidence/`, `facts/`, `documents/`, `verifications/` y `legal-analysis/`.

La separación evita confundir el gobierno del repositorio con el gobierno o contenido del caso. La arquitectura detallada se encuentra en `repository-governance/REPOSITORY_ARCHITECTURE.md`.

## Principios de infraestructura

1. **Trazabilidad:** todo cambio controlado debe poder relacionarse con su PR, commit, estado de integración y verificación correspondiente.
2. **Integridad histórica:** los eventos ya registrados no se reescriben para mejorar retrospectivamente su resultado.
3. **Separación de capas:** infraestructura, evidencia, hechos y análisis jurídico deben conservar límites explícitos.
4. **Evolución incremental:** los nuevos componentes se acoplan progresivamente al núcleo existente sin exigir una reconstrucción de la cadena histórica.
5. **Preservación temporal:** cuando un evento dependa del tiempo, deben conservarse los timestamps disponibles y distinguirse las distintas clases de tiempo relevantes.
6. **Verificación explícita:** una incorporación documental no se considera equivalente a una verificación; ambas deben quedar identificadas por separado.
7. **Interoperabilidad futura:** la infraestructura se diseña con convenciones claras y modulares para permitir su eventual adaptación a estándares externos o institucionales, sin crear dependencia actual respecto de ellos.

## Límites

La infraestructura demuestra principalmente **qué fue incorporado, cuándo fue registrado, mediante qué cambio controlado y qué estado de verificación recibió dentro del repositorio**. No convierte automáticamente esos registros en prueba de la verdad material de los hechos subyacentes.

## Roadmap

El orden de evolución está definido en `repository-governance/ROADMAP.md`. La siguiente etapa es la reconstrucción documental incremental del expediente a partir del baseline auditado.

La futura interfaz para abogado, autenticación segura y arquitectura multicaso se mantienen como etapas posteriores de arquitectura. No son parte del núcleo documental actual ni se confunde GitHub Pages con el límite de seguridad para información sensible.

## Regla arquitectónica

`repository-governance/` controla la infraestructura. `docs/` contiene el caso. El hecho de que ambos vivan dentro del mismo repositorio no elimina esta separación conceptual ni probatoria.

## Continuidad

Las nuevas capas deben incorporarse mediante cambios controlados y quedar reflejadas en el CHANGELOG sin alterar retrospectivamente la cadena histórica. Las etapas planificadas no deben presentarse como completadas hasta contar con su correspondiente estado de aceptación/verificación.
