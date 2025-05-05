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
  @kalbach2016,
  @tarzijan2019,
  @lin2024,
  @rijgersberg2025,
  @igartua2019desconexion,
  @jiang2024pervasive,
  @kaspersky_privacy,
  @collave2024datos,
  @rajput2021,
  @boyd2021,
  @richardson2020,
  @toussaint2020,
  @brown2021,
  @angular2024,
  @freeman2022,
  @edutransport2020,
  @skole2020,
  @satgeo2020,
  @allride2020,
  @ubusschool2020,
  @tilkov2017,
  @pilgrim2021
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

**Registro de Versiones del Informe**

\begin{longtable}{|c|c|c|p{6cm}|}
  \hline
  \textbf{Versión} & \textbf{Fecha} & \textbf{Autor} & \textbf{Descripción de Modificación} \\
  \hline
  tb1 & 25/04/2025 & Ortega Huaraca, Abel & Ayudé con la estructura del informe en general. Respecto a los puntos específicos, contribuí con la elaboración del \textit{Solution Profile}, \textit{Startup Profile}, Segmentos objetivo, \textit{User Stories} y una introducción para los \textit{Requirements Specification}. También colaboré con el \textit{Product Backlog}, \textit{Diseño de entrevistas}, \textit{Mobile Applications Prototyping}, implementación del producto, y la documentación del API RESTful. \\
  \hline
  tb1 & 25/04/2025 & Ramos Rios, Belén del Rocio & Elaboré el análisis competitivo y estrategias frente a competidores, el diseño de entrevistas y su análisis. Además, desarrollé los apartados de \textit{Style Guidelines}, \textit{Information Architecture}, y los sistemas de navegación. \\
  \hline
  tb1 & 25/04/2025 & Vilchez Rios, Mateo Alejandro & Redacté los antecedentes y problemática, además de contribuir con el \textit{Impact Mapping}. Participé en el diseño UX/UI de aplicaciones web y colaboré en la sección de arquitectura de software (\textit{Domain-Driven Software Architecture}). \\
  \hline
  tb1 & 25/04/2025 & Herrera González, Luis Eduardo & Desarrollé el apartado de \textit{Ubiquitous Language} y colaboré en el diseño de arquitectura de software, específicamente en los diagramas de contexto, contenedores y componentes. También apoyé en la parte de UX/UI para aplicaciones web. \\
  \hline
  tb1 & 25/04/2025 & Vargas Revollé, Ariana & Me encargué del \textit{To-Be Scenario Mapping}, \textit{Needfinding}, incluyendo \textit{User Personas}, \textit{Journey Map}, \textit{Empathy Mapping} y \textit{As-is Scenario Map}. También diseñé el \textit{Landing Page Mock-up}. \\
  \hline
\end{longtable}


\newpage

***Project Report Collaboration Insights***

**TB1:**

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


***Student Outcome***

El curso contribuye al cumplimiento del ***Student Outcome ABET:*** *ABET-EAC - Student Outcome 4*

* **Criterio:** *La capacidad de reconocer responsabilidades éticas y profesionales en situaciones de ingeniería y hacer juicios informados, que deben considerar el impacto de las soluciones de ingeniería en contextos globales, económicos, ambientales y sociales*.

En el siguiente cuadro se describe las acciones realizadas y enunciadas de conclusiones por parte del grupo, que permiten sustentar el haber alcanzado el logro de ***ABET - EAC - Student Outcome 4.***

\begin{longtable}{|p{4cm}|p{6cm}|p{5cm}|}
\hline
\multicolumn{1}{|c|}{\textbf{Criterio Específico}} & \multicolumn{1}{c|}{\textbf{Acciones Realizadas}} & \multicolumn{1}{c|}{\textbf{Conclusiones}} \\
\hline
\endfirsthead

\parbox[t]{4cm}{
\textit{\textbf{4.c.1} Reconoce responsabilidad ética y profesional en situaciones de ingeniería de software}
} 
&  
\parbox[t]{6cm}{
\textbf{TB1:} \\
\textbf{Abel Angel Ortega Huaraca} \\
Fomenté un ambiente de trabajo colaborativo y respetuoso, asumiendo con seriedad los compromisos asumidos. Evité prácticas deshonestas en la documentación y respeté los tiempos del equipo. \\
\textbf{Belen del Rocio Ramos Rios} \\
Mantuve imparcialidad en el análisis de la competencia y fui objetiva en las entrevistas, evitando sesgos o influencias indebidas. Promoví una participación ética durante la recolección de datos. \\
\textbf{Mateo Alejandro Vilchez Rios} \\
Durante la formulación del problema y el diseño UX, me aseguré de usar fuentes confiables y no tergiversar los hallazgos para beneficiar nuestras propuestas. \\
\textbf{Luis Eduardo Herrera González} \\
Durante el proyecto, siempre traté de ser transparente en las entrevistas y al dar opiniones sobre otras soluciones. Reconocí lo que la competencia hacía bien para mejorar nuestro trabajo, sin exagerar ni mentir. También me aseguré de comunicar cualquier problema al equipo de forma clara y honesta, manteniendo el respeto y la ética en todo momento. \\
\textbf{Ariana Vargas Revollé} \\
Durante la elaboración de los mapas de empatía y escenarios, me aseguré de representar fielmente las necesidades de los usuarios sin manipular la información para favorecer nuestras ideas. 
} 
&
\parbox[t]{5cm}{
\textbf{TB1:} \\
Todos los integrantes demostramos responsabilidad ética en cada etapa del proyecto. Se respetaron los derechos de los usuarios, se promovió la honestidad en la documentación y se evitó cualquier forma de desinformación o apropiación indebida.
} \\ 

\hline

\parbox[t]{4cm}{
\textit{\textbf{4.c.2} Emite juicios informados considerando el impacto de las soluciones de ingeniería de software en contextos globales, económicos, ambientales y sociales}
}
&  
\parbox[t]{6cm}{
\textbf{TB1:} \\
\textbf{Abel Angel Ortega Huaraca} \\
Consideré cómo nuestra solución podía escalar a otras ciudades y cómo afectaría la rutina familiar y escolar. Evalué el impacto económico para no generar exclusión. \\
\textbf{Belen del Rocio Ramos Rios} \\
Analicé el contexto competitivo para asegurar que nuestra solución tuviera un valor diferencial que aportara realmente a la sociedad, sin crear dependencias innecesarias en los usuarios. \\
\textbf{Mateo Alejandro Vilchez Rios} \\
Durante la definición de problemas, tomé en cuenta factores sociales y urbanos que afectan el transporte escolar. Procuré no sugerir soluciones que generaran mayor tráfico o contaminación. \\
\textbf{Luis Eduardo Herrera González} \\
Al investigar para nuestra solución de transporte escolar, tomé en cuenta el impacto social y la importancia de proteger la privacidad de los estudiantes. Evitamos propuestas que pudieran hacer que los padres invadieran la privacidad de sus hijos. También pensamos en que nuestro sistema fuera accesible y no generara un costo extra fuerte para las familias o colegios. \\
\textbf{Ariana Vargas Revollé} \\
Al crear los escenarios y perfiles de usuario, prioricé un enfoque inclusivo que tomara en cuenta distintos niveles socioeconómicos. También busqué que la experiencia del usuario no dependiera de dispositivos costosos o poco accesibles.
}
&
\parbox[t]{5cm}{
\textbf{TB1:} \\
Todos los integrantes demostramos conciencia del impacto de nuestras decisiones, priorizando una solución accesible, ética y útil socialmente. Se consideraron factores económicos y sociales durante el diseño y desarrollo del proyecto.
} \\
\hline
\end{longtable}


\newpage

# Capítulo I: Introducción

## Startup Profile

### Descripción de la Startup

***CodeMinds:*** **Innovación y Confianza en el Transporte Escolar**

CodeMinds es una startup peruana comprometida con la innovación en la gestión y la seguridad del transporte escolar en colegios privados, apoyándose en tecnologías avanzadas de Internet de las Cosas (IoT) y plataformas digitales de última generación. Nos especializamos en diseñar soluciones integrales que, más allá de optimizar rutas y recursos, sitúan la confianza de las familias y el bienestar de los estudiantes como ejes centrales de nuestro desarrollo. Nuestros sistemas de análisis de datos en tiempo real facilitan la toma de decisiones proactiva y el cumplimiento de los más exigentes estándares de calidad y normativas del sector. Con un firme compromiso por la privacidad y la protección de la información, proporcionamos herramientas intuitivas que empoderan a las instituciones educativas, a los operadores de transporte y a los padres de familia, garantizando transparencia total en cada trayecto. En CodeMinds, creemos en la colaboración constante con nuestros clientes para co-crear mejoras continuas, generando un impacto social positivo y redefiniendo los estándares de seguridad y eficiencia en el transporte escolar peruano.

![CodeMinds logo](src/img/logo/CodeMinds.png)

::: box 
**Misión**

Brindar a colegios privados y a las familias herramientas tecnológicas robustas que optimicen la gestión del transporte escolar, fortalezcan la seguridad de los estudiantes y fomenten la confianza de todos los actores involucrados.
:::

::: box
**Visión**

Ser reconocidos a nivel nacional e internacional como líderes en soluciones de transporte escolar basadas en IoT, estableciendo nuevos estándares de excelencia, innovación y responsabilidad social.
:::

\newpage

### Perfiles de integrantes del equipo

Nuestro equipo está conformado por individuos apasionados y comprometidos, cada uno aportando sus habilidades únicas para lograr nuestros objetivos de manera efectiva y colaborativa. Aquí se muestran a nuestros miembros clave:

\definecolor{mybackground}{HTML}{eed6d1}

\begin{tcolorbox}[colframe=mybackground, colback=mybackground, boxrule=0.8mm, width=\textwidth, sharp corners]
{
\begin{minipage}[c]{0.3\textwidth}
\includegraphics[width=\linewidth]{src/img/integrantes/abel.jpg}
\end{minipage}
\hfill
\begin{minipage}[c]{0.65\textwidth}
\textbf{Abel Angel Ortega Huaraca} \\
\textit{Ingeniero de Software} \\
Me considero una persona responsable y comprometida en las funciones que se me designe. Conforme a mis habilidades, puedo adaptarme rápidamente al equipo y al ritmo de trabajo. Asimismo, puedo contribuir con información y soluciones a través de una exhaustiva investigación para los problemas que el proyecto presente.
\end{minipage}
}
\end{tcolorbox}

\begin{tcolorbox}[colframe=mybackground, colback=mybackground, boxrule=0.8mm, width=\textwidth, sharp corners]
{
\begin{minipage}[c]{0.3\textwidth}
\includegraphics[width=\linewidth]{src/img/integrantes/belen.jpg}
\end{minipage}
\hfill
\begin{minipage}[c]{0.65\textwidth}
\textbf{Belen del Rocio Ramos Rios} \\
\textit{Ingeniera de Software} \\
Soy estudiante del séptimo ciclo de la carrera de Ingeniería de Software. A lo largo de mi formación, he adquirido conocimientos en diversos lenguajes de programación como Java, C++, SQL y recientemente Kotlin. También tengo experiencia en el uso de frameworks como Spring Boot para el desarrollo backend, y Vue, Angular y Flutter para el desarrollo frontend. Me considero una persona comprometida, con habilidades para el trabajo en equipo y siempre dispuesta a dar lo mejor de mí en cada proyecto que emprendo.
\end{minipage}
}
\end{tcolorbox}

\begin{tcolorbox}[colframe=mybackground, colback=mybackground, boxrule=0.8mm, width=\textwidth, sharp corners]
{
\begin{minipage}[c]{0.3\textwidth}
\includegraphics[width=\linewidth, height=\linewidth, keepaspectratio=false]{src/img/integrantes/mateo.jpg}
\end{minipage}
\hfill
\begin{minipage}[c]{0.65\textwidth}
\textbf{Mateo Alejandro Vilchez Rios} \\
\textit{Ingeniero de Software} \\
Soy estudiante de la carrera de Ingeniería de Software cursando actualmente el 7mo ciclo. Me considero una persona eficiente, disciplinada y responsable. Poseo conocimientos Java, JavaScript y TypeScript. Manejo de Base de Datos relacionales. Conocimientos en Frameworks como Angular y Spring. Me comprometo a brindar todo el apoyo necesario para cumplir con todos los requerimientos.
\end{minipage}
}
\end{tcolorbox}

\begin{tcolorbox}[colframe=mybackground, colback=mybackground, boxrule=0.8mm, width=\textwidth, sharp corners]
{
\begin{minipage}[c]{0.3\textwidth}
\includegraphics[width=\linewidth]{src/img/integrantes/luis.jpeg}
\end{minipage}
\hfill
\begin{minipage}[c]{0.65\textwidth}
\textbf{Luis Eduardo Herrera González} \\
\textit{Ingeniero de Software} \\
Soy estudiante del séptimo ciclo de la carrera de Ingeniería de Software. Me apasiona el desarrollo de aplicaciones web y de escritorio eficientes, utilizando tecnologías modernas como Bun, Tauri y Lit. También cuento con experiencia en frameworks ampliamente adoptados como Next.js, Angular y Spring Boot. Además, tengo un gran interés en el área de Machine Learning, trabajando con CUDA, C++ y MLX para crear soluciones de alto rendimiento. Me considero una persona curiosa, enfocada en la innovación tecnológica y comprometida a aportar mis habilidades técnicas para el éxito del equipo.
\end{minipage}
}
\end{tcolorbox}

\begin{tcolorbox}[colframe=mybackground, colback=mybackground, boxrule=0.8mm, width=\textwidth, sharp corners]
{
\begin{minipage}[c]{0.3\textwidth}
\includegraphics[width=\linewidth]{src/img/integrantes/ariana.jpg}
\end{minipage}
\hfill
\begin{minipage}[c]{0.65\textwidth}
\textbf{Ariana Vargas Revollé} \\
\textit{Ingeniera de Software} \\
Soy estudiante de la carrera de Ingeniería de Software cursando actualmente el 7mo ciclo. Me interesa el rubro de ciberseguridad y me gusta leer sobre nuevas tecnologías y su impacto en la vida de las personas. Me gusta trabajar en equipo y aprender de otras personas
\end{minipage}
}
\end{tcolorbox}

\newpage

## Solution Profile

En la era de la hiperconectividad y las crecientes exigencias de seguridad, el transporte escolar enfrenta retos cada vez más complejos. Los métodos tradicionales de supervisión —basados en registros manuales, comunicación puntual y seguimiento reactivo— resultan insuficientes para garantizar la tranquilidad de las familias y el cumplimiento de los estándares de calidad por parte de las instituciones educativas y las empresas de transporte.

Frente a este escenario, es imprescindible adoptar un enfoque integral que combine innovación tecnológica y procesos colaborativos. El perfil de solución de CodeMinds se enmarca en esta visión: busca ofrecer un modelo escalable y flexible que facilite la gestión proactiva del transporte escolar, mejore la visibilidad de cada trayecto y promueva la rendición de cuentas en todos los niveles operativos.

Nuestra propuesta se fundamenta en la integración de tecnologías emergentes con plataformas digitales intuitivas, con el objetivo de optimizar la planificación, fortalecer la comunicación entre actores y elevar los estándares de seguridad y eficiencia. De esta manera, CodeMinds aspira a redefinir la forma en que colegios, operadores de transporte y familias interactúan con el servicio de traslado de estudiantes, construyendo un entorno de confianza y excelencia operativa.

![Recurso extraído de Canva](src/img/cap1/solution.png)

\newpage

### Antecedentes y problemática

RutaKids es una startup peruana enfocada en ofrecer soluciones tecnológicas para mejorar la seguridad y eficiencia del transporte escolar en colegios privados. Actualmente se encuentra en fase de desarrollo, trabajando en una plataforma digital que permitirá a los padres monitorear en tiempo real el trayecto de sus hijos, a los colegios gestionar sus rutas y asistencias, y a los operadores de transporte organizar sus unidades. Se están diseñando las primeras versiones funcionales de la app y el dashboard, así como realizando validaciones con usuarios reales para asegurar que el producto responda a necesidades concretas.


::: info
***What***

RutaKids es una plataforma digital compuesta por una app móvil y un sistema web que permite gestionar, monitorear y comunicar todo lo relacionado con el transporte escolar. Su objetivo es brindar seguridad a los padres, eficiencia a los colegios y organización a los operadores.
:::

::: info
***Why***

Porque los métodos tradicionales para supervisar el transporte escolar son ineficientes, generan desconfianza y no ofrecen trazabilidad. RutaKids responde a la necesidad de digitalizar este servicio para garantizar la seguridad de los estudiantes y optimizar la operación de colegios y transportistas.
:::

::: info
***Where***

Inicialmente en colegios privados de Lima Metropolitana, con proyección de expansión a otras ciudades del país conforme se valide el modelo. La plataforma es accesible desde cualquier dispositivo con conexión a internet.
:::

::: info
***When***

La fase de desarrollo ya está en marcha. Se proyecta iniciar pruebas piloto durante el próximo ciclo escolar y escalar la solución de forma progresiva en el primer año.
:::

::: info
***Who***

Un equipo multidisciplinario que lidera la creación de RutaKids, compuesto por desarrolladores, diseñadores UX, expertos en educación, y personal técnico que trabaja en conjunto con colegios y operadores reales durante la etapa de validación.
:::

::: attn
***How***

Mediante el desarrollo de una app para padres y operadores, un panel web para colegios, e integración con dispositivos de rastreo GPS. Se seguirán prácticas de diseño centrado en el usuario y validaciones iterativas para garantizar la adopción del sistema.

:::

::: attn
***How Much***

RutaKids funcionará bajo un modelo de suscripción mensual. Se ofrecerá un plan piloto gratuito, un plan básico escalable y un plan premium con funciones avanzadas como reportes personalizados y soporte extendido. El presupuesto inicial incluye el desarrollo tecnológico, pruebas con usuarios, instalación de GPS y mantenimiento del sistema.
:::

\newpage

### Lean UX Process.

![Recurso extraído de Google](src/img/cap1/LeanUXProcess.png)

#### Lean UX Problem Statements.

::: note

***Problem Statement***

- Hemos observado que los padres de familia no se sienten completamente seguros ni informados sobre el trayecto de sus hijos al utilizar el servicio de transporte escolar, lo que genera ansiedad, llamadas constantes al colegio y desconfianza en el sistema educativo.
¿Cómo podríamos mejorar la visibilidad en tiempo real y la comunicación con los padres para que nuestro servicio aumente la confianza, reduzca el tiempo de respuesta ante incidentes y eleve la satisfacción en al menos un 30%?\newline

- Hemos observado que las instituciones educativas privadas aún gestionan el transporte escolar mediante procesos manuales y canales de comunicación no integrados, lo que causa ineficiencias operativas, baja trazabilidad y riesgos en el cumplimiento de normas de seguridad.
¿Cómo podríamos mejorar la planificación de rutas y el monitoreo operativo para que los colegios gestionen el transporte de manera un 40% más eficiente y alineada a los estándares normativos?\newline

- Hemos observado que los operadores de transporte escolar no cuentan con herramientas digitales integradas para la gestión diaria de sus flotas, lo que conlleva a desorganización, rutas ineficientes y problemas de comunicación con padres y colegios.
¿Cómo podríamos ofrecer una solución que facilite la gestión proactiva de rutas y responsabilidades, para que los operadores puedan optimizar recursos y profesionalizar su servicio?\newline

- Hemos observado que el sistema actual de transporte escolar en colegios privados no cumple adecuadamente con las necesidades de seguridad, coordinación y monitoreo en tiempo real, lo que ocasiona desconfianza en las familias, sobrecarga administrativa en los colegios y exposición a riesgos operativos.
¿Cómo podríamos mejorar la eficiencia, transparencia y seguridad de la gestión del transporte escolar para que todos los actores involucrados se beneficien y nuestra plataforma se convierta en el nuevo estándar nacional de movilidad estudiantil segura?
:::

\newpage

#### Lean UX Assumptions.

***Business Assumptions***

**1. El cliente necesita** garantizar la seguridad, trazabilidad y puntualidad en el traslado escolar de los estudiantes, sin depender de procesos manuales o comunicación informal.

**2. Las necesidades del cliente se resolverán mediante** una plataforma digital con tecnología IoT que permita el monitoreo en tiempo real de las movilidades escolares, alertas automatizadas y reportes inteligentes.

**3. Los clientes son (o serán)** instituciones educativas privadas, padres de familia preocupados por la seguridad de sus hijos y operadores de transporte escolar que desean digitalizar sus procesos.

**4. El cliente quiere** confianza, visibilidad en tiempo real y simplicidad **de nuestro servicio**, asegurando que puedan reaccionar a tiempo ante cualquier eventualidad durante el trayecto escolar.

**5. El cliente también puede obtener** una mejora significativa en la eficiencia operativa, reducción de incidentes no reportados y cumplimiento normativo mediante la automatización de procesos y trazabilidad completa del servicio.

**6. Obtendré mi base de clientes mediante** alianzas con colegios privados, programas piloto gratuitos, y campañas en redes sociales dirigidas a padres y operadores.

**7. Ganaré dinero mediante** suscripciones mensuales o anuales para colegios y operadores, además de servicios adicionales premium para padres como notificaciones personalizadas y acceso extendido al historial de rutas.

**8. Mi principal competencia son** sistemas GPS genéricos, soluciones locales poco especializadas, y el uso tradicional de planillas, WhatsApp o llamadas para el seguimiento del transporte escolar.

**9. Superaremos a la competencia mediante** una solución específica para el ecosistema escolar peruano, con enfoque en seguridad, facilidad de uso, integración de IoT y cumplimiento con las normativas del sector educativo.

**10. Mi mayor riesgo es** que las instituciones educativas o los operadores no adopten la solución por falta de presupuesto, desconocimiento del valor agregado o resistencia al cambio tecnológico.

**11. Solucionaremos el riesgo mediante** demostraciones prácticas, soporte técnico continuo, acompañamiento en la implementación y evidencia del retorno de inversión desde los primeros meses de uso.

**12. ¿Cuáles son las suposiciones que, si se demuestran falsas, harán que el proyecto fracase?**

- Los colegios están dispuestos a adoptar tecnología para optimizar su sistema de transporte.
    
- Los padres realmente valoran la visibilidad y seguridad en tiempo real del traslado escolar.  
  
- Los operadores están dispuestos a digitalizar sus procesos si cuentan con capacitación y soporte adecuados.
\newline

***Business Outcomes***

- **Esperamos lograr un aumento del 30% en la percepción de seguridad por parte de los padres de familia.** Medido a través de encuestas antes y después del uso del sistema.

- **Esperamos reducir en un 40% el tiempo que los colegios invierten en planificar rutas de transporte.** Como indicador de eficiencia operativa directa.

- **Esperamos reducir en un 50% los incidentes no reportados o comunicados tardíamente.** Gracias al monitoreo en tiempo real y las alertas automáticas.

- **Queremos alcanzar al menos 15 colegios clientes en los primeros 12 meses.** Lo cual reflejará validación del modelo y su necesidad en el mercado.

- **Anticipamos una disminución del 35% en las llamadas de padres al colegio para consultar sobre el paradero del alumno.** Como señal de mayor confianza y transparencia del sistema.

- **Buscamos lograr que el 70% de las rutas activas estén digitalizadas en los primeros 3 meses de implementación.** Para evaluar adopción efectiva de la solución.

- **Proyectamos una tasa de retención superior al 25% entre colegios y operadores tras el primer ciclo escolar completo.** Como medida de sostenibilidad del producto.

- **Queremos que al menos el 90% de los choferes usen la app diariamente durante el primer mes de implementación.** Indicador de aceptación del sistema por parte del usuario operativo.\newline

***User Assumptions***

**1. ¿Quién es el usuario?**  

Padres de familia con hijos en colegios privados, directores o administradores escolares responsables de logística, y operadores de transporte escolar (choferes y supervisores).


**2. ¿Dónde encajaría nuestro producto en la vida (o trabajo) del usuario?**  

- Para los padres: en su rutina diaria, al momento de dejar o recoger a sus hijos, y al monitorear su ubicación en tiempo real desde el trabajo o casa.  
  
- Para el colegio: durante la planificación de rutas, control de asistencia y respuesta ante incidentes.  
  
- Para los operadores: en la gestión diaria del transporte, organización de rutas y coordinación con colegios y padres.

**3. ¿Qué problemas resuelve el producto para el usuario?**  

- Falta de visibilidad sobre el trayecto del alumno.  
  
- Comunicación tardía o inexistente en caso de desvíos o retrasos.  
  
- Desorganización y exceso de carga administrativa en la gestión del transporte escolar.  
  
- Inseguridad percibida por padres sobre el sistema de movilidad escolar.

**4. ¿En qué contexto utiliza el usuario el producto?**  

- Los padres acceden desde su celular durante el día para revisar notificaciones o localizar a sus hijos.  

- El colegio lo usa como plataforma de gestión diaria y monitoreo de flotas.  
  
- Los operadores acceden desde una app móvil antes y durante cada ruta.

**5. ¿Qué características son esenciales para el usuario? ¿Y por qué?**  

- **Ubicación en tiempo real**: los padres quieren saber dónde están sus hijos. 
   
- **Alertas automáticas de llegada y salida**: reduce la necesidad de llamar o preguntar. 
   
- **Dashboard de control para el colegio**: facilita la supervisión y planificación.  
  
- **Registro automático de asistencia**: mejora la trazabilidad.  
  
- **Interfaz simple e intuitiva**: todos los actores deben usarla sin necesidad de capacitación técnica avanzada.


**6. ¿Cómo debería verse y comportarse el producto?** 

- Diseño limpio, moderno y accesible desde cualquier dispositivo.  
  
- Navegación clara y rápida, con flujos sencillos para cada tipo de usuario.  
  
- La app debe abrirse y cargar la ubicación en segundos.  
  
- Debe emitir notificaciones discretas pero efectivas.  
  
- El administrador debe tener acceso inmediato a reportes y visualización de rutas.\newline

***User Outcomes***

- **Los padres quieren sentirse tranquilos** sabiendo que sus hijos están seguros durante el trayecto escolar, gracias a la visibilidad en tiempo real desde su celular.

- **Los colegios quieren reducir su carga operativa** automatizando la gestión de rutas, la asistencia y la comunicación con los padres, logrando una gestión más eficiente y moderna.

- **Los operadores de transporte quieren profesionalizar su servicio**, usando herramientas digitales que les permitan organizar mejor sus rutas, responder ante imprevistos y mejorar su relación con colegios y familias.

- **Los padres esperan recibir alertas inmediatas y confiables**, sin tener que llamar al colegio o depender de grupos de WhatsApp para saber si su hijo llegó bien.

- **Los usuarios valoran una solución fácil de usar**, que no requiera capacitación avanzada y funcione bien en dispositivos móviles de uso común.

- **Los directivos escolares desean contar con reportes visuales y automáticos**, que les permitan tomar decisiones informadas y cumplir con normativas del sector educativo.

- **Todos los usuarios esperan mayor transparencia**, trazabilidad y rapidez en la comunicación respecto al transporte escolar, mejorando la confianza en el sistema.

- **Los usuarios buscan una experiencia fluida**, sin errores ni demoras, que les permita integrarla fácilmente en su rutina diaria (desde la app o el panel web).\newline


***Features Assumptions***

**1. Visibilidad en tiempo real (Tracking GPS):**

- **Suposición:** Si los padres pueden ver la ubicación del vehículo en tiempo real, se sentirán más tranquilos y reducirán las llamadas al colegio.
  
- **Riesgo:** Si el tracking no es preciso o falla frecuentemente, los padres perderán confianza en la plataforma y volverán a métodos informales de consulta.


**2. Alertas automáticas de llegada y salida:**

- **Suposición:** Las notificaciones automáticas permitirán a los padres mantenerse informados sin necesidad de intervenir activamente.
  
- **Riesgo:** Si las alertas llegan con retraso o no son claras, los padres podrían considerarlas poco útiles y desactivar la función, perdiendo valor clave del producto.


**3. Registro automático de asistencia (RFID/NFC):**

- **Suposición:** Automatizar el registro de ingreso y salida de los estudiantes aumentará la seguridad y facilitará la trazabilidad para colegios y padres.
  
- **Riesgo:** Si el sistema no reconoce correctamente a los alumnos o es lento, se perderá confianza en su fiabilidad y será reemplazado por procesos manuales.


**4. Dashboard para colegios:**

- **Suposición:** Un panel de control centralizado facilitará la gestión de rutas, la visualización de reportes y la toma de decisiones operativas.
  
- **Riesgo:** Si el dashboard es complejo o poco intuitivo, el personal administrativo evitará usarlo y se limitarán sus beneficios.

**5. Aplicación móvil para padres y conductores:**

- **Suposición:** Una app con navegación simple y clara permitirá a los padres monitorear fácilmente y a los choferes operar sin distracciones ni errores.
  
- **Riesgo:** Si la app presenta fallos, consume muchos datos o requiere dispositivos de gama alta, su adopción será baja.


**6. Sistema de notificaciones configurables:**

- **Suposición:** Dar control al usuario sobre qué alertas recibir y cuándo aumentará la satisfacción y percepción de personalización.
  
- **Riesgo:** Si el sistema de configuración es complejo o no cumple con lo prometido, generará frustración y desuso de las notificaciones.

**7. Generación de reportes automáticos:**

- **Suposición:** Los colegios valorarán tener reportes listos para reuniones, auditorías o decisiones internas.
  
- **Riesgo:** Si los reportes no son claros, exportables o personalizables, se percibirán como inútiles y no se justificaría el valor del sistema.


**8. Integración con plataformas educativas o sistemas escolares:**

- **Suposición:** La posibilidad de integrarse con otros sistemas institucionales facilitará la adopción por parte de colegios ya digitalizados.
  
- **Riesgo:** Si la integración técnica es complicada o limitada, el sistema será considerado poco flexible o difícil de implementar.\newline


#### Lean UX Hypothesis Statements.

::: tip

**1. Creemos que lograremos** aumentar la satisfacción de los padres en un 30%. **Si** los padres preocupados por la seguridad de sus hijos **obtienen** visibilidad en tiempo real del trayecto escolar **con** una aplicación móvil intuitiva y notificaciones automáticas de llegada y salida.\newline

**2. Creemos que lograremos** reducir en un 40% la carga operativa en los colegios. **Si** los administradores escolares **obtienen** un dashboard centralizado para gestionar rutas, asistencia y reportes **con** una plataforma digital accesible y automatizada.\newline

**3. Creemos que lograremos** incrementar la adopción del sistema en un 25% durante el primer año. **Si** los colegios y operadores de transporte **obtienen** una solución flexible, con soporte técnico y demostraciones prácticas **con** planes accesibles y personalización para su realidad operativa.\newline

**4. Creemos que lograremos** disminuir en un 50% los incidentes no reportados. **Si** los padres y el personal del colegio **obtienen** alertas automáticas y acceso inmediato a la ubicación de las movilidades **con** tecnología IoT conectada a la plataforma.\newline

**5. Creemos que lograremos** lograr una tasa de retención superior al 25% tras el primer ciclo escolar. **Si** colegios y operadores que implementan la plataforma **obtienen** mejoras medibles en eficiencia, confianza de los padres y cumplimiento normativo **con** funcionalidades personalizadas y soporte continuo.
:::

\newpage

#### Lean UX Canvas.

![Artefacto creado en Figma [URL](https://www.figma.com/design/K3gw63Gdzr8KOgE32BgreJ/Lean-UX-Canvas-Template-by-Jeff-Gothelf-(Community)?node-id=0-1&t=q5cZNvpSyA30WQQd-1)](src/img/cap1/LeanUXCanvas.pdf) 

\newpage

## Segmentos objetivo.

En esta sección se identifican los segmentos objetivos clave a los que está dirigida la solución de RutaKids. A través del análisis de variables demográficas, educativas y conductuales, se definen los perfiles de usuarios que interactúan con el sistema de transporte escolar. Este enfoque permite diseñar una solución centrada en las personas, asegurando que cada funcionalidad responda a las necesidades reales de padres, personal escolar y operadores de transporte.

![Artefacto creado en Figma [URL](https://www.figma.com/design/K3gw63Gdzr8KOgE32BgreJ/Lean-UX-Canvas-Template-by-Jeff-Gothelf--Community-?node-id=2015-2&t=urisk948grqgcqCL-1)](src/img/cap1/SegmentoObjetivo1.pdf) 

![Artefacto creado en Figma [URL](https://www.figma.com/design/K3gw63Gdzr8KOgE32BgreJ/Lean-UX-Canvas-Template-by-Jeff-Gothelf--Community-?node-id=2015-2&t=urisk948grqgcqCL-1)](src/img/cap1/SegmentoObjetivo2.pdf) 

\newpage

# Capítulo II: Requirements Elicitation & Analysis

Antes de construir una solución tecnológica efectiva, es esencial entender a fondo el problema, a los usuarios y el entorno en el que la solución será implementada. Este capítulo presenta el proceso de Requirements Elicitation & Analysis, una fase crítica en el desarrollo de soluciones centradas en el usuario. Aquí se identifican y analizan las necesidades del público objetivo, se estudia a la competencia y se utilizan técnicas como entrevistas, mapeo de tareas y escenarios para definir con claridad los requisitos funcionales y no funcionales del sistema. La información obtenida en esta etapa servirá como base sólida para el diseño e implementación de un producto alineado con las expectativas del mercado y con alto impacto en su adopción y uso.

\newpage

## Competidores.

![Recurso extraído de Canva](src/img/cap2/competidores-introduccion.png)

En un mercado donde la seguridad escolar, la eficiencia operativa y la comunicación con los padres se han convertido en prioridades fundamentales, contar con herramientas tecnológicas ya no es una opción, sino una necesidad. Por ello, es imprescindible realizar un análisis detallado de las soluciones existentes, que permita identificar áreas de mejora, oportunidades de diferenciación y enfoques innovadores capaces de posicionar a RutaKids como una opción estratégica para las instituciones educativas que buscan modernizar sus servicios de transporte.

\newpage

**Competidores:**

- ***Ultravision:*** Este servicio ofrece una solución modular para el control y seguimiento de transporte escolar mediante GPS y dispositivos embarcados. Sus herramientas permiten gestionar estudiantes en tiempo real, emitir alertas y generar reportes detallados de asistencia y rutas. Está orientado principalmente a instituciones que buscan trazabilidad y control de flotas.

![Imagen extraída de Ultravision [(URL)](https://www.ulvisions.com/es/ultravision-school-bus-solution)](src/img/cap2/ultravision-landing.png)

\vspace{1em}

- ***CalAmp:*** Es una empresa internacional especializada en soluciones de telemetría y gestión de flotas. Aunque su enfoque no es exclusivamente escolar, su plataforma permite el monitoreo en tiempo real de vehículos, alertas automáticas y reportes de desempeño, siendo utilizada por operadores de transporte escolar a gran escala.

![Imagen extraída de CalAmp [(URL)](https://www.calamp.com/es/)](src/img/cap2/calAmp-landing.png)


\newpage

- ***Satgeo:*** Es una plataforma latinoamericana orientada al control del transporte escolar. Integra una aplicación para padres, panel de administración para instituciones educativas y funciones automatizadas de asistencia. Su enfoque regional le permite adaptarse fácilmente a contextos locales.

![Imagen extraída de Satgeo [(URL)](https://satgeo.com/control-de-estudiantes)](src/img/cap2/satgeo-landing.png)
\vspace{1em}

- ***BusWhere:*** Es una solución enfocada en el rastreo de autobuses escolares. Ofrece una aplicación para padres y un sistema de visualización en la nube para escuelas, que permite conocer en tiempo real la ubicación de los estudiantes. Se destaca por su interfaz simple, alertas de llegada y experiencia amigable.

![Imagen extraída de BusWhere [(URL)]( https://www.buswhere.com/es/solutions-for-schools )](src/img/cap2/buswhere-landing.png)

\newpage

### Análisis competitivo.

Tras haber identificado a los principales actores en el ámbito del transporte escolar inteligente, se presenta a continuación un análisis comparativo que permite evaluar sus propuestas de valor. Este análisis se enfoca en aspectos clave como el enfoque de mercado, funcionalidades principales, diferenciadores y grado de especialización. La finalidad es identificar patrones, ventajas competitivas y posibles áreas de oportunidad que orienten el posicionamiento estratégico de nuestra solución.

![](src/img/cap2/analisisCompetitivo_1.png)

![](src/img/cap2/analisisCompetitivo_2.png)

![](src/img/cap2/analisisCompetitivo_3.png)

\newpage

### Estrategias y tácticas frente a competidores.

En el dinámico entorno empresarial actual, la formulación de estrategias efectivas requiere una comprensión profunda de las capacidades internas de la organización y de las condiciones del entorno. 

\begin{quote}
Según Tarziján (2019), la formulación de la estrategia comienza con el análisis del entorno de la empresa desde el punto de vista de debilidades, fortalezas, oportunidades y amenazas, evaluando la preparación de la empresa para competir en el mercado. 
\end{quote}

\vspace{1em}

Este enfoque permite a las organizaciones identificar oportunidades de diferenciación, anticipar los movimientos de la competencia y tomar decisiones fundamentadas para asegurar su sostenibilidad y crecimiento.

En el caso de RutaKids, una solución tecnológica orientada al transporte escolar seguro y eficiente, el análisis competitivo previamente desarrollado ha permitido comprender mejor el posicionamiento de los actores clave del mercado, así como detectar espacios estratégicos aún poco explotados.

Sobre esta base, se presentan a continuación las estrategias competitivas clave y las tácticas específicas propuestas para fortalecer la posición de RutaKids, tanto frente a la competencia actual como ante las exigencias emergentes del sector.

\vspace{1em}

**Estrategias competitivas para** ***RutaKids***

\vspace{1em}

::: box
**Innovación tecnológica centrada en la seguridad escolar:**
:::

**Estrategia:** *RutaKids*  debe consolidarse como una solución más allá del rastreo vehicular tradicional, posicionándose como un ecosistema tecnológico que automatiza procesos críticos como la asistencia estudiantil, el control de ingreso y el monitoreo predictivo de rutas. Anticiparse a las demandas del sistema educativo digital será clave para mantener su ventaja competitiva.

**Tácticas propuestas:**

   - Incorporar funcionalidades avanzadas como geocercas inteligentes, alertas automatizadas y análisis de comportamiento de rutas.
  
   - Invertir en I+D para desarrollar módulos complementarios de control escolar y generación de reportes para autoridades educativas.

   - Establecer un ciclo de actualizaciones periódicas basado en retroalimentación de usuarios (padres, instituciones, transportistas).

\vspace{2em}

::: box
**Segmentación según perfil institucional:**
:::
   
**Estrategia:** La propuesta de *RutaKids* debe adaptarse a distintos perfiles del sector educativo: desde pequeñas instituciones rurales hasta redes educativas privadas o municipalidades. La flexibilidad funcional y comercial es clave para responder a sus diversas realidades operativas.



**Tácticas propuestas:**

   - Diseñar planes escalables ajustados al número de estudiantes, unidades vehiculares o zonas geográficas.
  
   - Adaptar rutas, calendarios y funcionalidades según las particularidades culturales y logísticas de cada región.
  
   - Desarrollar campañas diferenciadas según el público objetivo: directores, asociaciones de padres, municipios o empresas de transporte.

\vspace{2em}

::: box
**Construcción de redes y alianzas estratégicas:**
:::
   
**Estrategia:** *RutaKids* debe fortalecer su presencia a través de alianzas con actores clave del ecosistema educativo y tecnológico, que le permitan ampliar su alcance, aumentar su credibilidad y facilitar procesos de adopción institucional.

**Tácticas propuestas:**

   - Establecer convenios con UGELs, DREs y gobiernos locales para implementación en zonas piloto.
  
   - Integrarse con operadores de transporte escolar mediante acuerdos de uso conjunto de plataforma.

   - Vincularse con soluciones EdTech existentes para ofrecer paquetes integrados (gestión escolar, pagos, comunicaciones).

\newpage

::: box
**Escalamiento regional con visión latinoamericana:**
:::
   
**Estrategia:** Una vez consolidada su presencia en el mercado nacional, *RutaKids* debe proyectarse hacia mercados latinoamericanos con necesidades similares de modernización y digitalización del transporte escolar.

**Tácticas propuestas:**

   - Realizar estudios comparativos para identificar países con alto potencial de adopción (como Bolivia, Ecuador o Colombia).
  
   - Asegurar la adecuación de la plataforma a marcos normativos y culturales de cada país.
  
   - Aplicar un modelo de expansión progresiva basado en aliados comerciales o distribuidores locales.

\newpage

**Tácticas Específicas para para el Fortalecimiento de *RutaKids***

\vspace{1em}

::: box
**Marketing Diferenciado y Posicionamiento Estratégico**
:::

**Táctica:**  
Desarrollar una identidad de marca clara y confiable que refleje el compromiso de RutaKids con la seguridad escolar y la transformación digital, destacando sus beneficios tecnológicos y sociales frente a la competencia.

**Acciones:**

  - Crear contenido audiovisual y gráfico que ilustre, desde casos reales, el impacto positivo del sistema en la comunidad educativa.

  - Participar en eventos del sector educativo y tecnológico para aumentar visibilidad institucional y generar alianzas estratégicas.

  - Adaptar los mensajes de comunicación según el perfil del usuario (padres, colegios, transportistas), destacando el valor específico para cada grupo.

\vspace{2em}

::: box
**Monitoreo Competitivo Continuo**
:::

**Táctica:**  
Establecer un sistema sistemático de vigilancia del entorno competitivo para anticipar cambios en el mercado, identificar oportunidades de innovación y ajustar la estrategia de RutaKids en tiempo real.

**Acciones:**

  - Comparar periódicamente precios, funcionalidades y propuestas de valor de competidores locales y regionales.

  - Analizar tendencias emergentes en tecnología educativa y movilidad escolar para detectar innovaciones aplicables.
  
  - Realizar sesiones de benchmarking cada trimestre para revisar la posición de RutaKids y actualizar su hoja de ruta comercial y técnica.

\newpage

::: box
**Optimización continua de la experiencia de usuario (UX)**
:::

**Táctica:** Priorizar la mejora continua de la experiencia de usuario en sus plataformas digitales, garantizando interfaces intuitivas, accesibles y funcionales para todos los actores involucrados: padres, instituciones educativas y transportistas.  

**Acciones:**

   - Establecer canales permanentes de retroalimentación dentro de la aplicación, permitiendo recoger sugerencias, reportes de errores y valoraciones del uso.

   - Realizar pruebas de usabilidad periódicas con usuarios reales de diferentes perfiles socioeducativos, considerando variables como edad, nivel de alfabetización digital y contexto urbano o rural.

   - Ajustar la interfaz gráfica y la arquitectura de navegación con base en los resultados obtenidos, incorporando elementos visuales claros y accesibles, así como funciones simplificadas para usuarios con menor familiaridad tecnológica.

\vspace{2em}

::: box
**Estructuración flexible de precios y modelos comerciales**
:::

**Táctica:** Implementar un modelo de precios adaptable que se ajuste a las capacidades presupuestales y necesidades funcionales de los distintos tipos de instituciones educativas.

**Acciones:**

   - Diseñar planes escalables que se ajusten a variables como el número de estudiantes, unidades vehiculares o características del servicio contratado.

   - Establecer esquemas de descuentos por contratación anual, licencias por volumen o implementación a nivel de red educativa.

   - Considerar la introducción de un modelo freemium con funcionalidades básicas disponibles sin costo durante un periodo limitado, como estrategia de entrada para instituciones que aún evalúan la solución.

\newpage

::: box
**Fortalecimiento de la fidelización institucional y del vínculo con los usuarios:**
:::

**Táctica:** Implementar una estrategia orientada a consolidar relaciones de largo plazo con las instituciones educativas y las familias usuarias del servicio.

**Acciones:**

   - Diseñar e implementar un programa de referidos institucionales, ofreciendo beneficios económicos o acceso a funciones premium a aquellas escuelas que recomienden RutaKids a otras entidades educativas.

   - Brindar capacitaciones periódicas y soporte técnico activo al personal administrativo y operativo, promoviendo un uso eficiente y sostenido de la plataforma.

   - Establecer un sistema de comunicaciones personalizadas que incluya reportes mensuales, alertas relevantes y sugerencias prácticas para mejorar la experiencia de uso en función del perfil del usuario (padres, directores o transportistas).


\newpage

## Entrevistas.
Las entrevistas están diseñadas para recolectar tanto información objetiva (edad, zona de residencia, ocupación, uso de tecnología) como subjetiva (motivaciones, frustraciones, percepción de seguridad), fundamentales para la construcción de arquetipos (User Personas), Empathy Maps y Journey Maps.

![Recurso extraído de Canva](src/img/cap2/entrevistas-introduccion.png)

::: note
Para acceder al video de las entrevistas, haga click en la [URL]( )
:::

\newpage

### Diseño de entrevistas.

Para el diseño de las entrevistas se definieron dos segmentos objetivo con perfiles claramente diferenciados: Padres de familia con hijos en edad escolar y Directivos escolares o personal administrativo. 

::: box
**Segmento Objetivo 1:** Directivos escolares o personal administrativo
:::

**Objetivo:**

Explorar el rol real del colegio en la movilidad escolar, identificar brechas de control y comunicación, y conocer la apertura institucional hacia soluciones tecnológicas que podrían profesionalizar el servicio.


**Perfil general**

1) ¿Podría indicarnos su nombre, edad y cargo dentro de la institución?

2) ¿En qué distrito se ubica el colegio y qué tipo de gestión tiene (pública, privada, parroquial, comunitaria)?

**Gestión actual del transporte escolar**

3) ¿Cómo está organizado actualmente el transporte escolar en su colegio? ¿Quiénes definen y gestionan los aspectos clave como rutas, horarios y selección de choferes?

4) ¿Qué grado de participación tiene la institución en ese proceso? ¿El colegio interviene directamente o actúa más como facilitador?

5) ¿Cómo se asegura el colegio de que los alumnos lleguen y regresen correctamente? ¿Se registra de alguna forma esta información?

6) ¿Qué herramientas o canales utilizan para coordinar el servicio (por ejemplo, WhatsApp, Excel, llamadas)? ¿Han intentado implementar alguna solución digital?

7) ¿Qué problemas o limitaciones han identificado con el modelo actual (por ejemplo, falta de trazabilidad, dependencia del chofer, poca coordinación)?


**Comunicación con familias y manejo de incidentes**

8) ¿Cómo se informa a los padres sobre retrasos, cambios de ruta o emergencias? ¿Quién suele encargarse de comunicar estas situaciones?

9) ¿Se presentan con frecuencia incidentes o reclamos relacionados al transporte? ¿En qué casos suele intervenir el colegio?

10) ¿Qué tan tranquilos cree que se sienten los padres con el sistema actual? ¿Le han transmitido preocupaciones?

**Interés y apertura hacia soluciones tecnológicas**

11) ¿Han evaluado antes alguna solución digital para mejorar la coordinación del transporte? ¿Cuál fue su experiencia?

12) ¿Qué funcionalidades considera prioritarias en una plataforma para la movilidad escolar?
   - Seguimiento del bus en tiempo real
   - Notificaciones automáticas de subida/bajada
   - Registro de asistencia
   - Reportes para la institución
   - Panel de control para padres y colegio


13) ¿Qué beneficios cree que una app así traería a su comunidad educativa?

14) ¿Qué obstáculos ve para su implementación (por ejemplo, acceso a internet, costos, resistencia de padres o choferes)?

\newpage

::: box
**Segmento Objetivo 2:** Padres de familia con hijos en edad escolar
:::

**Objetivo:**  
Entender cómo los padres viven la experiencia del transporte escolar, sus niveles de confianza, frustraciones actuales, apertura a soluciones digitales y disposición a pagar por servicios que mejoren seguridad y tranquilidad.

**Perfil general** 

1) ¿Cuál es tu nombre, edad y ocupación?

2) ¿Cuántos hijos tienes y en qué niveles educativos están?

3) ¿Usan actualmente movilidad escolar? ¿Cuántos días a la semana?

**Comunicación y seguimiento actual**  

4) ¿Cómo te enteras si tu hijo(a) llegó al colegio o a casa?

5)  ¿Quién suele avisarte si hay algún retraso o imprevisto con el transporte?

6) ¿En qué momento del día sueles preocuparte más por la movilidad escolar: al dejarlo/a, al recogerlo/a o en todo momento?

7) ¿Cuál ha sido la situación más preocupante que has vivido con la movilidad escolar?

**Percepción del servicio actual** 

8) ¿Cómo calificarías el servicio de movilidad actual en cuanto a seguridad, puntualidad y comunicación? (0 al 10, justifica)

9) ¿Qué es lo que menos te gusta o lo que cambiarías de inmediato?


**Uso y apertura a tecnología** 

10) ¿Qué tipo de celular usas actualmente? (Marca/modelo si sabes, y si es Android o iPhone)

11) ¿Usas apps regularmente para comunicarte con el colegio? ¿Cuáles y para qué?

12) ¿Te gustaría poder seguir el trayecto de tu hijo(a) en tiempo real? ¿Por qué?

13) Si pudieras recibir alertas automáticas (subida, bajada, llegada), ¿te sería útil o sientes que sería demasiado?

**Confianza y percepción de seguridad** 

14) ¿Qué es lo que más te genera desconfianza en el sistema actual?

15) ¿Qué tendría que pasar para que dejaras de usar la movilidad actual?

16) ¿Confías más en el chofer, la institución, o en algún sistema de control adicional?

**Valor percibido y disposición de pago** 

17) Si una solución digital te brindara tranquilidad, ¿estarías dispuesto/a a pagar por ella?

18) ¿Qué características tendría que tener para que sientas que vale lo que cuesta?

19) ¿Prefieres que lo gestione directamente el colegio o que sea una opción contratada por los padres?

20) Imagina el sistema de movilidad ideal:
  - ¿Cómo te informaría?
  - ¿Qué verías en tu celular?
  - ¿Qué podrías controlar tú?


\newpage

### Registro de entrevistas.

::: box
**Segmento Objetivo 1:** Directivos escolares o personal administrativo
:::

**Entrevista #1**

\begin{table}[H]
\begin{center}
\begin{tabular}{|p{5cm}|p{6cm}|}
\hline
\textbf{Nombre y Apellido}    & Max Paul Ramos Chupitazzi \\ \hline
\textbf{Edad}                 & 55 años                   \\ \hline
\textbf{Ubicación geográfica} & Paiján, Ascope, La Libertad, Perú \\ \hline
\textbf{Cargo}                & Docente de secundaria y asesor tecnológico \\ \hline
\textbf{Tiempo de entrevista} & 00:00 - 00:00             \\ \hline
\end{tabular}
\end{center}
\end{table}

**Resumen de la entrevista**

Max Paul Ramos Chupitazzi, docente de matemáticas y asesor tecnológico, señala que el colegio donde trabaja no cuenta con un sistema propio de transporte escolar. Actualmente, la responsabilidad recae enteramente en los padres, quienes contratan transportes de forma independiente y sin supervisión de la institución. Esto genera una serie de problemas: falta de puntualidad, ausencia de control de asistencia, y condiciones inseguras en los vehículos, muchos de los cuales carecen de seguro y operan con sobrecupo.
El colegio ha detectado una necesidad urgente de implementar un sistema institucional de transporte, especialmente para estudiantes que provienen de distritos cercanos como Rázuri y Macaví. Se ha planteado la adquisición de unidades propias, lo cual permitiría garantizar la seguridad de los alumnos, asegurar la puntualidad y mejorar la percepción del colegio ante la comunidad.
Actualmente, el colegio utiliza un sistema de photochip para controlar el ingreso de los estudiantes, lo que permite identificar ausencias tempranas. Sin embargo, no existe ningún control al abordar o descender del transporte escolar, lo que ha causado incidentes preocupantes, como el caso de una estudiante que terminó en otra ciudad sin ser detectada.
El entrevistado propone un sistema tecnológico que permita el registro digital de embarque y desembarque mediante códigos de barras, notificaciones automáticas a los padres, y una app o panel de control para el monitoreo en tiempo real. Destaca que esto brindaría beneficios como: Mayor seguridad y tranquilidad para las familias,  fidelización de los padres hacia la institución y una reputación positiva del colegio como espacio moderno y confiable.
El principal obstáculo para la implementación es el costo adicional para las familias, aunque considera que si el incremento no es excesivo, los padres estarían dispuestos a asumirlo a cambio de mayor seguridad.

![Imagen extraída del video de entrevistas](src/img/cap2/EntrevistaPaul.png)

\newpage

**Entrevista #2**

\begin{table}[H]
\begin{center}
\begin{tabular}{|p{5cm}|p{6cm}|}
\hline
\textbf{Nombre y Apellido}    & Juliana Chávez \\ \hline
\textbf{Edad}                 & 32 años                   \\ \hline
\textbf{Ubicación geográfica} & Paiján, Ascope, La Libertad, Perú \\ \hline
\textbf{Cargo}                & Directora de institución educativa privada \\ \hline
\textbf{Tiempo de entrevista} & 00:00 - 00:00             \\ \hline
\end{tabular}
\end{center}
\end{table}

**Resumen de la entrevista**

Juliana Chávez, directora de una institución educativa privada en Paiján, explica que actualmente no cuentan con un sistema de transporte escolar institucional. La organización del traslado de los alumnos recae completamente en los padres, quienes contratan por su cuenta movilidades desde distintas zonas como Puerto Malabrigo, Casagrande, Chiclín y Chumpón.
La institución se encarga de definir los horarios escolares, pero no participa en la selección de choferes, rutas o tarifas. Las movilidades contratadas llegan hasta la puerta del colegio, donde auxiliares y porteros reciben a los estudiantes, y a la salida los acompañan hasta que aborden.
Uno de los problemas identificados es la falta de respuesta rápida en caso de emergencias médicas. Si un estudiante se enferma durante el horario escolar, la movilidad no puede recogerlo, por lo que deben llamar a los padres, lo que puede generar complicaciones si no hay quien lo recoja de inmediato.
Aunque no han recibido reclamos formales por parte de los padres sobre el transporte, existen comentarios informales sobre la posibilidad de que el colegio implemente su propia movilidad, lo que, según la directora, aumentaría la seguridad y tranquilidad de las familias.
Juliana considera que sería muy útil implementar una aplicación o plataforma digital para monitorear en tiempo real el transporte escolar. Esta permitiría:

   - Ver si los alumnos subieron o no a la movilidad.
   - Notificar a los padres en caso de desvíos o incidentes.
   - Usar un sistema tipo GPS que registre las rutas y desplazamientos.

En cuanto a la viabilidad de este tipo de solución, cree que los padres estarían dispuestos a pagar por ella, siempre que el costo no sea mayor que el actual. Destaca que sería una inversión valiosa tanto para el bienestar emocional de los padres como para la imagen y compromiso del colegio.

![Imagen extraída del video de entrevistas](src/img/cap2/EntrevistaJuliana.png)

\newpage

**Entrevista #3**

\begin{table}[H]
\begin{center}
\begin{tabular}{|p{5cm}|p{6cm}|}
\hline
\textbf{Nombre y Apellido}    & Graciela Rios Alza \\ \hline
\textbf{Edad}                 & 52 años                   \\ \hline
\textbf{Ubicación geográfica} & Paiján, Ascope, La Libertad, Perú \\ \hline
\textbf{Cargo}                & Promotora de institución educativa \\ \hline
\textbf{Tiempo de entrevista} & 00:00 - 00:00             \\ \hline
\end{tabular}
\end{center}
\end{table}

**Resumen de la entrevista**

Graciela Rios Alza se desempeña como promotora en una institución educativa de Paiján, donde observa de cerca las dinámicas del transporte escolar. Actualmente, la movilidad de los estudiantes es gestionada por terceros, especialmente combis que llegan desde distritos cercanos como Puerto Malabrigo. La institución no cuenta con un sistema de transporte propio, ni tecnología para monitorear en tiempo real los viajes.
Aunque el colegio establece los horarios de entrada y salida, no interviene en la organización ni supervisión del transporte escolar: ni en rutas, ni en selección de choferes, ni en el control de asistencia. La única comunicación activa ocurre cuando:
   - El conductor se comunica con el colegio para avisar retrasos por problemas como llantas pinchadas.
   - Los padres avisan si un alumno no asistirá.
Todo el proceso es manual y reactivo, sin herramientas tecnológicas. No existe un sistema para confirmar si los alumnos llegaron o regresaron, y no se registra asistencia al abordar o descender de los vehículos. Esto ha llevado a situaciones preocupantes: algunos estudiantes no fueron recogidos a la salida, obligando al conductor a regresar al colegio por ellos tras ser olvidados.
Graciela señala que los padres se mantienen constantemente preocupados por la seguridad del traslado de sus hijos, y que no se sienten completamente tranquilos con el sistema actual. Aunque no hay una cantidad alta de reclamos formales, sí se han reportado fallas mecánicas y descuidos logísticos.
A pesar de que no se ha usado nunca un sistema digital para la gestión del transporte, Graciela ve con buenos ojos la implementación de una aplicación tecnológica que permita:
   - Notificar automáticamente cuando los niños llegan al colegio o están en camino a casa.
   - Proveer información en tiempo real sobre el trayecto.
   - Permitir a los padres confirmar si enviarán a su hijo o no, facilitando la gestión administrativa del colegio.
También menciona que el uso de este tipo de tecnología sería bien recibido por los padres, especialmente aquellos que dependen del transporte escolar diariamente. Considera que esto mejoraría la seguridad y la tranquilidad emocional tanto de los padres como del personal educativo.
Está convencida de que sería viable implementar esta solución en su colegio y que beneficiaría directamente a varias áreas institucionales, como administración, psicología y auxiliares, al mejorar la organización, la comunicación y la prevención de incidentes.


![Imagen extraída del video de entrevistas](src/img/cap2/EntrevistaRocio.png)

\newpage


::: box
**Segmento Objetivo 2:** Padres de familia con hijos en edad escolar
:::

**Entrevista #1**

\begin{table}[H]
\begin{center}
\begin{tabular}{|p{5cm}|p{6cm}|}
\hline
\textbf{Nombre y Apellido}    & Gabriela Ríos Lazaro \\ \hline
\textbf{Edad}                 & 52 años                   \\ \hline
\textbf{Ubicación geográfica} & Trujillo, La libertad \\ \hline
\textbf{Ocupación}            & Obstetra \\ \hline
\textbf{Relación con la educación} & Madre de un estudiante de secundaria \\ \hline
\textbf{Tiempo de entrevista} & 00:00 - 00:00             \\ \hline
\end{tabular}
\end{center}
\end{table}

**Resumen de la entrevista**

Gabriela Ríos es madre de un estudiante de nivel secundario que utiliza un servicio de movilidad escolar privado de lunes a viernes. Aunque no recibe notificaciones diarias sobre la llegada de su hijo al colegio, confía en el conductor con el que ha establecido un acuerdo de transporte. La comunicación es directa, principalmente mediante llamadas en caso de imprevistos, como fallas menores del vehículo.
En su experiencia, nunca ha tenido un incidente grave relacionado al transporte, aunque reconoce que ha habido ocasiones donde ha tenido que comunicarse por su cuenta para confirmar el paradero de su hijo. La movilidad cuenta con una persona encargada que apoya a los estudiantes durante el trayecto, lo cual le brinda seguridad adicional.
Gabriela califica el servicio actual con un 8 sobre 10. El motivo de esta calificación se relaciona con un ajuste logístico reciente: debido a que el conductor asumió una nueva ruta para otro colegio, su hijo comenzó a ser dejado a unas cuadras de casa en lugar del domicilio exacto. Aun así, al tratarse de un adolescente y contar con su autorización previa, no lo considera un problema crítico ni un motivo para cambiar de proveedor, resaltando la responsabilidad y confiabilidad del conductor.
En cuanto a mejoras al sistema actual, Gabriela está completamente a favor de que el colegio implemente su propio sistema de transporte escolar, respaldado por una aplicación digital que permita monitorear el trayecto en tiempo real. Considera que sería una forma efectiva de asegurar que los estudiantes llegan bien a su destino y retornan sin incidentes. Además, resalta que muchas familias no tienen la posibilidad de recoger personalmente a sus hijos y dependen del transporte contratado.
Está dispuesta a pagar un costo adicional por un servicio así, siempre que venga respaldado por el colegio, que considera más preparado que los grupos de padres para seleccionar personal capacitado y prudente. Subraya que, así como confían en las escuelas para contratar buenos docentes, también deberían poder confiar en que contraten buenos conductores.
Finalmente, considera que lo más importante en una solución tecnológica de este tipo es:
   - Confirmar la llegada del alumno al colegio y su retorno al hogar.
   - Notificaciones automáticas en caso de desvíos o emergencias.
   - Gestión directa desde la institución, para mayor confianza y profesionalismo.

![Imagen extraída del video de entrevistas](src/img/cap2/EntrevistaGabriela.png)

\newpage

**Entrevista #2**

\begin{table}[H]
\begin{center}
\begin{tabular}{|p{5cm}|p{6cm}|}
\hline
\textbf{Nombre y Apellido}    & Zoila Lescano Nureña \\ \hline
\textbf{Edad}                 & 43 años                   \\ \hline
\textbf{Ubicación geográfica} & Trujillo, La libertad \\ \hline
\textbf{Ocupación}            & Obstetra \\ \hline
\textbf{Relación con la educación} & Madre de cuatro hijos (tres en primaria y una bebé) \\ \hline
\textbf{Tiempo de entrevista} & 00:00 - 00:00             \\ \hline
\end{tabular}
\end{center}
\end{table}

**Resumen de la entrevista**

Zoila Lescano Nureña es madre de cuatro hijos, tres de ellos actualmente cursando primaria. En el pasado, sus hijos utilizaron movilidad escolar tradicional, compartida con otros estudiantes. Sin embargo, cambió a un servicio de taxi particular exclusivo para sus tres hijos debido a preocupaciones por la logística y los horarios inflexibles de la movilidad escolar.
Según Zoila, las movilidades compartidas recogían a los niños muy temprano y los devolvían a casa muy tarde, debido a la necesidad de recoger a varios estudiantes en diferentes puntos. Esta situación le generaba preocupación diaria, y por ello optó por una alternativa más personalizada y eficiente.
Actualmente, el servicio de taxi contratado ofrece una experiencia altamente satisfactoria:

   - El conductor informa detalladamente los horarios de recogida y llegada.
   - La familia cuenta con comunicación directa constante.
   - Considera que la seguridad, puntualidad y trato son excelentes.

Aunque se siente tranquila con la situación actual, Zoila apoya la idea de implementar tecnología adicional para monitorear los desplazamientos escolares. En particular, valoraría una aplicación conectada a dispositivos como pulseras escaneables que envíen alertas al celular en tiempo real sobre:

   - Abordaje y bajada del transporte.
   - Notificaciones de incidentes o retrasos.
   - Seguimiento de ruta sin necesidad de comunicación directa con el conductor.

Además, considera que esta solución debería ser promovida e implementada por el colegio como parte de su compromiso con la seguridad estudiantil. Sugiere que esté disponible para las familias que quieran adoptarla, destacando que no todos los padres tienen el tiempo ni los medios para estar al tanto constantemente del transporte de sus hijos.
Zoila estaría dispuesta a pagar un costo adicional por este servicio digital, siempre que garantice mayor tranquilidad, especialmente en contextos de inseguridad o posibles emergencias. También propone que la aplicación incorpore una señal de alarma o alerta que los niños puedan activar si algo inusual ocurre durante el trayecto.

![Imagen extraída del video de entrevistas](src/img/cap2/EntrevistaZoila.png)

\newpage

**Entrevista #3**

\begin{table}[H]
\begin{center}
\begin{tabular}{|p{5cm}|p{6cm}|}
\hline
\textbf{Nombre y Apellido}    & Hayle Ascoy Varas \\ \hline
\textbf{Edad}                 & 40 años                   \\ \hline
\textbf{Ubicación geográfica} & Paiján, Ascope, La Libertad \\ \hline
\textbf{Ocupación}            & Docente \\ \hline
\textbf{Relación con la educación} & Madre de una niña en tercer grado de primaria \\ \hline
\textbf{Tiempo de entrevista} & 00:00 - 00:00             \\ \hline
\end{tabular}
\end{center}
\end{table}

**Resumen de la entrevista**

Hayle Ascoy Varas, docente y madre de una niña de tercer grado, utiliza movilidad escolar privada de lunes a viernes. Aunque el servicio es funcional y el conductor es una persona en quien confía por su buen trato y responsabilidad, Hayle manifiesta una preocupación constante por la falta de seguimiento en tiempo real del traslado de su hija. La comunicación depende exclusivamente del celular del chofer, quien no siempre responde de inmediato, lo que la obliga a insistir para confirmar si su hija ha llegado al colegio o a casa.
Ha experimentado situaciones de incertidumbre debido a retrasos ocasionados por fallas mecánicas o falta de gasolina, sin previo aviso. Si bien califica el servicio actual como más seguro que en el pasado, afirma que dejaría de usarlo si la puntualidad se ve afectada o si pierde transparencia en la comunicación directa.
En un intento anterior por monitorear a su hija, utilizó un reloj GPS, pero dejó de hacerlo por restricciones del colegio y porque el dispositivo era fácilmente manipulado por la niña. Actualmente, no utiliza aplicaciones escolares específicas, y se comunica con el colegio únicamente vía WhatsApp con tutoras o la secretaría.
Hayle estaría dispuesta a pagar hasta 100 soles mensuales por una aplicación que brinde más seguridad y control, siempre que sea de calidad. Considera importante que esta incluya funciones como:
   - Notificaciones automáticas de embarque y desembarque.
   - Seguimiento en tiempo real de la ruta.
   - Alertas de paradas o incidencias no programadas.
Cree firmemente que el colegio debería ser quien gestione la aplicación, ya que esto garantizaría un control compartido y mayor confianza institucional. Para ella, la implementación de este tipo de solución sería una muestra concreta del compromiso del colegio con la seguridad y bienestar emocional tanto de estudiantes como de sus familias.

![Imagen extraída del video de entrevistas](src/img/cap2/EntrevistaHayle.png)

\newpage

### Análisis de entrevistas.

::: box
**Segmento Objetivo 1:** Directivos escolares o personal administrativo
:::

**Perfil Demográfico**

- **Edades:** Entre 32 y 55 años, con un promedio estimado de 46.3 años.  

- **Ubicación Geográfica:** Todos los entrevistados pertenecen al distrito de Paiján, provincia de Ascope, La Libertad (Perú).  

- **Cargos ocupados:**
  - Directora de institución educativa privada  

  - Docente y asesor tecnológico  

  - Promotora educativa  

Este segmento representa a profesionales con amplia experiencia en la gestión educativa, en su mayoría con roles de liderazgo o soporte tecnológico dentro de las instituciones. Su perspectiva combina conocimiento administrativo, contacto directo con padres de familia y comprensión de los problemas logísticos cotidianos.


**Experiencia y Conocimientos sobre Transporte Escolar**

Los directivos entrevistados muestran un conocimiento claro y directo sobre la situación actual del transporte escolar en sus instituciones, aunque ninguna de ellas gestiona un sistema institucional de transporte. La logística del traslado de estudiantes es responsabilidad exclusiva de los padres, quienes contratan servicios de movilidad de forma independiente. Esto genera una serie de limitaciones y problemas recurrentes:

- **Ausencia de supervisión institucional:** Las instituciones no participan en la selección de choferes, control de rutas, ni en protocolos de seguridad o asistencia al abordar y descender.
- **Falta de control ante emergencias:** No existe un plan o solución inmediata cuando un estudiante necesita regresar a casa por enfermedad u otro imprevisto durante el horario escolar.
- **Inseguridad y desorganización:** Se reportan problemas como estudiantes que no son recogidos, falta de comunicación efectiva con los transportistas, fallas mecánicas, e incluso situaciones más graves como alumnos que terminan en otra ciudad.
- **Ausencia de herramientas tecnológicas:** Aunque algunas instituciones utilizan sistemas de control de ingreso (como photochips), no existe ningún mecanismo de monitoreo del transporte escolar ni de control de asistencia en las unidades.

En general, los entrevistados reconocen que la situación actual no garantiza ni la seguridad ni la puntualidad, y que los padres no se sienten plenamente tranquilos con el sistema informal de transporte escolar vigente.


**Herramientas y Tecnología Actual**

Actualmente, las instituciones del segmento no cuentan con tecnología dedicada al monitoreo o gestión del transporte escolar. Sin embargo, algunos elementos tecnológicos se usan de manera limitada y en contextos distintos:

- **Herramientas existentes:**
   - Control de asistencia con photochip: En una institución, los estudiantes registran su ingreso con un sistema de marcación electrónica, permitiendo identificar ausencias de manera temprana.
   - Comunicación básica: La interacción con padres y transportistas se realiza principalmente por teléfono o WhatsApp, de forma manual y reactiva.
   - Registro de incidencias: Se lleva a cabo de manera verbal o informal, sin plataformas estandarizadas.

- **Brechas tecnológicas:**
   - No existe un sistema digital que permita monitorear el abordaje o descenso de estudiantes.
   - No hay plataforma institucional que gestione rutas, asistencia, ni alertas automatizadas.
   - El registro y control del transporte es completamente manual y externo a las instituciones.

**Intereses y Necesidades Tecnológicas**

Todos los entrevistados coincidieron en la importancia de implementar soluciones tecnológicas que permitan gestionar de forma segura y eficiente el transporte escolar.

- **Necesidades principales identificadas:**
   - Monitoreo en tiempo real del trayecto de los estudiantes
   - Registro digital de embarque y desembarque (códigos de barras o QR)
   - Notificaciones automáticas a los padres
   - Confirmación diaria por parte de los padres sobre si el alumno asistirá o no (evitando confusiones o ausencias imprevistas).
   - Panel administrativo que brinde visibilidad al personal del colegio sobre:
      - Alumnos presentes en movilidad
      - Rutas y choferes asignados
      - Incidentes o desviaciones en tiempo real


- **Valor percibido:**
   - Mayor seguridad y tranquilidad para las familias
   - Imagen institucional moderna y confiable
   - Apoyo a la gestión interna del colegio (administración, psicología, personal auxiliar)

- **Sobre la viabilidad económica:**

   - El costo es un obstáculo potencial, pero los entrevistados creen que los padres estarían dispuestos a pagar si el valor en seguridad es claro y el precio razonable.


**Preferencias y Comportamientos**

A pesar de no contar con sistemas digitales actualmente, los directivos muestran una actitud abierta, receptiva y proactiva hacia nuevas soluciones tecnológicas, siempre que sean:

- Fáciles de implementar  

- Comprensibles para los padres  

- Accesibles económicamente  

- **Comportamientos actuales:**
   - Gestión manual y reactiva mediante llamadas y WhatsApp
   - Supervisión parcial sin control al subir/bajar de la movilidad
   - Ausencia de protocolos ante emergencias durante el traslado

- **Cambios que buscan:**
   - Automatización del proceso de abordaje/desembarque con trazabilidad
   - Comunicación en tiempo real con los padres
   - Sistemas preventivos, no solo reactivos ante incidentes

En esencia, estos actores educativos buscan una solución que combine tecnología con simplicidad, que les permita mejorar la seguridad sin complejizar la rutina diaria, y que transforme un sistema informal en uno institucional y confiable.

**Estadísticas y Porcentajes**


![Creado en Excel](src/img/cap2/grafico1.png)

![Creado en Excel](src/img/cap2/grafico2.png)

![Creado en Excel](src/img/cap2/grafico3.png)

![Creado en Excel](src/img/cap2/grafico4.png)

\newpage

**Análisis de datos**

-Todos los directivos entrevistados indicaron que el transporte escolar es gestionado de forma externa por los padres, sin participación de la institución educativa. Esta situación genera preocupaciones frecuentes por la falta de control, puntualidad y seguridad.

El 33.3% de las instituciones cuenta con un sistema digital de asistencia, mientras que el 66.7% no utiliza ninguna herramienta tecnológica para registrar el ingreso escolar, lo que limita el control y la prevención de incidentes.

Respecto al acceso digital, Windows es el sistema operativo más utilizado (100%), lo que sugiere una familiaridad general con entornos convencionales de oficina.

En cuanto a dispositivos móviles, Android es el preferido por el 66.7% de los entrevistados, mientras que el 33.3% utiliza iOS, lo que muestra una ligera predominancia de accesibilidad sobre exclusividad.

El navegador web más usado es Google Chrome (66.7%), seguido de Microsoft Edge (33.3%), reforzando la tendencia hacia herramientas de uso masivo y compatibles con múltiples plataformas educativas.

Las funcionalidades tecnológicas más valoradas para un futuro sistema de gestión del transporte escolar incluyen:

   - Monitoreo en tiempo real (GPS) y notificaciones automáticas a los padres (ambas mencionadas por el 100% de los entrevistados).
   - Registro digital de embarque y desembarque, confirmación diaria de asistencia por parte de los padres y paneles administrativos, todos con una alta frecuencia de mención.
   - También se valora la posibilidad de generar historiales o reportes de trayectos para revisión institucional.


::: note 
Este análisis revela que los directivos escolares tienen una percepción clara de las limitaciones actuales del sistema de transporte escolar, especialmente en términos de seguridad y control. A pesar de la falta de implementación tecnológica actual, existe una alta disposición a adoptar herramientas digitales, siempre que estas sean accesibles, intuitivas y contribuyan al bienestar de los estudiantes y la tranquilidad de los padres.
Una solución digital de transporte bien diseñada podría no solo mejorar la logística, sino también fortalecer la imagen institucional y fidelizar a las familias mediante confianza y modernización.
:::

\newpage

::: box
**Segmento Objetivo 2:** Padres de familia con hijos en edad escolar
:::


**Perfil Demográfico**

- **Edad promedio:** 45 años  

- **Ubicación geográfica:** Mayoritariamente en las provincias de Trujillo y Ascope, departamento de La Libertad, Perú.  

- **Ocupación predominante:** Profesionales activas, principalmente en el área de la salud (obstetricia) y la docencia.  

- **Relación con el sistema educativo:** Madres de estudiantes en nivel primario y secundario, con participación activa en la supervisión del entorno escolar y toma de decisiones sobre movilidad.

Este grupo representa un perfil de madres altamente comprometidas con la seguridad y puntualidad en el traslado escolar de sus hijos. Sus decisiones están guiadas por la experiencia directa, criterios de confianza interpersonal, y una creciente expectativa hacia herramientas tecnológicas que profesionalicen el sistema de transporte escolar.

**Experiencia y Conocimientos sobre Transporte Escolar**

Las entrevistadas han transitado por diferentes modalidades de movilidad escolar, desde servicios compartidos (combi escolar) hasta servicios exclusivos (taxis contratados directamente). La elección de un modelo sobre otro responde a experiencias acumuladas que destacan fortalezas y limitaciones relevantes:

- **Problemas comunes en la movilidad compartida:**  
  - Recojos demasiado tempranos y retornos fuera de horario.
  - Recorridos extensos y falta de personalización.
  - Comunicación deficiente o inexistente sobre retrasos o percances.

- **Motivos de migración hacia transporte exclusivo:**  
  - Mayor control del horario.
  - Relación directa con el conductor.
  - Sensación de mayor seguridad y atención personalizada.

- **Percepción de confiabilidad:**  
  - A pesar de confiar en sus actuales proveedores, las madres reconocen que esta seguridad está basada exclusivamente en la relación interpersonal, sin respaldo institucional ni tecnología que garantice trazabilidad o monitoreo.

- **Situaciones críticas reportadas:**  
  - Fallas mecánicas, demoras no informadas, paradas no justificadas y ausencia de canales formales de reporte o respuesta.



**Herramientas y Tecnología Actual**

En el entorno doméstico y profesional, las entrevistadas hacen uso cotidiano de tecnología, principalmente a través de dispositivos móviles con sistema operativo Android. Sin embargo, este uso no se traduce en una integración efectiva con el entorno educativo ni con la movilidad escolar:

- **Dispositivos tecnológicos utilizados:**  
  - Smartphones (Samsung Galaxy predominante, sistema Android).

- **Herramientas de comunicación:**  
  - WhatsApp como canal informal entre padres, tutores y choferes.
  - Llamadas telefónicas directas en caso de emergencias o dudas.

- **Intentos de implementación tecnológica:**  
  - Una entrevistada intentó utilizar un reloj GPS infantil, pero fue restringido por la institución escolar y resultó inefectivo por manipulación del menor.

- **Limitaciones identificadas:**  
  - Falta de aplicaciones escolares dedicadas al monitoreo del transporte.
  - No existen sistemas automatizados de embarque, llegada o descenso.
  - Total ausencia de confirmaciones o alertas institucionales sobre el estado del trayecto o la asistencia del estudiante.


**Intereses y Necesidades Tecnológicas**

Existe un consenso claro sobre el interés y la apertura hacia soluciones tecnológicas que ofrezcan mayor visibilidad, trazabilidad y tranquilidad a las familias.

- **Requerimientos clave identificados:**
   - Monitoreo en tiempo real del trayecto escolar.
   - Notificaciones automáticas sobre subida, bajada, llegada, desvíos y emergencias.
   - Registro digital de embarque y desembarque mediante códigos o sensores.
   - Confirmación diaria de asistencia gestionada desde el hogar.
   - Historiales o bitácoras de trayectos para consulta y análisis posterior.
   - Botón de emergencia o alerta para uso por parte del estudiante en caso de urgencia.

- **Preferencias de gestión:**
   - Las entrevistadas consideran indispensable que el colegio sea el ente encargado de la implementación, gestión y supervisión de la tecnología y el personal del transporte escolar.
   - La participación institucional es percibida como un factor de garantía, profesionalismo y respaldo, frente a modelos gestionados informalmente por grupos de padres.

- **Disposición económica:**
   - Existe disposición general a asumir un costo adicional si el sistema garantiza seguridad, eficiencia y respaldo formal.
   - Se menciona un rango aceptable de pago mensual que puede alcanzar los S/100 soles si el valor percibido justifica la inversión.



**Preferencias y Comportamientos Observados**

Las entrevistadas presentan comportamientos orientados a la supervisión activa del traslado escolar, aunque carecen de herramientas formales para hacerlo.

- **Conductas comunes:**

   - Seguimiento manual mediante llamadas y mensajes al chofer.

   - Tolerancia a modificaciones en rutas o puntos de recojo si existe confianza previa.

   - Evaluación continua de la puntualidad y confiabilidad del servicio.

- **Criterios de cambio de servicio:**

   - Incumplimiento reiterado de horarios.

   - Falta de comunicación ante imprevistos.

   - Ausencia de trazabilidad.

- **Elementos prioritarios en una solución ideal:**

   - Automatización de procesos críticos como embarque y notificación de llegada.

   - Gestión institucional centralizada que permita reportes, control y respuestas rápidas.

   - Sistema fácil de usar, tanto para padres como para personal educativo.


**Estadísticas y Porcentajes**


![Creado en Excel](src/img/cap2/grafico1S2.png)

![Creado en Excel](src/img/cap2/grafico2S2.png)

![Creado en Excel](src/img/cap2/grafico3S2.png)

\newpage


**Análisis de Datos**

Las madres entrevistadas utilizan servicios de transporte escolar privado (movilidad compartida o taxi exclusivo), y coinciden en que, si bien actualmente no enfrentan grandes incidentes, la falta de seguimiento en tiempo real genera inseguridad y preocupación.

El 100% de las entrevistadas confía principalmente en la relación personal con el conductor, ya que no utilizan apps escolares ni sistemas institucionales para hacer seguimiento del transporte.

Asimismo, el 100% considera que el monitoreo digital debería estar gestionado por el colegio, lo cual reflejaría mayor compromiso institucional, profesionalismo en la selección del personal y respaldo en caso de emergencias.

Respecto a su disposición económica, todas están abiertas a pagar un monto adicional por una solución digital que brinde seguridad y control, siempre que esté correctamente respaldada por la institución educativa.

En cuanto a sus herramientas actuales:

- El sistema operativo más utilizado es Android (100%), lo que sugiere una fuerte afinidad con dispositivos de fácil acceso y uso común.

- Google Chrome fue el navegador mencionado con más frecuencia (66.7%), mientras que el 33.3% no especificó navegador, lo que puede deberse a menor uso activo de plataformas web escolares.


Las funcionalidades tecnológicas más mencionadas para una aplicación ideal incluyen:

- Monitoreo en tiempo real (GPS) y notificaciones automáticas a los padres (ambas mencionadas por el 100%).

- Registro digital de embarque/desembarque y confirmación diaria desde la app, con una frecuencia del 66.7%.

- También se valoraron herramientas innovadoras como una alerta de emergencia activada por el niño y la posibilidad de que el sistema sea gestionado institucionalmente.



::: note
Este análisis muestra que los padres de familia valoran altamente la seguridad, la puntualidad y el control durante el traslado escolar, y aunque confían en sus proveedores actuales, reconocen que la tecnología puede ofrecer un nivel de tranquilidad mucho más robusto y automatizado.
Existe una clara expectativa de que el colegio sea el actor responsable en implementar soluciones digitales, lo cual no solo fortalecería la confianza de las familias, sino también proyectaría una imagen institucional comprometida con el bienestar emocional y físico de sus estudiantes.

:::

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

- *Alumno*: Niño o niña que utiliza el servicio de transporte escolar. Es quien porta la Tarjeta RFID y genera eventos de abordaje y descenso. (Sinónimos: Estudiante, Niño)
- *Padre de Familia*: Persona responsable del Alumno (padre, madre o apoderado) que recibe notificaciones y puede gestionar permisos. (Sinónimos: Padre, Madre, Apoderado)
- *Conductor*: Chofer designado para una Unidad de Transporte; interactúa con la app Conductor y valida abordajes/desabordajes. (Sinónimos: Chofer)
- *Administrador Escolar*: Personal de la institución que configura Rutas, Paradas, Alumnos y Conductores y supervisa reportes. (Sinónimos: Admin, Colegio)
- *Tarjeta RFID*: Tarjeta (o llavero) pasiva, asignada de forma única a un Alumno para autenticarse al acercarla al Lector.
- *Lector RFID*: Dispositivo IoT instalado en la Unidad que lee la Tarjeta RFID y envía eventos en tiempo real.
- *Unidad de Transporte*: Vehículo escolar identificado por placa y código interno, equipado con Lector RFID y GPS.
- *App RutaKids Conductor*: Aplicación móvil vinculada a la Unidad; muestra la lista de Alumnos por Parada y confirma incidentes.
- *Backend RutaKids*: Plataforma en la nube que procesa eventos, reglas de negocio y persiste datos.
- *Panel de Control*: Interfaz web para Administradores Escolares y Operadores de Flota.
- *Ruta*: Conjunto ordenado de Paradas asociadas a una Institución y un Horario recurrente.
- *Parada*: Punto geográfico donde se recoge o deja Alumnos. Incluye ventana de tiempo y lista de Alumnos asignados.
- *Trayecto*: Ejecución diaria de una Ruta en una fecha concreta.
- *Horario*: Reglas de recurrencia de la Ruta (días laborables, hora de inicio y fin estimada).
- *AlumnoAbordóUnidad*: Evento emitido cuando un Alumno validó su Tarjeta y subió a la Unidad.
- *AlumnoDescendióUnidad*: Evento emitido cuando un Alumno validó su Tarjeta al salir de la Unidad.
- *TarjetaNoReconocida*: Evento emitido cuando se leyó un UID no asociado a ningún Alumno.
- *IncidenciaReportada*: Evento emitido cuando el Conductor registra un evento anómalo (retraso, avería, etc.).
- *CambioDeRutaProgramado*: Evento emitido cuando un Admin modificó la configuración de una Ruta.
- *RegistrarAlumno*: Comando para crear la Entidad Alumno y vincular al Padre de Familia.
- *AsignarTarjeta*: Comando para asociar Tarjeta RFID a Alumno.
- *ProgramarRuta*: Comando para crear o actualizar una Ruta, su Horario y Paradas.
- *MarcarAbordaje*: Comando para forzar confirmación manual de abordaje (modo fallback).
- *EnviarNotificación*: Comando para avisar a Padres de Familia sobre un Evento.
- *ServicioDeAutenticaciónRFID*: Servicio que valida UID, levanta Eventos y asegura consistencia.
- *ServicioDeNotificaciones*: Servicio que orquesta avisos (push, correo, SMS) a Padres de Familia y Admins.
- *ServicioDeRutas*: Servicio que calcula tiempos estimados, detecta desvíos y actualiza Estado de Trayecto.
- *ServicioDeReportes*: Servicio que genera KPIs: puntualidad, asistencia y uso de Rutas.
- *Estado de Trayecto*: Secuencia Pendiente → EnCurso → Finalizado / Cancelado.
- *Rol*: Identidades posibles en el sistema: Alumno, Padre de Familia, Conductor, Administrador Escolar, Operador de Flota.
- *Modo de Notificación*: Tipos de aviso soportados: Push, SMS, Email.
- *Incidencia*: Registro de evento no deseado (retraso, exceso de velocidad, ruta cambiada).

\newpage

# Capítulo III: Requirements Specification

La sección de Especificación de Requisitos tiene como objetivo describir de forma clara y detallada las necesidades funcionales y no funcionales que debe cumplir el sistema para garantizar su correcto desarrollo y funcionamiento. Esta especificación actúa como un acuerdo formal entre los desarrolladores y las partes interesadas, estableciendo una base común de entendimiento sobre lo que se espera del sistema.

Los requisitos presentados en esta sección se han recopilado a través de investigaciones con usuarios, entrevistas con los interesados y análisis de los procesos actuales. Están organizados de manera que reflejan tanto las necesidades del usuario como la viabilidad técnica. Este documento servirá como guía durante todas las etapas del ciclo de vida del proyecto: diseño, implementación, pruebas y mantenimiento.

## To-Be Scenario Mapping.

**To-Be Scenario – Marco (Padre de familia)**
Con la solución digital, Marco tiene información en tiempo real, alertas personalizadas y tranquilidad al saber que su hijo está seguro.

![To-be Scenario Mapping 1 - Recurso de Miro](https://i.postimg.cc/vZRHS6CS/to-be-esteban.png)

**To-Be Scenario – Carolina (Administradora)**
Carolina ahora gestiona rutas, asistencia y comunicaciones desde una plataforma centralizada, reduciendo el caos operativo y ganando eficiencia.

![To-be Scenario Mapping 2 - Recurso de Miro](https://i.postimg.cc/fTSRKvq9/to-be-carolina.png)

\newpage 
## User Stories.

### Administrador educativo

***Epics*** **y** ***User Stories:***

\begin{longtable}{|m{5cm}|m{10cm}|}
\hline
\textbf{EP01 (Gestión de cuentas de administrador educativo)} & \textbf{Como} administrador educativo, \textbf{quiero} registrarme, iniciar sesión y gestionar mi cuenta institucional \textbf{para} acceder de manera segura a la plataforma web y administrar el sistema de transporte escolar. \\
\hline
US01 & Registro de cuenta institucional \\
\hline
US02 & Confirmación de cuenta del administrador \\
\hline
US03 & Verificación de cuenta por parte del sistema \\
\hline
US04 & Inicio de sesión del administrador educativo \\
\hline
US05 & Recuperación de contraseña \\
\hline
US06 & Gestión de perfil administrativo \\
\hline
US07 & Cierre de sesión segura \\
\hline
\textbf{EP02 (Gestión de flotas y zonas)} & \textbf{Como} administrador educativo, \textbf{quiero} gestionar la información de vehículos y zonas geográficas \textbf{para} optimizar las rutas de transporte escolar y garantizar cobertura efectiva. \\
\hline
CS01 & Registro y edición de vehículos \\
\hline
CS02 & Definición y mapeo de zonas \\
\hline
CS03 & Visualización geoespacial de zonas y rutas \\
\hline
CS04 & Asignación de vehículos a rutas específicas \\
\hline
CS05 & Desactivación temporal de unidades fuera de servicio \\
\hline
\textbf{EP03 (Gestión de conductores y estudiantes)} & \textbf{Como} administrador educativo, \textbf{quiero} gestionar la información de conductores y estudiantes \textbf{para} asegurar que las rutas se asignen correctamente y optimizar la seguridad del transporte escolar. \\
\hline
DS01 & Registro y actualización de conductores \\
\hline
DS02 & Registro y asignación de pulseras RFID a estudiantes \\
\hline
DS03 & Asignación de conductores y estudiantes a rutas específicas \\
\hline
DS04 & Verificación de disponibilidad de conductores \\
\hline
DS05 & Control de cambios de última hora en la asignación de conductores y estudiantes \\
\hline
\textbf{EP04 (Integración IoT y captura de datos)} & \textbf{Como} administrador educativo, \textbf{quiero} integrar tecnologías IoT para el monitoreo en tiempo real de las flotas de transporte \textbf{para} optimizar la seguridad, eficiencia y control de las rutas de transporte escolar. \\
\hline
ES01 & Monitoreo de posición y velocidad en tiempo real de vehículos \\
\hline
ES02 & Monitoreo de temperatura interna de los vehículos \\
\hline
ES03 & Seguimiento de unidades de transporte para verificar salida y llegada \\
\hline
ES04 & Monitoreo de estudiantes que no abordaron la unidad \\
\hline
ES05 & Verificación de rutas alternativas en caso de desvíos \\
\hline
ES06 & Visualización de unidades en ruta para gestionar desviaciones o retrasos \\
\hline
\textbf{EP05 (Notificaciones y Alertas)} & \textbf{Como} administrador educativo, \textbf{quiero} recibir notificaciones y alertas en tiempo real sobre los eventos y condiciones críticas de las unidades de transporte \textbf{para} poder tomar decisiones rápidas y garantizar la seguridad y eficiencia del servicio. \\
\hline
FS01 & Alerta de temperatura fuera de rango \\
\hline
FS02 & Alerta de retrasos o desviaciones en las rutas \\
\hline
FS03 & Alerta de estudiantes no abordando la unidad \\
\hline
FS04 & Notificación automática ante cambios de ruta o posibles retrasos \\
\hline
FS05 & Alerta por fallo de equipo en el vehículo (GPS, RFID, sensores, etc.) \\
\hline
FS06 & Notificación cuando la unidad ha completado el recorrido \\
\hline
\textbf{EP06 (Reportes y Analítica)} & \textbf{Como} administrador educativo, \textbf{quiero} generar y analizar reportes e indicadores \textbf{para} evaluar el desempeño del transporte escolar y apoyar la toma de decisiones. \\
\hline
GS01 & Reporte de tiempos de ruta y cumplimiento \\
\hline
GS02 & Estadísticas de abordaje por estudiante \\
\hline
GS03 & Exportación de datos históricos en Excel/PDF \\
\hline
GS04 & Reporte de incidencias críticas \\
\hline
GS05 & Programación de envíos automáticos de reportes \\
\hline
GS06 & Filtrado y segmentación de datos históricos \\
\hline
\textbf{EP07 (Plataforma Web de Administración)} & \textbf{Como} administrador educativo, \textbf{quiero} acceder a herramientas de administración centralizadas \textbf{para} configurar, monitorear y asegurar el correcto funcionamiento de la plataforma. \\
\hline
HS01 & Dashboard con KPIs clave \\
\hline
HS02 & Gestión de roles y permisos \\
\hline
HS03 & Configuración de parámetros globales \\
\hline
HS04 & Registro de auditoría de actividad \\
\hline
HS05 & Configuración de notificaciones y alertas \\
\hline
HS06 & Personalización del dashboard \\
\hline
\end{longtable}

\newpage

***User Stories:***

\begin{longtable}{|p{1cm}|p{3cm}|p{4cm}|p{5cm}|p{1cm}|}
\hline
\multicolumn{1}{|c|}{\textbf{ID}} & \multicolumn{1}{c|}{\textbf{Título}} & \multicolumn{1}{c|}{\textbf{Descripción}} & \multicolumn{1}{c|}{\textbf{Criterios de Aceptación}} & \multicolumn{1}{c|}{\textbf{Epic}} \\
\hline
US01 & Registro de cuenta institucional & \textbf{Como} administrador educativo, \textbf{quiero} crear una cuenta institucional proporcionando mi nombre completo, correo institucional y contraseña, \textbf{para} acceder de manera segura a la plataforma web. & 
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Creación exitosa de cuenta}\\
\textbf{Dado que} el administrador accede al formulario de registro\\
\textbf{cuando} ingresa nombre, correo institucional válido y contraseña que cumple los requisitos\\
\textbf{entonces} el sistema crea la cuenta, envía un correo de confirmación y redirige al administrador al dashboard de bienvenida.\\[0.2em]

\textbf{Escenario 2: Campos obligatorios vacíos}\\
\textbf{Dado que} el administrador accede al formulario de registro\\
\textbf{cuando} no completa los campos obligatorios (nombre, correo o contraseña)\\
\textbf{entonces} el sistema muestra mensajes de error indicando los campos faltantes.\\[0.2em]

\textbf{Escenario 3: Correo institucional inválido}\\
\textbf{Dado que} el administrador ingresa un correo que no pertenece al dominio institucional\\
\textbf{cuando} intenta enviar el formulario de registro\\
\textbf{entonces} el sistema muestra un mensaje de error indicando que el correo debe ser del dominio oficial.\\[0.2em]
\end{tabular}
& EP01 \\
\hline
US02 & Confirmación de cuenta del administrador & \textbf{Como} administrador educativo, \textbf{quiero} confirmar mi cuenta a través de un enlace enviado a mi correo institucional, \textbf{para} verificar mi identidad y activar mi acceso al sistema. & 
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Confirmación exitosa}\\
\textbf{Dado que} el administrador ha recibido un correo de confirmación con un token válido\\
\textbf{cuando} hace clic en el enlace de confirmación\\
\textbf{entonces} el sistema activa su cuenta, muestra un mensaje de éxito y lo redirige a la página de inicio de sesión.\\[0.2em]

\textbf{Escenario 2: Token inválido}\\
\textbf{Dado que} el administrador hace clic en un enlace con un token incorrecto o modificado\\
\textbf{cuando} el sistema procesa el token\\
\textbf{entonces} muestra un mensaje de error indicando “Enlace inválido” y ofrece la opción de reenviar el correo de confirmación.\\[0.2em]

\textbf{Escenario 3: Token expirado}\\
\textbf{Dado que} el administrador hace clic en un enlace cuya validez ha expirado\\
\textbf{cuando} el sistema detecta la expiración del token\\
\textbf{entonces} muestra un mensaje de “Enlace expirado” y permite solicitar un nuevo correo de confirmación.\\[0.2em]
\end{tabular}
& EP01 \\
\hline
US03 & Verificación de cuenta por parte del sistema & \textbf{Como} administrador educativo, \textbf{quiero} que el sistema verifique automáticamente la validez de mi cuenta, \textbf{para} asegurarme de que mi información esté correctamente registrada y no haya problemas para acceder a la plataforma. & 
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Verificación exitosa}\\
\textbf{Dado que} el administrador ha completado el registro y confirmado su cuenta\\
\textbf{cuando} el sistema verifica que la cuenta está activa y con información válida\\
\textbf{entonces} el administrador accede sin problemas al sistema, y se le muestra el dashboard de administración.\\[0.2em]

\textbf{Escenario 2: Verificación fallida por falta de confirmación}\\
\textbf{Dado que} el administrador se encuentra en el proceso de registro\\
\textbf{cuando} el sistema detecta que la cuenta no ha sido confirmada\\
\textbf{entonces} el sistema muestra un mensaje de advertencia indicando que el correo de confirmación aún no ha sido validado.\\[0.2em]

\textbf{Escenario 3: Verificación fallida por datos incorrectos}\\
\textbf{Dado que} el administrador ha ingresado información incorrecta durante el registro (como un correo no institucional)\\
\textbf{cuando} el sistema verifica los datos registrados\\
\textbf{entonces} muestra un mensaje de error indicando que la cuenta no se puede activar debido a la información inválida.\\[0.2em]
\end{tabular}
& EP01 \\
\hline
US04 & Inicio de sesión del administrador educativo & \textbf{Como} administrador educativo, \textbf{quiero} iniciar sesión de manera segura en la plataforma utilizando mis credenciales (correo electrónico y contraseña), \textbf{para} acceder a las funcionalidades de administración del sistema de transporte escolar de manera eficiente. & 
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Inicio de sesión exitoso}\\
\textbf{Dado que} el administrador ingresa correctamente su correo electrónico y contraseña\\
\textbf{cuando} el sistema valida las credenciales\\
\textbf{entonces} el administrador accede exitosamente a la plataforma y se le redirige al dashboard de administración.\\[0.2em]

\textbf{Escenario 2: Intento de inicio de sesión con credenciales incorrectas}\\
\textbf{Dado que} el administrador ingresa un correo electrónico o contraseña incorrectos\\
\textbf{cuando} el sistema verifica las credenciales\\
\textbf{entonces} el sistema muestra un mensaje de error indicando que las credenciales no son válidas y solicita al administrador que las ingrese nuevamente.\\[0.2em]

\textbf{Escenario 3: Intento de inicio de sesión con cuenta bloqueada}\\
\textbf{Dado que} el administrador intenta acceder a la plataforma con una cuenta bloqueada\\
\textbf{cuando} el sistema detecta que la cuenta está bloqueada o desactivada\\
\textbf{entonces} el sistema muestra un mensaje indicando que la cuenta ha sido bloqueada y proporciona instrucciones sobre cómo desbloquearla.\\[0.2em]
\end{tabular}
& EP01 \\

\hline
US05 & Recuperación de contraseña & \textbf{Como} administrador educativo, \textbf{quiero} poder recuperar mi contraseña a través de un correo electrónico, \textbf{para} poder acceder nuevamente a mi cuenta si la olvido. & 
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Recuperación de contraseña exitosa}\\
\textbf{Dado que} el administrador ha solicitado la recuperación de su contraseña a través del correo electrónico\\
\textbf{cuando} el administrador ingresa la dirección de correo electrónico asociada a su cuenta y hace clic en "Recuperar contraseña"\\
\textbf{entonces} el sistema envía un enlace de recuperación al correo electrónico del administrador para permitirle restablecer la contraseña.\\[0.2em]

\textbf{Escenario 2: Intento de recuperación con un correo no registrado}\\
\textbf{Dado que} el administrador intenta recuperar la contraseña utilizando una dirección de correo electrónico que no está registrada en el sistema\\
\textbf{cuando} el sistema verifica la dirección de correo electrónico\\
\textbf{entonces} el sistema muestra un mensaje indicando que el correo electrónico no está asociado a ninguna cuenta y sugiere al administrador que verifique la dirección.\\[0.2em]
\end{tabular}
& EP01 \\

\hline
US06 & Gestión de perfil administrativo & \textbf{Como} administrador educativo, \textbf{quiero} poder editar y actualizar mi perfil (como datos de contacto, cargo, etc.), \textbf{para} mantener mi información actualizada en la plataforma. & 
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Edición de perfil exitosa}\\
\textbf{Dado que} el administrador ha accedido a la sección de gestión de perfil\\
\textbf{cuando} el administrador actualiza sus datos (como dirección de correo, número de contacto, cargo, etc.)\\
\textbf{entonces} el sistema guarda los cambios y muestra un mensaje de confirmación de que la actualización se ha realizado correctamente.\\[0.2em]

\textbf{Escenario 2: Intento de actualización con campos vacíos}\\
\textbf{Dado que} el administrador intenta actualizar su perfil\\
\textbf{cuando} deja campos obligatorios en blanco (como nombre o correo electrónico)\\
\textbf{entonces} el sistema muestra un mensaje de error indicando que los campos obligatorios deben completarse antes de guardar los cambios.\\[0.2em]

\textbf{Escenario 3: Visualización de perfil actualizado}\\
\textbf{Dado que} el administrador ha realizado cambios en su perfil\\
\textbf{cuando} el administrador regresa a la página principal de gestión de su cuenta\\
\textbf{entonces} el sistema muestra la información de perfil actualizada, reflejando los cambios realizados.\\[0.2em]
\end{tabular}
& EP01 \\

\hline
US07 & Cierre de sesión segura & \textbf{Como} administrador educativo, \textbf{quiero} cerrar sesión de manera segura en la plataforma, \textbf{para} garantizar que mi cuenta esté protegida y no quede abierta a accesos no autorizados. & 
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Cierre de sesión exitoso}\\
\textbf{Dado que} el administrador ha decidido cerrar sesión\\
\textbf{cuando} el administrador hace clic en el botón de "Cerrar sesión"\\
\textbf{entonces} el sistema cierra la sesión y redirige al administrador a la página de inicio de sesión, mostrando un mensaje de confirmación de que la sesión fue cerrada correctamente.\\[0.2em]

\textbf{Escenario 2: Intento de acceder sin haber cerrado sesión}\\
\textbf{Dado que} el administrador ha cerrado sesión\\
\textbf{cuando} el administrador intenta acceder a una página protegida de la plataforma sin volver a iniciar sesión\\
\textbf{entonces} el sistema redirige al administrador a la página de inicio de sesión, indicando que la sesión ha expirado.\\[0.2em]

\textbf{Escenario 3: Cierre de sesión con múltiples dispositivos}\\
\textbf{Dado que} el administrador tiene la sesión abierta en varios dispositivos\\
\textbf{cuando} el administrador cierra sesión en uno de los dispositivos\\
\textbf{entonces} la sesión se cierra solo en ese dispositivo, mientras que los demás dispositivos continúan con la sesión activa.\\[0.2em]
\end{tabular}
& EP01 \\

\hline
CS01 & Registro y edición de vehículos & \textbf{Como} administrador educativo, \textbf{quiero} registrar y editar los datos de cada vehículo (placa, modelo, capacidad y estado operativo), \textbf{para} mantener un catálogo actualizado y fiable de la flota. & 
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Registro exitoso de vehículo}\\
\textbf{Dado que} el administrador accede al formulario de registro de vehículos\\
\textbf{cuando} ingresa placa única, modelo, capacidad numérica y estado operativo válido\\
\textbf{entonces} el sistema guarda el nuevo vehículo y muestra un mensaje de confirmación.\\[0.2em]

\textbf{Escenario 2: Placa duplicada}\\
\textbf{Dado que} el administrador ingresa una placa que ya existe en el sistema\\
\textbf{cuando} envía el formulario de registro\\
\textbf{entonces} el sistema muestra un error indicando que la placa ya está registrada y no crea un duplicado.\\[0.2em]

\textbf{Escenario 3: Edición exitosa de vehículo}\\
\textbf{Dado que} el administrador selecciona un vehículo existente y modifica sus datos\\
\textbf{cuando} ingresa valores válidos en los campos y guarda los cambios\\
\textbf{entonces} el sistema actualiza la información y muestra un mensaje de confirmación.\\
\end{tabular}
& EP02 \\

\hline
CS02 & Definición y mapeo de zonas & \textbf{Como} administrador educativo, \textbf{quiero} definir y mapear zonas de recogida y entrega en un mapa interactivo, \textbf{para} optimizar la cobertura y asignar rutas con precisión. & 
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Creación exitosa de zona}\\
\textbf{Dado que} el administrador accede a la sección de zonas\\
\textbf{cuando} ingresa un nombre de zona y dibuja un polígono válido en el mapa\\
\textbf{entonces} el sistema guarda la zona y la muestra en el mapa con su nombre.\\[0.2em]

\textbf{Escenario 2: Polígono inválido}\\
\textbf{Dado que} el administrador dibuja un polígono con menos de tres puntos o con intersecciones propias\\
\textbf{cuando} intenta guardar la zona\\
\textbf{entonces} el sistema muestra un mensaje de error indicando que el polígono no es válido.\\[0.2em]

\textbf{Escenario 3: Edición de zona existente}\\
\textbf{Dado que} el administrador selecciona una zona ya creada\\
\textbf{cuando} modifica su nombre o ajusta el polígono en el mapa y guarda los cambios\\
\textbf{entonces} el sistema actualiza la zona y refleja los cambios en el mapa.\\
\end{tabular}
& EP02 \\

\hline
CS03 & Visualización geoespacial de zonas y rutas & \textbf{Como} administrador educativo, \textbf{quiero} visualizar todas las zonas de recogida y entrega y sus rutas asociadas en un mapa interactivo, \textbf{para} detectar posibles solapamientos, huecos de cobertura o áreas no cubiertas. & 
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Visualización correcta de zonas y rutas}\\
\textbf{Dado que} el administrador accede al mapa interactivo\\
\textbf{cuando} se cargan las zonas y sus rutas asociadas en el mapa\\
\textbf{entonces} el sistema muestra todas las zonas y rutas de manera precisa y clara, con un código de colores para diferenciarlas.\\[0.2em]

\textbf{Escenario 2: Solapamientos en zonas}\\
\textbf{Dado que} el administrador ve las zonas y sus rutas en el mapa\\
\textbf{cuando} dos zonas tienen solapamientos en sus límites o rutas\\
\textbf{entonces} el sistema resalta el área de solapamiento y muestra un mensaje de advertencia indicando el solapamiento.\\[0.2em]

\textbf{Escenario 3: Huecos de cobertura}\\
\textbf{Dado que} el administrador observa las zonas en el mapa\\
\textbf{cuando} existe una zona sin rutas asociadas o una ruta que no cubre completamente una zona\\
\textbf{entonces} el sistema resalta el área sin cobertura y sugiere una posible acción para corregirlo.\\[0.2em]

\end{tabular}
& EP02 \\

\hline
CS04 & Asignación de vehículos a rutas específicas & \textbf{Como} administrador educativo, \textbf{quiero} asignar vehículos específicos a rutas definidas, \textbf{para} tener un control operacional directo sobre qué unidad se utiliza en cada recorrido y facilitar la trazabilidad en caso de incidentes. & 
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Asignación de vehículo a ruta}\\
\textbf{Dado que} el administrador está visualizando las rutas disponibles\\
\textbf{cuando} selecciona una ruta y elige un vehículo disponible de la flota\\
\textbf{entonces} el sistema asigna correctamente el vehículo a la ruta seleccionada y muestra la información actualizada en la vista.\\[0.2em]

\textbf{Escenario 2: Verificación de la asignación de vehículo a ruta}\\
\textbf{Dado que} el administrador ha asignado un vehículo a una ruta\\
\textbf{cuando} el administrador consulta la ruta asignada\\
\textbf{entonces} el sistema muestra claramente qué vehículo está asignado a esa ruta, incluyendo la placa y el modelo del vehículo.\\[0.2em]

\textbf{Escenario 3: Desasignación de vehículo de ruta}\\
\textbf{Dado que} el administrador desea cambiar la asignación de un vehículo\\
\textbf{cuando} el administrador selecciona una ruta y desasigna el vehículo actual\\
\textbf{entonces} el sistema elimina la asignación del vehículo de esa ruta y lo muestra como disponible para otras rutas.\\[0.2em]
\end{tabular}
& EP02 \\

\hline
CS05 & Desactivación temporal de unidades fuera de servicio & \textbf{Como} administrador educativo, \textbf{quiero} desactivar temporalmente vehículos fuera de servicio, \textbf{para} evitar su asignación errónea a rutas mientras se mantiene su información en el sistema para futuras referencias y reactivación. & 
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Desactivación de vehículo fuera de servicio}\\
\textbf{Dado que} un vehículo requiere mantenimiento o no está operativo\\
\textbf{cuando} el administrador selecciona el vehículo en el sistema y lo marca como fuera de servicio\\
\textbf{entonces} el vehículo se desactiva temporalmente y no aparece como disponible para asignación en las rutas.\\[0.2em]

\textbf{Escenario 2: Verificación de desactivación de vehículo}\\
\textbf{Dado que} el administrador ha desactivado un vehículo\\
\textbf{cuando} consulta la lista de vehículos disponibles\\
\textbf{entonces} el vehículo aparece marcado como fuera de servicio y no está disponible para ser asignado a nuevas rutas.\\[0.2em]

\textbf{Escenario 3: Reactivación de vehículo fuera de servicio}\\
\textbf{Dado que} un vehículo ha sido desactivado temporalmente\\
\textbf{cuando} el administrador selecciona el vehículo y lo marca como disponible nuevamente\\
\textbf{entonces} el vehículo se reactiva y aparece como disponible para ser asignado a nuevas rutas.\\[0.2em]
\end{tabular}
& EP02 \\
\hline
DS01 & Registro y actualización de conductores & \textbf{Como} administrador educativo, \textbf{quiero} registrar nuevos conductores y actualizar sus datos de contacto, número de licencia y estado operativo, \textbf{para} mantener un personal actualizado y garantizar la correcta asignación de rutas. & 
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Registro exitoso de conductor}\\
\textbf{Dado que} el administrador accede al formulario de conductores\\
\textbf{cuando} ingresa nombre completo, correo, teléfono y número de licencia válidos\\
\textbf{entonces} el sistema guarda el nuevo conductor y muestra un mensaje de confirmación.\\[0.2em]

\textbf{Escenario 2: Licencia duplicada o inválida}\\
\textbf{Dado que} el administrador ingresa un número de licencia ya existente o mal formado\\
\textbf{cuando} envía el formulario de registro\\
\textbf{entonces} el sistema muestra un mensaje de error indicando “Número de licencia inválido o duplicado”.\\[0.2em]

\textbf{Escenario 3: Actualización exitosa de datos}\\
\textbf{Dado que} el administrador selecciona un conductor existente\\
\textbf{cuando} modifica sus datos (contacto, licencia, estado) y guarda los cambios\\
\textbf{entonces} el sistema actualiza la información y muestra un mensaje de “Perfil actualizado”.\\[0.2em]
\end{tabular}
& EP03 \\

\hline

DS02 & Registro y asignación de pulseras RFID a estudiantes & \textbf{Como} administrador educativo, \textbf{quiero} registrar a los estudiantes en el sistema y asignarles pulseras RFID con un identificador único, \textbf{para} vincular cada niño con su dispositivo de control y gestionar su transporte de manera más eficiente. & 
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Registro de estudiante exitoso}\\
\textbf{Dado que} el administrador accede al formulario de registro de estudiante\\
\textbf{cuando} ingresa los datos del estudiante (nombre, grado, etc.) y asigna una pulsera RFID\\
\textbf{entonces} el sistema guarda los datos del estudiante junto con el identificador RFID y confirma el registro.\\[0.2em]

\textbf{Escenario 2: Intento de asignación de pulsera duplicada}\\
\textbf{Dado que} el administrador intenta asignar una pulsera RFID ya asignada a otro estudiante\\
\textbf{cuando} el sistema detecta la duplicación\\
\textbf{entonces} el sistema muestra un mensaje de error indicando “Pulsera RFID ya asignada”.\\[0.2em]

\textbf{Escenario 3: Registro sin pulsera RFID}\\
\textbf{Dado que} el administrador está registrando un estudiante\\
\textbf{cuando} no asigna una pulsera RFID al estudiante\\
\textbf{entonces} el sistema muestra un mensaje de advertencia indicando que se debe asignar una pulsera RFID.\\[0.2em]
\end{tabular}
& EP03 \\

\hline
DS03 & Asignación de conductores y estudiantes a rutas específicas & \textbf{Como} administrador educativo, \textbf{quiero} asignar conductores y estudiantes a rutas específicas en el sistema, \textbf{para} asegurar que cada unidad opere con el personal y pasajeros correctos y optimizar la seguridad del transporte escolar. & 
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Asignación exitosa}\\
\textbf{Dado que} el administrador se encuentra en la interfaz de asignación de rutas\\
\textbf{cuando} selecciona una ruta y asigna un conductor disponible junto con los estudiantes correspondientes\\
\textbf{entonces} el sistema guarda la asignación y muestra una confirmación exitosa de la operación.\\[0.2em]

\textbf{Escenario 2: Intento de asignación con datos incompletos}\\
\textbf{Dado que} el administrador está asignando una ruta\\
\textbf{cuando} omite seleccionar al menos un conductor o uno o más estudiantes\\
\textbf{entonces} el sistema muestra un mensaje de error indicando “Debe asignar un conductor y al menos un estudiante para continuar”.\\[0.2em]

\textbf{Escenario 3: Validación de conflicto en asignación}\\
\textbf{Dado que} el administrador intenta asignar un conductor o estudiante que ya se encuentra asignado a otra ruta en el mismo horario\\
\textbf{cuando} el sistema detecta el conflicto de asignación\\
\textbf{entonces} el sistema muestra un mensaje de advertencia indicando “El conductor/estudiante ya se encuentra asignado a otra ruta en este horario” y no permite la asignación duplicada.\\[0.2em]
\end{tabular}
& EP03 \\

\hline

DS04 & Verificación de disponibilidad de conductores & \textbf{Como} administrador educativo, \textbf{quiero} verificar la disponibilidad de los conductores antes de asignarlos a una ruta, \textbf{para} evitar conflictos de horario y asegurar una gestión eficiente del personal y la flota. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Conductor disponible}\\
\textbf{Dado que} el administrador accede al panel de asignación de rutas\\
\textbf{cuando} consulta la disponibilidad de un conductor específico\\
\textbf{entonces} el sistema muestra que el conductor está disponible y permite su asignación.\\[0.2em]

\textbf{Escenario 2: Conductor ya asignado}\\
\textbf{Dado que} el administrador consulta la disponibilidad de un conductor\\
\textbf{cuando} el sistema detecta que el conductor ya está asignado a otra ruta en el mismo horario\\
\textbf{entonces} el sistema muestra una advertencia de “Conductor no disponible” e impide su asignación.\\[0.2em]

\textbf{Escenario 3: Filtro por disponibilidad general}\\
\textbf{Dado que} el administrador desea asignar un conductor a una nueva ruta\\
\textbf{cuando} utiliza un filtro para mostrar solo conductores disponibles\\
\textbf{entonces} el sistema muestra una lista actualizada de conductores sin asignación en ese horario.\\[0.2em]
\end{tabular}
& EP03 \\

\hline

DS05 & Control de cambios de última hora en la asignación de conductores y estudiantes & \textbf{Como} administrador educativo, \textbf{quiero} realizar cambios de última hora en la asignación de conductores y estudiantes, \textbf{para} asegurar la continuidad del servicio ante imprevistos sin afectar el resto de la programación. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Reasignación rápida de conductor}\\
\textbf{Dado que} un conductor asignado a una ruta reporta una ausencia inesperada\\
\textbf{cuando} el administrador selecciona otro conductor disponible\\
\textbf{entonces} el sistema actualiza la asignación de forma inmediata y notifica el cambio.\\[0.2em]

\textbf{Escenario 2: Cambio de estudiante de ruta}\\
\textbf{Dado que} un estudiante no podrá abordar en su ruta habitual por razones operativas\\
\textbf{cuando} el administrador lo reasigna a otra ruta disponible\\
\textbf{entonces} el sistema actualiza la información y vincula su RFID a la nueva unidad.\\[0.2em]

\textbf{Escenario 3: Registro de cambios realizados}\\
\textbf{Dado que} se realizan modificaciones en las asignaciones\\
\textbf{cuando} el sistema guarda el historial de cambios\\
\textbf{entonces} los administradores pueden revisar qué cambios se hicieron, por quién y cuándo.\\[0.2em]
\end{tabular}
& EP03 \\

\hline
ES01 & Monitoreo en tiempo real de posición y velocidad de vehículos & \textbf{Como} administrador educativo, \textbf{quiero} conocer la posición y velocidad en tiempo real de cada vehículo, \textbf{para} monitorear sus rutas y detectar posibles retrasos o desvíos oportunamente. & 
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Visualización de datos en tiempo real}\\
\textbf{Dado que} el administrador accede al panel de monitoreo\\
\textbf{cuando} selecciona un vehículo específico\\
\textbf{entonces} el sistema muestra la ubicación actual y la velocidad en tiempo real del vehículo.\\[0.2em]

\textbf{Escenario 2: Detección de desviación de ruta}\\
\textbf{Dado que} un vehículo se encuentra fuera de su ruta predefinida\\
\textbf{cuando} el sistema detecta la desviación\\
\textbf{entonces} se genera una alerta automática para notificar al administrador.\\[0.2em]

\textbf{Escenario 3: Monitoreo continuo sin interrupciones}\\
\textbf{Dado que} el administrador visualiza el panel de monitoreo\\
\textbf{cuando} el vehículo se desplaza por su ruta\\
\textbf{entonces} el sistema actualiza de forma continua y sin fallos la posición y velocidad del vehículo.
\end{tabular}
& EP04 \\

\hline
ES02 & Monitoreo de temperatura interna de los vehículos & \textbf{Como} administrador educativo, \textbf{quiero} monitorear remotamente la temperatura interna de los vehículos, \textbf{para} asegurarme de que las condiciones sean seguras para los pasajeros. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Visualización de temperatura actual}\\
\textbf{Dado que} el supervisor accede al panel de monitoreo de temperatura\\
\textbf{cuando} selecciona un vehículo en operación\\
\textbf{entonces} el sistema muestra la temperatura interna actual en tiempo real.\\[0.2em]

\textbf{Escenario 2: Alerta por temperatura fuera de rango}\\
\textbf{Dado que} la temperatura interna del vehículo supera los límites establecidos\\
\textbf{cuando} el sistema detecta esta condición anómala\\
\textbf{entonces} se genera una alerta visual y sonora en el panel de monitoreo.\\[0.2em]

\textbf{Escenario 3: Historial de temperatura}\\
\textbf{Dado que} el supervisor desea verificar condiciones pasadas\\
\textbf{cuando} accede al historial de temperatura de un vehículo\\
\textbf{entonces} el sistema muestra un gráfico con los valores registrados durante los recorridos anteriores.
\end{tabular}
& EP04 \\

\hline
ES03 & Seguimiento de unidades de transporte para verificar salida y llegada & \textbf{Como} administrador educativo, \textbf{quiero} visualizar en tiempo real qué unidades ya han partido para recoger a los estudiantes y qué unidades ya han llegado al centro educativo, \textbf{para} hacer un seguimiento eficiente del estado de las rutas y asegurarme de que todos los estudiantes han sido recogidos o entregados. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Visualización de estado de unidades}\\
\textbf{Dado que} el administrador accede al panel de seguimiento de rutas\\
\textbf{cuando} el sistema detecta que una unidad ha iniciado su recorrido o ha llegado al colegio\\
\textbf{entonces} el estado de la unidad cambia a “En ruta” o “Llegó al destino” en tiempo real.\\[0.2em]

\textbf{Escenario 2: Confirmación de llegada al colegio}\\
\textbf{Dado que} una unidad ha llegado al colegio\\
\textbf{cuando} el GPS registra la ubicación correspondiente al centro educativo\\
\textbf{entonces} el sistema actualiza automáticamente el estado a “Llegado” y registra la hora de llegada.\\[0.2em]

\textbf{Escenario 3: Generación de reporte de estados diarios}\\
\textbf{Dado que} el administrador desea revisar la operación diaria\\
\textbf{cuando} solicita un resumen de actividad del día\\
\textbf{entonces} el sistema genera un reporte indicando qué unidades salieron, a qué hora, y si llegaron correctamente al colegio.
\end{tabular}
& EP04 \\

\hline
ES04 & Monitoreo de estudiantes que no abordaron la unidad & \textbf{Como} administrador educativo, \textbf{quiero} hacer un seguimiento de qué estudiantes no abordaron la unidad, \textbf{para} tomar acciones inmediatas y asegurarme de que todos los estudiantes estén siendo transportados de forma segura. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Identificación de estudiantes ausentes}\\
\textbf{Dado que} el sistema tiene registrados los estudiantes asignados a una ruta\\
\textbf{cuando} el lector RFID no detecta el ingreso de un estudiante asignado\\
\textbf{entonces} el sistema marca automáticamente al estudiante como “No abordó” y notifica al administrador.\\[0.2em]

\textbf{Escenario 2: Visualización en tiempo real de estudiantes faltantes}\\
\textbf{Dado que} el administrador accede al panel de ruta\\
\textbf{cuando} la unidad inicia su recorrido\\
\textbf{entonces} el panel muestra en tiempo real qué estudiantes han abordado y quiénes no.\\[0.2em]

\textbf{Escenario 3: Generación de alerta por estudiante no abordado}\\
\textbf{Dado que} un estudiante no abordó la unidad\\
\textbf{cuando} la unidad continúa su ruta sin detectarlo\\
\textbf{entonces} el sistema envía una alerta al administrador indicando el nombre del estudiante y su punto de recojo.
\end{tabular}
& EP04 \\

\hline
ES05 & Verificación de rutas alternativas en caso de desvíos & \textbf{Como} administrador educativo, \textbf{quiero} verificar y gestionar rutas alternativas en tiempo real cuando una unidad se desvía de su ruta prevista, \textbf{para} garantizar que los estudiantes lleguen a su destino de manera segura y a tiempo frente a imprevistos. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Notificación de desvío detectado}\\
\textbf{Dado que} una unidad se desvía de su ruta establecida\\
\textbf{cuando} el sistema detecta el cambio de trayectoria vía GPS\\
\textbf{entonces} se genera una notificación en el panel del administrador indicando la unidad afectada y su nueva ubicación.\\[0.2em]

\textbf{Escenario 2: Sugerencia de rutas alternativas}\\
\textbf{Dado que} el sistema detecta un desvío\\
\textbf{cuando} hay rutas alternativas disponibles\\
\textbf{entonces} el sistema sugiere automáticamente rutas alternativas al administrador para evaluación y aprobación.\\[0.2em]

\textbf{Escenario 3: Confirmación de nueva ruta}\\
\textbf{Dado que} el administrador aprueba una ruta alternativa\\
\textbf{cuando} selecciona la nueva trayectoria en el sistema\\
\textbf{entonces} el sistema actualiza la ruta de seguimiento y notifica a los dispositivos correspondientes sobre el nuevo trayecto.
\end{tabular}
& EP04 \\
\hline
ES06 & Visualización de unidades en ruta para gestionar desviaciones o retrasos & \textbf{Como} administrador educativo, \textbf{quiero} visualizar en tiempo real todas las unidades en ruta, \textbf{para} detectar rápidamente desviaciones o retrasos y tomar decisiones oportunas que aseguren el cumplimiento de los horarios y la seguridad de los estudiantes. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Visualización en tiempo real de unidades activas}\\
\textbf{Dado que} el administrador accede al panel de monitoreo\\
\textbf{cuando} se muestran todas las unidades actualmente en recorrido\\
\textbf{entonces} el sistema presenta en un mapa interactivo la ubicación, velocidad y estado de cada unidad.\\[0.2em]

\textbf{Escenario 2: Alerta por retraso detectado}\\
\textbf{Dado que} una unidad excede el tiempo estimado para un punto de control\\
\textbf{cuando} el sistema compara el tiempo real con el tiempo programado\\
\textbf{entonces} se genera una alerta visual y sonora en el panel del administrador indicando un posible retraso.\\[0.2em]

\textbf{Escenario 3: Notificación de desvío de ruta}\\
\textbf{Dado que} una unidad se desvía de su ruta asignada\\
\textbf{cuando} el sistema detecta una trayectoria no planificada\\
\textbf{entonces} se notifica al administrador con la nueva ubicación de la unidad y posibles causas del desvío (tráfico, desvío manual, etc.).
\end{tabular}
& EP04 \\

\hline
FS01 & Alerta de temperatura fuera de rango & \textbf{Como} administrador educativo, \textbf{quiero} recibir alertas en tiempo real cuando la temperatura interna de un vehículo se salga de los parámetros establecidos, \textbf{para} tomar medidas inmediatas que garanticen la seguridad y el confort de los estudiantes durante el transporte. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Recepción de alerta por alta temperatura}\\
\textbf{Dado que} la temperatura interna de una unidad supera el umbral máximo permitido\\
\textbf{cuando} el sistema de monitoreo detecta este valor anómalo\\
\textbf{entonces} el administrador educativo recibe una notificación en su panel de control y en su dispositivo móvil.\\[0.2em]

\textbf{Escenario 2: Recepción de alerta por baja temperatura}\\
\textbf{Dado que} la temperatura interna desciende por debajo del umbral mínimo aceptado\\
\textbf{cuando} se registra esta condición en el sensor del vehículo\\
\textbf{entonces} se emite una alerta inmediata con los datos del vehículo afectado.\\[0.2em]

\textbf{Escenario 3: Consulta del historial de alertas térmicas}\\
\textbf{Dado que} el administrador quiere revisar incidentes anteriores relacionados con la temperatura\\
\textbf{cuando} accede a la sección de historial de alertas\\
\textbf{entonces} el sistema muestra un listado con fecha, unidad, valor de temperatura y acción tomada.
\end{tabular}
& EP05 \\

\hline
FS02 & Alerta de retrasos o desviaciones en las rutas & \textbf{Como} administrador educativo, \textbf{quiero} recibir alertas inmediatas cuando una unidad de transporte experimente retrasos o se desvíe de la ruta establecida, \textbf{para} poder coordinar con el conductor y tomar decisiones rápidas que minimicen el impacto en el servicio y garanticen la llegada segura y oportuna de los estudiantes. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Alerta por retraso en la ruta}\\
\textbf{Dado que} una unidad excede el tiempo estimado de llegada a un punto planificado\\
\textbf{cuando} el sistema detecta el retraso basado en la comparación con el horario predefinido\\
\textbf{entonces} el administrador recibe una notificación con los detalles del vehículo y el retraso detectado.\\[0.2em]

\textbf{Escenario 2: Alerta por desvío de ruta}\\
\textbf{Dado que} una unidad sale del recorrido autorizado\\
\textbf{cuando} el sistema de geolocalización detecta que el vehículo ha tomado una vía no planificada\\
\textbf{entonces} se emite una alerta automática al panel del administrador con el mapa y ubicación actual.\\[0.2em]

\textbf{Escenario 3: Coordinación tras alerta}\\
\textbf{Dado que} se ha generado una alerta por desviación o retraso\\
\textbf{cuando} el administrador accede a la alerta desde el panel\\
\textbf{entonces} puede comunicarse directamente con el conductor y visualizar rutas alternativas sugeridas por el sistema.
\end{tabular}
& EP05 \\

\hline
FS03 & Alerta de estudiantes no abordando la unidad & \textbf{Como} administrador educativo, \textbf{quiero} recibir alertas en tiempo real cuando un estudiante asignado a una ruta no aborde la unidad, \textbf{para} poder tomar medidas inmediatas como contactar al conductor o a los padres, y así garantizar la seguridad de todos los estudiantes. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Alerta automática de no abordaje}\\
\textbf{Dado que} un estudiante asignado a una unidad no es registrado como presente\\
\textbf{cuando} el sistema detecta que el estudiante no ha sido marcado como abordado al llegar al punto de recogida\\
\textbf{entonces} se genera una alerta inmediata para el administrador con los datos del estudiante y la unidad correspondiente.\\[0.2em]

\textbf{Escenario 2: Comunicación con el conductor}\\
\textbf{Dado que} se ha recibido una alerta de no abordaje\\
\textbf{cuando} el administrador accede al panel de incidentes\\
\textbf{entonces} puede comunicarse directamente con el conductor para confirmar la ausencia del estudiante.\\[0.2em]

\textbf{Escenario 3: Registro del incidente}\\
\textbf{Dado que} un estudiante no ha abordado y se ha confirmado la situación\\
\textbf{cuando} el administrador documenta el evento\\
\textbf{entonces} el sistema registra el incidente con fecha, hora y acciones tomadas, quedando disponible para auditoría futura.
\end{tabular}
& EP05 \\

\hline
FS04 & Notificación automática ante cambios de ruta o posibles retrasos & \textbf{Como} administrador educativo, \textbf{quiero} recibir notificaciones automáticas cuando un vehículo experimente cambios de ruta o posibles retrasos, \textbf{para} poder gestionar de manera proactiva las rutas y tomar decisiones para minimizar el impacto en los horarios de transporte. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Notificación de cambio de ruta}\\
\textbf{Dado que} un vehículo ha sido desviado de su ruta planificada debido a un imprevisto\\
\textbf{cuando} el sistema detecta el cambio de ruta\\
\textbf{entonces} se envía una notificación automática al administrador, informando sobre el cambio y la nueva ruta.\\[0.2em]

\textbf{Escenario 2: Notificación de retraso}\\
\textbf{Dado que} un vehículo ha experimentado un retraso debido a condiciones de tráfico o problemas mecánicos\\
\textbf{cuando} el sistema detecta que el retraso ha superado el umbral predefinido\\
\textbf{entonces} se genera una alerta de retraso que se envía al administrador con la información relevante del vehículo.\\[0.2em]

\textbf{Escenario 3: Gestión proactiva}\\
\textbf{Dado que} se ha recibido una notificación de cambio de ruta o retraso\\
\textbf{cuando} el administrador recibe la alerta\\
\textbf{entonces} el administrador puede tomar decisiones, como notificar a los padres o ajustar las rutas de otros vehículos si es necesario.\\[0.2em]
\end{tabular}
& EP05 \\

\hline
FS05 & Alerta por fallo de equipo en el vehículo (GPS, RFID, sensores, etc.) & \textbf{Como} administrador educativo, \textbf{quiero} recibir una alerta inmediata en caso de fallo de equipos en los vehículos, como el GPS, RFID o sensores, \textbf{para} poder tomar medidas rápidas y garantizar que el control de las rutas y la seguridad de los estudiantes no se vean comprometidos. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Alerta por fallo en el GPS}\\
\textbf{Dado que} el GPS de un vehículo ha dejado de funcionar correctamente\\
\textbf{cuando} el sistema detecta la falla en el GPS\\
\textbf{entonces} se envía una alerta al administrador indicando el fallo y el vehículo afectado.\\[0.2em]

\textbf{Escenario 2: Alerta por fallo en el lector RFID}\\
\textbf{Dado que} el lector RFID del vehículo no está funcionando\\
\textbf{cuando} el sistema detecta que el lector RFID está inactivo\\
\textbf{entonces} se genera una notificación para que el administrador pueda gestionar el problema rápidamente.\\[0.2em]

\textbf{Escenario 3: Alerta por fallo en el sensor de temperatura}\\
\textbf{Dado que} el sensor de temperatura del vehículo ha dejado de funcionar\\
\textbf{cuando} el sistema detecta que el sensor no está operando correctamente\\
\textbf{entonces} se envía una notificación al administrador sobre el fallo del sensor de temperatura.\\[0.2em]
\end{tabular}
& EP05 \\

\hline
FS06 & Notificación cuando la unidad ha completado el recorrido & \textbf{Como} administrador educativo, \textbf{quiero} recibir una notificación cuando una unidad haya completado su recorrido (tanto la ruta hacia el colegio como el retorno a casa) \textbf{para} poder gestionar eficientemente la programación de las unidades, evitando retrasos y asegurando que las unidades estén disponibles para nuevas asignaciones. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Notificación de llegada al colegio}\\
\textbf{Dado que} la unidad ha llegado al colegio para dejar a los estudiantes\\
\textbf{cuando} la unidad termina su recorrido hacia el colegio\\
\textbf{entonces} el sistema envía una notificación al administrador indicando que la unidad ha completado su recorrido.\\[0.2em]

\textbf{Escenario 2: Notificación de regreso a casa}\\
\textbf{Dado que} la unidad ha terminado su recorrido de regreso a casa\\
\textbf{cuando} la unidad termina su recorrido de regreso a la casa de los estudiantes\\
\textbf{entonces} el sistema envía una notificación al administrador indicando que la unidad ha completado su recorrido.\\[0.2em]

\textbf{Escenario 3: Gestión de unidades disponibles para nuevas asignaciones}\\
\textbf{Dado que} una unidad ha completado su recorrido y está lista para una nueva asignación\\
\textbf{cuando} la unidad termina su recorrido y se encuentra disponible\\
\textbf{entonces} el administrador recibe una alerta notificando que la unidad ha completado el recorrido y está lista para la siguiente asignación.\\[0.2em]
\end{tabular}
& EP05 \\

\hline
GS01 & Reporte de tiempos de ruta y cumplimiento & \textbf{Como} administrador educativo, \textbf{quiero} generar reportes de tiempos de ruta y cumplimiento, \textbf{para} evaluar el desempeño de la flota y apoyar la toma de decisiones basadas en datos operativos. & 
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Generación exitosa del reporte}\\
\textbf{Dado que} el administrador accede al módulo de reportes\\
\textbf{cuando} selecciona un rango de fechas y parámetros específicos\\
\textbf{entonces} el sistema genera un reporte detallado que muestra los tiempos de ruta y el grado de cumplimiento de cada recorrido.\\[0.2em]

\textbf{Escenario 2: Visualización de incumplimientos}\\
\textbf{Dado que} existen desviaciones o retrasos en las rutas\\
\textbf{cuando} el administrador revisa el reporte generado\\
\textbf{entonces} el sistema destaca los casos de incumplimiento, permitiendo identificar rápidamente las áreas de mejora.\\[0.2em]

\textbf{Escenario 3: Exportación del reporte}\\
\textbf{Dado que} el administrador necesita compartir o archivar la información\\
\textbf{cuando} selecciona la opción de exportar el reporte\\
\textbf{entonces} el sistema genera un archivo descargable en formato Excel o PDF con todos los datos del reporte.
\end{tabular}
& EP06 \\

\hline
GS02 & Estadísticas de abordaje por estudiante & \textbf{Como} administrador educativo, \textbf{quiero} obtener estadísticas de abordaje por estudiante, \textbf{para} detectar patrones de retraso o ausencias y tomar acciones preventivas que mejoren la eficiencia del transporte escolar. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Generación exitosa de estadísticas}\\
\textbf{Dado que} el administrador accede al módulo de reportes\\
\textbf{cuando} selecciona la opción de estadísticas de abordaje por estudiante y define un rango de fechas\\
\textbf{entonces} el sistema genera y muestra un reporte detallado con indicadores de abordaje, incluyendo retrasos y ausencias.\\[0.2em]

\textbf{Escenario 2: Identificación de patrones repetitivos}\\
\textbf{Dado que} ciertos estudiantes presentan ausencias o retrasos de forma recurrente\\
\textbf{cuando} se visualiza el reporte generado\\
\textbf{entonces} el sistema resalta automáticamente aquellos casos, facilitando su identificación para la toma de decisiones.\\[0.2em]

\textbf{Escenario 3: Exportación del reporte}\\
\textbf{Dado que} el administrador requiere analizar o compartir la información\\
\textbf{cuando} selecciona la opción de exportar el reporte\\
\textbf{entonces} el sistema genera un archivo descargable en formato Excel o PDF con todas las estadísticas de abordaje.
\end{tabular}
& EP06 \\

\hline
GS03 & Exportación de datos históricos en Excel/PDF & \textbf{Como} responsable de calidad, \textbf{quiero} exportar datos históricos en formatos Excel o PDF, \textbf{para} presentarlos en auditorías o juntas directivas y facilitar la toma de decisiones estratégicas basadas en datos históricos. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Exportación exitosa de datos históricos}\\
\textbf{Dado que} el responsable de calidad accede al módulo de reportes\\
\textbf{cuando} selecciona la opción de exportar datos históricos y define el rango de fechas\\
\textbf{entonces} el sistema genera un archivo Excel o PDF con todos los datos solicitados.\\[0.2em]

\textbf{Escenario 2: Formato adecuado para auditorías}\\
\textbf{Dado que} el archivo exportado debe ser adecuado para auditorías y presentaciones\\
\textbf{cuando} el responsable de calidad abre el archivo exportado\\
\textbf{entonces} los datos están organizados de manera clara y profesional, listos para ser presentados en auditorías o juntas directivas.\\[0.2em]

\textbf{Escenario 3: Verificación de datos exportados}\\
\textbf{Dado que} el responsable de calidad necesita asegurarse de que los datos exportados sean correctos\\
\textbf{cuando} abre el archivo exportado\\
\textbf{entonces} puede verificar que todos los datos históricos correspondientes al rango de fechas seleccionado están correctamente reflejados en el archivo.
\end{tabular}
& EP06 \\

\hline
GS04 & Reporte de incidencias críticas & \textbf{Como} administrador del sistema, \textbf{quiero} generar reportes de incidencias críticas, \textbf{para} consolidar y analizar eventos como alertas de temperatura, desviaciones de ruta o fallos de equipo, con el fin de identificar patrones recurrentes y focalizar acciones de mejora continua en la gestión de transporte escolar. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Generación de reporte de incidencias críticas}\\
\textbf{Dado que} el administrador accede a la sección de reportes de incidencias críticas\\
\textbf{cuando} selecciona el rango de fechas y los tipos de incidencias a analizar\\
\textbf{entonces} el sistema genera un reporte consolidado con los eventos críticos seleccionados, detallando cada incidencia por tipo y fecha.\\[0.2em]

\textbf{Escenario 2: Análisis de patrones de incidencias}\\
\textbf{Dado que} el reporte contiene incidencias críticas,\\
\textbf{cuando} el administrador revisa el reporte\\
\textbf{entonces} puede identificar patrones recurrentes en las incidencias y determinar áreas específicas para aplicar acciones correctivas.\\[0.2em]

\textbf{Escenario 3: Exportación del reporte de incidencias críticas}\\
\textbf{Dado que} el administrador necesita compartir el reporte con otros miembros del equipo\\
\textbf{cuando} el administrador elige la opción de exportar el reporte\\
\textbf{entonces} el sistema permite exportar el reporte en formatos como PDF o Excel para su distribución y análisis adicional. 
\end{tabular}
& EP06 \\

\hline
GS05 & Programación de envíos automáticos de reportes & \textbf{Como} administrador del sistema, \textbf{quiero} programar envíos automáticos de reportes, \textbf{para} automatizar la distribución periódica de reportes (diarios, semanales o mensuales) a los responsables, garantizando que la información llegue a tiempo sin necesidad de intervención manual. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Programación de envío automático de reportes}\\
\textbf{Dado que} el administrador desea enviar reportes periódicamente\\
\textbf{cuando} el administrador configura la periodicidad (diaria, semanal o mensual) y los destinatarios del reporte\\
\textbf{entonces} el sistema programará el envío automático de los reportes en los intervalos establecidos.\\[0.2em]

\textbf{Escenario 2: Confirmación de programación de reportes}\\
\textbf{Dado que} el administrador ha configurado la programación de envíos automáticos\\
\textbf{cuando} el administrador guarda la configuración de la programación\\
\textbf{entonces} el sistema mostrará una notificación confirmando que los envíos automáticos han sido correctamente programados.\\[0.2em]

\textbf{Escenario 3: Modificación de la programación de reportes}\\
\textbf{Dado que} el administrador desea cambiar la programación de los envíos de reportes\\
\textbf{cuando} el administrador modifica la frecuencia o los destinatarios de los reportes\\
\textbf{entonces} el sistema actualizará la programación de los envíos automáticos según los nuevos parámetros establecidos.\\[0.2em]
\end{tabular}
& EP06 \\

\hline
GS06 & Filtrado y segmentación de datos históricos & \textbf{Como} administrador del sistema, \textbf{quiero} filtrar y segmentar datos históricos por ruta, vehículo, conductor o rango de fechas, \textbf{para} optimizar el análisis detallado y la preparación de informes personalizados para auditorías o reuniones de gestión. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Filtrado de datos históricos por ruta}\\
\textbf{Dado que} el administrador necesita analizar los datos de una ruta específica\\
\textbf{cuando} el administrador selecciona una ruta y aplica el filtro\\
\textbf{entonces} el sistema mostrará solo los datos históricos relacionados con esa ruta.\\[0.2em]

\textbf{Escenario 2: Filtrado de datos históricos por vehículo}\\
\textbf{Dado que} el administrador desea analizar los datos de un vehículo específico\\
\textbf{cuando} el administrador selecciona un vehículo y aplica el filtro\\
\textbf{entonces} el sistema mostrará solo los datos históricos relacionados con ese vehículo.\\[0.2em]

\textbf{Escenario 3: Filtrado de datos históricos por conductor}\\
\textbf{Dado que} el administrador desea revisar el desempeño de un conductor\\
\textbf{cuando} el administrador selecciona un conductor y aplica el filtro\\
\textbf{entonces} el sistema mostrará solo los datos históricos relacionados con ese conductor.\\[0.2em]
\end{tabular}
& EP06 \\

\hline
HS01 & Dashboard con KPIs clave & \textbf{Como} administrador educativo, \textbf{quiero} acceder a un dashboard que muestre KPIs clave (número de rutas activas, incidencias, temperatura media, etc.), \textbf{para} monitorear la operación del transporte escolar de un vistazo y tomar decisiones basadas en datos en tiempo real. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Visualización del dashboard}\\
\textbf{Dado que} el administrador accede a la plataforma web\\
\textbf{cuando} ingresa al módulo de administración\\
\textbf{entonces} el sistema muestra un dashboard con KPIs actualizados en tiempo real, incluyendo número de rutas activas, incidencias registradas y temperatura media de las unidades.\\[0.2em]

\textbf{Escenario 2: Actualización en tiempo real}\\
\textbf{Dado que} se registran nuevos eventos en el sistema (por ejemplo, incidencias o cambios en las rutas)\\
\textbf{cuando} el administrador visualiza el dashboard\\
\textbf{entonces} el sistema actualiza automáticamente los KPIs para reflejar la situación actual.\\[0.2em]

\textbf{Escenario 3: Personalización del dashboard}\\
\textbf{Dado que} el administrador tiene necesidades específicas de información\\
\textbf{cuando} utiliza las opciones de configuración del dashboard\\
\textbf{entonces} el sistema permite personalizar la visualización de KPIs según preferencias (por ejemplo, mostrar o ocultar ciertos indicadores).
\end{tabular}
& EP07 \\

\hline
HS02 & Gestión de roles y permisos & \textbf{Como} administrador educativo, \textbf{quiero} gestionar los roles y permisos de los usuarios (coordinadores, supervisores, etc.), \textbf{para} delegar responsabilidades con seguridad y asegurarme de que cada usuario solo tenga acceso a la información y funciones necesarias para su rol. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Asignación de roles}\\
\textbf{Dado que} soy un administrador con privilegios para gestionar usuarios\\
\textbf{cuando} accedo al módulo de gestión de roles\\
\textbf{entonces} puedo asignar un rol a cada usuario (coordinador, supervisor, etc.), permitiendo el acceso correspondiente a funcionalidades específicas de la plataforma.\\[0.2em]

\textbf{Escenario 2: Edición de permisos de usuario}\\
\textbf{Dado que} tengo un usuario con permisos predefinidos\\
\textbf{cuando} accedo a la configuración de permisos de un usuario\\
\textbf{entonces} puedo modificar los permisos para permitir o restringir el acceso a ciertas funciones de la plataforma, como el monitoreo de rutas o la generación de reportes.\\[0.2em]

\textbf{Escenario 3: Eliminar un rol o usuario}\\
\textbf{Dado que} soy administrador de la plataforma\\
\textbf{cuando} decido eliminar un rol o usuario\\
\textbf{entonces} puedo eliminar el acceso de ese rol o usuario de la plataforma de forma segura, asegurando que no tenga acceso a ninguna función después de la eliminación.\\[0.2em]
\end{tabular}
& EP07 \\

\hline
HS03 & Configuración de parámetros globales & \textbf{Como} administrador educativo, \textbf{quiero} configurar parámetros globales (como los umbrales de temperatura, la frecuencia de reporte GPS, etc.), \textbf{para} adaptar el sistema a las políticas internas de la institución y asegurar el funcionamiento adecuado de la plataforma. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Configuración de umbrales de temperatura}\\
\textbf{Dado que} soy un administrador con privilegios para configurar parámetros\\
\textbf{cuando} accedo a la sección de configuración de umbrales de temperatura\\
\textbf{entonces} puedo establecer un valor mínimo y máximo para la temperatura dentro de los vehículos, de modo que el sistema me notifique si se supera cualquier umbral configurado.\\[0.2em]

\textbf{Escenario 2: Configuración de frecuencia de reporte GPS}\\
\textbf{Dado que} soy administrador y quiero personalizar la frecuencia de los reportes GPS\\
\textbf{cuando} accedo a la configuración de la frecuencia de reporte GPS\\
\textbf{entonces} puedo establecer un intervalo de tiempo para la actualización de la ubicación de los vehículos en el sistema.\\[0.2em]

\textbf{Escenario 3: Configuración de alertas automáticas}\\
\textbf{Dado que} soy administrador y quiero configurar alertas automáticas\\
\textbf{cuando} accedo a la sección de alertas automáticas\\
\textbf{entonces} puedo establecer condiciones para recibir notificaciones, como cuando un vehículo se desvía de la ruta planificada.\\[0.2em]
\end{tabular}
& EP07 \\

\hline
HS04 & Registro de auditoría de actividad & \textbf{Como} administrador educativo, \textbf{quiero} llevar un registro de auditoría de todas las acciones realizadas por los administradores y supervisores (como la creación/edición de usuarios, cambios en rutas, ajustes de parámetros), \textbf{para} garantizar la trazabilidad y el cumplimiento de normativas internas. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Registro de ajustes de parámetros}\\
\textbf{Dado que} soy un administrador y ajusto los parámetros globales del sistema\\
\textbf{cuando} guardo la nueva configuración de parámetros\\
\textbf{entonces} el sistema registra la acción en el historial de auditoría, detallando los parámetros modificados y el usuario responsable de la acción.\\[0.2em]

\textbf{Escenario 2: Acceso al historial de auditoría}\\
\textbf{Dado que} soy un administrador con privilegios para acceder al historial de auditoría\\
\textbf{cuando} accedo a la sección de auditoría en el sistema\\
\textbf{entonces} puedo visualizar un registro detallado de todas las acciones realizadas, con opciones para filtrar por tipo de acción, usuario y otros criterios relevantes.\\[0.2em]

\textbf{Escenario 3: Notificación de acciones no autorizadas}\\
\textbf{Dado que} un supervisor o administrador realiza una acción no autorizada\\
\textbf{cuando} la acción es registrada en el historial de auditoría\\
\textbf{entonces} el sistema genera una notificación para alertar a los administradores responsables de la supervisión de la acción no autorizada.
\end{tabular}
& EP07 \\

\hline
HS05 & Configuración de notificaciones y alertas & \textbf{Como} administrador educativo, \textbf{quiero} configurar qué tipos de notificaciones y alertas deseo recibir, por qué canal (correo electrónico, SMS, notificación push) y con qué umbrales, \textbf{para} adaptar la comunicación del sistema a los procesos internos de la institución. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Configuración de tipos de alertas}\\
\textbf{Dado que} soy un administrador con acceso a la configuración de notificaciones\\
\textbf{cuando} ingreso a la sección de tipos de alertas en el sistema\\
\textbf{entonces} puedo seleccionar qué tipos de eventos (temperatura fuera de rango, desviaciones de ruta, fallos de equipo, etc.) deseo recibir como notificación.\\[0.2em]

\textbf{Escenario 2: Selección de canales de notificación}\\
\textbf{Dado que} he seleccionado los tipos de alertas que deseo recibir\\
\textbf{cuando} configuro el canal de envío\\
\textbf{entonces} puedo elegir entre correo electrónico, SMS o notificaciones push, y guardar mis preferencias para cada tipo de alerta.\\[0.2em]

\textbf{Escenario 3: Definición de umbrales personalizados}\\
\textbf{Dado que} quiero personalizar cuándo se activa una alerta\\
\textbf{cuando} ingreso al módulo de configuración de umbrales\\
\textbf{entonces} puedo definir valores específicos (por ejemplo, temperatura máxima de 28°C, retraso superior a 10 minutos) que disparen las notificaciones correspondientes.\\[0.2em]
\end{tabular}
& EP07 \\

\hline
HS06 & Personalización del dashboard & \textbf{Como} administrador educativo, \textbf{quiero} personalizar el dashboard seleccionando qué widgets visualizar, su orden y frecuencia de actualización, \textbf{para} adaptar la interfaz a las prioridades específicas de mi institución y mejorar la usabilidad del sistema. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Selección de widgets del dashboard}\\
\textbf{Dado que} estoy visualizando el dashboard de administración\\
\textbf{cuando} ingreso al modo de personalización\\
\textbf{entonces} puedo seleccionar los widgets que deseo visualizar, como incidencias, rutas activas, estado de vehículos, estadísticas de abordaje, etc.\\[0.2em]

\textbf{Escenario 2: Reordenamiento de widgets}\\
\textbf{Dado que} he seleccionado los widgets de mi interés\\
\textbf{cuando} arrastro los elementos en la interfaz\\
\textbf{entonces} puedo reorganizarlos para que los más importantes estén visibles en la parte superior del dashboard.\\[0.2em]

\textbf{Escenario 3: Guardado de configuración personalizada}\\
\textbf{Dado que} he personalizado el dashboard a mis necesidades\\
\textbf{cuando} guardo los cambios\\
\textbf{entonces} el sistema almacena mi configuración para que se mantenga en futuras sesiones.\\[0.2em]
\end{tabular}
& EP07 \\

\hline

\end{longtable}

\newpage

### Tutor legal o familiar

***Epics*** **y** ***User Stories:***

\begin{longtable}{|m{5cm}|m{10cm}|}
\hline
\textbf{EP01 (Gestión de Cuentas de Padres)} & \textbf{Como} tutor legal, \textbf{quiero} gestionar mi cuenta de manera segura, para acceder a la aplicación móvil y administrar el seguimiento del transporte de mi hijo. \\
\hline
US01 & Registro e Inicio de Sesión \\
\hline
US02 & Recuperación de Contraseña \\
\hline
US03 & Edición de Perfil \\
\hline
US04 & Gestión de Dispositivos de Notificación \\
\hline
\textbf{EP02 (Seguimiento en Tiempo Real)} & \textbf{Como} tutor legal, \textbf{quiero} conocer la ubicación y el progreso de la ruta de transporte de mi hijo en tiempo real, para poder organizarme y estar informado. \\
\hline
CS01 & Ubicación en Vivo del Vehículo \\
\hline
CS02 & Consulta de Ruta Planificada \\
\hline
CS03 & Estimación de Tiempo Restante \\
\hline
\textbf{EP03 (Notificaciones y Alertas)} & \textbf{Como} tutor legal, \textbf{quiero} recibir alertas y notificaciones sobre los eventos críticos del viaje de mi hijo, para asegurarme de que todo esté en orden durante el trayecto. \\
\hline
DS01 & Notificación de Abordaje \\
\hline
DS02 & Notificación de Llegada \\
\hline
DS03 & Alerta por Desvío o Retraso \\
\hline
DS04 & Alerta de Temperatura Insegura \\
\hline
\textbf{EP04 (Supervisión Visual)} & \textbf{Como} tutor legal, \textbf{quiero} tener acceso en tiempo real a la transmisión de video desde la cámara a bordo, para poder supervisar el viaje de mi hijo en todo momento. \\
\hline
ES01 & Supervisión en Tiempo Real (Ida) \\
\hline
ES02 & Supervisión en Tiempo Real (Regreso) \\
\hline
\textbf{EP05 (Historial y Reportes Personales)} & \textbf{Como} tutor legal, \textbf{quiero} tener acceso al historial de viajes y eventos pasados de mi hijo, para poder revisar patrones de comportamiento y reportar cualquier anomalía. \\
\hline
FS01 & Historial de Rutas Diarias \\
\hline
FS02 & Log de Eventos Recientes \\
\hline
FS03 & Exportación de Historial \\
\hline
\textbf{EP06 (Preferencias y Configuración)} & \textbf{Como} tutor legal, \textbf{quiero} poder personalizar mi experiencia en la aplicación móvil, para ajustarla a mis necesidades y preferencias personales. \\
\hline
GS01 & Selección de Notificaciones por Hijo \\
\hline
GS02 & Definición de Horarios de Silencio \\
\hline
GS03 & Personalización de Idioma y Tema \\
\hline
\textbf{EP07 (Soporte y Comunicación)} & \textbf{Como} tutor legal, \textbf{quiero} poder comunicarme con el conductor o el administrador, y reportar incidencias, para resolver cualquier problema que surja durante el trayecto. \\
\hline
HS01 & Comunicación Directa con el Conductor \\
\hline
HS02 & Reporte de Incidencias con Evidencia \\
\hline
HS03 & Acceso a Ayuda y Preguntas Frecuentes \\
\hline
\end{longtable}

\newpage

***User Stories:***

\begin{longtable}{|p{1cm}|p{3cm}|p{4cm}|p{5cm}|p{1cm}|}
\hline
\multicolumn{1}{|c|}{\textbf{ID}} & \multicolumn{1}{c|}{\textbf{Título}} & \multicolumn{1}{c|}{\textbf{Descripción}} & \multicolumn{1}{c|}{\textbf{Criterios de Aceptación}} & \multicolumn{1}{c|}{\textbf{Epic}} \\
\hline
US01 & Registro e Inicio de Sesión & \textbf{Como} tutor legal, \textbf{quiero} registrarme e iniciar sesión con mi cuenta, \textbf{para} acceder de forma segura a la aplicación móvil y administrar el seguimiento del transporte de mi hijo. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Registro exitoso}\\
\textbf{Dado que} accedo al formulario de registro en la aplicación móvil\\
\textbf{cuando} ingreso mis datos personales (nombre, correo electrónico, número de teléfono) y creo una contraseña segura\\
\textbf{entonces} el sistema valida mi información, crea mi cuenta y me dirige a la pantalla de inicio.\\[0.2em]

\textbf{Escenario 2: Inicio de sesión exitoso}\\
\textbf{Dado que} ya poseo una cuenta registrada\\
\textbf{cuando} ingreso mis credenciales correctas (correo electrónico y contraseña) en el formulario de inicio de sesión\\
\textbf{entonces} el sistema autentica mi identidad y me permite acceder a la aplicación móvil.\\[0.2em]

\textbf{Escenario 3: Error en registro por datos incompletos o inválidos}\\
\textbf{Dado que} intento registrarme\\
\textbf{cuando} omito algún campo obligatorio o ingreso datos en formato incorrecto\\
\textbf{entonces} el sistema muestra mensajes de error específicos indicando la necesidad de completar o corregir la información ingresada.\\[0.2em]
\end{tabular}
& EP01 \\

\hline
US02 & Recuperación de Contraseña & \textbf{Como} tutor legal, \textbf{quiero} recuperar mi contraseña vía correo o SMS, \textbf{para} restablecer el acceso en caso de olvido y seguir utilizando la aplicación sin inconvenientes. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Solicitud de recuperación exitosa}\\
\textbf{Dado que} he olvidado mi contraseña\\
\textbf{cuando} selecciono la opción “¿Olvidaste tu contraseña?” en la pantalla de inicio de sesión\\
\textbf{y} proporciono mi correo electrónico o número de teléfono registrado\\
\textbf{entonces} el sistema envía un enlace o código de verificación para restablecer la contraseña.\\[0.2em]

\textbf{Escenario 2: Ingreso de nueva contraseña}\\
\textbf{Dado que} recibí el enlace o código de recuperación\\
\textbf{cuando} accedo al formulario correspondiente\\
\textbf{y} establezco una nueva contraseña válida\\
\textbf{entonces} el sistema actualiza la contraseña y me permite iniciar sesión con la nueva clave.\\[0.2em]

\textbf{Escenario 3: Error por correo o número no registrado}\\
\textbf{Dado que} intento recuperar mi contraseña\\
\textbf{cuando} ingreso un correo electrónico o número de teléfono no registrado en el sistema\\
\textbf{entonces} el sistema muestra un mensaje de error indicando que no se encuentra ninguna cuenta asociada.\\[0.2em]
\end{tabular}
& EP01 \\

\hline
US03 & Edición de Perfil & \textbf{Como} tutor legal, \textbf{quiero} editar mi perfil (datos de contacto) y la información de mis hijos (grado, pulsera RFID), \textbf{para} mantener toda la información actualizada y garantizar una correcta gestión del transporte. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Edición de datos de contacto exitosa}\\
\textbf{Dado que} accedo a la sección de perfil desde la aplicación móvil\\
\textbf{cuando} modifico mis datos de contacto como correo electrónico o número de teléfono\\
\textbf{entonces} el sistema guarda los cambios y muestra un mensaje de confirmación.\\[0.2em]

\textbf{Escenario 2: Edición de información del hijo}\\
\textbf{Dado que} deseo actualizar la información de mi hijo\\
\textbf{cuando} cambio el grado escolar o actualizo el identificador de su pulsera RFID\\
\textbf{entonces} el sistema almacena la nueva información correctamente.\\[0.2em]

\textbf{Escenario 3: Validación de campos obligatorios}\\
\textbf{Dado que} estoy editando mi perfil o la información de mi hijo\\
\textbf{cuando} dejo campos obligatorios vacíos o ingreso datos inválidos\\
\textbf{entonces} el sistema muestra mensajes de advertencia solicitando corrección antes de guardar.\\[0.2em]
\end{tabular}
& EP01 \\

\hline
US04 & Gestión de Dispositivos de Notificación & \textbf{Como} tutor legal, \textbf{quiero} gestionar mis dispositivos de notificación (push, email, SMS), \textbf{para} elegir cómo y cuándo recibir alertas sobre el transporte de mi hijo. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Configuración de canal de notificación preferido}\\
\textbf{Dado que} accedo a la configuración de notificaciones en la aplicación móvil\\
\textbf{cuando} selecciono uno o más canales como push, email o SMS\\
\textbf{entonces} el sistema guarda mis preferencias y las usa para futuras alertas.\\[0.2em]

\textbf{Escenario 2: Desactivación de un canal específico}\\
\textbf{Dado que} ya no deseo recibir notificaciones por un canal específico\\
\textbf{cuando} desactivo dicho canal desde la configuración\\
\textbf{entonces} el sistema deja de enviar notificaciones por ese medio.\\[0.2em]

\textbf{Escenario 3: Personalización de tipos de alertas}\\
\textbf{Dado que} deseo recibir solo ciertos tipos de alertas (abordaje, llegada, temperatura)\\
\textbf{cuando} selecciono mis preferencias dentro de la aplicación\\
\textbf{entonces} el sistema me notificará solo sobre los eventos seleccionados.\\[0.2em]
\end{tabular}
& EP01 \\

\hline
CS01 & Ubicación en Vivo del Vehículo & \textbf{Como} tutor legal, \textbf{quiero} ver la posición en vivo del vehículo que transporta a mi hijo, \textbf{para} estimar su hora de llegada y estar preparado ante cualquier eventualidad. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Visualización de la ubicación en tiempo real}\\
\textbf{Dado que} tengo acceso a la aplicación móvil como padre registrado\\
\textbf{cuando} ingreso a la sección de seguimiento\\
\textbf{entonces} el sistema muestra un mapa con la ubicación actual del vehículo en movimiento.\\[0.2em]

\textbf{Escenario 2: Actualización automática de la ubicación}\\
\textbf{Dado que} estoy visualizando el mapa de seguimiento\\
\textbf{cuando} el vehículo avanza por su ruta\\
\textbf{entonces} la ubicación se actualiza automáticamente cada cierto intervalo de tiempo (ej. cada 10 segundos).\\[0.2em]

\textbf{Escenario 3: Indicador del estudiante a bordo}\\
\textbf{Dado que} estoy visualizando la ubicación del vehículo\\
\textbf{cuando} mi hijo ha abordado o descendido del vehículo\\
\textbf{entonces} el sistema indica el estado del estudiante (a bordo / descendido) junto al ícono del vehículo.\\[0.2em]
\end{tabular}
& EP02 \\

\hline
CS02 & Consulta de Ruta Planificada & \textbf{Como} tutor legal, \textbf{quiero} consultar la ruta planificada y el progreso del recorrido, \textbf{para} saber por dónde va el vehículo y cuánto falta para que llegue a su destino. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Visualización de ruta planificada}\\
\textbf{Dado que} tengo acceso a la aplicación móvil\\
\textbf{cuando} ingreso a la sección de seguimiento\\
\textbf{entonces} se muestra la ruta completa planificada del vehículo, incluyendo puntos de abordaje y destino final.\\[0.2em]

\textbf{Escenario 2: Progreso de la ruta en porcentaje}\\
\textbf{Dado que} estoy visualizando la ruta del vehículo\\
\textbf{cuando} el vehículo avanza a lo largo de su trayecto\\
\textbf{entonces} el sistema muestra un indicador del porcentaje de ruta completado en tiempo real.\\[0.2em]

\textbf{Escenario 3: Resaltado de tramos recorridos y pendientes}\\
\textbf{Dado que} estoy viendo el mapa con la ruta\\
\textbf{cuando} el vehículo avanza\\
\textbf{entonces} los tramos recorridos se resaltan con un color distinto al de los tramos pendientes.\\[0.2em]
\end{tabular}
& EP02 \\

\hline
CS03 & Estimación de Tiempo Restante & \textbf{Como} tutor legal, \textbf{quiero} recibir la estimación de tiempo restante hasta el punto de recogida o entrega de mi hijo, \textbf{para} poder organizarme mejor y estar preparado a tiempo. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Visualización del tiempo estimado de llegada}\\
\textbf{Dado que} estoy en la aplicación móvil y consulto el estado del vehículo\\
\textbf{cuando} selecciono el punto de recogida o entrega de mi hijo\\
\textbf{entonces} el sistema muestra la hora estimada de llegada del vehículo.\\[0.2em]

\textbf{Escenario 2: Actualización dinámica del tiempo restante}\\
\textbf{Dado que} el vehículo está en movimiento\\
\textbf{cuando} hay cambios en el tráfico o desvíos\\
\textbf{entonces} la estimación de tiempo se actualiza automáticamente en la aplicación.\\[0.2em]

\textbf{Escenario 3: Notificación de proximidad}\\
\textbf{Dado que} el vehículo está próximo al punto de recogida o entrega\\
\textbf{cuando} está a menos de 5 minutos de distancia\\
\textbf{entonces} recibo una notificación indicando que el vehículo está cerca.\\[0.2em]
\end{tabular}
& EP02 \\

\hline
DS01 & Notificación de Abordaje & \textbf{Como} tutor legal, \textbf{quiero} recibir una notificación cuando mi hijo aborde la unidad, \textbf{para} saber que ha subido correctamente al vehículo y estar tranquilo durante el viaje. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Notificación exitosa de abordaje}\\
\textbf{Dado que} el sistema detecta la lectura exitosa de la pulsera RFID de mi hijo al abordar la unidad\\
\textbf{cuando} se registra el evento en el sistema\\
\textbf{entonces} recibo de inmediato una notificación en mi dispositivo móvil indicando “Abordaje exitoso: [Nombre del estudiante] ha subido a la unidad”.\\[0.2em]

\textbf{Escenario 2: Notificación en caso de retraso en el registro}\\
\textbf{Dado que} mi hijo aborda la unidad, pero la lectura RFID se demora por cuestiones técnicas\\
\textbf{cuando} el sistema eventualmente procesa la lectura\\
\textbf{entonces} recibo una notificación tardía indicando el abordaje y se me informa del retraso en la actualización.\\[0.2em]

\textbf{Escenario 3: Manejo de error en la lectura}\\
\textbf{Dado que} ocurre un error en la lectura de la pulsera RFID al abordar\\
\textbf{cuando} el sistema no puede confirmar el abordaje automáticamente\\
\textbf{entonces} recibo una notificación de “Abordaje pendiente” solicitando que se verifique manualmente el estado del estudiante.
\end{tabular}
& EP03 \\

\hline
DS02 & Notificación de Llegada & \textbf{Como} tutor legal, \textbf{quiero} recibir una notificación cuando mi hijo llegue al colegio o a casa, \textbf{para} confirmar su arribo seguro y tener tranquilidad sobre el cumplimiento del recorrido. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Notificación de llegada al colegio}\\
\textbf{Dado que} la unidad llega al punto de destino (colegio) y se detecta la bajada del estudiante mediante su pulsera RFID\\
\textbf{cuando} se registra la salida del vehículo y la lectura de la pulsera\\
\textbf{entonces} recibo una notificación que indica “Llegada confirmada: [Nombre del estudiante] ha llegado al colegio”.\\[0.2em]

\textbf{Escenario 2: Notificación de llegada a casa}\\
\textbf{Dado que} mi hijo está retornando del colegio y el vehículo llega al punto de bajada en casa\\
\textbf{cuando} se registra la lectura RFID al bajar de la unidad\\
\textbf{entonces} recibo una notificación que indica “Llegada confirmada: [Nombre del estudiante] ha llegado a casa”.\\[0.2em]

\textbf{Escenario 3: Fallo en la detección de bajada}\\
\textbf{Dado que} mi hijo llega al destino pero el sistema no detecta la bajada\\
\textbf{cuando} no se recibe lectura RFID al descender\\
\textbf{entonces} recibo una notificación de alerta indicando “No se ha confirmado la bajada de [Nombre del estudiante], por favor verifique el estado”.
\end{tabular}
& EP03 \\

\hline
DS03 & Alerta por Desvío o Retraso & \textbf{Como} tutor legal, \textbf{quiero} recibir una alerta si el vehículo se desvía de la ruta o sufre un retraso significativo, \textbf{para} estar informado de cualquier incidencia que pueda afectar la seguridad o puntualidad del trayecto de mi hijo. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Alerta por desvío de ruta}\\
\textbf{Dado que} el vehículo escolar está siguiendo una ruta planificada\\
\textbf{cuando} el sistema detecta que se ha desviado significativamente del trayecto autorizado\\
\textbf{entonces} recibo una notificación indicando “Alerta: Desvío detectado en la ruta del vehículo de [Nombre del estudiante]”.\\[0.2em]

\textbf{Escenario 2: Alerta por retraso significativo}\\
\textbf{Dado que} el vehículo está en tránsito hacia el colegio o hacia casa\\
\textbf{cuando} el tiempo estimado de llegada se ve superado en más de 10 minutos respecto al plan inicial\\
\textbf{entonces} recibo una notificación que indica “Alerta: Retraso en el trayecto del vehículo de [Nombre del estudiante]”.\\[0.2em]

\textbf{Escenario 3: Confirmación de resolución de incidente}\\
\textbf{Dado que} se ha enviado una alerta por desvío o retraso\\
\textbf{cuando} el sistema detecta que el vehículo ha retomado su ruta o se ha normalizado el tiempo estimado\\
\textbf{entonces} recibo una notificación indicando “Actualización: La unidad de [Nombre del estudiante] ha retomado su ruta con normalidad”.
\end{tabular}
& EP03 \\

\hline
DS04 & Alerta de Temperatura Insegura & \textbf{Como} tutor legal, \textbf{quiero} recibir una alerta si la temperatura interna del vehículo sale de los rangos seguros, \textbf{para} asegurarme del confort y la seguridad de mi hijo durante el trayecto. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Alerta por temperatura alta}\\
\textbf{Dado que} el sistema monitorea constantemente la temperatura dentro del vehículo\\
\textbf{cuando} la temperatura interna supera los 30°C\\
\textbf{entonces} recibo una notificación que indica “Alerta: Temperatura elevada en la unidad de [Nombre del estudiante]”.\\[0.2em]

\textbf{Escenario 2: Alerta por temperatura baja}\\
\textbf{Dado que} el sistema detecta condiciones térmicas inusuales dentro del vehículo\\
\textbf{cuando} la temperatura interna desciende por debajo de los 15°C\\
\textbf{entonces} recibo una notificación que indica “Alerta: Temperatura baja en la unidad de [Nombre del estudiante]”.\\[0.2em]

\textbf{Escenario 3: Confirmación de temperatura normalizada}\\
\textbf{Dado que} se ha enviado una alerta por temperatura insegura\\
\textbf{cuando} el sistema detecta que la temperatura vuelve al rango seguro (15°C a 30°C)\\
\textbf{entonces} recibo una notificación indicando “Actualización: Temperatura normalizada en la unidad de [Nombre del estudiante]”.
\end{tabular}
& EP03 \\

\hline
ES01 & Supervisión en Tiempo Real (Ida) & \textbf{Como} tutor legal, \textbf{quiero} ver en tiempo real el video de la cámara instalada en la unidad durante el trayecto de ida, \textbf{para} supervisar las condiciones del viaje y asegurarme de que mi hijo se encuentre en un ambiente seguro. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Acceso a la transmisión en vivo}\\
\textbf{Dado que} he iniciado sesión en la aplicación móvil\\
\textbf{cuando} selecciono la opción de supervisión en tiempo real para el trayecto de ida\\
\textbf{entonces} el sistema muestra la transmisión en vivo de la cámara a bordo del vehículo.\\[0.2em]

\textbf{Escenario 2: Calidad y estabilidad de la transmisión}\\
\textbf{Dado que} estoy visualizando la transmisión en vivo\\
\textbf{cuando} la conexión es estable y la cámara opera correctamente\\
\textbf{entonces} la imagen se muestra en alta calidad y con mínimo retraso, permitiéndome supervisar el viaje de forma clara.\\[0.2em]

\textbf{Escenario 3: Notificación de fallo en la transmisión}\\
\textbf{Dado que} la transmisión en vivo presenta problemas (pérdida de conexión, imagen borrosa, etc.)\\
\textbf{cuando} el sistema detecta un fallo en la transmisión\\
\textbf{entonces} recibo una notificación indicando “Problema en la transmisión en tiempo real”, invitándome a verificar la conexión o contactar soporte técnico.
\end{tabular}
& EP04 \\

\hline
ES02 & Supervisión en Tiempo Real (Regreso) & \textbf{Como} tutor legal, \textbf{quiero} ver en tiempo real el video de la cámara instalada en la unidad durante el trayecto de regreso, \textbf{para} asegurarme del bienestar de mi hijo y supervisar las condiciones del viaje de regreso a casa. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Acceso a la transmisión en vivo}\\
\textbf{Dado que} he iniciado sesión en la aplicación móvil\\
\textbf{cuando} selecciono la opción de supervisión en tiempo real para el trayecto de regreso\\
\textbf{entonces} el sistema muestra la transmisión en vivo de la cámara a bordo del vehículo.\\[0.2em]

\textbf{Escenario 2: Calidad y estabilidad de la transmisión}\\
\textbf{Dado que} estoy visualizando la transmisión en vivo\\
\textbf{cuando} la conexión es estable y la cámara funciona correctamente\\
\textbf{entonces} la imagen se muestra en alta calidad y con mínimo retraso, permitiéndome supervisar el viaje de regreso sin inconvenientes.\\[0.2em]

\textbf{Escenario 3: Notificación de fallo en la transmisión}\\
\textbf{Dado que} la transmisión en vivo presenta problemas (pérdida de conexión, imagen borrosa, etc.)\\
\textbf{cuando} el sistema detecta un fallo en la transmisión\\
\textbf{entonces} recibo una notificación indicando “Problema en la transmisión en tiempo real”, sugiriéndome verificar la conexión o contactar soporte técnico.
\end{tabular}
& EP04 \\

\hline
FS01 & Historial de Rutas Diarias & \textbf{Como} tutor legal, \textbf{quiero} consultar el historial de rutas diarias de mi hijo, \textbf{para} revisar su puntualidad y los recorridos anteriores, asegurándome de que todo transcurra como estaba planificado. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Consulta de historial de rutas diarias}\\
\textbf{Dado que} he iniciado sesión en la aplicación móvil\\
\textbf{cuando} accedo a la sección de historial de rutas diarias\\
\textbf{entonces} el sistema muestra una lista de las rutas realizadas por el vehículo con las fechas y horarios correspondientes.\\[0.2em]

\textbf{Escenario 2: Filtrado por fecha o rango de fechas}\\
\textbf{Dado que} quiero revisar las rutas realizadas en un periodo específico\\
\textbf{cuando} aplico un filtro de fechas (por ejemplo, una semana o mes)\\
\textbf{entonces} el sistema muestra solo las rutas realizadas en ese periodo de tiempo seleccionado.\\[0.2em]

\textbf{Escenario 3: Visualización de detalles del recorrido}\\
\textbf{Dado que} estoy revisando el historial de una ruta específica\\
\textbf{cuando} selecciono una ruta en particular\\
\textbf{entonces} el sistema muestra detalles del recorrido, incluyendo la hora de inicio, hora de finalización, puntos de recogida y entrega, y cualquier incidencia registrada (retrasos, desvíos, etc.).\\[0.2em]
\end{tabular}
& EP05 \\

\hline
FS02 & Log de Eventos Recientes & \textbf{Como} tutor legal, \textbf{quiero} ver un log de eventos (abordaje, llegada, alertas) de los últimos X días, \textbf{para} detectar posibles problemas recurrentes y garantizar el bienestar de mi hijo durante el trayecto. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Consulta de log de eventos recientes}\\
\textbf{Dado que} he iniciado sesión en la aplicación móvil\\
\textbf{cuando} accedo a la sección de log de eventos recientes\\
\textbf{entonces} el sistema muestra un listado de los eventos de los últimos X días, con detalles como la hora, tipo de evento (abordaje, llegada, alertas) y cualquier incidencia registrada.\\[0.2em]

\textbf{Escenario 2: Filtrado por tipo de evento}\\
\textbf{Dado que} quiero revisar eventos de un tipo específico\\
\textbf{cuando} aplico un filtro de tipo de evento (por ejemplo, solo abordajes o solo alertas)\\
\textbf{entonces} el sistema muestra solo los eventos correspondientes al tipo seleccionado.\\[0.2em]

\textbf{Escenario 3: Filtrado por rango de fechas}\\
\textbf{Dado que} quiero revisar los eventos dentro de un rango de fechas específico\\
\textbf{cuando} aplico un filtro de fechas (por ejemplo, los últimos 3 días)\\
\textbf{entonces} el sistema muestra los eventos ocurridos dentro de ese periodo de tiempo seleccionado.\\[0.2em]
\end{tabular}
& EP05 \\

\hline
FS03 & Exportación de Historial & \textbf{Como} tutor legal, \textbf{quiero} exportar o compartir el historial de rutas y eventos (en formato PDF/CSV), \textbf{para} presentarlo al colegio o a la empresa de transporte si surge alguna incidencia y tener un registro formal. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Exportación de historial a PDF}\\
\textbf{Dado que} he accedido al historial de rutas y eventos\\
\textbf{cuando} selecciono la opción para exportar el historial a PDF\\
\textbf{entonces} el sistema genera un archivo PDF con los detalles del historial de rutas y eventos, y lo pone disponible para descargar o compartir.\\[0.2em]

\textbf{Escenario 2: Exportación de historial a CSV}\\
\textbf{Dado que} he accedido al historial de rutas y eventos\\
\textbf{cuando} selecciono la opción para exportar el historial a CSV\\
\textbf{entonces} el sistema genera un archivo CSV con los detalles del historial de rutas y eventos, y lo pone disponible para descargar o compartir.\\[0.2em]

\textbf{Escenario 3: Error al exportar historial}\\
\textbf{Dado que} intento exportar el historial a PDF o CSV\\
\textbf{cuando} ocurre un error durante la exportación\\
\textbf{entonces} el sistema muestra un mensaje de error indicando que la exportación no se pudo completar y sugiere intentar nuevamente.\\[0.2em]
\end{tabular}
& EP05 \\

\hline
GS01 & Selección de Notificaciones por Hijo & \textbf{Como} tutor legal, \textbf{quiero} seleccionar para cuál de mis hijos quiero recibir notificaciones, \textbf{para} evitar recibir alertas innecesarias y personalizar mi experiencia en la aplicación móvil. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Visualización de lista de hijos}\\
\textbf{Dado que} tengo varios hijos registrados en mi perfil\\
\textbf{cuando} accedo a la sección de preferencias y notificaciones\\
\textbf{entonces} el sistema muestra una lista de todos mis hijos con opciones para activar o desactivar notificaciones individualmente.\\[0.2em]

\textbf{Escenario 2: Selección y deselección de notificaciones}\\
\textbf{Dado que} deseo personalizar las notificaciones recibidas\\
\textbf{cuando} marco o desmarco la opción de notificaciones para cada hijo en la lista\\
\textbf{entonces} el sistema guarda automáticamente mi selección y actualiza mis preferencias para que reciba alertas sólo para los hijos seleccionados.\\[0.2em]

\textbf{Escenario 3: Confirmación de actualización de preferencias}\\
\textbf{Dado que} he realizado cambios en la selección de notificaciones\\
\textbf{cuando} finalizo el proceso de configuración\\
\textbf{entonces} el sistema muestra un mensaje de confirmación (“Preferencias actualizadas con éxito”) y las futuras notificaciones se envían conforme a mis ajustes.
\end{tabular}
& EP06 \\

\hline
GS02 & Definición de Horarios de Silencio & \textbf{Como} tutor legal, \textbf{quiero} definir horarios de silencio (modo "No molestar"), \textbf{para} no recibir notificaciones fuera del rango permitido y evitar interrupciones en mis momentos de descanso o concentración. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Configuración de horario de silencio}\\
\textbf{Dado que} accedo a la sección de preferencias de notificaciones en la aplicación móvil\\
\textbf{cuando} selecciono la opción de "Horarios de Silencio" y establezco la franja horaria deseada\\
\textbf{entonces} el sistema guarda la configuración y desactiva automáticamente las notificaciones durante ese intervalo.\\[0.2em]

\textbf{Escenario 2: Confirmación de activación del modo silencio}\\
\textbf{Dado que} he configurado un horario de silencio\\
\textbf{cuando} la hora actual se encuentra dentro de la franja de silencio definida\\
\textbf{entonces} la aplicación deja de enviar notificaciones y muestra un indicador que confirma que el modo "No molestar" está activado.\\[0.2em]

\textbf{Escenario 3: Desactivación automática fuera del horario de silencio}\\
\textbf{Dado que} el horario de silencio ha finalizado\\
\textbf{cuando} el sistema detecta que la hora actual supera el rango configurado\\
\textbf{entonces} el modo "No molestar" se desactiva automáticamente y las notificaciones vuelven a enviarse normalmente.\\[0.2em]
\end{tabular}
& EP06 \\

\hline
GS03 & Personalización de Idioma y Tema & \textbf{Como} tutor legal, \textbf{quiero} cambiar el idioma y el tema (claro/oscuro) de la aplicación, \textbf{para} adaptar la interfaz a mis preferencias personales y mejorar mi experiencia de uso. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Cambio de idioma}\\
\textbf{Dado que} estoy en la pantalla de configuración de la aplicación\\
\textbf{cuando} selecciono el idioma de preferencia en el menú desplegable (ej. español, inglés, etc.)\\
\textbf{entonces} el idioma de la aplicación se actualiza inmediatamente y todas las pantallas se muestran en el nuevo idioma seleccionado.\\[0.2em]

\textbf{Escenario 2: Cambio de tema}\\
\textbf{Dado que} estoy en la pantalla de configuración de la aplicación\\
\textbf{cuando} selecciono el tema (claro u oscuro) que prefiero\\
\textbf{entonces} la interfaz de la aplicación cambia al tema seleccionado y se ajusta visualmente a la preferencia.\\[0.2em]

\textbf{Escenario 3: Confirmación de cambios}\\
\textbf{Dado que} he cambiado el idioma y el tema\\
\textbf{cuando} guardo los cambios\\
\textbf{entonces} el sistema muestra un mensaje de confirmación indicando “Idioma y tema actualizados con éxito” y la interfaz se adapta de acuerdo a las preferencias seleccionadas.\\[0.2em]
\end{tabular}
& EP06 \\

\hline
HS01 & Comunicación Directa con el Conductor & \textbf{Como} tutor legal, \textbf{quiero} enviar un mensaje o realizar una llamada al conductor desde la aplicación, \textbf{para} resolver dudas o coordinar imprevistos durante el trayecto. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Enviar mensaje al conductor}\\
\textbf{Dado que} estoy en la pantalla de seguimiento de mi hijo\\
\textbf{cuando} selecciono la opción de "Comunicación con el conductor" y elijo "Enviar mensaje"\\
\textbf{entonces} se abre una ventana de chat donde puedo escribir mi mensaje y enviarlo directamente al conductor.\\[0.2em]

\textbf{Escenario 2: Realizar llamada al conductor}\\
\textbf{Dado que} estoy en la pantalla de seguimiento de mi hijo\\
\textbf{cuando} selecciono la opción de "Comunicación con el conductor" y elijo "Llamar al conductor"\\
\textbf{entonces} se realiza la llamada telefónica al conductor a través de la aplicación, utilizando el número de contacto del conductor.\\[0.2em]

\textbf{Escenario 3: Confirmación de mensaje enviado}\\
\textbf{Dado que} he enviado un mensaje al conductor\\
\textbf{cuando} el mensaje es entregado\\
\textbf{entonces} la aplicación muestra una notificación de confirmación indicando “Mensaje enviado con éxito al conductor” en la pantalla de chat.\\[0.2em]
\end{tabular}
& EP07 \\

\hline
HS02 & Reporte de Incidencias con Evidencia & \textbf{Como} tutor legal, \textbf{quiero} reportar una incidencia (retraso, mal funcionamiento del sensor, etc.) con foto o video, \textbf{para} que el colegio pueda tomar acciones basadas en la evidencia proporcionada. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Reporte de incidencia con foto}\\
\textbf{Dado que} estoy en la pantalla de seguimiento de mi hijo y observo una incidencia (como un retraso o mal funcionamiento del sensor)\\
\textbf{cuando} selecciono la opción "Reportar incidencia" y elijo "Adjuntar foto"\\
\textbf{entonces} la aplicación me permite tomar una foto y enviarla junto con una descripción del problema, generando un reporte para el colegio.\\[0.2em]

\textbf{Escenario 2: Reporte de incidencia con video}\\
\textbf{Dado que} estoy en la pantalla de seguimiento de mi hijo y observo una incidencia\\
\textbf{cuando} selecciono la opción "Reportar incidencia" y elijo "Adjuntar video"\\
\textbf{entonces} la aplicación me permite grabar un video y enviarlo junto con una descripción del problema, generando un reporte para el colegio.\\[0.2em]

\textbf{Escenario 3: Confirmación de reporte enviado}\\
\textbf{Dado que} he enviado un reporte de incidencia con foto o video\\
\textbf{cuando} el reporte es enviado correctamente\\
\textbf{entonces} la aplicación muestra una notificación de confirmación indicando “Incidencia reportada con éxito” en la pantalla de reporte.\\[0.2em]
\end{tabular}
& EP07 \\

\hline
HS03 & Acceso a Ayuda y Preguntas Frecuentes & \textbf{Como} tutor legal, \textbf{quiero} acceder a una sección de ayuda y preguntas frecuentes, \textbf{para} resolver rápidamente mis dudas sobre el funcionamiento de la app. &
\begin{tabular}[t]{@{}p{5cm}@{}}
\textbf{Escenario 1: Acceso a la sección de ayuda}\\
\textbf{Dado que} estoy en la pantalla principal de la aplicación\\
\textbf{cuando} selecciono la opción de "Ayuda" en el menú principal\\
\textbf{entonces} la aplicación me redirige a la sección de ayuda y preguntas frecuentes, donde puedo ver una lista de preguntas comunes y sus respuestas.\\[0.2em]

\textbf{Escenario 2: Búsqueda de una pregunta específica}\\
\textbf{Dado que} estoy en la sección de preguntas frecuentes\\
\textbf{cuando} utilizo la barra de búsqueda para escribir una palabra clave relacionada con mi duda\\
\textbf{entonces} la aplicación muestra una lista de preguntas relacionadas con la búsqueda, para que pueda encontrar rápidamente la respuesta.\\[0.2em]

\textbf{Escenario 3: Acceso a información detallada de una pregunta}\\
\textbf{Dado que} estoy en la sección de preguntas frecuentes\\
\textbf{cuando} selecciono una pregunta de la lista\\
\textbf{entonces} la aplicación muestra una respuesta detallada con información adicional sobre cómo resolver el problema o gestionar la función relacionada.\\[0.2em]
\end{tabular}
& EP07 \\

\hline

\end{longtable}

\newpage

## Product Backlog.

Una de las técnicas más utilizadas para estimar el esfuerzo necesario para completar cada tarea es la escala de Fibonacci, la cual permite asignar puntos de historia de manera proporcional a la complejidad y tiempo requerido. 

\vspace{1em}

\begin{quote}
Como señala Smith (2020), esta escala no lineal facilita la identificación de tareas que requieren un mayor esfuerzo, lo que resulta en una planificación más precisa y eficiente.
\end{quote}

\vspace{1em}

A continuación, se presentan la tablas de nuestros *Product Backlog* para cada segmento objetivo, demostrando cómo se alinean nuestros recursos con las necesidades más urgentes de nuestros usuarios.

**Administrador educativo:**

\begin{longtable}{|c|p{4cm}|p{7cm}|c|}
\hline
\multicolumn{1}{|c|}{\textbf{ID}} & \multicolumn{1}{c|}{\textbf{Título}} & \multicolumn{1}{c|}{\textbf{Descripción}} & \multicolumn{1}{c|}{\textbf{Story Points}} \\
\hline

DS05 & Control de cambios de última hora en la asignación de conductores y estudiantes & \textbf{Como} administrador educativo, \textbf{quiero} realizar cambios de última hora en la asignación de conductores y estudiantes, \textbf{para} asegurar la continuidad del servicio ante imprevistos sin afectar el resto de la programación. & 13 \\
\hline
ES01 & Monitoreo en tiempo real de posición y velocidad de vehículos & \textbf{Como} administrador educativo, \textbf{quiero} conocer la posición y velocidad en tiempo real de cada vehículo, \textbf{para} monitorear sus rutas y detectar posibles retrasos o desvíos oportunamente. & 13 \\
\hline
ES05 & Verificación de rutas alternativas en caso de desvíos & \textbf{Como} administrador educativo, \textbf{quiero} verificar y gestionar rutas alternativas en tiempo real cuando una unidad se desvía de su ruta prevista, \textbf{para} garantizar que los estudiantes lleguen a su destino de manera segura y a tiempo frente a imprevistos. & 13 \\
\hline
HS01 & Dashboard con KPIs clave & \textbf{Como} administrador educativo, \textbf{quiero} acceder a un dashboard que muestre KPIs clave (número de rutas activas, incidencias, temperatura media, etc.), \textbf{para} monitorear la operación del transporte escolar de un vistazo y tomar decisiones basadas en datos en tiempo real. & 13 \\
\hline

CS02 & Definición y mapeo de zonas & \textbf{Como} administrador educativo, \textbf{quiero} definir y mapear zonas de recogida y entrega en un mapa interactivo, \textbf{para} optimizar la cobertura y asignar rutas con precisión. & 8 \\
\hline
CS03 & Visualización geoespacial de zonas y rutas & \textbf{Como} administrador educativo, \textbf{quiero} visualizar todas las zonas de recogida y entrega y sus rutas asociadas en un mapa interactivo, \textbf{para} detectar posibles solapamientos, huecos de cobertura o áreas no cubiertas. & 8 \\
\hline
DS02 & Registro y asignación de pulseras RFID a estudiantes & \textbf{Como} administrador educativo, \textbf{quiero} registrar a los estudiantes en el sistema y asignarles pulseras RFID con un identificador único, \textbf{para} vincular cada niño con su dispositivo de control y gestionar su transporte de manera más eficiente. & 8 \\
\hline
DS03 & Asignación de conductores y estudiantes a rutas específicas & \textbf{Como} administrador educativo, \textbf{quiero} asignar conductores y estudiantes a rutas específicas en el sistema, \textbf{para} asegurar que cada unidad opere con el personal y pasajeros correctos y optimizar la seguridad del transporte escolar. & 8 \\
\hline
ES02 & Monitoreo de temperatura interna de los vehículos & \textbf{Como} administrador educativo, \textbf{quiero} monitorear remotamente la temperatura interna de los vehículos, \textbf{para} asegurarme de que las condiciones sean seguras para los pasajeros. & 8 \\
\hline
ES03 & Seguimiento de unidades de transporte para verificar salida y llegada & \textbf{Como} administrador educativo, \textbf{quiero} visualizar en tiempo real qué unidades ya han partido para recoger a los estudiantes y qué unidades ya han llegado al centro educativo, \textbf{para} hacer un seguimiento eficiente del estado de las rutas y asegurarme de que todos los estudiantes han sido recogidos o entregados. & 8 \\
\hline
ES04 & Monitoreo de estudiantes que no abordaron la unidad & \textbf{Como} administrador educativo, \textbf{quiero} hacer un seguimiento de qué estudiantes no abordaron la unidad, \textbf{para} tomar acciones inmediatas y asegurarme de que todos los estudiantes estén siendo transportados de forma segura. & 8 \\
\hline
ES06 & Visualización de unidades en ruta para gestionar desviaciones o retrasos & \textbf{Como} administrador educativo, \textbf{quiero} visualizar en tiempo real todas las unidades en ruta, \textbf{para} detectar rápidamente desviaciones o retrasos y tomar decisiones oportunas que aseguren el cumplimiento de los horarios y la seguridad de los estudiantes. & 8 \\
\hline
GS01 & Reporte de tiempos de ruta y cumplimiento & \textbf{Como} administrador educativo, \textbf{quiero} generar reportes de tiempos de ruta y cumplimiento, \textbf{para} evaluar el desempeño de la flota y apoyar la toma de decisiones basadas en datos operativos. & 8 \\
\hline
GS04 & Reporte de incidencias críticas & \textbf{Como} administrador del sistema, \textbf{quiero} generar reportes de incidencias críticas, \textbf{para} consolidar y analizar eventos como alertas de temperatura, desviaciones de ruta o fallos de equipo, con el fin de identificar patrones recurrentes y focalizar acciones de mejora continua en la gestión de transporte escolar. & 8 \\
\hline
GS05 & Programación de envíos automáticos de reportes & \textbf{Como} administrador del sistema, \textbf{quiero} programar envíos automáticos de reportes, \textbf{para} automatizar la distribución periódica de reportes (diarios, semanales o mensuales) a los responsables, garantizando que la información llegue a tiempo sin necesidad de intervención manual. & 8 \\
\hline
HS02 & Gestión de roles y permisos & \textbf{Como} administrador educativo, \textbf{quiero} gestionar los roles y permisos de los usuarios (coordinadores, supervisores, etc.), \textbf{para} delegar responsabilidades con seguridad y asegurarme de que cada usuario solo tenga acceso a la información y funciones necesarias para su rol. & 8 \\
\hline
HS04 & Registro de auditoría de actividad & \textbf{Como} administrador educativo, \textbf{quiero} llevar un registro de auditoría de todas las acciones realizadas por los administradores y supervisores (como la creación/edición de usuarios, cambios en rutas, ajustes de parámetros), \textbf{para} garantizar la trazabilidad y el cumplimiento de normativas internas. & 8 \\
\hline
HS06 & Personalización del dashboard & \textbf{Como} administrador educativo, \textbf{quiero} personalizar el dashboard seleccionando qué widgets visualizar, su orden y frecuencia de actualización, \textbf{para} adaptar la interfaz a las prioridades específicas de mi institución y mejorar la usabilidad del sistema. & 8 \\
\hline

CS01 & Registro y edición de vehículos & \textbf{Como} administrador educativo, \textbf{quiero} registrar y editar los datos de cada vehículo (placa, modelo, capacidad y estado operativo), \textbf{para} mantener un catálogo actualizado y fiable de la flota. & 5 \\
\hline
CS04 & Asignación de vehículos a rutas específicas & \textbf{Como} administrador educativo, \textbf{quiero} asignar vehículos específicos a rutas definidas, \textbf{para} tener un control operacional directo sobre qué unidad se utiliza en cada recorrido y facilitar la trazabilidad en caso de incidentes. & 5 \\
\hline
DS01 & Registro y actualización de conductores & \textbf{Como} administrador educativo, \textbf{quiero} registrar nuevos conductores y actualizar sus datos de contacto, número de licencia y estado operativo, \textbf{para} mantener un personal actualizado y garantizar la correcta asignación de rutas. & 5 \\
\hline
DS04 & Verificación de disponibilidad de conductores & \textbf{Como} administrador educativo, \textbf{quiero} verificar la disponibilidad de los conductores antes de asignarlos a una ruta, \textbf{para} evitar conflictos de horario y asegurar una gestión eficiente del personal y la flota. & 5 \\
\hline
FS01 & Alerta de temperatura fuera de rango & \textbf{Como} administrador educativo, \textbf{quiero} recibir alertas en tiempo real cuando la temperatura interna de un vehículo se salga de los parámetros establecidos, \textbf{para} tomar medidas inmediatas que garanticen la seguridad y el confort de los estudiantes durante el transporte. & 5 \\
\hline
FS02 & Alerta de retrasos o desviaciones en las rutas & \textbf{Como} administrador educativo, \textbf{quiero} recibir alertas inmediatas cuando una unidad de transporte experimente retrasos o se desvíe de la ruta establecida, \textbf{para} poder coordinar con el conductor y tomar decisiones rápidas que minimicen el impacto en el servicio y garanticen la llegada segura y oportuna de los estudiantes. & 5 \\
\hline
FS03 & Alerta de estudiantes no abordando la unidad & \textbf{Como} administrador educativo, \textbf{quiero} recibir alertas en tiempo real cuando un estudiante asignado a una ruta no aborde la unidad, \textbf{para} poder tomar medidas inmediatas como contactar al conductor o a los padres, y así garantizar la seguridad de todos los estudiantes. & 5 \\
\hline
FS04 & Notificación automática ante cambios de ruta o posibles retrasos & \textbf{Como} administrador educativo, \textbf{quiero} recibir notificaciones automáticas cuando un vehículo experimente cambios de ruta o posibles retrasos, \textbf{para} poder gestionar de manera proactiva las rutas y tomar decisiones para minimizar el impacto en los horarios de transporte. & 5 \\
\hline
FS05 & Alerta por fallo de equipo en el vehículo (GPS, RFID, sensores, etc.) & \textbf{Como} administrador educativo, \textbf{quiero} recibir una alerta inmediata en caso de fallo de equipos en los vehículos, como el GPS, RFID o sensores, \textbf{para} poder tomar medidas rápidas y garantizar que el control de las rutas y la seguridad de los estudiantes no se vean comprometidos. & 5 \\
\hline
GS02 & Estadísticas de abordaje por estudiante & \textbf{Como} administrador educativo, \textbf{quiero} obtener estadísticas de abordaje por estudiante, \textbf{para} detectar patrones de retraso o ausencias y tomar acciones preventivas que mejoren la eficiencia del transporte escolar. & 5 \\
\hline
GS03 & Exportación de datos históricos en Excel/PDF & \textbf{Como} responsable de calidad, \textbf{quiero} exportar datos históricos en formatos Excel o PDF, \textbf{para} presentarlos en auditorías o juntas directivas y facilitar la toma de decisiones estratégicas basadas en datos históricos. & 5 \\
\hline
GS06 & Filtrado y segmentación de datos históricos & \textbf{Como} administrador del sistema, \textbf{quiero} filtrar y segmentar datos históricos por ruta, vehículo, conductor o rango de fechas, \textbf{para} optimizar el análisis detallado y la preparación de informes personalizados para auditorías o reuniones de gestión. & 5 \\
\hline
HS03 & Configuración de parámetros globales & \textbf{Como} administrador educativo, \textbf{quiero} configurar parámetros globales (como los umbrales de temperatura, la frecuencia de reporte GPS, etc.), \textbf{para} adaptar el sistema a las políticas internas de la institución y asegurar el funcionamiento adecuado de la plataforma. & 5 \\
\hline
HS05 & Configuración de notificaciones y alertas & \textbf{Como} administrador educativo, \textbf{quiero} configurar qué tipos de notificaciones y alertas deseo recibir, por qué canal (correo electrónico, SMS, notificación push) y con qué umbrales, \textbf{para} adaptar la comunicación del sistema a los procesos internos de la institución. & 5 \\
\hline

CS05 & Desactivación temporal de unidades fuera de servicio & \textbf{Como} administrador educativo, \textbf{quiero} desactivar temporalmente vehículos fuera de servicio, \textbf{para} evitar su asignación errónea a rutas mientras se mantiene su información en el sistema para futuras referencias y reactivación. & 3 \\
\hline
FS06 & Notificación cuando la unidad ha completado el recorrido & \textbf{Como} administrador educativo, \textbf{quiero} recibir una notificación cuando una unidad haya completado su recorrido (tanto la ruta hacia el colegio como el retorno a casa), \textbf{para} poder gestionar eficientemente la programación de las unidades, evitando retrasos y asegurando que las unidades estén disponibles para nuevas asignaciones. & 3 \\
\hline
US01 & Registro de cuenta institucional & \textbf{Como} administrador educativo, \textbf{quiero} crear una cuenta institucional proporcionando mi nombre completo, correo institucional y contraseña, \textbf{para} acceder de manera segura a la plataforma web. & 3 \\
\hline
US05 & Recuperación de contraseña & \textbf{Como} administrador educativo, \textbf{quiero} poder recuperar mi contraseña a través de un correo electrónico, \textbf{para} poder acceder nuevamente a mi cuenta si la olvido. & 3 \\
\hline
US06 & Gestión de perfil administrativo & \textbf{Como} administrador educativo, \textbf{quiero} poder editar y actualizar mi perfil (como datos de contacto, cargo, etc.), \textbf{para} mantener mi información actualizada en la plataforma. & 3 \\
\hline

US02 & Confirmación de cuenta del administrador & \textbf{Como} administrador educativo, \textbf{quiero} confirmar mi cuenta a través de un enlace enviado a mi correo institucional, \textbf{para} verificar mi identidad y activar mi acceso al sistema. & 2 \\
\hline
US03 & Verificación de cuenta por parte del sistema & \textbf{Como} administrador educativo, \textbf{quiero} que el sistema verifique automáticamente la validez de mi cuenta, \textbf{para} asegurarme de que mi información esté correctamente registrada y no haya problemas para acceder a la plataforma. & 2 \\
\hline
US04 & Inicio de sesión del administrador educativo & \textbf{Como} administrador educativo, \textbf{quiero} iniciar sesión de manera segura en la plataforma utilizando mis credenciales (correo electrónico y contraseña), \textbf{para} acceder a las funcionalidades de administración del sistema de transporte escolar de manera eficiente. & 2 \\
\hline

US07 & Cierre de sesión segura & \textbf{Como} administrador educativo, \textbf{quiero} cerrar sesión de manera segura en la plataforma, \textbf{para} garantizar que mi cuenta esté protegida y no quede abierta a accesos no autorizados. & 1 \\
\hline

\end{longtable}

\newpage

**Tutor legal o familiar**


\begin{longtable}{|c|p{4cm}|p{7cm}|c|}
\hline
\multicolumn{1}{|c|}{\textbf{ID}} & \multicolumn{1}{c|}{\textbf{Título}} & \multicolumn{1}{c|}{\textbf{Descripción}} & \multicolumn{1}{c|}{\textbf{Story Points}} \\
\hline

ES01 & Supervisión en Tiempo Real (Ida) & \textbf{Como} tutor legal, \textbf{quiero} ver en tiempo real el video de la cámara instalada en la unidad durante el trayecto de ida, \textbf{para} supervisar las condiciones del viaje y asegurarme de que mi hijo se encuentre en un ambiente seguro. & 13 \\
\hline
ES02 & Supervisión en Tiempo Real (Regreso) & \textbf{Como} tutor legal, \textbf{quiero} ver en tiempo real el video de la cámara instalada en la unidad durante el trayecto de regreso, \textbf{para} asegurarme del bienestar de mi hijo y supervisar las condiciones del viaje de regreso a casa. & 13 \\
\hline

CS01 & Ubicación en Vivo del Vehículo & \textbf{Como} tutor legal, \textbf{quiero} ver la posición en vivo del vehículo que transporta a mi hijo, \textbf{para} estimar su hora de llegada y estar preparado ante cualquier eventualidad. & 8 \\
\hline
DS03 & Alerta por Desvío o Retraso & \textbf{Como} tutor legal, \textbf{quiero} recibir una alerta si el vehículo se desvía de la ruta o sufre un retraso significativo, \textbf{para} estar informado de cualquier incidencia que pueda afectar la seguridad o puntualidad del trayecto de mi hijo. & 8 \\
\hline
DS04 & Alerta de Temperatura Insegura & \textbf{Como} tutor legal, \textbf{quiero} recibir una alerta si la temperatura interna del vehículo sale de los rangos seguros, \textbf{para} asegurarme del confort y la seguridad de mi hijo durante el trayecto. & 8 \\
\hline
HS01 & Comunicación Directa con el Conductor & \textbf{Como} tutor legal, \textbf{quiero} enviar un mensaje o realizar una llamada al conductor desde la aplicación, \textbf{para} resolver dudas o coordinar imprevistos durante el trayecto. & 8 \\
\hline
HS02 & Reporte de Incidencias con Evidencia & \textbf{Como} tutor legal, \textbf{quiero} reportar una incidencia (retraso, mal funcionamiento del sensor, etc.) con foto o video, \textbf{para} que el colegio pueda tomar acciones basadas en la evidencia proporcionada. & 8 \\
\hline

US01 & Registro e Inicio de Sesión & \textbf{Como} tutor legal, \textbf{quiero} registrarme e iniciar sesión con mi cuenta, \textbf{para} acceder de forma segura a la aplicación móvil y administrar el seguimiento del transporte de mi hijo. & 5 \\
\hline
US02 & Recuperación de Contraseña & \textbf{Como} tutor legal, \textbf{quiero} recuperar mi contraseña vía correo o SMS, \textbf{para} restablecer el acceso en caso de olvido y seguir utilizando la aplicación sin inconvenientes. & 5 \\
\hline
CS02 & Consulta de Ruta Planificada & \textbf{Como} tutor legal, \textbf{quiero} consultar la ruta planificada y el progreso del recorrido, \textbf{para} saber por dónde va el vehículo y cuánto falta para que llegue a su destino. & 5 \\
\hline
CS03 & Estimación de Tiempo Restante & \textbf{Como} tutor legal, \textbf{quiero} recibir la estimación de tiempo restante hasta el punto de recogida o entrega de mi hijo, \textbf{para} poder organizarme mejor y estar preparado a tiempo. & 5 \\
\hline
FS03 & Exportación de Historial & \textbf{Como} tutor legal, \textbf{quiero} exportar o compartir el historial de rutas y eventos (en formato PDF/CSV), \textbf{para} presentarlo al colegio o a la empresa de transporte si surge alguna incidencia y tener un registro formal. & 5 \\
\hline

US03 & Edición de Perfil & \textbf{Como} tutor legal, \textbf{quiero} editar mi perfil (datos de contacto) y la información de mis hijos (grado, pulsera RFID), \textbf{para} mantener toda la información actualizada y garantizar una correcta gestión del transporte. & 3 \\
\hline
US04 & Gestión de Dispositivos de Notificación & \textbf{Como} tutor legal, \textbf{quiero} gestionar mis dispositivos de notificación (push, email, SMS), \textbf{para} elegir cómo y cuándo recibir alertas sobre el transporte de mi hijo. & 3 \\
\hline
DS01 & Notificación de Abordaje & \textbf{Como} tutor legal, \textbf{quiero} recibir una notificación cuando mi hijo aborde la unidad, \textbf{para} saber que ha subido correctamente al vehículo y estar tranquilo durante el viaje. & 3 \\
\hline
DS02 & Notificación de Llegada & \textbf{Como} tutor legal, \textbf{quiero} recibir una notificación cuando mi hijo llegue al colegio o a casa, \textbf{para} confirmar su arribo seguro y tener tranquilidad sobre el cumplimiento del recorrido. & 3 \\
\hline
FS01 & Historial de Rutas Diarias & \textbf{Como} tutor legal, \textbf{quiero} consultar el historial de rutas diarias de mi hijo, \textbf{para} revisar su puntualidad y los recorridos anteriores, asegurándome de que todo transcurra como estaba planificado. & 3 \\
\hline
FS02 & Log de Eventos Recientes & \textbf{Como} tutor legal, \textbf{quiero} ver un log de eventos (abordaje, llegada, alertas) de los últimos X días, \textbf{para} detectar posibles problemas recurrentes y garantizar el bienestar de mi hijo durante el trayecto. & 3 \\
\hline

GS01 & Selección de Notificaciones por Hijo & \textbf{Como} tutor legal, \textbf{quiero} seleccionar para cuál de mis hijos quiero recibir notificaciones, \textbf{para} evitar recibir alertas innecesarias y personalizar mi experiencia en la aplicación móvil. & 2 \\
\hline
GS02 & Definición de Horarios de Silencio & \textbf{Como} tutor legal, \textbf{quiero} definir horarios de silencio (modo "No molestar"), \textbf{para} no recibir notificaciones fuera del rango permitido y evitar interrupciones en mis momentos de descanso o concentración. & 2 \\
\hline
GS03 & Personalización de Idioma y Tema & \textbf{Como} tutor legal, \textbf{quiero} cambiar el idioma y el tema (claro/oscuro) de la aplicación, \textbf{para} adaptar l\a interfaz a mis preferencias personales y mejorar mi experiencia de uso. & 2 \\
\hline
HS03 & Acceso a Ayuda y Preguntas Frecuentes & \textbf{Como} tutor legal, \textbf{quiero} acceder a una sección de ayuda y preguntas frecuentes, \textbf{para} resolver rápidamente mis dudas sobre el funcionamiento de la app. & 2 \\
\hline

\end{longtable}

\newpage

## Impact Mapping.

**Segmento Objetivo 1**

![Artefacto creado en UXPressia](src/img/cap3/ImpactMapping1.png)

**Segmento Objetivo 2**

![Artefacto creado en UXPressia](src/img/cap3/ImpactMapping2.png)

\newpage

# Capítulo IV: Product Design

El diseño del producto no solo refleja el propósito funcional de RutaKids, sino también sus valores fundamentales: seguridad, transparencia y eficiencia. 
En esta sección se detallan los principios visuales, patrones de interacción y estilos adoptados para asegurar una experiencia homogénea y accesible en todas las plataformas: web, móvil e IoT. Cada elemento de la interfaz ha sido concebido con base en las necesidades reales de nuestros usuarios, identificadas a través de entrevistas, mapas de empatía y journeys. El enfoque se centra en resolver problemas con soluciones visuales limpias, directas y adaptadas al entorno educativo.

\newpage

## Style Guidelines.


![Artefacto creado en Figma](src/img/cap4/cover.png)

Las directrices de estilo cumplen un papel clave en garantizar una identidad visual coherente en todos los productos de RutaKids. Estas pautas nos permiten mantener consistencia en los elementos gráficos, facilitando una experiencia clara y uniforme para los usuarios. A continuación, se detallan las guías generales y específicas aplicadas en cada plataforma.

### General Style Guidelines.

En el diseño de productos digitales, la estética no es solo una cuestión de apariencia, sino una herramienta estratégica para facilitar la interacción del usuario. Un lenguaje visual bien definido, que incluya criterios claros sobre identidad de marca, esquema de colores, tipografía y tono comunicacional, contribuye a que la experiencia sea coherente, fluida y significativa.

\vspace{1em}

\begin{quote}
Rijgersberg (2025) argumenta que reducir la complejidad visual y estructurar la información de manera accesible disminuye la carga cognitiva, permitiendo que los usuarios avancen con claridad hacia sus objetivos. Bajo esta lógica, la simplicidad no implica ausencia de diseño, sino decisiones intencionales orientadas a la funcionalidad.
\end{quote}

\vspace{1em}

Por eso, contar con principios de diseño sólidos no solo mejora la accesibilidad y la eficiencia del producto, sino que también habilita su evolución en distintos contextos y dispositivos. Así, se construye una identidad visual adaptable, al servicio tanto de la experiencia del usuario como de la narrativa de la organización.

\newpage

**Branding:**

*Rutakids* es una solución tecnológica pensada para brindar seguridad y control en el transporte escolar. Su identidad visual refleja confianza, cercanía y modernidad, valores clave para padres y colegios. La plataforma busca simplificar la experiencia de seguimiento escolar a través de una interfaz clara, accesible y conectada en tiempo real.
Cada elemento del branding (colores, tipografía y estilo visual) está diseñado para reforzar la misión de *RutaKids*: ofrecer tranquilidad a las familias y eficiencia a las instituciones, con una experiencia intuitiva y coherente en todos sus canales digitales.


**Logotipo:**

El logotipo de *RutaKids* fue diseñado para representar visualmente los valores fundamentales de la solución: movimiento, seguridad y tecnología accesible. Su símbolo principal es una rueda estilizada en movimiento, lo cual hace alusión directa al concepto de transporte escolar eficiente y monitoreado en tiempo real.
La elección del color azul vibrante busca transmitir confianza, profesionalismo y tranquilidad, mientras que las formas redondeadas del logotipo refuerzan la cercanía y la facilidad de uso que caracterizan a la plataforma. Además, se han definido variantes del logotipo para asegurar su correcta adaptación en diferentes fondos y contextos, sin comprometer la legibilidad ni la identidad visual del producto.

![Artefacto creado en Figma](src/img/cap4/LogoStyle.png)


\newpage

**Iconografía de la Aplicación**

La iconografía de *RutaKids* se basa en el uso del imagotipo de la marca (una rueda estilizada en movimiento) como símbolo principal en su versión para dispositivos móviles. Este elemento mantiene la coherencia gráfica de la marca al tiempo que asegura versatilidad y reconocimiento en pantallas reducidas. Además, para garantizar su legibilidad y funcionalidad, se desarrollaron distintas variantes del ícono, adaptables a diferentes fondos y contextos de uso. Su forma simplificada y su alto contraste permiten una fácil identificación desde la pantalla de inicio de cualquier dispositivo, reforzando la presencia visual de *RutaKids* dentro de su ecosistema digital.

![Artefacto creado en Figma](src/img/cap4/Icon_App.png)


\newpage

**Colores**

La paleta de colores de *RutaKids* está estructurada en dos grupos principales: los colores utilizados en la interfaz de usuario y aquellos aplicados en las variantes del logotipo e iconos. Esta clasificación permite mantener una coherencia visual sólida, adaptando el uso del color según su función en la experiencia del usuario y en la identidad de marca.

- **Colores Principales (Interfaz de la Aplicación)**

  Estos colores se aplican en la landing page, la aplicación web y la app móvil. Su selección busca optimizar la legibilidad, facilitar la navegación y establecer jerarquías visuales claras.
    
  - **Azul (#2979FF):** Color principal de acento, utilizado en botones, enlaces, íconos activos y llamadas a la acción. Simboliza tecnología, dinamismo y confiabilidad, atributos clave para una plataforma tecnológica dirigida al entorno infantil y familiar. Su intensidad favorece la visibilidad y guía la atención del usuario hacia las zonas de interacción.
  
  - **Blanco (#FFFFFF):** Funciona como fondo predominante en la interfaz. Su neutralidad permite maximizar la claridad, mejorar la percepción del contenido y generar una sensación de amplitud visual. Es fundamental para evitar la saturación cromática y facilitar la lectura en distintos dispositivos.
  
  - **Gris (#93868A):** Aplicado en textos secundarios, descripciones, etiquetas y componentes del dashboard. Este tono contribuye a una organización jerárquica de la información, diferenciando elementos sin provocar distracción visual. Su uso estratégico mejora la legibilidad y evita el contraste excesivo.
  
  - **Negro (#000000):** Utilizado en títulos, encabezados y textos primarios. Su alto contraste frente al blanco garantiza máxima legibilidad, especialmente en contenido textual de alta relevancia. Además, refuerza el énfasis visual y aporta un carácter formal a la estructura gráfica

  ![Artefacto creado en Figma](src/img/cap4/PrimaryColors.png)

\newpage

- **Colores Secundarios (Variantes de Logos e Iconos)**

  Estos tonos de azul se emplean para asegurar que el logotipo y los íconos mantengan su visibilidad y coherencia visual en diferentes fondos y dispositivos. Las variantes permiten adaptar la marca sin perder identidad.

  - **Azul (#256CE4):** Empleado principalmente en variantes del logotipo sobre fondos claros. Ofrece buena visibilidad sin generar un contraste excesivo, manteniendo una apariencia amigable y moderna.
  
  - **Azul (#205EC6):** Alternativa versátil que proporciona equilibrio visual entre contraste y presencia de marca. Es útil para contextos digitales y materiales impresos donde se requiere mantener una estética sobria sin perder fuerza gráfica.
  
  - **Azul Oscuro (#123672):** Aplicado sobre fondos oscuros o saturados. Este tono profundo refuerza la elegancia, seriedad y profesionalismo de la marca, siendo apropiado para presentaciones formales, documentación institucional o entornos corporativos.
  
  ![Artefacto creado en Figma](src/img/cap4/SecondColors.png)

\newpage

**Tipografía**

La identidad tipográfica de *RutaKids* ha sido cuidadosamente definida para asegurar legibilidad, jerarquía visual y consistencia en todas sus plataformas: landing page, aplicación web y aplicación móvil. Se emplean diferentes fuentes según el entorno, adaptadas a las necesidades visuales y funcionales de cada interfaz.

1. ***Landing Page***

- ***DM Sans* (Google Fonts)**
  
  - Pesos utilizados: *Bold, Medium, Regular, Italic*
  
  DM Sans es la tipografía principal utilizada en la landing page de RutaKids. Su diseño limpio y geométrico facilita la lectura tanto en títulos como en cuerpos de texto. La versión Bold se aplica a encabezados principales, Medium en párrafos destacados, y Regular e Italic en textos complementarios o citas.

  ![Artefacto creado en Figma](src/img/cap4/Typography_DMSans_landing.png)


- ***Space Grotesk* (Google Fonts)**
  
  - Peso utilizado: *Regular*
  
  Space Grotesk se utiliza de manera puntual en elementos destacados, como subtítulos o frases clave. Su estilo contemporáneo y ligeramente técnico aporta una personalidad moderna al diseño general de la landing page.

  ![Artefacto creado en Figma](src/img/cap4/Typography_SpaceGrotesk_landing.png)


2. **Aplicación Web**

- ***Outfit* (Google Fonts)**
  
  - Peso utilizado: *Bold, Medium, Regular*
  
  *Outfit* es la fuente principal empleada en la interfaz web. Su estructura sencilla y bien espaciada la hace ideal para entornos digitales centrados en la usabilidad. El peso Bold se asigna a títulos, Medium a subtítulos y elementos intermedios, y Regular al contenido general del sistema.

  ![Artefacto creado en Figma](src/img/cap4/Typography_Outfit_web.png)


3. **Aplicación Movil**

- ***Poppins* (Google Fonts)**
  
  - Peso utilizado: *Bold, Medium, Regular*
  
   *Poppins* es la tipografía principal de la app móvil. Su diseño geométrico y moderno contribuye a una interfaz clara y coherente. La versión Bold se utiliza para títulos y acciones clave, aportando énfasis visual. Medium se aplica en subtítulos y encabezados secundarios, manteniendo una jerarquía visual sólida. Y regular es ideal para el cuerpo del texto, asegurando una lectura fluida y accesible.

  ![Artefacto creado en Figma](src/img/cap4/Typography_Poppins_app.png)

\newpage

**Tonos de Comunicación**

El tono de voz de *RutaKids* fue cuidadosamente definido para alinearse con los valores del proyecto: seguridad, confiabilidad y eficiencia. Dado que se trata de una solución orientada al seguimiento de estudiantes en transporte escolar, la comunicación debe ser clara, profesional y empática. Por ello, se eligieron cuatro atributos clave que guían el estilo comunicativo en todas las plataformas y puntos de contacto:

- **Neutral:** Se emplea un lenguaje objetivo y sin juicios, especialmente útil en mensajes informativos, técnicos o institucionales. Este tono permite que la información sea comprendida sin ambigüedades ni interpretaciones subjetivas, ideal para notificaciones automatizadas o estados del sistema.

- **Formal:** Se emplea una redacción cuidada y profesional, adecuada para un entorno donde participan instituciones educativas y familias.  Este tono se aplica en secciones como configuraciones, paneles administrativos o documentación, donde se requiere precisión y credibilidad. Aporta seriedad y estructura sin resultar distante.

- **Respetuoso:** La comunicación se construye desde el respeto hacia todos los usuarios, considerando que se trata de un servicio vinculado al cuidado de menores. Este tono se refleja en el lenguaje empleado en interfaces, correos, mensajes de error o ayuda, evitando cualquier forma invasiva o autoritaria.

- **Objetivo:** Utilizado principalmente en situaciones críticas o informativas, este tono se enfoca en presentar los hechos de forma concisa y sin adornos. Es ideal para notificaciones de llegada/salida, alertas de seguridad, confirmaciones y registros. Aporta precisión y rapidez en la toma de decisiones.

La combinación de estos tonos permite que RutaKids mantenga una comunicación funcional, empática y profesional, fortaleciendo la experiencia del usuario y consolidando la confianza en la solución.

![Artefacto creado en Figma](src/img/cap4/ToneOfVoice.png)

\vspace{1em}

**Eslogan**

El eslogan de RutaKids, “Seguridad que te acompaña”, expresa de manera clara el propósito de la plataforma: ofrecer protección y acompañamiento continuo a los estudiantes durante sus trayectos escolares. Con un tono cercano y directo, transmite la tranquilidad que sienten padres y colegios al saber que cada viaje está monitoreado.
La palabra “acompaña” destaca el compromiso de la marca con una presencia constante, mientras que “seguridad” refuerza su enfoque en el bienestar infantil.

![Artefacto creado en Figma](src/img/cap4/Eslogan.png)


\newpage

### Web Style Guidelines.

![Artefacto creado en Figma](src/img/cap4/cover2.png)

Esta subsección describe los lineamientos técnicos y visuales aplicados en la interfaz web del sistema RutaKids, orientada principalmente a usuarios administradores. La prioridad de diseño está centrada en la organización jerárquica de la información, la eficiencia operativa y la accesibilidad, manteniendo una estética coherente con las demás plataformas.

- **Sistema de Grillas:** Se implementa un sistema de grillas de 12 columnas basado en resoluciones estándar (1024px) y alta definición (1440px), siguiendo principios de diseño responsive. Este sistema permite estructurar la interfaz de manera modular, facilitando la disposición equilibrada de formularios, tablas, dashboards y paneles administrativos. El ancho de columna, el gutter y el padding se ajustan según los puntos de quiebre definidos por frameworks como Bootstrap o Material Design.

- **Botones:** Los botones utilizados en la plataforma web responden a tres niveles jerárquicos: Primario, Secundario y Ghost. El tamaño más común es Medium, el cual se adapta bien al uso con cursor y teclado. Cada botón cuenta con estados diferenciados (default, hover, active, focus, disabled), garantizando retroalimentación visual inmediata y accesibilidad para usuarios con dispositivos de asistencia. Se aplica una tipografía legible, colores con contraste adecuado y padding optimizado para la interacción por mouse.

- **Campos de Entrada:** Los formularios presentan campos de entrada (inputs) con distintos tipos de apoyo visual: etiquetas flotantes, íconos contextuales, textos de ayuda y validaciones en tiempo real. Los estados de error, enfoque y desactivado están claramente definidos mediante colorimetría, íconos e indicaciones accesibles. Esta implementación mejora la precisión en la captura de datos y minimiza errores de entrada por parte de los usuarios administrativos.

- **Diálogos:** Los diálogos modales (modal dialogs) se emplean para operaciones críticas como confirmación de eliminación, edición avanzada, carga de datos o alertas del sistema. Se utilizan tamaños desde MD hasta LG, dependiendo de la complejidad de la acción. Cada diálogo sigue una estructura clara: título, mensaje principal y acciones principales bien jerarquizadas (normalmente alineadas a la derecha).

- **Pestañas y Rutas de Navegación (Tabs & Breadcrumbs):** Las pestañas permiten la organización de múltiples vistas dentro de un mismo módulo (por ejemplo, "Estudiantes | Rutas | Choferes"). Se aplican tanto tabs horizontales (en dashboards) como verticales (en paneles de configuración). Para la navegación jerárquica, se utilizan breadcrumbs que indican el camino recorrido por el usuario, permitiendo un retorno contextual a secciones anteriores. Estos elementos están diseñados para integrarse visualmente al layout general sin romper la jerarquía de contenido.

\newpage

### Mobile Style Guidelines.

![Artefacto creado en Figma](src/img/cap4/cover3.png)

Esta subsección aborda los lineamientos específicos de diseño para las aplicaciones móviles del sistema RutaKids, segmentados en función de los perfiles de usuario: padres de familia y choferes. En ambos casos, se busca optimizar la experiencia de uso considerando el contexto de movilidad, la simplicidad de interacción y la legibilidad de los elementos visuales.

**App Móvil (Padres):** La aplicación móvil para padres está diseñada para facilitar la consulta rápida de información relevante, como el estado del estudiante, notificaciones y configuración de alertas.

  - **Sistema de Grillas:** Se emplean estructuras tipo "card" que organizan la información por bloques visuales claramente diferenciados. Estas grillas priorizan la jerarquía informativa y la legibilidad desde dispositivos móviles.
  - **Botones:** Se utilizan botones de tamaño Medium o Large, acompañados de íconos y etiquetas claras. Están optimizados para pantallas táctiles, con colores familiares que facilitan la acción.
  - **Inputs:** Limitados a funciones específicas como edición de datos personales, contacto de emergencia o cambio de contraseña. Se prioriza la simplicidad y accesibilidad táctil.
  - **Diálogos:** Se implementan diálogos XS o SM, centrados en la toma de decisiones simples, como confirmar acciones o mostrar mensajes relevantes.
  - **Pestañas:** Scrollables en orientación horizontal, permitiendo acceder a múltiples secciones (seguimiento, historial, configuración) sin salir de la vista principal. Los íconos y el subrayado del tab activo facilitan la navegación.

**App Móvil (Chofer):** La interfaz móvil destinada a los choferes está pensada para su uso en movimiento, con un enfoque en la simplicidad operativa, accesibilidad rápida y visibilidad alta incluso bajo condiciones de luz variables.

  - **Sistema de Grillas:** Se utiliza una grilla reducida con espaciado amplio entre elementos, para evitar sobrecarga visual y permitir interacciones precisas.
  - **Botones:** Predominan los botones de tamaño Large, con alto contraste y accesibilidad con una sola mano. Acciones como "Iniciar ruta" o "Confirmar subida" están siempre visibles y priorizadas.
  - **Inputs:** Se utilizan de forma muy limitada, por ejemplo para ingresar un código de ruta o una nota corta. Se evita la introducción extensiva de datos.
  - **Diálogos:** De tipo XS, con acciones claras de una sola pulsación. Los mensajes deben poder visualizarse y comprenderse rápidamente.
  - **Pestañas:** Secciones como "Mapa de Ruta", "Lista de Estudiantes" y "Alertas" se organizan mediante tabs grandes y fácilmente accesibles. Se prioriza la navegabilidad sin distracción.


#### iOS Mobile Style Guidelines.

Esta subsección presenta los lineamientos de adaptación visual de la app RutaKids al sistema operativo iOS, siguiendo las convenciones de diseño establecidas por Apple sin perder coherencia con la identidad visual general del sistema.

**Tipografía y Espaciado:** Se respetan márgenes consistentes y áreas de interacción definidas por la Human Interface Guidelines (HIG).

**Componentes de navegación:** La navegación se apoya en tabs inferiores y gestos nativos. El uso de "pull to refresh", swipes horizontales y animaciones de rebote (bounce) mejora la percepción de fluidez.

**Botones e Inputs:** Botones integrados con estilos nativos, adecuadamente dimensionados para la interacción táctil. Inputs con comportamiento flotante y validación en línea según los patrones iOS.

**Diálogos:** Se adaptan a los alert controllers nativos, priorizando claridad textual, accesibilidad y consistencia visual con el resto del sistema.

**Aplicación por plataforma:**

  - **Padres:**Navegación basada en tab bar inferior, estilo pulido con animaciones suaves y uso de íconos nativos.

  - **Chofer:**Botones grandes, simplificación visual y respuestas táctiles inmediatas para operaciones rápidas.


#### Android Mobile Style Guidelines.

Esta subsección define la implementación visual de RutaKids sobre Android, enmarcada en los principios de Material Design. Se prioriza la familiaridad con el entorno Android sin comprometer la coherencia visual del sistema.

- **Diseño Material:** Uso de tarjetas (cards), sombras, colores planos y animaciones por jerarquía. Se emplean elementos como AppBars, BottomNavigation y Floating Action Buttons (FAB) cuando corresponde.
- **Componentes interactivos:** Botones con efectos ripple para feedback inmediato. Inputs con labels flotantes y validación dinámica. Compatible con temas claros y oscuros.
- **Navegación:** Navegación por pestañas (tabs) o mediante el Drawer Navigation (menú lateral deslizable). Scroll y comportamiento anidado acorde al patrón de jerarquías visuales.
- **Diálogos:** Material Dialogs estilizados, con botones alineados a la derecha y estructuras modulares según tipo de interacción requerida.
- **Aplicación por plataforma:**
  - **Padres:** Interfaz basada en navegación por tabs y cards, con colores suaves y accesibilidad táctil.
  - **Chofer:** Uso destacado de FAB para acciones clave, diseño sobrio y botones de acción de gran tamaño para accesibilidad en movimiento.

### Guía Gráfica de Componentes de Interfaz

A continuación, se presenta una ilustración unificada con la representación visual de los componentes descritos en las secciones anteriores. Esta guía gráfica sintetiza los estilos aplicados a:


\begin{longtable}{|c|c|p{5cm}|p{4cm}|}
\hline
\textbf{Componente} & \textbf{Plataforma} & \textbf{Medidas / Diseño} & \textbf{Propósito} \\
\hline
\endfirsthead
\hline
\textbf{Componente} & \textbf{Plataforma} & \textbf{Medidas / Diseño} & \textbf{Propósito} \\
\hline
\endhead
Sistema de Grillas & Web & Grillas de 12 columnas para dashboards & Organización robusta y flexible para interfaces amplias y modulares. \\
\hline
Sistema de Grillas & App Padres & Estructura en formato card & Visualización clara e individual de la información de cada hijo. \\
\hline
Sistema de Grillas & App Chofer & Grillas simplificadas, elementos separados & Claridad y acceso rápido para uso mientras se conduce. \\
\hline
Botones y Enlaces & Web & Hover/focus con interacción precisa & Mejora la usabilidad con retroalimentación visual clara. \\
\hline
Botones y Enlaces & App Padres & Botones grandes y con íconos & Facilidad de uso en pantallas táctiles. \\
\hline
Botones y Enlaces & App Chofer & Botones accesibles con una mano & Operación rápida y segura en movimiento. \\
\hline
Campos de Entrada & Web & Formularios extensos, validaciones completas & Permite entrada de datos compleja con control de errores. \\
\hline
Campos de Entrada & App Padres & Campos limitados, centrados en configuración & Enfoque simple para configuraciones clave. \\
\hline
Campos de Entrada & App Chofer & Inputs mínimos, simples & Minimiza distracciones y facilita el uso. \\
\hline
Diálogos Emergentes & Web & Edición, confirmación, advertencia & Gestión clara de acciones críticas. \\
\hline
Diálogos Emergentes & App Padres & Acciones directas y sencillas & Rápida toma de decisiones. \\
\hline
Diálogos Emergentes & App Chofer & Un toque, alta visibilidad & Interacción inmediata, útil en ruta. \\
\hline
Tabs de Navegación & Web & Organización por vistas & Segmentación clara de contenidos. \\
\hline
Tabs de Navegación & App Padres & Seguimiento e historial & Monitoreo del estado y recorridos previos. \\
\hline
Tabs de Navegación & App Chofer & Mapa, lista de alumnos & Verificación visual de ruta y estudiantes. \\
\hline
Breadcrumbs & Web & Esencial para vistas jerárquicas & Permite ubicar al usuario dentro del sistema. \\
\hline
Breadcrumbs & App Padres & No aplican directamente & Navegación simple, sin jerarquía compleja. \\
\hline
Breadcrumbs & App Chofer & No aplican directamente & Interfaz directa sin necesidad de navegación jerárquica. \\
\hline
\end{longtable}


Las siguientes figuras presentan una síntesis visual de los elementos de interfaz definidos para el sistema RutaKids. Cada imagen corresponde a un componente central previamente descrito y está alineada con las aplicaciones web, móviles e IoT. Este soporte gráfico permite validar la coherencia visual y facilita su implementación durante el desarrollo del sistema.

\newpage


![**Sistema de Grillas** - Artefacto creado en Figma](src/img/cap4/Grid.png)

![**Botones y Enlaces** - Artefacto creado en Figma](src/img/cap4/Button_Link.png)

![**Campos de Entrada** - Artefacto creado en Figma](src/img/cap4/Input_fields.png)

![**Diálogos Emergentes** - Artefacto creado en Figma](src/img/cap4/Dialog.png)

![**Pestañas de Navegación (Tabs)** - Artefacto creado en Figma](src/img/cap4/Tabs.png)

![**Rutas de Navegación (Breadcrumbs)** - Artefacto creado en Figma](src/img/cap4/Breadcrumbs.png)


\newpage


## Information Architecture.

![Artefacto creado en Canva](src/img/cap4/InformationArchitecture.png)

La arquitectura de la información (AI) se refiere al proceso de estructuración y categorización del contenido digital con el fin de facilitar su localización y comprensión por parte de los usuarios. Este aspecto es esencial para asegurar una experiencia fluida, especialmente en entornos digitales como aplicaciones móviles, donde la claridad en la organización puede determinar el éxito de la interacción usuario-sistema.


\begin{quote}
De acuerdo con Lin y Zarro (2024), una arquitectura de información bien diseñada “brinda estructura a la experiencia del usuario y actúa como una guía cognitiva que facilita la navegación, reduce la incertidumbre y mejora la eficiencia de uso en sistemas digitales complejos.
\end{quote}

\vspace{1em}

En el desarrollo de RutaKids, se adoptó una estructura centrada en los principales perfiles de usuarios: padres de familia, conductores y gestores de transporte escolar. La intención fue lograr una jerarquía de información comprensible, accesible y coherente que soporte la visualización en tiempo real, la administración de rutas y estudiantes, y la comunicación segura dentro de la aplicación.

A continuación se presentan los mapas generales de arquitectura de información correspondientes a cada tipo de usuario:

**Arquitectura de Información – App Móvil para Padres**

![Artefacto creado en Figma](src/img/cap4/AppPadres.png)

**Arquitectura de Información – App Móvil para Conductores**

![Artefacto creado en Figma](src/img/cap4/AppConductores.png)

**Arquitectura de Información – Plataforma Web para Administradores**

![Artefacto creado en Figma](src/img/cap4/AppWeb.png)


Las secciones siguientes profundizan en los sistemas implementados para organización, etiquetado, navegación y búsqueda, así como en los elementos de SEO (Search Engine Optimization) y ASO (App Store Optimization) que fortalecen la visibilidad del producto.

\newpage

### Organization Systems.

- **Propósito**

  La arquitectura organizativa de un producto digital permite estructurar la información de forma que los usuarios accedan rápida y eficientemente a los contenidos que necesitan. 

  Según Morville y Rosenfeld (2006), “los sistemas de organización son esenciales para transformar el caos en claridad, facilitando que los usuarios comprendan la lógica detrás del contenido digital”. 

  En el caso de *RutaKids*, se han diseñado diversos sistemas de organización visual y estructural adaptados tanto a padres como a administradores educativos.

- **Organización para padres de familia (App móvil)**

  La aplicación móvil muestra la información más relevante sobre el estado de sus hijos y el transporte escolar. La información sigue un modelo jerárquico en su interfaz principal y secuencial en el monitoreo de rutas.

\begin{longtable}{|p{3cm}|p{3cm}|p{2.5cm}|p{4cm}|}
\hline
\textbf{Tópico} & \textbf{Sistema de Organización Visual} & \textbf{Categorización Aplicada} & \textbf{Descripción} \\
\hline
\endfirsthead
\hline
\textbf{Tópico} & \textbf{Sistema de Organización Visual} & \textbf{Categorización Aplicada} & \textbf{Descripción} \\
\hline
\endhead
Estado del recorrido & Jerárquico visual & Cronológica & Se presenta primero el nombre del conductor, estado, hora estimada y destino. \\
\hline
Línea de tiempo del viaje & Secuencial (paso a paso) & Cronológica & Refleja el progreso del viaje con puntos y estados temporales en orden. \\
\hline
Historial de viajes & Lista jerárquica ordenada & Cronológica & Permite revisar viajes anteriores organizados por fecha. \\
\hline
Hijos registrados & Jerárquico visual & Por audiencia (por cada hijo) & Cada hijo tiene su propio conjunto de datos visibles en tiempo real. \\
\hline
\end{longtable}

- **Organización para administradores educativos (Plataforma web)**

  La plataforma web está orientada a la administración y seguimiento operativo. Utiliza una estructura modular con categorización por tópicos y por audiencia (vehículos, estudiantes, rutas, conductores).

\begin{longtable}{|p{3cm}|p{3cm}|p{2.5cm}|p{4cm}|}
\hline
\textbf{Tópico} & \textbf{Sistema de Organización Visual} & \textbf{Categorización Aplicada} & \textbf{Descripción} \\
\hline
\endfirsthead
\hline
\textbf{Tópico} & \textbf{Sistema de Organización Visual} & \textbf{Categorización Aplicada} & \textbf{Descripción} \\
\hline
\endhead
Dashboard & Jerárquico (panel con KPIs) & Por tópico & Muestra métricas clave: rutas activas, incidencias, temperatura, etc. \\
\hline
Gestión de estudiantes & Visual matricial & Por tópico y audiencia (grado/edad) & Clasificación de alumnos por grados escolares y grupos etarios. \\
\hline
Gestión de vehículos y rutas & Jerárquico + secuencial (módulo por pasos) & Por tópico (vehículos, zonas, rutas) & Panel para registro, edición y asignación de unidades a rutas. \\
\hline
Monitoreo en tiempo real & Jerárquico + secuencial & Cronológica y geoespacial & Muestra mapa con rutas, ubicación, velocidad, y eventos críticos. \\
\hline
Reportes e incidencias & Modular & Cronológica / por evento & Acceso a reportes por fecha, tipo de evento (desvíos, alertas térmicas). \\
\hline
\end{longtable}


- **Organización en la Landing Page (Sitio Estático)**

  La landing page está diseñada para atraer y guiar a nuevos usuarios. Utiliza una estructura secuencial, pensada para recorrer la información desde el valor de la app hasta las secciones específicas según audiencia.

\begin{longtable}{|p{3cm}|p{4cm}|p{2.5cm}|p{4cm}|}
\hline
\textbf{Tópico} & \textbf{Organización Visual} & \textbf{Categorización Aplicada} & \textbf{Descripción} \\
\hline
\endfirsthead
\hline
\textbf{Tópico} & \textbf{Organización Visual} & \textbf{Categorización Aplicada} & \textbf{Descripción} \\
\hline
\endhead
Menú principal & Jerárquico visual horizontal & Por tópicos & Inicio, Beneficios, Características, Padres, Colegios, Contáctanos. \\
\hline
Flujo de contenido & Secuencial (scroll vertical guiado) & Por audiencia & Explica beneficios para padres, luego para colegios. \\
\hline
CTA (Call to Action) & Jerárquico visual final & Ninguna & Botones de descarga o contacto resaltados al final. \\
\hline
\end{longtable}

Esta organización garantiza que tanto padres como administradores puedan interactuar de forma clara, eficiente y segura con la plataforma, reduciendo fricción y mejorando la toma de decisiones y la supervisión del servicio de transporte escolar.


\newpage

### Labeling Systems.

6. **Sistemas de Etiquetado**

- **Propósito**

  Los sistemas de etiquetado son fundamentales para la claridad del contenido y la navegación en cualquier producto digital. Una correcta nomenclatura ayuda a los usuarios a comprender de inmediato qué acciones pueden realizar, qué información están observando y qué pasos seguir.

  En *RutaKids*, las etiquetas han sido desarrolladas con un enfoque en simplicidad, consistencia y significado contextual, garantizando una experiencia clara para los distintos tipos de usuarios: padres, administradores y conductores.

- **App móvil – Padres de familia**

\begin{longtable}{|p{4cm}|p{10.5cm}|}
\hline
\textbf{Tópico} & \textbf{Definición} \\
\hline
\endfirsthead
\hline
\textbf{Tópico} & \textbf{Definición} \\
\hline
\endhead
Inicio & Etiqueta utilizada para acceder a la pantalla principal, donde se presenta un resumen del estado del recorrido escolar en tiempo real. \\
\hline
Monitoreo & Abre el mapa con la ubicación actual del vehículo asignado, permitiendo ver el avance de la ruta y el estado del transporte del estudiante. \\
\hline
Historial & Muestra los viajes anteriores del estudiante, organizados por fecha, incluyendo hora de salida, llegada y eventos registrados. \\
\hline
Cuenta & Acceso a la configuración de perfil del padre, donde puede editar datos personales, activar o desactivar notificaciones y cerrar sesión. \\
\hline
\end{longtable}

- **App móvil – Conductores**

\begin{longtable}{|p{4cm}|p{10.5cm}|}
\hline
\textbf{Tópico} & \textbf{Definición} \\
\hline
\endfirsthead
\hline
\textbf{Tópico} & \textbf{Definición} \\
\hline
\endhead
Iniciar ruta & Botón que activa el inicio oficial del recorrido asignado; al presionarlo, se activa la navegación GPS hacia el primer punto de recojo. \\
\hline
Ver en GPS & Redirección automática al sistema de navegación (Google Maps, Waze, etc.) con la ruta preestablecida desde la plataforma. \\
\hline
Finalizar ruta & Permite al conductor cerrar el recorrido una vez completado, registrando hora de llegada y finalizando el monitoreo en tiempo real. \\
\hline
\end{longtable}

\newpage

### SEO Tags and Meta Tags


- **Propósito**

  En la aplicación *RutaKids*, los *SEO Tags* y *Meta Tags* juegan un rol crucial para garantizar la visibilidad del producto tanto en motores de búsqueda como en tiendas de aplicaciones móviles. 

  Aunque el producto incluye una plataforma web y una aplicación móvil, la *landing page* cumple un rol estratégico al actuar como primer punto de contacto para nuevos usuarios, por lo que ha sido optimizada mediante el uso de etiquetas específicas.


- **SEO Tags**

  Los SEO Tags permiten mejorar el posicionamiento de la landing page de *RutaKids* en buscadores como Google, facilitando que padres y colegios interesados encuentren rápidamente el producto. A continuación se muestran algunos ejemplos aplicados:

  - **Title Tag**  
    Especifica el título visible en los resultados de búsqueda.

    ```html
    <title>RutaKids - Seguridad y Monitoreo Escolar en Tiempo Real</title>
    ```

  - **Meta Description**  
    Describe brevemente el contenido de la página.

    ```html
    <meta name="description" content="RutaKids es una plataforma de movilidad escolar con pulseras RFID. Permite a los padres monitorear en tiempo real los recorridos escolares de sus hijos y a los colegios gestionar rutas de forma eficiente." />
    ```

  - **Header Tags**  
    Estructuran jerárquicamente el contenido.

    ```html
    <h1>Movilidad Escolar Inteligente</h1>
    <h2>Monitorea a tus hijos en tiempo real</h2>
    <h3>Gestiona flotas escolares con tecnología RFID</h3>
    ```


- **Meta Tags**

  Los Meta Tags proporcionan información técnica a navegadores y motores de búsqueda, mejorando la experiencia del usuario y el SEO técnico. Algunos utilizados en *RutaKids* son:

  - **Charset Meta Tag**

    ```html
    <meta charset="UTF-8">
    ```

  - **Viewport Meta Tag**

    ```html
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    ```

  - **Robots Meta Tag**

    ```html
    <meta name="robots" content="index, follow">
    ```

  - **Canonical Tag**

    ```html
    <link rel="canonical" href="https://rutakids.com">
    ```


- **Landing Page SEO Tags (para la aplicación móvil)**

  Además de las etiquetas estándar, se han definido etiquetas específicas para promover la aplicación móvil directamente desde la landing page:

  ```html
  <title>RutaKids | Transporte Escolar Seguro y Conectado</title>
  <meta name="description" content="RutaKids permite a padres monitorear a sus hijos durante el transporte escolar mediante pulseras RFID. Disponible para iOS y Android.">
  <meta name="keywords" content="app transporte escolar, seguridad infantil, GPS escolar, pulseras RFID, monitoreo niños">
  <meta name="author" content="LlantaTech">
  <link rel="canonical" href="https://rutakids.com/">
    ```

- **App Store Optimization (ASO)**

  Para aumentar la visibilidad de la aplicación en tiendas como Google Play o App Store, RutaKids aplica estrategias de ASO (App Store Optimization) que incluyen título, descripción, palabras clave y categorías.


\begin{longtable}{|p{4cm}|p{10.5cm}|}
\hline
\textbf{Elemento} & \textbf{Valor propuesto} \\
\hline
\endfirsthead
\hline
\textbf{Elemento} & \textbf{Valor propuesto} \\
\hline
\endhead
App Title & RutaKids: Monitoreo Escolar en Tiempo Real \\
\hline
App Subtitle & Seguridad escolar con tecnología RFID \\
\hline
App Description & Con RutaKids, los padres pueden seguir en tiempo real los recorridos escolares de sus hijos, recibir alertas, revisar historial de viajes y confiar en un sistema seguro con tecnología RFID. Ideal para colegios modernos y comprometidos con la seguridad. \\
\hline
Keywords & transporte escolar, app para padres, seguridad infantil, RFID, monitoreo niños \\
\hline
Developer & LlantaTech \\
\hline
Categoría & Educación / Familias \\
\hline
URL descarga Android & \url{https://play.google.com/store/apps/details?id=com.rutakids} \\
\hline
URL descarga iOS & \url{https://apps.apple.com/app/rutakids/id123456789} \\
\hline
\end{longtable}


El uso estratégico de SEO Tags y Meta Tags en RutaKids no solo mejora la visibilidad en buscadores y redes sociales, sino que también facilita la experiencia del usuario desde el primer contacto con la plataforma. Además, las etiquetas ASO aseguran un buen posicionamiento en las tiendas de aplicaciones, promoviendo así la descarga y uso efectivo del producto.



### Searching Systems.


- **Propósito**

  Los sistemas de búsqueda en productos digitales permiten al usuario navegar grandes volúmenes de información de forma efectiva, evitando pérdida de tiempo y frustración.

  En *RutaKids*, la búsqueda activa está implementada únicamente en la plataforma web de administradores, ya que la aplicación móvil está diseñada para mostrar información personalizada y filtrada automáticamente para los padres de familia.



- **Filtros y herramientas de búsqueda en la Web App**

\begin{longtable}{|p{5cm}|p{9.5cm}|}
\hline
\textbf{Filtro / Función} & \textbf{Definición} \\
\hline
\endfirsthead
\hline
\textbf{Filtro / Función} & \textbf{Definición} \\
\hline
\endhead
Nombre del estudiante & Permite encontrar a un estudiante específico mediante la entrada parcial o completa de su nombre. \\
\hline
Código de pulsera RFID & Filtra directamente por el identificador asignado al estudiante. \\
\hline
Grado escolar / Edad & Muestra únicamente a estudiantes de un grado o grupo etario específico. \\
\hline
Ruta asignada & Filtra a los estudiantes según el recorrido o zona a la que pertenecen. \\
\hline
Nombre del conductor & Permite identificar qué conductor está asignado a una ruta o grupo de estudiantes. \\
\hline
Fecha / rango de fechas & Busca viajes, alertas o registros según el día o periodo seleccionado. \\
\hline
Tipo de alerta & Clasifica las notificaciones (ej. alerta de desvío, abordaje no detectado, temperatura fuera del umbral). \\
\hline
Estado del recorrido & Muestra únicamente registros en estado específico: “en tránsito”, “finalizado”, “no iniciado”. \\
\hline
Búsqueda combinada avanzada & Combina múltiples filtros (ej. por nombre + ruta + fecha) para obtener resultados más precisos. \\
\hline
\end{longtable}



- **Diseño de resultados y experiencia de búsqueda**

  - Resultados ordenados alfabéticamente o por fecha según el módulo.
  - Interfaz con autocompletado en campos de búsqueda (como nombres o placas).
  - Posibilidad de acceder al detalle directamente desde los resultados.
  - Visualización clara en tarjetas o tablas, según el tipo de información.



- **App móvil – Padres de familia**

  En la app móvil, no se requiere una herramienta de búsqueda, ya que toda la información está pre-filtrada por el sistema. Cada padre solo visualiza la información correspondiente a sus hijos y sus viajes.

\begin{longtable}{|p{5cm}|p{9.5cm}|}
\hline
\textbf{Característica} & \textbf{Función} \\
\hline
\endfirsthead
\hline
\textbf{Característica} & \textbf{Función} \\
\hline
\endhead
Vista filtrada por estudiante & Si hay más de un hijo, el sistema separa la información por cada uno. \\
\hline
Historial por fecha & Organiza automáticamente los viajes anteriores por orden cronológico. \\
\hline
Alertas personalizadas & Solo muestra notificaciones relevantes al estudiante registrado. \\
\hline
\end{longtable}



Esta combinación de sistemas asegura que tanto administradores como padres puedan encontrar información crítica sin esfuerzo, optimizando el uso del sistema y mejorando la experiencia general.


\newpage

### Navigation Systems.

- **Propósito**

  Los sistemas de navegación son el conjunto de elementos y patrones que permiten a los usuarios moverse a través del contenido y funcionalidades de una interfaz. Una buena navegación no solo facilita el desplazamiento, sino que también guía, orienta y reduce el esfuerzo cognitivo.

  Como afirman Garrett (2011), “la navegación efectiva proporciona al usuario una sensación de lugar, dirección y control dentro de un producto digital”.

  En *RutaKids*, se implementan sistemas de navegación adaptados a cada tipo de usuario: padres (app móvil), conductores (app móvil simplificada) y administradores escolares (plataforma web). En cada caso, la navegación fue diseñada para ajustarse al nivel de interacción y al contexto de uso.



- **App móvil – Padres de familia**

\begin{longtable}{|p{5cm}|p{9.5cm}|}
\hline
\textbf{Elemento de navegación} & \textbf{Descripción} \\
\hline
\endfirsthead
\hline
\textbf{Elemento de navegación} & \textbf{Descripción} \\
\hline
\endhead
Menú inferior (tab bar) & Contiene accesos directos a: Inicio, Monitoreo, Historial y Cuenta. Visible en toda la app. \\
\hline
Navegación jerárquica & Cada sección permite acceder a pantallas secundarias (por ejemplo, ver detalle del historial). \\
\hline
Retroalimentación visual & Íconos activos con cambio de color al seleccionarse, y notificaciones visibles (campana). \\
\hline
Navegación simplificada & Solo se muestran las funciones relevantes al rol del padre, evitando sobrecarga de opciones. \\
\hline
\end{longtable}



- **App móvil – Conductores**

\begin{longtable}{|p{5cm}|p{9.5cm}|}
\hline
\textbf{Elemento de navegación} & \textbf{Descripción} \\
\hline
\endfirsthead
\hline
\textbf{Elemento de navegación} & \textbf{Descripción} \\
\hline
\endhead
Interfaz de acción directa & La navegación está basada en 2 o 3 botones: Iniciar Ruta, Ver GPS, Finalizar Ruta. \\
\hline
Redirección externa (GPS) & Al iniciar ruta, se abre la app de navegación externa (Google Maps o Waze) automáticamente. \\
\hline
Diseño de una sola vista & La app evita navegación compleja; el conductor solo necesita cumplir un flujo puntual. \\
\hline
\end{longtable}



- **Plataforma Web – Administradores**

\begin{longtable}{|p{5cm}|p{9.5cm}|}
\hline
\textbf{Elemento de navegación} & \textbf{Descripción} \\
\hline
\endfirsthead
\hline
\textbf{Elemento de navegación} & \textbf{Descripción} \\
\hline
\endhead
Menú lateral persistente & Acceso directo a módulos: Dashboard, Estudiantes, Rutas, Monitoreo, Notificaciones, Configuración, etc. \\
\hline
Submenús plegables & Algunas secciones contienen subcategorías, como niveles escolares dentro de "Estudiantes". \\
\hline
Navegación matricial & Vista tipo grid para elementos como grados escolares o rutas disponibles. \\
\hline
Navegación contextual & Acciones como “Editar” o “Asignar ruta” aparecen directamente en el contexto de la información. \\
\hline
Accesos rápidos & Acciones frecuentes resaltadas visualmente (botones flotantes o en tarjetas). \\
\hline
\end{longtable}


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

El diseño UX/UI de aplicaciones móviles busca crear experiencias intuitivas, eficientes y agradables que respondan a las necesidades reales de los usuarios.
A través de un enfoque centrado en el usuario, se desarrollan interfaces funcionales y flujos de navegación claros que mejoran la interacción y fomentan la confianza en los servicios digitales.
Este proyecto aplica principios de usabilidad, accesibilidad y diseño visual para garantizar que cada tutor legal pueda monitorear y gestionar el transporte escolar de manera segura, sencilla y confiable.

\newpage

### Mobile Applications Wireframes.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### Mobile Applications Wireflow Diagrams.

En esta sección se presentan los wireflows diseñados para RutaKids. A través de estos diagramas, se busca representar de manera clara y estructurada cómo los padres de familia o tutores legales pueden navegar por la app, realizar tareas esenciales como el inicio de sesión, la visualización de trayectos en tiempo real, la recepción de notificaciones, el acceso al historial de viajes, entre otros.
Cada wireflow incluye tanto los objetivos del usuario como la descripción paso a paso del flujo de tareas, facilitando así la comprensión del recorrido de usuario y la funcionalidad de la aplicación.

**Wireflow Diagram 1 :  Inicio de Sesión**

- **User Goal:**
  El tutor legal desea acceder a la aplicación móvil para monitorear el transporte escolar de su hijo/a.

- **Task Flow (Flujo de tareas del usuario):**
  1. Visualiza la pantalla de carga con el logo de la aplicación al abrir la app por primera vez.
  2. Visualiza la pantalla con información de lo que ofrece la aplicación
  3. Accede a la pantalla de inicio de sesión.
  4. Ingresa sus credenciales (correo electrónico y contraseña).
  5. En caso de haber olvidado la contraseña, solicita su recuperación mediante correo electrónico.
  6. Si las credenciales son válidas, el sistema redirige a la pantalla de carga mientras valida la sesión.
  7. Finalmente, accede a la pantalla principal (dashboard) desde donde podrá realizar el monitoreo del transporte.

A continuación, se muestran de forma secuencial las pantallas involucradas en el proceso de inicio de sesión de un tutor legal, detallando las interacciones principales y transiciones posibles desde la carga inicial de la aplicación hasta el acceso exitoso al panel de monitoreo.

![Artefacto creado en Figma](src/img/cap4/WD/WD_SignIn.png)

\newpage

**Wireflow Diagram 2 :  Visualización de eventos del recorrido (línea de tiempo)**

- **User Goal:**  
  El tutor legal desea consultar el estado y el avance del recorrido escolar para asegurar el cumplimiento del trayecto.

- **Task Flow (Flujo de tareas del usuario):**
  1. Desde la pantalla principal, el tutor identifica el seguimiento activo del transporte.
  2. Presiona el botón "Detalles" ubicado en la parte inferior de la tarjeta del trayecto.
  3. El sistema redirige a una pantalla donde se presenta una línea de tiempo con los eventos del recorrido.
  4. En esta línea de tiempo, el usuario puede observar:
     - Inicio del recorrido
     - Llegada del conductor al punto de encuentro
     - Abordaje de los estudiantes
     - Estado "en camino"
     - Llegada al colegio
     - Descenso de los estudiantes
     - Finalización del trayecto
  5. El usuario puede tocar eventos interactivos (como el abordaje) para ver un modal con información adicional: nombres, horarios y matrícula del vehículo.
  6. El usuario puede regresar o navegar entre vistas sin perder el progreso visual del seguimiento.


![Artefacto creado en Figma](src/img/cap4/WD/WD_Details.png)

Este wireflow describe el módulo de visualización detallada del recorrido escolar. Tras acceder desde la pantalla principal, el tutor legal puede observar una representación cronológica de los eventos clave del trayecto, organizada mediante una línea de tiempo progresiva.
La visualización incluye horarios, estados y acciones del conductor, así como hitos importantes como el momento en que los estudiantes abordan o descienden de la unidad. Para mejorar la trazabilidad, algunos eventos son interactivos y despliegan ventanas modales con información adicional. Este módulo garantiza transparencia y confianza sobre el cumplimiento del servicio de transporte.


\newpage

**Wireflow Diagram 3 :  Notificaciones de eventos**

- **User Goal:**  
  El tutor legal desea recibir alertas sobre momentos importantes del viaje, como el inicio del recorrido o la llegada al punto de encuentro, para mantenerse informado sobre el trayecto de su hijo/a.

- **Task Flow (Flujo de tareas del usuario):**
  1. El sistema genera automáticamente notificaciones push cuando ocurre un evento clave del recorrido escolar, por ejemplo:
     - El conductor inicia el recorrido.
     - La unidad llega al punto de encuentro.
  2. El tutor recibe una alerta en su dispositivo móvil.
  3. Al abrir la aplicación, accede a la sección "Notificaciones" desde el ícono de campana o desde la barra inferior.
  4. Visualiza una lista de eventos relevantes en orden cronológico.
  5. Puede seleccionar una notificación específica para ver más detalles.
  6. Se despliega una tarjeta informativa con:
     - Iconografía del evento
     - Mensaje descriptivo
     - Hora exacta del suceso
     - Fecha y unidad asociada
  7. El tutor puede regresar a la vista anterior tras consultar el detalle.


![Artefacto creado en Figma](src/img/cap4/WD/WD_Notifications.png)

Este wireflow describe la interacción del tutor legal con el módulo de notificaciones dentro de la aplicación móvil. El sistema genera alertas automáticas basadas en eventos definidos durante el recorrido escolar, como la salida de la unidad o la llegada al punto de recogida.
Estas notificaciones se agrupan en una vista dedicada dentro de la app, accesible desde el menú inferior o un ícono persistente. Cada alerta incluye un resumen visual del evento, hora exacta, iconografía asociada y una breve descripción. Al seleccionar una notificación, el tutor puede expandir la información para entender mejor el contexto del evento, fortaleciendo la comunicación y el monitoreo en tiempo real del transporte escolar.

\newpage

**Wireflow Diagram 4 :  Visualización del trayecto del transporte escolar en mapa en tiempo real**

- **User Goal:**  
  El tutor legal desea visualizar en tiempo real la ruta que sigue la unidad de transporte escolar, con información resumida del conductor, clima y estado del viaje.

- **Task Flow (Flujo de tareas del usuario):**
  1. Desde la pantalla principal (Inicio), el tutor identifica la tarjeta con información de su unidad asignada.
  2. Presiona el botón “Detalles”.
  3. El sistema redirige al usuario a una pantalla con mapa en vivo.
  4. En esta pantalla se visualiza:
     - Ruta actual del transporte (de punto A al punto B)
     - Ubicación en tiempo real del bus
     - Nombre y contacto del conductor
     - Estado: "En tránsito"
     - Tiempo estimado de llegada
     - Temperatura actual
     - Pasajeros a bordo
  5. La información se actualiza automáticamente durante el trayecto.
  6. El usuario puede regresar a la pantalla principal en cualquier momento desde la navegación inferior.


![Artefacto creado en Figma](src/img/cap4/WD/WD_LiveMap.png)

Este wireflow representa el proceso mediante el cual el tutor accede al monitoreo visual del trayecto escolar a través de un mapa en tiempo real. Desde la pantalla principal, el usuario puede seleccionar la opción “Detalles”, lo cual lo redirige a una vista de mapa interactivo donde se muestra la posición actual del bus, así como la ruta proyectada desde origen hasta destino.
En la misma vista, se presentan datos complementarios como el nombre del conductor, número de pasajeros, clima y tiempo estimado de llegada. La información es dinámica y se actualiza en tiempo real sin intervención del usuario. Esta funcionalidad brinda una visión rápida y clara del estado actual del transporte escolar.

\newpage

**Wireflow Diagram 5 :  Visualización en vivo del interior de la unidad**

- **User Goal:**  
  El tutor legal desea observar visualmente la unidad de transporte en tiempo real para verificar las condiciones internas y confirmar que su hijo/a viaja de forma segura.

- **Task Flow (Flujo de tareas del usuario):**
  1. Desde la pantalla de Detalles del viaje (mapa con ruta y datos del transporte), el tutor identifica el botón "Visualizar Unidad".
  2. Presiona el botón y es redirigido a una nueva vista.
  3. La aplicación muestra una transmisión en tiempo real del interior del vehículo.
  4. En la parte inferior de la pantalla se presenta:
     - La temperatura interna del vehículo.
     - El botón de regreso para volver a la vista anterior.
  5. El tutor puede observar sin interactuar y cerrar la vista cuando lo desee.
  6. Al cerrar la visualización, vuelve a la pantalla de “Detalles del viaje”.



![Artefacto creado en Figma](src/img/cap4/WD/WD_LiveInteriorView.png)

Este wireflow representa la interacción del tutor con la funcionalidad de visualización en vivo del interior del transporte escolar. Desde la pantalla de seguimiento del viaje, el tutor puede acceder mediante el botón “Visualizar Unidad” a una transmisión de video en tiempo real.
Esta vista permite monitorear visualmente las condiciones internas del vehículo, incluyendo el comportamiento de los estudiantes y el estado del entorno. Además, se ofrece la temperatura interna del bus como dato adicional. Esta funcionalidad está diseñada para reforzar la percepción de seguridad y confianza del tutor legal durante el trayecto escolar.


\newpage

**Wireflow Diagram 6 :  Consulta de historial de viajes**

- **User Goal:**  
  El tutor legal desea revisar los viajes anteriores para verificar detalles como la hora de salida y llegada, la ruta recorrida y las condiciones generales del transporte escolar.

- **Task Flow (Flujo de tareas del usuario):**
  1. Desde la pantalla principal, el tutor accede a la sección "Historial" mediante la barra de navegación inferior.
  2. Se despliega una lista de viajes completados organizados por fecha (más reciente primero).
  3. Cada tarjeta de viaje muestra:
     - Fecha del recorrido
     - Hora de llegada
     - Dirección de origen y destino
     - Clima registrado
     - Cantidad de pasajeros a bordo
     - Iconografía de estado
  4. El tutor puede desplazarse por la lista para explorar días anteriores.
  5. Al finalizar la consulta, el tutor puede navegar hacia otra sección mediante el menú inferior.

![Artefacto creado en Figma](src/img/cap4/WD/WD_Record.png)

Este wireflow corresponde a la funcionalidad de consulta del historial de viajes previos. Al acceder desde el menú principal, el tutor visualiza una lista de recorridos completados, organizados por fecha. Cada ítem contiene información clave como la hora de llegada, el número de pasajeros, las condiciones climáticas y el estado general del trayecto.
La interfaz está diseñada para facilitar el seguimiento retrospectivo de la actividad del transporte escolar, brindando al tutor una herramienta útil para auditoría personal, validación de horarios y monitoreo histórico de la puntualidad y condiciones del servicio.

\newpage

**Wireflow Diagram 7 :  Gestión de cuenta**

- **User Goal:**  
  El tutor legal desea configurar y gestionar sus datos personales, seguridad, privacidad y notificaciones desde su perfil en la aplicación.

- **Task Flow (Flujo de tareas del usuario):**
  1. Desde cualquier vista de la app, el tutor accede a la sección "Cuenta" mediante el ícono del menú inferior.
  2. En la pantalla principal, se muestran las siguientes opciones:
     - Información personal
     - Seguridad
     - Protección de datos
     - Notificaciones
  3. Si selecciona "Información personal", accede a una vista donde puede consultar y actualizar:
     - Nombre
     - Número de teléfono
     - Correo electrónico
  4. Si selecciona "Seguridad", puede:
     - Cambiar su contraseña
     - Activar o revisar la verificación en dos pasos
     - Ver el correo de soporte técnico
  5. En "Protección de datos", el tutor puede revisar:
     - Términos y condiciones
     - Políticas de privacidad
     - Información sobre protección de datos
  6. En "Notificaciones", puede activar o desactivar alertas específicas relacionadas a:
     - Transporte
     - Mapa
     - Seguimiento
     - Otros servicios
  7. El tutor puede volver a la pantalla principal de cuenta mediante el ícono de retroceso o la barra inferior.

A continuación, se muestran de forma secuencial las pantallas involucradas en el proceso de gestión de cuenta, detallando las interacciones principales y transiciones posibles desde el acceso al menú de configuración hasta la actualización o consulta de datos personales, seguridad y preferencias.

![Artefacto creado en Figma](src/img/cap4/WD/WD_AccountConfiguration)

\newpage


### Mobile Applications Mock-ups.

En esta sección se presentan los mockups de la aplicación RutaKids, los cuales representan visualmente las principales pantallas y funcionalidades diseñadas. Estas interfaces han sido construidas siguiendo principios de diseño centrado en el usuario, diseño inclusivo, accesibilidad y consistencia visual, conforme al Design System definido para este producto digital.


![Inicio de sesión - Artefacto creado en Figma](src/img/cap4/Mockups/SignIn.png)

![Notificaciones - Artefacto creado en Figma](src/img/cap4/Mockups/Notifications.png)

![Mapa en tiempo real - Artefacto creado en Figma](src/img/cap4/Mockups/Details.png)

![Vista interior de la unidad - Artefacto creado en Figma](src/img/cap4/Mockups/LiveInteriorView.png)

![Historial de viajes - Artefacto creado en Figma](src/img/cap4/Mockups/Record.png)

![Gestión de cuenta - Artefacto creado en Figma](src/img/cap4/Mockups/AccountConfiguration.png)


\newpage

### Mobile Applications User Flow Diagrams.
En esta sección se presentan los flujos de usuario diseñados para RutaKids, enfocados en ofrecer a los tutores legales una experiencia clara, segura y eficiente en el monitoreo del transporte escolar de sus hijos/as.
Cada diagrama describe paso a paso cómo el usuario interactúa con la aplicación para cumplir sus objetivos principales, contemplando rutas típicas, alternativas y escenarios excepcionales.
Estos flujos buscan garantizar la transparencia, la facilidad de uso y la confianza en cada interacción, abordando funcionalidades clave como el acceso al sistema, la visualización en tiempo real del trayecto, la recepción de notificaciones, la consulta de historial de viajes y la gestión de la cuenta personal.

**Inicio de Sesión**

- **User Goal:**
  El tutor legal desea acceder a la aplicación móvil para monitorear el transporte escolar de su hijo/a.


![Artefacto creado en Figma](src/img/cap4/UF/SignIn.png)

Este User Flow inicia con la carga del sistema y guía al tutor legal hacia la pantalla de login, donde se permite ingresar sus credenciales o iniciar el proceso de recuperación de contraseña. Se ha considerado un flujo alternativo para usuarios que olvidan su contraseña, así como una condición de éxito que los redirige a la pantalla principal. El proceso incluye interacciones simples y claras, con rutas diferenciadas para escenarios típicos y excepcionales.

\newpage


**Visualización de eventos del recorrido (línea de tiempo)**

- **User Goal:**  
  El tutor legal desea consultar el estado y el avance del recorrido escolar para asegurar el cumplimiento del trayecto.

![Artefacto creado en Figma](src/img/cap4/UF/Details.png)

Este diagrama de flujo de usuario muestra el proceso mediante el cual el tutor legal accede a la línea de tiempo del recorrido escolar actual. Desde la pantalla principal, el usuario selecciona el botón “Detalles”, lo que lo redirige a una vista que presenta los hitos del viaje en orden cronológico.
La línea de tiempo muestra eventos clave como el inicio del trayecto, el abordaje de los estudiantes, el trayecto en curso, y la llegada al colegio.
Para una trazabilidad más detallada, algunos eventos incluyen íconos interactivos que permiten abrir ventanas modales con información adicional, como los nombres de los estudiantes que abordaron y la placa del vehículo. Esta funcionalidad permite al tutor monitorear el cumplimiento del servicio de transporte escolar de forma clara y precisa, fomentando la transparencia y confianza en el proceso.



\newpage

**Notificaciones de eventos**

- **User Goal:**  
  El tutor legal desea recibir alertas sobre momentos importantes del viaje, como el inicio del recorrido o la llegada al punto de encuentro, para mantenerse informado sobre el trayecto de su hijo/a.

![Artefacto creado en Figma](src/img/cap4/UF/Notifications.png)

Este diagrama representa el flujo de usuario para acceder a las notificaciones generadas automáticamente por la aplicación durante el recorrido escolar.
El tutor legal, desde la pantalla principal, puede visualizar un ícono de campana que indica nuevas alertas. Al presionarlo, se accede a una lista cronológica de eventos relevantes, como el inicio del recorrido o la llegada al punto de encuentro.
Cada notificación incluye iconografía, texto descriptivo, hora y fecha. Al seleccionar una notificación específica, se despliega una tarjeta con información extendida del evento.
Esta funcionalidad permite al tutor mantenerse informado en tiempo real, fortaleciendo el acompañamiento del trayecto sin necesidad de interacción directa con el sistema de transporte.


\newpage

**Visualización del trayecto del transporte escolar en mapa en tiempo real**

- **User Goal:**  
  El tutor legal desea visualizar en tiempo real la ruta que sigue la unidad de transporte escolar, con información resumida del conductor, clima y estado del viaje.

![Artefacto creado en Figma](src/img/cap4/UF/LiveMap.png)

Este diagrama de flujo de usuario representa la funcionalidad de monitoreo del trayecto escolar mediante un mapa en vivo.
El tutor legal accede a esta vista a través del botón “Monitoreo” en la barra inferior de navegación.
Al ingresar, se presenta una pantalla que muestra la ubicación actual del vehículo en tiempo real, junto con la ruta estimada desde el punto de origen hasta el destino.
Además, se incluyen datos complementarios como el nombre y placa del conductor, número de pasajeros a bordo, clima actual y tiempo estimado de llegada.
Esta vista se actualiza de manera automática sin necesidad de interacción por parte del usuario, permitiendo un seguimiento continuo y preciso del recorrido escolar.
Esta funcionalidad mejora significativamente la visibilidad y tranquilidad del tutor respecto a la seguridad y puntualidad del transporte.


\newpage

**Visualización en vivo del interior de la unidad**

- **User Goal:**  
  El tutor legal desea observar visualmente la unidad de transporte en tiempo real para verificar las condiciones internas y confirmar que su hijo/a viaja de forma segura.

![Artefacto creado en Figma](src/img/cap4/UF/LiveInteriorView.png)

Este flujo de usuario muestra la funcionalidad que permite al tutor legal acceder a una vista en tiempo real del interior del vehículo escolar.
Desde la pantalla de “Detalles del viaje”, el tutor puede presionar el botón “Visualizar unidad”, lo cual redirige a una vista dedicada donde se transmite un video en vivo del interior del bus.
Esta transmisión permite observar las condiciones internas, incluyendo el comportamiento de los estudiantes y el ambiente dentro de la unidad durante el trayecto.
Además, se muestra la temperatura interna del vehículo en la parte inferior de la pantalla como dato contextual relevante.
Esta funcionalidad tiene como objetivo principal fortalecer la confianza y seguridad del tutor legal, proporcionando una capa adicional de supervisión visual.



\newpage

**Consulta de historial de viajes**

- **User Goal:**  
  El tutor legal desea revisar los viajes anteriores para verificar detalles como la hora de salida y llegada, la ruta recorrida y las condiciones generales del transporte escolar.

![Artefacto creado en Figma](src/img/cap4/UF/Record.png)

Este flujo de usuario describe cómo el tutor legal puede acceder al historial de recorridos realizados por la unidad de transporte escolar.
Desde la pantalla principal, el tutor presiona el ícono de “Historial” ubicado en la barra de navegación inferior.
El sistema redirige a una nueva vista que presenta una lista cronológica de los viajes completados, ordenados desde el más reciente.
Cada tarjeta de viaje muestra información clave como:

- Fecha y hora del trayecto
- Dirección de origen
- Número de pasajeros a bordo
- Condiciones climáticas registradas
- Iconografía del estado del viaje

Esta funcionalidad permite al tutor verificar la puntualidad del servicio, confirmar que el trayecto se ha cumplido adecuadamente y llevar un registro retrospectivo de la actividad escolar de sus hijos/as.

\newpage

**Gestión de cuenta**

- **User Goal:**  
  El tutor legal desea configurar y gestionar sus datos personales, seguridad, privacidad y notificaciones desde su perfil en la aplicación.


![Artefacto creado en Figma](src/img/cap4/UF/AccountConfiguration.png)


Este flujo de usuario representa cómo el tutor legal accede y gestiona su configuración personal dentro de la aplicación RutaKids.
Desde cualquier pantalla, el tutor puede ingresar a la sección de cuenta ya sea presionando el ícono de perfil en la parte superior o a través del botón “Cuenta” en la barra inferior de navegación.
En la vista principal de cuenta, se le presentan cuatro opciones principales:

- **Información personal:** Permite visualizar y editar nombre, número telefónico y correo electrónico.
- **Seguridad:** Ofrece opciones para cambiar la contraseña, activar la verificación en dos pasos y contactar al soporte.
- **Protección de datos:** Muestra los términos y condiciones, políticas de privacidad y configuraciones sobre protección de datos personales.
- **Notificaciones:** El usuario puede activar o desactivar distintos tipos de alertas, como aquellas relacionadas con el transporte, el mapa, el seguimiento del viaje y otros servicios.

Cada sección está diseñada para brindar al tutor control total sobre su perfil y preferencias dentro de la app, promoviendo una experiencia personalizada, segura y transparente.


\newpage


## Mobile Applications Prototyping.

Esta sección presenta los prototipos interactivos desarrollados para las aplicaciones móviles, los cuales permiten simular la experiencia de usuario en condiciones reales de navegación, alineados con los User Flow Diagrams previamente definidos. Los prototipos contemplan el comportamiento esperado de la interfaz ante acciones como toques, desplazamientos y navegación entre pantallas, y fueron diseñados utilizando Figma como herramienta principal de diseño y simulación.

**Justificación de decisiones de diseño e interacción**

El diseño de interacción responde a una arquitectura de información centrada en el usuario, basada en jerarquías claras y flujos de navegación predecibles. Para ello se han definido rutas esperadas (happy paths) que guían al tutor legal desde el acceso inicial a la aplicación hasta funcionalidades clave como el monitoreo en tiempo real, la recepción de notificaciones o la gestión de cuenta personal.

El sistema de navegación utiliza una barra inferior persistente, con íconos universalmente reconocibles, que agrupa las secciones principales: Inicio, Monitoreo, Historial y Cuenta. Esta estructura se eligió por su efectividad en dispositivos móviles, permitiendo que el usuario navegue sin esfuerzo entre vistas relacionadas sin necesidad de regresar a menús superiores.

En cuanto a las interacciones, se ha priorizado una lógica de flujo lineal pero flexible, donde cada acción permite al usuario avanzar o retroceder sin pérdida de contexto. Los botones de acción primaria mantienen una jerarquía visual constante, con estilos y colores definidos por el Design System para asegurar accesibilidad y reconocimiento visual. Se usaron estilos consistentes de tipografía y espaciado en todos los mockups, siguiendo criterios de diseño inclusivo y contraste adecuado para la lectura en pantalla.

**Consistencia y adaptabilidad**

A pesar de que los prototipos fueron desarrollados inicialmente con frames de iOS para facilitar el testeo visual, todas las decisiones fueron tomadas considerando el desarrollo futuro con Flutter como framework multiplataforma. Esto asegura que los elementos visuales, tamaños de fuente, márgenes y estilos de interacción son adaptables a sistemas operativos Android, y que cualquier ajuste de microinteracción puede realizarse posteriormente sin romper la coherencia de experiencia.
Las diferencias menores en los tamaños de botones o alineaciones responden a las guías específicas de cada sistema operativo (Apple Human Interface Guidelines y Material Design), pero sin comprometer la armonía visual ni la funcionalidad entre plataformas.


### Android Mobile Applications Prototyping.

La versión prototipada corresponde a la arquitectura funcional de Android, replicando los mismos flujos de navegación definidos para iOS.
Gracias al enfoque cross-platform con Flutter, las decisiones de interacción son consistentes entre sistemas.


**Ver prototipo interactivo (Figma):** https://www.figma.com/proto/eciWGdnbz2vbcafpC3ry61/RutaKids?node-id=1-191&t=Q43WuZLUjqqKj29U-1&scaling=scale-down&content-scaling=fixed&page-id=0%3A1&starting-point-node-id=1%3A191  

**Ver demo en Microsoft Stream - Min(00:33):** https://upcedupe-my.sharepoint.com/:v:/g/personal/u202210059_upc_edu_pe/EWNyaDk6mgdMlrmkd3YCekQBkWfpMUBC7oBkGaqmv3HQIA?e=ZCJBW6&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D 



### iOS Mobile Applications Prototyping.

La interfaz se prototipó inicialmente para iOS siguiendo las guías de diseño de Apple (Human Interface Guidelines), aplicando principios de accesibilidad y navegación móvil.


**Ver prototipo interactivo (Figma):** https://www.figma.com/proto/eciWGdnbz2vbcafpC3ry61/RutaKids?node-id=5-1336&t=xAeh2weCXXUvbcOx-1&scaling=scale-down&content-scaling=fixed&page-id=5%3A1185&starting-point-node-id=5%3A1336 

**Ver demo en Microsoft Stream - Min(01:57):** https://upcedupe-my.sharepoint.com/:v:/g/personal/u202210059_upc_edu_pe/EWNyaDk6mgdMlrmkd3YCekQBkWfpMUBC7oBkGaqmv3HQIA?e=ZCJBW6&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D 




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

\newpage

**Navegación y funcionalidades complementarias**

![Dashboard general - Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/dashboard.png)

![Notificaciones - Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/notifications.png)

![Preguntas frecuentes - Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/faq.png)

![Política de privacidad - Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/privacy_policy.png)

![Cerrar sesión - Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/log_out.png)

![Terminos y Condiciones - Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/terms.png)

\newpage

**Gestión de estudiantes**

![Crear estudiante - Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/create_student.png)

![Lista de estudiantes - Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/students_list.png)

![Tarjetas de estudiantes - Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/students_cards.png)

\newpage

**Gestión de movilidades y rutas escolares**

![Crear movilidad escolar - Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/create_school_trans.png)

![Listado de movilidades - Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/school_trans_list.png)

![Crear ruta escolar - Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/create_school_routes.png)

![Listado de rutas escolares - Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/school_routes_list.png)


\newpage

### *Web Applications Wireflow Diagrams.*

Los wireflows representan visualmente la navegación entre las diferentes pantallas de la aplicación RutaKids, permitiendo comprender la lógica de interacción del usuario antes del desarrollo de las interfaces finales. Estos diagramas combinan los wireframes de cada vista con las conexiones funcionales entre ellas, trazando el recorrido esperado que realizarán los usuarios al interactuar con el sistema. La construcción de estos wireflows se realizó en **Uizard**, destacando la navegación entre módulos clave como autenticación, gestión de estudiantes, movilidades, rutas escolares y configuraciones. Este enfoque permite validar anticipadamente la usabilidad, fluidez y estructura lógica de la experiencia de usuario en RutaKids.


**Inicio de sesión y autenticación**

![Inicio de sesión – Artefacto creado en Uizard](src/img/cap4/rutakids_wireflows/login.jpeg)

Este wireflow representa el flujo completo de autenticación de usuarios en la aplicación. Desde la pantalla de inicio de sesión se habilita la navegación hacia funciones clave como la recuperación de contraseña, el restablecimiento de credenciales y el acceso al dashboard principal en caso de inicio exitoso. También se contempla el proceso de cierre de sesión. El objetivo es garantizar un acceso seguro y fluido, permitiendo que directivos, padres o personal autorizado ingresen a la plataforma con la menor fricción posible.

\newpage

**Gestión de estudiantes**

![Gestión de estudiantes – Artefacto creado en Uizard](src/img/cap4/rutakids_wireflows/students.jpeg)

Este wireflow muestra la navegación entre las secciones relacionadas a los estudiantes: listado general, vista en tarjetas individuales y el formulario de creación de nuevo alumno. Cada flujo parte desde el dashboard y está pensado para facilitar la gestión visual y estructurada de los alumnos registrados en el sistema, permitiendo búsquedas ágiles, navegación fluida entre vistas y registro eficiente de nuevos estudiantes.

**Gestión de movilidades escolares**

![Gestión de movilidades – Artefacto creado en Uizard](src/img/cap4/rutakids_wireflows/school_trans.jpeg)

Este flujo refleja la administración de los vehículos escolares asignados a cada ruta. A partir del dashboard, se puede acceder a la lista de movilidades registradas y a la vista para crear nuevas, incluyendo datos como matrícula, chofer y características del vehículo. El wireflow evidencia cómo el sistema facilita un control centralizado de la flota activa, promoviendo orden y eficiencia en la planificación logística del transporte.

\newpage

**Gestión de rutas escolares**

![Gestión de rutas escolares – Artefacto creado en Uizard](src/img/cap4/rutakids_wireflows/school_routes.jpeg)

Este wireflow detalla la navegación entre las vistas de lista y creación de rutas escolares. A partir del dashboard, se accede a las rutas activas con posibilidad de registrar nuevas, asignar alumnos y vincular una movilidad. La visualización jerárquica de esta sección permite una asignación clara y rastreable, asegurando cobertura y trazabilidad en cada recorrido escolar.

\newpage

**Configuración y secciones administrativas**

![Configuraciones y políticas – Artefacto creado en Uizard](src/img/cap4/rutakids_wireflows/settings.jpeg)

Aquí se detallan los flujos relacionados con la configuración personal del usuario, incluyendo el cambio de contraseña, política de privacidad y términos y condiciones. Todas las rutas se originan en el dashboard y apuntan a mejorar la transparencia del sistema, ofreciendo acceso fácil a las políticas institucionales y a la personalización de la cuenta, mejorando la confianza del usuario.

\newpage

**Otras funcionalidades complementarias**

![Otras funcionalidades – Artefacto creado en Uizard](src/img/cap4/rutakids_wireflows/others.jpeg)

Este wireflow agrupa funciones de soporte como las notificaciones y la sección de preguntas frecuentes (FAQ). Estos apartados permiten mejorar la experiencia del usuario mediante respuestas rápidas y una comunicación efectiva. La navegación parte desde el dashboard y está diseñada para no interferir con las tareas principales, pero sí ofrecer valor añadido al sistema en términos de asistencia y seguimiento.

\newpage

### *Web Applications Mock-ups.*

**Autenticación y recuperación de acceso**

![Pantalla de inicio de sesión - Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/sign_in.png)

![Recuperación de contraseña - Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/forgot_password.png)

![Reinicio de contraseña - Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/reset_password.png)

![Cambio de contraseña - Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/change_password.png)

\newpage

**Navegación y funcionalidades complementarias**

![Dashboard general - Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/dashboard.png)

![Notificaciones - Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/notifications.png)

![Preguntas frecuentes - Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/faq.png)

![Política de privacidad - Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/privacy_policy.png)

![Cerrar sesión - Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/log_out.png)

![Terminos y Condiciones - Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/terms.png)

\newpage

**Gestión de estudiantes**

![Crear estudiante - Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/create_student.png)

![Lista de estudiantes - Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/students_list.png)

![Tarjetas de estudiantes - Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/students_cards.png)

\newpage

**Gestión de movilidades y rutas escolares**

![Crear movilidad escolar - Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/create_school_trans.png)

![Listado de movilidades - Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/school_trans_list.png)

![Crear ruta escolar - Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/create_school_routes.png)

![Listado de rutas escolares - Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/school_routes_list.png)

\newpage

### *Web Applications User Flow Diagrams.*

Los wireflows representan visualmente la navegación entre las diferentes pantallas de la aplicación RutaKids, permitiendo comprender la lógica de interacción del usuario antes del desarrollo de las interfaces finales. Estos diagramas combinan los wireframes de cada vista con las conexiones funcionales entre ellas, trazando el recorrido esperado que realizarán los usuarios al interactuar con el sistema. La construcción de estos wireflows se realizó en **Uizard**, destacando la navegación entre módulos clave como autenticación, gestión de estudiantes, movilidades, rutas escolares y configuraciones. Este enfoque permite validar anticipadamente la usabilidad, fluidez y estructura lógica de la experiencia de usuario en RutaKids.

**Inicio de sesión y autenticación**

![Inicio de sesión – Artefacto creado en Uizard](src/img/cap4/rutakids_userflows/login.jpeg)

Este wireflow representa el flujo completo de autenticación de usuarios en la aplicación. Desde la pantalla de inicio de sesión se habilita la navegación hacia funciones clave como la recuperación de contraseña, el restablecimiento de credenciales y el acceso al dashboard principal en caso de inicio exitoso. También se contempla el proceso de cierre de sesión. El objetivo es garantizar un acceso seguro y fluido, permitiendo que directivos, padres o personal autorizado ingresen a la plataforma con la menor fricción posible.

\newpage

**Gestión de estudiantes**

![Gestión de estudiantes – Artefacto creado en Uizard](src/img/cap4/rutakids_userflows/students.jpeg)

Este wireflow muestra la navegación entre las secciones relacionadas a los estudiantes: listado general, vista en tarjetas individuales y el formulario de creación de nuevo alumno. Cada flujo parte desde el dashboard y está pensado para facilitar la gestión visual y estructurada de los alumnos registrados en el sistema, permitiendo búsquedas ágiles, navegación fluida entre vistas y registro eficiente de nuevos estudiantes.

**Gestión de movilidades escolares**

![Gestión de movilidades – Artefacto creado en Uizard](src/img/cap4/rutakids_userflows/school_trans.jpeg)

Este flujo refleja la administración de los vehículos escolares asignados a cada ruta. A partir del dashboard, se puede acceder a la lista de movilidades registradas y a la vista para crear nuevas, incluyendo datos como matrícula, chofer y características del vehículo. El wireflow evidencia cómo el sistema facilita un control centralizado de la flota activa, promoviendo orden y eficiencia en la planificación logística del transporte.

\newpage

**Gestión de rutas escolares**

![Gestión de rutas escolares – Artefacto creado en Uizard](src/img/cap4/rutakids_userflows/school_routes.jpeg)

Este wireflow detalla la navegación entre las vistas de lista y creación de rutas escolares. A partir del dashboard, se accede a las rutas activas con posibilidad de registrar nuevas, asignar alumnos y vincular una movilidad. La visualización jerárquica de esta sección permite una asignación clara y rastreable, asegurando cobertura y trazabilidad en cada recorrido escolar.

\newpage

**Configuración y secciones administrativas**

![Configuraciones y políticas – Artefacto creado en Uizard](src/img/cap4/rutakids_userflows/settings.jpeg)

Aquí se detallan los flujos relacionados con la configuración personal del usuario, incluyendo el cambio de contraseña, política de privacidad y términos y condiciones. Todas las rutas se originan en el dashboard y apuntan a mejorar la transparencia del sistema, ofreciendo acceso fácil a las políticas institucionales y a la personalización de la cuenta, mejorando la confianza del usuario.

\newpage

**Otras funcionalidades complementarias**

![Otras funcionalidades – Artefacto creado en Uizard](src/img/cap4/rutakids_userflows/others.jpeg)

Este wireflow agrupa funciones de soporte como las notificaciones y la sección de preguntas frecuentes (FAQ). Estos apartados permiten mejorar la experiencia del usuario mediante respuestas rápidas y una comunicación efectiva. La navegación parte desde el dashboard y está diseñada para no interferir con las tareas principales, pero sí ofrecer valor añadido al sistema en términos de asistencia y seguimiento.

\newpage

## *Web Applications Prototyping.*

::: warn
Para visualizar el video del prototipo de la aplicación,  haga click en la [URL](https://upcedupe-my.sharepoint.com/:v:/g/personal/u202210059_upc_edu_pe/EWNyaDk6mgdMlrmkd3YCekQBkWfpMUBC7oBkGaqmv3HQIA?e=ZCJBW6&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D 
)
:::


\newpage

## Domain-Driven Software Architecture.

En esta sección se describe la arquitectura impulsada por el dominio para **CodeMinds**, nuestra solución de autenticación IoT enfocada en el transporte escolar seguro. Utilizamos principios de *Domain-Driven Design* (DDD) para estructurar los componentes de software de manera alineada con las necesidades del negocio, garantizando escalabilidad, robustez y claridad en la separación de responsabilidades.

\newpage

### Software Architecture Context Diagram.

El Diagrama de Contexto muestra cómo **CodeMinds** se integra en su ecosistema. Describe a alto nivel los actores externos (como padres, colegios, conductores y autoridades escolares) y los sistemas externos (por ejemplo, bases de datos escolares, plataformas de mensajería y servidores de autenticación) que interactúan con nuestra plataforma. También identifica los flujos principales de información entre estos actores y el sistema central de **CodeMinds**.

![CodeMinds Software Context Diagram](src/img/cap4/structurizr-83808-SystemContext-001.png)

\newpage

### Software Architecture Container Diagrams.

El Diagrama de Contenedores de **CodeMinds** descompone el sistema en contenedores principales: aplicaciones móviles, API gateway, servicios backend, bases de datos, y dispositivos IoT de escaneo RFID/NFC instalados en autobuses escolares. Este diagrama detalla cómo cada contenedor contribuye a funcionalidades específicas, como la autenticación de estudiantes, la generación de reportes, las notificaciones a padres en tiempo real y la administración del sistema desde una consola web.

![CodeMinds Software Container Diagram](src/img/cap4/structurizr-83808-Container-001.png)

\newpage

### Software Architecture Components Diagrams.

En esta sección presentamos el Diagrama de Componentes de **CodeMinds**, que profundizan en la estructura interna de cada contenedor principal. Cada componente se detalla mostrando su responsabilidad y las interacciones internas y externas. Por ejemplo, dentro del servicio de autenticación, mostramos componentes como el Módulo de Verificación de Identidad, el Módulo de Gestión de Horarios y Rutas, y el Módulo de Alertas en Tiempo Real, explicando cómo colaboran entre sí para garantizar la seguridad y el seguimiento de los escolares.

![CodeMinds Software Components Diagram](src/img/cap4/structurizr-83808-Component-001.png)

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

\newpage

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

# Bibliografia
