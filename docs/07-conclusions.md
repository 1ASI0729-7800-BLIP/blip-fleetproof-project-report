# Conclusiones

## Investigación y propuesta de valor

FleetProof aborda un problema reconocible: la dispersión de información documentaria y la coordinación manual de observaciones vehiculares. La investigación orienta el producto principalmente a empresas con flotas pequeñas y medianas, mientras que propietarios y compradores particulares constituyen un segmento complementario.

Las entrevistas y validaciones aportan evidencia cualitativa sobre el problema y la comprensión de la propuesta. No demuestran todavía representatividad del mercado, demanda comercial, reducción de tiempos ni disminución de sanciones. Esos beneficios permanecen como hipótesis que deben medirse mediante tareas, tiempos, errores y trazabilidad observada.

## Diseño e implementación

El frontend utiliza Angular, TypeScript y Angular Material, y está organizado en seis bounded contexts: Identity and Access Management, Subscription Management, Vehicle Information, Fleet Management, Report Management y Vehicle Monitoring, además de `shared`. Durante Sprint 3 se retiró el consumo de JSON Server y se configuró la URL pública del backend; la nueva versión compiló correctamente, aunque todavía debe publicarse y recorrerse desde Netlify.

El backend se consolidó como un monolito modular en Java 21 y Spring Boot, organizado mediante Domain-Driven Design y persistencia con Spring Data JPA. La versión desplegada en Railway utiliza MySQL, publica Swagger y 15 rutas OpenAPI para los seis contextos. Las comprobaciones públicas obtuvieron HTTP 200 y CORS autorizó el dominio de Netlify. Este avance no equivale todavía a integración con fuentes vehiculares oficiales ni a autenticación y pagos de producción.

## Validación y evidencia

Las evidencias de Sprint 2 muestran pantallas, navegación, internacionalización y despliegues documentados. Sprint 3 incorpora dos sesiones moderadas con perfiles particular y empresarial. Estas sesiones ayudan a comprender expectativas sobre reportes, monitoreo, riesgo, planes y flotas, pero el moderador operó el navegador; por ello, no acreditan usabilidad autónoma ni tiempos de ejecución.

La evidencia pendiente más importante es un recorrido integral desde la versión pública de Netlify: registro, creación de flota y vehículo, reporte, detección, alerta, responsable, evidencia, resolución e historial. Los contratos HTTP, el prefijo `/api/v1`, CORS y OpenAPI ya fueron alineados; falta documentar respuestas y capturas del flujo extremo a extremo.

## Colaboración

El equipo utilizó ramas, commits y Pull Requests para integrar las correcciones de los capítulos I–V y los seis módulos del frontend. El historial de GitHub acredita cambios registrados, pero la cantidad de commits no sustituye la evaluación de calidad, esfuerzo, aceptación o dominio individual. Cada integrante debe poder explicar y demostrar su aporte en la exposición final.

## Recomendaciones

1. Completar la trazabilidad entre necesidad, User Story, tarea, rama, commit, Pull Request, prueba y evidencia.
2. Ejecutar pruebas autónomas con administradores de flota y medir tiempo, errores y comprensión.
3. Demostrar el recorrido completo de resolución y conservar su historial.
4. Alinear la consulta de vehículos por identificador o placa en requisitos, backend, frontend y Swagger.
5. Publicar en Netlify la configuración que apunta a Railway y ejecutar pruebas integrales sobre MySQL.
6. Registrar solicitudes y respuestas de Postman o Swagger, incluyendo status HTTP y payloads del recorrido completo.
7. Monitorear las URLs públicas de Netlify y Railway y conservar evidencia diferenciada de construcción, publicación y funcionamiento.
8. Incorporar About-the-Team, exposición, Participant Performance Report, presentación, release y ZIP complementario.

FleetProof presenta avances técnicos y documentales verificables, pero debe continuar diferenciando claramente lo diseñado, implementado, simulado, validado y desplegado.
