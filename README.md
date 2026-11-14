<div align="center">

<img src="https://upload.wikimedia.org/wikipedia/commons/f/fc/UPC_logo_transparente.png" alt="Universidad Peruana de Ciencias Aplicadas" width="90">

## Universidad Peruana de Ciencias Aplicadas

### Facultad de Ingeniería — Carrera de Ingeniería de Software

# Desarrollo de Aplicaciones Open Source

**Código del curso:** 1ASI0729<br>
**NRC:** 7800<br>
**Docente:** Robles Fernández, Iván<br>
**Periodo académico:** 202620

# BLIP — FleetProof

## Informe del Trabajo Final

**Última actualización:** noviembre de 2026

</div>

---

## Integrantes

| Código | Apellidos y nombres | GitHub | Responsabilidad principal documentada |
|---|---|---|---|
| U202311656 | Reyes Limo, Sebastian | `llegastian11` | Team Leader, SCM, investigación, Fleet Management, `shared` y documentación |
| U202315007 | Quintanilla Pozo, Gonzalo Samuel | `GoldQP` | Lean UX, Identity and Access Management y apoyo en integración |
| U202311464 | Gómez De La Torre, Rodrigo | `rod670` | Requirements Specification y Report Management |
| U202316049 | Morales, Jefferson | `Fenfito` | UX Research y Vehicle Monitoring |
| U202314216 | Gorbeña Vargas, Eduardo Alexander | `EduardooGV` | Product Design, Landing Page y Vehicle Information |

Las responsabilidades anteriores resumen los aportes documentados durante AV1, TB1 y Sprint 3. La autoría definitiva de cada entrega se acredita mediante commits, ramas, Pull Requests, merges y evidencias enlazadas en el Capítulo V.

## Descripción del proyecto

FleetProof es una propuesta orientada principalmente a empresas peruanas que administran flotas pequeñas y medianas. Busca centralizar información documentaria de vehículos, conservar el historial de revisiones, explicar riesgos, detectar cambios y facilitar el seguimiento de observaciones mediante responsables y evidencias.

Como segmento complementario, considera propietarios y compradores de vehículos usados que necesitan interpretar antecedentes y realizar seguimiento posterior a una consulta.

La propuesta no debe confundirse con una fuente oficial ni con una certificación vehicular. Durante la etapa académica se utilizan datos ficticios y servicios simulados. La integración con fuentes externas oficiales requiere convenios, autorización y evidencia técnica independiente.

## Alcance funcional

El diseño de dominio contempla seis bounded contexts:

| Bounded Context | Responsabilidad |
|---|---|
| Identity and Access Management | Acceso, registro, perfil y autorización de usuarios |
| Subscription Management | Planes, activación y estado de suscripciones simuladas |
| Vehicle Information | Registro y consulta de información básica de vehículos |
| Fleet Management | Organización de flotas, importación CSV y casos de resolución |
| Report Management | Reportes vehiculares, fuentes, hallazgos, riesgo y comparación histórica |
| Vehicle Monitoring | Ciclos de monitoreo, detección de cambios y alertas |

El frontend contiene actualmente los seis módulos anteriores y el módulo transversal `shared`. La existencia de una pantalla o módulo no acredita por sí sola que todos sus criterios de aceptación hayan sido validados.

## Arquitectura y tecnologías

| Producto | Tecnologías |
|---|---|
| Landing Page | HTML5, CSS3 y JavaScript |
| Frontend Web Application | Angular, TypeScript y Angular Material |
| API simulada | JSON Server con datos de demostración |
| Backend definitivo | Java 25, Spring Boot, Spring Web MVC y Spring Data JPA |
| Documentación de API | OpenAPI mediante Swagger UI |
| Persistencia objetivo | Base de datos relacional; PostgreSQL o MySQL según la configuración final |
| Arquitectura | Monolito modular organizado con Domain-Driven Design y bounded contexts |

Los diagramas de arquitectura del Capítulo IV representan el diseño objetivo. La API simulada, los conectores oficiales, pagos, notificaciones, tareas programadas y persistencia de producción deben distinguirse de las funcionalidades efectivamente implementadas y verificadas.

## Repositorios y despliegues

| Producto | Repositorio o URL | Estado documentado |
|---|---|---|
| Project Report | [blip-fleetproof-project-report](https://github.com/1ASI0729-7800-BLIP/blip-fleetproof-project-report) | Correcciones de capítulos 1–5 integradas en `develop` |
| Landing Page | [Repositorio](https://github.com/1ASI0729-7800-BLIP/blip-fleetproof-LandingPage) | Versión AV1 documentada |
| Landing Page publicada | [fleetproof-landingpage.netlify.app](https://fleetproof-landingpage.netlify.app/) | Publicación histórica documentada; verificar antes de la entrega final |
| Frontend Web Application | [blip-fleetproof-frontend](https://github.com/1ASI0729-7800-BLIP/blip-fleetproof-frontend) | Seis bounded contexts integrados en `develop` |
| Frontend publicado | [blip-fleetproof.netlify.app](https://blip-fleetproof.netlify.app/) | Publicación documentada en Netlify |
| Fake API | [blip-fleetproof-fake-api](https://github.com/1ASI0729-7800-BLIP/blip-fleetproof-fake-api) | JSON Server para demostración; no equivale al backend definitivo |
| Fake API desplegada | [fleetproof-fake-api.onrender.com](https://fleetproof-fake-api.onrender.com/) | URL documentada; disponibilidad y contratos deben verificarse antes de la entrega |
| Backend Spring Boot | [blip-fleetproof-backend](https://github.com/1ASI0729-7800-BLIP/blip-fleetproof-backend) | Base DDD y primeras ramas de bounded contexts publicadas |

## Estado por entrega

### AV1 — Sprint 1

- Perfil de la startup y solución.
- Lean UX Process y Lean UX Canvas.
- Competitive Analysis, entrevistas y Needfinding.
- Big Picture Event Storming y Ubiquitous Language.
- User Stories, Acceptance Criteria y Product Backlog inicial.
- Product Design y Landing Page v1.0.0.
- Corrección del NRC a 7800.

### TB1 — Sprint 2

- Frontend Angular organizado inicialmente por bounded contexts.
- Uso de Angular Material, internacionalización y diseño adaptable.
- API simulada mediante JSON Server.
- Evidencias locales de acceso, vehículos, reportes, monitoreo, alertas, flotas y perfil.
- Despliegues documentados en Netlify y Render.
- Historial de ramas, commits, Pull Requests y contribuciones.

Las capturas acreditan las pantallas visibles en el momento de la demostración, pero no sustituyen pruebas completas de aceptación.

### Sprint 3 — Correcciones y validación

- Capítulo I: beneficios esperados diferenciados de resultados medidos y priorización del segmento empresarial.
- Capítulo II: evidencia reorganizada por entrevista y análisis diferenciado por segmento.
- Capítulo III: criterios de aceptación ampliados y matriz inicial de trazabilidad.
- Capítulo IV: diagramas alineados con Angular, Spring Boot, Spring Data JPA y persistencia relacional. El despliegue del Sprint 3 usa MySQL.
- Capítulo V: configuración, convenciones, planificación, despliegue y colaboración revisados.
- Frontend: seis bounded contexts integrados en `develop`, incluido Subscription Management.
- Validación: dos sesiones moderadas documentadas con Cristhian Amaya y Roxana Limo.
- Backend: Spring Boot y MySQL desplegados en Railway con Swagger y OpenAPI públicos.

Las sesiones de Sprint 3 fueron demostraciones moderadas: el moderador controló la aplicación. Por ello, recogen comprensión, comentarios e intención de uso, pero no miden todavía la ejecución autónoma ni el tiempo por tarea.

## Estado actual de validación

| Aspecto | Estado | Observación |
|---|---|---|
| Segmento empresarial prioritario | Documentado | Empresas con flotas pequeñas y medianas; particulares como segmento complementario |
| Problema y propuesta de valor | Documentado | Sustentados mediante entrevistas y análisis del dominio |
| Frontend integrado | Implementado con datos simulados | Requiere cerrar la aceptación trazable de cada historia |
| Recorrido completo de resolución | Pendiente de evidencia | Debe demostrar detección, alerta, responsable, evidencia, cierre e historial |
| Pruebas autónomas de usabilidad | Pendiente | Las sesiones actuales fueron operadas por el moderador |
| Hipótesis de innovación | Formuladas | Falta medir tiempo, errores o mejora de trazabilidad frente al proceso actual |
| Fuentes oficiales | No integradas | La demostración utiliza datos ficticios y Source Fixtures |
| Backend definitivo | Desplegado en Railway | La app pública apunta a Railway. Se verificó una consulta de lectura desde Netlify. Falta documentar el recorrido completo. |
| Swagger | Público en Railway | [Swagger UI](https://blip-fleetproof-backend-production.up.railway.app/swagger-ui/index.html) |

## Pendientes antes del cierre de la siguiente entrega

1. Completar el Sprint Backlog con historias de IAM, suscripciones, flotas, casos, alertas y cierre de observaciones.
2. Vincular cada User Story con tarea, responsable, rama, commit, Pull Request, prueba y evidencia de aceptación.
3. Demostrar un recorrido completo: vehículo registrado → observación → alerta → responsable → evidencia → caso resuelto → historial.
4. Realizar al menos una prueba de usabilidad donde una persona del segmento empresarial opere la aplicación sin ayuda.
5. Alinear el contrato de consulta de vehículos por `id` o por `plate` entre requisitos, frontend, backend y Swagger.
6. Diferenciar en todos los capítulos los datos oficiales, declarados, simulados, incompletos y no disponibles.
7. Complementar las evidencias del [Student Outcome de AV1, TB1 y AV2](docs/01-student-outcome.md).
8. Incorporar capturas de Postman y Swagger, respuestas HTTP y resultados de pruebas del backend.
9. Verificar los despliegues públicos y registrar fecha, entorno y resultado observado.
10. Mantener actualizados los enlaces de los videos y archivos de entrega.
11. Preparar una release etiquetada cuando el contenido sea aprobado por el equipo.

## Tabla de contenidos

- [Registro de versiones y colaboración](docs/00-report-control.md)
- [Student Outcome](docs/01-student-outcome.md)
- [Capítulo I: Introducción](docs/02-chapter-1-introduction.md)
- [Capítulo II: Requirements Elicitation & Analysis](docs/03-chapter-2-requirements-elicitation-analysis.md)
- [Capítulo III: Requirements Specification](docs/04-chapter-3-requirements-specification.md)
- [Capítulo IV: Product Design](docs/05-chapter-4-product-design.md)
- [Capítulo V: Product Implementation, Validation & Deployment](docs/06-chapter-5-implementation-validation-deployment.md)
- [Video About the Product](https://drive.google.com/file/d/1k0bitM5iUU-4UJTjsc9pVj1xav-0AAPJ/view?usp=sharing)
- [Video About the Team](https://drive.google.com/file/d/1_nJ6RfL8EJEy9pMxYwACRxUXkV4gmNjI/view?usp=sharing)
- [Conclusiones](docs/07-conclusions.md)
- [Bibliografía](docs/08-bibliography.md)
- [Anexos](docs/09-annexes.md)

## Criterio de evidencia

Una funcionalidad se considera:

- **Diseñada:** cuando aparece en diagramas, wireframes o historias.
- **Implementada:** cuando existe código ejecutable integrado en el repositorio correspondiente.
- **Simulada:** cuando funciona con datos ficticios, JSON Server o adaptadores de demostración.
- **Validada:** cuando posee criterios de aceptación ejecutados y evidencia reproducible.
- **Desplegada:** cuando existe una URL pública verificada y una evidencia fechada de funcionamiento.

Esta clasificación evita presentar funcionalidades diseñadas o simuladas como resultados terminados o integraciones oficiales.
