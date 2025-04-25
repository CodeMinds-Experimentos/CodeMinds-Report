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

# Capítulo IV: Product Design

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

## Style Guidelines.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### General Style Guidelines.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### Web Style Guidelines.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### Mobile Style Guidelines.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

#### iOS Mobile Style Guidelines.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

#### Android Mobile Style Guidelines.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

## Information Architecture.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### Organization Systems.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### Labeling Systems.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### SEO Tags and Meta Tags

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### Searching Systems.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### Navigation Systems.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

## Landing Page UI Design.

El diseño de la interfaz de usuario (UI) de la landing page fue concebido con un enfoque centrado en el usuario, priorizando la claridad, accesibilidad y jerarquía visual. A través de un lenguaje visual coherente y elementos interactivos bien distribuidos, se buscó comunicar el valor de la plataforma de manera inmediata y efectiva. La estructura de la landing page permite a los usuarios identificar rápidamente las secciones clave, generando interés y facilitando la navegación hacia las áreas de mayor conversión. Este proceso de diseño incluyó tanto la creación de wireframes como mockups, permitiendo validar la experiencia antes de su implementación definitiva

### Landing Page Wireframe.

Los wireframes representan la estructura básica de la landing page, enfocándose en la disposición de los elementos sin distraer con colores o estilos visuales complejos. Esta etapa fue clave para definir la jerarquía de la información, la ubicación de llamados a la acción (CTAs) y la secuencia de navegación esperada. Cada sección fue diseñada para cumplir un objetivo específico dentro del recorrido del usuario, desde la presentación inicial hasta los beneficios, características, segmentos objetivo (padres y colegios), equipo, demostración y contacto. El uso de wireframes permitió validar la lógica de la interfaz antes de pasar a etapas más detalladas de diseño visual.

![](https://i.postimg.cc/Jh7nbHyD/wireframe-inicio.png){ width=50% }
![](https://i.postimg.cc/CxgdxQS4/wireframe-beneficios.png){ width=50% }
![](https://i.postimg.cc/J4JGmLVn/wireframe-caracteristicas.png){ width=50% }
![](https://i.postimg.cc/FFYYWST0/wireframe-padres.png){ width=50% }
![](https://i.postimg.cc/66FyDQPg/wireframe-colegios.png){ width=50% }
![](https://i.postimg.cc/jCV0vmZ3/wireframe-team.png){ width=50% }
![](https://i.postimg.cc/C1QVnzDg/wireframe-demo.png){ width=50% }
![](https://i.postimg.cc/0QQsNpzn/wireframe-contactanos-footer.png){ width=50% }

[Figma CodeMinds Wireframe](https://www.figma.com/design/hWQCYGLq8uiSZolh8ChRN7/Untitled?node-id=0-1&t=r3o6PxgMClNo9kx7-1)
\newpage

### Landing Page Mock-up.

Los mockups son representaciones de alta fidelidad de la interfaz, incorporando el estilo visual definitivo, paleta de colores, tipografías, imágenes y demás elementos gráficos. En esta etapa, se reflejó la identidad visual de la plataforma, asegurando coherencia entre el mensaje y la estética. Los mockups también permiten evaluar aspectos como el contraste, el espaciado, la legibilidad y el impacto visual de cada sección. Gracias a esta representación visual detallada, fue posible obtener retroalimentación específica y realizar ajustes antes de iniciar la implementación del diseño en código.

![](https://i.postimg.cc/Kj3hPxrg/mockup-inicio.png)
![](https://i.postimg.cc/q7prPf09/mockup-beneficios.png)
![](https://i.postimg.cc/k5wC9jgD/mockup-caracteristicas.png)
![](https://i.postimg.cc/RZ79pCr7/mockup-padres.png)
![](https://i.postimg.cc/RZ54T6YC/mockup-colegios.png)
![](https://i.postimg.cc/BQ1JDcMw/mockup-team.png)
![](https://i.postimg.cc/kMHnBhFb/mockup-demo.png)
![Landing Page Mockup - Recurso de Figma](https://i.postimg.cc/2y1r04my/mockup-contactanos-footer.png)
[Figma CodeMinds Mockup](https://www.figma.com/design/hWQCYGLq8uiSZolh8ChRN7/Untitled?node-id=0-1&t=r3o6PxgMClNo9kx7-1)


\newpage

## Mobile Applications UX/UI Design.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### Mobile Applications Wireframes.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### Mobile Applications Wireflow Diagrams.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### Mobile Applications Mock-ups.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### Mobile Applications User Flow Diagrams.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

## Mobile Applications Prototyping.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### Android Mobile Applications Prototyping.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### iOS Mobile Applications Prototyping.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

## *Web Applications UX/UI Design.*

![Recurso estraído de Google](src/img/cap4/angular.jpg)

En esta sección se presenta el proceso de diseño UX/UI desarrollado para la aplicación web de RutaKids, centrado en ofrecer una experiencia funcional, accesible y coherente con las necesidades de sus principales usuarios: colegios, padres de familia y operadores de transporte escolar. A partir de una investigación previa, se definieron flujos clave, se estructuraron wireframes en baja fidelidad y se evolucionó hacia interfaces modernas, basadas en principios de usabilidad y diseño centrado en el usuario. El objetivo es garantizar que cada interacción dentro del sistema sea intuitiva, segura y alineada a los objetivos del proyecto.

::: warn
Para visualizar todo el diseño de los wireframes y mockups de la aplicación, haga click en la [URL](https://app.uizard.io/p/726b9d4c)
:::

\newpage

### *Web Applications Wireframes.*

**Autenticación y recuperación de acceso**

![Pantalla de inicio de sesión - Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/sign_in.png)

![Recuperación de contraseña - Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/forgot_password.png)

![Reinicio de contraseña - Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/reset_password.png)

![Cambio de contraseña - Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/change_password.png)

**Navegación y funcionalidades complementarias**

![Dashboard general - Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/dashboard.png)

![Notificaciones - Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/notifications.png)

![Preguntas frecuentes - Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/faq.png)

![Política de privacidad - Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/privacy_policy.png)

![Cerrar sesión - Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/log_out.png)

![Terminos y Condiciones - Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/terms.png)


**Gestión de estudiantes**

![Crear estudiante - Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/create_student.png)

![Lista de estudiantes - Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/students_list.png)

![Tarjetas de estudiantes - Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/students_cards.png)


**Gestión de movilidades y rutas escolares**

![Crear movilidad escolar - Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/create_school_trans.png)

![Listado de movilidades - Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/school_trans_list.png)

![Crear ruta escolar - Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/create_school_routes.png)

![Listado de rutas escolares - Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/school_routes_list.png)


\newpage

### *Web Applications Wireflow Diagrams.*

solo falta subir canchis canchis

\newpage

### *Web Applications Mock-ups.*

**Autenticación y recuperación de acceso**

![Pantalla de inicio de sesión - Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/sign_in.png)

![Recuperación de contraseña - Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/forgot_password.png)

![Reinicio de contraseña - Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/reset_password.png)

![Cambio de contraseña - Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/change_password.png)


**Navegación y funcionalidades complementarias**

![Dashboard general - Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/dashboard.png)

![Notificaciones - Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/notifications.png)

![Preguntas frecuentes - Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/faq.png)

![Política de privacidad - Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/privacy_policy.png)

![Cerrar sesión - Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/log_out.png)

![Terminos y Condiciones - Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/terms.png)


**Gestión de estudiantes**

![Crear estudiante - Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/create_student.png)

![Lista de estudiantes - Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/students_list.png)

![Tarjetas de estudiantes - Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/students_cards.png)


**Gestión de movilidades y rutas escolares**

![Crear movilidad escolar - Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/create_school_trans.png)

![Listado de movilidades - Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/school_trans_list.png)

![Crear ruta escolar - Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/create_school_routes.png)

![Listado de rutas escolares - Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/school_routes_list.png)

\newpage

### *Web Applications User Flow Diagrams.*

solo falta subir canchis canchis

\newpage

## *Web Applications Prototyping.*

::: warn
Para visualizar el video del prototipo de la aplicación,  haga click en la [URL](https://upcedupe-my.sharepoint.com/:v:/g/personal/u202210059_upc_edu_pe/EaarYyGV9fFJpLWK1u04GaIBtRlSoc7_affoLtT38NNzEQ?e=krmvNP&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D)
:::


\newpage

## Domain-Driven Software Architecture.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### Software Architecture Context Diagram.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### Software Architecture Container Diagrams.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### Software Architecture Components Diagrams.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

## Software Object-Oriented Design.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### Class Diagrams.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### Class Dictionary.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

## Database Design.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### Relational/Non-Relational Database Diagram.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.
