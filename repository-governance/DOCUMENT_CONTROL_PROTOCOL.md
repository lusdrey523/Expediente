---
id: EMM-PROTO-DOC-001
title: Protocolo de Control Documental del Proyecto EMM
version: 1.0.0
status: Active
language: es-CL
jurisdiction: Chile
system: Expediente Maestro Migratorio (EMM)
document_type: protocol
owner_role: Repository Administrator
created_at: 2026-08-18
last_updated_at: 2026-08-18
effective_date: 2026-08-18
---

# Protocolo de Control Documental del Proyecto EMM

## 1. Propósito

Establecer el procedimiento operativo común para crear, modificar, aprobar, incorporar, verificar, sustituir y retirar documentos controlados sin romper la cadena histórica del proyecto.

## 2. Regla de autoridad

La Constitución y los instrumentos normativos superiores determinan la autoridad documental. Este protocolo ejecuta esas reglas y no puede contradecirlas.

## 3. Ciclo documental

Cada documento controlado sigue, según corresponda, este ciclo:

**Propuesta → revisión → aprobación → incorporación → verificación → mantenimiento → sustitución/archivo.**

La aprobación es un evento de decisión; `Active` es el estado documental que representa que esa decisión ya produjo vigencia dentro del repositorio. Un documento en una rama de PR no modifica por sí mismo el estado vinculante de `main`.

## 4. Estados

Los estados permitidos son los definidos por `METADATA_STANDARD.md`:

- `Proposed`: propuesto, sin vigencia.
- `Active`: aprobado y vigente dentro del alcance declarado.
- `Superseded`: reemplazado por una versión posterior.
- `Deprecated`: retirado para uso nuevo, conservando su historia.
- `Archived`: conservado únicamente como registro histórico.

No se utilizará `Approved` como estado documental independiente. Cuando una decisión de aprobación se materializa mediante merge a `main`, el estado resultante debe representarse como `Active` cuando el instrumento corresponda a una norma vigente.

## 5. Cambios mediante PR

Todo cambio normativo, estructural o de control relevante debe ejecutarse mediante un PR único que contenga el conjunto coherente de modificaciones.

El mismo PR debe actualizar los cuatro instrumentos de continuidad:

1. `README.md`;
2. `CHANGELOG.md`;
3. `repository-governance/TRACEABILITY_REGISTER.md`;
4. `repository-governance/VERIFICATION_REGISTER.md`.

Cuando el cambio requiera varios archivos, estos forman una sola unidad de cambio aunque GitHub muestre múltiples commits intermedios en la rama. La aceptación final debe utilizar el método fundador-controlado establecido para el proyecto.

## 6. Verificación pre-merge y estado vinculante

La verificación de una rama puede confirmar que una propuesta es coherente y apta para aceptación. No debe presentarse como un evento de integración.

Una vez producido el merge efectivo en `main`, el siguiente registro debe representar el estado real de integración y, cuando corresponda, convertir la propuesta normativa en `Active` mediante un nuevo evento controlado dentro del siguiente PR sustantivo. No se crea un PR de mera limpieza si la corrección puede incorporarse legítimamente al siguiente cambio.

## 7. Integridad histórica

No se reescriben commits, timestamps, PR históricos ni verificaciones para hacerlos coincidir con una interpretación posterior. Una corrección se registra como un evento nuevo que referencia el evento anterior.

## 8. Metadatos e idioma

Los documentos nuevos deben usar el esquema de `METADATA_STANDARD.md` y español como idioma normativo principal. Los identificadores técnicos, nombres de archivos, comandos y términos internacionales pueden conservar su forma original cuando sea necesario.

## 9. Evidencia y documentos derivados

La incorporación de una copia, extracción, clasificación o resumen no sustituye la fuente. Todo derivado relevante debe mantener vínculo con su fuente y declarar si su contenido fue transformado.

## 10. Límite probatorio

El control documental demuestra el estado de los registros dentro del sistema. No convierte por sí mismo un documento en auténtico, un hecho en verdadero ni un análisis en asesoría jurídica profesional.
