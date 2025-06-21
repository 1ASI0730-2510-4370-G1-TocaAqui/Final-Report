# Capítulo V: Product Implementation, Validation & Deployment

## 5.1. Software Configuration Management

### 5.1.1. Software Development Environment Configuration

#### Requirements Management

**Jira**: Herramienta de gestión ágil utilizada para organizar y monitorear las tareas del proyecto. Cada actividad fue registrada con una clave única y se asignó a miembros responsables, permitiendo controlar el avance por capítulo.  
Ruta de referencia: [https://www.atlassian.com/software/jira](https://www.atlassian.com/software/jira)

#### Product UX/UI Design

**Figma**: Plataforma online empleada para crear diseños visuales y prototipos navegables tanto para escritorio como dispositivos móvilxes. Fue esencial en la definición de la experiencia de usuario del landing.  
Ruta de referencia: [https://www.figma.com](https://www.figma.com)

#### Software Development

**Visual Studio Code**: Editor de texto utilizado por todos los miembros del equipo, elegido por su ligereza, compatibilidad con múltiples lenguajes y sus extensiones útiles para desarrollo web y control de versiones.  
Ruta de referencia: [https://code.visualstudio.com](https://code.visualstudio.com)

**HTML5 / CSS3 / JavaScript**: Tecnologías base para el desarrollo del sitio web estático. HTML estructura el contenido, CSS define el estilo visual y JavaScript brinda interactividad.

Referencias:
- HTML5: [https://www.w3schools.com/html/html5_syntax.asp](https://www.w3schools.com/html/html5_syntax.asp)
- CSS3: [https://google.github.io/styleguide/htmlcssguide.html](https://google.github.io/styleguide/htmlcssguide.html)
- JavaScript: [https://developer.mozilla.org/es/docs/Web/JavaScript](https://developer.mozilla.org/es/docs/Web/JavaScript)

**Git**: Sistema de control de versiones distribuido usado localmente para manejar el historial de cambios del proyecto.  
Ruta de referencia: [https://git-scm.com](https://git-scm.com)

#### Documentation & Project Hosting

**GitHub**: Plataforma en la nube donde se alojan los repositorios del equipo. Se utilizó para controlar versiones, gestionar ramas con GitFlow y mantener sincronizado el avance entre todos los integrantes.  
Repositorio de la Landing Page:  
[https://github.com/1ASI0730-2510-4370-G1-TocaAqui/Landing-Page](https://github.com/1ASI0730-2510-4370-G1-TocaAqui/Landing-Page)

#### Software Deployment

**GitHub Pages**: Servicio empleado para desplegar el sitio estático del proyecto directamente desde la rama `main`.  
Enlace en producción:  
[https://1asi0730-2510-4370-g1-tocaaqui.github.io/Landing-Page/](https://1asi0730-2510-4370-g1-tocaaqui.github.io/Landing-Page/)

**Vercel (previsto)**: Plataforma que será usada en los próximos sprints para desplegar la aplicación frontend en Vue.js, permitiendo despliegues automáticos desde GitHub.  
Ruta de referencia: [https://vercel.com](https://vercel.com)


### 5.1.2. Source Code Management

El equipo aplica la estrategia GitFlow, que organiza el desarrollo con ramas específicas para cada tipo de contribución. Las ramas implementadas en este Sprint fueron:

- `main`: contiene la versión estable desplegada
- `develop`: utilizada como base para integrar avances
- `feature/*`: se creó una rama por cada funcionalidad nueva del landing page

Durante este primer Sprint, se realizó trabajo activo en ramas `feature/*`, que luego fueron integradas mediante `merge` hacia la rama `main` para el despliegue en GitHub Pages. La estructura de ramas puede verse directamente en el historial del repositorio.

   ![Gitflow](../../assets/gitflow.png)


Repositorio principal:  
[https://github.com/1ASI0730-2510-4370-G1-TocaAqui/Landing-Page](https://github.com/1ASI0730-2510-4370-G1-TocaAqui/Landing-Page)

**Commits estructurados (Conventional Commits)**  
Se siguió el estándar [Conventional Commits](https://www.conventionalcommits.org) para mantener claridad y coherencia en el historial del proyecto. Ejemplos reales incluidos:

- `feat(html): added material design`
- `style(icons): replace RemixIcon with Material Design Icons library`
- `feat(a11y): add ARIA attributes to main navigation and header sections`
- `docs(readme): update documentation for UPC university project`



### 5.1.3. Source Code Style Guide & Conventions


#### HTML

- Todas las etiquetas deben cerrarse correctamente
- Comentarios cortos en línea
- Uso obligatorio de atributos `alt`, `width`, `height` en imágenes
- Nombres de clases en inglés, en lower-case con guiones

Referencia: [https://www.w3schools.com/html/html5_syntax.asp](https://www.w3schools.com/html/html5_syntax.asp)

#### CSS

- Indentación de 2 espacios
- Código en minúscula y limpio
- Comentarios explicativos por bloque
- Nombres de clase descriptivos y semánticos

Referencia: [https://google.github.io/styleguide/htmlcssguide.html](https://google.github.io/styleguide/htmlcssguide.html)

#### JavaScript

- Variables con nombres representativos
- Uso coherente de comillas (simples o dobles)
- Funciones modulares y reutilizables
- Comentarios en secciones complejas
- Evitar variables globales

Referencia: [https://developer.mozilla.org/es/docs/Web/JavaScript](https://developer.mozilla.org/es/docs/Web/JavaScript)

#### Vue.js (para sprints futuros)

- Carpetas organizadas por módulos: `components/`, `views/`, `store/`
- Reutilización de componentes
- Separación clara entre lógica y vista
- Documentación interna con props, eventos y métodos

Referencia: [https://vuejs.org/guide/introduction](https://vuejs.org/guide/introduction)

### 5.1.4. Software Deployment Configuration

Para desplegar la **Landing Page** del proyecto **TocaAquí** usando **GitHub Pages**, se siguieron los siguientes pasos:

1. **Ubicar el repositorio del proyecto**  
   Se accede al repositorio público alojado en GitHub que contiene el código fuente del sitio:  
   ![Paso 1](../../assets/Deploy-first.png)

2. **Ir a la sección de configuración (Settings)**  
   En la barra superior del repositorio, se hace clic en la pestaña **Settings**.

   ![Paso 2](../../assets/Deploy-two.png)

3. **Configurar GitHub Pages desde una rama**  
   En la sección **Pages**, dentro de **Build and deployment**, se selecciona `Deploy from a branch`.  
   Luego, se elige la rama `main` y la carpeta raíz `/ (root)` como origen del contenido.

   ![Paso 3](../../assets/Deploy-three.png)

Una vez configurado, GitHub genera automáticamente la URL pública del sitio, que queda disponible para validación, pruebas o entrevistas con usuarios.

**URL:** [`https://1asi0730-2510-4370-g1-tocaaqui.github.io/Landing-Page/index.html`](https://1asi0730-2510-4370-g1-tocaaqui.github.io/Landing-Page/index.html)

## 5.2. Landing Page, Services & Applications Implementation
### 5.2.1. Sprint 1
#### 5.2.1.1. Sprint Planning 1

| **Sprint #**                      | **Sprint 1**                                                                 |
|----------------------------------|------------------------------------------------------------------------------|
| **Sprint Planning Background**   |                                                                              |
| **Date**                         | 11/04/2025                                                                   |
| **Time**                         | 05:00 PM                                                                     |
| **Location**                     | Servidor de Discord del Equipo                                               |
| **Prepared By**                  | Oscar Antayhua                                                              |
| **Attendees (to planning meeting)** | Oscar Antayhua / Juan Llamccaya / Nelson Pereira / Diego Cabrera / Eddo Su Caletti |
| **Sprint 1 Review Summary**      |   Durante este sprint, el equipo trabajó en la base del proyecto: se desarrolló, diseñó y publicó la primera versión funcional de la landing page, incluyendo componentes clave como la descripción del servicio, los planes de suscripción, formularios de contacto y estructura multilenguaje. También se completaron actividades de UX como User Personas, Journey Maps y arquitectura de información.                                                                           |
| **Sprint 1 Retrospective Summary** |      Los integrantes coincidieron en que el trabajo en equipo fue eficiente y colaborativo. Se destacaron aciertos en la integración de herramientas como UXPressia, Figma y el diseño responsivo. Como mejora, se mencionó optimizar la gestión de tiempos entre subtareas y usar criterios de aceptación más claros desde el inicio.                                                                      |
| **Sprint Goal & User Stories**   |        Completar la fase de descubrimiento e investigación, validación de usuarios, análisis de la competencia, arquitectura de información y base de la landing.                                                                     |
| **Sprint 1 Goal**                |   Nuestro objetivo es desarrollar una landing page completa y coherente con el enfoque del proyecto “TocaAquí”, asegurando que fuera funcional, responsiva, accesible y atractiva para artistas y locales. Este sprint también sentó las bases para la experiencia del usuario mediante entregables como los User Personas, Empathy Maps, Wireframes y Style Guides.                                                                           |
| **Sprint 1 Velocity**            | 4 Velocity                                                                   |
| **Sum of Story Points**          | 6 Story Points                                                               |

#### 5.2.1.2. Aspect Leaders and Collaborators

| Team Member              | GitHub Username     | Landing Page | Diseño UI/UX | HTML/CSS | JavaScript | Documentación |
|--------------------------|---------------------|--------------|---------------|----------|-------------|----------------|
| Nelson Pereira           | fabrizzioper        | C            | C             | C        | L           | C              |
| Oscar Antayhua           | OscarAntayhuaCastillo | L            | C             | C        | C           | L              |
| Juan Llamccaya           | JuanPaulLla        | C            | C             | L        | C           | C              |
| Diego Cabrera            | omele7             | C            | C             | C        | L           | C              |
| Eddo Su Caletti          | Asalreon520        | C            | L             | C        | C           | C              |

#### 5.2.1.3. Sprint Backlog 1


| **User Story Id** | **User Story Title** | **Work-Item/Task Id** | **Work-Item/Task Title** | **Description** | **Estimation** | **Assigned To** | **Status** |
|:-----------------:|:--------------------:|:---------------------:|:-----------------------:|:---------------:|:--------------:|:--------------:|:----------:|
| US01 | Acceso a la Landing Page desde distintos dispositivos | T01 | Diseño responsivo | Ajustar estilos CSS para adaptación en mobile, tablet y desktop | 5h | Juan Llamccaya | Done |
| US02 | Visualización de información del propósito | T02 | Redacción de sección "Sobre Nosotros" | Crear texto descriptivo para explicar misión y beneficios de TocaAquí | 3h | Nelson Pereira | Done |
| US03 | Visualización de imágenes y gráficos relevantes | T03 | Selección y carga de imágenes | Seleccionar imágenes ilustrativas y cargarlas en la landing page | 2h | Diego Cabrera | Done |
| US04 | Tipografía cómoda y agradable estéticamente | T04 | Definición de tipografía y estilos | Elegir y aplicar fuentes estéticas y legibles para todo el sitio | 3h | Eddo Su Caletti | Done |
| US05 | Opción de navegación entre secciones | T05 | Implementación de navegación | Programar menú de navegación funcional con anclas internas | 4h | Oscar Antayhua | Done |
| US06 | Formulario de contacto funcional | T06 | Desarrollo de formulario de contacto | Crear y validar formulario de contacto en HTML, CSS y JavaScript | 5h | Diego Cabrera | Done |



#### 5.2.1.4. Development Evidence for Sprint Review

| Repository                                   | Branch | Commit Id | Commit Message                                           | Commit Message Body (resumen)                                                 | Committed on  |
|----------------------------------------------|--------|-----------|----------------------------------------------------------|--------------------------------------------------------------------------------|----------------|
| Landing-Page                                 | main   | 66dc745   | style(icons): update social media icons to Material Design in English version | Actualización de íconos en versión en inglés                                  | Apr 14, 2025   |
| Landing-Page                                 | main   | 7a73592   | Merge branch 'develop'                                  | Fusión de cambios desde rama develop                                           | Apr 14, 2025   |
| Landing-Page                                 | main   | 96d4570   | styles(webkit): fix errors on webkit background         | Correcciones visuales para navegadores WebKit                                 | Apr 14, 2025   |
| Landing-Page                                 | main   | e7d5c76   | feat(html): added material design.                      | Integración de Material Design a la estructura HTML                            | Apr 14, 2025   |
| Landing-Page                                 | main   | 041541c   | style(icons): replace RemixIcon with Material Design Icons library | Reemplazo de biblioteca de íconos por Material Design Icons                  | Apr 14, 2025   |
| Landing-Page                                 | main   | 4f76ad4   | feat(redes-sociales): added social icons                | Adición de íconos de redes sociales                                            | Apr 14, 2025   |
| Landing-Page                                 | main   | fe42468   | feat(a11y): add ARIA attributes to main navigation and header sections | Mejora de accesibilidad usando atributos ARIA                                | Apr 14, 2025   |
| Landing-Page                                 | main   | 3a2b1c0   | feat(assets): added nelson picture profile              | Imagen de perfil agregada a los assets                                         | Apr 14, 2025   |
| Landing-Page                                 | main   | f48a5df   | feat(html): added nelson profile picture url            | URL de imagen de perfil de Nelson en HTML                                      | Apr 14, 2025   |
| Landing-Page                                 | main   | 72f9f94   | fix(readme): fix year                                   | Corrección del año en README                                                  | Apr 14, 2025   |
| Landing-Page                                 | main   | 8102961   | docs(readme): update documentation for UPC university project | Actualización de README con detalles del proyecto universitario             | Apr 14, 2025   |
| Landing-Page                                 | main   | 8a13d40   | fix(styles): add standard background-clip property for cross-browser compatibility | Mejora de compatibilidad CSS                                                 | Apr 13, 2025   |
| Landing-Page                                 | main   | 3c01cbf   | fix(team): fix alt names.                               | Corrección de textos alternativos para accesibilidad                          | Apr 13, 2025   |
| Landing-Page                                 | main   | d2349fe   | style(responsive): enhance mobile layout and responsiveness | Mejora de estilos responsive                                                 | Apr 13, 2025   |
| Landing-Page                                 | main   | b84e7c7   | feat(hero): add segmentation buttons and improve responsive design | Botones segmentados para artistas y locales en la sección principal         | Apr 13, 2025   |
| Landing-Page                                 | main   | 9aeb89a   | fix(spaces-name): fixed spaces names and changed to venues and locales | Cambio de texto: "spaces" por "venues/locales"                              | Apr 13, 2025   |
| Landing-Page                                 | main   | 877734e   | feat(main.js): added event listener for plans           | JS para detectar selección de planes                                           | Apr 13, 2025   |
| Landing-Page                                 | main   | d7c58d5   | feat(assets): added some assets                         | Nuevos recursos gráficos                                                       | Apr 13, 2025   |
| Landing-Page                                 | main   | e9cf84f   | feat(styles): added some styles for different sections of html | Estilos adicionales para secciones varias                                  | Apr 13, 2025   |
| Landing-Page                                 | main   | 4041d0e   | feat(main-en): added javascript function for english landing page | Funcionalidad en JS para cambio de idioma                                    | Apr 13, 2025   |
| Landing-Page                                 | main   | b542750   | feat(landing-page): added plans and fix html structure  | Incorporación de planes y corrección de estructura                            | Apr 13, 2025   |
| Landing-Page                                 | main   | 257f243   | feat(index): Added english landing page                 | Se creó la versión en inglés de la landing                                     | Apr 13, 2025   |
| Landing-Page                                 | main   | 9eab618   | Merge branch 'feature/team' into develop                | Fusión de rama feature/team                                                   | Apr 12, 2025   |
| Landing-Page                                 | main   | a61b54a   | Merge branch 'feature/contact-us' into develop          | Fusión de rama feature/contact-us                                            | Apr 12, 2025   |
| Landing-Page                                 | main   | e34ae9a   | Merge branch 'feature/footer' into develop              | Fusión de rama feature/footer                                                | Apr 12, 2025   |
| Landing-Page                                 | main   | 5efaecc   | feat(styles): added some contact-us section styles      | Estilos para sección de contacto                                              | Apr 12, 2025   |
| Landing-Page                                 | main   | 1e1660d   | feat(contact-us): section contact-us added to html      | Maquetado HTML de la sección de contacto                                      | Apr 12, 2025   |
| Landing-Page                                 | main   | 40a6d3e   | fix(about-experience): fix duplicated content           | Corrección de contenido duplicado                                             | Apr 12, 2025   |
| Landing-Page                                 | main   | 9bfe3d2   | feat(team): update styles.css with responsive team section design | Diseño responsive de sección equipo                                        | Apr 11, 2025   |
| Landing-Page                                 | main   | 39e1e3e   | feat(team): add team section with basic structure and styles | Sección del equipo con estructura básica y estilos                         | Apr 11, 2025   |
| Landing-Page                                 | main   | 0a7f37f   | feat(about-experience): add experience section markup and styles | Sección de experiencia implementada                                        | Apr 11, 2025   |
| Landing-Page                                 | main   | 70e1ee6   | feat(contact): add styles for contact section            | Estilos CSS de la sección contacto                                            | Apr 11, 2025   |
| Landing-Page                                 | main   | 3d10749   | feat(footer): add footer section and structure          | Pie de página agregado                                                        | Apr 11, 2025   |
| Landing-Page                                 | main   | 58d02cc   | feat: added the experience section                      | Sección de experiencia general agregada                                       | Apr 11, 2025   |
| Landing-Page                                 | main   | 1c8b0e4   | feat: updated the landing page                          | Actualización general de la estructura de la landing                          | Apr 11, 2025   |
| Landing-Page                                 | main   | 62d0c5e   | feat(home): add hero section styles and animation       | Animación y estilos del home                                                  | Apr 08, 2025   |
| Landing-Page                                 | main   | 801c76e   | feat(about-us): add about section markup and styling    | Sección sobre nosotros                                                        | Apr 08, 2025   |
| Landing-Page                                 | main   | 9ff7dd7   | feat(assets): add about and home background             | Fondos de secciones                                                            | Apr 08, 2025   |
| Landing-Page                                 | main   | b74b1a2   | feat(assets): add light and dark versions of logo images | Versiones claras y oscuras del logo                                         | Apr 08, 2025   |
| Landing-Page                                 | main   | 3a20ccf   | feat(navbar): add responsive styles for navigation       | Estilos responsive para navbar                                                | Apr 08, 2025   |
| Landing-Page                                 | main   | 1c325e4   | feat(navbar): main js created                          | Funcionalidad JS para navegación                                              | Apr 08, 2025   |
| Landing-Page                                 | main   | 6f37fc7   | feat(navbar): index created                            | Archivo inicial index                                                         | Apr 08, 2025   |
| Landing-Page                                 | main   | 8e06aeb   | Create Readme.md                                        | README base creado                                                            | Apr 07, 2025   |

#### 5.2.1.5. Execution Evidence for Sprint Review
Para este primer Sprint, hemos desarrollado la Landing Page del proyecto "TocaAquí". A través de esta landing, los usuarios pueden visualizar de forma clara la propuesta de valor de nuestra plataforma, destinada a conectar músicos emergentes con locales de eventos, facilitando la contratación, coordinación y pagos seguros.

A continuación, se presentan las User Stories asociadas que se ejecutaron y evidencian el trabajo realizado:

| **ID** | **User Story** | **Evidencia en Landing Page** |
|:------:|:--------------:|:-----------------------------:|
| US01 | Acceso a la Landing Page desde distintos dispositivos | Visualización responsive en computadoras y móviles |
| US02 | Visualización de la información del propósito | Sección "Sobre Nosotros" describiendo la solución |
| US03 | Visualización de imágenes y gráficos relevantes | Imágenes en las secciones principales (home, about) |
| US04 | Tipografía cómoda y estéticamente agradable | Fuente limpia y moderna compatible con el estilo |
| US05 | Opción de navegación entre secciones | Menú de navegación y botones de acción funcionales |
| US06 | Formulario de contacto funcional | Sección de contacto con campos de entrada validados |

**Sección Sobre Nosotros**  
Muestra el propósito de TocaAquí, permitiendo al visitante entender rápidamente el objetivo de la plataforma.

![Sobre-nosotros](/assets/sobre-nosotros.png)

**Nuestro Equipo**  
Se exhiben los perfiles de los desarrolladores de la startup, reforzando la transparencia y profesionalismo del proyecto.

![Equipo](/assets/equiopo.png)


**Planes Disponibles**  
Se muestra una estructura clara de planes para artistas y locales, acompañada de botones de acción intuitivos.

![Planes](/assets/planes.png)


**Formulario de Contacto**  
Formularios para el envío de mensajes de contacto, cumpliendo criterios de accesibilidad y usabilidad.

![Contacto](/assets/contacto.png)


#### 5.2.1.6. Services Documentation Evidence for Sprint Review

Durante el Sprint 1 no se trabajaron endpoints documentados, ya que el alcance se centró exclusivamente en el desarrollo del Landing Page. La documentación OpenAPI comenzará en el Sprint 2.

#### 5.2.1.7. Software Deployment Evidence for Sprint Review

Durante el Sprint 1, se realizó el despliegue de la landing page del proyecto utilizando **GitHub Pages**.

- **Repositorio:** [Landing-Page](https://github.com/1ASI0730-2510-4370-G1-TocaAqui/Landing-Page)
- **URL de producción:** [https://1asi0730-2510-4370-g1-tocaaqui.github.io/Landing-Page/](https://1asi0730-2510-4370-g1-tocaaqui.github.io/Landing-Page/)
- **Branch desplegado:** `main`

El sitio fue configurado y publicado correctamente, permitiendo acceso público a las secciones: Home, About Us, Team, Contact y Planes.

![Landing_page](/assets/landing.png)

#### 5.2.1.8. Team Collaboration Insights during Sprint

Durante el desarrollo del Sprint 1, se evidenció una participación activa y distribuida entre los integrantes del equipo, reflejada tanto en la frecuencia de commits como en las funcionalidades aportadas. En total, se realizaron 39 commits, los cuales fueron generados por 5 autores diferentes, destacando la colaboración en ramas específicas como feature/about-us, feature/navbar y develop, todas correctamente integradas mediante pull requests.

| Integrante             | Commits | Líneas añadidas | Líneas eliminadas | Áreas de contribución principales                                                                 |
|------------------------|---------|------------------|--------------------|---------------------------------------------------------------------------------------------------|
| Oscar Antayhua Castillo | 32      | 2896             | 929                | Navegación, accesibilidad (ARIA), responsive, estilos, íconos, estructura HTML, despliegue GitHub Pages |
| JuanPaulLla            | 2       | 181              | 2                  | Sección de equipo (team), ajustes visuales                                                        |
| Asalreon520            | 2       | 132              | 0                  | Footer, sección de contacto                                                                       |
| omele7                 | 2       | 114              | 2                  | Sección de experiencia, mejoras generales en la landing                                           |
| fabrizzioper           | 1       | 112              | 0                  | Estructura y estilos de la sección experiencia                                                    |


Commits:
![Commits](../../assets/commits.png)

Analiticas de Colaboración:
![Contributors](../../assets/contributors.png)



### 5.2.2. Sprint 2
#### 5.2.2.1. Sprint Planning 2

| Sprint # | Sprint 2 |
|----------------------------------|------------------------------------------------------------------------------|
| Sprint Planning Background | |
| Date | 05/05/2025 |
| Time | 05:00 PM |
| Location | Servidor de Discord del Equipo |
| Prepared By | Oscar Antayhua |
| Attendees (to planning meeting) | Oscar Antayhua / Juan Llamccaya / Nelson Pereira / Diego Cabrera / Eddo Su Caletti |
| Sprint 2 Review Summary | Durante este sprint, el equipo se enfocó en el desarrollo de la aplicación web principal utilizando Vue.js y PrimeVue como biblioteca de componentes UI. Se implementó un backend simulado con JSON Server para el desarrollo rápido de prototipos. Se completaron las funcionalidades clave del dashboard, gestión de eventos, sistema de pagos y calificaciones. |
| Sprint 2 Retrospective Summary | El equipo destacó la productividad alcanzada con Vue.js y la calidad de los componentes de PrimeVue. El uso de JSON Server facilitó el desarrollo del frontend sin dependencias de un backend real. Como puntos de mejora, se identificó la necesidad de mejorar la gestión del estado con Pinia y optimizar las llamadas a la API. |
| Sprint Goal & User Stories | Desarrollar la primera versión de la aplicación web que permita a artistas y locales gestionar sus perfiles, eventos, pagos y calificaciones. Implementar la autenticación de usuarios, sistema de gestión de eventos, módulo de pagos y funcionalidades básicas de interacción entre artistas y locales utilizando Vue.js, PrimeVue y JSON Server como stack tecnológico. |
| Sprint 2 Goal | Nuestro objetivo es implementar la primera versión funcional de la aplicación web que permita a los usuarios registrarse, gestionar sus perfiles, coordinar eventos y realizar seguimiento de pagos. La aplicación debe ofrecer una experiencia fluida y moderna utilizando Vue.js y PrimeVue, con datos simulados mediante JSON Server para facilitar el desarrollo y pruebas. |
| Sprint 2 Velocity | 6 Velocity |
| Sum of Story Points | 8 Story Points |


#### 5.2.2.2. Aspect Leaders and Collaborators

| Team Member | GitHub Username | Frontend | Backend | UI/UX | Testing | Documentation |
|------------|----------------|-----------|---------|-------|---------|---------------|
| Nelson Pereira | fabrizzioper | C | L | C | C | C |
| Oscar Antayhua | OscarAntayhuaCastillo | L | C | C | C | L |
| Juan Llamccaya | JuanPaulLla | C | C | L | C | C |
| Diego Cabrera | omele7 | C | C | C | L | C |
| Eddo Su Caletti | Asalreon520 | C | C | C | C | C |

#### 5.2.2.3. Sprint Backlog 2

| **User Story Id** | **User Story Title** | **Work-Item/Task Id** | **Work-Item/Task Title** | **Description** | **Estimation** | **Assigned To** | **Status** |
|:-----------------:|:--------------------:|:---------------------:|:-----------------------:|:---------------:|:--------------:|:--------------:|:----------:|
| US07 | Registro como artista en la plataforma | T01 | Implementar formulario de registro | Crear formulario con validaciones para registro de artistas con Vue.js y PrimeVue | 8h | Nelson Pereira | Done |
| US08 | Acceso al dashboard personalizado de artista | T02 | Diseño y desarrollo del dashboard | Implementar vista principal con módulos de perfil, postulaciones, agenda y pagos | 10h | Oscar Antayhua | Done |
| US09 | Búsqueda de eventos compatibles con mi perfil | T03 | Sistema de búsqueda y filtros | Desarrollar funcionalidad de búsqueda y filtrado de eventos por género y ubicación | 12h | Juan Llamccaya | Done |
| US10 | Postulación rápida a un evento desde la plataforma | T04 | Proceso de postulación | Implementar flujo de postulación a eventos con confirmaciones | 8h | Diego Cabrera | Done |
| US11 | Gestión y edición de mi perfil artístico | T05 | Editor de perfil | Crear interfaz para editar biografía, estilo musical y contenido multimedia | 6h | Eddo Su Caletti | Done |
| US33 | Visualización de pagos recibidos y pendientes | T06 | Panel de pagos | Implementar vista de pagos con estados y detalles | 8h | Nelson Pereira | Done |
| US34 | Visualización de agenda de eventos | T07 | Calendario de eventos | Desarrollar vista de agenda con eventos confirmados y estados | 10h | Oscar Antayhua | Done |
| US27 | Visualización de próximos eventos agendados | T08 | Widget de eventos próximos | Crear componente de resumen de eventos en el dashboard | 6h | Juan Llamccaya | Done |
| US28 | Visualización de pagos pendientes desde el dashboard | T09 | Widget de pagos pendientes | Implementar componente de resumen de pagos en el panel principal | 6h | Diego Cabrera | Done |
| US29 | Acceso rápido a calificaciones recibidas | T10 | Sistema de calificaciones | Desarrollar módulo de visualización de calificaciones y reviews | 8h | Eddo Su Caletti | Done |




#### 5.2.2.4. Development Evidence for Sprint Review

| Repository        | Branch | Commit Id | Commit Message                                                             | Commit Message Body (resumen)                                                  | Committed on  |
|-------------------|--------|-----------|-----------------------------------------------------------------------------|-------------------------------------------------------------------------------|---------------|
| TocaAqui-WebApp   | develop | 933ae7e   | fix(http): fixed                                                            | Corrección de errores en el módulo HTTP                                        | May 15, 2025  |
| TocaAqui-WebApp   | develop | 8293ae9   | feat(http): added json server multiple endpoints fix                        | Solución para manejar múltiples endpoints en JSON Server                       | May 15, 2025  |
| TocaAqui-WebApp   | develop | 0db86e3   | Merge branch 'feature/event-evaluation' into develop                        | Fusión de la rama feature/event-evaluation en develop                          | May 15, 2025  |
| TocaAqui-WebApp   | develop | c358de9   | fix(db): fixed                                                              | Corrección de errores en la base de datos                                       | May 15, 2025  |
| TocaAqui-WebApp   | develop | e2dbd5f   | Merge branch 'login' into develop                                           | Integración de la rama login en develop                                        | May 15, 2025  |
| TocaAqui-WebApp   | develop | bdb2cac   | refactor(dashboard): refactor dashboard bounded context                     | Refactorización de dashboard en su contexto delimitado                         | May 15, 2025  |
| TocaAqui-WebApp   | develop | 03028f4   | feat(event): added rider document upload function                           | Función para subir documentos de riders en eventos                             | May 15, 2025  |
| TocaAqui-WebApp   | develop | c0c85dc   | feat(evaluations): fixed the problem of adding evaluations to events        | Solución al problema de registro de evaluaciones en eventos                    | May 15, 2025  |
| TocaAqui-WebApp   | develop | 61c7b72   | fix(even-application): fixed post sign                                      | Corrección de errores en la firma de envíos de la aplicación de eventos         | May 15, 2025  |
| TocaAqui-WebApp   | develop | ff60507   | feat(schedule): added i18n                                                  | Se añade internacionalización (i18n) en schedule                               | May 15, 2025  |
| TocaAqui-WebApp   | develop | e5556d9   | fix(index): fix div id app                                                  | Corrección de ID de div en la aplicación                                       | May 15, 2025  |
| TocaAqui-WebApp   | develop | 5447a33   | feat(index): added comment                                                  | Comentarios añadidos en index para mejorar la legibilidad                      | May 15, 2025  |
| TocaAqui-WebApp   | develop | 3269301   | Fix rollup native module issue - clean install                              | Corrección de errores de módulos nativos en Rollup con reinstalación limpia    | May 15, 2025  |
| TocaAqui-WebApp   | develop | 68ba287   | feat(core): added pnpm                                                      | Integración de pnpm como gestor de paquetes                                    | May 15, 2025  |
| TocaAqui-WebApp   | develop | 0dfe5b0   | fix(node-modules): Fix rollup native module issue - reinstall node_modules  | Reinstalación de node_modules para corregir problemas con Rollup                | May 15, 2025  |
| TocaAqui-WebApp   | develop | ff4bfec   | fix(evaluation): fixed route                                                | Corrección de la ruta de evaluaciones                                          | May 15, 2025  |
| TocaAqui-WebApp   | develop | f43b1fe   | Merge branch 'feature/payment-processing' into develop                      | Fusión de la rama feature/payment-processing en develop                        | May 15, 2025  |
| TocaAqui-WebApp   | develop | 6a65d7a   | fix(evaluation): ixed                                                       | Corrección de errores en evaluaciones (typo "ixed")                            | May 15, 2025  |
| TocaAqui-WebApp   | develop | b9de9c4   | feat(db): updated database                                                  | Actualización de la base de datos                                              | May 15, 2025  |
| TocaAqui-WebApp   | develop | 4e2e810   | feat(event): updated calendar                                               | Actualización del componente de calendario de eventos                          | May 15, 2025  |
| TocaAqui-WebApp   | develop | a8163f5   | faet(events-card-schedule): updated                                         | Corrección y actualización del módulo card-schedule de eventos                 | May 15, 2025  |
| TocaAqui-WebApp   | develop | bd0086c   | feat(i18n): updated                                                         | Actualización de textos e internacionalización                                | May 15, 2025  |
| TocaAqui-WebApp   | develop | 92ebb40   | feat(dashboard): updated                                                    | Mejoras y actualizaciones visuales en el dashboard                             | May 15, 2025  |
TocaAqui-WebApp | develop | 85fa1bf | Merge branch 'feature/event-evaluation' into develop | Fusión de la rama feature/event-evaluation en develop | May 14, 2025
TocaAqui-WebApp | develop | 5029090 | feat:added changes to compile | Ajustes para compilar correctamente | May 14, 2025
TocaAqui-WebApp | develop | 29fc6c0 | feat:added evaluation content of bounded context | Agrega contenido de evaluación en bounded context | May 14, 2025
TocaAqui-WebApp | develop | 3b8a1b6 | feat(profile): added the profile section and his editing functionality | Sección de perfil y su funcionalidad de edición | May 14, 2025
TocaAqui-WebApp | develop | 207edb0 | Merge branch 'develop' into feature/payment-processing | Sincronización de develop en feature/payment-processing | May 14, 2025
TocaAqui-WebApp | develop | 64c8614 | fix(payment.service): fix http request | Corrección en el servicio de pagos para las solicitudes http | May 14, 2025
TocaAqui-WebApp | develop | 2694dc3 | feat(inxed.js): added new routes | Agrega nuevas rutas en inxed.js | May 14, 2025
TocaAqui-WebApp | develop | 043e0fc | feat(contrac-dialog): added and setup component | Configuración inicial del componente de diálogo de contrato | May 14, 2025
TocaAqui-WebApp | develop | 7b2a77a | feat(shared-components): added shared components | Se agregan componentes compartidos al proyecto | May 14, 2025
TocaAqui-WebApp | develop | 3530b69 | feat(event): added new information to the event | Se añade nueva información a los eventos | May 14, 2025
TocaAqui-WebApp | develop | 4aa8f85 | feat(payment): added payment bounded context | Implementación del bounded context para pagos | May 14, 2025
TocaAqui-WebApp | develop | 3473bc3 | refactor(shared-components): remove useless components | Eliminación de componentes innecesarios | May 14, 2025
TocaAqui-WebApp | develop | a6897b8 | feat(tracking): added tacking component | Se añade el componente de tracking | May 14, 2025
TocaAqui-WebApp | develop | 251cd88 | fix(dashboard): fdixed primevue components called | Corrección de llamadas a componentes de PrimeVue en dashboard | May 14, 2025
TocaAqui-WebApp | develop | d91b7af | feat(main.js): added new components | Nuevos componentes añadidos en main.js | May 14, 2025
TocaAqui-WebApp | develop | ce89e73 | fix(app): fixed components routes | Corrección de rutas de componentes en la app | May 14, 2025
TocaAqui-WebApp | develop | 6c90a14 | feat(db): added new endpoints | Nuevos endpoints añadidos a la base de datos | May 14, 2025
TocaAqui-WebApp | develop | d8f4327 | feat(i18n): added information to translate | Información adicional para traducción | May 14, 2025
TocaAqui-WebApp | develop | 48029d5 | feat:added some changes to compile project | Cambios para mejorar la compilación del proyecto | May 14, 2025
TocaAqui-WebApp | develop | 48c57d5 | Merge remote-tracking branch 'origin/develop' into develop | Actualización desde origin/develop | May 14, 2025
TocaAqui-WebApp | develop | 6fd29d6 | feat:added some changes to compile project | Mejoras para asegurar la compilación | May 14, 2025
TocaAqui-WebApp | develop | 460dc14 | feat(db.json):feat added events data | Datos de eventos añadidos en db.json | May 14, 2025
TocaAqui-WebApp | develop | eb5020c | Merge remote-tracking branch 'origin/feature/user-portal' into develop | Fusión de la rama feature/user-portal en develop | May 14, 2025
TocaAqui-WebApp | develop | 6f827b6 | feat(added): added dependencies | Se agregan dependencias al proyecto | May 14, 2025
TocaAqui-WebApp | develop | cdd14c0 | feat(payments): add the payments section of the artist | Añadida sección de pagos para artistas | May 14, 2025
TocaAqui-WebApp | develop | 38fe1c4 | feat(login): fixed the register section and fixed the styles | Corrección de la sección de registro y estilos | May 14, 2025
TocaAqui-WebApp | develop | cd549f8 | feat(i18n): added new information | Nuevos textos añadidos para internacionalización | May 14, 2025
TocaAqui-WebApp | develop | cab8872 | feat(dashboard): added events info to dashboard | Información de eventos añadida al dashboard | May 14, 2025
TocaAqui-WebApp | develop | 283deab | feat(event): added information and contract | Se añaden detalles e información contractual | May 14, 2025
TocaAqui-WebApp | develop | eaac858 | feat(db): added events application database | Base de datos para gestión de eventos añadida | May 14, 2025
TocaAqui-WebApp | develop | 59560d6 | feat(app): added pinia | Integración de Pinia para gestión de estado | May 14, 2025
TocaAqui-WebApp | develop | 2319bcf | fix(login): login fixed | Corrección de errores en el login | May 14, 2025
TocaAqui-WebApp | develop | 9279308 | fix(primevue-theme): fixed primevue theme | Ajustes en el tema visual de PrimeVue | May 14, 2025


#### 5.2.2.5. Execution Evidence for Sprint Review
Durante el Sprint 2, hemos desarrollado la primera versión de la aplicación web utilizando Vue.js, PrimeVue y JSON Server. A continuación, se presentan las User Stories implementadas y su evidencia:

| **ID** | **User Story** | **Evidencia en Aplicación** |
|:------:|:--------------:|:-----------------------------:|
| US07 | Registro como artista en la plataforma | Formulario de registro implementado con validaciones y selección de rol |
| US08 | Acceso al dashboard personalizado de artista | Panel principal con vista general de actividades y métricas |
| US09 | Búsqueda de eventos compatibles con mi perfil | Sistema de búsqueda con filtros por género y ubicación |
| US10 | Postulación rápida a un evento desde la plataforma | Proceso simplificado de postulación a eventos |
| US11 | Gestión y edición de mi perfil artístico | Editor de perfil con campos para biografía y multimedia |
| US33 | Visualización de pagos recibidos y pendientes | Panel detallado de estados de pagos y transacciones |
| US34 | Visualización de agenda de eventos | Calendario interactivo con eventos confirmados |
| US27 | Visualización de próximos eventos agendados | Widget de resumen de próximos shows en dashboard |
| US28 | Visualización de pagos pendientes desde el dashboard | Indicadores de pagos pendientes y estados |
| US29 | Acceso rápido a calificaciones recibidas | Sistema de visualización de reviews y ratings |

**Dashboard Principal del Artista**  
Panel centralizado que muestra las funcionalidades principales implementadas para los artistas.

![Aplicacion](../../assets/Aplicación-dashboard.png)

**Características implementadas:**

1. **Sistema de Autenticación**
   - Registro de usuarios con roles específicos
   - Login seguro con validaciones
   - Recuperación de contraseña

2. **Dashboard Personalizado**
   - Vista general de actividades
   - Métricas importantes
   - Accesos rápidos a funciones principales

3. **Gestión de Eventos**
   - Búsqueda avanzada de eventos
   - Filtros por género y ubicación
   - Sistema de postulaciones

4. **Sistema de Pagos**
   - Visualización de estados de pago
   - Historial de transacciones
   - Indicadores de pagos pendientes

5. **Agenda y Calendario**
   - Vista de eventos confirmados
   - Organización temporal de shows
   - Estados de contratos y pagos

6. **Perfiles y Evaluaciones**
   - Editor de perfil artístico
   - Sistema de calificaciones
   - Historial de reviews

**Stack Tecnológico Utilizado:**
- Frontend: Vue.js 3 + PrimeVue
- Backend Simulado: JSON Server
- Estilos: CSS personalizado
- Gestión de Estado: Vue Router + Pinia
- Despliegue: Vercel

#### 5.2.2.6. Services Documentation Evidence for Sprint Review

**API Endpoints implementados con JSON Server:**

```json
{
  "users": "/api/users",
  "events": "/api/events",
  "payments": "/api/payments",
  "evaluation": "/api/evaluation"
}
```

#### 5.2.2.7. Software Deployment Evidence for Sprint Review

Durante el Sprint 2, se realizó el despliegue de la Web Application utilizando **Vercel**.
![Aplicacion](../../assets/deploy-app.png)



- **Repositorio:** [Web Application](https://github.com/1ASI0730-2510-4370-G1-TocaAqui/Landing-Page)
- **URL de producción:** [https://tocaaqui-frontend.vercel.app/](https://tocaaqui-frontend.vercel.app/)
- **Branch desplegado:** `main`


![Aplicacion](../../assets/Aplicación-dashboard.png)

#### 5.2.2.8. Team Collaboration Insights during Sprint 2

Durante el Sprint 2, el equipo trabajó intensamente en la implementación de la aplicación web con Vue.js, PrimeVue y JSON Server. La carga de trabajo se concentró en la gestión de eventos, evaluaciones, pagos, así como en la integración de componentes y solución de errores. Se mantuvo la estrategia GitFlow con integración continua hacia la rama develop.

| **Integrante**              | **Commits** | **Líneas añadidas** | **Líneas eliminadas** | **Áreas de contribución principales**                                                                 |
|-----------------------------|-------------|--------------------:|----------------------:|-----------------------------------------------------------------------------------------------------|
| Oscar Antayhua Castillo     | 48          | 4100                | 1500                  | Gestión de eventos, pagos, i18n, dashboard, fixes de build, refactors y despliegue                    |
| Diego Cabrera (omele7)      | 12          | 800                 | 200                   | Evaluaciones, login, perfil, fixes en flujo de usuario y registro                                     |
| Fabrizzio Pereira (fabrizzioper) | 10     | 700                 | 100                   | Sidebar, rutas, navegación, estructura base de componentes                                            |
| JuanPaulLla                 | 4           | 300                 | 20                    | Ajustes menores en estilos, cambios de textos, fixes en layouts                                       |
| Asalreon520                 | 1           | 100                 | 0                     | Corrección en componente de pagos, ajustes mínimos                                                   |


Commits:

![team-collaborate-commits](../../assets/team-is-2.png)

![Contributors](/assets/contributors.png)


# 5.2.3 Sprint 3

#### 5.2.3.1. Spring Planning 3


#### 5.2.3.2. Aspect Leaders and Collaborators

En el Sprint 3, los principales aspectos considerados fueron la autenticación y gestión de usuarios (IAM), la gestión de eventos y postulaciones (Events), y la infraestructura compartida (Shared). A continuación, se presenta la matriz de liderazgo y colaboración del equipo para cada aspecto:

| Team Member (Last Name, First Name)      | GitHub Username         | IAM (Auth & Users) | Events (Gestión de eventos) | Shared (Infraestructura) |
|------------------------------------------|------------------------|--------------------|----------------------------|-------------------------|
| Pereira, Fabrizzio                       | fabrizzoper            | L                  | C                          | L                       |
| Antayhua Castillo, Oscar Josué           | OscarAntayhuaCastillo  | C                  | L                          | C                       |
| Su Caletti, Eddo                         | Asalreon520            | C                  | C                          | C                       |
| Llamccaya Arone, Juan Paul               | JuanPaulLla            | C                  | C                          | C                       |
| Cabrera, Diego                           | omele7                 | C                  | C                          | C                       |

L: Leader (Líder)  |  C: Collaborator (Colaborador)



#### 5.2.3.3. Sprint Backlog 3

**Objetivo del Sprint** 
El objetivo principal de este Sprint es consolidar y finalizar las funcionalidades clave del backend de la plataforma TocaAquí, permitiendo a artistas y promotores gestionar eventos, postulaciones, invitaciones y contratos digitales de manera segura y eficiente. Durante este Sprint, se han implementado y probado todos los flujos principales de registro, autenticación, gestión de eventos y notificaciones, asegurando una experiencia robusta y lista para integración con el frontend.

**Sprint Board**

![Sprint Board Screenshot](../../assets/Sprint3-Kan.png)
- **URL del Board:** [Enlace público a Jira](https://tocaqui.atlassian.net/jira/software/projects/KAN/list)

**Tabla de Control de Estado para el Sprint**

| User Story Id | User Story Title                                   | Task Id | Task Title                  | Description                                         | Estimation (Hours) | Assigned To         | Status |
|---------------|-----------------------------------------------------|---------|-----------------------------|-----------------------------------------------------|--------------------|---------------------|--------|
| US07          | Registro como artista en la plataforma              | T01     | Crear entidad Artista       | Implementar modelo y persistencia de artista        | 3                  | Fabrizzio Pereria   | Done   |
| US07          | Registro como artista en la plataforma              | T02     | Endpoint de registro        | Crear endpoint para registro de artista             | 2                  | Fabrizzio Pereria   | Done   |
| US14          | Registro como administrador de local                | T03     | Crear entidad Promotor      | Implementar modelo y persistencia de promotor       | 4                  | Fabrizzio Pereria   | Done   |
| US14          | Registro como administrador de local                | T04     | Endpoint de registro        | Crear endpoint para registro de promotor            | 2                  | Fabrizzio Pereria   | Done   |
| TS02          | Inicio de sesión mediante RESTful API               | T05     | Lógica de autenticación     | Implementar login y generación de token             | 3                  | Fabrizzio Pereria   | Done   |
| US16          | Publicación de eventos musicales                    | T06     | Crear entidad Evento        | Implementar modelo y persistencia de evento         | 2                  | Oscar Antayhua      | Done   |
| US16          | Publicación de eventos musicales                    | T07     | Endpoint de eventos         | Crear endpoint para crear y actualizar eventos      | 4                  | Oscar Antayhua      | Done   |
| US09          | Búsqueda de eventos compatibles con mi perfil       | T08     | Listar eventos              | Endpoint para listar eventos disponibles            | 2                  | Oscar Antayhua      | Done   |
| US10          | Postulación rápida a un evento desde la plataforma  | T09     | Crear entidad Postulación   | Implementar modelo y persistencia de postulación    | 3                  | Oscar Antayhua      | Done   |
| US10          | Postulación rápida a un evento desde la plataforma  | T10     | Endpoint de postulación     | Crear endpoint para postularse a eventos            | 2                  | Oscar Antayhua      | Done   |
| US17          | Revisión de postulaciones y selección de artista    | T11     | Listar postulaciones        | Endpoint para listar postulaciones de un evento     | 2                  | Oscar Antayhua      | Done   |
| US15          | Gestión de postulaciones e invitaciones             | T12     | Crear entidad Invitación    | Implementar modelo y persistencia de invitación     | 3                  | Oscar Antayhua      | Done   |
| US15          | Gestión de postulaciones e invitaciones             | T13     | Endpoint de invitaciones    | Crear endpoint para enviar invitaciones             | 2                  | Oscar Antayhua      | Done   |
| US12          | Subida y validación del rider técnico               | T14     | Crear entidad Contrato      | Implementar modelo y persistencia de contrato       | 4                  | Oscar Antayhua      | Done   |
| US12          | Subida y validación del rider técnico               | T15     | Endpoint de contratos       | Crear endpoint para firmar contratos digitales      | 2                  | Oscar Antayhua      | Done   |
| US18          | Validación del rider técnico enviado por artista    | T16     | Lógica de notificaciones    | Implementar lógica para notificar cambios de estado | 2                  | Fabrizzio Pereria   | Done   |
| US14          | Registro como administrador de local                | T17     | Endpoint de historial       | Crear endpoint para ver historial de eventos        | 3                  | Oscar Antayhua      | Done   |
| US15          | Gestión de postulaciones e invitaciones             | T18     | Lógica de invitaciones      | Implementar lógica para aceptar/rechazar invitaciones| 2                 | Oscar Antayhua      | Done   |
| US13          | Visualización de pagos recibidos y pendientes       | T19     | Endpoint de contratos firmados| Crear endpoint para listar contratos firmados    | 2                  | Oscar Antayhua      | Done   |
| TS01          | Registro de usuario (artista o promotor) a través de un RESTful API | T20     | Middleware de autenticación | Proteger endpoints con validación de token          | 3                  | Fabrizzio Pereria   | Done   |
| US08          | Acceso al dashboard personalizado de artista        | T21     | Endpoint de administración  | Crear endpoint para listar usuarios y eventos       | 2                  | Fabrizzio Pereria   | Done   |


#### 5.2.3.4. Development Evidence for Sprint Review

Durante el Sprint 3 se lograron avances significativos en la implementación del backend de la plataforma, completando los módulos de autenticación, gestión de usuarios, eventos, postulaciones, invitaciones y contratos digitales. A continuación, se presenta la evidencia de los commits realizados, que reflejan el trabajo colaborativo y el cumplimiento de los objetivos planteados para este ciclo.

| Repository                  | Branch                        | Commit Id | Commit Message           | Commit Message Body                | Commited on (Date) |
|-----------------------------|-------------------------------|-----------|-------------------------|------------------------------------|--------------------|
| CODENINJAS.TocaAqui.API/IAM | feature/IAM                   | 8298342   | merge (IAM)             | merged and fixed IAM bounded       | 2025-06-16         |
| CODENINJAS.TocaAqui.API     | develop, origin/develop       | 0accbce   | feat(program)           | fixed create database              | 2025-06-16         |
| CODENINJAS.TocaAqui.API     |                               | 795d8c0   | feat(program)           | fixed                              | 2025-06-16         |
| CODENINJAS.TocaAqui.API     | origin/feature/events         | 8298342   | merge (IAM)             | merged and fixed IAM bounded       | 2025-06-16         |
| CODENINJAS.TocaAqui.API     |                               | 26d8eee   | refactor(evets)         | refactored all bounded             | 2025-06-16         |
| CODENINJAS.TocaAqui.API     |                               | ae16b09   | refactor(events)        | refactored events bounded          | 2025-06-12         |
| CODENINJAS.TocaAqui.API     | origin/main, origin/HEAD, main| d070413   | refactor(http)          | refactored                         | 2025-06-11         |
| CODENINJAS.TocaAqui.API     |                               | 51c80ed   | feat(http)              | added http                         | 2025-06-11         |
| CODENINJAS.TocaAqui.API     |                               | 4eb111a   | feat(net8)              | eliminate unuse sln                | 2025-06-11         |
| CODENINJAS.TocaAqui.API     |                               | 4489ec7   | feat(sln)               | eliminate unuse sln                | 2025-06-11         |
| CODENINJAS.TocaAqui.API     |                               | 52cfd89   | refactor(name)          | named for the api refactored        | 2025-06-11         |

#### 5.2.3.5. Execution Evidence for Sprint Review

