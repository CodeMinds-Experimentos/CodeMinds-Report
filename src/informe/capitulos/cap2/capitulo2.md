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

# Capítulo II: Requirements Elicitation & Analysis

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

## Competidores.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### Análisis competitivo.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### Estrategias y tácticas frente a competidores.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

## Entrevistas.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### Diseño de entrevistas.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### Registro de entrevistas.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### Análisis de entrevistas.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage


## Needfinding.

Para garantizar que las soluciones propuestas respondan efectivamente a los problemas reales de los usuarios, es fundamental comprender a fondo sus necesidades, contextos y comportamientos. En esta etapa de needfinding, se llevó a cabo una exploración detallada orientada a descubrir oportunidades de diseño a través de la observación directa, entrevistas y otras técnicas de investigación centradas en el usuario.

Este proceso no solo permitió identificar las tareas clave, frustraciones y objetivos de los usuarios, sino que también ayudó a construir una base sólida para el desarrollo de funcionalidades relevantes y valiosas. A través de herramientas como perfiles de usuario, mapas de empatía, y journeys, se consolidó una visión clara de los desafíos actuales y las motivaciones de los actores principales, sentando así las bases para un diseño centrado en el usuario.

### User Personas.
Presentamos perfiles representativos de nuestros usuarios objetivos. Estos arquetipos nos ayudan a diseñar centrados en sus motivaciones, frustraciones y objetivos.

**User Persona 1** - Segmento Tutor/Padre Apoderado
Esteban representa a los padres que buscan seguridad, puntualidad y confianza en el servicio de transporte escolar.

![User Persona 1 - Recurso de Figma](https://i.postimg.cc/5tVd8BDb/user-person-esteban.png)

**User Persona 2** - Segmento Administrador Educativo
Carolina representa a las administradoras que necesitan eficiencia, control y visibilidad en la gestión del transporte escolar.

![User Persona 2 - Recurso de Figma](https://i.postimg.cc/GmYnB77X/user-person-carolina.png)


### User Task Matrix.

Se mapea la relación entre los usuarios y sus tareas principales. Esto nos permite priorizar funcionalidades clave del sistema según las necesidades del segmento.

![User Task Matrix - Recurso de Miro](https://i.postimg.cc/JnKLrs6m/task-matrix.png)


### User Journey Mapping.

Visualizamos el recorrido actual de cada usuario con el servicio. Esta herramienta permite identificar puntos de dolor, emociones y oportunidades de mejora.

**User Journey – Esteban (Padre de familia)**
Muestra cómo Esteban experimenta el servicio día a día, destacando momentos críticos como la espera o la llegada del bus.

![User Journey Mapping 1 - Recurso de Miro](https://i.postimg.cc/vHCdZFz1/user-journey-esteban.png)

**User Journey – Carolina (Administradora)**
Refleja las acciones y frustraciones que Carolina enfrenta al gestionar manualmente el transporte escolar.

![User Journey Mapping 2 - Recurso de Miro](https://i.postimg.cc/ZKWSmKrt/user-journey-carolina.png)


### Empathy Mapping.

Ayuda a profundizar en la perspectiva emocional y racional de cada usuario: lo que piensa, siente, ve, escucha, dice y hace.

**Empathy Map – Esteban**
Nos permite entender el entorno emocional de Esteban frente a la seguridad y control del transporte escolar.

![Empathy Mapping 1 - Recurso de Miro](https://i.postimg.cc/Y2nHTmLz/empathy-esteban.png)

**Empathy Map – Carolina**
Expone las preocupaciones, necesidades y entorno de Carolina como gestora del sistema de transporte.

![Empathy Mapping 2 - Recurso de Miro](https://i.postimg.cc/BbVfFdfV/empathy-carolina.png)


### As-is Scenario Mapping.

Describe cómo es actualmente la experiencia del usuario sin una solución tecnológica centralizada. Se evidencian fricciones, ineficiencias y oportunidades.

**As-Is Scenario – Esteban**
Esteban enfrenta incertidumbre en los horarios y poca información en tiempo real.

![As-is Scenario Mapping 1 - Recurso de Miro](https://i.postimg.cc/tJTHY9w6/as-is-esteban.png)

**As-Is Scenario – Carolina**
Carolina gestiona procesos con llamadas y hojas de cálculo, con baja automatización.

![As-is Scenario Mapping 2 - Recurso de Miro](https://i.postimg.cc/50fJWBmn/as-is-carolina.png)


## Ubiquitous Language.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.
