---
id: EMM-POL-AUTH-001
title: Modelo de Autoridad y Separación de Funciones del Proyecto EMM
version: 1.0.1
status: Active
language: es-CL
jurisdiction: Chile
system: Expediente Maestro Migratorio (EMM)
document_type: policy
owner_role: Project Owner
created_at: 2026-08-18
last_updated_at: 2026-08-18
effective_date: 2026-08-18
related_pr: PR #12
related_commit: 67d540bfcc00db3413432da334545bdf4204fb13
---

# Modelo de Autoridad y Separación de Funciones del Proyecto EMM

## 1. Propósito

Definir quién puede decidir, ejecutar, verificar, preservar y revisar cada clase de actividad del proyecto, evitando que una sola capa se atribuya autoridad que no le corresponde.

## 2. Línea de mando documental

La línea de precedencia es:

**Constitución → Políticas/Estándares → Protocolos → Registros/Modelos → Documentos y artefactos → Interfaces.**

Esta línea describe autoridad documental interna, no una jerarquía sobre la autoridad legal del Estado ni sobre el criterio profesional del abogado.

## 3. Matriz de funciones

| Función | Puede aprobar | Puede ejecutar | Puede verificar | Puede modificar hechos/evidencia fuente |
|---|---|---|---|---|
| Project Owner | Arquitectura y políticas | Sí | Cuando el protocolo lo permita | No de forma silenciosa |
| Repository Administrator | Cambios técnicos delegados | Sí | Controles técnicos | No |
| Evidence Custodian | Recepción/preservación según protocolo | Sí | Preservación propia si el protocolo lo permite | No |
| Verifier | No sustituye aprobación | Sí | Sí, dentro del alcance | No |
| Legal Reviewer | Análisis jurídico profesional | Sí | Revisión jurídica | No altera evidencia fuente |

## 4. Regla de independencia

Cuando un protocolo requiera verificación independiente, la persona que realizó la modificación no debe ser la única persona que certifique su propio resultado.

Si la independencia no es materialmente posible, el registro debe declarar la limitación y reducir el alcance de la conclusión.

## 5. Cambios constitucionales

Una modificación de la Constitución requiere:

1. propuesta identificable;
2. revisión de impacto;
3. Pull Request controlado;
4. aprobación del Project Owner;
5. verificación de integración;
6. registro de versión y vigencia.

La aprobación se considera materializada cuando el evento de decisión y la integración efectiva quedan registrados. El estado `Active` representa la vigencia posterior a esa materialización.

## 6. Cambios de evidencia

La evidencia fuente debe preservarse como referencia inmutable. Las representaciones normalizadas, extractos o clasificaciones son derivados controlados y deben mantener vínculo con la fuente.

## 7. Cambios de hechos

Los registros fácticos deben distinguir entre el hecho documentado y la interpretación. Una corrección factual debe conservar la versión anterior y explicar la razón del cambio.

## 8. Análisis jurídico

El análisis jurídico debe quedar separado de los hechos y de la evidencia. El sistema puede organizar preguntas, fuentes y argumentos, pero no debe presentar una conclusión automatizada como asesoría jurídica profesional.

## 9. Acceso futuro

La futura aplicación multicaso deberá implementar autorización por rol y, como mínimo, aislamiento por caso. La interfaz no podrá ampliar privilegios respecto de los definidos por el modelo de autoridad.

## 10. Auditoría

Las actividades críticas deben poder reconstruirse mediante actor/rol, fecha-hora, objeto afectado, motivo, cambio, evidencia de ejecución y resultado de verificación cuando aplique.
