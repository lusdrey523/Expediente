---
id: EMM-REC-SOURCE-001
title: Registro de Recepción del Paquete Fuente para Reconstrucción Documental
version: 1.0.0
status: Pending
language: es-CL
jurisdiction: Chile
system: Expediente Maestro Migratorio (EMM)
document_type: receipt
owner_role: Repository Administrator
created_at: 2026-08-18
last_updated_at: 2026-08-18
effective_date: null
related_pr: PR #14
---

# Registro de Recepción del Paquete Fuente para Reconstrucción Documental

## 1. Propósito

Registrar de forma controlada la recepción, identificación, preservación y verificación del paquete fuente que servirá como input para F-01.

Este registro es deliberadamente `Pending` hasta que el paquete exacto sea presentado como input verificable y su SHA-256 sea comprobado independientemente.

## 2. Identidad histórica declarada

| Campo | Valor |
|---|---|
| Paquete fuente declarado | `Legalbreto-main.zip` |
| SHA-256 declarado en el baseline auditado | `26f599f89d7e546deb53ad316123f16cf6683015547a7f5bc5eb2c99f628435f` |
| Inventario histórico reportado | 48 archivos |
| Evaluación asociada | `EMM_SYSTEM_ASSESSMENT_001` |
| Estado de recepción actual en este registro | Pendiente de verificación independiente |

Los datos anteriores son referencias históricas del baseline. No constituyen por sí mismos una nueva recepción del archivo.

## 3. Condiciones para cambiar el estado

El registro solo podrá pasar a un estado operativo posterior cuando exista evidencia reproducible de:

1. recepción del paquete exacto;
2. identificación inequívoca del archivo;
3. cálculo independiente de SHA-256;
4. coincidencia o explicación documentada de cualquier divergencia respecto del SHA histórico;
5. preservación del input exacto utilizado para F-01;
6. inventario del contenido sin modificar la fuente.

## 4. Regla de no inferencia

No se considera recibido un paquete porque su nombre, hash o inventario aparezca en registros históricos. Tampoco se reconstruirá su contenido a partir de memoria, prompts, nombres de archivos o copias parciales no verificadas.

## 5. Salida prevista de F-01

Una vez satisfechas las condiciones anteriores, este registro podrá vincularse al primer registro controlado de evidencia y a los hashes individuales de los artefactos incorporados.

## 6. Límite

Este registro controla procedencia e intake documental. No certifica por sí mismo autenticidad material, verdad de hechos jurídicos, elegibilidad migratoria ni conclusiones legales.
