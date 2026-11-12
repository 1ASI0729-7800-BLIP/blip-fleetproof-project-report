# Capítulo III: Requirements Specification

## 3.1 User Stories

| ID | Título | User Story | Acceptance Criteria principales | Relación |
|---|---|---|---|---|
| EPIC01 | Landing Page | Como negocio, deseo presentar la propuesta de FleetProof para comunicar su valor a los segmentos objetivo. | - | - |
| US01 | Presentación para flotas | Como visitante empresarial, deseo conocer la propuesta para entender cómo apoya el control documentario de flotas. | Dado que visita la Landing Page, cuando revisa la propuesta, entonces identifica el segmento, problema y beneficio esperado sin confundirlo con una fuente oficial. | EPIC01 |
| US02 | Beneficios para particulares | Como comprador o propietario, deseo comprender los beneficios de una consulta para evaluar si responde a mi necesidad. | Dado que navega por la Landing Page, cuando revisa la sección correspondiente, entonces distingue consulta puntual y seguimiento posterior. | EPIC01 |
| EPIC02 | Vehicle Report | Como negocio, deseo consolidar información vehicular en reportes trazables. | - | - |
| US03 | Consulta inicial por placa | Como administrador de flota, deseo ingresar una placa para generar un reporte con antecedentes unificados. | Si la placa es válida, genera un Vehicle Report inicial. Si una fuente simulada no responde, registra `Source Unavailability`, conserva los demás resultados y no interpreta la ausencia como falta de antecedentes. | EPIC02 |
| US04 | Semáforo explicable | Como supervisor, deseo visualizar el nivel de riesgo y sus causas para priorizar vehículos. | Evalúa Findings mediante reglas conocidas, asigna un nivel y muestra una explicación textual. El resultado no se presenta como certificación oficial. | EPIC02 |
| US05 | Consulta REST de vehículo | Como desarrollador, deseo consultar un vehículo mediante el contrato implementado para integrarlo con otros módulos. | `GET /api/v1/vehicles/{id}` retorna HTTP 200 y el recurso cuando existe, o HTTP 404 con error estandarizado cuando no existe. La consulta directa por placa queda como evolución pendiente hasta alinear frontend, backend y Swagger. | EPIC02 |
| EPIC03 | Fleet and Vehicle Monitoring | Como negocio, deseo registrar varios vehículos y comparar sus estados para ofrecer seguimiento continuo. | - | - |
| US06 | Importación CSV | Como administrador, deseo importar vehículos mediante CSV para evitar registrarlos individualmente. | Valida encabezados, formato, placas y duplicados; informa filas rechazadas y registra únicamente los elementos válidos confirmados por el usuario. | EPIC03 |
| US07 | Comparación histórica | Como analista, deseo comparar snapshots para detectar nueva información. | Cuando existen dos estados comparables, identifica diferencias por fuente; si una fuente no está disponible, comunica la limitación sin producir una conclusión falsa. | EPIC03 |
| EPIC04 | Identity and Access Management | Como negocio, deseo identificar usuarios para proteger sus vehículos, reportes y flotas. | - | - |
| US08 | Acceso y perfil | Como usuario, deseo registrarme, iniciar sesión y actualizar mi perfil. | Con credenciales válidas de demostración accede al workspace; al actualizar datos válidos, la aplicación conserva y muestra los cambios. La autenticación actual no se declara como seguridad de producción. | EPIC04 |
| EPIC05 | Subscription Management | Como negocio, deseo ofrecer planes con límites y estados comprensibles. | - | - |
| US09 | Activación simulada | Como usuario, deseo seleccionar un plan para conocer el estado y alcance del monitoreo. | Al confirmar la activación simulada, muestra plan y estado activo e indica que no constituye un pago real. | EPIC05 |
| EPIC06 | Fleet and Resolution Management | Como administrador, deseo organizar vehículos y atender observaciones con responsables y evidencia. | - | - |
| US10 | Crear una flota | Como administrador, deseo crear una flota y asociar vehículos para organizar el seguimiento. | Con un nombre válido registra la agrupación y permite consultar los vehículos asociados. | EPIC06 |
| US11 | Generar alertas | Como supervisor, deseo recibir una alerta cuando aparece un cambio relevante. | Cuando un cambio cumple una regla, registra vehículo, reporte, tipo, fecha, estado y explicación. | EPIC06 |
| US12 | Resolver con evidencia | Como responsable, deseo actualizar un caso y adjuntar evidencia para demostrar la atención de una observación. | Conserva responsable, estado, notas e historial; no permite cerrar el caso sin evidencia. | EPIC06 |

## 3.2 Impact Mapping

![Impact Map de FleetProof: objetivos, actores e impactos](<assets/Impact map 1.png>)

![Continuación del Impact Map de FleetProof](<assets/Impact map 2.png>)

Los Impact Maps relacionan el objetivo de reducir la dispersión de información con actores empresariales y particulares. La prioridad inicial corresponde a empresas con flotas pequeñas y medianas; los particulares se mantienen como segmento complementario.

## 3.3 Product Backlog

| Orden | ID | Título | Story Points | Estado documentado |
|---:|---|---|---:|---|
| 1 | US01 | Presentación para flotas | 3 | Implementado históricamente en Landing Page; verificar publicación actual |
| 2 | US02 | Beneficios para particulares | 2 | Implementado históricamente en Landing Page; verificar publicación actual |
| 3 | US08 | Acceso y perfil | 5 | Implementado con datos de demostración; aceptación completa pendiente |
| 4 | US03 | Consulta inicial por placa | 5 | Demostrada con Source Fixtures; fuentes oficiales no integradas |
| 5 | US04 | Semáforo explicable | 5 | Visible en reportes; reglas y pruebas requieren trazabilidad final |
| 6 | US10 | Crear una flota | 5 | Demostrado en sesión moderada; asignación autónoma pendiente |
| 7 | US06 | Importación CSV | 8 | Implementado en frontend; prueba de aceptación pendiente |
| 8 | US07 | Comparación histórica | 8 | Implementado con datos simulados; ciclo completo pendiente |
| 9 | US11 | Generar alertas | 5 | Vista implementada; generación resultante debe demostrarse |
| 10 | US12 | Resolver con evidencia | 8 | Caso implementado parcialmente; recorrido completo pendiente |
| 11 | US09 | Activación simulada | 5 | Demostrada como simulación; pago real fuera del alcance actual |
| 12 | US05 | Consulta REST de vehículo | 5 | Implementada inicialmente en rama del backend; integración pendiente |

Los Story Points representan estimación relativa, no horas ejecutadas ni aceptación. El estado se actualiza únicamente con evidencia verificable.

## 3.4 Trazabilidad de requisitos

| Evidencia de necesidad | Necesidad | US | Prueba esperada | Estado actual |
|---|---|---|---|---|
| Roxana Limo (E4) trabaja con información distribuida entre áreas y sedes. | Centralizar vehículos, riesgo y responsables. | US03, US04, US10 | Crear flota, asociar vehículo, consultar reporte y explicar riesgo. | Creación de flota y reporte mostrados en sesión moderada; asociación autónoma pendiente. |
| Cristhian Amaya (E1 y validación Sprint 3) consulta varias fuentes y pregunta por cambios posteriores. | Diferenciar reporte puntual y monitoreo. | US03, US07, US11 | Generar reporte, crear segundo snapshot y comprobar alerta explicable. | Reporte mostrado; ciclo posterior y alerta resultante pendientes. |
| Patricia Valdez (E5) coordina observaciones mediante mensajería. | Asignar responsables y conservar evidencia de cierre. | US12 | Abrir caso, asignar responsable, adjuntar evidencia, resolver y revisar historial. | Flujo completo pendiente de evidencia. |
| Jorge Quispe (E6) revisa vehículos uno por uno. | Reducir registro manual repetitivo. | US06 | Importar CSV válido, informar errores y confirmar registros creados. | Implementación disponible; aceptación reproducible pendiente. |
| Mei Lin Tanaka (E7) necesita detectar documentos vencidos o modificados. | Comparar estados y comunicar cambios. | US07, US11 | Comparar snapshots y registrar alerta con fecha y fuente. | Implementado con datos simulados; prueba integral pendiente. |
| Arquitectura de integración | Consultar recursos mediante API documentada. | US05 | Ejecutar petición desde Postman/Swagger y registrar status y payload. | Endpoint inicial disponible en ramas del backend; capturas pendientes. |

Cada historia debe vincularse en el Sprint Backlog con tarea, responsable, rama, commit, Pull Request, resultado de prueba y evidencia. Un escenario redactado no equivale a una prueba aprobada.
