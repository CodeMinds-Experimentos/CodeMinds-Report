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

# Capítulo IV: Product Design

El diseño del producto no solo refleja el propósito funcional de RutaKids, sino también sus valores fundamentales: seguridad, transparencia y eficiencia. 
En esta sección se detallan los principios visuales, patrones de interacción y estilos adoptados para asegurar una experiencia homogénea y accesible en todas las plataformas: web, móvil e IoT. Cada elemento de la interfaz ha sido concebido con base en las necesidades reales de nuestros usuarios, identificadas a través de entrevistas, mapas de empatía y journeys. El enfoque se centra en resolver problemas con soluciones visuales limpias, directas y adaptadas al entorno educativo.

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

**Branding:**

*Rutakids* es una solución tecnológica pensada para brindar seguridad y control en el transporte escolar. Su identidad visual refleja confianza, cercanía y modernidad, valores clave para padres y colegios. La plataforma busca simplificar la experiencia de seguimiento escolar a través de una interfaz clara, accesible y conectada en tiempo real.
Cada elemento del branding (colores, tipografía y estilo visual) está diseñado para reforzar la misión de *RutaKids*: ofrecer tranquilidad a las familias y eficiencia a las instituciones, con una experiencia intuitiva y coherente en todos sus canales digitales.

**Logotipo:**

El logotipo de *RutaKids* fue diseñado para representar visualmente los valores fundamentales de la solución: movimiento, seguridad y tecnología accesible. Su símbolo principal es una rueda estilizada en movimiento, lo cual hace alusión directa al concepto de transporte escolar eficiente y monitoreado en tiempo real.
La elección del color azul vibrante busca transmitir confianza, profesionalismo y tranquilidad, mientras que las formas redondeadas del logotipo refuerzan la cercanía y la facilidad de uso que caracterizan a la plataforma. Además, se han definido variantes del logotipo para asegurar su correcta adaptación en diferentes fondos y contextos, sin comprometer la legibilidad ni la identidad visual del producto.

![Artefacto creado en Figma](src/img/cap4/LogoStyle.png)


**Iconografía de la Aplicación**

La iconografía de *RutaKids* se basa en el uso del imagotipo de la marca (una rueda estilizada en movimiento) como símbolo principal en su versión para dispositivos móviles. Este elemento mantiene la coherencia gráfica de la marca al tiempo que asegura versatilidad y reconocimiento en pantallas reducidas. Además, para garantizar su legibilidad y funcionalidad, se desarrollaron distintas variantes del ícono, adaptables a diferentes fondos y contextos de uso. Su forma simplificada y su alto contraste permiten una fácil identificación desde la pantalla de inicio de cualquier dispositivo, reforzando la presencia visual de *RutaKids* dentro de su ecosistema digital.

![Artefacto creado en Figma](src/img/cap4/Icon_App.png)

**Colores**

La paleta de colores de *RutaKids* está estructurada en dos grupos principales: los colores utilizados en la interfaz de usuario y aquellos aplicados en las variantes del logotipo e iconos. Esta clasificación permite mantener una coherencia visual sólida, adaptando el uso del color según su función en la experiencia del usuario y en la identidad de marca.

- **Colores Principales (Interfaz de la Aplicación)**

  Estos colores se aplican en la landing page, la aplicación web y la app móvil. Su selección busca optimizar la legibilidad, facilitar la navegación y establecer jerarquías visuales claras.
    
  - **Azul (#2979FF):** Color principal de acento, utilizado en botones, enlaces, íconos activos y llamadas a la acción. Simboliza tecnología, dinamismo y confiabilidad, atributos clave para una plataforma tecnológica dirigida al entorno infantil y familiar. Su intensidad favorece la visibilidad y guía la atención del usuario hacia las zonas de interacción.
  
  - **Blanco (#FFFFFF):** Funciona como fondo predominante en la interfaz. Su neutralidad permite maximizar la claridad, mejorar la percepción del contenido y generar una sensación de amplitud visual. Es fundamental para evitar la saturación cromática y facilitar la lectura en distintos dispositivos.
  
  - **Gris (#93868A):** Aplicado en textos secundarios, descripciones, etiquetas y componentes del dashboard. Este tono contribuye a una organización jerárquica de la información, diferenciando elementos sin provocar distracción visual. Su uso estratégico mejora la legibilidad y evita el contraste excesivo.
  
  - **Negro (#000000):** Utilizado en títulos, encabezados y textos primarios. Su alto contraste frente al blanco garantiza máxima legibilidad, especialmente en contenido textual de alta relevancia. Además, refuerza el énfasis visual y aporta un carácter formal a la estructura gráfica

  ![Artefacto creado en Figma](src/img/cap4/PrimaryColors.png)

- **Colores Secundarios (Variantes de Logos e Iconos)**

  Estos tonos de azul se emplean para asegurar que el logotipo y los íconos mantengan su visibilidad y coherencia visual en diferentes fondos y dispositivos. Las variantes permiten adaptar la marca sin perder identidad.

  - **Azul (#256CE4):** Empleado principalmente en variantes del logotipo sobre fondos claros. Ofrece buena visibilidad sin generar un contraste excesivo, manteniendo una apariencia amigable y moderna.
  
  - **Azul (#205EC6):** Alternativa versátil que proporciona equilibrio visual entre contraste y presencia de marca. Es útil para contextos digitales y materiales impresos donde se requiere mantener una estética sobria sin perder fuerza gráfica.
  
  - **Azul Oscuro (#123672):** Aplicado sobre fondos oscuros o saturados. Este tono profundo refuerza la elegancia, seriedad y profesionalismo de la marca, siendo apropiado para presentaciones formales, documentación institucional o entornos corporativos.
  
  ![Artefacto creado en Figma](src/img/cap4/SecondColors.png)

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

**Sistema de Grillas:**

![**Sistema de Grillas** - Artefacto creado en Figma](src/img/cap4/Grid.png)

\newpage

**Botones y Enlaces:**

![**Botones y Enlaces** - Artefacto creado en Figma](src/img/cap4/Button_Link.png){ height=90%}

\newpage

**Campos de Entrada:**

![**Campos de Entrada** - Artefacto creado en Figma](src/img/cap4/Input_fields.png)

\newpage

**Diálogos Emergentes:**

![**Diálogos Emergentes** - Artefacto creado en Figma](src/img/cap4/Dialog.png){ height=90% }

\newpage

**Pestañas de Navegación (Tabs):**

![**Pestañas de Navegación (Tabs)** - Artefacto creado en Figma](src/img/cap4/Tabs.png){ height=90% }

\newpage

**Rutas de Navegación (Breadcrumbs):**

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

\newpage

A continuación se presentan los mapas generales de arquitectura de información correspondientes a cada tipo de usuario:

**Arquitectura de Información – App Móvil para Padres**

![Artefacto creado en Figma](src/img/cap4/AppPadres.png){ width=85% }

**Arquitectura de Información – App Móvil para Conductores**

![Artefacto creado en Figma](src/img/cap4/AppConductores.png){ width=85% }

\newpage

**Arquitectura de Información – Plataforma Web para Administradores**

![Artefacto creado en Figma](src/img/cap4/AppWeb.png){ width=90% }

Las secciones siguientes profundizan en los sistemas implementados para organización, etiquetado, navegación y búsqueda, así como en los elementos de SEO (Search Engine Optimization) y ASO (App Store Optimization) que fortalecen la visibilidad del producto.

\newpage

### Organization Systems.

- **Propósito**

  La arquitectura organizativa de un producto digital permite estructurar la información de forma que los usuarios accedan rápida y eficientemente a los contenidos que necesitan. 

  > Según Morville y Rosenfeld (2006), “los sistemas de organización son esenciales para transformar el caos en claridad, facilitando que los usuarios comprendan la lógica detrás del contenido digital”. 

  En el caso de *RutaKids*, se han diseñado diversos sistemas de organización visual y estructural adaptados tanto a padres como a administradores educativos.

- **Organización para padres de familia (App móvil)**

  La aplicación móvil muestra la información más relevante sobre el estado de sus hijos y el transporte escolar. La información sigue un modelo jerárquico en su interfaz principal y secuencial en el monitoreo de rutas.

\begin{longtable}{|p{3cm}|p{3cm}|p{3cm}|p{5cm}|}
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

\newpage

- **Organización para administradores educativos (Plataforma web)**

  La plataforma web está orientada a la administración y seguimiento operativo. Utiliza una estructura modular con categorización por tópicos y por audiencia (vehículos, estudiantes, rutas, conductores).

\begin{longtable}{|p{3cm}|p{3cm}|p{3cm}|p{5cm}|}
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

\begin{longtable}{|p{3cm}|p{3cm}|p{3cm}|p{5cm}|}
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

\newpage

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

::: warn
Para acceder a los wireframes de la landing page, haga click en la [URL](https://www.figma.com/design/hWQCYGLq8uiSZolh8ChRN7/Untitled?node-id=0-1&t=r3o6PxgMClNo9kx7-1)
:::

### Landing Page Wireframe.

Los wireframes representan la estructura básica de la landing page, enfocándose en la disposición de los elementos sin distraer con colores o estilos visuales complejos. Esta etapa fue clave para definir la jerarquía de la información, la ubicación de llamados a la acción (CTAs) y la secuencia de navegación esperada. Cada sección fue diseñada para cumplir un objetivo específico dentro del recorrido del usuario, desde la presentación inicial hasta los beneficios, características, segmentos objetivo (padres y colegios), equipo, demostración y contacto. El uso de wireframes permitió validar la lógica de la interfaz antes de pasar a etapas más detalladas de diseño visual.

**Landing Page Wireframe 1:**

![Figma CodeMinds Wireframe](https://i.postimg.cc/Jh7nbHyD/wireframe-inicio.png)

\newpage

**Landing Page Wireframe 2:**

![Figma CodeMinds Wireframe](https://i.postimg.cc/CxgdxQS4/wireframe-beneficios.png)

**Landing Page Wireframe 3:**

![Figma CodeMinds Wireframe](https://i.postimg.cc/J4JGmLVn/wireframe-caracteristicas.png)

\newpage

**Landing Page Wireframe 4:**

![Figma CodeMinds Wireframe](https://i.postimg.cc/FFYYWST0/wireframe-padres.png)

**Landing Page Wireframe 5:**

![Figma CodeMinds Wireframe](https://i.postimg.cc/66FyDQPg/wireframe-colegios.png)

\newpage

**Landing Page Wireframe 6:**

![Figma CodeMinds Wireframe](https://i.postimg.cc/jCV0vmZ3/wireframe-team.png)

**Landing Page Wireframe 7:**

![Figma CodeMinds Wireframe](https://i.postimg.cc/C1QVnzDg/wireframe-demo.png)

\newpage

**Landing Page Wireframe 8:**

![Figma CodeMinds Wireframe](https://i.postimg.cc/0QQsNpzn/wireframe-contactanos-footer.png)

\newpage

### Landing Page Mock-up.

Los mockups son representaciones de alta fidelidad de la interfaz, incorporando el estilo visual definitivo, paleta de colores, tipografías, imágenes y demás elementos gráficos. En esta etapa, se reflejó la identidad visual de la plataforma, asegurando coherencia entre el mensaje y la estética. Los mockups también permiten evaluar aspectos como el contraste, el espaciado, la legibilidad y el impacto visual de cada sección. Gracias a esta representación visual detallada, fue posible obtener retroalimentación específica y realizar ajustes antes de iniciar la implementación del diseño en código.

::: warn
Para acceder a los mockups de la landing page, haga click en la [URL](https://www.figma.com/design/hWQCYGLq8uiSZolh8ChRN7/Untitled?node-id=0-1&t=r3o6PxgMClNo9kx7-1)
:::

**Landing Page Mockups 1:**

![Figma CodeMinds Mockups](https://i.postimg.cc/Kj3hPxrg/mockup-inicio.png)

\newpage


**Landing Page Mockups 2:**

![Figma CodeMinds Mockups](https://i.postimg.cc/q7prPf09/mockup-beneficios.png)

**Landing Page Mockups 3:**

![Figma CodeMinds Mockups](https://i.postimg.cc/k5wC9jgD/mockup-caracteristicas.png)

\newpage

**Landing Page Mockups 4:**

![Figma CodeMinds Mockups](https://i.postimg.cc/RZ79pCr7/mockup-padres.png)

**Landing Page Mockups 5:**

![Figma CodeMinds Mockups](https://i.postimg.cc/RZ54T6YC/mockup-colegios.png)

\newpage

**Landing Page Mockups 6:**

![Figma CodeMinds Mockups](https://i.postimg.cc/BQ1JDcMw/mockup-team.png)

**Landing Page Mockups 7:**

![Figma CodeMinds Mockups](https://i.postimg.cc/kMHnBhFb/mockup-demo.png)

\newpage

**Landing Page Mockups 8:**

![Figma CodeMinds Mockups](https://i.postimg.cc/2y1r04my/mockup-contactanos-footer.png)

\newpage

## Mobile Applications UX/UI Design.

El diseño UX/UI de aplicaciones móviles busca crear experiencias intuitivas, eficientes y agradables que respondan a las necesidades reales de los usuarios.
A través de un enfoque centrado en el usuario, se desarrollan interfaces funcionales y flujos de navegación claros que mejoran la interacción y fomentan la confianza en los servicios digitales.
Este proyecto aplica principios de usabilidad, accesibilidad y diseño visual para garantizar que cada tutor legal pueda monitorear y gestionar el transporte escolar de manera segura, sencilla y confiable.

### Mobile Applications Wireframes.

Los wireframes de aplicaciones móviles son representaciones visuales que permiten planificar la estructura y funcionalidad de la interfaz antes de su desarrollo.
A través de esquemas de baja y alta fidelidad, se definen la disposición de elementos, los flujos de navegación y las interacciones clave, asegurando que las necesidades del usuario se aborden de manera efectiva.

Este proyecto presenta wireframes que priorizan la claridad, la usabilidad y la accesibilidad, facilitando una supervisión intuitiva del transporte escolar por parte de los tutores legales.

::: warn
Para acceder a los wireframes de la mobile app, haga click en la [URL](https://www.figma.com/design/ph6aTjM4mzxkNic0Hk4VLX/RutaKids?node-id=275-3006&t=8oFGZm5oHMybkhay-1)
:::

**Mobile Application Wireframes - Splash:**

![Figma CodeMinds Wireframes](src/img/cap4/mobile-wireframes/splash.png){ height=35% }

\newpage

**Mobile Application Wireframes - Bienvenida:**

![Figma CodeMinds Wireframes](src/img/cap4/mobile-wireframes/bienvenida.png){ height=35% }

**Mobile Application Wireframes - Login:**

![Figma CodeMinds Wireframes](src/img/cap4/mobile-wireframes/login.png){ height=35% }

\newpage

**Mobile Application Wireframes - Recuperar Contraseña:**

![Figma CodeMinds Wireframes](src/img/cap4/mobile-wireframes/recuperar-password.png){ height=35% }

**Mobile Application Wireframes - Home:**

![Figma CodeMinds Wireframes](src/img/cap4/mobile-wireframes/principal.png){ height=35% }

\newpage

**Mobile Application Wireframes - Home - Notificaciones:**

![Figma CodeMinds Wireframes](src/img/cap4/mobile-wireframes/principal-notificaciones.png){ height=35% }

**Mobile Application Wireframes - Home - Notificaciones - Popup:**

![Figma CodeMinds Wireframes](src/img/cap4/mobile-wireframes/principal-notificaciones-popup.png){ height=35% }

\newpage

**Mobile Application Wireframes - Home - Detalles:**

![Figma CodeMinds Wireframes](src/img/cap4/mobile-wireframes/principal-detalles.png){ height=35% }

**Mobile Application Wireframes - Home - Detalles - Popup:**

![Figma CodeMinds Wireframes](src/img/cap4/mobile-wireframes/principal-detalles-popup.png){ height=35% }

\newpage

**Mobile Application Wireframes - Monitoreo:**

![Figma CodeMinds Wireframes](src/img/cap4/mobile-wireframes/monitoreo.png){ height=35% }

**Mobile Application Wireframes - Monitoreo - Cam:**

![Figma CodeMinds Wireframes](src/img/cap4/mobile-wireframes/monitoreo-cam.png){ height=35% }

\newpage

**Mobile Application Wireframes - Historial:**

![Figma CodeMinds Wireframes](src/img/cap4/mobile-wireframes/historial.png){ height=35% }

**Mobile Application Wireframes - Cuenta:**

![Figma CodeMinds Wireframes](src/img/cap4/mobile-wireframes/cuenta.png){ height=35% }

\newpage

**Mobile Application Wireframes - Cuenta - Settings:**

![Figma CodeMinds Wireframes](src/img/cap4/mobile-wireframes/cuenta-settings.png){ height=35% }

\newpage

### Mobile Applications Wireflow Diagrams.

En esta sección se presentan los wireflows diseñados para RutaKids. A través de estos diagramas, se busca representar de manera clara y estructurada cómo los padres de familia o tutores legales pueden navegar por la app, realizar tareas esenciales como el inicio de sesión, la visualización de trayectos en tiempo real, la recepción de notificaciones, el acceso al historial de viajes, entre otros.

Cada wireflow incluye tanto los objetivos del usuario como la descripción paso a paso del flujo de tareas, facilitando así la comprensión del recorrido de usuario y la funcionalidad de la aplicación.

**Wireflow Diagram 1: Inicio de Sesión**

- **User Goal**

  El tutor legal desea acceder a la aplicación móvil para monitorear el transporte escolar de su hijo/a.

- **Task Flow (Flujo de tareas del usuario)**

  1. Visualiza la pantalla de carga con el logo de la aplicación al abrir la app por primera vez.
  2. Visualiza la pantalla con información de lo que ofrece la aplicación
  3. Accede a la pantalla de inicio de sesión.
  4. Ingresa sus credenciales (correo electrónico y contraseña).
  5. En caso de haber olvidado la contraseña, solicita su recuperación mediante correo electrónico.
  6. Si las credenciales son válidas, el sistema redirige a la pantalla de carga mientras valida la sesión.
  7. Finalmente, accede a la pantalla principal (dashboard) desde donde podrá realizar el monitoreo del transporte.

A continuación, se muestran de forma secuencial las pantallas involucradas en el proceso de inicio de sesión de un tutor legal, detallando las interacciones principales y transiciones posibles desde la carga inicial de la aplicación hasta el acceso exitoso al panel de monitoreo.

\newpage

**Wireflow:  Inicio de Sesión**

![Artefacto creado en Figma](src/img/cap4/WD/WD_SignIn.png)

\newpage

**Wireflow Diagram 2: Visualización de eventos del recorrido (línea de tiempo)**

- **User Goal**  

  El tutor legal desea consultar el estado y el avance del recorrido escolar para asegurar el cumplimiento del trayecto.

- **Task Flow (Flujo de tareas del usuario)**

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

**Wireflow:  Timeline Details**

![Artefacto creado en Figma](src/img/cap4/WD/WD_Details.png){ width=90% }

\newpage

**Wireflow Diagram 3: Notificaciones de eventos**

- **User Goal**  

  El tutor legal desea recibir alertas sobre momentos importantes del viaje, como el inicio del recorrido o la llegada al punto de encuentro, para mantenerse informado sobre el trayecto de su hijo/a.

- **Task Flow (Flujo de tareas del usuario)**

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

**Wireflow: Notificaciones**

![Artefacto creado en Figma](src/img/cap4/WD/WD_Notifications.png){ width=90% }

\newpage

**Wireflow Diagram 4: Visualización del trayecto del transporte escolar en mapa en tiempo real**

- **User Goal**  

  El tutor legal desea visualizar en tiempo real la ruta que sigue la unidad de transporte escolar, con información resumida del conductor, clima y estado del viaje.

- **Task Flow (Flujo de tareas del usuario)**

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

**Wireflow: Home a Monitoreo**

![Artefacto creado en Figma](src/img/cap4/WD/WD_LiveMap.png)

\newpage

**Wireflow Diagram 5: Visualización en vivo del interior de la unidad**

- **User Goal**  

  El tutor legal desea observar visualmente la unidad de transporte en tiempo real para verificar las condiciones internas y confirmar que su hijo/a viaja de forma segura.

- **Task Flow (Flujo de tareas del usuario)**

  1. Desde la pantalla de Detalles del viaje (mapa con ruta y datos del transporte), el tutor identifica el botón "Visualizar Unidad".
  2. Presiona el botón y es redirigido a una nueva vista.
  3. La aplicación muestra una transmisión en tiempo real del interior del vehículo.
  4. En la parte inferior de la pantalla se presenta:

     - La temperatura interna del vehículo.
     - El botón de regreso para volver a la vista anterior.

  5. El tutor puede observar sin interactuar y cerrar la vista cuando lo desee.
  6. Al cerrar la visualización, vuelve a la pantalla de “Detalles del viaje”.

**Wireflow: Visualizar Cámara**

![Artefacto creado en Figma](src/img/cap4/WD/WD_LiveInteriorView.png)

Esta vista permite monitorear visualmente las condiciones internas del vehículo, incluyendo el comportamiento de los estudiantes y el estado del entorno. Además, se ofrece la temperatura interna del bus como dato adicional. Esta funcionalidad está diseñada para reforzar la percepción de seguridad y confianza del tutor legal durante el trayecto escolar.

\newpage

**Wireflow Diagram 6: Consulta de historial de viajes**

- **User Goal**  

  El tutor legal desea revisar los viajes anteriores para verificar detalles como la hora de salida y llegada, la ruta recorrida y las condiciones generales del transporte escolar.

- **Task Flow (Flujo de tareas del usuario)**

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

**Wireflow: Historial de Viajes**

![Artefacto creado en Figma](src/img/cap4/WD/WD_Record.png)

Este wireflow corresponde a la funcionalidad de consulta del historial de viajes previos. Al acceder desde el menú principal, el tutor visualiza una lista de recorridos completados, organizados por fecha.

\newpage

**Wireflow Diagram 7: Gestión de cuenta**

- **User Goal**  

  El tutor legal desea configurar y gestionar sus datos personales, seguridad, privacidad y notificaciones desde su perfil en la aplicación.

- **Task Flow (Flujo de tareas del usuario)**

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

**Wireflow: Gestión de Cuenta**

![Artefacto creado en Figma](src/img/cap4/WD/WD_AccountConfiguration.png)

\newpage


### Mobile Applications Mock-ups.

En esta sección se presentan los mockups de la aplicación RutaKids, los cuales representan visualmente las principales pantallas y funcionalidades diseñadas. Estas interfaces han sido construidas siguiendo principios de diseño centrado en el usuario, diseño inclusivo, accesibilidad y consistencia visual, conforme al Design System definido para este producto digital.

**Inicio de sesión - Mock-up**

![Artefacto creado en Figma](src/img/cap4/Mockups/SignIn.png)

**Notificaciones - Mock-up**

![Artefacto creado en Figma](src/img/cap4/Mockups/Notifications.png)

\newpage

**Visualización del mapa - Mock-up**

![Artefacto creado en Figma](src/img/cap4/Mockups/Details.png)

**Cámara activada - Mock-up**

![Artefacto creado en Figma](src/img/cap4/Mockups/LiveInteriorView.png)

\newpage

**Historial de viajes - Mock-up**

![Artefacto creado en Figma](src/img/cap4/Mockups/Record.png)

**Gestión de cuenta - Mock-up**

![Artefacto creado en Figma](src/img/cap4/Mockups/AccountConfiguration.png)

\newpage

### Mobile Applications User Flow Diagrams.
En esta sección se presentan los flujos de usuario diseñados para RutaKids, enfocados en ofrecer a los tutores legales una experiencia clara, segura y eficiente en el monitoreo del transporte escolar de sus hijos/as.
Cada diagrama describe paso a paso cómo el usuario interactúa con la aplicación para cumplir sus objetivos principales, contemplando rutas típicas, alternativas y escenarios excepcionales.
Estos flujos buscan garantizar la transparencia, la facilidad de uso y la confianza en cada interacción, abordando funcionalidades clave como el acceso al sistema, la visualización en tiempo real del trayecto, la recepción de notificaciones, la consulta de historial de viajes y la gestión de la cuenta personal.

**Inicio de Sesión**

- **User Goal**

  El tutor legal desea acceder a la aplicación móvil para monitorear el transporte escolar de su hijo/a.


![Artefacto creado en Figma](src/img/cap4/UF/SignIn.png)

Este User Flow inicia con la carga del sistema y guía al tutor legal hacia la pantalla de login, donde se permite ingresar sus credenciales o iniciar el proceso de recuperación de contraseña. Se ha considerado un flujo alternativo para usuarios que olvidan su contraseña, así como una condición de éxito que los redirige a la pantalla principal. El proceso incluye interacciones simples y claras, con rutas diferenciadas para escenarios típicos y excepcionales.

**Visualización de eventos del recorrido (línea de tiempo)**

- **User Goal**  

  El tutor legal desea consultar el estado y el avance del recorrido escolar para asegurar el cumplimiento del trayecto.

![Artefacto creado en Figma](src/img/cap4/UF/Details.png)

Este diagrama de flujo de usuario muestra el proceso mediante el cual el tutor legal accede a la línea de tiempo del recorrido escolar actual. Desde la pantalla principal, el usuario selecciona el botón “Detalles”, lo que lo redirige a una vista que presenta los hitos del viaje en orden cronológico.
La línea de tiempo muestra eventos clave como el inicio del trayecto, el abordaje de los estudiantes, el trayecto en curso, y la llegada al colegio.
Para una trazabilidad más detallada, algunos eventos incluyen íconos interactivos que permiten abrir ventanas modales con información adicional, como los nombres de los estudiantes que abordaron y la placa del vehículo. Esta funcionalidad permite al tutor monitorear el cumplimiento del servicio de transporte escolar de forma clara y precisa, fomentando la transparencia y confianza en el proceso.

\newpage

**Notificaciones de eventos**

- **User Goal**  

  El tutor legal desea recibir alertas sobre momentos importantes del viaje, como el inicio del recorrido o la llegada al punto de encuentro, para mantenerse informado sobre el trayecto de su hijo/a.

![Artefacto creado en Figma](src/img/cap4/UF/Notifications.png)

Este diagrama representa el flujo de usuario para acceder a las notificaciones generadas automáticamente por la aplicación durante el recorrido escolar.
El tutor legal, desde la pantalla principal, puede visualizar un ícono de campana que indica nuevas alertas. Al presionarlo, se accede a una lista cronológica de eventos relevantes, como el inicio del recorrido o la llegada al punto de encuentro.
Cada notificación incluye iconografía, texto descriptivo, hora y fecha. Al seleccionar una notificación específica, se despliega una tarjeta con información extendida del evento.
Esta funcionalidad permite al tutor mantenerse informado en tiempo real, fortaleciendo el acompañamiento del trayecto sin necesidad de interacción directa con el sistema de transporte.

\newpage

**Visualización del trayecto del transporte escolar en mapa en tiempo real**

- **User Goal**  

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

- **User Goal**  

  El tutor legal desea observar visualmente la unidad de transporte en tiempo real para verificar las condiciones internas y confirmar que su hijo/a viaja de forma segura.

![Artefacto creado en Figma](src/img/cap4/UF/LiveInteriorView.png)

Este flujo de usuario muestra la funcionalidad que permite al tutor legal acceder a una vista en tiempo real del interior del vehículo escolar.
Desde la pantalla de “Detalles del viaje”, el tutor puede presionar el botón “Visualizar unidad”, lo cual redirige a una vista dedicada donde se transmite un video en vivo del interior del bus.
Esta transmisión permite observar las condiciones internas, incluyendo el comportamiento de los estudiantes y el ambiente dentro de la unidad durante el trayecto.
Además, se muestra la temperatura interna del vehículo en la parte inferior de la pantalla como dato contextual relevante.
Esta funcionalidad tiene como objetivo principal fortalecer la confianza y seguridad del tutor legal, proporcionando una capa adicional de supervisión visual.

\newpage

**Consulta de historial de viajes**

- **User Goal**  

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

- **User Goal**  

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

![Recurso extraído de Canva](src/img/cap4/mobile-applications-prototyping.png)

**Justificación de decisiones de diseño e interacción**

El diseño de interacción responde a una arquitectura de información centrada en el usuario, basada en jerarquías claras y flujos de navegación predecibles. Para ello se han definido rutas esperadas (happy paths) que guían al tutor legal desde el acceso inicial a la aplicación hasta funcionalidades clave como el monitoreo en tiempo real, la recepción de notificaciones o la gestión de cuenta personal.

El sistema de navegación utiliza una barra inferior persistente, con íconos universalmente reconocibles, que agrupa las secciones principales: Inicio, Monitoreo, Historial y Cuenta. Esta estructura se eligió por su efectividad en dispositivos móviles, permitiendo que el usuario navegue sin esfuerzo entre vistas relacionadas sin necesidad de regresar a menús superiores.

**Consistencia y adaptabilidad**

A pesar de que los prototipos fueron desarrollados inicialmente con frames de iOS para facilitar el testeo visual, todas las decisiones fueron tomadas considerando el desarrollo futuro con Flutter como framework multiplataforma. Esto asegura que los elementos visuales, tamaños de fuente, márgenes y estilos de interacción son adaptables a sistemas operativos Android, y que cualquier ajuste de microinteracción puede realizarse posteriormente sin romper la coherencia de experiencia.

\newpage

### Android Mobile Applications Prototyping.

La versión prototipada corresponde a la arquitectura funcional de Android, replicando los mismos flujos de navegación definidos para iOS.
Gracias al enfoque cross-platform con Flutter, las decisiones de interacción son consistentes entre sistemas.

::: warn
Para acceder al prototipo de la Android Mobile, haga click en la [URL](https://www.figma.com/proto/eciWGdnbz2vbcafpC3ry61/RutaKids?node-id=1-191&t=Q43WuZLUjqqKj29U-1&scaling=scale-down&content-scaling=fixed&page-id=0%3A1&starting-point-node-id=1%3A191)
:::

::: warn
Para ver la demo en Microsoft Stream - Min(00:33), haga click en la [URL](https://upcedupe-my.sharepoint.com/:v:/g/personal/u202210059_upc_edu_pe/EWNyaDk6mgdMlrmkd3YCekQBkWfpMUBC7oBkGaqmv3HQIA?e=ZCJBW6&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D)
:::


![Android Prototyping - Figma](src/img/cap4/android-proto.png)

\newpage

### iOS Mobile Applications Prototyping.

La interfaz se prototipó inicialmente para iOS siguiendo las guías de diseño de Apple (Human Interface Guidelines), aplicando principios de accesibilidad y navegación móvil.

::: warn
Para acceder al prototipo de la iOS Mobile, haga click en la [URL](https://www.figma.com/proto/eciWGdnbz2vbcafpC3ry61/RutaKids?node-id=5-1336&t=xAeh2weCXXUvbcOx-1&scaling=scale-down&content-scaling=fixed&page-id=5%3A1185&starting-point-node-id=5%3A1336)
:::

::: warn
Para ver la demo en Microsoft Stream - Min(01:57), haga click en la [URL](https://upcedupe-my.sharepoint.com/:v:/g/personal/u202210059_upc_edu_pe/EWNyaDk6mgdMlrmkd3YCekQBkWfpMUBC7oBkGaqmv3HQIA?e=ZCJBW6&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D)
:::

![iOS Prototyping - Figma](src/img/cap4/ios-proto.png)

\newpage

## *Web Applications UX/UI Design.*

![Recurso estraído de Google](src/img/cap4/angular.jpg)

En esta sección se presenta el proceso de diseño UX/UI desarrollado para la aplicación web de RutaKids, centrado en ofrecer una experiencia funcional, accesible y coherente con las necesidades de sus principales usuarios: colegios, padres de familia y operadores de transporte escolar. A partir de una investigación previa, se definieron flujos clave, se estructuraron wireframes en baja fidelidad y se evolucionó hacia interfaces modernas, basadas en principios de usabilidad y diseño centrado en el usuario. El objetivo es garantizar que cada interacción dentro del sistema sea intuitiva, segura y alineada a los objetivos del proyecto.

::: warn
Para visualizar todo el diseño de los wireframes y mockups de la aplicación, haga click en la [URL](https://app.uizard.io/p/726b9d4c)
:::

\newpage

### *Web Applications Wireframes.*

**Inicio de sesión - Wireframe**

![Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/sign_in.png){ height=38% }

**Recuperación de contraseña - Wireframe**

![Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/forgot_password.png){ height=38% }

\newpage

**Reinicio de contraseña - Wireframe**

![Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/reset_password.png){ height=38% }

**Cambio de contraseña - Wireframe**

![Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/change_password.png){ height=38% }

\newpage

**Dashboard general - Wireframe**

![Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/dashboard.png){ height=38% }

**Notificaciones - Wireframe**

![Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/notifications.png){ height=38% }

\newpage

**Preguntas frecuentes - Wireframe**

![Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/faq.png){ height=38% }

**Política de privacidad - Wireframe**

![Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/privacy_policy.png){ height=38% }

\newpage

**Cerrar sesión - Wireframe**

![Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/log_out.png){ height=38% }

**Terminos y condiciones - Wireframe**

![Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/terms.png){ height=38% }

\newpage

**Gestión de estudiantes**

**Crear estudiante - Wireframe**

![Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/create_student.png){ height=38% }

**Lista de estudiantes - Wireframe**

![Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/students_list.png){ height=38% }

\newpage

**Tarjetas de estudiantes - Wireframe**

![Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/students_cards.png){ height=38% }

**Gestión de movilidades y rutas escolares**

**Crear movilidad escolar - Wireframe**

![Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/create_school_trans.png){ height=38% }

\newpage

**Listado de movilidades - Wireframe**

![Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/school_trans_list.png){ height=38% }

**Crear ruta escolar - Wireframe**

![Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/create_school_routes.png){ height=38% }

\newpage

**Listado de rutas escolares - Wireframe**

![Artefacto creado en Uizard](src/img/cap4/rutakids_wireframes/school_routes_list.png){ height=38% }

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

**Inicio de sesión - Mock-up**

![Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/sign_in.png){ height=35% }

**Recuperación de contraseña - Mock-up**

![Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/forgot_password.png){ height=35% }

\newpage

**Reinicio de contraseña - Mock-up**

![Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/reset_password.png){ height=38% }

**Cambio de contraseña - Mock-up**

![Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/change_password.png){ height=38% }

\newpage

**Navegación y funcionalidades complementarias**

**Dashboard general - Mock-up**

![Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/dashboard.png){ height=38% }

**Notificaciones - Mock-up**

![Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/notifications.png){ height=38% }

\newpage

**Preguntas frecuentes - Mock-up**

![Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/faq.png){ height=38% }

**Política de privacidad - Mock-up**

![Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/privacy_policy.png){ height=38% }

\newpage

**Cerrar sesión - Mock-up**

![Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/log_out.png){ height=38% }

**Terminos y condiciones - Mock-up**

![Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/terms.png){ height=38% }

\newpage

**Gestión de estudiantes**

**Crear estudiante - Mock-up**

![Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/create_student.png){ height=38% }

**Lista de estudiantes - Mock-up**

![Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/students_list.png){ height=38% }

\newpage

**Tarjetas de estudiantes - Mock-up**

![Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/students_cards.png){ height=38% }

**Gestión de movilidades y rutas escolares**

**Crear movilidad escolar - Mock-up**

![Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/create_school_trans.png){ height=38% }

\newpage

**Listado de movilidades - Mock-up**

![Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/school_trans_list.png){ height=38% }

**Crear ruta escolar - Mock-up**

![Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/create_school_routes.png){ height=38% }

\newpage

**Listado de rutas escolares - Mock-up**

![Artefacto creado en Uizard](src/img/cap4/rutakids_mockups/school_routes_list.png){ height=38% }

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

![Captura de Microsoft Stream](src/img/cap4/web-application-prototyping-video.png)

\newpage

## Domain-Driven Software Architecture.

En esta sección se describe la arquitectura impulsada por el dominio para **CodeMinds**, nuestra solución de autenticación IoT enfocada en el transporte escolar seguro. Utilizamos principios de *Domain-Driven Design* (DDD) para estructurar los componentes de software de manera alineada con las necesidades del negocio, garantizando escalabilidad, robustez y claridad en la separación de responsabilidades.

El diseño de la solución de software constituye una etapa crítica para garantizar que el sistema responda de manera eficaz a las necesidades estratégicas del dominio de negocio identificado. A partir de la estructura de Bounded Contexts previamente definida, se propone una arquitectura modular basada en microservicios, donde cada servicio es responsable de una parte específica del dominio y se comunica a través de interfaces bien delimitadas.

En **RutaKids**, esta solución se implementa mediante una combinación de tecnologías modernas como **Spring Boot** para el desarrollo de microservicios, **Kafka** para la comunicación asíncrona basada en eventos, **OAuth2 / Keycloak** para la autenticación segura de usuarios, y **Angular 17** como framework principal para el frontend modularizado. Además, se adoptan principios de arquitectura orientada a eventos, utilizando técnicas como EventStorming, Domain Message Flow Modeling y Bounded Context Canvas para asegurar una alineación continua entre el diseño técnico y los objetivos de negocio.

![Recurso extraído de Canva](src/img/cap4/dddimage.png)

\newpage

### Software Architecture Context Diagram.

![System Context Level Diagram - C4](src/img/cap4/structurizr-SystemContext.png)

![System Context Level Diagram - C4](src/img/cap4/structurizr-SystemContext-keys.png)

\newpage

### Software Architecture Container Diagrams.

![System Container Level Diagram - C4](src/img/cap4/structurizr-Containers.png)

![System Container Level Diagram - C4](src/img/cap4/structurizr-Containers-keys.png)

\newpage

### Software Architecture Components Diagrams.

**Parent Service**

![Component Level Diagram](src/img/cap4/structurizr-ParentServiceComponents.png){ height=38% }

**IoT Service**

![Component Level Diagram](src/img/cap4/structurizr-IoTServiceComponents.png){ height=38% }

\newpage

**IoT Interceptor Service**

![Component Level Diagram](src/img/cap4/structurizr-InterceptorComponents.png){ height=90% }

\newpage

**Routes Service**

![Component Level Diagram](src/img/cap4/structurizr-RoutesServiceComponents.png)

\newpage

## Software Object-Oriented Design.

El diseño orientado a objetos (Object-Oriented Design, OOD) es un enfoque esencial en el desarrollo de sistemas de software modernos, ya que permite modelar soluciones complejas mediante la definición de objetos que interactúan entre sí dentro de un entorno bien estructurado. Este paradigma promueve la creación de sistemas más comprensibles, reutilizables y fáciles de mantener, al organizar la lógica del software en torno a clases y objetos que encapsulan datos y comportamientos. En este apartado se presenta el diseño orientado a objetos desarrollado para el sistema, haciendo uso de dos herramientas fundamentales: el Diagrama de Clases y el Diccionario de Clases. Estas herramientas proporcionan una visión clara y estructurada del sistema desde la perspectiva del diseño, antes de proceder a la implementación.

El Diagrama de Clases representa gráficamente las entidades del sistema, conocidas como clases, junto con sus atributos, métodos y relaciones. Este diagrama permite identificar las jerarquías de herencia, asociaciones, composiciones y otras relaciones entre clases, lo que facilita la comprensión del comportamiento esperado del sistema y sus interacciones internas. Además, sirve como puente entre el análisis de requisitos y la codificación, ayudando a validar que el diseño cumpla con las necesidades funcionales y no funcionales definidas previamente.

Por otro lado, el Diccionario de Clases proporciona una descripción detallada y textual de cada clase del sistema. Incluye información clave como el propósito de la clase, los atributos que contiene, los métodos que implementa, y las relaciones que mantiene con otras clases. Este diccionario actúa como una guía de referencia para desarrolladores y diseñadores, ya que establece un lenguaje común y consistente para todos los elementos que forman parte del sistema.

![Recurso extraído de Canva](src/img/cap4/object-oriented-design.png)

\newpage

### Class Diagrams.

**Rutakids - Infrastructure UML Diagram**

::: warn
Para una mejor visualización del diagrama, haga click en la [URL](https://mermaid.live/edit#pako:eNqNlVuPmkAUx7_KZJJ9c43gCisxJpalDWm9BNw-NCRmAiMSZcYMg61r_O493BpEusiLzOH_m3OZOccL9nlAsYH9A0mSt4iEgsQee3pC9uKrM3PXzru5fncsZC7nq-XCWqxdjyF4cj2arezNNyLpb3JGl-JD9kwmpXE6LYxXj9UxKxV0TzYuFScqMnAyyd4jn6K3KPE5WHM0xwrE5GwbhTdIYUKFqSH_Ts_-gZP9pto3J-yAMhnJM1oJfoqCe4psIawvgu8rH9YJCORKQUkcsRCtDkRuuYj_gVCpuW06S9dyftqm5VZbrYgAsnJfWW2-bpocnkqatAltJqnw6VFyUXpyrB-ztb1cuNm6Xvvn52nDIzKQyHdG03tpLYxPdbexfSq9K7iBSCp3Wb19UjIea8SYgbd3AVzQMEog8ZyoB9opbkT70Oa1GncDrfHfXkwDban0d5CvX9zOliS6iZZMHnPTTKebas2p5TBP5BAF-UFK6A7WejoPYi3ZPUi2uKx3rIGOggepDwzN-va_p9ygoBpJGt9QbUXphNoS64RwD8dUxCQKYArnM9TD0Dcx9bABrwERew_DsAEdNBR3z8zHhhQp7WHoxnCHjS05JLBKj1m5yhFeSY6E_eK8vsTGBf_Bhq73h5qiKYMXRR2NdU3r4TM21OGwP359HemKomnjsapee_gj5wd9fQRf9EytqergBQAaRFDRefkHkv30cCiyRMr4KIMZa_KUSWwor9e_vsU5ag)
:::

![UML Class Diagram - Mermaid](src/img/cap4/rutakids-infrastructure.png)

**Parent Service - Class Diagram**

::: warn
Para una mejor visualización del diagrama, haga click en la [URL](https://mermaid.live/edit#pako:eNq9V1Fv2jAQ_iuRpUpsAwS00BEhJAp0ikqhSmAPEy9eYiBqsCPb6cY6_vvsJJDEGAZMGi_E5-983_k7X5x34BIPARO4AWRs4MMlhes5vrkxhuOpNbWGzhwb4hdPGy-QIsyN98Qmf53OEHOfb7rdzPZpNrMGhu-ploghauWtDqc-XhoLnzI-hmt0OCWiqjMjn_FOf-UHXtdw5Z-glExv5zhPNsZcwfU6VsSFwQByZHz3KV_JJy2pmdiD6znJHcRaSmgN_eDQHIqYPwj11P1LprsGJQFiOaJC98F0otFcWIu0heG_aK4T9Qoy_xhWynZ91LNk2-2_PXyZONZ0YmvPno1CwnxO6KbIJbMXKC187PWCoPTBNGLdk0VUxMPG8kope4GchNwnGAZFtE6I69g8bJKFd0HDdLQjmRzuozpcEfRhM0slKCmS5NOVmG5RDGdof7X6OiEcRN98FxUppEZd0okXU5SQJaRgkwlFkj36uBYXEeqnjfMsKTKSGjUuCisdTmqRnrOiCP3JeGpPRqOhrdGhTzAXXSxQ22pmL7BYIl4Uw0YsJJihpA13FG0UV602ygqqsDqtLietCnYgly6PvXrH5bucyV81VJikkioH66n3-NSTyjqz56F9KOsTXLxCQYJFa5VaPCXzQ1hh5yb4ZIXhm9ymlN4aMQaXkt0bKXRosYMsdXiBm4BAr7R_dcbDI4cvKctH68vM7k2tyTifQS8MBfOFv9Rdl5KZiELZdArsPcghIxF1UYKR1SnuEdCJbepLYhSHdeQ4DTMH9TkwSKUinj6Kp-T-YxoryIxuhsu1z87valVpZ6ZUMsarDT4GFzpNhlXacgzNN4cMuWOxm6lUurkbhmmElHiRm2OQB-5f_kVcPpKE7V7WRdQucq7is-BH0lewJ7JXkKeTLxa3jkWIKBMVHnud9kkTlWWcxlDLL8PmJDINNy3ExE3npFbAOT5KJZzjostP9QNlIMzisuSJT5X4PM0BXyFxpQKmePQgfZ2DOd4KHIw4cTbYBSanESoDSqLlCpgLGDAxikJxzFD6nbODhBB_IyQ_BOY7-AnMer1Vbd3W7hvt1n2z0W6078tgI8ytdrVRb9417-q1erPVaG7L4Fe8QK3abDdrtdtGrfW53m7f3d2WAfLkXjynn1nyrwyWVGaSEkTYkwUUYS6Xbm7_AKSxSAY)
:::

![UML Class Diagram - Mermaid](src/img/cap4/parent-service-uml.png)

\newpage

**Routes Service - Class Diagram**

::: warn
Para una mejor visualización del diagrama, haga click en la [URL](https://mermaid.live/edit#pako:eNqtVlFv2jAQ_iuWpUrdRtGaBQYRQmKFblFpqRK6h4kXLznSqMGObKca6_rfZyehxEnatWi8kJy_83333fniBxywELCDg4QIMY1JxMlmRY-O0Oxq6S7dmb-iSP3yZeSxTAJ6KEz6NxrNqIzldjze2z7c3LhTFIcViy95TCNEyQaa1hBEwONUxoxWFuexkKM83jWLqRyjVP-JAvG4og1aOewAblOW_UwAJURhsxBaVhiN6ksulRABR4yHwFs5LTm5h-SbyoLx7QG0cktKOFDpNuxcJ2yY5ywgyZRIWMYbQEISLiGcyGcRQMP9ek5dlXy6XDTLrYwmfWV4a7mfrdcBm7-1Xi_V5YDw_0Vob3a98N3lwms7Xx6kTMTNttnbDYrrmIaTJDl-56D9makDvmzd8LhMRgEX-WkjiQF-SajDOH3ZXpcNfGy0846qEWJsSuTPvO_uWYs8PvD7OKhNodLYRiJ3EqY8usw1ZG6vybTD_lufN5GqesYgdiq9QqM9751MZ4urpbeYz2deU6kzRiVnSaLmlMFrbzeoRSANuTwQKaMCinE1MtWrObaqZ_rXhH9JzbcTr0nakLItl4ayNWkvJucXEy2wf3M58xrqiguyviOKksg2daL5kg4CtMY1KPD5DrN7XfVyWG5ACBKB4nrPjIGjshAF_ppsE0bCnUdavLb3adEa5-7XG2-ydBdXVfqTNFW013FU5NHQWK1knOgJYVAPiSSCZTyAAqN7RI054ue2-oCb52F9_V7cGlb4dIUROzlRT-_VU-Wj7aCAbdQggRCxNVIxzY9ngT85GZd7FPs5iMMaVIUDlcL4KU5lUo3-dLvmzHBQJgr0c9Mt92k92nvfMtJuQRN7-lI6KOUszIKWKFV84ytk-pURKufgKcg_Uqm5vC6TWiu3xEqBC7VJ7vSiS5mL7tkyQr3bnqAV1XUDFG1XeLX5PFex1_i2Ua774Q5W5g2JQ3Ubzo_ECstbUFcY7KjHkPC7FV7RR4UjmWT-lgbYkTyDDlbXsegWO2uSCPWWpeqkQHmV3kFSQn8wVn3FzgP-hR3L_twdDvq9z5bV7_WtXgdvsXM67HUty7ZOrb7dtwf2p8FjB__O_T927f7Atu3e4ONwOBgMrQ6GUCtxWd7j9V8HR1znUdLTdxB-xjIqsTN8_AsPXc6i)
:::

![UML Class Diagram - Mermaid](src/img/cap4/routes-service-uml.png)

**Iot Service - Class Diagram**

::: warn
Para una mejor visualización del diagrama, haga click en la [URL](https://mermaid.live/edit#pako:eNq1V21vmzAQ_ivI0qRsS6MkpXlBUaSsSTfUl1RAN2nKFy-4GSrYCJtoWdf_PgNm2IY2HdryIYHzvTx3z53tPIIt8RGwwDaElC4DuEtgtMFv3hirG8_27JW7wQb_5MvGEu2DLTIeC1n2mc1WmAXsMJ9Xsvd3d_bSCHxJ4rIkwDsDwwjVpewQI906hgnCzJZ9XAWUzVyEKUnmBs1_abH8tMEyykKnPUoNj5CmOGAvhFtCBluEzCVFMmqyZAtD7hN5QYQMxr8og1EsaSxJ-i1Exh6GKZJwceaW3rqBNS5V8XHBv2GtuR6tw7Uuf4uQ_6P8zup27dre2mkcHgfFhAaMJAcVayVXIN8H2F-EYeetZeT9XzjRNT4cbL8jsuOa65gFBMNQ1W6sWzs4Hw6F5zKqL95KlGJKj_DVNrYr-Ooo7KmxM_9zlRd35Xy2z5s4cVFS39eEsAlCYUU1UrJu03SLBY2dP9ovlOevEBUm9HWkVCif5aVF8Mzs9cRolaJwj6rFjjrQPiPcwZ6UY1uyeb6-8Zz11dXKaSD0nGCWkDBE2ilQyZU8doiprDqIxgRTVGzhM41kzbSRZM2D3iGNtf971BrzNd6b8qja4FgftMWTs6i3wAtQREdo43q5uLhcZDS7d9crR0ZoE-8S3j9k-Gga6ejypcw9whrAbaFfRF3t-f2iIw4Xvr1TuENKo-Um_BpChcEtPIQE-qVJXLxyEyWLWpNe2B_vnIVnr2_kFBZxzNHfBzueS624XJwmMNvCFfgRwTvioSgO-bmUdem1LJAUH-TiXMBttpNm-ppIP7WucpSu8cX2PmVCcdnbgMEGGOTkhD-940_idmUZvJwMBpgaHKQQNuvmVyPLSNCWJH6uXjqXToDZr15P244tI6VIcq9rq1ulrq2dMJKFvMdVViWmcuXkZC7dnDL4LE3kbGXF6s7ToCjHk5TFBqcYlCCk0atwPJeppny8LI0Gz1WlNm3PmcQooXzscrMjRkXe-XCJKMpAVClLBOYNl49GYVOzqDXJKy20RjlqVctNtwBdwMURDHz-vyof7g1g3xG_RAOLP_owediADX7iejBlxD3gLbBYkqIuSEi6-w6sexhS_pbGPp9s8afsjzSG-CshUWnCX4H1CH4AazDqjcaTs745NU8n5nh0NuqCAxePB73-dGqOh33zbDKdmOZTF_zMPfR7k_5w2B9MB6Ph4PTUHI67APlZHa7Fv8Lspwt2SZaLgIiwj3jPpZgByxw-_QYdRYMe)
:::

![UML Class Diagram - Mermaid](src/img/cap4/iot-service-uml.png)

\newpage

**Iot Interceptor Service - Class Diagram**

::: warn
Para una mejor visualización del diagrama, haga click en la [URL](https://mermaid.live/edit#pako:eNqVVN9v2jAQ_lcsPzE1RSWkSWpVSFXZJLROe4Cq0pQXYx_BIrEj22FjiP99TkIhgVTV_BDbd_fdffcj3mOmOGCCWUaNmQqaaponErlVS9BMLZ6VNGUOGu0bRbUeH7_T1Ya-CGNBgp5Mzqob1tg75NctSDuYWy1kinIwhqbwhaCtErxlX2jFnG4O0ig9pZYOzsfp4ifibu-gDolsU3yD5VyxDVhH1GqVZZdUTwYdmkutKGfU2HbghioHY4WkVijpoS6Zgu4yh7vO4uTuycW3_Z4-LsRFSk9F4ZJZiXQmLWgGhVUXOTXqUteuO3ltqsa89-wbZQ66G7hgF6IW4nergM5pZfzWFZUadC_RbnFaDG9eX2dT1KlQLeGwFQxmV3JTO-rIXxSjmXMNC5EDsu5jLM2LlsVUlcsM0JZmJVzQa8_t7e2kS5Sg44waNOk375kpgrgwBbVsfYb19qnCt_zVwZoafo7rjXuN7xv5nixPM_m_QA0MxLaJhz3sssip4O6ZqDucYLuGHBJM3JFTvUlwIg_OjpZWzXeSYWJ1CR7WqkzXmKxoZtytLNyfDMc35iQtqPylVP4OcVdM9vgPJv4oHgZ3cRjch_5DHPuxh3eYjKJoGPphMA7GfjiKRnF88PDf2sHdMIrjIIhGfhiF9w_jKPAwcOFK--P4xlWbh1NdpXJkCJKDflaltJiEY__wDzdZpJU)
:::

![UML Class Diagram - Mermaid](src/img/cap4/iot-interceptor-uml.png)

\newpage

### Class Dictionary.

::: scenario
**Class Dictionary – Infraestructura del Sistema**
:::

::: box
**API-Gateway**
:::

* **Estereotipo**: `<<Gateway>>`
* **Descripción**: Punto de entrada principal al sistema. Se encarga de enrutar las solicitudes externas hacia los microservicios correspondientes.
* **Responsabilidades**:

  * Encaminamiento de solicitudes a `Parent_Service`, `IoT_Service` y `Routes_Service`.
  * Redirección de autenticaciones hacia `Keycloak_Service`.

* **Relaciones**:

  * Usa `Keycloak_Service` para autenticación.
  * Redirige solicitudes a `Parent_Service`, `IoT_Service`, y `Routes_Service`.

::: box
**Eureka-Server**
:::

* **Estereotipo**: `<<Service Discovery>>`
* **Descripción**: Servicio de descubrimiento que permite a los microservicios encontrar y comunicarse entre sí sin necesidad de configurar manualmente sus ubicaciones.
* **Responsabilidades**:

  * Registrar microservicios disponibles.
  * Facilitar la resolución dinámica de servicios.

* **Relaciones**:

  * Recibe registros desde `Parent_Service`, `IoT_Service`, `Routes_Service`, y `IoT_Interceptor`.

::: box
**Config-Server**
:::

* **Estereotipo**: `<<Config Server>>`
* **Descripción**: Proveedor centralizado de configuración para los microservicios, basado en repositorios externos (generalmente Git).
* **Responsabilidades**:

  * Suministrar archivos de configuración a los microservicios.

* **Relaciones**:

  * Es consultado por `Parent_Service`, `IoT_Service`, `Routes_Service`, y `IoT_Interceptor` para obtener configuraciones.

::: box
**Keycloak-Service**
:::

* **Estereotipo**: `<<Identity Provider>>`
* **Descripción**: Sistema de gestión de identidades que maneja autenticación, autorización y emisión de tokens.
* **Responsabilidades**:

  * Validar tokens JWT emitidos.
  * Autenticar usuarios que ingresan por el `API_Gateway`.

* **Relaciones**:

  * Autentica a través del `API_Gateway`.
  * Valida tokens para `Parent_Service`, `IoT_Service`, y `Routes_Service`.

::: box
**Kafka-Broker**
:::

* **Estereotipo**: `<<Event Streaming Platform>>`
* **Descripción**: Plataforma de mensajería basada en eventos. Permite la comunicación asincrónica entre microservicios mediante producción y consumo de eventos.
* **Responsabilidades**:

  * Recibir eventos de los productores.
  * Distribuir eventos a los consumidores.

* **Relaciones**:

  * Recibe eventos de `IoT_Service`.
  * Entrega eventos a `Parent_Service`, `Routes_Service`, y `IoT_Interceptor`.

::: box
**Parent-Service**
:::

* **Descripción**: Microservicio núcleo que probablemente actúa como orquestador o lógica principal del sistema.
* **Responsabilidades**:

  * Registrar en `Eureka_Server`.
  * Obtener configuración del `Config_Server`.
  * Validar tokens con `Keycloak_Service`.
  * Consumir eventos desde `Kafka_Broker`.

* **Relaciones**:

  * Integración completa con todos los componentes principales de infraestructura.

::: box
**IoT-Service**
:::

* **Descripción**: Microservicio responsable de gestionar dispositivos IoT, recolectar y enviar datos al sistema.
* **Responsabilidades**:

  * Registrar en `Eureka_Server`.
  * Obtener configuración del `Config_Server`.
  * Validar tokens con `Keycloak_Service`.
  * Producir eventos hacia `Kafka_Broker`.

* **Relaciones**:

  * Usa `Kafka_Broker` como productor de eventos.

::: box
**Routes-Service**
:::

* **Descripción**: Servicio encargado de administrar rutas o trayectos (posiblemente para logística, transporte o navegación).
* **Responsabilidades**:

  * Registrar en `Eureka_Server`.
  * Obtener configuración del `Config_Server`.
  * Validar tokens con `Keycloak_Service`.
  * Consumir eventos desde `Kafka_Broker`.

* **Relaciones**:

  * Interactúa con la mayoría de los servicios de infraestructura.

::: box
**IoT-Interceptor**
:::

* **Descripción**: Microservicio especializado que intercepta datos IoT, posiblemente para análisis, filtrado o seguridad.
* **Responsabilidades**:

  * Registrar en `Eureka_Server`.
  * Obtener configuración del `Config_Server`.
  * Consumir eventos desde `Kafka_Broker`.

* **Relaciones**:

  * Actúa como consumidor de eventos emitidos por `IoT_Service`.

\newpage


::: scenario
**Class Dictionary – Microservicio `Routes Service`**
:::

::: box
**Route**
:::

* **Estereotipo**: `<<Entity>>`
* **Descripción**: Representa una ruta completa, compuesta por múltiples puntos geográficos ordenados.
* **Atributos**:

  * `UUID id`: Identificador único de la ruta.
  * `String name`: Nombre descriptivo de la ruta.
  * `String description`: Descripción adicional de la ruta.
  * `List<RoutePoint> points`: Lista ordenada de puntos que forman la ruta.

* **Relaciones**:

  * Composición con `RoutePoint` (una ruta contiene múltiples puntos).
  * Referenciada por `TravelHistory`.

::: box
**RoutePoint**
:::

* **Estereotipo**: `<<Entity>>`
* **Descripción**: Punto geográfico que forma parte de una ruta.
* **Atributos**:

  * `UUID id`: Identificador del punto.
  * `Double latitude`: Coordenada latitudinal.
  * `Double longitude`: Coordenada longitudinal.
  * `Integer order`: Posición en la ruta.

::: box
**TravelHistory**
:::

* **Estereotipo**: `<<Entity>>`
* **Descripción**: Registro del historial de viajes de un "parent" (posiblemente un dispositivo o usuario).
* **Atributos**:

  * `UUID id`: Identificador del historial.
  * `UUID parentId`: Identificador del emisor o dispositivo.
  * `UUID routeId`: Ruta que se ha recorrido.
  * `LocalDateTime startedAt`: Fecha y hora de inicio.
  * `LocalDateTime endedAt`: Fecha y hora de fin.

* **Relaciones**:

  * Asociación hacia `Route`.


::: box
**RouteDTO**
:::

* **Estereotipo**: `<<DTO>>`
* **Descripción**: Representación simplificada de `Route` para transferencias de datos.
* **Atributos**:

  * `UUID id`, `String name`.

::: box
**RoutePointDTO**
:::

* **Estereotipo**: `<<DTO>>`
* **Descripción**: DTO que representa un punto de una ruta sin información de orden.
* **Atributos**:

  * `UUID id`, `Double latitude`, `Double longitude`.

::: box
**TravelHistoryDTO**
:::

* **Estereotipo**: `<<DTO>>`
* **Descripción**: DTO para transferir información básica del historial de viajes.
* **Atributos**:

  * `UUID id`, `LocalDateTime startedAt`, `LocalDateTime endedAt`.

:: box
**RouteRepository**
:::

* **Estereotipo**: `<<Repository>>`
* **Descripción**: Interfaz para el acceso a datos de `Route`.
* **Métodos**:

  * `findAll()`: Obtiene todas las rutas.
  * `findById(UUID id)`: Busca una ruta por ID.

::: box
**TravelHistoryRepository**
:::

* **Estereotipo**: `<<Repository>>`
* **Descripción**: Maneja la persistencia de historiales de viaje.
* **Métodos**:

  * `findAllByParentId(UUID parentId)`: Encuentra todos los viajes de un dispositivo/usuario.

::: box
**RouteService**
:::

* **Estereotipo**: `<<Service>>`
* **Descripción**: Capa de lógica de negocio para la gestión de rutas.
* **Métodos**:

  * `findAllRoutes()`: Devuelve todas las rutas en forma de `RouteDTO`.
  * `findRouteById(UUID id)`: Devuelve una ruta específica como `RouteDTO`.

* **Relaciones**:

  * Usa `RouteRepository`.
  * Produce `RouteDTO`.

::: box
**TravelHistoryService**
:::

* **Estereotipo**: `<<Service>>`
* **Descripción**: Lógica de negocio para la gestión de historiales de viaje.
* **Métodos**:

  * `findTravelHistoriesByParent(UUID parentId)`: Devuelve los historiales asociados a un "parent".

* **Relaciones**:

  * Usa `TravelHistoryRepository`.
  * Produce `TravelHistoryDTO`.

::: box
**RouteController**
:::

* **Estereotipo**: `<<Controller>>`
* **Descripción**: Controlador REST que expone rutas relacionadas a `Route`.
* **Métodos**:

  * `getAllRoutes()`: Devuelve todas las rutas.
  * `getRouteById(UUID id)`: Devuelve una ruta por su ID.

* **Relaciones**:

  * Usa `RouteService`.

::: box
**TravelHistoryController**
:::

* **Estereotipo**: `<<Controller>>`
* **Descripción**: Controlador REST para los historiales de viaje.
* **Métodos**:

  * `getTravelHistories(UUID parentId)`: Devuelve historiales de un "parent".

* **Relaciones**:

  * Usa `TravelHistoryService`.

::: box
**RoutesKafkaConsumer**
:::

* **Estereotipo**: `<<KafkaListener>>`
* **Descripción**: Escucha mensajes desde Kafka para crear o actualizar rutas.
* **Métodos**:

  * `consumeRouteEvent(String message)`: Procesa eventos entrantes.
  * `parseRoutePayload(String payload)`: Convierte un mensaje en un `RouteDTO`.

* **Relaciones**:

  * Usa `RouteService` para persistencia.
  * Produce `RouteDTO`.

::: box
**AppConfigRoutes**
:::

* **Estereotipo**: `<<Configuration>>`
* **Descripción**: Clase de configuración del microservicio.
* **Métodos**:

  * `datasourceConfig()`: Proporciona la configuración de la fuente de datos.

* **Relaciones**:

  * Configura `RouteRepository`, `TravelHistoryRepository`, y `RoutesKafkaConsumer`.

\newpage

::: scenario
**Class Dictionary – Microservicio `Parent Service`**
:::

::: box
**Parent**
:::

* **Descripción:** Representa a un padre registrado en el sistema.
* **Atributos:**

  * `UUID id`: Identificador único del padre.
  * `UUID userId`: Identificador del usuario relacionado (autenticación).
  * `String firstName`: Nombre del padre.
  * `String lastName`: Apellido del padre.
  * `List<Child> children`: Lista de hijos asociados al padre.

::: box
**Child**
:::

* **Descripción:** Representa a un hijo o hija de un padre registrado.
* **Atributos:**

  * `UUID id`: Identificador único del hijo.
  * `String firstName`: Nombre del hijo.
  * `String lastName`: Apellido del hijo.
  * `LocalDate birthDate`: Fecha de nacimiento del hijo.

::: box
`**User**
:::

* **Descripción:** Entidad que representa al usuario autenticado del sistema.
* **Atributos:**

  * `UUID id`: Identificador único del usuario.
  * `String username`: Nombre de usuario.
  * `String email`: Correo electrónico del usuario.
  * `String password`: Contraseña (probablemente encriptada).
  * `List<String> roles`: Lista de roles asignados al usuario.

::: box
**ParentDTO**
:::

* **Descripción:** Objeto de transferencia de datos para la entidad `Parent`.
* **Atributos:**

  * `UUID id`
  * `UUID userId`
  * `String firstName`
  * `String lastName`

::: box
**ChildDTO**
:::

* **Descripción:** Objeto de transferencia para `Child`.
* **Atributos:**

  * `UUID id`
  * `String firstName`
  * `String lastName`

::: box
**UserDTO**
:::

* **Descripción:** Representación simplificada del usuario, omitiendo la contraseña.
* **Atributos:**

  * `UUID id`
  * `String username`
  * `String email`

::: box
**ParentRepository**
:::

* **Descripción:** Interfaz que define operaciones de persistencia para `Parent`.
* **Métodos:**

  * `List<Parent> findAll()`
  * `Optional<Parent> findById(UUID id)`

::: box
**ChildRepository**
:::

* **Descripción:** Repositorio para la entidad `Child`.
* **Métodos:**

  * `List<Child> findAllByParentId(UUID parentId)`

::: box
**UserRepository**
:::

* **Descripción:** Repositorio para usuarios autenticados del sistema.
* **Métodos:**

  * `Optional<User> findByUsername(String username)`

::: box
**ParentService**
:::

* **Descripción:** Lógica de negocio para padres.
* **Métodos:**

  * `List<ParentDTO> findAllParents()`
  * `ParentDTO findParentById(UUID id)`

::: box
**ChildService**
:::

* **Descripción:** Lógica de negocio para hijos.
* **Métodos:**

  * `List<ChildDTO> findChildrenByParentId(UUID parentId)`

::: box
**UserService**
:::

* **Descripción:** Gestión de usuarios.
* **Métodos:**

  * `UserDTO findUserByUsername(String username)`


::: box
**ParentController**
:::

* **Descripción:** Exposición HTTP de recursos `Parent`.
* **Endpoints:**

  * `getAllParents() → ResponseEntity<List<ParentDTO>>`
  * `getParentById(UUID id) → ResponseEntity<ParentDTO>`

::: box
**ChildController**
:::

* **Descripción:** Exposición HTTP para acceder a hijos de un padre.
* **Endpoints:**

  * `getChildrenByParent(UUID parentId) → ResponseEntity<List<ChildDTO>>`

::: box
**UserController**
:::

* **Descripción:** Controlador para operaciones relacionadas con usuarios.
* **Endpoints:**

  * `getUserByUsername(String username) → ResponseEntity<UserDTO>`


::: box
**ParentKafkaConsumer**
:::

* **Descripción:** Consume eventos Kafka relacionados con padres.
* **Métodos:**

  * `consumeParentEvent(String message)`: Consume el mensaje Kafka entrante.
  * `parseParentPayload(String payload): ParentDTO`: Parsea el mensaje en formato DTO.

::: box
**AppConfigParent**
:::

* **Descripción:** Clase de configuración principal del microservicio.
* **Métodos:**

  * `DataSource datasourceConfig()`: Configura la fuente de datos.

* **Configura:** `ParentRepository`, `ChildRepository`, `UserRepository`, `ParentKafkaConsumer`.

\newpage

::: scenario
**Class Dictionary – Microservicio `IoT Service`**
:::

::: box
**Device**
:::

* **Descripción:** Representa un dispositivo físico propiedad de un padre que contiene sensores.
* **Atributos:**

  * `UUID id`: Identificador único del dispositivo.
  * `String name`: Nombre del dispositivo.
  * `String type`: Tipo de dispositivo (ej. "Pulsera", "Sensor ambiental").
  * `UUID parentId`: ID del padre propietario del dispositivo.
  * `List<Sensor> sensors`: Lista de sensores asociados al dispositivo.

::: box
**Sensor**
:::

* **Descripción:** Componente que mide una variable física y se asocia a un dispositivo.
* **Atributos:**

  * `UUID id`: Identificador único del sensor.
  * `String type`: Tipo de sensor (ej. temperatura, frecuencia cardíaca).
  * `String unit`: Unidad de medida (ej. "°C", "bpm").

::: box
**SensorData**
:::

* **Descripción:** Registros históricos de los datos recolectados por un sensor.
* **Atributos:**

  * `UUID id`: Identificador del dato.
  * `UUID sensorId`: ID del sensor que generó el dato.
  * `LocalDateTime timestamp`: Fecha y hora del registro.
  * `Double value`: Valor medido por el sensor.

::: box
**DeviceDTO**
:::

* **Descripción:** Representación simplificada de un `Device` para transferencias de datos.
* **Atributos:**

  * `UUID id`
  * `String name`
  * `String type`

::: box
**SensorDTO**
:::

* **Descripción:** Transferencia de datos del objeto `Sensor`.
* **Atributos:**

  * `UUID id`
  * `String type`
  * `String unit`

::: box
**SensorDataDTO**
:::

* **Descripción:** DTO que encapsula los datos generados por sensores.
* **Atributos:**

  * `UUID id`
  * `UUID sensorId`
  * `LocalDateTime timestamp`
  * `Double value`

::: box
**DeviceRepository**
:::

* **Descripción:** Acceso a la persistencia para dispositivos.
* **Métodos:**

  * `List<Device> findAll()`
  * `Optional<Device> findById(UUID id)`

::: box
**SensorRepository**
:::

* **Descripción:** Provee acceso a sensores.
* **Métodos:**

  * `List<Sensor> findAllByDeviceId(UUID deviceId)`

::: box
**SensorDataRepository**
:::

* **Descripción:** Manejo de almacenamiento de datos de sensores.
* **Métodos:**

  * `List<SensorData> findAllBySensorId(UUID sensorId)`

::: box
**DeviceService**
:::

* **Descripción:** Lógica de negocio para dispositivos.
* **Métodos:**

  * `List<DeviceDTO> findAllDevices()`
  * `DeviceDTO findDeviceById(UUID id)`

::: box
**SensorService**
:::

* **Descripción:** Servicios relacionados con sensores.
* **Métodos:**

  * `List<SensorDTO> findSensorsByDeviceId(UUID deviceId)`

::: box
**SensorDataService**
:::

* **Descripción:** Manejo y persistencia de los datos recogidos por sensores.
* **Métodos:**

  * `List<SensorDataDTO> findSensorDataBySensorId(UUID sensorId)`
  * `void saveSensorData(SensorDataDTO dto)`

::: box
**DeviceController**
:::

* **Descripción:** Expone la API REST relacionada a dispositivos.
* **Endpoints:**

  * `getAllDevices() → ResponseEntity<List<DeviceDTO>>`
  * `getDeviceById(UUID id) → ResponseEntity<DeviceDTO>`

::: box
**SensorController**
:::

* **Descripción:** Endpoints relacionados a sensores dentro de un dispositivo.
* **Endpoints:**

  * `getSensorsByDevice(UUID deviceId) → ResponseEntity<List<SensorDTO>>`

::: box
**SensorDataController**
:::

* **Descripción:** Controlador que expone los datos recolectados por sensores.
* **Endpoints:**

  * `getSensorData(UUID sensorId) → ResponseEntity<List<SensorDataDTO>>`

::: box
**IoTKafkaConsumer**
:::

* **Descripción:** Componente que consume eventos enviados vía Kafka con datos de sensores.
* **Métodos:**

  * `consumeSensorEvent(String message)`: Procesa y guarda los datos de sensor recibidos.
  * `parseSensorPayload(String payload): SensorDataDTO`: Parsea un mensaje JSON en un DTO válido.

::: box
**AppConfigIoT**
:::

* **Descripción:** Clase de configuración general del microservicio IoT.

* **Métodos:**

  * `MongoTemplate mongoTemplate()`: Configura acceso a MongoDB.
  * `ConsumerFactory kafkaConsumerFactory()`: Configura el factory para Kafka consumer.

* **Configura:**

  * Repositorios: `DeviceRepository`, `SensorRepository`, `SensorDataRepository`
  * Kafka: `IoTKafkaConsumer`

\newpage

::: scenario
**Class Dictionary – Microservicio `IoT Interceptor Service`**
:::

::: box
**IoTConsumer**
:::

* **Descripción:** Componente que escucha eventos Kafka provenientes del servicio IoT y actúa como interceptor de datos de sensores.
* **Métodos:**

  * `consumeIoTEvent(String message)`: Escucha y recibe mensajes JSON desde Kafka que contienen datos de sensores.
  * `processSensorData(SensorDataDTO data)`: Procesa el mensaje recibido y lo convierte en un DTO válido, que luego es reenviado por WebSocket a los clientes suscritos.

::: box
**WebSocketController**
:::

* **Descripción:** Controlador que gestiona la difusión de datos a través de WebSocket hacia los clientes conectados en tiempo real.
* **Métodos:**

  * `broadcastSensorData(String destination, SensorDataDTO payload)`: Difunde los datos de sensor a un destino WebSocket específico.
  * `broadcastAlert(String destination, String message)`: Envía un mensaje de alerta en tiempo real a través de WebSocket (por ejemplo, para notificaciones críticas o anormales).

::: box
**AppConfigInterceptor**
:::

* **Descripción:** Clase de configuración para el microservicio, enfocada en Kafka y WebSocket.

* **Métodos:**

  * `kafkaConsumerFactory()`: Configura y expone un `ConsumerFactory` necesario para consumir eventos Kafka.
  * `webSocketConfig()`: Configura el canal y comportamiento de WebSocket del sistema.

* **Configura:**

  * `IoTConsumer`
  * `WebSocketController`

::: box
**SensorDataDTO**
:::

* **Descripción:** Objeto de transferencia de datos que representa una medición de un sensor, extendido para incluir el `deviceId`.
* **Atributos:**

  * `UUID id`: Identificador del dato de sensor.
  * `UUID deviceId`: Identificador del dispositivo que contiene el sensor.
  * `UUID sensorId`: Identificador del sensor que produjo el dato.
  * `LocalDateTime timestamp`: Marca de tiempo del momento de recolección.
  * `Double value`: Valor numérico medido.

* `IoTConsumer --> SensorDataDTO`: Consume los datos como entrada desde Kafka.
* `IoTConsumer --> WebSocketController`: Envía los datos procesados para su difusión.
* `WebSocketController --> SensorDataDTO`: Utiliza el DTO tanto para entrada como para difusión.
* `AppConfigInterceptor`: Configura la infraestructura para Kafka y WebSocket.

\newpage

## Database Design.

El diseño de bases de datos es un componente fundamental en el desarrollo de aplicaciones modernas, ya que permite estructurar, almacenar y gestionar de manera eficiente grandes volúmenes de información. Una base de datos bien diseñada no solo mejora el rendimiento y la escalabilidad del sistema, sino que también garantiza la integridad, consistencia y accesibilidad de los datos. En este apartado se describe el proceso de diseño de la base de datos del sistema, considerando tanto modelos relacionales como no relacionales, según la naturaleza de la información y los requerimientos específicos del proyecto.

Para ello, se han utilizado herramientas como el **Modelo Entidad-Relación (ER)** y los **diagramas de esquemas lógicos**, que permiten representar gráficamente las entidades clave, sus atributos y las relaciones existentes entre ellas. Este modelo facilita la comprensión global de la estructura de datos, además de ser un punto de partida para la posterior implementación en un sistema de gestión de bases de datos (DBMS).

Este diseño actúa como un puente entre el análisis de requerimientos y la implementación, permitiendo validar que la estructura de datos propuesta cumple con los objetivos funcionales del sistema, y sirviendo como referencia para desarrolladores, analistas y administradores de bases de datos a lo largo del ciclo de vida del software.

![Recurso extraído de Canva](src/img/cap4/database-design-intro.png)

\newpage

### Relational/Non-Relational Database Diagram.

**Parent Service - Database Design**

::: warn
Para una mejor visualización del diagrama, haga click en la [URL](https://mermaid.live/edit#pako:eNqtU8tuwjAQ_BVrzwElgSSKbxGkApVSGqCHCilyaxOigo0cR5QC_17nQQFR1B7qk3dnNbOza-_gTVAGGJjspiSRZDXjSJ_pOIzQrrqX8bTfRSlFo_tT7jmIOr0gQnnGJCcrhqbD_tM0vC5gK5Iub6JrkmUbIWmFHE76cfQ4CK-aKNTiG51IsWTfQM00CqJwOPnNywX13Q_U81RmKi5sXmNLcgHVwp1ef9D9k-6aSMbVPygXpxtMQvSaSrWIKVGnls72ut83GmJ3nAxGYsOza_i0Aoz0itKEMxoXE84uBltXV24xWhANgwErJvXWqX5Z5QRmoBZMtwlYXymR7zOY8YOuI7kS4y1_A6xkzgyQIk8WgOdkmekoXxce6pd5LFkT_iLEeQh4Bx-ALcttui3Ts33Xc2zf9j0Dtjrt-k3bctpO2zItx7WdgwGfJYHZdHzHNFuW67mmaXmeawCjqRLyofoV5ecwIJGFk7pBximTHZFzVVIfvgBz_O2Y)
:::

![Database Design Diagram Mermaid](src/img/cap4/parent-service-database.png){height=70%}

\newpage

**Routes Service - Database Design**

::: warn
Para una mejor visualización del diagrama, haga click en la [URL](https://mermaid.live/edit#pako:eNqNUttuwjAM_ZXIzwVBSUvpGxsdq8ZNpUzaVAllxEA1SFBIpTHovy8FpnGTRt7sc2KfY3sLE8kRfEDVStlMsWUiiHlRfxQHZHsIijcahS2ScjJ4-csN4yjstYlgS7xKclxPVLrSqRQHLE_ESenxoB_24v8a7HNKZhrHBnk6QVr90UMnIAumU51xvAakmF0gpl_QDiIiFUd1oSmOmq9BZ_wcDuN-9HaXrBVTKLTRdZfcZhzEYTcga82URj5m-gaIgp9A5wMju12pJLdn0_PJnK1vcC7c-CQBhVM0eifIyccmgUSABUtUS5Zys_y93wT0HM0moeBzpj4LWm54LNNyuBET8LXK0ALjcDYHf8oWaxNlK840Ho_nl7Ji4l3K0xD8LXyBb9N6ueG5Tt22Xce1HQs24FcbTtm2qV21XepSj9a83ILv_f9KmboepdRxG5UardGqZwHyVEvVPdzt_nwtmKnCyFFfMUf1KDOhTe1a_gNZ3tTZ)
:::

![Database Design Diagram Mermaid](src/img/cap4/routes-service-database.png){height=70%}

\newpage

**IoT Service - Database Design**

::: warn
Para una mejor visualización del diagrama, haga click en la [URL](https://mermaid.live/edit#pako:eNqNUttugkAQ_ZXNPKNBQJB9s0obY9VGtA8Nidm4UyWVXbIsplb9966iqdomdp5mzlzO3LYwlxyBAqpuyhaKZYkgRrrRa68TkW1lHWQ67XVJyslL_weLJ-Pe8IkIluEvUG9yvMnOmUKhZymv8H0iKiWOhvFofI_siHFcp3M0Jchj_w7lCSxFqv_km3Xbk_a_SAsUhVS3pCY9mvQGEdFphoVmWX7hG00fniOyZqsSb8hPm93tajW5PY9OyZIVV8u48letUqJwLhU3gWBBhipjKTenO46QgF6iOQNQo3KmPhJIxN7EsVLLeCPmQLUq0QIly8US6DtbFcYqc840nk5_DsmZeJPy0gS6hU-gruvV_aDlhYHb8Lym27BgAzR06nYYNm2n6bte4Df9vQVfx3y73rIdx26EXtBw3MDzQwuQp1qqQfV1x-ezYKEOg5z6Q8FRdWQptCkd7L8BYvq_Sg)
:::

![Database Design Diagram Mermaid](src/img/cap4/iot-service-database.png){height=70%}

\newpage

**IoT Interceptor Service - Database Design**

::: warn
Para una mejor visualización del diagrama, haga click en la [URL](https://mermaid.live/edit#pako:eNpdkE1vwjAMhv9K5XOFaBuSkBsbPaANmMbHYaqEIuJBNJKgNEVjqP994WPThk_2Y_vVa59g7RSCAPRDLTdemsomMWblZDZ9XQ0H88GqXJaTeXK6Ns6xWIyGiVbJy9MdU3jQa1xpdcdrtLXz_3hULuejcZkEbbAO0uz_9KaLh-cyOchdg1faVhZSMOiN1Cq6vZipIGzRYAUipkr6jwoq28Y52QQ3O9o1iOAbTMG7ZrMF8S53dayavZIBb9f-0r20b86Zn5VYgjjBJ4g84x3S5ZT0aN7nPOcpHEFkjHVoTklBipxmLOO8TeHrItDtMM4JYRkreLdfMNJLAZUOzo-vr758PIWNP59yc4hWoX90jQ0gaEHbbxpId9c)
:::

![Database Design Diagram Mermaid](src/img/cap4/iot-interceptor-database.png){height=70%}

