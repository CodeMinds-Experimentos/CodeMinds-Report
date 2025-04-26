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
