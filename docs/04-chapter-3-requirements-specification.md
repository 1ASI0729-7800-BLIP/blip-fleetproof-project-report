# Capítulo III: Requirements Specification

## 3.1 User Stories

| Epic / Story ID | Título | Descripción | Criterios de aceptación | Relacionado con |
|---|---|---|---|---|
| EPIC01 | Sitio Web Estático (Landing Page) | Como negocio, deseo contar con un sitio web estático para presentar la propuesta de valor de FleetProof y captar a los segmentos objetivo. | - | - |
| US01 | Presentación de propuesta para flotas | Como visitante del segmento empresas, deseo conocer la propuesta de valor del producto para entender cómo reduce mi riesgo operativo. | Escenario 1: Carga de propuesta.<br>Dado que un visitante del segmento empresas ingresa al sitio web,<br>Cuando el sistema procesa la petición de la página principal,<br>Entonces el sistema muestra el título y la descripción del servicio orientado a la gestión de flotas. | EPIC01 |
| US02 | Beneficios para usuarios particulares | Como visitante del segmento compradores particulares, deseo leer los beneficios de consultar una placa para decidir mi compra. | Escenario 1: Visualización de beneficios.<br>Dado que un visitante navega por el sitio web,<br>Cuando el visitante accede a la sección de particulares,<br>Entonces el sistema despliega la información sobre prevención de multas y evaluación de riesgos vehiculares. | EPIC01 |
| EPIC02 | Generación de Vehicle Report | Como negocio, deseo que el sistema centralice la información vehicular en un reporte para reducir el trabajo manual del usuario. | - | - |
| US03 | Consulta inicial por placa | Como administrador de flota, deseo ingresar una placa vehicular para generar un reporte con sus antecedentes unificados. | Escenario 1: Generación exitosa.<br>Dado que un administrador de flota posee una cuenta activa,<br>Cuando el sistema recibe una solicitud de consulta con una placa válida,<br>Entonces el sistema genera y almacena un Vehicle Report inicial.<br>Escenario 2: Indisponibilidad de fuente.<br>Dado que el sistema intenta realizar un Source Check,<br>Cuando una fuente oficial externa no responde,<br>Entonces el sistema registra un estado de Source Unavailability y conserva los demás datos obtenidos. | EPIC02 |
| US04 | Evaluación con Semáforo de Riesgo | Como supervisor de flota, deseo visualizar un semáforo de riesgo para identificar unidades vehiculares críticas rápidamente. | Escenario 1: Cálculo de riesgo.<br>Dado que el sistema consolida un Vehicle Report,<br>Cuando el sistema evalúa los Findings registrados,<br>Entonces el sistema asigna un Risk Level (Alto, Medio o Bajo) al vehículo.<br>Escenario 2: Explicación del riesgo.<br>Dado que un supervisor consulta un reporte finalizado,<br>Cuando el sistema despliega el Risk Level,<br>Entonces el sistema detalla textualmente las reglas y causas que originaron dicha clasificación. | EPIC02 |
| US05 | API Endpoint: Consulta de Vehicle Report (Technical Story) | Como Developer, deseo disponer de un endpoint RESTful para consultar el estado de un vehículo mediante su placa para su integración. | Escenario 1: Petición válida.<br>Dado que el cliente realiza un HTTP GET request a /api/v1/vehicles/{plate},<br>Cuando la placa existe en la base de datos,<br>Entonces el sistema retorna un HTTP Status 200 OK con el payload en formato JSON del vehículo.<br>Escenario 2: Vehículo no encontrado.<br>Dado que el cliente realiza un HTTP GET request a /api/v1/vehicles/{plate},<br>Cuando la placa no tiene registros previos,<br>Entonces el sistema retorna un HTTP Status 404 Not Found con un mensaje de error estandarizado. | EPIC02 |
| EPIC03 | Gestión y Monitoreo de Flotas | Como negocio, deseo que los usuarios puedan registrar múltiples vehículos y comparar su historial para un monitoreo continuo. | - | - |
| US06 | Carga masiva mediante CSV | Como administrador de flota, deseo importar un archivo CSV con placas para registrar mis vehículos masivamente sin esfuerzo manual. | Escenario 1: Importación correcta.<br>Dado que el administrador sube un archivo CSV,<br>Cuando el sistema valida que el formato y las placas son correctos,<br>Entonces el sistema registra los elementos como Fleet Vehicle asociados a la cuenta del usuario. | EPIC03 |
| US07 | Comparación histórica de Snapshots | Como analista documentario, deseo que el sistema compare dos estados históricos para detectar nueva información de forma inmediata. | Escenario 1: Detección de cambios.<br>Dado que un vehículo posee más de un Snapshot guardado,<br>Cuando el sistema ejecuta un Monitoring Cycle,<br>Entonces el sistema compara el último estado con el anterior y resalta un Vehicle Change si existen diferencias. | EPIC03 |

## 3.2 Impact Mapping

<img src="assets/Impact map 1.png" alt="Impact Map de FleetProof: objetivos, actores e impactos" />

<img src="assets/Impact map 2.png" alt="Continuación del Impact Map de FleetProof" />

## 3.3 Product Backlog

| Orden | User Story ID | Título | Descripción | Story Points |
|---:|---|---|---|---:|
| 1 | US01 | Presentación de propuesta para flotas | Como visitante del segmento empresas, deseo conocer la propuesta de valor del producto para entender cómo reduce mi riesgo operativo. | 3 |
| 2 | US02 | Beneficios para usuarios particulares | Como visitante del segmento compradores particulares, deseo leer los beneficios de consultar una placa para decidir mi compra. | 2 |
| 3 | US03 | Consulta inicial por placa | Como administrador de flota, deseo ingresar una placa vehicular para generar un reporte con sus antecedentes unificados. | 5 |
| 4 | US05 | API Endpoint: Consulta de Vehicle Report | Como Developer, deseo disponer de un endpoint RESTful para consultar el estado de un vehículo mediante su placa para su integración. | 3 |
| 5 | US04 | Evaluación con Semáforo de Riesgo | Como supervisor de flota, deseo visualizar un semáforo de riesgo para identificar unidades vehiculares críticas rápidamente. | 5 |
| 6 | US06 | Carga masiva mediante CSV | Como administrador de flota, deseo importar un archivo CSV con placas para registrar mis vehículos masivamente sin esfuerzo manual. | 8 |
| 7 | US07 | Comparación histórica de Snapshots | Como analista documentario, deseo que el sistema compare dos estados históricos para detectar nueva información de forma inmediata. | 8 |


