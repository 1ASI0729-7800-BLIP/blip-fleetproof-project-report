# Conclusiones

## Investigación y propuesta de valor

FleetProof aborda un problema reconocible: la dispersión de información documentaria y la coordinación manual de observaciones vehiculares. La investigación orienta el producto principalmente a empresas con flotas pequeñas y medianas, mientras que propietarios y compradores particulares constituyen un segmento complementario.

Las entrevistas y validaciones aportan evidencia cualitativa sobre el problema y la comprensión de la propuesta. No demuestran todavía representatividad del mercado, demanda comercial, reducción de tiempos ni disminución de sanciones. Esos beneficios permanecen como hipótesis que deben medirse mediante tareas, tiempos, errores y trazabilidad observada.

## Diseño e implementación

El frontend utiliza Angular, TypeScript y Angular Material, y está organizado en seis bounded contexts: Identity and Access Management, Subscription Management, Vehicle Information, Fleet Management, Report Management y Vehicle Monitoring, además de `shared`. La versión actual utiliza datos ficticios y JSON Server; no equivale a una integración con fuentes oficiales ni a autenticación o pagos de producción.

La arquitectura objetivo propone un monolito modular en Java y Spring Boot, organizado mediante Domain-Driven Design y persistencia relacional con Spring Data JPA. El backend definitivo se encuentra en desarrollo: la base, Swagger y los primeros contextos de Vehicle Information, Fleet Management y Report Management están disponibles en ramas independientes, pero todavía no están conectados al frontend ni desplegados como servicio de producción.

## Validación y evidencia

Las evidencias de Sprint 2 muestran pantallas, navegación, internacionalización y despliegues documentados. Sprint 3 incorpora dos sesiones moderadas con perfiles particular y empresarial. Estas sesiones ayudan a comprender expectativas sobre reportes, monitoreo, riesgo, planes y flotas, pero el moderador operó el navegador; por ello, no acreditan usabilidad autónoma ni tiempos de ejecución.

La evidencia pendiente más importante es un recorrido integral desde el registro del vehículo hasta el cierre de una observación: detección, alerta, responsable, evidencia, resolución e historial. También se requiere alinear historias, contratos HTTP, frontend, backend, OpenAPI y pruebas.

## Colaboración

El equipo utilizó ramas, commits y Pull Requests para integrar las correcciones de los capítulos I–V y los seis módulos del frontend. El historial de GitHub acredita cambios registrados, pero la cantidad de commits no sustituye la evaluación de calidad, esfuerzo, aceptación o dominio individual. Cada integrante debe poder explicar y demostrar su aporte en la exposición final.

## Recomendaciones

1. Completar la trazabilidad entre necesidad, User Story, tarea, rama, commit, Pull Request, prueba y evidencia.
2. Ejecutar pruebas autónomas con administradores de flota y medir tiempo, errores y comprensión.
3. Demostrar el recorrido completo de resolución y conservar su historial.
4. Alinear la consulta de vehículos por identificador o placa en requisitos, backend, frontend y Swagger.
5. Integrar progresivamente el backend mediante Pull Requests, resolver configuraciones compartidas y definir la estrategia definitiva de identificadores y DBMS.
6. Registrar capturas de Postman y Swagger, status HTTP, payloads y resultados de pruebas.
7. Verificar las URLs públicas antes de la entrega y distinguir construcción, publicación y funcionamiento.
8. Incorporar About-the-Team, exposición, Participant Performance Report, presentación, release y ZIP complementario.

FleetProof presenta avances técnicos y documentales verificables, pero debe continuar diferenciando claramente lo diseñado, implementado, simulado, validado y desplegado.
