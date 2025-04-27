---
title: "Universidad Peruana de Ciencias Aplicadas - Informe de Trabajo Final"
author: 
  - "Startup: CodeMinds"
  - "Producto: RutaKids"
  - "Profesor: Robles Fernández, Ivan"
  - "Integrantes:"
  - "Ortega Huaraca, Abel Angel: U20201B380"
  - "Vilchez Rios, Mateo Alejandro: U202210059"
  - "Ramos Rios, Belén del Rocio: U202216246"
  - "Herrera González, Luis Eduardo: U202218227"
  - "Vargas Revollé, Ariana: U20221A928"

date: "2025-01"
subject: "Markdown"
keywords: [Markdown, Report]
subtitle: "Diseño de Experimentos de Ingeniería de Software - 4429 - 1ASI0732"
lang: "es"
colorlinks: true
footer-left: "CodeMinds"
titlepage: true
titlepage-text-color: "FFFAFA"
titlepage-color: "DC143C"
titlepage-rule-height: 2
titlepage-rule-color: "FFFAFA"
titlepage-logo: "src/img/logo/logo-upc.pdf"
logo-width: 30mm
bibliography: src/informe/bibliografia/bibliografia.bib
csl: src/informe/bibliografia/apa.csl
book: true
classoption: oneside
code-block-font-size: \scriptsize
nocite: |
  @gothelf2021,
  @hernandez2018,
  @kasparova2022,
  @kalbach2016,
  @smith2020,
  @johnson2019,
  @brown2022,
  @igartua2019desconexion,
  @jiang2024pervasive,
  @kaspersky_privacy,
  @collave2024datos
header-includes:
- |
  ```{=latex} 
  \usepackage{morefloats}
  \usepackage{awesomebox}
  \usepackage{fontawesome5}
  \usepackage{tcolorbox}
  \usepackage{graphicx}
  \usepackage{parskip}
  \usepackage{xcolor}
  \usepackage{float} 
  \usepackage{longtable}
  \usepackage{array}
  \usepackage{lscape}
  \usepackage{multirow}
  \usepackage{geometry}
  \usepackage{booktabs}
 
  \newtcolorbox{info-box}{colback=cyan!5!white,arc=0pt,outer arc=0pt,colframe=cyan!60!black}
  \newtcolorbox{error-box}{colback=red!5!white,arc=0pt,outer arc=0pt,colframe=red!75!black}
  \newtcolorbox{norm-box}{colback=gray!5!white,arc=0pt,outer arc=0pt,colframe=gray!60!black}
  \newtcolorbox{warn-box}{colback=orange!5!white,arc=0pt,outer arc=0pt,colframe=orange!80!black}
  \newtcolorbox{attn-box}{colback=green!5!white,arc=0pt,outer arc=0pt,colframe=green!75!black}
  \newtcolorbox{code-box}{colback=pink!5!white,arc=0pt,outer arc=0pt,colframe=pink!80!black}
  \newtcolorbox{learn-box}{colback=blue!5!white,arc=0pt,outer arc=0pt,colframe=blue!40!black,title=\textbf{Objectives:}}
  \newtcolorbox{scenario-box}{colback=orange!5!white,arc=0pt,outer arc=0pt,colframe=orange!80!black,title=\textbf{Scenario:}}
  \newtcolorbox{outline-box}{colback=cyan!5!white,arc=0pt,outer arc=0pt,colframe=cyan!60!black,title=\textbf{Outline:}}
  \newtcolorbox{prereqs-box}{colback=red!5!white,arc=0pt,outer arc=0pt,colframe=red!60!black,title=\textbf{Prerequisites:}}
  \newtcolorbox{labtime-box}{colback=yellow!5!white,arc=0pt,outer arc=0pt,colframe=yellow!60!black,title=\textbf{Lab:}}
  \newcommand{\pandocbounded}[1]{#1} 
  ```
pandoc-latex-environment:
  tcolorbox: [box]
  info-box: [info]
  error-box: [error]
  norm-box: [norm]
  warn-box: [warn]
  attn-box: [attn]
  code-box: [code]
  learn-box: [learn]
  scenario-box: [scenario]
  outline-box: [outline]
  prereqs-box: [prereqs]
  labtime-box: [labtime]
  noteblock: [note]
  tipblock: [tip]
  warningblock: [warning]
  cautionblock: [caution]
  importantblock: [important]
---

# Capítulo V: Product Implementation

## Software Configuration Management.

En esta sección se establecen las bases para controlar y coordinar todos los elementos que componen nuestro sistema de transporte escolar, desde el entorno de desarrollo hasta el despliegue en producción. Recoge la configuración del entorno de desarrollo, donde se definen las versiones mínimas de IDE, SDK, librerías y contenedores que garantizan entornos homogéneos y fácilmente reproducibles; el control de versiones, con un modelo de ramas, políticas de merge y flujos de pull request que facilitan la colaboración y minimizan conflictos; la guía de estilo y convenciones de código, apoyada en linters y formateadores automáticos para asegurar la legibilidad y mantenibilidad del software; y, finalmente, la configuración de despliegue, a través de pipelines de CI/CD y scripts parametrizados que automatizan la provisión y actualización de los entornos de staging y producción de forma segura y confiable.

Con este enfoque integral de la Gestión de Configuración de Software (SCM), cada cambio queda registrado, validado y desplegado siguiendo un flujo de trabajo claro y trazable, lo que redunda en mayor estabilidad, transparencia y velocidad en la entrega de nuevas funcionalidades.

![Imagen extraída de Canva](src/img/cap5/capitulo5.png)

\newpage

### Software Development Environment Configuration.

En esta sección se detallan los productos de software que el equipo utilizará a lo largo de todo el ciclo de vida del sistema de transporte escolar. Para cada herramienta se especifica su nombre, su propósito dentro del proyecto y la forma de acceso, ya sea mediante la ruta de referencia de un servicio SaaS o el enlace de descarga para instalación local. Además, se cubren todas las fases de trabajo: gestión de proyectos, gestión de requisitos, diseño UX/UI del producto, desarrollo de software, pruebas, despliegue y documentación, garantizando que cada herramienta cumpla con las restricciones y estándares definidos por la institución.

#### Gestión de Proyectos y Requisitos

**UxPresia**  

Nos ayudará a capturar y priorizar requerimientos mediante mapas de historias de usuario, tableros de retrospectivas y definición de flujos de trabajo colaborativos.

![Imagen extraída de Canva](src/img/cap5/uxpressia-logo.png)

\newpage

#### Comunicación y Almacenamiento

**Discord**  

Nos ayudará a coordinar comunicación asíncrona y en tiempo real con canales temáticos, integrando notificaciones de repositorios y pipelines.

![Imagen extraída de Canva](src/img/cap5/discord-logo.png)

**Google Drive**  

Nos ayudará a centralizar y compartir recursos estáticos (imágenes, documentos de diseño, exportaciones) con control de versiones automático.

![Imagen extraída de Canva](src/img/cap5/drive-logo.png)

\newpage

#### Diseño UX/UI y Modelado

**Figma**  

Nos ayudará a prototipar y validar interfaces interactivas, facilitando la colaboración en diseño de pantallas móviles y web.

![Imagen extraída de Canva](src/img/cap5/figma-logo.png)

**Mermaid**  

Nos ayudará a generar diagramas (flujo, secuencia, entidad-relación) directamente desde texto, manteniendo la documentación arquitectónica actualizada.

![Imagen extraída de Canva](src/img/cap5/mermaid-logo.png)

\newpage

**Structurizr**  

Nos ayudará a crear modelos C4 de arquitectura de software, exportables para compartir vistas de contexto, contenedores y componentes.

![Imagen extraída de Canva](src/img/cap5/Structurizr-logo.png)

#### Entornos de Desarrollo e IDEs

**WebStorm**  

Nos ayudará a desarrollar el front-end con herramientas avanzadas de refactor, debug y pruebas de JavaScript/TypeScript.

![Imagen extraída de Canva](src/img/cap5/webstorm-logo.png)

\newpage

**IntelliJ IDEA**  

Nos ayudará a programar el backend en Java/Spring Boot con integración nativa de Maven/Gradle y soporte de debugging.

![Imagen extraída de Canva](src/img/cap5/intellij-logo.png)

**Visual Studio Code**  

Nos ayudará a editar scripts, archivos de configuración y pequeños microservicios con su vasta biblioteca de extensiones.

![Imagen extraída de Canva](src/img/cap5/vsc-logo.png)

\newpage

**Vim**  

Nos ayudará a realizar ediciones rápidas en servidor, escribir scripts o revisar logs directamente desde la terminal.

![Imagen extraída de Canva](src/img/cap5/vim-logo.png)

#### Frameworks y Plataformas de Desarrollo

**Spring Boot**  

Nos ayudará a estructurar y exponer servicios RESTful en Java, con arranque rápido, configuración mínima y soporte de seguridad.

![Imagen extraída de Canva](src/img/cap5/spring-logo.png)

\newpage

**Angular**  

Nos ayudará a construir la aplicación web de gestión con componentes modulables, inyección de dependencias y rutinas de pruebas.

![Imagen extraída de Canva](src/img/cap5/angular-logo.png)

**React**  

Nos ayudará a desarrollar la landing page y dashboards ligeros, aprovechando su ecosistema de hooks y librerías de visualización.

![Imagen extraída de Canva](src/img/cap5/react-logo.png)

\newpage

**Flutter**  

Nos ayudará a crear la aplicación móvil multiplataforma con un solo código, garantizando rendimiento nativo y consistencia UI.

![Imagen extraída de Canva](src/img/cap5/flutter-logo.png)

#### Integración Continua e Infraestructura

**Jenkins**  

Nos ayudará a orquestar pipelines de compilación, pruebas unitarias y despliegue automático mediante jobs parametrizados.

![Imagen extraída de Canva](src/img/cap5/Jenkins-logo.png)

\newpage

**AWS**  

Nos ayudará a desplegar microservicios, bases de datos y recursos en la nube con alta disponibilidad y escalabilidad.

![Imagen extraída de Canva](src/img/cap5/aws-logo.png)

**Vercel**  

Nos ayudará a alojar y distribuir la landing de React con despliegue automático en cada push al repositorio.

![Imagen extraída de Canva](src/img/cap5/vercel-logo.png)

\newpage

**Netlify**  

Nos ayudará a publicar y versionar la aplicación Angular con previews de pull request y funciones serverless integradas.

![Imagen extraída de Canva](src/img/cap5/netlify-logo.png)

#### Control de Versiones y Repositorios

**Git**  

Nos ayudará a versionar todo el código fuente y documentar cada cambio mediante commits atómicos y etiquetado semántico.

![Imagen extraída de Canva](src/img/cap5/git-logo.png)

\newpage

**GitHub**  

Nos ayudará a hospedar repositorios remotos, gestionar pull requests, proteger ramas y automatizar integraciones con acciones.

![Imagen extraída de Canva](src/img/cap5/github-logo.png)

#### Documentación y Formateo

**Pandoc**  

Nos ayudará a convertir documentos técnicos (Markdown, DOCX, LaTeX) entre formatos para distribuciones internas y reportes.

![Imagen extraída de Canva](src/img/cap5/pandoc-logo.png)

\newpage

**LaTeX**  

Nos ayudará a generar informes formales con alta calidad tipográfica y estructuras complejas (fórmulas, tablas, figuras).

![Imagen extraída de Canva](src/img/cap5/latex-logo.png)

\newpage

### Source Code Management.

En esta subsección de Source Code Management, el equipo establecerá los medios y el esquema de organización que aplicará para el seguimiento de todas las modificaciones al código fuente. Para ello se utilizará GitHub como plataforma y sistema de control de versiones. Se incluirá la URL de cada repositorio correspondiente a los diferentes productos del proyecto (Landing Page, Web Services y Frontend Web Applications). En el caso de los Web Services, el repositorio contendrá tanto el proyecto principal como los archivos de pruebas unitarias y de integración/aceptación.

Asimismo, se implementará el modelo GitFlow (ver “A successful Git branching model” de Vincent Driessen en Referencias) como workflow de control de versiones. Además de la rama principal (main), se creará una rama de desarrollo (develop). Cada nueva funcionalidad o corrección atravesará un branch propio siguiendo la convención feature/< descripción_corta >. De igual forma, se definirán convenciones para las ramas de liberación (release/< versión >) y de corrección urgente (hotfix/< versión >). Para el versionado de lanzamientos se aplicará Semantic Versioning 2.0.0 —p. ej. v1.2.0— y para los mensajes de commit se seguirá el estándar Conventional Commits (ver “Conventional Commits” en Referencias), asegurando claridad y trazabilidad en cada cambio.

\vspace{0.4cm}

![Artefacto creado con Mermaid](src/img/cap5/gitflow.png)

\newpage

### Source Code Style Guide & Conventions.

Para el desarrollo de nuestro sistema de transporte escolar, cada solución (Landing Page, Web Application, Mobile Application y Web Services) cuenta con su propio stack tecnológico, conjunto de herramientas, convenciones de idioma y estrategia de pruebas. A continuación se detalla cada una:

::: box  
**Landing Page**  
:::

- **Tecnologías**  

  - *React* con *HTML5*, *CSS3* y *JavaScript (ES6+)*.  

  - Librerías de estilo: *Tailwind CSS* y componentes de *shadcn/ui*.  

- **Herramientas**  

  - IDE: *Visual Studio Code* / *WebStorm*.  

  - Control de versiones: *Git* y *GitHub* (repositorio `landing-page`).  

  - Diseño visual y prototipos: *Figma*.  

  - Despliegue: *Vercel* con previews automáticas por Pull Request.  

- **Convenciones de idioma**  

  - Código y comentarios en **inglés**.  

  - Implementación de *i18n* para soporte de español.  

- **Pruebas y documentación**  

  - Pruebas de integración y E2E en *Playwright* con escenarios escritos en *Gherkin*.  

  - Documentación de componentes en *Storybook*.  

![Recurso extraido de Canva](src/img/cap5/landing-banner.png)

\newpage

::: box  
**Web Application (Admin Console)**  
:::

- **Tecnologías**  

  - *Angular* (TypeScript, RxJS, Angular CLI).  

  - Componentes modulares y formularios reactivos.  

- **Herramientas**  

  - IDE: *WebStorm* / *Visual Studio Code*.  
  
  - Control de versiones: *Git* y *GitHub* (repositorio `admin-web-app`).  

  - Diseño: *Figma* para wireframes y flujos de usuario.  

  - QA y pruebas: *Cypress* para tests E2E.  

  - Contenedorización local: *Docker Compose* (servicio web + base de datos de desarrollo).  

  - Hosting: *Netlify* para previews y producción.  

- **Convenciones de idioma**  

  - Código y mensajes en **inglés**.  

- **Pruebas y documentación**  

  - Historias de usuario descritas en *Gherkin* dentro del repositorio.  

  - Documentación de API REST consumidas a través de *Swagger UI*.  

![Recurso extraido de Canva](src/img/cap5/web-app-banner.png)

\newpage

::: box  
**Mobile Application (Tutor App)**  
:::

- **Tecnologías**  

  - *Flutter* (Dart) para iOS y Android con arquitectura *BLoC*.  

  - Plugins para geolocalización en tiempo real, notificaciones push y cámara.  

- **Herramientas**  

  - IDE: *Android Studio* / *Visual Studio Code*.  

  - Control de versiones: *Git* y *GitHub* (repositorio `mobile-app`).  

  - Diseño de pantallas: *Figma* + prototipos interactivos.  

  - Emulación y pruebas: *Android Emulator*, *iOS Simulator*.  

- **Convenciones de idioma**  

  - Código y recursos en **inglés**.  

  - Soporte multilenguaje con paquetes *flutter_localizations*.  

- **Pruebas y documentación**  

  - Tests unitarios y widget tests en *Flutter Test*, escenarios de usuario en *Gherkin*.  

  - Documentación de flujos en *Mermaid* incrustada en el README.  

![Recurso extraido de Canva](src/img/cap5/mobile-app-banner.png)

\newpage

::: box  
**Web Services (Backend)**  
:::

- **Tecnologías**  

  - **Auth Service:** *Java*, *Spring Boot*, *Spring Security* y *JWT*.  

  - **Temporary Email Service:** *Python*, *Flask* y librería *TempMail API*.  

  - Persistencia: *MySQL* / *PostgreSQL* con *Flyway* para migraciones.  

  - Mensajería interna con *RabbitMQ*.  

- **Herramientas**  

  - IDE: *IntelliJ IDEA* / *Visual Studio Code*.  

  - Control de versiones: *Git* y *GitHub* (repositorio `web-services`).  

  - Contenedores: *Docker* + *Docker Compose* para entornos locales.  

  - Documentación de API: *Swagger* (OpenAPI 3).  

  - Pruebas: *JUnit 5*, *Mockito* (Java) y *pytest* (Python).  

  - Orquestación CI/CD: *Jenkins* con pipelines definidas en Jenkinsfile.  

  - Monitoreo: *Prometheus* + *Grafana* (métricas de servicios).  

- **Convenciones de idioma**  

  - Código, variables y documentación en **inglés**.  

- **Pruebas y documentación**  

  - Pruebas unitarias, de integración y aceptación descritas en *Gherkin* y enlazadas a las historias de usuario.  

  - Diagrama C4 de la arquitectura en *Structurizr* y diagramas de secuencia en *Mermaid*.  

![Recurso extraido de Canva](src/img/cap5/web-service-banner.png)

\newpage

::: box  
**Convenciones de Commits**  
:::

Adoptamos **Conventional Commits v1.0.0**:
```text
<type>[scope opt]: <short description>
```
- **type:** feat, fix, docs, style, refactor, test, chore  

- **scope:** componente o módulo afectado  

- **description:** resumen breve y claro  

::: box  
**Versionado Semántico**  
:::

Seguimos **Semantic Versioning 2.0.0 (X.Y.Z)**:  

- **X (Major):** cambios incompatibles  

- **Y (Minor):** nuevas funcionalidades compatibles  

- **Z (Patch):** correcciones menores  

Las ramas y tags se nombran así:  

- Feature branches: `feature/<short-description>`  

- Release branches: `release/vX.Y.0`  

- Hotfix branches: `hotfix/vX.Y.Z`

\newpage

### Software Deployment Configuration.

Esta sección describe la configuración de despliegue utilizada para cada componente de la solución digital: Landing Page, Web Services y Aplicacion Web Frontend. A partir del código fuente en los repositorios, se detallan los pasos necesarios para su correcta publicación en entornos de desarrollo y producción.

::: warn
Para acceder al flujo de trabajo, haga click a la [URL](https://github.com/orgs/CodeMinds-Experimentos/repositories)
:::

**Desplegar** ***Landing Page***

* Clone el repositorio: *CodeMinds-LandingPage*

![Organización CodeMinds, imagen extraída de Github](src/img/cap5/landing-deploy-1.png){ width=80% }

* Abra el proyecto en su IDE de confianza y realice lo siguiente:

    - Instale las dependencias del proyecto web

    - Ejecute el proyecto con npm

![Organización CodeMinds, imagen extraída de Github](src/img/cap5/landing-deploy-2.png){ width=80% }

\newpage

**Desplegar** ***Web Application***

* Clone el repositorio: *RutaKids-WebApp*

![Organización CodeMinds, imagen extraída de Github](src/img/cap5/webapp-deploy-1.png){ width=80% }

* Abra el proyecto en su IDE de confianza y realice lo siguiente:

    - Instale las dependencias del proyecto web

    - Ejecute el proyecto con ng

![Organización CodeMinds, imagen extraída de Github](src/img/cap5/webapp-deploy-2.jpg){ width=80% }

\newpage

**Desplegar** ***Web Services***

* Clone el repositorio: *RutaKids-Micro-Servicios*

![Organización CodeMinds, imagen extraída de Github](src/img/cap5/webservices-deploy-1.png){ width=80% }

* Abra el proyecto en su IDE de confianza y realice lo siguiente:

    - Instale las dependencias del proyecto Spring

    - Para pruebas, ejecute cada servicio por separado

![Organización CodeMinds, imagen extraída de Github](src/img/cap5/webservices-deploy-2.jpg){ width=80% }

\newpage

## Product Implementation & Deployment.

### Sprint Backlogs.

***Sprint Backlog 1***

En este primer sprint, se estableció como prioridad el desarrollo de funcionalidades clave relacionadas con la landing page, el backend, la aplicacion web y la aplicación móvil de *RutaKids*. Estas tareas se organizaron en función de User Stories (Historias de Usuario) que representan los requisitos fundamentales para entregar una experiencia de usuario sólida y funcional.

En este Sprint Backlog se detalla los elementos de trabajo (Work Items) asignados a cada Historia de Usuario, así como el esfuerzo estimado en horas, los responsables y el estado de progreso de cada tarea. El enfoque de este sprint ha sido garantizar que tanto la landing page como el backend y las funcionalidades de la aplicación móvil estén bien estructurados y listos para futuras integraciones.

\begin{longtable}{|c|p{2.5cm}|p{1cm}|p{4cm}|p{2cm}|p{2cm}|p{1cm}|}
\hline
\textbf{ID} & \textbf{User Story} & \textbf{Work Item (WI)} & \textbf{Description} & \textbf{Estimation (Hours)} & \textbf{Assigned To} & \textbf{Status} \\ \hline
\multirow{3}{*}{US38} & \multirow{3}{*}{\parbox[t]{2.5cm}{Descubrimiento intuitivo \vspace{0.5cm}}} & WI01 & Diseño de la estructura HTML y navegación principal para facilitar el descubrimiento intuitivo en la landing page & 6h & Belén Ramos & Done \\ \cline{3-7} 
 &  & WI02 & Implementación de los elementos de navegación y estructura responsive & 4h & Belén Ramos & Done \\ \cline{3-7} 
 &  & WI03 & Pruebas de usabilidad para navegación y descubrimiento & 2h & Mateo Vílchez & Done \\ \hline
\multirow{2}{*}{US39} & \multirow{2}{*}{\parbox[t]{2.5cm}{Contenido informativo \vspace{0.5cm}}} & WI04 & Redacción de todo el contenido informativo para la landing page & 3h & Belén Ramos & Done \\ \cline{3-7} 
 &  & WI05 & Implementación del contenido en la landing page & 2h & Belén Ramos & Done \\ \hline
\multirow{2}{*}{US40} & \multirow{2}{*}{\parbox[t]{2.5cm}{Compatibilidad móvil \vspace{0.5cm}}} & WI06 & Desarrollo del diseño responsive para dispositivos móviles & 4h & Belén Ramos & Done \\ \cline{3-7} 
 &  & WI07 & Pruebas de responsividad en diferentes resoluciones & 3h & Belén Ramos & Done \\ \hline
\multirow{2}{*}{US41} & \multirow{2}{*}{\parbox[t]{2.5cm}{Formulario de contacto \vspace{0.5cm}}} & WI08 & Diseño e implementación del formulario de contacto & 5h & Belén Ramos & Done \\ \cline{3-7} 
 &  & WI09 & Validación de formulario de contacto & 2h & Mateo Vílchez & Done \\ \hline
\multirow{2}{*}{US42} & \multirow{2}{*}{\parbox[t]{2.5cm}{Contenido multimedia \vspace{0.5cm}}} & WI10 & Integración de imágenes, íconos y secciones visuales multimedia & 3h & Belén Ramos & Done \\ \cline{3-7} 
 &  & WI11 & Optimización de recursos multimedia para tiempos de carga más rápidos & 2h & Mateo Vílchez & Done \\ \hline
US43 & \parbox[t]{2.5cm}{Call-to-action claro \vspace{0.5cm}} & WI12 & Diseño y optimización de los botones de call-to-action (CTA) en la landing page & 3h & Mateo Vílchez & Done \\ \hline
\multirow{3}{*}{US32} & \multirow{3}{*}{\parbox[t]{2.5cm}{RESTful API Registro de usuario \vspace{0.5cm}}} & WI13 & Implementación de la API para el registro de usuario & 6h & Alex Avila & Done \\ \cline{3-7} 
 &  & WI14 & Añadir index para role seed en persistencia & 3h & Alex Avila & Done \\ \cline{3-7} 
 &  & WI15 & Middleware para manejo de excepciones & 4h & Alex Avila & Done \\ \hline
\multirow{2}{*}{US33} & \multirow{2}{*}{\parbox[t]{2.5cm}{RESTful API Inicio de sesión de usuario \vspace{0.5cm}}} & WI16 & Implementación de la API para inicio de sesión & 5h & Alex Avila & Done \\ \cline{3-7} 
 &  & WI17 & Implementación de pipeline de seguridad & 5h & Alex Avila & Done \\ \hline
\multirow{2}{*}{US34} & \multirow{2}{*}{\parbox[t]{2.5cm}{Autenticación basada en token JWT \vspace{0.5cm}}} & WI18 & Implementación de autenticación JWT en backend & 6h & Alex Avila & Done \\ \cline{3-7} 
 &  & WI19 & Configuración inicial de OpenAPI & 5h & Alex Avila & Done \\ \hline
US35 & \parbox[t]{2.5cm}{Recuperación de contraseña \vspace{0.5cm}} & WI20 & Implementación de perfiles en Spring Boot & 4h & Alex Avila & Done \\ \hline
\multirow{3}{*}{US36} & \multirow{3}{*}{\parbox[t]{2.5cm}{RESTful API Creación de sesiones \vspace{0.5cm}}} & WI21 & Implementación de la API para la creación de sesiones & 4h & Alex Avila & Done \\ \cline{3-7} 
 &  & WI22 & Creación de Dockerfile para build y compose & 5h & Alex Avila & Done \\ \cline{3-7} 
 &  & WI23 & Creación de Dockerfile para entorno de desarrollo & 4h & Alex Avila & Done \\ \hline
US37 & \parbox[t]{2.5cm}{Paginación y filtrado de resultados \vspace{0.5cm}} & WI24 & Implementación de la paginación y filtrado & 5h & Alex Avila & In-Process \\ \hline
\multirow{2}{*}{US01} & \multirow{2}{*}{\parbox[t]{2.5cm}{Registro de usuario \vspace{0.5cm}}} & WI025 & Diseño del mockup de la pantalla de registro de usuario & 4h & Abel Ortega & Done \\ \cline{3-7} 
 &  & WI26 & Implementación de la funcionalidad de registro en la app & 6h & Abel Ortega & In Process \\ \hline
\multirow{2}{*}{US02} & \multirow{2}{*}{\parbox[t]{2.5cm}{Confirmación de creación de cuenta \vspace{0.5cm}}} & WI27 & Diseño del correo de confirmación (mockup) & 3h & Abel Ortega & Done \\ \cline{3-7} 
 &  & WI28 & Implementación del inicio de sesión con Google y Facebook & 3h & Abel Ortega & In Process \\ \hline
\multirow{2}{*}{US03} & \multirow{2}{*}{\parbox[t]{2.5cm}{Historial de viajes \vspace{0.5cm}}} & WI29 & Diseño del mockup de la interfaz de historial de viajes & 3h & Abel Ortega & Done \\ \cline{3-7} 
 &  & WI30 & Implementación de la visualización del historial de viajes & 6h & Abel Ortega & To Do \\ \hline
US04 & \parbox[t]{2.5cm}{Eliminación de cuenta \vspace{0.5cm}} & WI31 & Diseño del mockup de la pantalla de eliminación de cuenta & 2h & Abel Ortega & Done \\ \hline
\multirow{2}{*}{US08} & \multirow{2}{*}{\parbox[t]{2.5cm}{Personalización del dominio de correo \vspace{0.5cm}}} & WI32 & Diseño del mockup para personalización del correo & 3h & Abel Ortega & Done \\ \cline{3-7} 
 &  & WI33 & Implementar la funcionalidad de personalización de correos & 5h & Abel Ortega & To-Do \\ \hline
US10 & \parbox[t]{2.5cm}{Redireccionar con el correo del conductor \vspace{0.5cm}} & WI34 & Diseño del mockup de la función redireccionar al correo & 3h & Abel Ortega & Done \\ \hline
\end{longtable}

\newpage

***Sprint Backlog 2***

En este segundo sprint, el foco ha sido completar e integrar funcionalidades críticas dentro de la aplicación web de RutaKids, así como afianzar la conexión con el backend. Las historias de usuario incluidas en este sprint cubren tareas relacionadas con la creación y gestión de correos, personalización de dominios, y optimización del proceso de generación y visualización de correos, asegurando que la experiencia de usuario sea intuitiva y eficiente.

Ademas, se ha priorizado garantizar una interacción fluida entre las interfaces móviles desarrolladas en Flutter y las APIs del backend, permitiendo a los usuarios gestionar correos temporales de manera más personalizada. Además, se incluyeron optimizaciones en la API y el manejo de estado en la aplicación móvil.

A continuación, se detallan las Historias de Usuario, los Work Items (WI) asignados, las horas estimadas, los responsables y el estado de cada tarea.

\begin{longtable}{|c|p{2.5cm}|p{1cm}|p{4cm}|p{2cm}|p{2cm}|p{1cm}|}
\hline
\textbf{ID} & \textbf{User Story} & \textbf{Work Item (WI)} & \textbf{Description} & \textbf{Estimation (Hours)} & \textbf{Assigned To} & \textbf{Status} \\ \hline

\multirow{3}{*}{US38} & \multirow{3}{*}{\parbox[t]{2.5cm}{Descubrimiento intuitivo}} & WI01 & Diseño de la estructura HTML y navegación principal para facilitar el descubrimiento intuitivo en la landing page & 6 & Belén Ramos & Done \\ \cline{3-7}
 &  & WI02 & Implementación de los elementos de navegación y estructura responsive & 4 & Belén Ramos & Done \\ \cline{3-7}
 &  & WI03 & Pruebas de usabilidad para navegación y descubrimiento & 2 & Mateo Vílchez & Done \\ \hline

\multirow{2}{*}{US39} & \multirow{2}{*}{\parbox[t]{2.5cm}{Contenido informativo}} & WI04 & Redacción de todo el contenido informativo para la landing page & 3 & Belén Ramos & Done \\ \cline{3-7}
 &  & WI05 & Implementación del contenido en la landing page & 2 & Belén Ramos & Done \\ \hline

\multirow{2}{*}{US40} & \multirow{2}{*}{\parbox[t]{2.5cm}{Compatibilidad móvil}} & WI06 & Desarrollo del diseño responsive para dispositivos móviles & 4 & Belén Ramos & Done \\ \cline{3-7}
 &  & WI07 & Pruebas de responsividad en diferentes resoluciones & 3 & Belén Ramos & Done \\ \hline

\multirow{2}{*}{US41} & \multirow{2}{*}{\parbox[t]{2.5cm}{Formulario de contacto}} & WI08 & Diseño e implementación del formulario de contacto & 5 & Belén Ramos & Done \\ \cline{3-7}
 &  & WI09 & Validación de formulario de contacto & 2 & Mateo Vílchez & Done \\ \hline

\multirow{2}{*}{US42} & \multirow{2}{*}{\parbox[t]{2.5cm}{Contenido multimedia}} & WI10 & Integración de imágenes, íconos y secciones visuales multimedia & 3 & Belén Ramos & Done \\ \cline{3-7}
 &  & WI11 & Optimización de recursos multimedia para tiempos de carga más rápidos & 2 & Mateo Vílchez & Done \\ \hline

US43 & \parbox[t]{2.5cm}{Call-to-action claro} & WI12 & Diseño y optimización de los botones de call-to-action (CTA) en la landing page & 3 & Mateo Vílchez & Done \\ \hline

\multirow{3}{*}{US32} & \multirow{3}{*}{\parbox[t]{2.5cm}{RESTful API Registro de usuario}} & WI13 & Implementación de la API para el registro de usuario & 6 & Alex Avila & Done \\ \cline{3-7}
 &  & WI14 & Añadir index para role seed en persistencia & 3 & Alex Avila & Done \\ \cline{3-7}
 &  & WI15 & Middleware para manejo de excepciones & 4 & Alex Avila & Done \\ \hline

\newpage

\multirow{2}{*}{US33} & \multirow{2}{*}{\parbox[t]{2.5cm}{RESTful API Inicio de sesión de usuario}} & WI16 & Implementación de la API para inicio de sesión & 5 & Alex Avila & Done \\ \cline{3-7}
 &  & WI17 & Implementación de pipeline de seguridad & 5 & Alex Avila & Done \\ \hline

\multirow{2}{*}{US34} & \multirow{2}{*}{\parbox[t]{2.5cm}{Autenticación basada en token JWT}} & WI18 & Implementación de autenticación JWT en backend & 6 & Alex Avila & Done \\ \cline{3-7}
 &  & WI19 & Configuración inicial de OpenAPI & 5 & Alex Avila & Done \\ \hline

US35 & \parbox[t]{2.5cm}{Recuperación de contraseña} & WI20 & Implementación de perfiles en Spring Boot & 4 & Alex Avila & Done \\ \hline

\multirow{3}{*}{US36} & \multirow{3}{*}{\parbox[t]{2.5cm}{RESTful API Creación de sesiones}} & WI21 & Implementación de la API para la creación de sesiones & 4 & Alex Avila & Done \\ \cline{3-7}
 &  & WI22 & Creación de Dockerfile para build y compose & 5 & Alex Avila & Done \\ \cline{3-7}
 &  & WI23 & Creación de Dockerfile para entorno de desarrollo & 4 & Alex Avila & Done \\ \hline

US37 & \parbox[t]{2.5cm}{Paginación y filtrado de resultados} & WI24 & Implementación de la paginación y filtrado & 5 & Alex Avila & In Process \\ \hline

\multirow{2}{*}{US05} & \multirow{2}{*}{\parbox[t]{2.5cm}{Generación de correo temporal con un clic}} & WI25 & Implementación del recurso POST para generar un correo temporal & 5 & Abel Ortega & Done \\ \cline{3-7}
 &  & WI26 & Implementación del recurso GET para obtener la lista de correos temporales generados & 4 & Abel Ortega & Done \\ \hline

US06 & \parbox[t]{2.5cm}{Duración específica del correo temporal} & WI27 & Implementación del recurso PUT para actualizar la duración específica del correo temporal & 4 & Abel Ortega & Done \\ \hline

US07 & \parbox[t]{2.5cm}{Confirmación visual de creación de correo} & WI28 & Implementación del recurso GET para confirmar la creación visual del correo temporal & 3 & Abel Ortega & Done \\ \hline

US08 & \parbox[t]{2.5cm}{Personalización del dominio del correo temporal} & WI29 & Implementación del recurso PUT para personalizar el dominio del correo temporal & 5 & Abel Ortega & Done \\ \hline

\multirow{4}{*}{US01} & \multirow{4}{*}{\parbox[t]{2.5cm}{Registro de usuario}} & WI30 & Diseño de la pantalla de registro utilizando Jetpack Compose & 6 & Alex Avila & Done \\ \cline{3-7}
 &  & WI02 & Conectar la pantalla de registro con la API & 5 & Alex Avila & Done \\ \cline{3-7}
 &  & WI03 & Implementar validación de campos en la pantalla de registro & 4 & Alex Avila & Done \\ \cline{3-7}
 &  & WI04 & Pruebas de usabilidad para el registro de usuario & 3 & Alex Avila & Done \\ \hline

\multirow{3}{*}{US02} & \multirow{3}{*}{\parbox[t]{2.5cm}{Confirmación de creación de cuenta}} & WI05 & Implementar la funcionalidad de confirmación de cuenta con la API & 5 & Alex Avila & Done \\ \cline{3-7}
 &  & WI31 & Diseño de la pantalla de confirmación de cuenta en Compose & 4 & Alex Avila & Done \\ \cline{3-7}
 &  & WI32 & Pruebas para la confirmación de cuenta & 2 & Alex Avila & Done \\ \hline

\multirow{2}{*}{US03} & \multirow{2}{*}{\parbox[t]{2.5cm}{Verificación de cuenta}} & WI33 & Conectar la verificación de cuenta con la API & 4 & Alex Avila & Done \\ \cline{3-7}
 &  & WI34 & Implementar la pantalla de verificación de cuenta & 3 & Alex Avila & Done \\ \hline

\multirow{2}{*}{US04} & \multirow{2}{*}{\parbox[t]{2.5cm}{Inicio de sesión de cuenta}} & WI35 & Crear la pantalla de inicio de sesión en Compose & 5 & Alex Avila & Done \\ \cline{3-7}
 &  & WI36 & Conectar la pantalla de inicio de sesión con la API & 5 & Alex Avila & Done \\ \hline

\multirow{3}{*}{US05} & \multirow{3}{*}{\parbox[t]{2.5cm}{Generación de correo temporal con un clic}} & WI37 & Diseño de la pantalla de generación de correos temporales & 4 & Abel Ortega & Done \\ \cline{3-7}
 &  & WI38 & Implementar la funcionalidad de generación de correos con un clic & 5 & Abel Ortega & Done \\ \cline{3-7}
 &  & WI39 & Pruebas de generación de correos temporales & 2 & Abel Ortega & Done \\ \hline

\multirow{2}{*}{US06} & \multirow{2}{*}{\parbox[t]{2.5cm}{Duración específica del correo temporal}} & WI40 & Implementar opción para seleccionar duración del correo & 4 & Abel Ortega & Done \\ \cline{3-7}
 &  & WI41 & Conectar la opción de duración con la API & 4 & Abel Ortega & Done \\ \hline

\multirow{2}{*}{US07} & \multirow{2}{*}{\parbox[t]{2.5cm}{Confirmación visual de creación de correo}} & WI42 & Añadir confirmación visual en la pantalla de generación de correos & 3 & Abel Ortega & Done \\ \cline{3-7}
 &  & WI43 & Pruebas de confirmación visual & 2 & Abel Ortega & Done \\ \hline

\multirow{2}{*}{US09} & \multirow{2}{*}{\parbox[t]{2.5cm}{Generación múltiple de correos temporales}} & WI44 & Implementar la opción para generar múltiples correos & 4 & Abel Ortega & Done \\ \cline{3-7}
 &  & WI45 & Pruebas para la generación de múltiples correos & 3 & Abel Ortega & Done \\ \hline

\multirow{2}{*}{US10} & \multirow{2}{*}{\parbox[t]{2.5cm}{Copiar correo temporal al portapapeles}} & WI46 & Implementar la funcionalidad para copiar correos al portapapeles & 4 & Abel Ortega & Done \\ \cline{3-7}
 &  & WI47 & Pruebas para la funcionalidad de copiar al portapapeles & 2 & Abel Ortega & Done \\ \hline

\multirow{3}{*}{US11} & \multirow{3}{*}{\parbox[t]{2.5cm}{Visualización de correos temporales activos}} & WI48 & Diseño de la interfaz de visualización de correos activos & 5 & Abel Ortega & Done \\ \cline{3-7}
 &  & WI49 & Implementación de la funcionalidad de visualización de correos activos & 6 & Abel Ortega & Done \\ \cline{3-7}
 &  & WI50 & Pruebas para la visualización de correos activos & 2 & Abel Ortega & Done \\ \hline

\multirow{2}{*}{US13} & \multirow{2}{*}{\parbox[t]{2.5cm}{Proceso de generación rápido y fluido}} & WI51 & Implementar un proceso rápido de generación de correos temporales & 4 & Abel Ortega & Done \\ \cline{3-7}
 &  & WI52 & Pruebas del proceso rápido de generación & 2 & Abel Ortega & Done \\ \hline


\multirow{2}{*}{US15} & \multirow{2}{*}{\parbox[t]{2.5cm}{Acceso a bandeja de entrada de correos temporales}} & WI53 & Implementar la funcionalidad de acceso a la bandeja de entrada & 5 & Abel Ortega & Done \\ \cline{3-7}
 &  & WI54 & Pruebas para el acceso a la bandeja de entrada & 2 & Abel Ortega & Done \\ \hline

\multirow{2}{*}{US16} & \multirow{2}{*}{\parbox[t]{2.5cm}{Visualización de correos recibidos}} & WI55 & Implementar la funcionalidad de visualización de correos recibidos & 5 & Abel Ortega & Done \\ \cline{3-7}
 &  & WI56 & Pruebas para la visualización de correos recibidos & 2 & Abel Ortega & Done \\ \hline

\multirow{9}{*}{US32} & \multirow{9}{*}{\parbox[t]{2.5cm}{Manejo de consentimiento de usuario}} & WI57 & Implementación del manejo de estado del consentimiento de usuario en la app móvil & 3h & Belen Ramos & Done \\ \cline{3-7}
 &  & WI58 & Implementación de la lógica para mostrar/ocultar mensajes según aceptación del consentimiento & 3h & Belen Ramos & Done \\ \cline{3-7}
 &  & WI59 & Integración de la funcionalidad de "I Agree" con el flujo de consentimiento y su persistencia & 3h & Belen Ramos & Done \\ \cline{3-7}
 &  & WI60 & Implementación de la navegación entre la pantalla de consentimiento y la pantalla principal & 2h & Mateo Vilchez & In Process \\ \cline{3-7}
 &  & WI70 & Implementación del click handler para navegar a la sección completa de "Privacy Policy" & 2h & Belen Ramos & Done \\ \cline{3-7}
 &  & WI71 & Pruebas unitarias para el componente de consentimiento y verificación de aceptación & 3h & Mateo Vilchez & To Do \\ \cline{3-7}
 &  & WI72 & Manejo de estados para permitir o deshabilitar interacciones con botones según el consentimiento & 2h & Mateo Vilchez & Done \\ \cline{3-7}
 &  & WI73 & Pruebas de usabilidad para asegurar el flujo correcto en la sección de "Privacy Policy" & 2h & Mateo Vilchez & In Process \\ \cline{3-7}
 &  & WI74 & Validación de errores y feedback visual al usuario en caso de fallos en el consentimiento & 3h & Belen Ramos & Done \\ \hline

\end{longtable}

\newpage

**Gestión de los Sprint (Tablero Kanban):**

Para mejorar la gestión y seguimiento de las tareas de este sprint, se implementó un tablero Kanban.
Este tablero permite visualizar claramente los elementos clave a desarrollar, asignar responsables
para cada tarea, y utilizar etiquetas (labels) que categorizan los Issues de forma precisa. Además, los
Milestones fueron utilizados estratégicamente para planificar las fechas de entrega y gestionar los
entregables, facilitando un control eficiente del progreso del proyecto.

![Imagen extraída de Canva](src/img/cap5/gestion-sprints-kanban.png)

\newpage

### Implemented Landing Page Evidence

::: warn
Para acceder al repositorio de este proyecto, haga click a la [URL](https://github.com/CodeMinds-Experimentos/CodeMinds-RutaKids-LandingPage)
:::

**Captura del repositorio:**

![Organización CodeMinds, imagen extraída de Github](src/img/cap5/landing-deploy-1.png){ width=80% }

**Landing Page en funcionamiento:**

![Organización CodeMinds, imagen extraída de Github](src/img/cap5/landing-deploy-2.png){ width=80% }

\newpage

### Implemented Frontend-Web Application Evidence

::: warn
Para acceder al repositorio de este proyecto, haga click a la [URL](https://github.com/CodeMinds-Experimentos/RutaKids-WebApp)
:::

**Captura del repositorio:**

![Organización CodeMinds, imagen extraída de Github](src/img/cap5/webapp-deploy-1.png){ width=80% }

**Web Application en funcionamiento:**

![Organización CodeMinds, imagen extraída de Github](src/img/cap5/webapp-deploy-2.jpg){ width=80% }

\newpage

### Implemented Native-Mobile Application Evidence

::: warn
Para acceder al repositorio de este proyecto, haga click a la [URL](https://www.figma.com/design/ph6aTjM4mzxkNic0Hk4VLX/RutaKids?node-id=275-3006&t=aZ58NPtaowKWvMte-1)
:::

**Captura del figma:**

![Organización CodeMinds, imagen extraída de Figma](src/img/cap5/mobile-app-figma.png){ width=80% }

**Mobile Application en mockup:**

![Organización CodeMinds, imagen extraída de Figma](src/img/cap5/mobile-app-figma-view.png){ width=50% }

\newpage

### Implemented RESTful API and/or Serverless Backend Evidence

::: warn
Para acceder al repositorio de este proyecto, haga click a la [URL](https://github.com/LlantaTech/ruta-kids-microservicios)
:::

**Captura del repositorio:**

![Organización CodeMinds, imagen extraída de Github](src/img/cap5/webservices-deploy-1.png){ width=80% }

**Web Service Application en funcionamiento:**

![Organización CodeMinds, imagen extraída de Github](src/img/cap5/webservices-deploy-2.jpg){ width=80% }

\newpage

### RESTful API documentation

::: warn
Para acceder al repositorio de este proyecto, haga click a la [URL](https://github.com/LlantaTech/ruta-kids-microservicios)
:::

**Captura del repositorio:**

![Organización CodeMinds, imagen extraída de Github](src/img/cap5/webservices-doc.png)

\newpage

### Team Collaboration Insights

::: warn
Para acceder los insights de este proyecto, haga click a la [URL](https://github.com/CodeMinds-Experimentos/CodeMinds-Report/pulse)
:::

**Tablero Kanban:**

![Organización CodeMinds, imagen extraída de Github](src/img/cap5/insights-kanban-todo-1.png){ width=80% }

**Kanban List:**

![Organización CodeMinds, imagen extraída de Github](src/img/cap5/insights-kanban-list-1.png){ width=80% }

**Network Graph:**

![Organización CodeMinds, imagen extraída de Github](src/img/cap5/insights-network-graph-1.png){ width=80% }

**Traffic Map:**

![Organización CodeMinds, imagen extraída de Github](src/img/cap5/insights-traffic-1.png){ width=80% }

\newpage

## Video *About-the-Product.*

::: warn
Para acceder al video  about the product, haga click en la [URL](https://upcedupe-my.sharepoint.com/:v:/g/personal/u202210059_upc_edu_pe/EWO4I1TkuVdCnZbW0aswNssBgLRcrsjVJa2rl-7IQv-QoA?e=vw70w7&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D)
:::
