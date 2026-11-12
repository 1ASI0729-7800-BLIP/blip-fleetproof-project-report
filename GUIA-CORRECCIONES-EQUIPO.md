# Guía de correcciones restantes — Eduardo y Rodrigo

Revisión editorial local del 9 de noviembre de 2026. Esta guía coordina el trabajo; no forma parte del contenido académico del informe ni acredita tareas realizadas por sus destinatarios. No requiere repetir la auditoría completa.

## Lo preparado por Sebastian

Se armonizaron NRC y enlaces de organización, tecnologías en textos y diagramas editables, formato de criterios de aceptación, IDs del backlog, conclusiones, anexos, bibliografía y workplan. Se conservan las entrevistas, imágenes e historial de Sprint 1 y Sprint 2. No se incorporaron las 34 tareas ni las pruebas de la rama de auditoría como si ya estuvieran aceptadas o integradas.

## Rodrigo: investigación y requisitos

| Dónde | Qué incorporar o corregir | Criterio de cierre |
|---|---|---|
| Capítulo I: segmentos y Lean UX | Definir el segmento prioritario y explicar qué entrevistas lo respaldan. Separar hipótesis de beneficios medidos. | Ninguna afirmación de validación comercial o reducción de tiempos carece de resultados. |
| Capítulo II, 2.2.3 y 2.3 | Cotejar los resúmenes con las entrevistas existentes, especialmente Roxana y Cristhian. Añadir referencia al video y minuto cuando se sustente un hallazgo. | Cada hallazgo tiene fuente identificable; porcentajes solo con muestra y cálculo comprobables. |
| Capítulo III, después de 3.3 | Añadir matriz: entrevista/hallazgo, necesidad, requisito, US, criterio de aceptación y prueba. | Cada historia seleccionada puede rastrearse hasta una necesidad; los requisitos técnicos se identifican como tales. |
| Capítulo III, US05; capítulo V, servicios | Acordar el contrato de consulta por placa: método, ruta, parámetro, respuesta y errores. Distinguirlo de la búsqueda por ID del mock. | El contrato documentado coincide con la implementación comprobada o queda identificado como objetivo. |
| Capítulo V, 5.2.2.3; planificación de Sprint 3 | Descomponer historias en Engineering Tasks de 4 a 8 horas. Usar columnas US ID, título US, Task ID, título, descripción, horas estimadas, responsable y estado. | IDs únicos, sumas verificadas y responsables acordados. No convertir story points en horas ni reconstruir estimaciones históricas. |

US04 identifica evaluación de riesgo; US05 identifica contrato API. Al corregir el alcance y los puntos, revisar todas las referencias de Sprint 2: la selección US03/US04/US06/US07 suma 26 según las estimaciones de sus historias, no 24. Si el compromiso histórico fue distinto, documentar la diferencia en vez de reescribirlo.

## Eduardo: diseño y evidencia

| Dónde | Qué incorporar o corregir | Criterio de cierre |
|---|---|---|
| Capítulo IV, arquitectura y diagramas | Revisar las imágenes externas y contrastarlas con los diagramas editables ya armonizados. Distinguir seis contextos objetivo de cinco módulos frontend y soporte `shared`. | Ninguna imagen se presenta como implementación actual si corresponde a otra tecnología o a diseño futuro. |
| Capítulo IV, reglas de dominio; capítulo II, 2.5 | Especificar origen y fecha de datos, vigencia, fuente no disponible, riesgo no evaluado, permisos, responsable y evidencia necesaria para cerrar casos. | Las reglas tienen criterios comprobables y se distingue propuesta de funcionalidad implementada. |
| Capítulo V, 5.2.2.4 y 5.2.2.5 | Vincular historias con commits y pruebas completas: registro, consulta, reporte/PDF, CSV, monitoreo, alerta y resolución. | Cada prueba indica fecha, entorno, datos sintéticos, resultado esperado, resultado observado y evidencia. No basta una captura del menú. |
| Capítulo V, 5.2.2.6 | Adjuntar solicitudes y respuestas de Postman: URL, método, código HTTP y cuerpo sin secretos. | Los endpoints y errores coinciden con el contrato; Fake API y backend definitivo se documentan por separado. |
| Capítulo V, 5.2.2.7 | Incorporar publicación exitosa de Netlify y Render y comprobar el recorrido público. | URL, fecha, versión o commit y resultado verificable; una captura Building no cierra el despliegue. |
| Capítulo V, 5.2.2.8 y Student Outcome | Relacionar cada integrante con aporte, commit/PR y explicación del resultado. | Evidencia individual comprobable, sin deducir horas o reuniones del conteo de commits. |

## Cierre entre los tres

1. Completar una matriz de mejora continua en `docs/11-rubric-quality-control.md`: observación del profesor, sección, cambio, evidencia, responsable y estado real.
2. Cotejar la rúbrica y el PDF originales antes de registrar notas o ponderaciones. La rúbrica compartida muestra 14,25/20; no convertir una reevaluación propuesta en nota oficial.
3. Si la entrega exige validación con usuarios, ejecutar y documentar tareas, participantes consentidos, resultados y limitaciones. Un protocolo o prueba técnica no equivale a sesión realizada.
4. Enlazar archivos finales desde anexos: presentación, performance, exposición, About-the-Team y ZIP. Indicar duración de videos y permitir al Team Leader evaluar el desempeño real.
5. Actualizar estados del workplan después de completar la evidencia. Preparar la exposición con aportes reales de cada integrante; este requisito no se resuelve solo editando texto.
6. Revisar el PDF exportado: tablas sin cortes ilegibles, imágenes nítidas, títulos numerados y enlaces funcionales. Trabajar en las ramas Sprint 3 del informe; integrar solo con autorización del equipo.

Los 22 hallazgos de auditoría incluyen problemas técnicos además del feedback docente. El incidente de pruebas sintéticas en Render no es una observación del profesor: conservar su registro técnico, sin crear nuevas pruebas públicas ni borrar registros desde esta revisión editorial.

## Comprobación adicional contra la rúbrica compartida

La auditoría de 22 hallazgos no sustituye la rúbrica ni el PDF docente original. Antes de cerrar, el equipo debe cotejar ambos documentos. En esta revisión se dispone de la transcripción de auditoría y de las capturas de rúbrica aportadas; no se ha vuelto a leer el PDF original.

| Criterio que perdió puntos | Acción concreta y responsable propuesto | Evidencia que debe quedar |
|---|---|---|
| Sprint Backlog | Rodrigo: añadir tareas de ingeniería estimadas de 4 a 8 horas y registrar su evolución en la herramienta ágil usada por el equipo. | Tabla vinculada a historias, responsables y estados To Do, In Process, To Review y Done; capturas o historial real de movimientos. Una tabla final de Done no acredita la evolución. |
| Landing Page responsive | Eduardo: comprobar móvil y escritorio y cubrir propósito del producto, demostración con capturas o video, mensaje de valor, CTA, contacto y enlaces sociales aplicables. | Capítulo V: URL, versión, vistas responsive y explicación de las secciones. Si no existen cuentas sociales o contacto comercial, no inventarlos; resolver con el docente qué canal real corresponde. El reporte no corrige por sí solo la web. |
| Proceso colaborativo | Eduardo, con cada integrante: acreditar desarrollo, ejecución, documentación y despliegue, además del historial Git. | Matriz de aportes y enlaces verificables; identificar quién hizo y quién revisó cada actividad. |
| Mejora continua | Sebastian coordina; Rodrigo y Eduardo completan las evidencias de sus cambios. | Matriz que cierre cada observación de la entrega anterior con cambio, prueba y resultado. No limitarse a describir intenciones. |
| Comunicación oral y escrita | Los cinco integrantes: revisar el documento exportado y preparar una explicación individual del problema, aporte y resultado. | Informe y presentación coherentes, video o exposición y desempeño real de cada integrante. Las correcciones editoriales no acreditan la preparación oral. |

Configuración de desarrollo y frontend recibieron el puntaje completo en las capturas compartidas. Deben conservar ese nivel al integrar cambios: verificar convenciones, GitFlow, alcance de historias, responsive y conexión a la Fake API. Los requisitos específicos de Sprint 3 deben contrastarse con su enunciado actual; esta guía cubre las deficiencias conocidas de TB1, no certifica requisitos nuevos que no se hayan aportado.
