---
id: EMM-CONST-001
title: Constitución Documental y de Gobernanza del Proyecto EMM
version: 1.0.0
status: Proposed
language: es-CL
jurisdiction: Chile
system: Expediente Maestro Migratorio (EMM)
document_type: constitution
owner_role: Project Owner
effective_date: null
created_at: 2026-08-18
last_updated_at: 2026-08-18
---

# Constitución Documental y de Gobernanza del Proyecto EMM

## 1. Naturaleza

Esta Constitución es el instrumento rector de la infraestructura documental y operativa del Proyecto Expediente Maestro Migratorio (EMM).

Su función es establecer los principios, límites, jerarquía documental, autoridades operativas, reglas de cambio, controles de integridad, ciclos de verificación y relaciones entre las distintas capas del sistema.

La Constitución gobierna **el sistema documental y su infraestructura**. No sustituye la legislación chilena, las decisiones de la autoridad competente ni el criterio profesional del abogado que revise el caso.

## 2. Principios superiores

1. **Integridad histórica:** ningún evento histórico se reescribe para mejorar retrospectivamente su resultado.
2. **Procedencia:** ningún registro sustantivo se considera confiable únicamente por existir dentro del repositorio.
3. **Separación de capas:** gobierno de infraestructura, gobierno del caso, evidencia, hechos, documentos, verificaciones y análisis jurídico tienen responsabilidades diferenciadas.
4. **Trazabilidad:** toda modificación controlada debe poder relacionarse con una causa, autor, cambio, PR/commit y estado de verificación cuando corresponda.
5. **Temporalidad:** los tiempos del hecho, emisión, adquisición, observación, incorporación, modificación y verificación son categorías distintas y no deben colapsarse sin justificación.
6. **No inferencia:** cuando un dato es desconocido, ausente o no verificable, se registra como tal. No se completa por memoria, apariencia, nombre de archivo o suposición.
7. **Verificación explícita:** incorporación, preservación y verificación son eventos distintos.
8. **Mínimo privilegio:** cada autoridad operativa debe tener únicamente las capacidades necesarias para su función.
9. **Reversibilidad controlada:** una corrección posterior se representa mediante un nuevo evento; no mediante la alteración silenciosa de la historia.
10. **Interoperabilidad futura:** las convenciones deben facilitar una futura adaptación tecnológica o institucional sin crear dependencia actual de sistemas externos.

## 3. Jerarquía normativa interna

Dentro del proyecto, y exclusivamente para su gobierno documental y operativo, rige la siguiente precedencia:

1. **Esta Constitución.** Define principios, autoridad, límites y reglas superiores.
2. **Políticas y estándares constitucionalmente derivados.** Desarrollan reglas generales sin contradecir la Constitución.
3. **Protocolos operativos.** Definen procedimientos concretos para ejecutar los estándares.
4. **Registros y modelos controlados.** Capturan estados, eventos, relaciones y resultados.
5. **Documentos y artefactos del caso.** Constituyen el contenido gestionado por las capas anteriores.
6. **Presentaciones e interfaces.** Exponen información controlada; no adquieren autoridad por el hecho de presentarla.

Ningún documento de nivel inferior puede derogar, reinterpretar silenciosamente o contradecir una regla superior.

## 4. Arquitectura de gobierno

### 4.1 Gobierno de infraestructura

`repository-governance/` gobierna el repositorio como infraestructura: estructura, trazabilidad Git, PR, verificaciones, convenciones, roadmap, integridad y controles de cambio.

### 4.2 Gobierno del caso

`docs/case-governance/` gobierna las reglas específicas para organizar y controlar la documentación sustantiva del caso.

### 4.3 Capas sustantivas

Las capas `evidence/`, `facts/`, `documents/`, `verifications/` y `legal-analysis/` gestionan contenido especializado conforme a las reglas superiores. No pueden modificar unilateralmente la jerarquía de gobierno.

### 4.4 Aplicación futura

Una interfaz web o aplicación puede consultar y presentar información controlada, pero no se convierte por ello en fuente primaria ni en autoridad superior al registro documental subyacente.

## 5. Autoridades y separación de funciones

### Project Owner

Autoridad operativa superior del proyecto para aprobar arquitectura, prioridades, políticas internas y cambios constitucionales. Esta autoridad no convierte opiniones personales en hechos probados ni sustituye la revisión jurídica profesional.

### Repository Administrator

Responsable de mantener la infraestructura Git/GitHub, ramas, PR y controles técnicos. No puede alterar unilateralmente hechos o conclusiones jurídicas.

### Evidence Custodian

Responsable de preservar, identificar y controlar la procedencia de evidencia y artefactos fuente. No debe modificar silenciosamente el contenido fuente.

### Verifier

Responsable de ejecutar verificaciones definidas por protocolo y registrar resultados reproducibles. La verificación debe declarar su alcance y sus límites.

### Legal Reviewer

Profesional jurídico que revisa cuestiones legales, suficiencia documental y conclusiones jurídicas. Su función no queda subordinada a una etiqueta técnica de PASS del repositorio.

Una misma persona puede ejercer más de un rol cuando sea necesario, pero el registro debe conservar qué función ejerció en cada evento. Cuando un control exija independencia, esa independencia debe satisfacerse mediante una persona o proceso distinto y quedar registrada.

## 6. Regla de autoridad sobre el contenido

La infraestructura puede demostrar que un archivo, registro o cambio fue incorporado, preservado o verificado bajo determinadas condiciones. No puede transformar por sí misma una afirmación en un hecho verdadero ni un hash en una certificación de autenticidad material.

Las conclusiones jurídicas deben permanecer identificadas como análisis profesional, no como hechos.

## 7. Control de cambios

Todo cambio estructural o normativo relevante debe ejecutarse mediante el mecanismo controlado de Pull Request establecido por el proyecto.

Cuando el fundador/Project Owner deba intervenir manualmente para completar un merge, el registro debe conservar como mínimo: número de PR, título exacto del commit, mensaje exacto, SHA esperado del head, método de merge, SHA resultante y fecha/hora disponible.

Los commits de merge y registros históricos no deben editarse retrospectivamente para corregir una representación posterior.

## 8. Estados de autoridad

Un documento puede encontrarse, como mínimo, en los estados `Proposed`, `Active`, `Superseded`, `Deprecated` o `Archived`.

`Proposed` no equivale a norma vigente. Una regla constitucional o política pasa a ser obligatoria únicamente cuando su estado de entrada en vigor haya sido registrado.

## 9. Idioma y metadatos

El idioma normativo principal del proyecto será español. Los nombres técnicos, comandos, identificadores y términos que deban conservar su forma internacional podrán permanecer en inglés.

Todo documento controlado debe utilizar el esquema de metadatos definido por el estándar vigente. Los documentos históricos no se reescriben únicamente para uniformarlos; su normalización se realiza como migración controlada.

## 10. Auditoría y verificación

El proyecto operará mediante ciclos: planificación → ejecución → verificación → aceptación → registro → siguiente ciclo.

Una auditoría debe declarar alcance, baseline, método, evidencia utilizada, resultado, condiciones y límites.

`PASS` siempre es relativo al alcance declarado. Nunca debe interpretarse como certificación universal del expediente.

## 11. Conflicto normativo

Si dos documentos internos entran en conflicto, debe aplicarse la jerarquía normativa. El conflicto debe registrarse y resolverse mediante un cambio controlado.

Si una regla interna entra en conflicto con una obligación legal aplicable, la obligación legal prevalece y el conflicto debe remitirse a revisión jurídica.

## 12. Evolución

Esta Constitución puede evolucionar, pero toda modificación debe conservar la versión anterior como evento histórico y explicar qué cambió, por qué cambió, quién la aprobó y desde cuándo rige.

La compatibilidad futura con otros estándares es un objetivo arquitectónico. No crea actualmente subordinación, dependencia, incorporación ni autoridad externa sobre este proyecto.

## 13. Gate de entrada

Esta versión se registra inicialmente como `Proposed`. Antes de declararse `Active` debe existir un evento de aprobación y, cuando corresponda, una verificación de consistencia con la infraestructura vigente.
