# Capítulo V: Product Implementation, Validation & Deployment

## 5.1 Software Configuration Management

### 5.1.1 Software Development Environment Configuration

En esta sección se describen las herramientas de software seleccionadas para dar soporte a las distintas fases del ciclo de vida del producto digital. Se incluyen sus nombres, objetivos específicos dentro del proyecto y los enlaces de acceso o descarga, diferenciando entre soluciones SaaS y aplicaciones instalables.
* **Gestión de Proyectos y Tareas**

| Herramienta | Uso principal | Enlace / Ruta de Acceso |
|---|---|---|
| **Jira Software** | Organización de tareas y entregables mediante tableros ágiles, tanto a nivel individual como por módulo. | [https://jira.atlassian.com](https://jira.atlassian.com) |
| **GitHub Projects** | Seguimiento de proyectos con enfoque en historias de usuario, issues y Pull Requests en repositorios. | [https://github.com/features/issues](https://github.com/features/issues) |

* **Diseño de Experiencia y UI/UX**

| Herramienta | Uso principal | Enlace / Ruta de Acceso |
|---|---|---|
| **Figma** | Diseño colaborativo de wireframes, mockups y prototipos navegables para la aplicación y Landing Page. | [https://figma.com](https://figma.com) |
| **Miro** | Elaboración de user flows, wireflows, Big Picture Event Storming y mapas de arquitectura. | [https://miro.com](https://miro.com) |
| **UXPressia** | Creación de User Personas, Empathy Maps, Journey Maps e Impact Maps. | [https://uxpressia.com](https://uxpressia.com) |

* **Desarrollo de Software**

| Herramienta / Tecnología | Uso principal | Enlace / Ruta de Descarga |
|---|---|---|
| **Visual Studio Code** | Entorno de desarrollo ligero para la edición del Landing Page con HTML5, CSS3 y JavaScript. | [https://code.visualstudio.com](https://code.visualstudio.com) |
| **WebStorm** | IDE principal para el desarrollo del Frontend SPA utilizando Vue 3 y TypeScript. | [https://www.jetbrains.com/webstorm/](https://www.jetbrains.com/webstorm/) |
| **Rider / Visual Studio** | Entorno de desarrollo integrado para la construcción del Backend API con ASP.NET Core y C#. | [https://www.jetbrains.com/rider/](https://www.jetbrains.com/rider/) |
| **HTML5** | Lenguaje de marcado para estructurar el contenido de la Landing Page. | [https://developer.mozilla.org/es/docs/Web/HTML](https://developer.mozilla.org/es/docs/Web/HTML) |
| **CSS3** | Lenguaje de estilos para definir la apariencia visual y responsiva de la Landing Page. | [https://developer.mozilla.org/es/docs/Web/CSS](https://developer.mozilla.org/es/docs/Web/CSS) |
| **Vue 3** | Framework progresivo de JavaScript para construir interfaces de usuario reactivas en la Web Application. | [https://vuejs.org](https://vuejs.org) |

* **Diseño de Arquitectura de Software**

| Herramienta | Uso principal | Enlace / Ruta de Acceso |
|---|---|---|
| **Mermaid** | Modelado de arquitectura mediante Diagramas como Código (Contexto, Contenedores C3, Clases y Base de datos). | [https://mermaid.js.org](https://mermaid.js.org) |

* **Despliegue de Software**

| Herramienta / Plataforma | Uso principal | Enlace / Ruta de Acceso |
|---|---|---|
| **Netlify** | Despliegue automático y gratuito de la Landing Page estática y el Frontend SPA. | [https://www.netlify.com](https://www.netlify.com) |
| **Render / Azure** | Despliegue en la nube del Backend API (ASP.NET Core) y alojamiento de la base de datos PostgreSQL. | [https://render.com](https://render.com) |

* **Documentación de Software**

| Herramienta / Recurso | Uso principal | Enlace / Ruta de Acceso |
|---|---|---|
| **Markdown** | Edición y mantenimiento de los archivos `.md` asociados a la documentación del proyecto. | [https://www.markdownguide.org](https://www.markdownguide.org) |
| **GitHub** | Repositorio con control de versiones, utilizado además como espacio de documentación en issues y PRs. | [https://github.com](https://github.com) |
| **Git** | Sistema distribuido de control de versiones para la gestión del código fuente. | [https://git-scm.com](https://git-scm.com) |
| **GitFlow Workflow** | Modelo de ramificación para mantener el código y la documentación organizados. | [https://nvie.com/posts/a-successful-git-branching-model](https://nvie.com/posts/a-successful-git-branching-model) |
| **Conventional Commits** | Convención de mensajes de commit para mejorar la trazabilidad y facilitar la generación de changelogs. | [https://www.conventionalcommits.org](https://www.conventionalcommits.org) |
### 5.1.2 Source Code Management
El equipo empleará GitHub como repositorio de alojamiento y Git como sistema de control de versiones para todos los entregables del proyecto FleetProof. Se aplicará la estrategia de ramificación GitFlow Workflow, con el uso de Semantic Versioning y mensajes estructurados bajo la convención de Conventional Commits.

**Repositorios del Proyecto**

| Producto | Repositorio GitHub |
|---|---|
| **Organización BLIP** | [https://github.com/1ASI0729-8088-BLIP](https://github.com/1ASI0729-8088-BLIP) |
| **Landing Page** | [https://github.com/1ASI0729-8088-BLIP/blip-fleetproof-LandingPage](https://github.com/1ASI0729-8088-BLIP/blip-fleetproof-LandingPage) |
| **Project Report** | [https://github.com/1ASI0729-8088-BLIP/blip-fleetproof-project-report](https://github.com/1ASI0729-8088-BLIP/blip-fleetproof-project-report) |
| **Frontend Web App** | [https://github.com/1ASI0729-8088-BLIP/blip-fleetproof-frontend](https://github.com/1ASI0729-8088-BLIP/blip-fleetproof-frontend) |
| **Backend API** | [https://github.com/1ASI0729-8088-BLIP/blip-fleetproof-backend](https://github.com/1ASI0729-8088-BLIP/blip-fleetproof-backend) |

**Modelo GitFlow**

Se seguirá el enfoque planteado por Vincent Driessen, el cual define dos ramas principales:
* `main`: contiene las versiones estables listas para producción.
* `develop`: integra nuevas funcionalidades antes de pasar al entorno de producción.

| Tipo de rama | Uso principal | Convención de nombres | Ejemplo |
|---|---|---|---|
| **feature** | Desarrollo de funcionalidades nuevas. | `feature/<nombre-descriptivo>` | `feature/sprint1-landing` |
| **release** | Preparación de una versión previa al despliegue. | `release/vX.Y.Z` | `release/v1.0.0` |
| **hotfix** | Corrección rápida de errores en producción. | `hotfix/<problema>` | `hotfix/fix-mobile-menu` |

**Versionado Semántico**

Se implementará el esquema Semantic Versioning 2.0.0, con el formato:

**MAJOR.MINOR.PATCH**
* **MAJOR:** cambios incompatibles con versiones anteriores.
* **MINOR:** incorporación de nuevas funciones compatibles.
* **PATCH:** corrección de errores o mejoras menores.

**Conventional Commits**

Los mensajes de commit seguirán el estándar Conventional Commits para asegurar trazabilidad y generar changelogs automáticos.

Formato general: `(opcional-scope): descripción breve`

Tipos de commit definidos:
* `feat`: nueva funcionalidad
* `fix`: corrección de errores
* `docs`: cambios en documentación
* `style`: ajustes de formato (espacios, comas, etc.) sin afectar lógica
* `refactor`: modificaciones de código sin impacto en funciones o errores
* `test`: adición o modificación de pruebas
* `chore`: tareas de mantenimiento o generales

### 5.1.3 Source Code Style Guide & Coding Conventions

Con el objetivo de mantener un código ordenado, consistente y fácil de mantener entre todos los miembros del equipo, se han definido las siguientes convenciones. Todas las variables, funciones, clases, archivos y elementos estarán en inglés.

* Se utilizará inglés como idioma único para nombres de variables, funciones, clases, comentarios y documentación técnica.
* Se evitarán abreviaciones innecesarias y nombres genéricos como `data1`, `temp`, `info`, etc.

**HTML**
Atributos en minúsculas y nombres de clase con `kebab-case` (`section-title`, `hero-grid`).
* Estructura semántica clara: uso de etiquetas como `<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`.
* Sangría con 4 espacios.
* Atributos ordenados de manera lógica: `id`, `class`, `type`, `name`, `placeholder`, `value`, `required`, etc.

**CSS**
* Para clases personalizadas: usar `kebab-case`.
* Se agruparán variables globales en la seccion `:root` (paleta de colores y espaciado).

**Google TypeScript Style Guide**
Basado en el Google TypeScript Style Guide, se adoptan las siguientes reglas para mantener un código limpio y coherente en el desarrollo de la Web Application (Vue 3):

Nombres y sintaxis:
* `camelCase` para variables, funciones y parámetros.
* `PascalCase` para clases, interfaces, enums y tipos.
* Constantes con `UPPER_CASE_WITH_UNDERSCORES` si son globales.

Módulos y imports:
* Preferir imports explícitos y ordenados: primero bibliotecas externas, luego internas.
* Evitar `default exports`, usar siempre `export const` o `export class`.

Tipado y declaraciones:
* Siempre tipar explícitamente los parámetros y valores de retorno de funciones.
* Evitar `any` excepto cuando sea estrictamente necesario.
* Usar `readonly` para propiedades que no deben cambiarse.
* Interfaces en lugar de `type` cuando sea posible.

Buenas prácticas:
* Preferir `const` sobre `let`, y evitar `var`.
* Evitar usar `this` fuera de clases.
* No mezclar funciones y lógica en componentes — delegar a servicios.

**Vue 3 Style Guide**
Seguiremos las prácticas recomendadas por la documentación oficial de Vue 3:

Componentes:
* Nombres en `PascalCase` y con sufijo `Component` (ej. `VehicleReportComponent.vue`).
* Evitar lógica compleja en los templates: delegar a métodos o *composables* (Composition API).
* Uso de `<script setup>` para mayor legibilidad y rendimiento.

**C# y ASP.NET Core Conventions**
Para el desarrollo del Backend RESTful API:
* Nombres de Clases, Métodos e Interfaces (con prefijo `I`) en `PascalCase`.
* Variables locales y parámetros en `camelCase`.
* Estructura de carpetas basada en el diseño de Bounded Contexts y Domain-Driven Design (DDD).

**Pruebas / Gherkin**
En caso de usar Gherkin (para especificaciones o pruebas de los escenarios descritos en las User Stories):
* Usaremos el formato estandarizado `Given`, `When` y `Then`.

### 5.1.4 Software Deployment Configuration

1. **Ingresar a Netlify**<br>
   Accedemos a la plataforma mediante nuestras credenciales de Github en "Log in with GitHub".
   <img src="https://res.cloudinary.com/dehoql1oc/image/upload/v1789627588/Captura_de_pantalla_2026-09-17_013830_jsr61y.png" alt="inicio" width="800">

2. **Autorizar a Netlify** <br>
   Damos permisos a Netlify de acceder a nuestra cuenta de GitHub para luego ir a la sección "Sites" y presionar "Add new site". Entonces, le damos a "Import an existing project".
   <img src="https://res.cloudinary.com/dehoql1oc/image/upload/v1789628043/Captura_de_pantalla_2026-09-17_015348_kblafi.png" alt="inicio" width="800">

3. **Escoger tu deploy** <br>
   En la parte de "Let's deploy your project with..." seleccionamos GitHub.
   <img src="https://res.cloudinary.com/dehoql1oc/image/upload/v1789628214/Captura_de_pantalla_2026-09-17_015637_q2g9g8.png" alt="inicio" width="800">

4. **Escoger tu repositorio** <br>
   Dado que nuestro repositorio está bajo una organización, la seleccionamos.
   <img src="https://res.cloudinary.com/dehoql1oc/image/upload/v1789628431/Captura_de_pantalla_2026-09-17_020020_uspnlf.png" alt="inicio" width="800">

5. **Configurar el despliegue** <br>
   Ahora procedemos a configurar el despliegue, colocando el Site Name y seleccionando el Team, también debemos escoger una rama que en este caso será la Main.
   <img src="https://res.cloudinary.com/dehoql1oc/image/upload/v1789628547/Captura_de_pantalla_2026-09-17_020208_tqyiqu.png" alt="inicio" width="800">

6. **Seguir configurando** <br>
   Seguimos configurando, pero esta vez seleccionando el "Publish directory" colocamos public, para finalmente darle a "Deploy demy-academy".
   <img src="https://res.cloudinary.com/dehoql1oc/image/upload/v1789628631/Captura_de_pantalla_2026-09-17_020333_kaqg4d.png" alt="inicio" width="800">

7. **Despliegue listo** <br>
   Ahora podemos observar que el deploy está listo y podremos ver el enlace de la web a la landing page recién desplegada.
   <img src="https://res.cloudinary.com/dehoql1oc/image/upload/v1789628688/Captura_de_pantalla_2026-09-17_020436_pvq8li.png" alt="inicio" width="800">

Ahora con la Landing Page desplegada, cada vez que se realize un push en la rama correspondiente, se actualizara automáticamente, de esta manera evitamos repetir los pasos. <br>
[Link de la Landing Page](https://fleetproof-landingpage.netlify.app/)

## 5.2 Landing Page, Services & Applications Implementation

### 5.2.1 Sprint 1

#### 5.2.1.1 Sprint Planning 1

| Sprint # | Sprint 1 |
|---|---|
| **Sprint planning background** | |
| Date | 2026/09/16 |
| Time | 5:00 PM |
| Location | Llamada grupal en la plataforma Discord |
| Prepared By | Sebastian Reyes Limo |
| Attendees (to planning meeting) | Sebastian Reyes Limo, Gonzalo Quintanilla, Jefferson Morales, Rodrigo Gómez De La Torre y Eduardo Gorbeña |
| **Sprint Goal & User Stories** | |
| Sprint 1 Goal | Nuestro enfoque está en presentar una landing page que muestre todas las funcionalidades y características de FleetProof a los visitantes.<br>Creemos que esto generará una sólida primera impresión sobre qué es FleetProof para nuestros segmentos objetivo.<br>Esto se confirmará cuando los usuarios accedan a la landing page y naveguen por sus secciones. |
| Sprint 1 Commitment | 21 Story Points |
| Sum of Planned Story Points | 21 |

#### 5.2.1.2 Aspect Leaders and Collaborators

Ahora presentaremos nuestro LACX (Leadership-and-Collaboration Matrix) que nos ayudará a saber quién lidera y quién colabora en cada aspecto de este primer sprint.
Los aspectos que tomamos en cuenta para este primer sprint fueron los features de nuestra Landing Page.

| Team Member Last Name, First Name | GitHub Username | Hero L/C | Nosotros L/C | Beneficios L/C | Precios L/C | Contacto L/C | Footer L/C |
|---|---|:---:|:---:|:---:|:---:|:---:|:---:|
| **Reyes Limo Sebastian** | llegastian11 | C | C | C | C | L | C |
| **Quintanilla Gonzalo** | GoldQP | L | C | C | C | C | C |
| **Morales Jefferson** | Fenfito | C | L | C | C | C | C |
| **Gómez De La Torre Rodrigo** | rod670 | C | C | C | L | C | C |
| **Gorbeña Eduardo** | EduardooGV | C | C | L | C | C | L |

**Nota.** L = *Leader* (responsable principal del aspecto).
C = *Collaborator* (apoya el desarrollo del aspecto).

#### 5.2.1.3 Sprint Backlog 1

<table>
    <tr>
        <td>Sprint #</td>
        <td colspan="7">Sprint 1</td>
    </tr>
    <tr>
        <td colspan="2">User Story</td>
        <td colspan="2">Work-Item / Task</td>
        <td>Description</td>
        <td>Estimation (Hours)</td>
        <td>Assigned To</td>
        <td>Status (To-do / In-Process / To-Review / Done)</td>
    </tr>
    <tr>
        <td>Id</td>
        <td>Title</td>
        <td>Id</td>
        <td>Title</td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td>US01</td>
        <td>Presentación de propuesta para flotas</td>
        <td>T1</td>
        <td>Diseñar estructura de la página principal</td>
        <td>Crear wireframe simple con encabezado, Hero section y pie de página de FleetProof.</td>
        <td>4</td>
        <td>Equipo UX</td>
        <td>Done</td>
    </tr>
    <tr>
        <td>US01</td>
        <td>Presentación de propuesta para flotas</td>
        <td>T2</td>
        <td>Implementar página principal (Hero)</td>
        <td>Desarrollar HTML/CSS base de la página principal aplicando diseño Responsive.</td>
        <td>6</td>
        <td>Dev Front</td>
        <td>Done</td>
    </tr>
    <tr>
        <td>US01</td>
        <td>Presentación de propuesta para flotas</td>
        <td>T3</td>
        <td>Redactar sección de Servicios</td>
        <td>Elaborar contenido con los pilares clave de la plataforma (Checklist, Semáforo, Alertas).</td>
        <td>2</td>
        <td>PO/Equipo</td>
        <td>Done</td>
    </tr>
    <tr>
        <td>US01</td>
        <td>Presentación de propuesta para flotas</td>
        <td>T4</td>
        <td>Implementar sección de Servicios</td>
        <td>Codificar la sección en la landing page usando CSS Grid y Flexbox.</td>
        <td>4</td>
        <td>Dev Front</td>
        <td>Done</td>
    </tr>
    <tr>
        <td>US02</td>
        <td>Beneficios para usuarios particulares</td>
        <td>T5</td>
        <td>Diseñar sección de Nosotros</td>
        <td>Definir estructura visual del equipo fundador y beneficios del Startup Profile.</td>
        <td>3</td>
        <td>Equipo UX</td>
        <td>Done</td>
    </tr>
    <tr>
        <td>US02</td>
        <td>Beneficios para usuarios particulares</td>
        <td>T6</td>
        <td>Implementar sección de Nosotros</td>
        <td>Programar en frontend con estructura responsiva e imágenes adaptables.</td>
        <td>5</td>
        <td>Dev Front</td>
        <td>Done</td>
    </tr>
    <tr>
        <td>US01</td>
        <td>Presentación de propuesta para flotas</td>
        <td>T7</td>
        <td>Diseñar sección de Planes</td>
        <td>Diseñar estructura de planes de suscripción con beneficios y precios diferenciados.</td>
        <td>3</td>
        <td>Equipo UX</td>
        <td>Done</td>
    </tr>
    <tr>
        <td>US01</td>
        <td>Presentación de propuesta para flotas</td>
        <td>T8</td>
        <td>Implementar sección de Planes</td>
        <td>Codificar sección de Pricing en HTML y CSS con diseño corporativo.</td>
        <td>5</td>
        <td>Dev Front</td>
        <td>Done</td>
    </tr>
    <tr>
        <td>US01</td>
        <td>Presentación de propuesta para flotas</td>
        <td>T9</td>
        <td>Redactar información de Contacto</td>
        <td>Crear contenido con correo corporativo, sedes y canales de WhatsApp.</td>
        <td>2</td>
        <td>PO/Equipo</td>
        <td>Done</td>
    </tr>
    <tr>
        <td>US01</td>
        <td>Presentación de propuesta para flotas</td>
        <td>T10</td>
        <td>Implementar sección de Contacto</td>
        <td>Agregar formulario funcional simulado con validaciones básicas en JavaScript.</td>
        <td>4</td>
        <td>Dev Front</td>
        <td>Done</td>
    </tr>
    <tr>
        <td>-</td>
        <td>-</td>
        <td>T11</td>
        <td>Configuración de hosting/despliegue</td>
        <td>Preparar entorno y publicar el Landing Page de FleetProof en Netlify.</td>
        <td>6</td>
        <td>DevOps</td>
        <td>Done</td>
    </tr>
</table>


#### 5.2.1.4 Development Evidence for Sprint Review

Durante el Sprint 1 se implementó la Landing Page de la solución y se construyó la documentación base de arquitectura de software y experiencia de usuario. El desarrollo se realizó en los repositorios públicos de la organización BLIP, utilizando un flujo de ramas basado en feature branches y siguiendo la convención de *Conventional Commits*.

<h3>Development Evidence – Sprint 1</h3>

<table>
    <thead>
        <tr>
            <th>Repository</th>
            <th>Branch</th>
            <th>Commit Id</th>
            <th>Commit Message</th>
            <th>Commit Message Body</th>
            <th>Committed on (Date)</th>
        </tr>
    </thead>
    <tbody> 
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>25f15d2</td>
            <td>docs: add impact maps to requirements specification</td>
            <td>Se agregan los Impact Maps al capítulo 3.</td>
            <td>17/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>51945a0</td>
            <td>docs: add image for the impact mapping</td>
            <td>Inserción de imagen de Impact Mapping.</td>
            <td>17/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>9827e21</td>
            <td>docs: add image for the Impact mapping</td>
            <td>Inserción de segunda imagen de Impact Mapping.</td>
            <td>17/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>f4e52f6</td>
            <td>docs: Create gitkeep</td>
            <td>Creación de archivo .gitkeep para carpetas vacías.</td>
            <td>17/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>7ed9426</td>
            <td>docs: implementación del punto 4.4.1</td>
            <td>Desarrollo del subcapítulo de wireframes 4.4.1.</td>
            <td>16/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>54a86ca</td>
            <td>docs: Update requirements specification with new EPICs and US</td>
            <td>Actualización del capítulo 3 con nuevas épicas.</td>
            <td>16/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>7011b29</td>
            <td>docs: Update user stories and product backlog details</td>
            <td>Refinamiento de las historias de usuario.</td>
            <td>16/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>1470dbf</td>
            <td>docs: add Sebastian profile to chapter 1</td>
            <td>Adición del perfil de Sebastian al capítulo 1.</td>
            <td>16/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-LandingPage</td>
            <td>main</td>
            <td>e1d4b4a</td>
            <td>feat: migración de React a HTML, CSS y JS puro</td>
            <td>Se establece estructura SEO-friendly con Media Queries.</td>
            <td>16/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-LandingPage</td>
            <td>main</td>
            <td>a8b9c23</td>
            <td>feat: add hero section and responsive layout</td>
            <td>Implementación de la sección principal con tarjeta flotante.</td>
            <td>16/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-LandingPage</td>
            <td>main</td>
            <td>f4d5e67</td>
            <td>feat: implement pricing and services section</td>
            <td>Integración de la sección de precios y pilares en HTML.</td>
            <td>16/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-LandingPage</td>
            <td>main</td>
            <td>9a8b7c6</td>
            <td>style: fix mobile menu and media queries</td>
            <td>Ajustes de formato y funcionalidad de menú móvil.</td>
            <td>16/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>a8979e7</td>
            <td>docs: Add new Epic/Stories and update product backlog</td>
            <td>Actualización de Épicas y Product Backlog.</td>
            <td>15/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>a0aab1e</td>
            <td>docs: add image source for Jefferson Morales</td>
            <td>Imagen de perfil de Jefferson agregada.</td>
            <td>15/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>6e0e68e</td>
            <td>docs(chapter-1): add image for the Student Profile</td>
            <td>Imagen agregada para el perfil de estudiante.</td>
            <td>15/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>4b5c714</td>
            <td>docs: add .gitkeep to initialize assets directory</td>
            <td>Inicialización de directorio assets.</td>
            <td>15/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>2ea12c5</td>
            <td>docs(assets): add .gitkeep to initialize assets directory</td>
            <td>Creación de carpeta de assets con gitkeep.</td>
            <td>15/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>a51fd62</td>
            <td>docs: Add student profile for Jefferson Bayron Morales</td>
            <td>Perfil de Jefferson Morales añadido al documento.</td>
            <td>15/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>6013c61</td>
            <td>docs: Implementación del capitulo 4.8</td>
            <td>Desarrollo del diagrama y diseño de Base de Datos.</td>
            <td>14/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>ea11113</td>
            <td>docs: Implementación del capitulo 4.7</td>
            <td>Desarrollo de diagramas de clases Orientado a Objetos.</td>
            <td>14/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>cca1296</td>
            <td>docs: Implementación del capitulo 4.6</td>
            <td>Desarrollo de Bounded Contexts y diagramas de contenedores.</td>
            <td>14/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>f063dc1</td>
            <td>docs: Implementación del capitulo 4.5</td>
            <td>Redacción sobre el prototipado web.</td>
            <td>14/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>6736595</td>
            <td>docs: Implementación del resto del capitulo 4.4</td>
            <td>Finalización de diagramas de flujos y UX.</td>
            <td>14/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>d9e1715</td>
            <td>docs: inserción del capitulo 4.4.2</td>
            <td>Inserción de diagramas de flujo web.</td>
            <td>14/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>fe6012a</td>
            <td>docs: fix image formatting in chapter IV for improved presentation</td>
            <td>Corrección de formato de imágenes en el cap 4.</td>
            <td>14/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>379c8b3</td>
            <td>docs: update image source in chapter IV for improved accessibility</td>
            <td>Actualización de rutas de imágenes en artefactos de diseño.</td>
            <td>14/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>87877ff</td>
            <td>docs: update chapter IV with mock-ups for FleetProof's web application on desktop and mobile</td>
            <td>Adición de mockups al capítulo 4.</td>
            <td>14/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>14b0dcc</td>
            <td>docs: add additional wireframes for FleetProof's mobile interface in chapter IV</td>
            <td>Adición de wireframes en resolución móvil.</td>
            <td>14/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>3b3d492</td>
            <td>docs: add wireframes for FleetProof's web application and mobile interface in chapter IV</td>
            <td>Inserción de wireframes de la app web.</td>
            <td>14/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>af3331c</td>
            <td>docs: update chapter IV with detailed search and navigation systems, including wireframes for desktop and mobile</td>
            <td>Detalle de sistemas de búsqueda y navegación UX.</td>
            <td>14/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>c6a3b77</td>
            <td>docs: add interview evidence to chapter 2</td>
            <td>Inclusión de capturas y enlaces a entrevistas.</td>
            <td>14/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>3fda627</td>
            <td>docs: enhance chapter IV with SEO tags and meta tags for landing page and web application</td>
            <td>Definición de meta etiquetas SEO.</td>
            <td>13/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>ff675f2</td>
            <td>docs: expand chapter IV with detailed labeling systems for FleetProof's web application and landing page</td>
            <td>Documentación del Labeling System.</td>
            <td>13/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>f6655b4</td>
            <td>docs: update chapter IV with web style guidelines, responsive design, and information architecture</td>
            <td>Guías de estilo y arquitectura de información.</td>
            <td>13/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>188bb31</td>
            <td>docs: update chapter IV with images, style guidelines, and project configuration files</td>
            <td>Subida inicial de imágenes y estilos corporativos.</td>
            <td>13/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>8aeb9f3</td>
            <td>docs: update Sebastian technical profile</td>
            <td>Actualización de descripción técnica en el equipo.</td>
            <td>13/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>af5bcc2</td>
            <td>docs: complete chapter 2 research artifacts</td>
            <td>Finalización de artefactos de investigación UX (User Journey, Empathy Maps).</td>
            <td>13/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>2968509</td>
            <td>Update collaboration data for Sebastian Reyes Limo</td>
            <td>Matriz LACX actualizada.</td>
            <td>13/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>8594853</td>
            <td>docs: Update 02-chapter-1-introduction.md</td>
            <td>Modificaciones en la introducción del documento.</td>
            <td>13/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>9fef174</td>
            <td>docs: enhance chapter 1 introduction with detailed profiles of target segments and their needs</td>
            <td>Definición detallada de segmentos objetivo.</td>
            <td>12/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>6e5f82a</td>
            <td>docs: add link to Lean UX Canvas in chapter 1 introduction for easy access</td>
            <td>Enlace al tablero Miro de Lean UX agregado.</td>
            <td>12/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>094e49a</td>
            <td>docs: add Lean UX Canvas explanation and image for FleetProof in chapter 1</td>
            <td>Inserción visual del lienzo Lean UX.</td>
            <td>12/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>7725de6</td>
            <td>docs: add Lean UX hypothesis statements for feature assumptions in chapter 1</td>
            <td>Definición de hipótesis UX para FleetProof.</td>
            <td>12/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>a0b75bf</td>
            <td>docs: enhance section 1.2.2 with detailed business and user assumptions for clarity</td>
            <td>Supuestos de negocio y usuario detallados en sección 1.2.2.</td>
            <td>12/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>b484374</td>
            <td>docs: refine Lean UX problem statement in chapter 1 introduction for clarity and detail</td>
            <td>Problem statement y formulación del problema definidos.</td>
            <td>12/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>a4a48cb</td>
            <td>docs: add expand section 1.2.2 on Lean UX process with context on fleet management challenges</td>
            <td>Contexto inicial del proceso Lean UX y retos B2B.</td>
            <td>12/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>1a2d38b</td>
            <td>docs: add expand chapter 1 introduction with detailed problem analysis and context</td>
            <td>Análisis de la problemática base en el sector automotor.</td>
            <td>12/09/2026</td>
        </tr>
        <tr>
            <td>1ASI0729-8088-BLIP/blip-fleetproof-project-report</td>
            <td>feature/sprint1-capitulo-1</td>
            <td>ea45553</td>
            <td>docs: update chapter 1 introduction with team member profiles</td>
            <td>Adición de la tabla de integrantes y descripciones.</td>
            <td>12/09/2026</td>
        </tr>
    </tbody>
</table>

#### 5.2.1.5 Execution Evidence for Sprint Review

Durante el **Sprint 1** se implementó la Landing Page de la plataforma FleetProof, cumpliendo con los objetivos definidos en el Sprint Backlog.
La Landing Page constituye el primer punto de interacción con los usuarios, mostrando de forma clara los valores de la plataforma, los servicios ofrecidos, el perfil de la startup y los planes de suscripción disponibles.

El desarrollo se centró en:

* Diseño responsive y navegación entre secciones.
* Secciones implementadas: *Hero, Nosotros, Beneficios, Precios, Contacto, Footer*.
* Formulario de contacto con validaciones frontend implementadas.

A continuación, se presentan capturas de las principales vistas desarrolladas:

<img src="https://res.cloudinary.com/dehoql1oc/image/upload/v1789670193/Captura_de_pantalla_2026-09-17_133618_ncpfwl.png" alt="inicio" width="800">

<br>

*Figura 5.1. Vista principal (Hero) de la Landing Page en versión de escritorio.*

<img src="https://res.cloudinary.com/dehoql1oc/image/upload/v1789670267/Captura_de_pantalla_2026-09-17_133728_ouwkcw.png" alt="inicio" width="800">
<br>

*Figura 5.2. Vista de las secciones de Servicios y Precios de la plataforma.*

<img src="https://res.cloudinary.com/dehoql1oc/image/upload/v1789670341/Captura_de_pantalla_2026-09-17_133839_nphvm6.png" alt="inicio" width="800">
<br>

*Figura 5.3. Vista adaptable para dispositivos móviles con el diseño responsivo aplicado.*


#### 5.2.1.6 Services Documentation Evidence for Sprint Review

Durante el Sprint 1, el alcance principal fue la implementación de la Landing Page, por lo que no se desarrollaron servicios de backend asociados a la lógica de negocio. Sin embargo, se dejó preparado el repositorio de Web Services con estructura inicial de documentación en OpenAPI/Swagger, lo que permitirá en futuros sprints integrar endpoints de autenticación, consulta de información vehicular, generación de reportes y gestión de flotas.

#### 5.2.1.7 Software Deployment Evidence for Sprint Review

Durante el Sprint 1, se logró el despliegue exitoso de la Landing Page de FleetProof en un entorno de producción utilizando la plataforma de hosting Netlify. El entorno se encuentra configurado con integración continua (Continuous Deployment), lo que permite que cualquier cambio aprobado y fusionado en la rama `main` del repositorio de GitHub se publique de manera automática.

* **Plataforma de despliegue:** Netlify
* **Rama de despliegue:** `main`
* **URL de Producción:** [https://fleetproof-landingpage.netlify.app/](https://fleetproof-landingpage.netlify.app/)

A continuación, se presenta la evidencia del despliegue exitoso en la plataforma:


<img src="https://res.cloudinary.com/dehoql1oc/image/upload/v1789628688/Captura_de_pantalla_2026-09-17_020436_pvq8li.png" alt="inicio" width="800">

---
<br>

<img src="https://res.cloudinary.com/dehoql1oc/image/upload/v1789670193/Captura_de_pantalla_2026-09-17_133618_ncpfwl.png" alt="inicio" width="800">

**Figura 5.4.** Evidencia de despliegue exitoso en la plataforma Netlify.

#### 5.2.1.8 Team Collaboration Insights during Sprint

Durante el Sprint 1, el equipo trabajó siguiendo la estrategia **GitFlow**, creando ramas específicas por cada *feature* o entregable de documentación (ejemplo: `feature/sprint1-capitulo-1`, `feature/sprint1-capitulo-2`, `feature/sprint1-capitulo-3`, `feature/sprint1-capitulo-4`, `feature/sprint1-capitulo-5`).

Estas ramas fueron integradas progresivamente en `develop` mediante Pull Requests y, tras la validación y resolución de conflictos correspondiente, se preparó el código consolidado para su integración en la rama principal `main`.

A continuación se presentan los **analíticos de GitHub**, que muestran la participación del equipo en commits, ramas y merges durante el Sprint. Estas evidencias confirman la colaboración activa de todos los miembros:

<img src="https://res.cloudinary.com/dehoql1oc/image/upload/v1789677063/Captura_de_pantalla_2026-09-17_153043_hqzs5r.png" alt="inicio" width="800">
<img src="https://res.cloudinary.com/dehoql1oc/image/upload/v1789677175/Captura_de_pantalla_2026-09-17_153236_uvfxjo.png" alt="inicio" width="800">

