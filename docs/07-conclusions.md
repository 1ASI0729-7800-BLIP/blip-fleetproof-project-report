# Conclusiones

## Conclusiones y recomendaciones

Durante el desarrollo de este primer avance (AV1), el equipo de BLIP logró consolidar las bases estratégicas y técnicas del proyecto FleetProof. Las principales conclusiones, alineadas a nuestro proceso de investigación, son las siguientes:

* **Sobre el Problema:** Se validó que la dispersión de información y la falta de trazabilidad en los historiales vehiculares peruanos representan un dolor real (pain point) crítico. Esta deficiencia genera ineficiencias operativas y riesgo de multas, afectando tanto a empresas que gestionan flotas (B2B) como a particulares (B2C).
* **Assumptions & Hypothesis Statements:** Mediante el marco de trabajo Lean UX, establecimos nuestras asunciones de negocio y usuario. Nuestra hipótesis principal concluye que, al proporcionar un ecosistema digital unificado con alertas automatizadas y semáforos de estado, reduciremos significativamente la carga administrativa y el tiempo de investigación para nuestros usuarios.
* **Criterios de éxito:** El despliegue exitoso de la Landing Page en Netlify marca el cumplimiento de nuestro primer gran hito técnico. El interés generado y la validación inicial mediante entrevistas confirman la viabilidad del proyecto.

**Recomendaciones:**
Para los siguientes sprints, se recomienda mantener un ciclo de validación continuo con usuarios reales para ajustar el *Product Backlog* según el feedback obtenido. Desde el punto de vista técnico, se plantea estructurar la base de datos relacional y desarrollar los endpoints del backend definitivo con Spring Boot y Java, documentados mediante OpenAPI/Swagger, de acuerdo con el stack oficial del curso.

## Conclusiones de TB1 — Sprint 2

* **Frontend:** FleetProof cuenta con una primera versión en Angular organizada en cinco bounded contexts. La reutilización de `shared` mantiene contratos HTTP, controles y presentación comunes.
* **Ejecución:** Se verificaron acceso demo, navegación, apertura del diálogo CSV y cambio ES/EN. Las capturas documentan dashboard, vehículos, reportes, comparación, monitoreo, alertas, perfil y móvil. No prueban por sí solas todos los criterios de aceptación ni importación CSV o exportación PDF completadas.
* **Publicación:** Netlify muestra el frontend publicado. Render muestra la configuración de la Fake API en construcción; falta acreditar su publicación y la conexión pública.
* **Colaboración:** GitHub muestra aportes de los cinco integrantes. El capítulo V se integró en `develop`, conservando el historial. El número de commits no sustituye la revisión de calidad ni aceptación de historias.
* **Validación:** Los datos y la API son de demostración. Esta entrega no acredita fuentes oficiales, autenticación de producción ni reducciones medidas del tiempo de consulta. Estas hipótesis requieren validación posterior con usuarios.

**Recomendaciones:** completar pruebas de registro, edición, generación y exportación PDF, CSV, monitoreo y resolución de casos; registrar solicitudes y respuestas en Postman; revisar el runtime de Render; optimizar el logo y cerrar la trazabilidad entre historias, pruebas y evidencias. El backend definitivo debe seguir el stack oficial del curso documentado en el control de rúbrica; JSON Server no constituye un backend de producción.

---
## Video About-the-Team

**Pendiente:** incorporar resumen, pauta de secuencias, captura, URL y duración del video About-the-Team.
