# Capítulo III: Requirements Specification

## 3.1 User Stories

| Epic / Story ID | Título | Descripción | Criterios de Aceptacion | Relacionado con |
|---|---|---|---|---|
| EPIC01 | Sitio Web Estático (Landing Page) | Como negocio, deseo contar con un sitio web estático para presentar la propuesta de valor de FleetProof y captar a los segmentos objetivo. | - | - |
| US01 | Presentación de propuesta para flotas | Como visitante del segmento empresas, deseo conocer la propuesta de valor del producto para entender cómo reduce mi riesgo operativo. | Escenario 1: Carga de propuesta. Dado que un visitante del segmento empresas ingresa al sitio web,Cuando el sistema procesa la petición de la página principal,Entonces el sistema muestra el título y la descripción del servicio orientado a la gestión de flotas. | EPIC01 |
| US02 | Beneficios para usuarios particulares | Como visitante del segmento compradores particulares, deseo leer los beneficios de consultar una placa para decidir mi compra. | Escenario 1: Visualización de beneficios. Dado que un visitante navega por el sitio web,Cuando el visitante accede a la sección de particulares,Entonces el sistema despliega la información sobre prevención de multas y evaluación de riesgos vehiculares. | EPIC01 |
| EPIC02 | Generación de Vehicle Report | Como negocio, deseo que el sistema centralice la información vehicular en un reporte para reducir el trabajo manual del usuario. | - | - |
| US03 | Consulta inicial por placa | Como administrador de flota, deseo ingresar una placa vehicular para generar un reporte con sus antecedentes unificados. | Escenario 1: Generación exitosa. Dado que un administrador de flota posee una cuenta activa,Cuando el sistema recibe una solicitud de consulta con una placa válida,Entonces el sistema genera y almacena un Vehicle Report inicial.Escenario 2: Indisponibilidad de fuente. Dado que el sistema intenta realizar un Source Check,Cuando una fuente oficial externa no responde,Entonces el sistema registra un estado de Source Unavailability y conserva los demás datos obtenidos. | EPIC02 |
| US04 | Evaluación con Semáforo de Riesgo | Como supervisor de flota, deseo visualizar un semáforo de riesgo para identificar unidades vehiculares críticas rápidamente. | Escenario 1: Cálculo de riesgo.Dado que el sistema consolida un Vehicle Report,Cuando el sistema evalúa los Findings registrados,Entonces el sistema asigna un Risk Level (Alto, Medio o Bajo) al vehículo.Escenario 2: Explicación del riesgo. Dado que un supervisor consulta un reporte finalizado,Cuando el sistema despliega el Risk Level,Entonces el sistema detalla textualmente las reglas y causas que originaron dicha clasificación. | EPIC02 |
| EN01 | API Endpoint: Consulta de Vehicle Report (Technical Story) | Implementar un endpoint RESTful (método GET) que permita consultar el estado y la información de un vehículo mediante su placa, retornando los datos en formato JSON | Escenario 1: Petición exitosa. Dado que se realiza una solicitud HTTP GET al endpoint /api/v1/vehicles/{plate} con una placa válida y registrada, cuando el servicio procesa la solicitud correctamente, entonces el sistema retorna un estado HTTP 200 OK junto con la información disponible del vehículo en formato JSON. Escenario 2: Vehículo no encontrado. Dado que se realiza una solicitud HTTP GET al endpoint /api/v1/vehicles/{plate}, cuando la placa consultada no posee registros disponibles, entonces el sistema retorna un estado HTTP 404 Not Found acompañado de un mensaje de error estandarizado. | EPIC02 / US03 |
| EPIC03 | Gestión y Monitoreo de Flotas | Como negocio, deseo que los usuarios puedan registrar múltiples vehículos y comparar su historial para un monitoreo continuo. | - | - |
| US06 | Carga masiva mediante CSV | Como administrador de flota, deseo importar un archivo CSV con placas para registrar mis vehículos masivamente sin esfuerzo manual. | Escenario 1: Importación correcta. Dado que el administrador sube un archivo CSV,Cuando el sistema valida que el formato y las placas son correctos,Entonces el sistema registra los elementos como Fleet Vehicle asociados a la cuenta del usuario. | EPIC03 |
| US07 | Comparación histórica de Snapshots | Como analista documentario, deseo que el sistema compare dos estados históricos para detectar nueva información de forma inmediata. | Escenario 1: Detección de cambios. Dado que un vehículo posee más de un Snapshot guardado,Cuando el sistema ejecuta un Monitoring Cycle,Entonces el sistema compara el último estado con el anterior y resalta un Vehicle Change si existen diferencias. | EPIC03 |
| EPIC04 | Autenticación y Seguridad | Como negocio, deseo que la aplicación web cuente con flujos de autenticación seguros para garantizar que cada segmento de usuario acceda únicamente a sus paneles e información privada. | - | - |
| US08 | Autenticación de Usuario (Login) | Como usuario registrado, deseo un formulario de inicio de sesión para ingresar al panel de control de mis vehículos. | Escenario 1: Validación visual de campos. Dado que el usuario interactúa con el formulario de login, Cuando ingresa sus credenciales, Entonces la interfaz valida reactivamente el formato del correo y enmascara la contraseña. | EPIC04 |
| US09 | Interfaz interactiva de consulta por placa | Como administrador de flota, deseo un campo de búsqueda con validación en tiempo real para ingresar una placa vehicular. | Escenario 1: Estado de carga interactivo. Dado que el usuario hace clic en "Buscar", Cuando el sistema envía la petición al backend, Entonces la UI muestra un estado de carga (skeleton/spinner) bloqueando temporalmente el botón para evitar clics duplicados. | EPIC02 |
| US10 | Componente visual de Semáforo de Riesgo | Como supervisor de flota, deseo visualizar un componente gráfico interactivo en el perfil del vehículo para identificar rápidamente su nivel de riesgo. | Escenario 1: Visualización de tooltips. Dado que el componente renderiza el nivel de riesgo con los colores corporativos, Cuando el usuario pasa el cursor (hover) sobre el badge, Entonces se despliega un tooltip dinámico explicando las causas del riesgo. | EPIC02 |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

## 3.2 Impact Mapping

<img src="assets/Impact map 1.png" />

<img src="assets/Impact map 2.png" />

## 3.3 Product Backlog

| Orden | User Story ID | Título | Descripción | Story Points |
|---:|---|---|---|---:|
| 1 | US01 | Presentación de propuesta para flotas | Como visitante del segmento empresas, deseo conocer la propuesta de valor del producto para entender cómo reduce mi riesgo operativo. | 3 |
| 2 | US02 | Beneficios para usuarios particulares | Como visitante del segmento compradores particulares, deseo leer los beneficios de consultar una placa para decidir mi compra. | 2 |
| 3 | US03 | Consulta inicial por placa | Como administrador de flota, deseo ingresar una placa vehicular para generar un reporte con sus antecedentes unificados. | 5 |
| 4 | US04 | Evaluación con Semáforo de Riesgo | Como supervisor de flota, deseo visualizar un semáforo de riesgo para identificar rápidamente las unidades vehiculares críticas y priorizar su atención. | 3 |
| 5 | EN01 | API Endpoint para consulta de Vehicle Report | Implementar un endpoint RESTful para consultar la información de un vehículo mediante su placa, como habilitador técnico de la US03 “Consulta inicial por placa”. | 5 |
| 6 | US06 | Carga masiva mediante CSV | Como administrador de flota, deseo importar un archivo CSV con placas para registrar mis vehículos masivamente sin esfuerzo manual. | 8 |
| 7 | US07 | Comparación histórica de Snapshots| Como analista documentario, deseo que el sistema compare dos estados históricos para detectar nueva información de forma inmediata. | 8 |


