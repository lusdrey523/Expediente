# Expediente

Repositorio de infraestructura documental y trazabilidad del Expediente Maestro Migratorio (EMM).

## Propósito

Este repositorio proporciona una capa controlada para registrar, preservar y verificar la evolución documental del expediente mediante historial Git, Pull Requests, verificaciones y registros de control.

GitHub funciona como infraestructura de trazabilidad y control de cambios. No sustituye la evidencia primaria ni certifica por sí mismo la verdad de hechos jurídicos, la autenticidad material de documentos externos, la elegibilidad migratoria ni conclusiones legales.

## Estado actual de la infraestructura

- **Repositorio:** `lusdrey523/Expediente`
- **Rama principal:** `main`
- **Último hito integrado:** PR #6 — `EMM-AUDIT-001`
- **Estado de la capa Git y de gobernanza auditada:** PASS dentro del alcance definido por `INTEGRITY_AUDIT_EMM-001.md`.
- **Cadena PR:** PR #1 → PR #6, con verificaciones post-merge incorporadas progresivamente.
- **Cadena de evidencia sustantiva:** aún en fase de incorporación y formalización.
- **Cadena temporal:** preparada a nivel de control, con separación requerida entre tiempo del hecho, emisión, adquisición, observación, incorporación, modificación y verificación.

## Arquitectura de evolución

La infraestructura se desarrolla de forma incremental y modular. La capa de trazabilidad y gobernanza constituye el núcleo de control sobre el cual pueden incorporarse posteriormente módulos de hechos, evidencias, documentos, verificaciones y paquetes de trabajo jurídico.

La incorporación de nuevos módulos debe conservar la trazabilidad histórica, evitar la reescritura retroactiva de verificaciones y mantener explícitos los límites de cada afirmación documental.

## Principios de infraestructura

1. **Trazabilidad:** todo cambio controlado debe poder relacionarse con su PR, commit, estado de integración y verificación correspondiente.
2. **Integridad histórica:** los eventos ya registrados no se reescriben para mejorar retrospectivamente su resultado.
3. **Separación de capas:** infraestructura, evidencia, hechos y análisis jurídico deben conservar límites explícitos.
4. **Evolución incremental:** los nuevos componentes se acoplan progresivamente al núcleo existente sin exigir una reconstrucción de la cadena histórica.
5. **Preservación temporal:** cuando un evento dependa del tiempo, deben conservarse los timestamps disponibles y distinguirse las distintas clases de tiempo relevantes.
6. **Verificación explícita:** una incorporación documental no se considera equivalente a una verificación; ambas deben quedar identificadas por separado.
7. **Interoperabilidad futura:** la infraestructura se diseña con convenciones suficientemente claras y modulares para permitir su eventual adaptación a estándares externos o institucionales, sin crear dependencia actual respecto de ellos.

## Límites

La infraestructura demuestra principalmente **qué fue incorporado, cuándo fue registrado, mediante qué cambio controlado y qué estado de verificación recibió dentro del repositorio**. No convierte automáticamente esos registros en prueba de la verdad material de los hechos subyacentes.

## Próxima evolución

El siguiente desarrollo debe concentrarse en incorporar el cuerpo documental y de evidencia utilizando esta infraestructura como capa de control, preservando la separación entre:

- hechos;
- evidencias;
- documentos;
- metadatos de procedencia e integridad;
- verificaciones;
- análisis jurídico.

La estructura podrá evolucionar conforme aumente el alcance del expediente, siempre que las nuevas capas sean compatibles con la trazabilidad ya consolidada.
