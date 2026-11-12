# Registro de Versiones del Informe

| Versión | Fecha | Autor | Descripción de modificación |
|---|---|---|---|
| 0.1.0 | 2026-09-12 | BLIP | Estructura base del informe de Open Source; el aporte del Capítulo II se desarrolla en una rama independiente. |
| 0.2.0 | 2026-09-17 | Reyes Limo, Sebastian | Corrección de roles y responsabilidades del equipo (README), actualización del estado real de los capítulos en Estado AV1, y completado del cuadro de Student Outcome con las acciones de todos los integrantes. |
| 0.3.0 | 2026-10-06 | Reyes Limo, Sebastian | Documentación de Sprint 2, 19 capturas y colaboración; actualización de conclusiones, anexos, workplan y estados para TB1. Revisión final de entrega pendiente. |
| 0.4.0 | 2026-11-12 | Equipo BLIP | Integración de las correcciones de los capítulos I–V, actualización del stack a Angular y Spring Boot, incorporación de trazabilidad de requisitos, seis bounded contexts del frontend y validaciones moderadas de Sprint 3. |
| 0.4.1 | 2026-11-12 | Quintanilla Pozo, Gonzalo Samuel | Revisión transversal del README, Student Outcome, Sprint 3, conclusiones, anexos, workplan y control de calidad; alineación del estado documentado con los repositorios actuales. |

## Revisión editorial local — 09/11/2026

Se preparó una revisión de redacción, tablas, referencias, NRC, coherencia del stack, anexos, conclusiones y workplan. Esta revisión no constituye una release ni certifica el cierre funcional de historias. Las pruebas y las evidencias de las entregas mantienen sus fechas originales.

# Project Report Collaboration Insights

## Repositorio

URL del repositorio del informe: https://github.com/1ASI0729-7800-BLIP/blip-fleetproof-project-report

## Estrategia de colaboración

El equipo BLIP elaborará el informe en Markdown usando GitHub como sistema de control de versiones. El archivo principal será `README.md` y cada capítulo tendrá un archivo independiente en `docs/`, con el fin de reducir conflictos de edición y evidenciar aportes individuales.

## Evidencias por entrega

| Entrega | Evidencia requerida | Estado |
|---|---|---|
| AV1 | Commits, ramas, Pull Requests, merges y capturas de colaboración del informe. | Completado: registro histórico de Sprint 1. |
| TB1 | Actualización de commits, mejoras sobre feedback y nueva versión del informe. | Documentado: Sprint 2 integrado; se conservan pendientes de aceptación y evidencias finales. |
| Sprint 3 / preparación de AV2 | Correcciones de los capítulos I–V, validación moderada del frontend e inicio del backend Spring Boot. | Integrado en `develop`; el producto continúa en desarrollo y no constituye cierre final. |
| AV2 | Evidencias ampliadas de colaboración, validación y mejoras. | En preparación: completar pruebas autónomas, trazabilidad, backend y artefactos de entrega. |
| TB2 | Evidencia final de colaboración durante todo el ciclo. | Pendiente: entrega posterior. |

## Convenciones de GitFlow

| Tipo | Convención |
|---|---|
| Main branch | `main` |
| Development branch | `develop` |
| Report feature branch | `feature/sprint<n>-capitulo-<n>` y `feature/sprint<n>-cierre-entrega`; actualmente Sprint 3 |
| Feature branch | `feature/usXXX-<short-name>` |
| Release branch | `release/vX.Y.Z` |
| Hotfix branch | `hotfix/<short-name>` |

## Versiones requeridas por producto

| Producto | Releases requeridos |
|---|---|
| Landing Page | `v1.0.0`, `v2.0.0`, `v3.0.0`, `v4.0.0` |
| Frontend Web Application | `v1.0.0`, `v2.0.0`, `v3.0.0` |
| Web Services | `v1.0.0`, `v2.0.0` |
