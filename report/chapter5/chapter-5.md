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

   ![Gitflow](/assets/gitflow.png)


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
![Commits](/assets/commits.png)

Analiticas de Colaboración:
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

