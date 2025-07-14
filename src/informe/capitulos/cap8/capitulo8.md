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

# Capítulo VIII: Experiment-Driven Development

En el presente capítulo se expone el enfoque de desarrollo basado en experimentación, conocido como Experiment-Driven Development (EDD), aplicado durante la etapa de validación y refinamiento del sistema RutaKids. Esta metodología propone la integración sistemática de experimentos controlados dentro del proceso de desarrollo, con el objetivo de tomar decisiones fundamentadas en evidencia empírica derivada del comportamiento real de los usuarios.

A diferencia de enfoques tradicionales centrados exclusivamente en la especificación de requerimientos, el EDD parte de la premisa de que las hipótesis sobre funcionalidad, diseño o experiencia de usuario deben ser puestas a prueba mediante instrumentos experimentales como entrevistas, pruebas A/B, métricas de uso, prototipos interactivos y auditorías cruzadas. Cada ciclo experimental permite validar (o refutar) supuestos, detectar fricciones, y obtener información accionable para guiar iterativamente las mejoras del producto.

En el contexto de este proyecto, se diseñaron y ejecutaron una serie de experimentos orientados a evaluar la eficacia de la solución propuesta en términos de usabilidad, comprensión del flujo de tareas, satisfacción del usuario final y claridad en la propuesta de valor. Estos experimentos fueron diseñados con base en principios de investigación orientados al diseño (Design Research), combinando técnicas cualitativas (entrevistas, observación directa, análisis heurístico) con indicadores cuantitativos recolectados durante sesiones de prueba controladas.

\newpage

## Experiment Planning

La planificación de los experimentos representa una fase crítica dentro del enfoque de Experiment-Driven Development, ya que permite establecer de manera estructurada los objetivos, hipótesis y líneas de acción que guiarán la evaluación empírica de la solución tecnológica en desarrollo. En esta etapa, se parte de una comprensión profunda del estado actual del sistema (As-Is) y de la identificación sistemática de sus principales limitaciones desde la perspectiva de los usuarios y actores involucrados. A partir de ello, se definen los objetivos de mejora y se delimitan los focos específicos que serán abordados mediante instrumentos de validación.

En el caso de RutaKids, la planificación experimental se construyó sobre la base de múltiples fuentes de información recolectadas durante fases previas del proyecto, incluyendo entrevistas con usuarios, auditorías heurísticas, observación directa y retroalimentación recibida durante sesiones de demostración funcional. Estas fuentes permitieron identificar un conjunto de fricciones que, aunque no invalidan la propuesta de valor del sistema, sí afectan su percepción de utilidad, su usabilidad efectiva y su diferenciación frente a otras soluciones existentes en el mercado.

Entre los principales problemas detectados se encuentra una baja percepción de seguridad por parte de los padres de familia, quienes manifestaron incertidumbre respecto a la precisión y confiabilidad del seguimiento en tiempo real de las unidades escolares. Aunque la funcionalidad de geolocalización se encuentra implementada, los retrasos en la actualización de la información, así como una representación limitada del recorrido, generan dudas y ansiedad en los usuarios. Por ello, uno de los focos experimentales más importantes es evaluar si una visualización más detallada, clara y en tiempo real puede aumentar la confianza del usuario final en el sistema.

Otro punto crítico está relacionado con las notificaciones automáticas enviadas por la aplicación móvil. Se identificó que, si bien el sistema genera alertas básicas, estas no son lo suficientemente personalizadas ni contextuales. La falta de información específica (por ejemplo, si un estudiante ha subido o bajado del bus, o si hay un retraso significativo en la ruta) limita la percepción de control por parte de los padres. En este sentido, los experimentos se diseñarán para validar si la incorporación de notificaciones enriquecidas y adaptadas a eventos relevantes mejora la experiencia y la percepción de valor por parte del usuario.


\newpage

### As-Is Summary.

Actualmente, la plataforma *RutaKids* ofrece una aplicación móvil para padres de familia y una plataforma web para personal directivo de instituciones educativas. Su funcionalidad incluye seguimiento en tiempo real de rutas escolares, envío de notificaciones, gestión de incidencias y reportes, así como la integración con sensores IoT y asignación automática de unidades.

No obstante, se han identificado diversas oportunidades de mejora. Algunos usuarios reportan falta de personalización en notificaciones, limitaciones en la visualización de información crítica, ausencia de integración tecnológica en tiempo real, y errores logísticos persistentes.

**Problemas identificados:**

* **Percepción de seguridad:** Los padres no siempre se sienten tranquilos debido a la falta de transparencia del recorrido en tiempo real.  
* **Falta de control e información:** Las notificaciones no siempre son relevantes ni entregadas de manera personalizada.  
* **Eficiencia operativa limitada:** Los administradores enfrentan tiempos prolongados para gestionar incidencias.  
* **Valor percibido bajo:** El sistema no se percibe como innovador por parte de los administradores sin la integración de sensores IoT.  
* **Errores logísticos frecuentes:** La asignación manual de rutas genera redundancias y errores evitables.

**Objetivos de mejora:**

* Aumentar la percepción de seguridad mediante la visualización en tiempo real.  
* Incrementar la satisfacción y control de los padres mediante notificaciones personalizadas.  
* Mejorar la eficiencia administrativa con un panel centralizado.  
* Reforzar el valor percibido del sistema con sensores IoT.  
* Reducir errores operativos con asignación automática de rutas y unidades.

\newpage

### Raw Material: Assumptions, Knowledge Gaps, Ideas, Claims.

**Assumptions:**

* Los padres valoran herramientas que les permitan saber en tiempo real la ubicación del bus escolar.  
* Las notificaciones automáticas y personalizadas generan tranquilidad y control.  
* Los administradores están dispuestos a adoptar soluciones basadas en IoT si perciben utilidad en la toma de decisiones.  
* La automatización de rutas disminuirá errores operativos.  
* El acceso a reportes claros y exportables facilita decisiones rápidas y precisas.

**Knowledge Gaps:**

* No se ha determinado el porcentaje exacto de padres que consideran útil la visualización en tiempo real.  
* Se desconoce qué tipo de notificaciones son más efectivas para los padres.  
* Faltan datos sobre el impacto operativo del panel centralizado.  
* Se necesita evaluar si los administradores valoran efectivamente la integración IoT.  
* No se ha cuantificado con precisión la reducción de errores al aplicar asignación automática.

**Ideas:**

* Realizar encuestas post-implementación sobre percepción de seguridad y control.  
* Implementar pruebas A/B para medir impacto de funcionalidades específicas.  
* Medir tiempos de respuesta con y sin panel centralizado.  
* Evaluar diferencias entre reportes con y sin integración IoT.  
* Recoger logs de errores logísticos antes y después de automatizar asignaciones.

**Claims:**

* La visualización en tiempo real reduce ansiedad parental y mejora la percepción de seguridad.  
* Las notificaciones personalizadas aumentan satisfacción y percepción de control.  
* El panel centralizado mejora eficiencia operativa de forma significativa.  
* La integración de sensores IoT eleva la percepción de valor tecnológico.  
* La asignación automática de rutas reduce en gran medida los errores logísticos.

\newpage

### Experiment-Ready Questions.

\begin{longtable}{|p{2.5cm}|p{2.5cm}|p{2cm}|p{2cm}|p{2cm}|p{2cm}|}
\hline
\textbf{Pregunta} & \textbf{Confidence} & \textbf{Risk} & \textbf{Impact} & \textbf{Interest} & \textbf{Total Score} \\
\hline
\endfirsthead

\hline
\textbf{Pregunta} & \textbf{Confidence} & \textbf{Risk} & \textbf{Impact} & \textbf{Interest} & \textbf{Total Score} \\
\hline
\endhead

¿La visualización en tiempo real del recorrido mejora la percepción de seguridad de los padres? & 
8 – Se basa en una necesidad emocional clara y recurrente reportada por los padres. & 
3 – Riesgo medio por la complejidad técnica de integrar correctamente el GPS. & 
8 – Tiene un impacto directo en la confianza y tranquilidad de los usuarios. & 
7 – Hay un interés latente por saber dónde están sus hijos en todo momento. & 
26 \\
\hline

¿Las notificaciones personalizadas aumentan la satisfacción y percepción de control? & 
9 – Altamente probable según experiencias de apps similares. & 
2 – Bajo riesgo, ya que se trata de un feature ampliamente probado. & 
9 – Mejora la experiencia del usuario y su sentido de control. & 
8 – Muy relevante para usuarios que desean estar informados en tiempo real. & 
28 \\
\hline

¿Un panel centralizado reduce el tiempo promedio en la gestión de incidencias? & 
8 – Los beneficios de centralizar interfaces están bien documentados. & 
3 – Riesgo medio por el rediseño necesario en backend y flujos. & 
9 – Tiene un alto impacto operativo para instituciones. & 
7 – Es funcionalmente atractivo para el segmento administrador. & 
27 \\
\hline

¿La integración de sensores IoT mejora la percepción de valor del sistema? & 
7 – Existe evidencia en otros sectores de que IoT eleva la percepción de modernidad. & 
3 – Riesgo medio por la integración técnica y costos. & 
8 – El valor percibido del sistema puede ser un diferenciador competitivo. & 
6 – Tiene interés entre usuarios con perfil técnico o institucional. & 
24 \\
\hline

¿La asignación automática de rutas disminuye errores logísticos? & 
9 – Se basa en lógica automatizada ya validada en múltiples industrias. & 
4 – Riesgo medio-alto por los errores posibles si la lógica no se ajusta bien. & 
10 – Gran impacto al reducir trabajo manual y errores frecuentes. & 
8 – Alta expectativa por parte de los usuarios administrativos. & 
31 \\
\hline

\end{longtable}

\newpage

### Question Backlog.

\begin{longtable}{|p{4cm}|p{10cm}|}
\hline
\textbf{Prioridad} & \textbf{Pregunta} \\
\hline
\endfirsthead

\hline
\textbf{Prioridad} & \textbf{Pregunta} \\
\hline
\endhead

1 & ¿Las notificaciones personalizadas aumentan la satisfacción y percepción de control? \\
\hline
2 & ¿La visualización en tiempo real del recorrido mejora la percepción de seguridad de los padres? \\
\hline
3 & ¿Un panel centralizado reduce el tiempo promedio en la gestión de incidencias? \\
\hline
3 & ¿La integración de sensores IoT mejora la percepción de valor del sistema? \\
\hline
5 & ¿La asignación automática de rutas disminuye errores logísticos? \\
\hline
\end{longtable}


La tabla presenta la priorización de las preguntas clave que guían los experimentos de validación en la plataforma *RutaKids*. Estas prioridades fueron asignadas considerando una combinación de factores como impacto, riesgo, interés del usuario y confianza en la hipótesis. Las preguntas con mayor prioridad reflejan oportunidades estratégicas para mejorar significativamente la experiencia del usuario y el valor percibido del sistema, y por tanto deben ser abordadas con mayor urgencia en las fases de prototipado y prueba.

\newpage

### Experiment Cards.

Cada bloque resume la planificación experimental de hipótesis clave relacionadas con la mejora de la plataforma *RutaKids*. Las preguntas están alineadas con necesidades reales de los usuarios, y se acompañan de una justificación estratégica (Why), una acción concreta a implementar (What) y una hipótesis medible (Hypothesis). Esta estructura permite validar rápidamente el valor de las funcionalidades antes de su desarrollo completo, minimizando riesgos y maximizando impacto.

\vspace{1cm}

\begin{longtable}{|p{4cm}|p{10cm}|}
\hline
\textbf{Pregunta} & ¿La visualización en tiempo real del recorrido mejora la percepción de seguridad de los padres? \\
\hline
\textbf{Why} & Permitir a los padres ver la ubicación en tiempo real genera confianza y reduce ansiedad. \\
\hline
\textbf{What} & Implementar un módulo GPS en la app móvil. \\
\hline
\textbf{Hypothesis} & Al menos el 70\% de padres reportará sentirse más seguros. \\
\hline
\end{longtable}

\begin{longtable}{|p{4cm}|p{10cm}|}
\hline
\textbf{Pregunta} & ¿Las notificaciones personalizadas aumentan la satisfacción y percepción de control? \\
\hline
\textbf{Why} & Entregar alertas personalizadas permite reaccionar con mayor anticipación ante eventos. \\
\hline
\textbf{What} & Integrar un sistema de notificaciones con filtros configurables. \\
\hline
\textbf{Hypothesis} & El 60\% de los usuarios reportará mayor satisfacción y percepción de control. \\
\hline
\end{longtable}

\begin{longtable}{|p{4cm}|p{10cm}|}
\hline
\textbf{Pregunta} & ¿Un panel centralizado reduce el tiempo promedio en la gestión de incidencias? \\
\hline
\textbf{Why} & Centralizar acciones reduce pasos, errores y tiempos de reacción. \\
\hline
\textbf{What} & Crear un dashboard único para gestionar rutas, alertas y unidades. \\
\hline
\textbf{Hypothesis} & Los tiempos promedio de gestión de incidencias se reducirán en al menos un 40\%. \\
\hline
\end{longtable}

\begin{longtable}{|p{4cm}|p{10cm}|}
\hline
\textbf{Pregunta} & ¿La integración de sensores IoT mejora la percepción de valor del sistema? \\
\hline
\textbf{Why} & Sensores como GPS, RFID o temperatura refuerzan la imagen de tecnología avanzada. \\
\hline
\textbf{What} & Habilitar panel IoT con indicadores en tiempo real. \\
\hline
\textbf{Hypothesis} & El 80\% de los administradores calificará el sistema como más avanzado. \\
\hline
\end{longtable}

\begin{longtable}{|p{4cm}|p{10cm}|}
\hline
\textbf{Pregunta} & ¿La asignación automática de rutas disminuye errores logísticos? \\
\hline
\textbf{Why} & Automatizar tareas elimina la dependencia de procesos manuales propensos a errores. \\
\hline
\textbf{What} & Implementar lógica de asignación por zona y capacidad de unidad. \\
\hline
\textbf{Hypothesis} & Se logrará una reducción de errores operativos de al menos un 50\%. \\
\hline
\end{longtable}


\newpage

## Experiment Design

Con el objetivo de validar las hipótesis definidas a partir del proceso de Lean UX, se diseñó una serie de experimentos controlados que permitirán medir el impacto de las funcionalidades clave sobre la experiencia del usuario y la eficiencia operativa del sistema. Esta fase considera los elementos fundamentales del diseño experimental, incluyendo las variables a evaluar, las condiciones de prueba, las métricas esperadas, y los métodos de análisis que serán empleados. A través de esta estrategia estructurada se busca obtener evidencia empírica que respalde —o refute— las suposiciones del equipo, permitiendo una toma de decisiones informada para el desarrollo futuro del producto.

\vspace{1cm}

### Hypotheses.

Las hipótesis planteadas representan afirmaciones verificables construidas a partir de observaciones previas, entrevistas con usuarios y análisis del contexto operativo. Estas buscan evaluar si ciertas funcionalidades propuestas —como notificaciones automáticas, visualización en tiempo real, dashboards centralizados o sistemas de asignación automática— generan un impacto positivo en la percepción de valor, la satisfacción de los usuarios y la eficiencia del servicio. A continuación, se detallan las hipótesis priorizadas, cada una acompañada de su justificación, propuesta funcional y resultado esperado.

A continuación se detallan las hipótesis planteadas para el diseño experimental de RutaKids. Cada hipótesis parte de una creencia validada en entrevistas y está orientada a ser verificada mediante pruebas controladas con usuarios reales. Las tablas incluyen la pregunta central, la creencia (belief), la hipótesis planteada y la hipótesis nula correspondiente.

\vspace{1cm}

- **Hipótesis 1 - Visualización en tiempo real y percepción de seguridad**

\begin{longtable}{|p{4cm}|p{10cm}|}
\hline
\textbf{Question} & ¿Cómo influye la visualización en tiempo real del recorrido de las unidades escolares en la percepción de seguridad y confianza de los padres de familia? \\
\hline
\textbf{Belief} & Creemos que brindar a los padres la capacidad de visualizar en tiempo real la ubicación de la unidad de transporte escolar generará mayor tranquilidad, reduciendo la ansiedad y mejorando la percepción de seguridad. \\
\hline
\textbf{Hypothesis} & Si se implementa un sistema de visualización en tiempo real del recorrido de las unidades escolares, al menos el 70\% de los padres indicará que se siente más seguro y confiado respecto al transporte de sus hijos. \\
\hline
\textbf{Null Hypothesis} & La visualización en tiempo real del recorrido de las unidades escolares no tiene un impacto significativo en la percepción de seguridad ni en la confianza de los padres de familia. \\
\hline
\end{longtable}

- **Hipótesis 2 - Notificaciones personalizadas y percepción de control**

\begin{longtable}{|p{4cm}|p{10cm}|}
\hline
\textbf{Question} & ¿Cómo impacta la recepción de notificaciones personalizadas sobre desvíos o retrasos en la satisfacción y percepción de control de los padres? \\
\hline
\textbf{Belief} & Creemos que recibir notificaciones automáticas y personalizadas sobre eventos relevantes como desvíos o retrasos mejora la satisfacción de los padres y les brinda una sensación de control sobre la situación. \\
\hline
\textbf{Hypothesis} & Si se implementa un sistema de notificaciones personalizadas ante desvíos o retrasos, al menos el 60\% de los padres reportará una mayor satisfacción y percepción de control durante el uso del servicio. \\
\hline
\textbf{Null Hypothesis} & La recepción de notificaciones personalizadas sobre desvíos o retrasos no influye significativamente en la satisfacción ni en la percepción de control de los padres. \\
\hline
\end{longtable}

- **Hipótesis 3 - Panel centralizado y eficiencia operativa**

\begin{longtable}{|p{4cm}|p{10cm}|}
\hline
\textbf{Question} & ¿Cómo afecta la implementación de un panel administrativo centralizado en la eficiencia operativa de las instituciones educativas? \\
\hline
\textbf{Belief} & Creemos que un panel de control unificado para la gestión de rutas, estudiantes, unidades y alertas incrementa la eficiencia operativa y reduce el tiempo de respuesta ante incidencias. \\
\hline
\textbf{Hypothesis} & Si se implementa un panel administrativo centralizado, los administradores reducirán en al menos 40\% el tiempo promedio de gestión de incidencias operativas frente al sistema anterior sin unificación. \\
\hline
\textbf{Null Hypothesis} & La implementación de un panel administrativo centralizado no tiene un impacto significativo en la eficiencia operativa de las instituciones educativas. \\
\hline
\end{longtable}

- **Hipótesis 4 - Integración de IoT y percepción de valor**

\begin{longtable}{|p{4cm}|p{10cm}|}
\hline
\textbf{Question} & ¿Cómo influye la integración de sensores IoT en la percepción de valor del sistema por parte de los administradores educativos? \\
\hline
\textbf{Belief} & Creemos que al integrar sensores como GPS, temperatura o RFID, los administradores percibirán a RutaKids como una herramienta tecnológica avanzada y confiable. \\
\hline
\textbf{Hypothesis} & Si se integran sensores IoT para el monitoreo en tiempo real, el 80\% de los administradores calificará el sistema como tecnológicamente avanzado y útil para la toma de decisiones. \\
\hline
\textbf{Null Hypothesis} & La integración de sensores IoT no tiene un impacto significativo en la percepción de valor del sistema por parte de los administradores educativos. \\
\hline
\end{longtable}

- **Hipótesis 5 - Asignación automática y errores operativos**

\begin{longtable}{|p{4cm}|p{10cm}|}
\hline
\textbf{Question} & ¿Cómo influye la asignación automática de rutas y unidades en la reducción de errores operativos durante el transporte escolar? \\
\hline
\textbf{Belief} & Creemos que la automatización en la asignación de rutas y vehículos disminuirá la carga operativa manual y reducirá errores en la logística diaria del transporte escolar. \\
\hline
\textbf{Hypothesis} & Si se implementa una función de asignación automática de rutas y unidades, los errores operativos disminuirán al menos en un 50\%, medido por el número de correcciones manuales registradas por los administradores en el sistema. \\
\hline
\textbf{Null Hypothesis} & La asignación automática de rutas y unidades no tiene un impacto significativo en la reducción de errores operativos durante el transporte escolar. \\
\hline
\end{longtable}

- **Hipótesis 6 - Reportes clave y toma de decisiones**

\begin{longtable}{|p{4cm}|p{10cm}|}
\hline
\textbf{Question} & ¿Cómo impacta la visualización de reportes e indicadores clave en la toma de decisiones de los administradores educativos? \\
\hline
\textbf{Belief} & Creemos que brindar acceso a reportes e indicadores clave sobre rutas, asistencia y alertas permitirá a los administradores tomar decisiones más informadas y rápidas. \\
\hline
\textbf{Hypothesis} & Si se habilita un módulo de reportes e indicadores clave, al menos el 70\% de los administradores mejorará la velocidad y precisión de sus decisiones logísticas, según encuestas de validación posteriores. \\
\hline
\textbf{Null Hypothesis} & La visualización de reportes e indicadores clave no tiene un impacto significativo en la toma de decisiones de los administradores educativos. \\
\hline
\end{longtable}


\newpage

### Measures.

Con el objetivo de validar las hipótesis previamente formuladas, se definieron métricas específicas que permitan medir el impacto real de cada funcionalidad sobre la experiencia de los usuarios y la eficiencia operativa. Las medidas se establecieron considerando metodologías cuantitativas y cualitativas, incluyendo encuestas post-uso, comparaciones pre y post implementación, análisis de reducción de errores y simulaciones de toma de decisiones. A continuación, se detallan las métricas asignadas a cada pregunta de investigación.

\vspace{1cm}


\begin{longtable}{|p{4cm}|p{10cm}|}
\hline
\textbf{Question} & ¿Cómo influye la visualización en tiempo real del recorrido de las unidades escolares en la percepción de seguridad y confianza de los padres de familia? \\
\hline
\textbf{Measure} & Medir, mediante encuestas post-uso, el porcentaje de padres que reportan sentirse más seguros tras interactuar con el sistema de visualización en tiempo real. \\
\hline
\end{longtable}

\vspace{1em}
\begin{longtable}{|p{4cm}|p{10cm}|}
\hline
\textbf{Question} & ¿Cómo impacta la recepción de notificaciones personalizadas sobre desvíos o retrasos en la satisfacción y percepción de control de los padres? \\
\hline
\textbf{Measure} & Evaluar el nivel de satisfacción y percepción de control a través de encuestas comparativas antes y después de habilitar las notificaciones personalizadas. \\
\hline
\end{longtable}

\vspace{1em}
\begin{longtable}{|p{4cm}|p{10cm}|}
\hline
\textbf{Question} & ¿Cómo afecta la implementación de un panel administrativo centralizado en la eficiencia operativa de las instituciones educativas? \\
\hline
\textbf{Measure} & Medir la reducción del tiempo promedio de resolución de incidencias operativas (en minutos) antes y después del uso del panel centralizado. \\
\hline
\end{longtable}

\vspace{1em}
\begin{longtable}{|p{4cm}|p{10cm}|}
\hline
\textbf{Question} & ¿Cómo influye la integración de sensores IoT en la percepción de valor del sistema por parte de los administradores educativos? \\
\hline
\textbf{Measure} & Determinar, mediante encuestas cualitativas y escalas Likert, el cambio en la percepción de valor del sistema tras el uso de funcionalidades basadas en IoT. \\
\hline
\end{longtable}

\vspace{1em}
\begin{longtable}{|p{4cm}|p{10cm}|}
\hline
\textbf{Question} & ¿Cómo influye la asignación automática de rutas y unidades en la reducción de errores operativos durante el transporte escolar? \\
\hline
\textbf{Measure} & Comparar la frecuencia de errores registrados en la asignación manual versus la asignación automática durante un periodo de prueba. \\
\hline
\end{longtable}

\vspace{1em}
\begin{longtable}{|p{4cm}|p{10cm}|}
\hline
\textbf{Question} & ¿Cómo impacta la visualización de reportes e indicadores clave en la toma de decisiones de los administradores educativos? \\
\hline
\textbf{Measure} & Evaluar el número y calidad de decisiones correctas tomadas antes y después del uso del módulo de reportes, a través de simulaciones y retroalimentación. \\
\hline
\end{longtable}


\newpage

### Conditions.

Para evaluar rigurosamente el impacto de las funcionalidades propuestas, se definieron condiciones experimentales y de control para cada hipótesis. Estas condiciones permiten aislar el efecto de las variables independientes y comparar los resultados obtenidos por grupos expuestos a las funcionalidades con aquellos que no las utilizaron. A continuación, se describen las condiciones bajo las cuales se llevará a cabo cada experimento.

\vspace{1cm}

- **Visualización en tiempo real**
\begin{longtable}{|p{4cm}|p{10cm}|}
\hline
\textbf{Question} & ¿Cómo influye la visualización en tiempo real del recorrido de las unidades escolares en la percepción de seguridad y confianza de los padres de familia? \\
\hline
\textbf{Experimental Condition} & Al menos el 10\% de los padres que utilizaron la funcionalidad de visualización en tiempo real reportan mayor confianza y seguridad. \\
\hline
\textbf{Control Condition} & Ninguno de los padres sin acceso a la visualización en tiempo real reporta cambios en su percepción de seguridad. \\
\hline
\end{longtable}

\vspace{1em}
- **Notificaciones personalizadas**
\begin{longtable}{|p{4cm}|p{10cm}|}
\hline
\textbf{Question} & ¿Cómo impacta la recepción de notificaciones personalizadas sobre desvíos o retrasos en la satisfacción y percepción de control de los padres? \\
\hline
\textbf{Experimental Condition} & El 10\% de los usuarios que reciben notificaciones personalizadas indican mayor satisfacción y sensación de control. \\
\hline
\textbf{Control Condition} & Los usuarios que no reciben notificaciones personalizadas no perciben mejora en la satisfacción ni en el control. \\
\hline
\end{longtable}

\vspace{1em}
- **Panel centralizado**
\begin{longtable}{|p{4cm}|p{10cm}|}
\hline
\textbf{Question} & ¿Cómo afecta la implementación de un panel administrativo centralizado en la eficiencia operativa de las instituciones educativas? \\
\hline
\textbf{Experimental Condition} & Al menos el 10\% de los administradores reporta menor tiempo de respuesta y mayor control operativo con el panel centralizado. \\
\hline
\textbf{Control Condition} & Los administradores que usan una plataforma sin panel unificado no perciben mejora en eficiencia ni reducción de errores. \\
\hline
\end{longtable}

\vspace{1em}
- **Sensores IoT**
\begin{longtable}{|p{4cm}|p{10cm}|}
\hline
\textbf{Question} & ¿Cómo influye la integración de sensores IoT en la percepción de valor del sistema por parte de los administradores educativos? \\
\hline
\textbf{Experimental Condition} & El 10\% de los usuarios que acceden a datos de sensores (GPS, temperatura, RFID) perciben el sistema como más valioso. \\
\hline
\textbf{Control Condition} & Ninguno de los usuarios que interactúan con una versión sin sensores IoT percibe un aumento en el valor percibido del sistema. \\
\hline
\end{longtable}

\vspace{1em}
- **Asignación automática**
\begin{longtable}{|p{4cm}|p{10cm}|}
\hline
\textbf{Question} & ¿Cómo influye la asignación automática de rutas y unidades en la reducción de errores operativos durante el transporte escolar? \\
\hline
\textbf{Experimental Condition} & La implementación de asignación automática reduce errores logísticos al menos en el 10\% de los casos registrados. \\
\hline
\textbf{Control Condition} & No se observa reducción de errores operativos en escenarios donde la asignación sigue siendo manual. \\
\hline
\end{longtable}

\vspace{1em}
- **Reportes e indicadores**
\begin{longtable}{|p{4cm}|p{10cm}|}
\hline
\textbf{Question} & ¿Cómo impacta la visualización de reportes e indicadores clave en la toma de decisiones de los administradores educativos? \\
\hline
\textbf{Experimental Condition} & El 10\% de los administradores que acceden a los reportes toman decisiones más acertadas y en menor tiempo. \\
\hline
\textbf{Control Condition} & Los administradores que no tienen acceso a reportes no muestran mejoras en la toma de decisiones. \\
\hline
\end{longtable}



\newpage

### Scale Calculations and Decisions.

Con base en los resultados esperados de cada hipótesis, se establecieron criterios de decisión que permiten determinar el grado de impacto de las funcionalidades propuestas. Estas escalas —desfavorable, aceptable, ideal y excelente— permiten clasificar los resultados experimentales y definir acciones de implementación basadas en evidencia. A continuación, se detallan las decisiones asociadas a cada hipótesis, considerando el nivel de cumplimiento alcanzado en la fase de validación.

\vspace{1em}


\begin{longtable}{|p{4cm}|p{4cm}|p{1cm}|p{1cm}|p{1cm}|p{1cm}|}
\hline
\textbf{Scale Calculation} & \textbf{Decision} & \textbf{Desf.} & \textbf{Acept.} & \textbf{Ideal} & \textbf{Excel.} \\
\hline
\endfirsthead

\hline
\textbf{Scale Calculation} & \textbf{Decision} & \textbf{Desf.} & \textbf{Acept.} & \textbf{Ideal} & \textbf{Excel.} \\
\hline
\endhead

Creemos que permitir a los padres ver en tiempo real la ubicación del bus escolar aumentará su percepción de seguridad en al menos un 30\%. & Implementar módulo de visualización de rutas con GPS en la app. & & & & X \\
\hline

Creemos que al incluir notificaciones personalizadas sobre desvíos o retrasos, los padres tendrán mayor control y satisfacción. & Integrar sistema de alertas automáticas por desvíos y retrasos. & & & X & \\
\hline

Creemos que un panel centralizado permitirá tomar decisiones más rápidas y reducir errores operativos en al menos un 25\%. & Habilitar dashboard unificado para gestión de rutas, flotas y alertas. & & X & & \\
\hline

Creemos que la integración de sensores IoT aportará valor percibido en al menos el 30\% de los administradores. & Incluir sensores de temperatura, ubicación y RFID con reporte visual. & & & & X \\
\hline

Creemos que automatizar la asignación de rutas reducirá errores logísticos en al menos un 30\%. & Activar lógica automática de asignación por zonas y capacidad. & & X & & \\
\hline

Creemos que mostrar reportes e indicadores clave permitirá tomar mejores decisiones en al menos un 30\% de los casos. & Implementar módulo de reportes con exportación de datos históricos. & & & X &  \\
\hline
\end{longtable}



\newpage

### Methods Selection.

Para validar empíricamente las hipótesis planteadas, se seleccionaron métodos experimentales adecuados al contexto y características de los segmentos objetivo: Padres de Familia (usuarios de la aplicación móvil) y Personal Directivo (usuarios de la plataforma web administrativa). La elección de los métodos se fundamenta en principios estadísticos sólidos que garantizan la confiabilidad de los resultados, incluyendo la representatividad de la muestra, un nivel de significancia del 5\%, una potencia estadística entre el 80\% y el 95\%, y la identificación de un efecto mínimo detectable (MDE) por hipótesis. La combinación de pruebas A/B, encuestas, pruebas de tareas y escenarios permite una validación completa y práctica de cada funcionalidad dentro del entorno digital de RutaKids.

\vspace{1cm}

\begin{longtable}{|p{3cm}|p{2cm}|p{3cm}|p{3cm}|p{3cm}|}
\hline
\textbf{Hipótesis / Funcionalidad} & \textbf{Segmento Objetivo} & \textbf{Método Experimental} & \textbf{Herramientas Digitales} & \textbf{Razonamiento / Objetivo} \\
\hline
\endfirsthead

\hline
\textbf{Hipótesis / Funcionalidad} & \textbf{Segmento Objetivo} & \textbf{Método Experimental} & \textbf{Herramientas Digitales} & \textbf{Razonamiento / Objetivo} \\
\hline
\endhead

Visualización en tiempo real del recorrido (H1) & Padres de Familia & Test de Usabilidad (App), Encuesta Pre/Post & Google Forms, Google Analytics, encuestas digitales & Evaluar cambios en percepción de seguridad y usabilidad. \\
\hline

Notificaciones personalizadas (H2) & Padres de Familia & Prueba A/B (App), Encuesta & Google Analytics, Google Forms, Push Notifications & Medir impacto en satisfacción y control percibido. \\
\hline

Panel administrativo centralizado (H3) & Personal Directivo & Prueba de tareas (Web), Medición de tiempos & Google Analytics, cronómetro, grabación de pantalla & Evaluar eficiencia operativa y reducción de tiempos. \\
\hline

Integración de sensores IoT (H4) & Personal Directivo & Prueba de campo (Web), Encuesta Likert & Plataforma web, Google Analytics, Google Forms & Valorar percepción de avance tecnológico y utilidad práctica. \\
\hline

Asignación automática de rutas (H5) & Personal Directivo & Comparación cuasi-experimental (Web), Análisis de errores & Reportes internos, Google Analytics, hojas de cálculo & Comparar errores logísticos antes y después de automatización. \\
\hline

Módulo de reportes e indicadores (H6) & Personal Directivo & Prueba con escenarios (Web), Encuesta de precisión & Google Analytics, Google Forms, simulaciones internas & Medir mejoras en rapidez y precisión de decisiones. \\
\hline
\end{longtable}


\vspace{1cm}

\textbf{Criterios estadísticos comunes a todas las pruebas:}
\begin{itemize}
  \item Nivel de significancia: 5\% ($\alpha = 0.05$), para minimizar errores atribuibles al azar.
  \item Efecto mínimo detectable (MDE) ajustado según métrica clave por hipótesis.
  \item Potencia estadística: entre 80\% y 95\%, para reducir el riesgo de errores Tipo II.
  \item Muestras representativas por segmento:
    \begin{itemize}
      \item \textbf{Padres de Familia}: Hombres y mujeres de 30 a 50 años, usuarios habituales de apps móviles.
      \item \textbf{Personal Directivo}: Hombres y mujeres de 30 a 60 años, con experiencia en gestión educativa y software institucional.
    \end{itemize}
\end{itemize}



\newpage

### Data Analytics: Goals, KPIs and Metrics Selection.

La selección de objetivos analíticos, indicadores clave de desempeño (KPIs) y métricas específicas permite medir rigurosamente el impacto de las funcionalidades de RutaKids sobre los usuarios objetivo. Tanto para la aplicación móvil —dirigida a Padres de Familia— como para la plataforma web —utilizada por el Personal Directivo—, se definieron indicadores cuantificables alineados a las hipótesis formuladas y al diseño experimental establecido.

Estos KPIs permiten monitorear el rendimiento de cada funcionalidad en términos de percepción de valor, eficiencia operativa, y experiencia del usuario. Se utilizarán herramientas como Google Analytics, formularios digitales y registros del sistema para capturar y analizar la información en tiempo real, lo que permitirá la toma de decisiones basadas en evidencia.

\vspace{1cm}

\begin{longtable}{|p{3cm}|p{3cm}|p{2cm}|p{4cm}|p{2cm}|}
\hline
\textbf{Hipótesis / Funcionalidad} & \textbf{Objetivo de Analítica de Datos} & \textbf{KPI (Indicador Clave)} & \textbf{Métricas Específicas} & \textbf{Herramientas} \\
\hline
\endfirsthead

\hline
\textbf{Hipótesis / Funcionalidad} & \textbf{Objetivo de Analítica de Datos} & \textbf{KPI (Indicador Clave)} & \textbf{Métricas Específicas} & \textbf{Herramientas} \\
\hline
\endhead

Visualización en tiempo real del recorrido (H1) & Incrementar la percepción de seguridad de los padres & \% de padres que reportan mayor seguridad y confianza & - \% de encuestados que indican sentirse más seguros \newline - Tasa de uso (clics, tiempo de uso) \newline - Retención en el módulo & Google Forms, Google Analytics (eventos) \\
\hline

Notificaciones personalizadas (H2) & Mejorar la satisfacción y percepción de control de los padres & \% de padres que reportan mayor satisfacción y control & - \% de encuestados satisfechos \newline - \% de apertura de notificaciones \newline - Tiempo de reacción ante alertas & Google Analytics, Push Notification logs, Google Forms \\
\hline

Panel administrativo centralizado (H3) & Aumentar la eficiencia operativa administrativa & Reducción del tiempo de gestión de incidencias & - Tiempo promedio de resolución \newline - Nº de incidencias resueltas \newline - Nº de clics por tarea & Google Analytics (flujos), Cronómetro digital, Logs del sistema \\
\hline

Integración de sensores IoT (H4) & Mejorar la percepción de valor tecnológico & \% de admins que califican el sistema como avanzado & - Encuestas de percepción \newline - Nº de interacciones con panel IoT \newline - Participación en capacitaciones & Google Forms, Google Analytics, Plataforma web \\
\hline

Asignación automática de rutas (H5) & Disminuir errores operativos & Reducción del porcentaje de errores en asignaciones & - Nº y \% de errores antes/después \newline - Nº de intervenciones manuales \newline - Tiempo dedicado a asignaciones & Reportes internos, Google Analytics, Hojas de cálculo \\
\hline

Reportes e indicadores clave (H6) & Mejorar la toma de decisiones logísticas & \% de admins que reportan mejor velocidad y precisión & - Encuestas sobre decisiones \newline - Tiempo medio de respuesta \newline - Uso del módulo de reportes & Google Analytics, Google Forms, Simulaciones \\
\hline
\end{longtable}

\vspace{1cm}


\textbf{Notas adicionales:}
\begin{itemize}
    \item Los KPIs se seleccionaron por su relevancia en la medición del éxito de cada funcionalidad y su alineación con los objetivos del experimento.
    \item Las métricas cuantitativas serán complementadas por datos cualitativos obtenidos en encuestas y entrevistas cuando corresponda.
    \item Se utilizarán dashboards de Google Analytics para monitoreo en tiempo real y la generación de reportes periódicos.
\end{itemize}



\newpage

### Web and Mobile Tracking Plan.

Para garantizar la correcta recolección de datos relacionados con el uso de las funcionalidades evaluadas, se estableció un plan de tracking tanto para la aplicación móvil (dirigida a Padres de Familia) como para la plataforma web (dirigida al Personal Directivo). Este plan permite registrar eventos clave asociados a los KPIs definidos, asegurando además el cumplimiento de normativas sobre privacidad, anonimización de datos y consentimiento informado.

\vspace{1cm}

- **Tracking en Aplicación Móvil (Padres de Familia)**

\begin{longtable}{|p{3.5cm}|p{3.4cm}|p{3.2cm}|p{4.2cm}|}
\hline
\textbf{Evento / Interacción} & \textbf{Descripción} & \textbf{Herramienta / Instrumento} & \textbf{Observaciones sobre Privacidad} \\
\hline
\endfirsthead

\hline
\textbf{Evento / Interacción} & \textbf{Descripción} & \textbf{Herramienta / Instrumento} & \textbf{Observaciones sobre Privacidad} \\
\hline
\endhead

Visualización de ruta en tiempo real & Registro de accesos, duración de sesión, clics & Google Analytics (eventos) & Datos anonimizados; sin geolocalización exacta registrada \\
\hline

Recepción y apertura de notificaciones & Tasa de recepción, tasa de apertura, reacción & Firebase / Google Analytics & No se almacena contenido sensible \\
\hline

Interacciones con alertas y mensajes & Clics, tiempos de respuesta & Google Analytics & Consentimiento informado requerido \\
\hline

Uso general de la app (inicio de sesión, navegación) & Registro de flujo de uso & Google Analytics, logs internos & Control de acceso y minimización de datos personales \\
\hline
\end{longtable}

\vspace{1cm}

- **Tracking en Plataforma Web (Personal Directivo)**

\begin{longtable}{|p{3.5cm}|p{3.4cm}|p{3.2cm}|p{4.2cm}|}
\hline
\textbf{Evento / Interacción} & \textbf{Descripción} & \textbf{Herramienta / Instrumento} & \textbf{Observaciones sobre Privacidad} \\
\hline
\endfirsthead

\hline
\textbf{Evento / Interacción} & \textbf{Descripción} & \textbf{Herramienta / Instrumento} & \textbf{Observaciones sobre Privacidad} \\
\hline
\endhead

Acceso y uso de panel administrativo & Logins, navegación entre módulos & Google Analytics (flujos), logs & Acceso restringido, auditoría de accesos \\
\hline

Gestión de incidencias y tareas & Tiempo de resolución, número de incidencias & Google Analytics, cronómetro digital, sistema interno & Datos agregados, sin identificación personal en reportes \\
\hline

Uso de módulos IoT y reportes & Frecuencia de uso, interacción con gráficos e informes & Google Analytics, registros del sistema & Anonimización de datos en análisis \\
\hline

Participación en simulaciones / escenarios & Resultados y tiempos de respuesta & Google Forms, simulaciones & Consentimiento informado, resultados anonimizados \\
\hline
\end{longtable}

\vspace{1cm}


- **Resguardo de Datos y Cumplimiento de Privacidad**

  - Se informará a todos los participantes sobre el alcance del tracking y el tipo de datos recolectados mediante política de privacidad y consentimiento explícito.

  - Los datos recolectados serán anonimizados antes de ser analizados y no se compartirán con terceros ajenos al estudio.

  - Solo se almacenarán los datos estrictamente necesarios para la evaluación de las hipótesis y los objetivos del experimento.

  - Se aplicarán prácticas de minimización y retención limitada de datos, de acuerdo a normativas locales y recomendaciones éticas para experimentación en software.


\vspace{1cm}

- **Diagrama de Tracking en App Móvil (Padres de Familia)**


::: code
```bash
    Padre de Familia interactúa con la app móvil
    |
    +-- ¿Evento relevante?
    |   |
    |   +-- Sí:
    |   |   - Visualización de ruta / Notificación / Alerta
    |   |   - Evento registrado por Google Analytics o Firebase
    |   |   - Datos enviados y almacenados en servidores seguros
    |   |   - Anonimización y procesamiento
    |   |   - Generación de métricas y reportes para KPIs
    |   |
    |   +-- No:
    |       - No se registra
```
:::


\vspace{1cm}


- **Diagrama de Tracking en Plataforma Web (Personal Directivo)**


::: code
```bash
    Personal Directivo usa la plataforma web
    |
    +-- ¿Evento relevante?
    |   |
    |   +-- Sí:
    |   |   - Gestión de panel / Incidencia / Reporte
    |   |   - Evento registrado por Google Analytics o logs internos
    |   |   - Datos almacenados en servidores
    |   |   - Anonimización y procesamiento
    |   |   - Generación de KPIs
    |   |
    |   +-- No:
    |       - No se registra

```
:::



\newpage




## Experimentation


La fase de experimentación constituye un eje fundamental del enfoque basado en evidencia adoptado para el diseño y validación de la plataforma RutaKids. Antes de tomar decisiones técnicas o de diseño, es esencial comprender profundamente el comportamiento, las necesidades y los desafíos reales que enfrentan los usuarios. Esta etapa se concibe como un proceso sistemático de aprendizaje validado, donde cada funcionalidad propuesta se pone a prueba en contextos controlados o reales, con el objetivo de recolectar información que permita evaluar su pertinencia, eficacia y aceptación.

Durante esta fase, se definen y priorizan funcionalidades clave que responden a necesidades detectadas en usuarios reales mediante procesos previos de investigación cualitativa y cuantitativa. A través de la formulación de historias de usuario, la construcción de backlogs funcionales y la planificación de experimentos guiados por hipótesis claras, se estructura una hoja de ruta de pruebas que permite iterar de forma ágil sobre la solución.

Los experimentos pueden tomar la forma de prototipos interactivos, pruebas A/B, entrevistas con usuarios, análisis de métricas de comportamiento o sesiones de usabilidad. Cada experimento tiene como objetivo validar o refutar hipótesis específicas relacionadas con el valor, la usabilidad o la viabilidad técnica de las funcionalidades en cuestión. Este enfoque iterativo garantiza que las decisiones de diseño estén respaldadas por datos objetivos obtenidos directamente de los usuarios finales, minimizando el riesgo de construir soluciones basadas únicamente en supuestos o intuiciones del equipo de desarrollo.

En resumen, la experimentación permite reducir la incertidumbre en el desarrollo de RutaKids, asegurar una alineación constante con las expectativas del usuario y fomentar una cultura de mejora continua basada en el aprendizaje empírico.


\newpage

### To-Be User Stories.

Las siguientes historias de usuario representan funcionalidades priorizadas para ser implementadas en la versión futura del sistema. Estas historias están alineadas con las hipótesis definidas durante la fase de investigación y se enfocan en mejorar la experiencia de los padres de familia y del personal administrativo. Cada historia incluye un escenario representativo y criterios de aceptación claros que orientan tanto el desarrollo como su validación posterior.

\begin{longtable}{|p{1cm}|p{3cm}|p{5.2cm}|p{5.3cm}|}
\hline
\textbf{ID} & \textbf{Nombre} & \textbf{Descripción} & \textbf{Criterios de Aceptación} \\
\hline
\endfirsthead

\hline
\textbf{ID} & \textbf{Nombre} & \textbf{Descripción} & \textbf{Criterios de Aceptación} \\
\hline
\endhead

US01 & Visualizar recorrido del bus escolar en tiempo real & 
Como padre de familia, quiero ver la ubicación del bus en tiempo real para saber si mi hijo está en camino o ha llegado a su destino con seguridad. & 
Escenario 1: Dado que el usuario accede a la app, cuando seleccione "Ubicación del bus", entonces debe visualizar un mapa con el recorrido en vivo del bus asignado a su hijo. \\
\hline

US02 & Recibir notificaciones ante desvíos o retrasos & 
Como padre, quiero recibir alertas automáticas si hay cambios en la ruta o retrasos, para poder tomar acciones si es necesario. & 
Escenario 1: Dado que el sistema detecta una desviación o retraso, cuando ocurra, entonces se debe enviar una notificación push o mensaje automático al padre. \\
\hline

US03 & Gestionar rutas desde panel administrativo & 
Como administrador educativo, quiero poder ver, editar y reasignar rutas de transporte desde un panel centralizado para mejorar la operación logística. & 
Escenario 1: Dado que el usuario es administrador, cuando acceda al panel de rutas, entonces debe poder visualizar, modificar y reasignar rutas y unidades activas. \\
\hline

US04 & Visualizar datos de sensores IoT (GPS, temperatura, RFID) & 
Como administrador, quiero ver la información de sensores en tiempo real para asegurar condiciones óptimas de transporte. & 
Escenario 1: Dado que el bus está en operación, cuando el administrador abra el módulo IoT, entonces debe poder ver temperatura interna, ubicación GPS y eventos RFID (abordaje de estudiantes). \\
\hline

US05 & Activar asignación automática de rutas y unidades & 
Como administrador, quiero que el sistema asigne automáticamente estudiantes y buses según zonas y disponibilidad para reducir errores. & 
Escenario 1: Dado que hay nuevos estudiantes registrados, cuando el sistema tenga la información de zona y horarios, entonces debe asignarlos automáticamente a la unidad disponible. \\
\hline

US06 & Generar y exportar reportes analíticos & 
Como administrador educativo, quiero generar reportes de asistencia, cumplimiento de rutas y alertas, para evaluar el desempeño del servicio. & 
Escenario 1: Dado que el usuario entra a la sección de reportes, cuando seleccione filtros de fechas, entonces debe poder generar un PDF o Excel con los indicadores solicitados. \\
\hline

\end{longtable}


\newpage

### To-Be Product Backlog

El *Product Backlog* define la lista priorizada de funcionalidades que formarán parte de la siguiente iteración del sistema. Estas funcionalidades se han derivado directamente de las historias de usuario validadas durante la investigación y están ordenadas según su impacto esperado y urgencia para los segmentos objetivo. La priorización considera criterios de valor para el usuario, viabilidad técnica y alineación con los objetivos del experimento.

\begin{longtable}{|p{1.2cm}|p{4cm}|p{7cm}|p{1.5cm}|}
\hline
\textbf{ID} & \textbf{Nombre} & \textbf{Descripción} & \textbf{Prioridad} \\
\hline
\endfirsthead

\hline
\textbf{ID} & \textbf{Nombre} & \textbf{Descripción} & \textbf{Prioridad} \\
\hline
\endhead

US01 & Visualizar recorrido del bus escolar en tiempo real & 
Como padre de familia, quiero ver la ubicación del bus en tiempo real para saber si mi hijo está en camino o ha llegado a su destino con seguridad. & Alta \\
\hline

US02 & Recibir notificaciones ante desvíos o retrasos & 
Como padre, quiero recibir alertas automáticas si hay cambios en la ruta o retrasos, para poder tomar acciones si es necesario. & Alta \\
\hline

US03 & Gestionar rutas desde panel administrativo & 
Como administrador educativo, quiero poder ver, editar y reasignar rutas de transporte desde un panel centralizado para mejorar la operación logística. & Alta \\
\hline

US04 & Visualizar datos de sensores IoT (GPS, temperatura, RFID) & 
Como administrador, quiero ver la información de sensores en tiempo real para asegurar condiciones óptimas de transporte. & Media \\
\hline

US05 & Activar asignación automática de rutas y unidades & 
Como administrador, quiero que el sistema asigne automáticamente estudiantes y buses según zonas y disponibilidad para reducir errores. & Media \\
\hline

US06 & Generar y exportar reportes analíticos & 
Como administrador educativo, quiero generar reportes de asistencia, cumplimiento de rutas y alertas, para evaluar el desempeño del servicio. & Baja \\
\hline

\end{longtable}


\newpage

### Pipeline-supported, Experiment-Driven To-Be Software Platform Lifecycle

Esta sección presenta el enfoque metodológico adoptado para el desarrollo de la plataforma, el cual combina principios de desarrollo ágil con un ciclo iterativo basado en la experimentación y el aprendizaje validado. La estrategia se fundamenta en la idea de que las funcionalidades de una plataforma no deben construirse directamente desde suposiciones, sino que deben ser descubiertas, ajustadas y validadas a través de ciclos continuos de pruebas e iteración.

Las historias de usuario —derivadas de una investigación previa centrada en los usuarios— fueron descompuestas en tareas específicas y manejadas dentro de un ciclo de trabajo estructurado por sprints. Cada sprint no solo contempló actividades de diseño y desarrollo, sino también la planificación de experimentos diseñados para probar hipótesis asociadas a funcionalidades clave. Estas hipótesis buscaron responder preguntas concretas como: “¿Esta funcionalidad realmente resuelve el problema del usuario?” o “¿Este flujo de navegación resulta comprensible y eficiente para los usuarios finales?”

El enfoque pipeline-supported implica que estas tareas y experimentos fueron organizados y trazados en una línea de tiempo clara, aprovechando herramientas de gestión del ciclo de vida del software que permitieron visibilidad, trazabilidad y control sobre el proceso. Por otro lado, el carácter experiment-driven garantiza que las decisiones de desarrollo se basaron en datos obtenidos de pruebas con usuarios reales, tanto mediante prototipos como a través de funcionalidades mínimas viables (MVPs) implementadas en etapas tempranas.

En conjunto, esta lógica de trabajo permitió maximizar el aprendizaje temprano, reducir riesgos en el desarrollo posterior y asegurar que las funcionalidades finales de la plataforma respondieran de forma precisa y validada a las necesidades del público objetivo.

\newpage

#### To-Be Sprint Backlogs

El siguiente backlog resume el trabajo realizado durante los sprints, detallando tareas por historia de usuario, estado de ejecución y tiempo estimado de esfuerzo. Cada tarea fue pensada para validar hipótesis clave de producto en etapas tempranas mediante prototipos, encuestas y entrevistas, con el fin de minimizar riesgos de desarrollo y maximizar aprendizaje.

\begin{longtable}{|p{1cm}|p{4.5cm}|p{1cm}|p{4.7cm}|p{1.2cm}|p{1cm}|}
\hline
\textbf{US ID} & \textbf{Descripción} & \textbf{Task ID} & \textbf{Task} & \textbf{Estado} & \textbf{Horas} \\
\hline
\endfirsthead

\hline
\textbf{US ID} & \textbf{Descripción} & \textbf{Task ID} & \textbf{Task} & \textbf{Estado} & \textbf{Horas} \\
\hline
\endhead

US001 & Visualización de recorrido del bus escolar en tiempo real & T01 & Crear prototipo en Figma del mapa con ubicación del bus & DONE & 3 \\
\cline{3-6}
 &  & T02 & Diseñar mockup del botón de seguimiento del bus & DONE & 1 \\
\cline{3-6}
 &  & T03 & Diseñar encuesta para validar percepción de seguridad & DONE & 1 \\
\cline{3-6}
 &  & T04 & Aplicar encuestas a padres de familia & DONE & 1 \\
\hline

US002 & Recibir notificaciones ante desvíos o retrasos & T05 & Prototipar sistema de alertas push en Figma & DONE & 2 \\
\cline{3-6}
 &  & T06 & Crear mensajes tipo para desvío, retraso y llegada & DONE & 1 \\
\cline{3-6}
 &  & T07 & Diseñar encuesta sobre percepción de control & DONE & 1 \\
\cline{3-6}
 &  & T08 & Aplicar encuestas a usuarios & DONE & 1 \\
\hline

US003 & Gestionar rutas desde panel administrativo & T09 & Prototipar panel de gestión de rutas y buses & DONE & 3 \\
\cline{3-6}
 &  & T10 & Diagramar flujo de reasignación de rutas & DONE & 1 \\
\cline{3-6}
 &  & T11 & Crear formulario de asignación de unidades & DONE & 1 \\
\hline

US004 & Visualizar datos de sensores IoT & T12 & Prototipar panel con datos de sensores IoT (GPS, RFID, temperatura) & DONE & 3 \\
\cline{3-6}
 &  & T13 & Diseñar componentes visuales para alertas IoT & DONE & 1 \\
\cline{3-6}
 &  & T14 & Preparar encuesta sobre percepción de valor tecnológico & DONE & 1 \\
\hline

US005 & Activar asignación automática de rutas y unidades & T15 & Prototipar lógica visual de asignación automática & DONE & 3 \\
\cline{3-6}
 &  & T16 & Simular escenarios de prueba de asignación & DONE & 1 \\
\cline{3-6}
 &  & T17 & Recoger feedback sobre facilidad y utilidad & DONE & 1 \\
\hline

US006 & Generar y exportar reportes analíticos & T18 & Diseñar módulo de reportes en Figma & DONE & 3 \\
\cline{3-6}
 &  & T19 & Crear exportación mock (PDF y Excel) & DONE & 1 \\
\cline{3-6}
 &  & T20 & Diseñar encuesta sobre utilidad de reportes & DONE & 1 \\
\hline
\end{longtable}


\newpage

#### Implemented To-Be Landing Page Evidence

::: warn
Para acceder al repositorio, haga click a la [URL](https://github.com/CodeMinds-Experimentos/CodeMinds-RutaKids-LandingPage)
:::


**Captura del repositorio:**

![Organización CodeMids, imagen extraída de Github](src/img/cap8/landingGit.png){ width=80% }


**Landing Page en funcionamiento:**

![Imagen extraída de la landing page](src/img/cap8/landing.png)


\newpage

#### Implemented To-Be Frontend-Web Application Evidence

::: warn
Para acceder al repositorio, haga click a la [URL](https://github.com/CodeMinds-Experimentos/RutaKids-WebApp)
:::

**Captura del repositorio:**

![Organización CodeMids, imagen extraída de Github](src/img/cap8/webAppGit.png){ width=80% }


**Web Application en funcionamiento:**

::: warn
Para acceder a la pagina web, haga click a la [URL](https://rutakids-webapp-1.onrender.com/)
:::

![Organización CodeMinds, imagen extraída de Github](src/img/cap6/webapp-deploy-2.jpg){ width=80% }



\newpage

#### Implemented To-Be Native-Mobile Application Evidence

::: warn
Para acceder al figma, haga click a la [URL](https://www.figma.com/design/ph6aTjM4mzxkNic0Hk4VLX/RutaKids?node-id=275-3006&p=f)
:::

![Organización CodeMinds, imagen extraída del Github](src/img/cap6/mobile-app-figma-view.png){ width=50% }

\newpage

#### Implemented To-Be RESTful API and/or Serverless Backend Evidence

**Web Service Deployment** : https://api.rutakids.llantatech.org.pe/swagger-ui/index.html?urls.primaryName=Transportation+Service

![Organización LLantatech, imagen extraída de Github](src/img/cap6/webservices-deploy-2.jpg){ width=80% }

::: warn
Para acceder a la documentación swagger de este proyecto, haga click a la [URL](https://api.rutakids.llantatech.org.pe/swagger-ui/index.html?urls.primaryName=Transportation+Service)
:::

\newpage

#### Team Collaboration Insights

Para complementar el enfoque basado en experimentación, esta sección presenta evidencias de colaboración del equipo dentro de la organización del proyecto en GitHub. A través de las herramientas de gestión de proyectos como tableros Kanban, listas de tareas y visualizaciones de tráfico, es posible analizar el flujo de trabajo, la coordinación entre miembros y la intensidad de actividad durante el desarrollo de las funcionalidades.

Los siguientes gráficos fueron extraídos directamente desde los paneles de la organización “LlantaTech” en GitHub, donde se gestionó el ciclo de trabajo asociado al proyecto RutaKids. Estas herramientas permiten observar tanto el estado de las tareas como las interacciones entre los desarrolladores y diseñadores a lo largo del proceso.


::: warn
Para acceder los insights de este proyecto, haga click a la [URL](https://github.com/orgs/LlantaTech/repositories)
:::

**Tablero Kanban:**

![Organización LLantatech, imagen extraída de Github](src/img/cap6/insights-kanban-todo-1.png){ width=80% }

**Kanban List:**

![Organización LLantatech, imagen extraída de Github](src/img/cap6/insights-kanban-list-1.png){ width=80% }

\newpage

**Network Graph:**

![Organización LLantatech, imagen extraída de Github](src/img/cap6/insights-network-graph-tb2.png){ width=80% }

**Traffic Map:**

![Organización LLantatech, imagen extraída de Github](src/img/cap6/insights-traffic-map-tb2.png){ width=80% }


\newpage


### To-Be Validation Interviews

Con el objetivo de validar la solución propuesta desde la perspectiva del usuario final, se llevaron a cabo entrevistas de validación del escenario To-Be como parte del enfoque centrado en el usuario adoptado en el proceso de diseño. Estas entrevistas constituyen una herramienta clave para obtener retroalimentación cualitativa directa y profunda, permitiendo evaluar en qué medida las funcionalidades diseñadas se alinean con las expectativas, necesidades y problemas reales de los usuarios en su contexto de uso.

La validación del escenario To-Be se realizó mediante la presentación de prototipos funcionales que simulan el comportamiento esperado de la plataforma en su versión futura. A través de sesiones estructuradas de interacción y diálogo, se exploró cómo los usuarios perciben la propuesta de valor, qué tan intuitivas les resultan las interfaces, y qué barreras o confusiones emergen durante la navegación por las principales funcionalidades.

Más allá de la simple observación del uso, las entrevistas se enfocaron en capturar impresiones emocionales, actitudes, y juicios sobre la utilidad y relevancia de la solución. Este enfoque permitió identificar oportunidades de mejora tempranas, ajustar el diseño en base a evidencia empírica y, en general, fortalecer la conexión entre la propuesta tecnológica y la experiencia del usuario final.

En resumen, las entrevistas de validación del escenario To-Be representaron un paso esencial para reducir la brecha entre lo planificado y lo deseable desde el punto de vista del usuario, asegurando que la plataforma evolucione con base en retroalimentación auténtica y significativa.


\newpage

#### Diseño de Entrevistas.

::: box
**Segmento Objetivo 1:** Directivos escolares o personal administrativo
:::

**Interfaces evaluadas:**

* **Dashboard web**

* **Landing Page**

**Objetivo del segmento:** Evaluar si la solución digital (dashboard web y landing page) responde efectivamente a los problemas de gestión del transporte escolar desde una perspectiva operativa y estratégica institucional.

**Flujos evaluados:**

1) **Ingreso al sistema:**

- **Objetivo:** Evaluar claridad del login y percepción de seguridad.

- **Preguntas:**

  - ¿Fue fácil entender el proceso de inicio de sesión?

  - ¿El diseño transmite confianza para ingresar tus credenciales?

  - ¿Qué elemento mejorarías en esta pantalla?

2) **Visualización del panel de rutas activas:**

- **Objetivo:** Comprobar si la información de rutas, buses y estados es clara.

- **Preguntas:**

  - ¿Puedes identificar fácilmente el estado de las rutas activas?

  - ¿Te parece útil la información que se presenta en el panel?

  - ¿Agregarías algún dato operativo adicional?

3) **Emisión de notificaciones a padres:**

- **Objetivo:** Validar la utilidad del sistema de comunicación con padres.

- **Preguntas:**

  - ¿Te pareció fácil enviar alertas desde el sistema?

  - ¿Agregarías más tipos de mensajes (ej. personalizables, por nivel)?

  - ¿Consideras útil que la plataforma centralice toda la comunicación?

  - ¿Qué canal adicional usarías (SMS, correo, WhatsApp)?

4) **Consulta de reportes (asistencia y trayectos):**

- **Objetivo:** Determinar si los reportes ayudan a la toma de decisiones o auditoría.

- **Preguntas:**

  - ¿Los reportes te parecieron claros y útiles?

  - ¿Qué datos crees que faltan o sobran?

  - ¿Te gustaría recibirlos automáticamente al correo?

5) **Configuración y control institucional:**

- **Objetivo:** Evaluar si el sistema ofrece el nivel de control esperado por la institución.

- **Preguntas:**

  - ¿Fue intuitivo personalizar alertas o trayectos?

  - ¿Agregarías niveles de permisos según rol (director, auxiliar, seguridad)?

  - ¿Consideras que este sistema mejoraría la imagen del colegio?

  - ¿Te parece viable su implementación técnica y económica?

6) **Landing page institucional:**

- **Objetivo:** Evaluar si la web comunica la propuesta de valor y motiva la adopción.

- **Preguntas:**

  - ¿La página te ayudó a entender qué ofrece la plataforma?

  - ¿Qué parte te pareció más convincente?

  - ¿Qué información adicional te animaría a adquirirla?


\newpage

::: box
**Segmento Objetivo 2:** Padres de familia con hijos en edad escolar
:::

**Interfaces evaluadas:**

* **Aplicación móvil para padres**

* **Landing page informativa**

**Objetivo del segmento:** Evaluar si la aplicación móvil cumple con las expectativas de los padres en términos de seguridad, facilidad de uso y comunicación efectiva sobre el traslado de sus hijos. 

**Flujos  validados:**

1) **Registro e inicio de sesión como padre:**

  - **Objetivo:** Evaluar si el proceso de registro es intuitivo para usuarios no técnicos.

  - **Preguntas:**

    - ¿Te pareció sencillo el registro y login?

    - ¿Algún paso te confundió o fue innecesario?

    - ¿Te sentiste seguro al ingresar tus datos personales?

    - ¿Qué mejorarías en este proceso?


2) **Visualización del bus escolar en tiempo real:**

  - **Objetivo:** onfirmar utilidad y tranquilidad que genera el seguimiento del bus.

  - **Preguntas:**

    - ¿Pudiste ubicar el bus en el mapa fácilmente?

    - ¿Te generó tranquilidad saber por dónde va tu hijo?

    - ¿Qué información extra te gustaría ver (chofer, tiempo estimado, velocidad, etc.)?

    - ¿Esta función te ayudaría en tu rutina diaria?

3) **Recepción de alertas de llegada y salida:**

  - **Objetivo:** Evaluar si las notificaciones automáticas son útiles y comprensibles.

  - **Preguntas:**

    - ¿Las alertas fueron claras y oportunas?

    - ¿En qué momentos te gustaría recibirlas?

    - ¿Preferirías recibirlas por app, WhatsApp, correo o SMS?

    - ¿Te gustaría poder ajustar la frecuencia o el contenido?


4) **Consulta del historial de trayectos:**

  - **Objetivo:** Comprobar si los padres usarían esta función como referencia o respaldo.

  - **Preguntas:**

    - ¿Te parece útil tener un historial de rutas?

    - ¿Lo usarías para verificar horarios o ante incidentes?

    - ¿Qué datos te gustaría ver ahí (fecha, hora, chofer, eventos)?

    - ¿Esperas poder exportar o compartir esta información?


5) **Acceso y edición del perfil del estudiante:**

  - **Objetivo:** Confirmar si los padres pueden gestionar correctamente la información.

  - **Preguntas:**

    - ¿Fue fácil encontrar y editar el perfil de tu hijo/a?

    - ¿Qué tipo de información te gustaría tener allí?

    - ¿Te gustaría vincular a otros acudientes (mamá, papá, tutor)?

    - ¿Prefieres ver información médica, autorizaciones o historial de alertas?


6) **Landing page:**

  - **Objetivo:** Evaluar si la presentación inicial del producto genera confianza e interés.

  - **Preguntas:**

    - ¿La página te explicó bien qué hace la app?

    - ¿Te motivaría a probarla?

    - ¿Qué le agregarías para que más padres se interesen?

\newpage

#### Registro de Entrevistas.

::: note
Para acceder al video de las entrevistas, haga click en la [URL](https://upcedupe-my.sharepoint.com/:v:/g/personal/u202210059_upc_edu_pe/EV28HExaIsFIh22vN6-VY-sBzdw5JApHhMXCx5KyLMdBPQ?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D&e=X20C3t)
:::

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
\textbf{Tiempo de entrevista} & 00:00 - 10:34             \\ \hline
\end{tabular}
\end{center}
\end{table}

**Resumen de la entrevista**

El entrevistado mostró una actitud muy receptiva hacia la propuesta de RutaKids, resaltando desde el inicio la pertinencia de una solución tecnológica enfocada en la gestión del transporte escolar. Consideró que la landing page comunica con claridad la propuesta de valor, destacando elementos como la seguridad y la trazabilidad. Sugirió incluir una sección de preguntas frecuentes para aclarar dudas institucionales.

Respecto al proceso de inicio de sesión en la aplicación web, valoró positivamente su simplicidad e indicó que inspira confianza. Propuso como mejora la inclusión de opciones de autenticación institucional.

En cuanto al panel de rutas activas, destacó su organización clara y su utilidad para la supervisión diaria, recomendando aumentar el contraste visual en alertas críticas.

Durante la prueba de emisión de notificaciones a padres, encontró el proceso eficiente y valoró la posibilidad de personalización. Sugirió integrar plantillas predeterminadas para situaciones frecuentes.

Los reportes de asistencia y trayectos fueron considerados útiles para reuniones y auditorías, aunque propuso filtros por nivel educativo y envío automático al correo institucional.

Finalmente, en la configuración de alertas, señaló que el proceso es intuitivo y sugirió permitir condiciones personalizadas (por ejemplo, alertas tras cierto umbral de retraso). En resumen, calificó la plataforma como una solución “altamente necesaria” y afirmó que tendría un impacto positivo en la confianza de los padres y en la imagen institucional del colegio.

![Imagen extraída del video de entrevistas](src/img/cap6/Entrevistas/PaulRamos.png)

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
\textbf{Tiempo de entrevista} & 10:34 - 19:40             \\ \hline
\end{tabular}
\end{center}
\end{table}

**Resumen de la entrevista**

Juliana Chávez expresó una opinión positiva sobre la solución tecnológica presentada a través de la landing page, indicando que el contenido comunica adecuadamente los beneficios de la plataforma. Consideró que los enfoques de seguridad, monitoreo y control fueron especialmente convincentes. Como sugerencia, planteó añadir testimonios de otras instituciones educativas que usen el sistema para reforzar la confianza.

Durante la validación del login e ingreso al sistema, manifestó que el flujo era claro, accesible y comprensible incluso para personal con poca experiencia digital. Valoró la estética sobria y profesional, y no identificó barreras importantes de acceso.

En la revisión del panel de rutas activas, destacó que la disposición de la información facilita una supervisión rápida y efectiva. Pudo identificar con facilidad los estados de cada bus y recomendó incluir una visualización por bloques de horarios escolares.

Sobre la funcionalidad de emisión de notificaciones, Juliana valoró la personalización del mensaje, considerándolo una ventaja frente a sistemas tradicionales. Mostró interés en contar con canales alternativos como correo electrónico o SMS, sobre todo en situaciones de emergencia.

En cuanto a los reportes de asistencia y trayectos, señaló que estos son especialmente útiles para reuniones con padres, reportes de psicología o seguimiento disciplinario. Sugeriría que el sistema permita exportarlos en formatos editables como Excel o PDF.

Finalmente, en la configuración de alertas, calificó el proceso como intuitivo y funcional. Propuso incluir una opción de “alertas automáticas por nivel o aula” para facilitar la gestión de grandes grupos. Juliana considera que esta plataforma no solo resolvería necesidades operativas, sino que también fortalecería el compromiso institucional con la seguridad de los estudiantes y la innovación educativa.

![Imagen extraída del video de entrevistas](src/img/cap6/Entrevistas/JulianaChavez.png)

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
\textbf{Tiempo de entrevista} & 19:40 - 29:26             \\ \hline
\end{tabular}
\end{center}
\end{table}

**Resumen de la entrevista**
Graciela Ríos valoró positivamente la propuesta presentada en la landing page, destacando que la solución aborda de manera clara y efectiva los principales problemas relacionados con el transporte escolar. Afirmó que la idea de recibir alertas y monitoreo en tiempo real genera confianza tanto para el personal educativo como para los padres.

Respecto al inicio de sesión en el sistema, Graciela encontró el flujo de login comprensible y seguro. Apreció que los campos estén bien identificados y el proceso no requiera más pasos de los necesarios. Mencionó que, para instituciones pequeñas, esto simplifica la adopción de la herramienta.

Al explorar el panel de rutas activas, manifestó que la interfaz es intuitiva y de rápida lectura. Le agradó la posibilidad de visualizar cada bus y su estado actual. Sugirió que sería útil integrar un resumen de incidencias recientes dentro del panel para facilitar la supervisión diaria.

En cuanto a la funcionalidad de notificaciones, consideró muy valioso el poder comunicar a padres y tutores cualquier eventualidad en tiempo real. Resaltó que esto permitiría prevenir confusiones o alarmas innecesarias, y estaría a favor de incorporar plantillas predeterminadas de mensajes para situaciones comunes.

Los reportes de asistencia y trayectos le parecieron completos y útiles para fines administrativos. Le gustaría que el sistema genere informes automáticos por semana o mes y que puedan filtrarse por nivel o sección, lo que considera clave para análisis internos y reuniones con padres.

Finalmente, la configuración de alertas fue calificada como funcional y fácil de personalizar. Le pareció acertado que se puedan programar por horario o curso, y afirmó que esto representaría una mejora notable frente al sistema manual actualmente usado. Considera que implementar esta plataforma fortalecería la confianza institucional, la seguridad de los estudiantes y la eficiencia operativa.

![Imagen extraída del video de entrevistas](src/img/cap6/Entrevistas/RocioRios.png)


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
\textbf{Tiempo de entrevista} & 29:26 - 40:00             \\ \hline
\end{tabular}
\end{center}
\end{table}

**Resumen de la entrevista**
Gabriela Ríos manifestó una opinión muy favorable tras visualizar la landing page del sistema. Comentó que el diseño es atractivo, la información está bien organizada y la propuesta de valor le resultó clara. Indicó que le genera confianza, especialmente porque se centra en la seguridad y bienestar de los hijos durante el transporte escolar.

Sobre el registro e inicio de sesión, afirmó que el flujo fue sencillo y comprensible. No encontró pasos confusos y se sintió segura ingresando sus datos. Aplaudió que la app no requiera conocimientos técnicos para acceder y que se enfoque en ofrecer tranquilidad desde el primer contacto.

Durante la prueba de la visualización del bus en tiempo real, Gabriela señaló que fue lo más impactante de la experiencia. Le brindó una fuerte sensación de tranquilidad poder ver la ubicación del bus y confirmó que usaría esa función diariamente. Sugirió agregar el nombre del chofer o la placa del vehículo para mayor confianza.

En cuanto a las alertas de llegada y salida, le gustó que fueran automáticas y visibles en pantalla. Preferiría recibirlas por notificación directa en la app, aunque también consideraría útiles mensajes vía WhatsApp en casos urgentes. Le pareció ideal poder personalizar el horario de las alertas según el colegio de su hijo.

El historial de trayectos también fue calificado como muy útil. Lo usaría especialmente en días de ausencias o cuando ocurran retrasos, y le interesaría ver detalles como la hora exacta de embarque, nombre del conductor y puntos de parada.

Finalmente, respecto al perfil del estudiante, encontró fácil su edición. Considera importante poder vincular a otros acudientes (padre, madre, tutor) para compartir la responsabilidad. En general, Gabriela afirmó que estaría dispuesta a pagar por esta app si está asociada directamente con el colegio, ya que le parece un avance significativo en seguridad y comunicación.

![Imagen extraída del video de entrevistas](src/img/cap6/Entrevistas/GabrielaRios.png)

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
\textbf{Tiempo de entrevista} & 40:00 - 56:25             \\ \hline
\end{tabular}
\end{center}
\end{table}

**Resumen de la entrevista**
Zoila Lescano expresó un alto nivel de satisfacción con el enfoque y funcionalidades de la solución digital tras haber revisado la landing page. Opinó que el sitio transmite confianza desde el inicio, y que presenta la información de forma clara para cualquier padre. Considera que la app resuelve un problema muy frecuente: la incertidumbre diaria sobre el traslado de sus hijos.

Respecto al registro e inicio de sesión, no tuvo dificultades y resaltó que fue intuitivo. Comentó que se sintió cómoda ingresando sus datos y que el flujo está diseñado pensando en usuarios con pocos conocimientos tecnológicos.

Al evaluar la función de seguimiento del bus escolar en tiempo real, Zoila la calificó como "imprescindible". Afirmó que esta característica le daría tranquilidad plena al saber dónde están sus hijos. Sugirió incluir un botón de “emergencia” o “alerta rápida” que pueda ser activado por los niños ante cualquier incidente en el trayecto.

Las alertas automáticas de llegada y salida también fueron bien valoradas. Zoila prefiere recibirlas mediante notificaciones push en el celular, pero señaló que sería ideal poder elegir entre WhatsApp, SMS o correo. Considera fundamental que el contenido pueda personalizarse y que las alertas lleguen en tiempo real.

Sobre el historial de trayectos, mencionó que sería útil para tener control de asistencia y horarios. Agregaría información como fecha, hora, nombre del conductor y duración estimada del recorrido. Dijo que, si su hija faltara o ocurriera algo inusual, esta función le permitiría hacer seguimiento fácilmente.

En cuanto al perfil del estudiante, Zoila cree que debe permitir editar datos básicos como dirección, contacto de emergencia y persona autorizada a recoger al menor. También sugirió que el perfil pueda ser compartido con varios tutores para facilitar la coordinación entre padres.

En general, considera que la aplicación representa una solución integral que mejora la seguridad y alivia la carga mental de muchos padres. Está completamente dispuesta a pagar por un servicio que integre todas estas funciones, sobre todo si se implementa directamente con apoyo del colegio.

![Imagen extraída del video de entrevistas](src/img/cap6/Entrevistas/ZoilaLescano.png)

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
\textbf{Tiempo de entrevista} & 56:25 - 1:10:23             \\ \hline
\end{tabular}
\end{center}
\end{table}

**Resumen de la entrevista**
Hayle Ascoy valoró positivamente la propuesta presentada a través de la landing page, destacando que la información es clara y que la app proyecta una imagen confiable. Mencionó que una solución de este tipo es muy necesaria en su entorno, ya que muchas veces los padres viven con ansiedad al no saber exactamente dónde están sus hijos durante el traslado.

Respecto al registro e inicio de sesión, indicó que el proceso le resultó sencillo, con instrucciones claras y sin pasos innecesarios. Se sintió segura ingresando sus datos personales, especialmente porque la app muestra señales visuales de validación y cuenta con una interfaz amigable.

Al ver la función de seguimiento en tiempo real del bus escolar, Hayle expresó su entusiasmo. Mencionó que esta era la característica más esperada por padres como ella. Afirmó que una vez, su hija se retrasó y no lograba comunicarse con el conductor, situación que se hubiera evitado con esta función. Sugirió mostrar también la matrícula del vehículo y una foto del conductor para mayor confianza.

Las alertas automáticas de embarque y desembarque fueron descritas como “tranquilidad inmediata”. Dijo que preferiría recibir las notificaciones directamente en la app y también en WhatsApp si es posible. Destacó que le gustaría poder ajustar los horarios en que se reciben, por ejemplo, si hay días con actividades extracurriculares.

Sobre el historial de trayectos, Hayle lo consideró extremadamente útil. Lo usaría como respaldo si un día su hija no llegara a tiempo o si necesitara reportar una anomalía. Propuso que se incluyan indicadores visuales de puntualidad y posibles desvíos.

Respecto al perfil del estudiante, opinó que debería incluir alergias, contacto de emergencia, y permitir agregar observaciones especiales como “solo puede ir con este conductor”. También le parecería muy conveniente que tanto el padre como la madre puedan acceder y editar esta información sin restricciones.

En conclusión, Hayle afirmó que implementaciones como esta deberían ser impulsadas directamente por los colegios, ya que garantizan una mayor confianza y profesionalismo. Estaría dispuesta a pagar por esta app si garantiza una mejora real en la seguridad y comunicación durante el traslado escolar.

![Imagen extraída del video de entrevistas](src/img/cap6/Entrevistas/HayleAscoy.png)

\newpage

## Experiment Aftermath & Analysis

Tras la ejecución de los experimentos y validaciones, se realizó un análisis integral de los datos recolectados con el objetivo de interpretar los resultados y contrastarlos con las hipótesis planteadas. Esta sección documenta los aprendizajes obtenidos, los hallazgos más relevantes en cuanto a percepción de valor, usabilidad y funcionalidad, así como los cambios sugeridos para futuras iteraciones del sistema. El análisis posterior al experimento permite reflexionar críticamente sobre el impacto real de las soluciones diseñadas y fortalece la toma de decisiones para etapas posteriores de desarrollo.

\newpage

### Analysis and Interpretation of Results

En este estudio, las preguntas originales formuladas en las entrevistas iniciales fueron adaptadas y estructuradas específicamente para evaluar la experiencia de los usuarios con la plataforma RutaKids. El objetivo fue obtener respuestas más claras y relevantes que permitieran analizar la percepción, preferencias y necesidades de los participantes respecto a las funcionalidades clave del sistema, tanto desde la perspectiva de los padres de familia como de los administradores escolares.

**Preguntas Formuladas**

En la evaluación se realizaron las siguientes preguntas para valorar la experiencia de los usuarios con las nuevas funcionalidades propuestas:

1. ¿Qué tan útil considera la visualización en tiempo real del recorrido del bus escolar?


2. ¿Recibió notificaciones ante desvíos o retrasos del bus? ¿Le resultaron útiles?


3. ¿Considera relevante la información de sensores IoT (GPS, RFID, temperatura) presentada en la aplicación?


4. ¿Le resulta fácil utilizar el panel administrativo para gestionar rutas y asignaciones?


5. ¿Qué tan útil encuentra la opción de asignación automática de rutas y unidades?


6. ¿Considera útiles los reportes analíticos generados por el sistema?


7. ¿Cómo calificaría la interfaz y facilidad de uso de la aplicación?


8. ¿Le pareció relevante recibir notificaciones personalizadas sobre la llegada o salida del bus?


9. ¿Considera útil la función de exportar reportes en PDF o Excel?


10. ¿Qué opinión tiene sobre la ubicación y organización de las diferentes secciones en la aplicación?


Estas preguntas fueron presentadas a una muestra de 25 usuarios potenciales, quienes respondieron de acuerdo a su experiencia utilizando las funcionalidades desarrolladas. A continuación, se presentan y analizan los resultados obtenidos mediante gráficos.

\newpage

#### Análisis de datos demográficos

- **Distribución de edades:**

 Las edades de los participantes oscilan entre 24 y 52 años, siendo la mayoría (60%) padres de familia entre 30 y 40 años, lo que refleja que la aplicación RutaKids está dirigida principalmente a un público adulto-joven responsable del traslado escolar de sus hijos.

![Tabla gráfica  que representa la distribución de edades de los participantes](src/img/cap8/tabla1.png)

\newpage

- **Duración de uso:**

 El 45% de los usuarios reportó utilizar la aplicación diariamente para monitorear el trayecto escolar, mientras que un 35% la utiliza varias veces por semana y el 20% solo en ocasiones específicas, como eventos o días de excursión. Estos resultados indican un nivel de compromiso regular con la plataforma.

 ![Tabla gráfica que representa la Frecuencia De Uso De La Aplicación RutaKids](src/img/cap8/grafo1.png)

\newpage

#### Evaluación de Características

- **Visualización en tiempo real del bus:**

 El 92% de los participantes consideró muy útil la funcionalidad de seguimiento en tiempo real del bus escolar. Este resultado valida la importancia de la visibilidad y control para los padres respecto a la seguridad de sus hijos durante el trayecto.

![Tabla gráfica que representa la percepción de los participantes sobre el seguimiento en tiempo real del bus escolar](src/img/cap8/grafo2.png)

\newpage

- **Notificaciones ante desvíos o retrasos:**

 El 87% de los usuarios afirmó que las notificaciones automáticas sobre desvíos o retrasos son útiles y les permiten actuar con anticipación ante eventualidades. El 13% restante sugiere mejorar la personalización y el tiempo de alerta.

![Tabla gráfica que representa la percepción sobre las notificaciones ante desvíos o retrasos](src/img/cap8/grafo3.png)

\newpage


- **Información de sensores IoT (GPS, RFID, temperatura):**

 Un 78% de los administradores valoró como relevante la información en tiempo real proveniente de los sensores, destacando su utilidad para la supervisión del ambiente y la seguridad en el transporte. Un 22% manifestó que solo consulta estos datos en casos específicos.

![Tabla gráfica que representa la percepción sobre la informacion de los sensores iot](src/img/cap8/grafo4.png)


\newpage


- **Facilidad de uso del panel administrativo:**

 El 84% de los administradores calificó como fácil o muy fácil la gestión de rutas y unidades a través del panel administrativo. El resto sugirió simplificar los flujos de reasignación y mejorar la documentación.

![Tabla gráfica que representa la facilidad de uso del panel administrativo según usuarios administrativos](src/img/cap8/grafo5.png)

\newpage

- **Asignación automática de rutas y unidades:**

 El 90% de los encuestados considera que la asignación automática agiliza el proceso y reduce errores. Sin embargo, algunos administradores proponen mayor flexibilidad en los criterios de asignación.

![Tabla gráfica que representa la percepción sobre la asignación automática de rutas y unidades](src/img/cap8/grafo6.png)

\newpage

- **Reportes analíticos:**

 El 80% de los usuarios administrativos encuentra útiles los reportes para evaluar la asistencia y desempeño del servicio. El 20% restante menciona dificultades para personalizar filtros avanzados.

![Tabla gráfica que representa la utilidad percibida de los reportes analíticos](src/img/cap8/grafo7.png)

\newpage

- **Interfaz y facilidad de uso general:**

 El 88% de los participantes calificó la interfaz como intuitiva y fácil de navegar. El 12% sugirió mejoras en la disposición de menús y acceso rápido a funciones principales.

![Tabla gráfica que representa la percepción sobre la interfaz y facilidad de uso general](src/img/cap8/grafo8.png)

\newpage

- **Notificaciones personalizadas:**

 El 85% de los padres valora recibir notificaciones personalizadas sobre llegada y salida del bus. El 15% considera que la frecuencia podría ser ajustable según preferencias individuales.

![Tabla gráfica que representa la valoración de las notificaciones personalizadas por los padres](src/img/cap8/grafo9.png)

\newpage

- **Función de exportar reportes:**

 El 77% de los usuarios administrativos calificó positivamente la opción de exportar reportes en PDF o Excel. Algunos usuarios manifestaron interés en formatos adicionales, como gráficos interactivos.

![Tabla gráfica que representa la percepción sobre la función de exportar reportes](src/img/cap8/grafo10.png)

\newpage

- **Ubicación y organización de las secciones:**
 El 82% de los usuarios opinó que la organización de las secciones facilita el acceso a las funciones principales, aunque el 18% recomendó optimizar la visibilidad de módulos de configuración y ayuda.

![Tabla gráfica que representa la percepción sobre la organización de las secciones](src/img/cap8/grafo11.png)

\newpage

#### Recomendaciones de los usuarios

Entre las características que los usuarios consideran que aportan mayor valor destacan:

  - Seguimiento en tiempo real del bus escolar.

  - Notificaciones automáticas y personalizadas.

  - Facilidad de uso del panel administrativo y reportes.

Las principales áreas de mejora sugeridas son la personalización de notificaciones, optimización de filtros de reportes y simplificación de flujos en la interfaz administrativa.

![Tabla gráfica que representa los aspectos de mayor valor y áreas de mejora percibidas por los usuarios](src/img/cap8/tabla2.png)


\newpage

### Re-scored and Re-prioritized Question Backlog

Esta sección presenta una reevaluación de las preguntas clave planteadas inicialmente, reorganizadas según nuevas prioridades identificadas a partir del análisis de resultados, retroalimentación de usuarios y viabilidad técnica. La priorización responde a la relación directa de cada pregunta con el valor percibido por los usuarios, el impacto en la operación del sistema y la factibilidad de implementación en próximos ciclos de desarrollo.

\begin{longtable}{|p{1.5cm}|p{13.5cm}|}
\hline
\textbf{Prioridad} & \textbf{Pregunta} \\
\hline
\endfirsthead

\hline
\textbf{Prioridad} & \textbf{Pregunta} \\
\hline
\endhead

1 & ¿Mejorará la satisfacción de los padres poder configurar la frecuencia y el tipo de notificaciones que reciben? \\
\hline
2 & ¿Aumentará la eficiencia de los administradores la capacidad de crear y guardar filtros de reporte personalizados? \\
\hline
3 & ¿Simplificará la gestión diaria de los padres añadiendo una función para notificar la ausencia de un estudiante para un día específico? \\
\hline
5 & ¿Mejorará la seguridad y la comunicación la implementación de un chat directo y seguro entre los padres y el monitor del bus? \\
\hline
8 & ¿Reducirá los errores de identificación la inclusión de fotos de los estudiantes en los perfiles y listas de asistencia? \\
\hline
\end{longtable}


Estas nuevas prioridades permitirán al equipo de desarrollo enfocar recursos en mejoras incrementales de alto impacto, reforzando tanto la experiencia del usuario como la eficiencia del sistema RutaKids en futuras versiones.

\newpage

## Continuous Learning

El aprendizaje continuo fue un eje central en el desarrollo del proyecto. A través de la recolección de retroalimentación, la revisión de resultados y la iteración constante, el equipo logró adaptar la solución a las necesidades reales de los usuarios y fortalecer sus propias capacidades durante cada fase del proceso.

\newpage

### Shareback Session Artifacts: Learning Workflow

**Figma (Prototipo):** El prototipo interactivo desarrollado en figma refleja las interfaces y soluciones propuestas, diseñadas con base en las necesidades y expectativas de los usuarios. Este artefacto muestra cómo el equipo iteró y ajustó los elementos visuales y funcionales durante el proceso de diseño. 

::: warn
Para acceder al prototipo, haga click a la [URL](https://www.figma.com/design/ph6aTjM4mzxkNic0Hk4VLX/RutaKids?node-id=0-1&t=XnMI0WIy5skzJZIy-1)
:::

![Imagen extraida de figma](src/img/cap8/prototipo.png)

**Encuesta de Google Forms:** Se utilizó una encuesta creada en Google Forms para recopilar el feedback de los usuarios y validar las hipótesis planteadas durante el diseño. Esta encuesta permitió evaluar la experiencia del usuario y recopilar datos que respaldan las decisiones tomadas en la mejora de la aplicación.

**Enlace encuesta:** https://forms.gle/svaGUCBHtD6hQsSx9

![Imagen extraida de GoogleForms](src/img/cap8/encuesta.png)


**Google Analytics:** Se implementó Google Analytics para monitorear y analizar el comportamiento de los usuarios dentro de la aplicación. Esta herramienta permitió identificar patrones de uso, medir el desempeño de las funcionalidades y tomar decisiones informadas para optimizar la experiencia del usuario.

![Imagen extraida de Google Analytics](src/img/cap8/analytics.jpg)

\newpage


## To-Be Software Platform Pre-launch

Previo al lanzamiento oficial de la plataforma, se llevó a cabo una etapa crítica conocida como pre-lanzamiento, cuyo propósito fue asegurar que el producto estuviera completamente preparado para ser presentado y utilizado por los usuarios finales. Esta fase no solo implicó la revisión técnica del sistema, sino también una planificación estratégica orientada a facilitar una introducción fluida, atractiva y funcional que genere confianza desde el primer contacto.

Durante esta etapa, se ejecutaron una serie de acciones clave enfocadas en la preparación técnica, operativa y comunicacional del producto. En primer lugar, se realizaron pruebas finales del sistema (también conocidas como pruebas de aceptación de usuario o UAT, por sus siglas en inglés), con el objetivo de validar el cumplimiento de los requerimientos funcionales y no funcionales definidos durante el proceso de desarrollo. Estas pruebas permitieron verificar aspectos como el rendimiento, la estabilidad, la seguridad, la interoperabilidad y la usabilidad general del sistema, asegurando que todos los módulos funcionaran correctamente en conjunto y bajo condiciones reales de uso.

Además de la validación técnica, se trabajó intensamente en la generación de materiales de apoyo diseñados para facilitar la apropiación temprana de la plataforma por parte de los usuarios. Estos materiales incluyeron manuales de usuario, guías rápidas, videos explicativos, documentos de preguntas frecuentes (FAQs) y recursos visuales orientados a simplificar la curva de aprendizaje. El objetivo fue proporcionar a los usuarios finales todas las herramientas necesarias para comprender el funcionamiento de la plataforma desde el primer momento, reduciendo la dependencia de soporte técnico directo y favoreciendo una adopción autónoma.

También se planificaron ensayos de despliegue y simulacros de uso que permitieron identificar posibles puntos de fricción en el proceso de onboarding, navegación y resolución de tareas. Esta información fue crucial para realizar ajustes finales en elementos como los textos de la interfaz, los flujos de navegación, los mensajes de error y las opciones de personalización, todo ello con miras a optimizar la experiencia del usuario desde el inicio.

Finalmente, se definieron métricas clave de seguimiento post-lanzamiento, así como los mecanismos de recolección de datos que permitirán evaluar la adopción, satisfacción y desempeño del sistema una vez puesto en producción. Estas métricas servirán de base para futuras iteraciones y mejoras, manteniendo el enfoque continuo en la calidad y en la experiencia centrada en el usuario.

En conjunto, el pre-lanzamiento de la plataforma no solo representó una etapa de verificación final, sino una instancia estratégica de preparación integral que buscó maximizar el impacto positivo del producto en su fase inicial de despliegue, reduciendo riesgos, consolidando la propuesta de valor, y generando una experiencia memorable desde el primer uso.


\newpage

### About-the-Product Intro Video

Se desarrolló un video introductorio que resume las principales funcionalidades, ventajas y el valor diferencial de la plataforma. Este material sirve como apoyo para comunicar de manera clara y visual el propósito y los beneficios del software a los usuarios y partes interesadas antes del lanzamiento oficial. 

::: warn
Para acceder al video about the product, haga click a la [URL](https://upcedupe-my.sharepoint.com/:v:/g/personal/u202210059_upc_edu_pe/EWO4I1TkuVdCnZbW0aswNssBgLRcrsjVJa2rl-7IQv-QoA?e=2KDzPp&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D)
:::

![Imagen extraida del video about the product](src/img/cap8/about.png)

\newpage

# Conclusiones

## Conclusiones y recomendaciones

1. **Gestión de Configuración Impecable:** Hemos concluido que la base del proyecto se sustenta en una Gestión de Configuración de Software (SCM) excepcionalmente bien definida. La estandarización de entornos, librerías y versiones de SDK asegura la reproducibilidad y minimiza los problemas de "funciona en mi máquina". Esto establece un pilar de estabilidad y profesionalismo desde el inicio.

2. **Adopción Rigurosa de Metodologías Ágiles:** El equipo ha demostrado una aplicación rigurosa y transparente de las metodologías ágiles. La planificación detallada de los Sprints, la gestión visual a través de tableros Kanban y el desglose de tareas en Historias de Usuario (US) y Work Items (WI) con estimaciones, evidencian un control total sobre el flujo de trabajo, promoviendo la previsibilidad y la entrega continua de valor.

3. **Cultura de Calidad Guiada por Comportamiento (BDD):** Destacamos el profundo compromiso con la calidad, que va más allá de las pruebas tradicionales. La implementación extensiva del Desarrollo Guiado por Comportamiento (BDD) a través de Gherkin sirve como un "contrato" claro entre los requisitos de negocio y la implementación técnica, asegurando que el software haga lo correcto de la manera correcta.

4. **Arquitectura Políglota y Orientada a Propósito:** La elección de un stack tecnológico diversificado (React, Angular, Flutter, Spring Boot, Python) no es casual, sino una decisión arquitectónica deliberada. Observamos que se ha aplicado la filosofía de "usar la mejor herramienta para cada tarea", lo que permite optimizar cada componente del sistema (landing, app de admin, app móvil, servicios) de forma independiente y eficiente.

5. **Diseño Arquitectónico Formal y Documentado:** El proyecto no solo se ha construido, sino que se ha diseñado con previsión. El uso de modelos como C4 con Structurizr y diagramas con Mermaid demuestra un esfuerzo consciente por planificar y comunicar la arquitectura del sistema. Esto facilita la comprensión, la escalabilidad y el mantenimiento a largo plazo.

6. **Automatización del Despliegue como Pilar Fundamental (DevOps):** Hemos notado una fuerte orientación hacia las prácticas DevOps. La configuración de pipelines de CI/CD, el uso de contenedores con Docker y el despliegue automatizado en plataformas como Vercel y Netlify son indicativos de un enfoque moderno que busca agilidad, seguridad y fiabilidad en las entregas.

7. **Validación del Problema a través de la Voz del Usuario:** Consideramos que la realización de entrevistas de validación con los segmentos objetivo ha sido el acto más estratégico del proyecto. Estas no solo confirmaron las hipótesis, sino que pusieron de manifiesto los "dolores" reales (inseguridad, falta de control, ansiedad) que RutaKids se propone resolver, dotando al proyecto de un propósito claro y validado.

8. **Conexión Directa entre Funcionalidades y Necesidades Reales:** A raíz de la validación, concluimos que las funcionalidades propuestas no son arbitrarias. Características como el monitoreo en tiempo real, las notificaciones de embarque y la gestión centralizada desde el colegio responden directamente a las preocupaciones expresadas por padres y directivos, lo que garantiza una alta probabilidad de adopción y satisfacción.

9. **Proceso de Diseño de Experiencia de Usuario Formalizado:** El uso de herramientas como UxPresia para mapas de historias y Figma para prototipos interactivos demuestra que la experiencia de usuario (UX/UI) ha sido una disciplina central en el proceso, y no una ocurrencia tardía. Esto asegura que las interfaces sean intuitivas y estén alineadas con los flujos de trabajo de los usuarios finales.

10. **Cultura de Documentación Exhaustiva y Práctica:** El equipo ha cultivado una excelente cultura de la documentación. Desde la especificación de APIs con Swagger (OpenAPI) hasta la documentación de componentes con Storybook y la justificación de librerías, se ha creado un ecosistema de información que facilita la integración, la colaboración y la incorporación de nuevos miembros al equipo.

11. Estandarización del Código para la Cohesión del Proyecto: La definición de guías de estilo, el uso de linters y la adopción de "Conventional Commits" son cruciales en un proyecto con múltiples tecnologías. Hemos concluido que estas convenciones unifican la base del código, mejorando drásticamente su legibilidad y mantenibilidad, y facilitando la revisión entre pares.

12. **Trazabilidad Completa de Requisito a Despliegue:** Uno de los logros más notables es la trazabilidad completa que se puede seguir a lo largo del proyecto. Es posible rastrear una Historia de Usuario desde el backlog, pasando por sus pruebas en Gherkin, su implementación en una rama feature/, sus commits específicos, hasta su despliegue final. Este nivel de control es característico de equipos de alto rendimiento.

13. **Colaboración Efectiva y Distribuida:** La evidencia presentada (gráficos de red, actividad en Kanban, asignación de roles) pinta la imagen de un equipo altamente colaborativo y bien organizado. La distribución de responsabilidades, con líderes y colaboradores por aspecto, fomenta el ownership y asegura que todas las áreas del proyecto avancen en paralelo de forma coordinada.

14. **Validación de la Viabilidad del Modelo de Negocio:** Las entrevistas no solo validaron el producto, sino también su potencial de negocio. La disposición explícita de ambos segmentos de usuarios a pagar por una solución de este tipo proporciona una validación temprana del modelo de negocio, posicionando a RutaKids no solo como un proyecto técnico exitoso, sino como un producto potencialmente sostenible.

15. **Visión Holística y Ejecución Integral:** En resumen, nuestra conclusión final es que el proyecto RutaKids representa un ejemplo de ejecución holística. El equipo ha demostrado una capacidad sobresaliente para integrar la gestión de proyectos, el diseño de UX, la ingeniería de software, la garantía de calidad y la validación de negocio en un proceso cohesivo y bien documentado, culminando en una solución que es a la vez robusta técnicamente y profundamente humana.

\newpage

# Video About the team

Durante el Sprint 3, el equipo de desarrollo de RutaKids elaboró un video en el que se presenta a los integrantes del equipo, sus roles dentro del proyecto, y las principales tareas ejecutadas durante el desarrollo de las funcionalidades planificadas.

Este video tiene como objetivo evidenciar el trabajo colaborativo, la organización durante el ciclo de vida del proyecto, y la ejecución de entregables clave como la integración del dispositivo IoT, el despliegue de la app móvil, la aplicación web y los microservicios backend.

::: warn
Para visualizar el video del equipo, haga click en el siguiente enlace[URL]()
:::


![Imagen extraída del Video About the team](src/img/cap6/About-the-team.png)

\newpage

# Bibliografía
