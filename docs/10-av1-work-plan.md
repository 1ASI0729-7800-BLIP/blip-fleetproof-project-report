# Plan de Trabajo AV1 y TB1

## Criterios de estado

Completado indica un artefacto elaborado con evidencia del alcance descrito, no aprobación académica. En revisión indica trabajo disponible pendiente de aceptación; en progreso, avance parcial; pendiente, falta de evidencia suficiente. Las fechas, horas y cumplimiento a tiempo deben confirmarse con el equipo.

## Roles AV1 y alcance documentado

| Integrante | Rol AV1 | Responsabilidad principal | Evidencia mínima |
|---|---|---|---|
| Reyes Limo Sebastian | Team Leader, SCM y Capítulo II Owner | Organizar el informe y elaborar investigación, entrevistas, Needfinding y artefactos del capítulo II. | Capítulo II, enlaces y evidencias del informe. |
| Quintanilla Gonzalo | Lean UX Owner | Capítulo I: Startup Profile, Solution Profile, Problem Statement, Assumptions, Hypothesis Statements y Lean UX Canvas. | 1 rama, 3 commits, 1 Pull Request, captura de Lean UX Canvas. |
| Morales Jefferson | Colaborador UX Research | Apoyo en investigación y registro de perfil de integrante; no se atribuye la autoría principal del capítulo II. | Perfil y registro de apoyo AV1. |
| Gómez De La Torre Rodrigo | Requirements Owner | Capítulo III: User Stories, Acceptance Criteria, Impact Map y Product Backlog. | 1 rama, 3 commits, 1 Pull Request, backlog público. |
| Gorbeña Eduardo | Product Design and Landing Page Owner | Capítulo IV y Landing Page v1.0.0: wireframes, mock-ups, style guide y despliegue. | 1 rama, 5 commits, 1 Pull Request, URL desplegada y release. |

El plan histórico y las ramas sugeridas no sustituyen la evidencia de autoría. Para TB1, la distribución vigente por bounded context se documenta en el Workplan y en la matriz LACX del capítulo V.

## Ramas AV1 sugeridas

| Rama | Dueño | Objetivo |
|---|---|---|
| `feature/sprint1-scm` | Reyes Limo Sebastian | Completar GitFlow, herramientas y Capítulo V 5.1. |
| `feature/sprint1-capitulo-1` | Quintanilla Gonzalo | Completar Capítulo I. |
| `feature/sprint1-capitulo-2` | Reyes Limo Sebastian | Incorporar los artefactos de Needfinding del proyecto BLIP FleetProof. |
| `feature/sprint1-entrevistas` | Morales Jefferson | Completar entrevistas y análisis competitivo. |
| `feature/sprint1-capitulo-3` | Gómez De La Torre Rodrigo | Completar Capítulo III. |
| `feature/sprint1-capitulo-4` | Gorbeña Eduardo | Completar Capítulo IV. |
| `feature/us001-landing-page-value-proposition` | Equipo | Implementar primera User Story de Landing Page. |

## Entregables AV1

Las ramas anteriores son propuestas de organización; se crean al iniciar cada aporte.
AV1 corresponde al Sprint 1 según la guía del curso. El nombre de una rama no
sustituye el Sprint Planning, el Sprint Backlog ni las evidencias del trabajo realizado.
Las cantidades de commits indicadas en este plan son orientativas internas y no
deben interpretarse como mínimos impuestos por la rúbrica.

| Entregable | Responsable | Fecha límite interna | Estado |
|---|---|---|---|
| Informe Markdown hasta Capítulo V | Reyes Limo Sebastian | Por confirmar | Completado: artefactos AV1 documentados. |
| Lean UX Process | Quintanilla Gonzalo | Por confirmar | Completado: capítulo I. |
| UX Research plan | Sebastian, con apoyo de Jefferson | Por confirmar | Completado: capítulo II. |
| User Stories and Product Backlog | Gómez De La Torre Rodrigo | Por confirmar | Completado: capítulo III. |
| Landing Page v1.0.0 desplegada | Gorbeña Eduardo | Por confirmar | Completado: evidencia Sprint 1. |
| Keynote AV1 | Equipo | Por confirmar | Pendiente verificar archivo final entregado. |
| Video de exposición AV1 | Equipo | Por confirmar | Pendiente incorporar enlace de entrega. |
| Participant Performance Report AV1 | Team Leader | Por confirmar | Completado: documento AV1 disponible como referencia. |

## Workplan TB1 — Sprint 2

| Responsable | Trabajo asignado y desarrollado | Tareas | Estado y evidencia |
|---|---|---|---|
| Sebastian Reyes Limo | Base Angular, shared, i18n, Fleet Management, identidad visual y documentación. | T12, T13, T19, T22, T23 | En revisión: commits y capturas; CSV y casos requieren prueba completa. Capítulo V integrado en develop; PPTX elaborado. |
| Gonzalo Quintanilla | IAM: acceso, registro y perfil. | T14 | En revisión: commit UserAssembler, acceso demo y perfil capturados; registro y edición por validar. |
| Eduardo Gorbeña | Vehicle Information: registro, listado y consulta. | T15 | En revisión: commit del módulo y listado capturado; registro y consulta nuevos por validar. |
| Rodrigo Gómez De La Torre | Report Management: reportes, semáforo, PDF y comparación. | T16, T17, T18, T20 | En revisión: commits y capturas; generación nueva y PDF por validar. |
| Jefferson Morales | Vehicle Monitoring: monitoreo y alertas. | T21 | En revisión: commits y capturas; nuevo ciclo y alerta resultante por validar. |
| Equipo | Integración y validación completa del frontend. | T24 | Pendiente documentar integración remota y aceptación de historias. |
| Responsable por confirmar | Netlify y Render. | T25 | En revisión: Netlify Published; Render Building, conexión pública por validar. |

### Entregables TB1

| Entregable | Responsable | Plazo interno | Estado |
|---|---|---|---|
| Planning, LACX, backlog y evidencias Sprint 2 | Sebastian | Por confirmar | Completado: capítulo V integrado en develop, merge 39c9d93. |
| Conclusiones, anexos y workplan | Sebastian | Por confirmar | En revisión: actualización de cierre preparada. |
| Frontend v1 | Equipo | Por confirmar | En revisión: publicado, criterios completos pendientes de aceptación. |
| Landing Page actualizada TB1 | Por confirmar | Por confirmar | Pendiente verificar mejoras y nueva publicación. |
| Presentación TB1 | Sebastian | Por confirmar | En revisión: PPTX elaborado; revisión final pendiente. |
| Performance Report TB1 | Team Leader | Por confirmar | En revisión: tareas actualizadas; evaluar cumplimiento y notas. |
| Student Outcome TB1 | Cada integrante | Por confirmar | Pendiente revisar aportes de esta entrega. |
| Videos y ZIP complementario | Equipo | Por confirmar | Pendiente incorporar evidencias finales. |
| Postman y publicación Fake API | Por confirmar | Por confirmar | Pendiente completar evidencia HTTP y Render publicado. |

## Checklist diario

- Cada integrante registra al menos un avance en su rama.
- Cada rama mantiene commits pequeños y con Conventional Commits.
- Cada sección nueva tiene evidencia o una actividad pendiente explícita.
- Cada imagen del informe se conserva en `docs/assets/chapter-<n>/`.
- Cada entrega parcial se revisa contra Programación, Redacción y GitHub.
