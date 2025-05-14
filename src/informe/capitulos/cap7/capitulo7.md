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

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

## Continuous Integration

La integración continua (CI, por sus siglas en inglés) es una práctica fundamental de DevOps que busca automatizar el proceso de integración de cambios en el código fuente, permitiendo validar cada actualización mediante pruebas y compilaciones automáticas. 

En este proyecto, la CI se implementa con el objetivo de asegurar que cada módulo del sistema, tanto en el frontend como en el backend, se mantenga funcional, probado y listo para ser desplegado. 

Actualmente se emplea GitHub como sistema de control de versiones, y se han comenzado a aplicar flujos automatizados con GitHub Actions, especialmente para la documentación técnica del frontend Angular. A medida que el proyecto evoluciona, se integrarán más etapas en el pipeline de CI, enfocadas en pruebas, calidad de código y despliegues controlados.

\newpage

### Tools and Practices.

***Angular***

Para el frontend Angular, se ha adoptado una arquitectura modular con componentes standalone bajo Angular 17. Las prácticas de integración continua (CI) se gestionan a través de GitHub, utilizando GitHub Actions para automatizar la generación de documentación con Compodoc.

Si bien la infraestructura completa de CI/CD aún está en planificación (con miras al despliegue en un dominio propio), actualmente se aplican las siguientes prácticas:

- Uso de **GitHub como sistema de control de versiones**, siguiendo un flujo de trabajo basado en ramas (`git flow`).

- La rama `main` se mantiene como fuente principal para despliegues.

- No se permite realizar merge a `main` si existen errores en pruebas o compilación.

- Se ejecutan pruebas unitarias mediante `ng test` con Karma.

- Se genera documentación automáticamente con **Compodoc** usando GitHub Actions.

En futuras fases de producción, se espera incorporar un pipeline más robusto que incluya:

- Ejecución automatizada de pruebas, lint y build con GitHub Actions.

- Despliegues automáticos desde `main`.

- Configuración de entornos diferenciados (`development`, `staging`, `production`).

\newpage

### Build & Test Suite Pipeline Components.

***Angular***

Aunque el pipeline completo aún está en desarrollo, se ha definido una estructura base que contempla las siguientes etapas para el frontend Angular:

**Etapas previstas del pipeline de CI para Angular:**

| Etapa     | Descripción                                            | Comando                                                |
|-----------|--------------------------------------------------------|--------------------------------------------------------|
| Install   | Instalación de dependencias                            | `npm ci`                                               |
| Test      | Ejecución de pruebas unitarias con Karma               | `ng test --watch=false --browsers=ChromeHeadless`     |
| Build     | Compilación del proyecto en modo producción            | `ng build --configuration=production`                 |
| Docs      | Generación de documentación con Compodoc               | `npx compodoc -p tsconfig.app.json -s`                |

**Reglas de activación:**

- El pipeline se activa ante push o pull request a la rama `main`.

- Si alguna etapa falla (build o test), se bloquea el merge automáticamente.

**Mejoras futuras previstas:**

- Integración de `lint` con ESLint (`ng lint`).

- Generación de badges y reporte de cobertura.

- Separación de flujos para despliegue en `staging` y `producción`.

Esta estructura asegura que los módulos Angular sean correctamente validados antes de su integración, manteniendo la estabilidad y calidad de la aplicación.

**Diagrama del pipeline CI/CD para Angular**

![Artefacto creado en Diagrams - Build & Test Suite Pipeline - Angular SSR + GitFlow](src/img/cap7/7.1.2_build_&_test_suite_pipeline_(angular_ssr_+_gitflow).png)

\newpage

## Continuous Delivery

***Angular***

La entrega continua (CD) es una práctica que extiende la integración continua, permitiendo que las versiones del sistema que superan las pruebas sean entregadas automáticamente a entornos intermedios como `staging` o `QA`. En el contexto del frontend Angular, esta práctica facilita validar los cambios en un entorno similar al de producción antes de realizar el despliegue definitivo.

Aunque actualmente el proyecto aún se encuentra en etapas iniciales de automatización del despliegue, ya se ha planificado una estructura basada en ramas (`develop` y `main`) con un pipeline controlado que incluye compilación SSR, pruebas end-to-end (Cypress) y despliegue vía SSH a servidores externos.

\newpage

### Tools and Practices.

***Angular***

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


\newpage

### Stages Deployment Pipeline Components.

***Angular***

El pipeline propuesto se divide en dos grandes etapas:

**Etapa: Staging (rama `develop`)**

- **Build SSR** para entorno de pruebas (`npm run build:ssr`)

- **Serve SSR** local para pruebas manuales o visuales

- **Ejecución de pruebas unitarias y E2E**

- **Validación de lint y cobertura de código**

- **Bloqueo automático si falla alguna verificación**

- **Permite revisiones colaborativas antes de aprobar el paso a producción**

**Etapa: Producción (rama `main`)**

- **Rebuild SSR final**

- **Despliegue por SSH al servidor con NGINX**

- **Arranque de servidor con PM2 o Node directo**

- **Notificaciones automáticas al equipo (Slack/Email)**

![Artefacto creado en Diagrams - Stages Deployment Pipeline - Angular SSR + GitFlow](src/img/cap7/7.2.2_–_stages_deployment_pipeline_(angular_ssr_+_gitflow).png)

\newpage

## Continuous deployment

***Angular***

El despliegue continuo (CD) representa el nivel más avanzado en una estrategia DevOps, permitiendo que las versiones validadas del sistema se desplieguen automáticamente a producción sin intervención manual. Aunque actualmente no se ha implementado esta práctica, se ha diseñado un flujo profesional futuro que busca alcanzar dicha automatización para el frontend desarrollado en Angular.

Este enfoque apunta a minimizar errores humanos, reducir tiempos de entrega y asegurar una operación estable mediante validaciones automatizadas y despliegue seguro a servidores externos.

\newpage

### Tools and Practices.

***Angular**

Para alcanzar el despliegue continuo en el frontend Angular, se planea la implementación de las siguientes herramientas y prácticas:

- **GitHub Actions** como base del pipeline CI/CD.

- Activación automática del despliegue a producción tras merge exitoso a `main`.

- **Compilación final SSR (`ng build:ssr`)**.

- Despliegue al servidor usando **FTP/SSH** con credenciales seguras.

- **PM2 o Node** para iniciar el servidor de forma controlada.

- Verificación post-despliegue con herramientas como `curl` o tests visuales rápidos.

- **Notificaciones automáticas por Slack o correo**, informando sobre cada despliegue.

Además, se planea incluir un sistema de rollback simple en caso de fallos críticos, manteniendo una copia previa de la versión estable.

\newpage

### Production Deployment Pipeline Components.

***Angular***

El pipeline de despliegue continuo está planificado con la siguiente estructura para la rama `main`:

| Etapa               | Descripción                                                  |
|---------------------|--------------------------------------------------------------|
| Build SSR           | Compilación de Angular en modo SSR (`ng build:ssr`)          |
| Validación final    | Ejecución de verificación mínima (ping, lint, SSR render)    |
| Despliegue          | Subida automática vía FTP/SSH al servidor de producción      |
| Activación          | Inicio del SSR con PM2 o script personalizado                |
| Notificación        | Envío de alertas a Slack o email tras despliegue exitoso     |

![Production Deployment Pipeline - Angular SSR + GitFlow](src/img/cap7/7.2.3_pipeline_diagram_(angular_ssr_+_gitflow).png)


\newpage

## Continuous Monitoring

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### Tools and Practices

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### Monitoring Pipeline Components

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### Alerting Pipeline Components

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### Notification Pipeline Components.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.
