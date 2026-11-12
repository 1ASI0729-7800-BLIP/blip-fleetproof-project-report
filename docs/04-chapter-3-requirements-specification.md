# Capítulo III: Requirements Specification

## 3.1 User Stories

| Epic / Story ID | Título | Descripción | Criterios de Aceptacion | Relacionado con |
|---|---|---|---|---|
| EPIC01 | Sitio Web Estático (Landing Page) | Como negocio, deseo contar con un sitio web estático para presentar la propuesta de valor de FleetProof y captar a los segmentos objetivo. | - | - |
| US01 | Presentación de propuesta para flotas | Como visitante del segmento empresas, deseo conocer la propuesta de valor del producto para entender cómo reduce mi riesgo operativo. | Escenario 1: Carga de propuesta.Dado que un visitante del segmento empresas ingresa al sitio web,Cuando el sistema procesa la petición de la página principal,Entonces el sistema muestra el título y la descripción del servicio orientado a la gestión de flotas. | EPIC01 |
| US02 | Beneficios para usuarios particulares | Como visitante del segmento compradores particulares, deseo leer los beneficios de consultar una placa para decidir mi compra. | Escenario 1: Visualización de beneficios.Dado que un visitante navega por el sitio web,Cuando el visitante accede a la sección de particulares,Entonces el sistema despliega la información sobre prevención de multas y evaluación de riesgos vehiculares. | EPIC01 |
| EPIC02 | Generación de Vehicle Report | Como negocio, deseo que el sistema centralice la información vehicular en un reporte para reducir el trabajo manual del usuario. | - | - |
| US03 | Consulta inicial por placa | Como administrador de flota, deseo ingresar una placa vehicular para generar un reporte con sus antecedentes unificados. | Escenario 1: Generación exitosa.Dado que un administrador de flota posee una cuenta activa,Cuando el sistema recibe una solicitud de consulta con una placa válida,Entonces el sistema genera y almacena un Vehicle Report inicial.Escenario 2: Indisponibilidad de fuente.Dado que el sistema intenta realizar un Source Check,Cuando una fuente oficial externa no responde,Entonces el sistema registra un estado de Source Unavailability y conserva los demás datos obtenidos. | EPIC02 |
| US04 | Evaluación con Semáforo de Riesgo | Como supervisor de flota, deseo visualizar un semáforo de riesgo para identificar unidades vehiculares críticas rápidamente. | Escenario 1: Cálculo de riesgo.Dado que el sistema consolida un Vehicle Report,Cuando el sistema evalúa los Findings registrados,Entonces el sistema asigna un Risk Level (Alto, Medio o Bajo) al vehículo.Escenario 2: Explicación del riesgo.Dado que un supervisor consulta un reporte finalizado,Cuando el sistema despliega el Risk Level,Entonces el sistema detalla textualmente las reglas y causas que originaron dicha clasificación. | EPIC02 |
| US05 | API Endpoint: Consulta de Vehicle Report (Technical Story) | Como Developer, deseo disponer de un endpoint RESTful para consultar el estado de un vehículo mediante su placa para su integración. | Escenario 1: Given que el sistema externo se autentica con un token válido (`Bearer {token}`). When realiza una petición `GET` a `/api/v1/vehicles/{plate}` ingresando una placa con formato válido. Then el sistema retorna un código HTTP 200 con un JSON que contiene: `plate`, `riskLevel`, `lastSnapshotDate` y `reportUrl`. Escenario 2: **Given** que se intenta consumir el endpoint. **Then** el sistema debe retornar: **HTTP 400 (Bad Request):** Si el formato de la placa es inválido. **HTTP 401 (Unauthorized):** Si el token de autorización está ausente o expirado. **HTTP 404 (Not Found):**  Si la placa consultada no pertenece a la flota de la cuenta autenticada (previniendo fuga de datos). | EPIC02 |
| EPIC03 | Gestión y Monitoreo de Flotas | Como negocio, deseo que los usuarios puedan registrar múltiples vehículos y comparar su historial para un monitoreo continuo. | - | - |
| US06 | Carga masiva mediante CSV | Como administrador de flota, deseo importar un archivo CSV con placas para registrar mis vehículos masivamente sin esfuerzo manual. | Escenario 1: Importación correcta.Dado que el administrador sube un archivo CSV,Cuando el sistema valida que el formato y las placas son correctos,Entonces el sistema registra los elementos como Fleet Vehicle asociados a la cuenta del usuario. | EPIC03 |
| US07 | Comparación histórica de Snapshots | Como analista documentario, deseo que el sistema compare dos estados históricos para detectar nueva información de forma inmediata. | Escenario 1: Detección de cambios.Dado que un vehículo posee más de un Snapshot guardado,Cuando el sistema ejecuta un Monitoring Cycle,Entonces el sistema compara el último estado con el anterior y resalta un Vehicle Change si existen diferencias. | EPIC03 |

## 3.2 Impact Mapping

<img src="assets/Impact map 1.png" />

<img src="assets/Impact map 2.png" />

## 3.3 Product Backlog

| Orden | User Story ID | Título | Descripción | Story Points |
|---:|---|---|---|---:|
| 1 | US01 | Presentación de propuesta para flotas | Como visitante del segmento empresas, deseo conocer la propuesta de valor del producto para entender cómo reduce mi riesgo operativo. | 3 |
| 2 | US02 | Beneficios para usuarios particulares | Como visitante del segmento compradores particulares, deseo leer los beneficios de consultar una placa para decidir mi compra. | 2 |
| 3 | US03 | Consulta inicial por placa | Como administrador de flota, deseo ingresar una placa vehicular para generar un reporte con sus antecedentes unificados. | 5 |
| 4 | US04 | Evaluación con Semáforo de Riesgo | Como supervisor de flota, deseo visualizar un semáforo de riesgo para identificar unidades vehiculares críticas rápidamente. | 3 |
| 5 | US05 | Como Developer, deseo disponer de un endpoint RESTful para consultar el estado de un vehículo mediante su placa (no UUID interno) para su integración con sistemas externos. | 5 |
| 6 | US06 | Carga masiva mediante CSV | Como administrador de flota, deseo importar un archivo CSV con placas para registrar mis vehículos masivamente sin esfuerzo manual. | 3 |
| 7 | US07 | Comparación histórica de Snapshots| Como analista documentario, deseo que el sistema compare dos estados históricos para detectar nueva información de forma inmediata. | 8 |


## 3.4 Trazabilidad de Requerimientos

| Hallazgo / Entrevista                                                         | Necesidad                                                    | Requisito                           | US   | Criterio de Aceptación                                                    | Prueba (BDD / Técnica)                                                                       |
|-------------------------------------------------------------------------------|--------------------------------------------------------------|-------------------------------------|------|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| **Roxana Limo (E4):** Información distribuida retrasa toma de decisiones.         | Centralizar consultas vehiculares desde una única vista.     | Consulta inicial por placa.         | **US03** | Genera y almacena un Vehicle Report inicial si la placa es válida.        | **Given** admin con cuenta, **When** consulta placa válida, **Then** sistema genera el reporte.          |
| **Cristhian Amaya (E1):** Dificultad para interpretar datos técnicos registrales. | Resumen visual explicable del riesgo encontrado.             | Semáforo determinístico de riesgo.  | **US04** | Asigna un Risk Level (Alto/Medio/Bajo) y detalla textualmente las causas. | **Given** reporte consolidado, **When** sistema evalúa Findings, **Then** clasifica y explica el riesgo. |
| **Arquitectura (Technical Story):** Sistemas B2B requieren interoperar.           | Consultar reportes desde sistemas externos (ERP/Logística).  | API Endpoint de consulta.           | **US05** | Retorna Status 200 y JSON del vehículo al consultar por placa.            | **Given** API endpoint disponible, **When** se realiza solicitud GET, **Then** se retorna HTTP 200 con datos del vehículo.              |
| **Jorge Quispe (E6):** Revisar flota uno por uno exige mucho esfuerzo.            | Registrar múltiples vehículos simultáneamente.               | Carga masiva mediante CSV.          | **US06** | Importa archivo CSV, valida formato y registra Fleet Vehicles.            | **Given** CSV válido, **When** administrador importa archivo, **Then** sistema registra los vehículos.   |
| **Mei Lin Tanaka (E7):** Necesidad de detectar qué documentos vencen o cambian.   | Comparar estados históricos para detectar información nueva. | Comparación histórica de Snapshots. | **US07** | Compara el último estado con el anterior y resalta el "Vehicle Change".   | **Given** 2 snapshots, **When** ejecuta Monitoring Cycle, **Then** resalta diferencias.                  |
