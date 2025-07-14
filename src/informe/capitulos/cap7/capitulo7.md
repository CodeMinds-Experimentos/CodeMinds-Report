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
block-headings: true
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

# Capítulo VII: DevOps Practices

La adopción de prácticas DevOps ha revolucionado el ciclo de vida del desarrollo de software al integrar de manera fluida las etapas de desarrollo, prueba, entrega y operación en un flujo continuo y automatizado. Este capítulo aborda las prácticas fundamentales de DevOps implementadas en el proyecto, centradas en los principios de Integración Continua (CI), Entrega Continua (CD) y Despliegue Continuo (Continuous Deployment).

Se describen las herramientas seleccionadas, las estrategias aplicadas en cada fase del pipeline, y la manera en que estas prácticas han contribuido a mejorar la eficiencia, la calidad del producto y la reducción del tiempo de entrega. Asimismo, se detallan los componentes de los pipelines de integración, entrega y despliegue, incluyendo la automatización de pruebas, validaciones previas al despliegue y controles en ambientes de staging y producción.

La implementación de estas prácticas ha sido clave para garantizar una entrega rápida, confiable y segura del software, permitiendo a los equipos responder ágilmente a cambios y retroalimentación sin comprometer la estabilidad del sistema.

![Recurso extraído de Canva](src/img/cap7/devops-practices.png)

\newpage

## Continuous Integration

La integración continua (CI, por sus siglas en inglés) es una práctica fundamental dentro del enfoque DevOps que tiene como objetivo automatizar el proceso de integración de cambios en el código fuente. Esta metodología permite validar cada actualización mediante compilaciones automáticas y la ejecución de pruebas, con el fin de detectar errores de forma temprana, minimizar conflictos de integración y garantizar la estabilidad del sistema a lo largo del desarrollo.

En el contexto de este proyecto, la CI se implementa con la finalidad de asegurar que cada módulo del sistema —tanto en el frontend desarrollado en Angular como en el backend— se mantenga funcional, probado y preparado para su eventual despliegue en diferentes entornos. Esto permite que los equipos puedan colaborar de manera eficiente, integrando sus contribuciones de forma frecuente y con un menor riesgo de introducir errores en la base de código compartida.

Actualmente, se emplea GitHub como sistema de control de versiones, y se han comenzado a aplicar flujos automatizados mediante GitHub Actions, centrados en tareas como la generación y validación de la documentación técnica del frontend. Esta automatización no solo garantiza consistencia en la documentación, sino que sienta las bases para una mayor cobertura en futuras etapas del pipeline.

A medida que el proyecto avanza, se tiene previsto extender la infraestructura de CI para incluir pruebas unitarias y de integración, análisis estático de código, verificación de convenciones de estilo y despliegues automáticos en entornos de desarrollo. Estas mejoras fortalecerán la calidad del software y facilitarán la entrega continua de valor al usuario final, alineándose con los principios de entrega ágil y mejora continua.

![Recurso extraído de Canva](src/img/cap7/integracion-continua.png)

\newpage

### Tools and Practices.

::: info
***Angular***
:::

Para el frontend Angular, se ha adoptado una arquitectura modular con componentes standalone bajo Angular 17. Las prácticas de integración continua (CI) se gestionan a través de GitHub, utilizando GitHub Actions para automatizar la generación de documentación con Compodoc.

Si bien la infraestructura completa de CI/CD aún está en planificación (con miras al despliegue en un dominio propio), actualmente se aplican las siguientes prácticas:

- Uso de *GitHub como sistema de control de versiones*, siguiendo un flujo de trabajo basado en ramas (`git flow`).

- La rama `main` se mantiene como fuente principal para despliegues.

- No se permite realizar merge a `main` si existen errores en pruebas o compilación.

- Se ejecutan pruebas unitarias mediante `ng test` con Karma.

- Se genera documentación automáticamente con *Compodoc* usando GitHub Actions.

En futuras fases de producción, se espera incorporar un pipeline más robusto que incluya:

- Ejecución automatizada de pruebas, lint y build con GitHub Actions.

- Despliegues automáticos desde `main`.

- Configuración de entornos diferenciados (`development`, `staging`, `production`).


::: info
***Spring Boot***
:::

Para el backend desarrollado con Spring Boot, se ha adoptado una arquitectura en capas (Controller, Service, Repository) con un diseño modular por funcionalidad. Las prácticas de integración continua (CI) se gestionan a través de GitHub, utilizando GitHub Actions para automatizar la ejecución de pruebas y la generación de documentación de la API con Springdoc-openapi.

Si bien la infraestructura completa de CI/CD aún está en planificación (con miras al despliegue en un servidor en la nube o una plataforma de contenedores), actualmente se aplican las siguientes prácticas:

-   Uso de **GitHub como sistema de control de versiones**, siguiendo un flujo de trabajo basado en ramas (`git flow`).

-   La rama `main` se mantiene como la fuente principal para despliegues.

-   No se permite realizar un merge a `main` si existen errores en las pruebas o en la construcción del artefacto (build).

-   Se ejecutan pruebas unitarias y de integración mediante `mvn test` (o `./gradlew test`), utilizando **JUnit 5** y **Mockito**.

-   Se genera documentación de la API automáticamente con **Springdoc-openapi** usando GitHub Actions, publicando la especificación para los consumidores de la API.

En futuras fases de producción, se espera incorporar un pipeline más robusto que incluya:

-   Ejecución automatizada de pruebas, análisis de código estático (lint con Checkstyle) y construcción del artefacto (`.jar`) con GitHub Actions.

-   Containerización de la aplicación con **Docker** y despliegues automáticos de la imagen desde `main` a un registro de contenedores.

-   Uso de **Spring Profiles** para gestionar configuraciones diferenciadas para los entornos de `development`, `staging` y `production`.

\newpage

### Build & Test Suite Pipeline Components.

::: info
***Angular***
:::

Aunque el pipeline completo aún está en desarrollo, se ha definido una estructura base que contempla las siguientes etapas para el frontend Angular:

**Etapas previstas del pipeline de CI para Angular:**

\begin{longtable}{|p{3cm}|p{5cm}|p{6cm}|}
\hline
\textbf{Etapa} & \textbf{Descripción} & \textbf{Comando} \\
\hline
\endfirsthead

\hline
\textbf{Etapa} & \textbf{Descripción} & \textbf{Comando} \\
\hline
\endhead

Install & Instalación de dependencias & \texttt{npm ci} \\
\hline
Test & Ejecución de pruebas unitarias con Karma & \texttt{ng test --watch=false --browsers=ChromeHeadless} \\
\hline
Build & Compilación del proyecto en modo producción & \texttt{ng build --configuration=production} \\
\hline
Docs & Generación de documentación con Compodoc & \texttt{npx compodoc -p tsconfig.app.json -s} \\
\hline

\end{longtable}

**Reglas de activación:**

- El pipeline se activa ante push o pull request a la rama `main`.

- Si alguna etapa falla (build o test), se bloquea el merge automáticamente.

**Mejoras futuras previstas:**

- Integración de `lint` con ESLint (`ng lint`).

- Generación de badges y reporte de cobertura.

- Separación de flujos para despliegue en `staging` y `producción`.

Esta estructura asegura que los módulos Angular sean correctamente validados antes de su integración, manteniendo la estabilidad y calidad de la aplicación.

\newpage

**Diagrama del pipeline CI/CD para Angular**

![Artefacto creado en Diagrams - Build & Test Suite Pipeline](src/img/cap7/build_test_suite_pipeline.png)

\newpage


::: info
***Spring Boot***
:::

Aunque el pipeline completo aún está en desarrollo, se ha definido una estructura base que contempla las siguientes etapas para el backend de Spring Boot:

**Etapas previstas del pipeline de CI para Spring Boot:**

\begin{longtable}{|p{3cm}|p{5cm}|p{6cm}|}
\hline
\textbf{Etapa} & \textbf{Descripción} & \textbf{Comando (Maven)} \\
\hline
\endfirsthead

\hline
\textbf{Etapa} & \textbf{Descripción} & \textbf{Comando (Maven)} \\
\hline
\endhead

Build & Compila el código fuente Java y procesa los recursos (incluye descarga de dependencias). & \texttt{mvn compile} \\
\hline
Test & Ejecución de pruebas unitarias y de integración con JUnit 5 y Mockito. & \texttt{mvn test} \\
\hline
Package & Empaqueta la aplicación compilada en un artefacto ejecutable (.jar). & \texttt{mvn package} \\
\hline
Docs & Generación de la documentación de la API a través de la especificación OpenAPI (Swagger). & Integrado en la fase de package o mediante un plugin específico. \\
\hline

\end{longtable}

**Reglas de activación:**

-   El pipeline se activa ante `push` o `pull request` a la rama `main`.
-   Si alguna etapa falla (build o test), se bloquea el merge automáticamente.

**Mejoras futuras previstas:**

-   Integración de análisis de código estático con **Checkstyle** o **SonarQube**.
-   Generación de badges y reporte de cobertura de código con **JaCoCo**.
-   Separación de flujos de despliegue para `staging` y `producción` utilizando **Spring Profiles**.

Esta estructura asegura que los servicios del backend sean correctamente validados antes de su integración, manteniendo la estabilidad, seguridad y calidad de la API.

\newpage

**Diagrama del pipeline CI/CD para Spring Boot**

![Artefacto creado en Diagrams - Build & Test Suite Pipeline](src/img/cap7/build_test_suite_pipeline2.png)


\newpage

## Continuous Delivery

La entrega continua (CD, por sus siglas en inglés) es una práctica clave dentro del enfoque DevOps que representa la evolución natural de la integración continua. Esta metodología busca garantizar que cualquier versión del sistema que haya superado las pruebas automatizadas pueda ser entregada de forma automática y segura a entornos de prueba intermedios, como staging o QA, sin intervención manual significativa. El objetivo principal es reducir el tiempo que transcurre desde que un cambio es confirmado en el repositorio hasta que puede ser validado en un entorno que simula fielmente la producción.

En el contexto de este proyecto, la entrega continua se aplica principalmente sobre el frontend desarrollado en Angular, permitiendo validar visual y funcionalmente los cambios antes de realizar el despliegue final. Esta práctica contribuye significativamente a la detección temprana de errores, mejora la colaboración entre equipos y fortalece la calidad del software entregado al usuario final.

Actualmente, si bien el proyecto aún se encuentra en una fase temprana de automatización completa del proceso de despliegue, se ha definido una arquitectura de trabajo basada en ramas estructuradas como develop y main. Esta organización permite implementar un flujo de entrega escalonado y controlado. A nivel técnico, se ha planteado un pipeline automatizado que incluye la compilación en modo servidor (Server-Side Rendering, SSR), ejecución de pruebas end-to-end mediante la herramienta Cypress, verificación del estado del sistema y posterior despliegue mediante transferencia segura (SSH) a servidores externos de validación.

A medida que el sistema evolucione y los pipelines se refuercen, se espera incorporar etapas adicionales que incluyan validaciones de accesibilidad, control de versiones semántico, análisis de seguridad automatizado y notificaciones integradas con herramientas colaborativas, todo con el propósito de garantizar entregas frecuentes, confiables y sin fricciones.

![Recurso extraído de Canva](src/img/cap7/continuous-delivery.png)

\newpage

### Tools and Practices.

::: info
***Angular***
:::

Para la futura implementación de entrega continua en Angular, se planea el siguiente conjunto de herramientas y buenas prácticas:

- **GitHub Actions** como orquestador de pipelines CI/CD.

- **Flujo de ramas GitFlow**, donde `develop` representa el entorno staging.

- **Angular SSR (`npm run build:ssr`)** para construir versiones renderizadas del lado del servidor.

- **Pruebas automatizadas** con:

  - `ng test` para pruebas unitarias (Karma)
  - `Cypress` para pruebas end-to-end.

- **Despliegue a servidor staging vía SSH/FTP**, activado tras validación de `develop`.

- **Validación manual previa al merge a producción (`main`)**, solo autorizada por el equipo administrador.

Esta planificación busca garantizar que cada cambio relevante pueda ser validado visual y funcionalmente en un entorno aislado, antes de ser promovido a producción.


::: info
***Spring Boot***
:::

Para alcanzar el despliegue continuo en el backend de Spring Boot, se planea la implementación de las siguientes herramientas y prácticas:

-   **GitHub Actions** como base del pipeline CI/CD.
-   Activación automática del despliegue a producción tras un merge exitoso a `main`.
-   Empaquetado de la aplicación en un **artefacto `.jar` ejecutable** y su posterior **containerización en una imagen Docker**.
-   Despliegue de la imagen Docker a un **registro de contenedores** (ej. Docker Hub, GHCR) y su posterior ejecución en el servidor usando **SSH** para orquestar los comandos.
-   **Docker** para iniciar y gestionar el contenedor, o **systemd** para gestionar el proceso Java en un despliegue tradicional.
-   Verificación post-despliegue mediante una llamada al **endpoint de health check** (`/actuator/health`) provisto por Spring Boot Actuator.
-   **Notificaciones automáticas por Slack o correo**, informando sobre el estado de cada despliegue.

Además, se planea incluir un sistema de rollback ágil. Al usar contenedores, un rollback consiste en detener la versión fallida y redesplegar la etiqueta (tag) de la imagen anterior, que permanece disponible en el registro de contenedores.

\newpage

### Stages Deployment Pipeline Components.

::: info
***Angular***
:::

El pipeline propuesto se divide en dos grandes etapas:

**Etapa:** Staging (rama `develop`)

- *Build SSR* para entorno de pruebas (`npm run build:ssr`)

- *Serve SSR* local para pruebas manuales o visuales

- Ejecución de pruebas unitarias y E2E

- Validación de lint y cobertura de código

- Bloqueo automático si falla alguna verificación

- Permite revisiones colaborativas antes de aprobar el paso a producción

**Etapa:** Producción (rama `main`)

- *Rebuild SSR* final

- Despliegue por SSH al servidor con NGINX

- Arranque de servidor con PM2 o Node directo

- Notificaciones automáticas al equipo (Slack/Email)

![Artefacto creado en Diagrams - Stages Deployment Pipeline](src/img/cap7/stages_deployment_pipeline.png){ height=40% }

\newpage

::: box
***Spring Boot***
:::

El pipeline de despliegue propuesto para el backend se divide en dos grandes etapas, alineadas con los entornos de `staging` y `producción`.

**Etapa: Staging (rama `develop`)**

-   **Empaquetado de la aplicación** para el entorno de pruebas, activando el perfil de `staging` (`mvn package -Dspring.profiles.active=staging`).
-   **Ejecución de la aplicación** para pruebas manuales y de integración con la base de datos de staging (`java -jar target/app.jar --spring.profiles.active=staging`).
-   **Ejecución del set completo de pruebas** (unitarias, integración) y validación de calidad.
-   **Análisis de cobertura de código** con **JaCoCo** y de estilo con **Checkstyle**.
-   **Bloqueo automático del Pull Request** si falla alguna verificación.
-   Permite revisiones colaborativas del equipo antes de aprobar el merge a `main`.

**Etapa: Producción (rama `main`)**

-   **Empaquetado final** de la aplicación con el perfil de `production` (`mvn package -Dspring.profiles.active=production`).
-   **Creación de una imagen Docker** que contiene el artefacto `.jar` ejecutable.
-   **Despliegue de la imagen Docker** al servidor, que se ejecuta detrás de un reverse proxy como **NGINX**.
-   **Arranque del contenedor** con `docker run` o gestión del servicio con **systemd**.
-   **Notificaciones automáticas** al equipo sobre el despliegue (Slack/Email).

![Artefacto creado en Diagrams - Stages Deployment Pipeline](src/img/cap7/stages_deployment_pipeline2.png){ height=40% }


\newpage

## Continuous deployment

El despliegue continuo (CD, por sus siglas en inglés) constituye el nivel más avanzado y maduro dentro de la cadena de prácticas DevOps. A diferencia de la entrega continua, donde la entrega a producción aún requiere una decisión manual, el despliegue continuo automatiza completamente este último paso, permitiendo que las versiones del sistema que hayan superado todas las validaciones y pruebas sean desplegadas directamente en el entorno de producción sin intervención humana. Esta estrategia no solo acorta drásticamente los ciclos de entrega de software, sino que también promueve una cultura de confianza, calidad continua y retroalimentación inmediata.

En el marco de este proyecto, el despliegue continuo aún no ha sido implementado de forma activa; sin embargo, se ha trazado una hoja de ruta clara para su incorporación progresiva. Este plan considera una arquitectura robusta para el frontend desarrollado en Angular, que incluirá mecanismos de revisión automática, auditorías de seguridad, generación de versiones con control semántico y despliegue seguro a través de protocolos como SSH o integraciones con servicios en la nube.

El objetivo a futuro es lograr un pipeline completamente automatizado que, al detectar un merge exitoso a la rama main, ejecute una secuencia de validaciones automatizadas, construcción optimizada del artefacto, pruebas funcionales finales y despliegue inmediato al entorno productivo. Este flujo garantizará que cada cambio relevante llegue a los usuarios finales de manera ágil, fiable y trazable.

Además de reducir los tiempos de entrega y eliminar cuellos de botella operativos, el despliegue continuo contribuye a minimizar los errores humanos y facilita una respuesta más rápida ante incidentes. También habilita prácticas de monitoreo post-despliegue y rollback automatizado en caso de fallos críticos, fortaleciendo así la resiliencia del sistema. La implementación futura de esta práctica representará un paso fundamental hacia una operación DevOps completamente integrada y eficiente.

![Recurso extraído de Canva](src/img/cap7/continuous-deployment.png)

\newpage

### Tools and Practices.

::: info
***Angular***
:::

Para alcanzar el despliegue continuo en el frontend Angular, se planea la implementación de las siguientes herramientas y prácticas:

- *GitHub Actions* como base del pipeline CI/CD.

- Activación automática del despliegue a producción tras merge exitoso a `main`.

- **Compilación final SSR (`ng build:ssr`)**.

- Despliegue al servidor usando *FTP/SSH* con credenciales seguras.

- *PM2 o Node* para iniciar el servidor de forma controlada.

- Verificación post-despliegue con herramientas como `curl` o tests visuales rápidos.

- *Notificaciones automáticas por Slack o correo*, informando sobre cada despliegue.

Además, se planea incluir un sistema de rollback simple en caso de fallos críticos, manteniendo una copia previa de la versión estable.

::: info
***Spring Boot***
:::

Para alcanzar el despliegue continuo en el backend de Spring Boot, se planea la implementación de las siguientes herramientas y prácticas:

-   **GitHub Actions** como base del pipeline CI/CD.
-   Activación automática del despliegue a producción tras un merge exitoso a `main`.
-   Empaquetado de la aplicación en un **artefacto `.jar` ejecutable** y su posterior **containerización en una imagen Docker**.
-   Despliegue de la imagen Docker a un **registro de contenedores** (ej. Docker Hub, GHCR) y su posterior ejecución en el servidor usando **SSH** para orquestar los comandos.
-   **Docker** para iniciar y gestionar el contenedor, o **systemd** para gestionar el proceso Java en un despliegue tradicional.
-   Verificación post-despliegue mediante una llamada al **endpoint de health check** (`/actuator/health`) provisto por Spring Boot Actuator.
-   **Notificaciones automáticas por Slack o correo**, informando sobre el estado de cada despliegue.

Además, se planea incluir un sistema de rollback ágil. Al usar contenedores, un rollback consiste en detener la versión fallida y redesplegar la etiqueta (tag) de la imagen anterior, que permanece disponible en el registro de contenedores.


\newpage

### Production Deployment Pipeline Components.

::: info
***Angular***
:::

El pipeline de despliegue continuo está planificado con la siguiente estructura para la rama **main**:

\begin{longtable}{|p{4cm}|p{9cm}|}
\hline
\textbf{Etapa} & \textbf{Descripción} \\
\hline
\endfirsthead

\hline
\textbf{Etapa} & \textbf{Descripción} \\
\hline
\endhead

Build SSR & Compilación de Angular en modo SSR (\texttt{ng build:ssr}) \\
\hline
Validación final & Ejecución de verificación mínima (ping, lint, SSR render) \\
\hline
Despliegue & Subida automática vía FTP/SSH al servidor de producción \\
\hline
Activación & Inicio del SSR con PM2 o script personalizado \\
\hline
Notificación & Envío de alertas a Slack o email tras despliegue exitoso \\
\hline

\end{longtable}


![Production Deployment Pipeline - Angular SSR](src/img/cap7/pipeline_diagram.png){ height=60% }


\newpage

::: info
***Spring Boot***
:::

El pipeline de despliegue continuo para el backend está planificado con la siguiente estructura para la rama **main**:

\begin{longtable}{|p{4cm}|p{9cm}|}
\hline
\textbf{Etapa} & \textbf{Descripción} \\
\hline
\endfirsthead

\hline
\textbf{Etapa} & \textbf{Descripción} \\
\hline
\endhead

Build & Compilar la aplicación y empaquetarla en un artefacto \texttt{.jar} ejecutable y una imagen **Docker** (\texttt{mvn package} y \texttt{docker build}). \\
\hline
Push to Registry & Publicar la imagen Docker versionada en un registro de contenedores centralizado (ej. Docker Hub, GHCR). \\
\hline
Deploy & Conexión vía **SSH** al servidor de producción para descargar la nueva imagen Docker y reiniciar el servicio usando la nueva versión. \\
\hline
Activate & Verificar e Iniciar el nuevo contenedor con \texttt{docker run} y realizar una comprobación automática del estado de la aplicación llamando a su endpoint de salud (\texttt{/actuator/health}). \\
\hline
Notify & Envío de alertas a **Slack** o email tras el despliegue exitoso, informando la nueva versión desplegada. \\
\hline

\end{longtable}


![Production Deployment Pipeline - Spring Boot](src/img/cap7/pipeline_diagram2.png){ height=60% }


\newpage

## Continuous Monitoring

El monitoreo continuo (Continuous Monitoring) es una práctica DevOps fundamental que actúa como el sistema de retroalimentación para todo el ciclo de vida del desarrollo y despliegue. No se limita a supervisar la infraestructura subyacente, sino que se enfoca en obtener visibilidad en tiempo real sobre la salud, el rendimiento y el comportamiento de la aplicación una vez que está en producción. Es el complemento indispensable del despliegue continuo, ya que permite validar el impacto de cada nuevo cambio y garantizar que el sistema opera de manera óptima.

En el marco de este proyecto Spring Boot, el monitoreo continuo se encuentra en una fase inicial, pero se ha trazado una hoja de ruta clara para su implementación robusta. Este plan se centra en aprovechar las capacidades nativas del ecosistema de Spring, como **Spring Boot Actuator**, para exponer métricas clave (salud, rendimiento, tráfico) y en integrarlas con herramientas estándar de la industria como **Prometheus** para la recolección de series temporales y **Grafana** para la creación de dashboards de visualización.

El objetivo a futuro es establecer un observatorio centralizado que brinde una visión de 360 grados sobre el estado del backend. Esto incluirá la configuración de **alertas proactivas** que notifiquen al equipo a través de Slack o correo ante anomalías o degradación del rendimiento, mucho antes de que los usuarios se vean afectados. Asimismo, se planea incorporar **centralización de logs** (con el stack ELK o Loki) y **trazabilidad distribuida** (con Jaeger o Zipkin) para diagnosticar problemas complejos de manera eficiente.

Más allá de la detección de fallos, el monitoreo continuo permite optimizar el rendimiento, planificar la capacidad del sistema y tomar decisiones de negocio basadas en datos de uso real. La implementación de esta práctica no solo fortalecerá la resiliencia y fiabilidad de la aplicación, sino que también cerrará el ciclo DevOps, proporcionando la confianza necesaria para innovar y desplegar cambios de manera rápida y segura. Es un pilar indispensable para la operación y evolución sostenible del servicio.

![Recurso extraído de Canva](src/img/cap7/continuous-monitoring-logo.png)

\newpage

### Tools and Practices

::: info
***Angular***
:::

El monitoreo en el frontend se centra en la experiencia del usuario (UX) y el rendimiento percibido en el navegador. Las prácticas y herramientas clave son:

-   **Error Tracking & Diagnostics con Sentry o Bugsnag**:
    -   **Práctica**: Capturar automáticamente errores de JavaScript no controlados, fallos en la renderización de componentes y errores de red (ej. llamadas a API fallidas).
    -   **Herramienta**: Integrar un SDK como **Sentry**, que agrupa errores, proporciona el stack trace completo y enriquece los reportes con contexto del navegador (versión, OS, URL) para facilitar una depuración rápida.

-   **Real User Monitoring (RUM) y Core Web Vitals**:
    -   **Práctica**: Medir el rendimiento real que experimentan los usuarios. Esto incluye los **Core Web Vitals** de Google (LCP, FID, CLS) y métricas de navegación como el Tiempo hasta el Primer Byte (TTFB) y el rendimiento de las transiciones de ruta en la SPA.
    -   **Herramienta**: Utilizar servicios como **Google Analytics 4**, **Datadog RUM** o el módulo de Performance de **Sentry** para recolectar y analizar estas métricas a lo largo del tiempo.

-   **Análisis de Comportamiento de Usuario**:
    -   **Práctica**: Entender cómo los usuarios interactúan con la aplicación: qué flujos son los más populares, dónde abandonan un proceso (ej. un formulario) y qué características son las más utilizadas.
    -   **Herramienta**: **Google Analytics** o herramientas más especializadas como **Hotjar** o **Mixpanel** para mapear los recorridos de usuario y generar mapas de calor (heatmaps).

-   **Monitoreo Sintético (Synthetic Monitoring)**:
    -   **Práctica**: Simular recorridos de usuario críticos (ej. flujo de inicio de sesión, proceso de compra) a intervalos regulares desde diferentes ubicaciones geográficas para detectar problemas de disponibilidad o degradación del rendimiento de forma proactiva.
    -   **Herramienta**: Servicios como **Datadog Synthetics** o **Checkly** que ejecutan scripts (similares a los de Cypress) contra la aplicación en producción.

::: info
***Spring Boot***
:::

El monitoreo en el backend se enfoca en la salud del servicio, el rendimiento de la API, el consumo de recursos y la integridad de los datos. El ecosistema de Spring Boot provee una base excelente para esto.

-   **Exposición de Métricas con Spring Boot Actuator**:
    -   **Práctica**: Exponer endpoints seguros (`/actuator/health`, `/actuator/metrics`, `/actuator/info`) que proporcionen una visión interna del estado de la aplicación. Esto incluye el estado de la base de datos, métricas de la JVM, rendimiento de los endpoints HTTP, etc.
    -   **Herramienta**: **Spring Boot Actuator** con **Micrometer** como fachada de métricas.

-   **Recolección y Almacenamiento de Métricas con Prometheus**:
    -   **Práctica**: Recolectar de forma periódica (scraping) las métricas expuestas por Actuator y almacenarlas en una base de datos de series temporales, optimizada para consultas y análisis de rendimiento a lo largo del tiempo.
    -   **Herramienta**: **Prometheus**, el estándar de facto en el ecosistema nativo de la nube.

-   **Visualización y Dashboards con Grafana**:
    -   **Práctica**: Crear dashboards personalizados que muestren de forma gráfica las métricas más importantes: latencia de la API, tasa de errores (HTTP 5xx), uso de CPU y memoria, estado del pool de conexiones a la base de datos, etc.
    -   **Herramienta**: **Grafana**, que se integra nativamente con Prometheus para crear visualizaciones potentes e intuitivas.

-   **Centralización de Logs con Loki o ELK Stack**:
    -   **Práctica**: Agregar todos los logs generados por la aplicación (y sus réplicas, si está containerizada) en un único sistema centralizado para facilitar la búsqueda, el filtrado y el análisis de errores.
    -   **Herramienta**: El stack **Loki + Promtail** (integrado con Grafana) o el más tradicional **ELK Stack (Elasticsearch, Logstash, Kibana)**.

-   **Sistema de Alertas con Alertmanager**:
    -   **Práctica**: Definir reglas sobre las métricas (ej. si la tasa de errores HTTP 5xx supera el 5\% durante 2 minutos) para generar alertas automáticas y proactivas que notifiquen al equipo.
    -   **Herramienta**: **Alertmanager**, que se integra con Prometheus y puede enrutar alertas a Slack, PagerDuty o email.

-   **Trazabilidad Distribuida (Distributed Tracing)**:
    -   **Práctica**: Rastrear una solicitud individual a través de las diferentes capas de la aplicación (Controller, Service, Repository) o a través de múltiples microservicios para identificar cuellos de botella y entender el flujo completo de una operación.
    -   **Herramienta**: **Jaeger** o **Zipkin**, integrados con Spring Boot a través de la instrumentación de **Micrometer Tracing**.

\newpage

### Monitoring Pipeline Components

::: info
***Angular***
:::

El pipeline de monitoreo para el frontend se enfoca en el flujo de datos desde que se genera un evento en el navegador del usuario hasta que se convierte en información accionable para el equipo de desarrollo. No es un pipeline de CI/CD, sino un **flujo de telemetría**.

\begin{longtable}{|p{4cm}|p{4cm}|p{6cm}|}
\hline
\textbf{Componente} & \textbf{Herramienta Principal} & \textbf{Descripción del Flujo} \\
\hline
\endfirsthead

\hline
\textbf{Componente} & \textbf{Herramienta Principal} & \textbf{Descripción del Flujo} \\
\hline
\endhead

Generación de Datos (Client-Side) & Navegador del Usuario & Es el punto de origen. Aquí se ejecutan el código Angular, ocurren los errores de JavaScript, se miden los Core Web Vitals y se registran las interacciones del usuario (clics, navegación). \\
\hline
Recolección y Envío (SDKs) & Sentry SDK, Google Analytics (gtag.js) & Librerías de JavaScript integradas en la aplicación Angular que actúan como agentes. Escuchan los eventos, los empaquetan con contexto (URL, ID de usuario, versión del navegador) y los envían de forma asíncrona a las plataformas de monitoreo. \\
\hline
Procesamiento y Agregación & Plataformas SaaS (Sentry, Google Analytics, Datadog) & Los servidores de estas plataformas reciben los datos crudos. Aquí se agrupan errores idénticos en un solo issue, se calculan los percentiles de rendimiento (p95, p99) y se almacenan los datos de forma estructurada para su posterior consulta. \\
\hline
Visualización y Análisis (Dashboards) & Dashboards de Sentry, Informes de Google Analytics & La interfaz donde el equipo interactúa con los datos. Se visualizan gráficos de rendimiento, listas de errores priorizados por impacto y análisis de flujos de usuario. Permite responder preguntas sobre la salud y el uso de la aplicación. \\
\hline
Alertas y Notificaciones & Integraciones con Slack, Email, PagerDuty & El componente proactivo del pipeline. Se configuran reglas (ej: alertar si la tasa de errores supera el 1\%). Cuando se cumple una condición, el sistema envía una notificación automática al canal designado, permitiendo una reacción rápida del equipo. \\
\hline

\end{longtable}

![Monitoring Pipeline Components - Angular](src/img/cap7/angular_monitoring_pipeline.png)

\newpage

::: info
***Spring Boot***
:::

El pipeline de monitoreo para el backend se enfoca en el flujo de datos desde que se genera un evento en el servidor de la aplicación hasta que se convierte en información accionable para el equipo de desarrollo. No es un pipeline de CI/CD, sino un **flujo de telemetría**.

\begin{longtable}{|p{4cm}|p{4cm}|p{6cm}|}
\hline
\textbf{Componente} & \textbf{Herramienta Principal} & \textbf{Descripción del Flujo} \\
\hline
\endfirsthead

\hline
\textbf{Componente} & \textbf{Herramienta Principal} & \textbf{Descripción del Flujo} \\
\hline
\endhead

Generación de Datos (Server-Side) & Spring Boot Actuator, Logback/SLF4J & Es el punto de origen. La aplicación Spring Boot expone métricas de rendimiento (JVM, HTTP, latencia) a través del endpoint \texttt{/actuator/prometheus} y escribe logs estructurados sobre su actividad y posibles errores. \\
\hline
Recolección y Envío (Agents/Scrapers) & Prometheus Scraper, Promtail (Loki) / Filebeat (ELK) & Agentes que se ejecutan en el servidor. Prometheus raspa (scrapes) el endpoint de métricas a intervalos regulares. Promtail/Filebeat leen los archivos de log en tiempo real y los envían al sistema de agregación. \\
\hline
Procesamiento y Agregación & Prometheus (Metrics DB), Loki / Elasticsearch (Logs DB) & Los servidores de monitoreo reciben los datos crudos. Prometheus almacena las métricas como series temporales. Loki/Elasticsearch indexan los logs para permitir búsquedas y análisis de texto completo de manera ultra rápida. \\
\hline
Visualización y Análisis (Dashboards) & Grafana & La interfaz unificada donde el equipo interactúa con todos los datos de monitoreo. Se conecta a Prometheus y Loki/Elasticsearch como fuentes de datos para construir dashboards que correlacionan métricas (ej. picos de CPU) con logs de errores. \\
\hline
Alertas y Notificaciones & Alertmanager & El componente proactivo del pipeline. Alertmanager recibe alertas definidas en Prometheus (ej. alta latencia de API), las de-duplica, agrupa y enruta al canal correcto (Slack, Email, PagerDuty), asegurando que el equipo sea notificado de problemas críticos. \\
\hline

\end{longtable}

![Monitoring Pipeline Components - Spring Boot](src/img/cap7/springboot_monitoring_pipeline.png)

\newpage

### Alerting Pipeline Components

::: info
***Angular***
:::

El pipeline de alertas para el frontend no es una herramienta independiente, sino una **funcionalidad integrada dentro de las plataformas de monitoreo** (como Sentry o Datadog). Su propósito es transformar un evento anómalo (un error o una métrica de rendimiento deficiente) en una notificación accionable para el equipo.

\begin{longtable}{|p{4cm}|p{4cm}|p{6cm}|}
\hline
\textbf{Componente} & \textbf{Herramienta Principal} & \textbf{Descripción del Flujo} \\
\hline
\endfirsthead

\hline
\textbf{Componente} & \textbf{Herramienta Principal} & \textbf{Descripción del Flujo} \\
\hline
\endhead

Disparo del Evento (Event Trigger) & Navegador del Usuario / Angular App & El punto de partida. Ocurre una condición anómala: un error de JavaScript no capturado, una llamada a API que devuelve un error 500, o una métrica de Core Web Vitals que excede un umbral definido (ej. LCP > 4s). \\
\hline
Ingesta y Contextualización & Sentry SDK / Datadog RUM SDK & El SDK en el cliente captura el evento. Crucialmente, lo enriquece con contexto: la URL donde ocurrió, la versión de la aplicación, el navegador y SO del usuario, y las migas de pan (breadcrumbs) de las últimas acciones del usuario. \\
\hline
Evaluación de Reglas (Rule Engine) & Sentry Alerting Engine / Datadog Monitors & El evento enriquecido llega a la plataforma SaaS. Su motor de reglas evalúa si el evento cumple las condiciones para generar una alerta. Por ejemplo: Alertar si un *nuevo* tipo de error aparece o Alertar si la tasa de errores de un endpoint supera el 5\% en 10 minutos. \\
\hline
Enrutamiento de Notificación & Módulo de Integraciones (Sentry, Datadog) & Una vez que una regla se activa, el sistema decide a dónde enviar la notificación. Puede ser un canal específico de Slack para errores críticos (\texttt{frontend-critical}), un correo electrónico para advertencias de rendimiento, o una llamada a PagerDuty para el ingeniero de guardia. \\
\hline
Entrega y Acción (Delivery \& Action) & Slack, Email, PagerDuty & La notificación final llega al equipo. Debe ser clara y accionable, incluyendo un título del problema, un resumen del impacto (ej. afectando a 50 usuarios en la última hora) y un enlace directo a la plataforma de monitoreo para iniciar la investigación. \\
\hline

\end{longtable}


![Alerting Pipeline Components - Angular](src/img/cap7/angular_alerting_pipeline.png)


\newpage

::: info
***Spring Boot***
:::

El pipeline de alertas para el backend es una composición de **herramientas especializadas que trabajan en conjunto**. Su propósito es detectar condiciones anómalas en el servidor (como alta latencia o consumo de recursos) y transformarlas en una notificación accionable para el equipo.

\begin{longtable}{|p{4cm}|p{4cm}|p{6cm}|}
\hline
\textbf{Componente} & \textbf{Herramienta Principal} & \textbf{Descripción del Flujo} \\
\hline
\endfirsthead

\hline
\textbf{Componente} & \textbf{Herramienta Principal} & \textbf{Descripción del Flujo} \\
\hline
\endhead

Disparo del Evento (Event Trigger) & Spring Boot Application / JVM & El punto de partida. Ocurre una condición anómala en el servidor: la latencia de un endpoint supera los 500ms, el uso de CPU excede el 80\%, el pool de conexiones a la base de datos se agota. La métrica correspondiente, expuesta por Actuator, cambia de valor. \\
\hline
Recolección y Almacenamiento & Prometheus & El scraper de Prometheus sondea periódicamente el endpoint \texttt{/actuator/prometheus} de la aplicación, recolecta el estado actual de todas las métricas y lo almacena en su base de datos de series temporales. \\
\hline
Evaluación de Reglas (Rule Engine) & Prometheus Alerting Engine & Prometheus evalúa continuamente un conjunto de reglas de alerta predefinidas (escritas en PromQL) contra las métricas almacenadas. Si una condición (ej. \texttt{tasa de errores > 5\% durante 2 minutos}) se cumple, la regla entra en estado firing (disparando). \\
\hline
Enrutamiento y Agrupación & Alertmanager & Cuando una regla se dispara, Prometheus envía una alerta a Alertmanager. Alertmanager es el cerebro de la notificación: de-duplica, agrupa alertas relacionadas (ej. 10 instancias de la misma app están caídas) y las enruta al receptor correcto basándose en etiquetas como \texttt{severity=critical}. \\
\hline
Entrega y Acción (Delivery \& Action) & Slack, Email, PagerDuty & Alertmanager envía la notificación final y procesada al canal configurado. El mensaje incluye etiquetas clave (\texttt{cluster=prod}, \texttt{app=iot-service}) y un enlace a un dashboard de Grafana pre-filtrado para que el equipo pueda iniciar la investigación de inmediato. \\
\hline

\end{longtable}


![Alerting Pipeline Components - Spring Boot](src/img/cap7/springboot_alerting_pipeline.png)

\newpage

### Notification Pipeline Components.

::: info
***Angular***
:::

El pipeline de notificación es la última milla del proceso de monitoreo. Se activa una vez que el motor de alertas ha decidido que un evento requiere atención humana. Su objetivo es construir y entregar un mensaje claro, contextualizado y accionable.

\begin{longtable}{|p{4cm}|p{4cm}|p{6cm}|}
\hline
\textbf{Componente} & \textbf{Herramienta Principal} & \textbf{Descripción del Flujo} \\
\hline
\endfirsthead

\hline
\textbf{Componente} & \textbf{Herramienta Principal} & \textbf{Descripción del Flujo} \\
\hline
\endhead

Disparo de la Notificación (Notification Trigger) & Sentry / Datadog Alerting Engine & El motor de alertas ha confirmado una violación de regla. Este componente es el punto de partida, pasando los datos del evento (el error, la métrica) al siguiente eslabón de la cadena. \\
\hline
Formateo del Mensaje (Message Formatting) & Motores de Plantillas de Sentry/Datadog & Los datos crudos del evento (JSON) se transforman en un mensaje legible para humanos usando plantillas. Se insertan variables como el título del error, el nombre del proyecto y la severidad para construir el texto final que se enviará a Slack o por email. \\
\hline
Canal de Entrega (Delivery Channel) & Integraciones (Webhooks a Slack, API de PagerDuty) & El sistema utiliza una integración preconfigurada para enviar el mensaje formateado. Típicamente, esto implica una llamada API a un webhook de Slack o al endpoint de eventos de PagerDuty. Este es el componente de transporte. \\
\hline
Contenido Accionable (Actionable Payload) & El Mensaje de Alerta & Es el contenido del mensaje final. Para ser efectivo, debe incluir: **1.** Título claro del problema. **2.** Impacto (ej. nº de usuarios afectados). **3.** Contexto clave (versión de la app, navegador). **4.** Un **enlace directo** (deep link) al evento en la plataforma de monitoreo para una investigación inmediata. \\
\hline
Recepción y Triage (Reception \& Triage) & Equipo de Desarrollo / Ingeniero de Guardia & El destino final. El equipo recibe la notificación. El primer paso es el triage: evaluar la urgencia, confirmar la recepción (acknowledge), asignar un responsable o hacer clic en el enlace para comenzar a depurar el problema. \\
\hline

\end{longtable}


![Notification Pipeline Components - Angular](src/img/cap7/angular_notification_pipeline.png)

\newpage

::: info
***Spring Boot***
:::

El pipeline de notificación es la última milla del proceso de monitoreo. Se activa una vez que Prometheus ha detectado una anomalía y pasa el control a Alertmanager, cuyo objetivo es construir y entregar un mensaje claro, contextualizado y accionable.

\begin{longtable}{|p{4cm}|p{4cm}|p{6cm}|}
\hline
\textbf{Componente} & \textbf{Herramienta Principal} & \textbf{Descripción del Flujo} \\
\hline
\endfirsthead

\hline
\textbf{Componente} & \textbf{Herramienta Principal} & \textbf{Descripción del Flujo} \\
\hline
\endhead

Disparo de la Notificación (Notification Trigger) & Prometheus Alerting Engine & El motor de alertas de Prometheus ha confirmado que una métrica viola una regla (ej. `latencia > 500ms`). Prometheus envía un payload JSON con la alerta y sus etiquetas (`labels`) y anotaciones (`annotations`) a Alertmanager. \\
\hline
Formateo y Agrupación (Formatting \& Grouping) & Alertmanager (Go Templating) & Alertmanager recibe una o más alertas. Primero, las agrupa por etiquetas (ej. todas las alertas del mismo servicio). Luego, utiliza su motor de plantillas Go para transformar los datos crudos (labels, annotations) en un único mensaje legible y bien estructurado. \\
\hline
Canal de Entrega (Delivery Channel) & Alertmanager Receivers & Basándose en las etiquetas de la alerta (ej. `severity=critical`), el árbol de enrutamiento de Alertmanager selecciona el receptor correcto. Cada receptor está configurado para un servicio específico (un webhook de Slack, la API de PagerDuty, un servidor de email). \\
\hline
Contenido Accionable (Actionable Payload) & El Mensaje de Alerta & Es el contenido del mensaje final. Para ser efectivo, debe incluir: **1.** Nombre de la alerta (`HighApiLatency`). **2.** Etiquetas clave (`cluster=prod`, `app=iot-service`). **3.** Un resumen o valor. **4.** Un **enlace directo a un dashboard de Grafana** pre-filtrado para una investigación inmediata. \\
\hline
Recepción y Triage (Reception \& Triage) & Equipo de Desarrollo / Ingeniero de Guardia & El destino final. El equipo recibe la notificación. El primer paso es el triage: evaluar la urgencia, confirmar la recepción en la interfaz de Alertmanager (acknowledge), y hacer clic en el enlace a Grafana para comenzar a diagnosticar el problema. \\
\hline

\end{longtable}


![Notification Pipeline Components - Spring Boot](src/img/cap7/springboot_notification_pipeline.png)
