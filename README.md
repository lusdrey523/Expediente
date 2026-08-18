# Expediente

Repositorio de infraestructura documental y trazabilidad del Expediente Maestro Migratorio (EMM).

## Propósito

Este repositorio proporciona una capa controlada para registrar, preservar y verificar la evolución documental del expediente mediante historial Git, Pull Requests, verificaciones y registros de control.

GitHub funciona como infraestructura de trazabilidad y control de cambios. No sustituye la evidencia primaria ni certifica por sí mismo la verdad de hechos jurídicos, la autenticidad material de documentos externos, la elegibilidad migratoria ni conclusiones legales.

## Estado actual de la infraestructura

- **Repositorio:** `lusdrey523/Expediente`
- **Rama principal:** `main`
- **SHA actual de `main`:** `2233cb6f2c80ba474a171a467feab278906480a5`
- **Último hito integrado:** PR #13 — `EMM-GOV-OPS-001`
- **Integración de PR #13:** `2026-08-18T19:18:15Z`
- **Cadena PR integrada:** PR #1 → PR #13.
- **PR en ejecución:** PR #14 — `EMM-F01-SOURCE-INTAKE-001`
- **Cadena de evidencia sustantiva:** preparada a nivel de control; F-01 continúa condicionado a la recepción verificable del paquete fuente auditado.
- **Cadena temporal:** preparada a nivel de infraestructura; la cronología fáctica debe reconstruirse separando tiempo del hecho, emisión, adquisición, observación, incorporación, modificación y verificación.

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
8. **Normalización documental:** los nuevos documentos controlados deben seguir el estándar de idioma, nomenclatura y metadatos vigente; los históricos se normalizan mediante migraciones controladas.
9. **Gobernanza activa:** la Constitución, el estándar de metadatos, el modelo de autoridad y el protocolo de control documental rigen la infraestructura desde su integración efectiva en `main`.
10. **No inferencia:** ningún documento fuente, hecho, fecha o relación faltante se reconstruye por memoria, nombre de archivo o suposición cuando pueda preservarse como desconocido o pendiente de verificación.

## Límites

La infraestructura demuestra principalmente **qué fue incorporado, cuándo fue registrado, mediante qué cambio controlado y qué estado de verificación recibió dentro del repositorio**. No convierte automáticamente esos registros en prueba de la verdad material de los hechos subyacentes.

## Roadmap

El orden de evolución está definido en `repository-governance/ROADMAP.md`.

El gate actual es **Stage 4 / F-01 — Evidence register foundation**. PR #11 estableció el intake; PR #12 estableció la Constitución; PR #13 activó el gobierno documental. PR #14 prepara el recibo controlado del paquete fuente sin afirmar que dicho paquete haya sido recibido o verificado en esta rama.

La futura interfaz para abogado, autenticación segura y arquitectura multicaso permanecen como etapas posteriores. GitHub Pages puede servir como presentación, pero no constituye por sí mismo una frontera de autenticación para información sensible.

## Regla de sincronización de trazabilidad

Todo PR que incorpore una modificación relevante debe actualizar, dentro del mismo PR, los cuatro instrumentos de continuidad institucional:

- `README.md`
- `CHANGELOG.md`
- `repository-governance/TRACEABILITY_REGISTER.md`
- `repository-governance/VERIFICATION_REGISTER.md`

Estos archivos representan el estado documental de la infraestructura. En un PR abierto pueden describir el estado propuesto del cambio; al entrar en `main`, el siguiente estado integrado debe quedar registrado en el mismo cambio controlado o en el siguiente PR legítimo, sin PRs de mera limpieza cuando la corrección pueda incorporarse con la siguiente evolución sustantiva.

## Continuidad

Las nuevas capas deben incorporarse mediante cambios controlados y quedar reflejadas en los cuatro instrumentos de continuidad sin alterar retrospectivamente la cadena histórica. Las etapas planificadas no deben presentarse como completadas hasta contar con su correspondiente estado de aceptación/verificación.
