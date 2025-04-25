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

## Web Applications UX/UI Design.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### Web Applications Wireframes.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### Web Applications Wireflow Diagrams.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### Web Applications Mock-ups.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### Web Applications User Flow Diagrams.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

## Web Applications Prototyping.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

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
