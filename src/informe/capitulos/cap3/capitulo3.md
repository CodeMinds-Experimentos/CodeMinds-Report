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

# Capítulo III: Requirements Specification

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

## To-Be Scenario Mapping.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

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
US01 & Registro y edición de vehículos \\
\hline
US02 & Definición y mapeo de zonas \\
\hline
US03 & Visualización geoespacial de zonas y rutas \\
\hline
US04 & Asignación de vehículos a rutas específicas \\
\hline
US05 & Desactivación temporal de unidades fuera de servicio \\
\hline
\textbf{EP03 (Gestión de conductores y estudiantes)} & \textbf{Como} administrador educativo, \textbf{quiero} gestionar la información de conductores y estudiantes \textbf{para} asegurar que las rutas se asignen correctamente y optimizar la seguridad del transporte escolar. \\
\hline
US01 & Registro y actualización de conductores \\
\hline
US02 & Registro y asignación de pulseras RFID a estudiantes \\
\hline
US03 & Asignación de conductores y estudiantes a rutas específicas \\
\hline
US04 & Verificación de disponibilidad de conductores \\
\hline
US05 & Control de cambios de última hora en la asignación de conductores y estudiantes \\
\hline
\textbf{EP04 (Integración IoT y captura de datos)} & \textbf{Como} administrador educativo, \textbf{quiero} integrar tecnologías IoT para el monitoreo en tiempo real de las flotas de transporte \textbf{para} optimizar la seguridad, eficiencia y control de las rutas de transporte escolar. \\
\hline
US01 & Monitoreo de posición y velocidad en tiempo real de vehículos \\
\hline
US02 & Monitoreo de temperatura interna de los vehículos \\
\hline
US03 & Seguimiento de unidades de transporte para verificar salida y llegada \\
\hline
US04 & Monitoreo de estudiantes que no abordaron la unidad \\
\hline
US05 & Verificación de rutas alternativas en caso de desvíos \\
\hline
US06 & Visualización de unidades en ruta para gestionar desviaciones o retrasos \\
\hline
\textbf{EP05 (Notificaciones y Alertas)} & \textbf{Como} administrador educativo, \textbf{quiero} recibir notificaciones y alertas en tiempo real sobre los eventos y condiciones críticas de las unidades de transporte \textbf{para} poder tomar decisiones rápidas y garantizar la seguridad y eficiencia del servicio. \\
\hline
US01 & Alerta de temperatura fuera de rango \\
\hline
US02 & Alerta de retrasos o desviaciones en las rutas \\
\hline
US03 & Alerta de estudiantes no abordando la unidad \\
\hline
US04 & Notificación automática ante cambios de ruta o posibles retrasos \\
\hline
US05 & Alerta por fallo de equipo en el vehículo (GPS, RFID, sensores, etc.) \\
\hline
US06 & Notificación cuando la unidad ha completado el recorrido \\
\hline
\textbf{EP06 (Reportes y Analítica)} & \textbf{Como} administrador educativo, \textbf{quiero} generar y analizar reportes e indicadores \textbf{para} evaluar el desempeño del transporte escolar y apoyar la toma de decisiones. \\
\hline
US01 & Reporte de tiempos de ruta y cumplimiento \\
\hline
US02 & Estadísticas de abordaje por estudiante \\
\hline
US03 & Exportación de datos históricos en Excel/PDF \\
\hline
US04 & Reporte de incidencias críticas \\
\hline
US05 & Programación de envíos automáticos de reportes \\
\hline
US06 & Filtrado y segmentación de datos históricos \\
\hline
\textbf{EP07 (Plataforma Web de Administración)} & \textbf{Como} administrador educativo, \textbf{quiero} acceder a herramientas de administración centralizadas \textbf{para} configurar, monitorear y asegurar el correcto funcionamiento de la plataforma. \\
\hline
US01 & Dashboard con KPIs clave \\
\hline
US02 & Gestión de roles y permisos \\
\hline
US03 & Configuración de parámetros globales \\
\hline
US04 & Registro de auditoría de actividad \\
\hline
US05 & Configuración de notificaciones y alertas \\
\hline
US06 & Personalización del dashboard \\
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
US01 & Registro y edición de vehículos & \textbf{Como} administrador educativo, \textbf{quiero} registrar y editar los datos de cada vehículo (placa, modelo, capacidad y estado operativo), \textbf{para} mantener un catálogo actualizado y fiable de la flota. & 
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
US02 & Definición y mapeo de zonas & \textbf{Como} administrador educativo, \textbf{quiero} definir y mapear zonas de recogida y entrega en un mapa interactivo, \textbf{para} optimizar la cobertura y asignar rutas con precisión. & 
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
US03 & Visualización geoespacial de zonas y rutas & \textbf{Como} administrador educativo, \textbf{quiero} visualizar todas las zonas de recogida y entrega y sus rutas asociadas en un mapa interactivo, \textbf{para} detectar posibles solapamientos, huecos de cobertura o áreas no cubiertas. & 
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
US04 & Asignación de vehículos a rutas específicas & \textbf{Como} administrador educativo, \textbf{quiero} asignar vehículos específicos a rutas definidas, \textbf{para} tener un control operacional directo sobre qué unidad se utiliza en cada recorrido y facilitar la trazabilidad en caso de incidentes. & 
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
US05 & Desactivación temporal de unidades fuera de servicio & \textbf{Como} administrador educativo, \textbf{quiero} desactivar temporalmente vehículos fuera de servicio, \textbf{para} evitar su asignación errónea a rutas mientras se mantiene su información en el sistema para futuras referencias y reactivación. & 
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
US01 & Registro y actualización de conductores & \textbf{Como} administrador educativo, \textbf{quiero} registrar nuevos conductores y actualizar sus datos de contacto, número de licencia y estado operativo, \textbf{para} mantener un personal actualizado y garantizar la correcta asignación de rutas. & 
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

US02 & Registro y asignación de pulseras RFID a estudiantes & \textbf{Como} administrador educativo, \textbf{quiero} registrar a los estudiantes en el sistema y asignarles pulseras RFID con un identificador único, \textbf{para} vincular cada niño con su dispositivo de control y gestionar su transporte de manera más eficiente. & 
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
US03 & Asignación de conductores y estudiantes a rutas específicas & \textbf{Como} administrador educativo, \textbf{quiero} asignar conductores y estudiantes a rutas específicas en el sistema, \textbf{para} asegurar que cada unidad opere con el personal y pasajeros correctos y optimizar la seguridad del transporte escolar. & 
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
US04 & Verificación de disponibilidad de conductores & \textbf{Como} administrador educativo, \textbf{quiero} verificar la disponibilidad de los conductores antes de asignarlos a una ruta, \textbf{para} evitar conflictos de horario y asegurar una gestión eficiente del personal y la flota. &
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
US05 & Control de cambios de última hora en la asignación de conductores y estudiantes & \textbf{Como} administrador educativo, \textbf{quiero} realizar cambios de última hora en la asignación de conductores y estudiantes, \textbf{para} asegurar la continuidad del servicio ante imprevistos sin afectar el resto de la programación. &
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
US01 & Monitoreo en tiempo real de posición y velocidad de vehículos & \textbf{Como} administrador educativo, \textbf{quiero} conocer la posición y velocidad en tiempo real de cada vehículo, \textbf{para} monitorear sus rutas y detectar posibles retrasos o desvíos oportunamente. & 
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
US02 & Monitoreo de temperatura interna de los vehículos & \textbf{Como} administrador educativo, \textbf{quiero} monitorear remotamente la temperatura interna de los vehículos, \textbf{para} asegurarme de que las condiciones sean seguras para los pasajeros. &
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
US03 & Seguimiento de unidades de transporte para verificar salida y llegada & \textbf{Como} administrador educativo, \textbf{quiero} visualizar en tiempo real qué unidades ya han partido para recoger a los estudiantes y qué unidades ya han llegado al centro educativo, \textbf{para} hacer un seguimiento eficiente del estado de las rutas y asegurarme de que todos los estudiantes han sido recogidos o entregados. &
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
US04 & Monitoreo de estudiantes que no abordaron la unidad & \textbf{Como} administrador educativo, \textbf{quiero} hacer un seguimiento de qué estudiantes no abordaron la unidad, \textbf{para} tomar acciones inmediatas y asegurarme de que todos los estudiantes estén siendo transportados de forma segura. &
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
US05 & Verificación de rutas alternativas en caso de desvíos & \textbf{Como} administrador educativo, \textbf{quiero} verificar y gestionar rutas alternativas en tiempo real cuando una unidad se desvía de su ruta prevista, \textbf{para} garantizar que los estudiantes lleguen a su destino de manera segura y a tiempo frente a imprevistos. &
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
US06 & Visualización de unidades en ruta para gestionar desviaciones o retrasos & \textbf{Como} administrador educativo, \textbf{quiero} visualizar en tiempo real todas las unidades en ruta, \textbf{para} detectar rápidamente desviaciones o retrasos y tomar decisiones oportunas que aseguren el cumplimiento de los horarios y la seguridad de los estudiantes. &
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
US01 & Alerta de temperatura fuera de rango & \textbf{Como} administrador educativo, \textbf{quiero} recibir alertas en tiempo real cuando la temperatura interna de un vehículo se salga de los parámetros establecidos, \textbf{para} tomar medidas inmediatas que garanticen la seguridad y el confort de los estudiantes durante el transporte. &
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
US02 & Alerta de retrasos o desviaciones en las rutas & \textbf{Como} administrador educativo, \textbf{quiero} recibir alertas inmediatas cuando una unidad de transporte experimente retrasos o se desvíe de la ruta establecida, \textbf{para} poder coordinar con el conductor y tomar decisiones rápidas que minimicen el impacto en el servicio y garanticen la llegada segura y oportuna de los estudiantes. &
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
US03 & Alerta de estudiantes no abordando la unidad & \textbf{Como} administrador educativo, \textbf{quiero} recibir alertas en tiempo real cuando un estudiante asignado a una ruta no aborde la unidad, \textbf{para} poder tomar medidas inmediatas como contactar al conductor o a los padres, y así garantizar la seguridad de todos los estudiantes. &
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
US04 & Notificación automática ante cambios de ruta o posibles retrasos & \textbf{Como} administrador educativo, \textbf{quiero} recibir notificaciones automáticas cuando un vehículo experimente cambios de ruta o posibles retrasos, \textbf{para} poder gestionar de manera proactiva las rutas y tomar decisiones para minimizar el impacto en los horarios de transporte. &
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
US05 & Alerta por fallo de equipo en el vehículo (GPS, RFID, sensores, etc.) & \textbf{Como} administrador educativo, \textbf{quiero} recibir una alerta inmediata en caso de fallo de equipos en los vehículos, como el GPS, RFID o sensores, \textbf{para} poder tomar medidas rápidas y garantizar que el control de las rutas y la seguridad de los estudiantes no se vean comprometidos. &
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
US06 & Notificación cuando la unidad ha completado el recorrido & \textbf{Como} administrador educativo, \textbf{quiero} recibir una notificación cuando una unidad haya completado su recorrido (tanto la ruta hacia el colegio como el retorno a casa) \textbf{para} poder gestionar eficientemente la programación de las unidades, evitando retrasos y asegurando que las unidades estén disponibles para nuevas asignaciones. &
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
US01 & Reporte de tiempos de ruta y cumplimiento & \textbf{Como} administrador educativo, \textbf{quiero} generar reportes de tiempos de ruta y cumplimiento, \textbf{para} evaluar el desempeño de la flota y apoyar la toma de decisiones basadas en datos operativos. & 
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
US02 & Estadísticas de abordaje por estudiante & \textbf{Como} administrador educativo, \textbf{quiero} obtener estadísticas de abordaje por estudiante, \textbf{para} detectar patrones de retraso o ausencias y tomar acciones preventivas que mejoren la eficiencia del transporte escolar. &
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
US03 & Exportación de datos históricos en Excel/PDF & \textbf{Como} responsable de calidad, \textbf{quiero} exportar datos históricos en formatos Excel o PDF, \textbf{para} presentarlos en auditorías o juntas directivas y facilitar la toma de decisiones estratégicas basadas en datos históricos. &
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
US04 & Reporte de incidencias críticas & \textbf{Como} administrador del sistema, \textbf{quiero} generar reportes de incidencias críticas, \textbf{para} consolidar y analizar eventos como alertas de temperatura, desviaciones de ruta o fallos de equipo, con el fin de identificar patrones recurrentes y focalizar acciones de mejora continua en la gestión de transporte escolar. &
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
US05 & Programación de envíos automáticos de reportes & \textbf{Como} administrador del sistema, \textbf{quiero} programar envíos automáticos de reportes, \textbf{para} automatizar la distribución periódica de reportes (diarios, semanales o mensuales) a los responsables, garantizando que la información llegue a tiempo sin necesidad de intervención manual. &
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
US06 & Filtrado y segmentación de datos históricos & \textbf{Como} administrador del sistema, \textbf{quiero} filtrar y segmentar datos históricos por ruta, vehículo, conductor o rango de fechas, \textbf{para} optimizar el análisis detallado y la preparación de informes personalizados para auditorías o reuniones de gestión. &
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
US01 & Dashboard con KPIs clave & \textbf{Como} administrador educativo, \textbf{quiero} acceder a un dashboard que muestre KPIs clave (número de rutas activas, incidencias, temperatura media, etc.), \textbf{para} monitorear la operación del transporte escolar de un vistazo y tomar decisiones basadas en datos en tiempo real. &
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
US02 & Gestión de roles y permisos & \textbf{Como} administrador educativo, \textbf{quiero} gestionar los roles y permisos de los usuarios (coordinadores, supervisores, etc.), \textbf{para} delegar responsabilidades con seguridad y asegurarme de que cada usuario solo tenga acceso a la información y funciones necesarias para su rol. &
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
US03 & Configuración de parámetros globales & \textbf{Como} administrador educativo, \textbf{quiero} configurar parámetros globales (como los umbrales de temperatura, la frecuencia de reporte GPS, etc.), \textbf{para} adaptar el sistema a las políticas internas de la institución y asegurar el funcionamiento adecuado de la plataforma. &
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
US04 & Registro de auditoría de actividad & \textbf{Como} administrador educativo, \textbf{quiero} llevar un registro de auditoría de todas las acciones realizadas por los administradores y supervisores (como la creación/edición de usuarios, cambios en rutas, ajustes de parámetros), \textbf{para} garantizar la trazabilidad y el cumplimiento de normativas internas. &
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
US05 & Configuración de notificaciones y alertas & \textbf{Como} administrador educativo, \textbf{quiero} configurar qué tipos de notificaciones y alertas deseo recibir, por qué canal (correo electrónico, SMS, notificación push) y con qué umbrales, \textbf{para} adaptar la comunicación del sistema a los procesos internos de la institución. &
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
US06 & Personalización del dashboard & \textbf{Como} administrador educativo, \textbf{quiero} personalizar el dashboard seleccionando qué widgets visualizar, su orden y frecuencia de actualización, \textbf{para} adaptar la interfaz a las prioridades específicas de mi institución y mejorar la usabilidad del sistema. &
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
US01 & Ubicación en Vivo del Vehículo \\
\hline
US02 & Consulta de Ruta Planificada \\
\hline
US03 & Estimación de Tiempo Restante \\
\hline
\textbf{EP03 (Notificaciones y Alertas)} & \textbf{Como} tutor legal, \textbf{quiero} recibir alertas y notificaciones sobre los eventos críticos del viaje de mi hijo, para asegurarme de que todo esté en orden durante el trayecto. \\
\hline
US01 & Notificación de Abordaje \\
\hline
US02 & Notificación de Llegada \\
\hline
US03 & Alerta por Desvío o Retraso \\
\hline
US04 & Alerta de Temperatura Insegura \\
\hline
\textbf{EP04 (Supervisión Visual)} & \textbf{Como} tutor legal, \textbf{quiero} tener acceso en tiempo real a la transmisión de video desde la cámara a bordo, para poder supervisar el viaje de mi hijo en todo momento. \\
\hline
US01 & Supervisión en Tiempo Real (Ida) \\
\hline
US02 & Supervisión en Tiempo Real (Regreso) \\
\hline
\textbf{EP05 (Historial y Reportes Personales)} & \textbf{Como} tutor legal, \textbf{quiero} tener acceso al historial de viajes y eventos pasados de mi hijo, para poder revisar patrones de comportamiento y reportar cualquier anomalía. \\
\hline
US01 & Historial de Rutas Diarias \\
\hline
US02 & Log de Eventos Recientes \\
\hline
US03 & Exportación de Historial \\
\hline
\textbf{EP06 (Preferencias y Configuración)} & \textbf{Como} tutor legal, \textbf{quiero} poder personalizar mi experiencia en la aplicación móvil, para ajustarla a mis necesidades y preferencias personales. \\
\hline
US01 & Selección de Notificaciones por Hijo \\
\hline
US02 & Definición de Horarios de Silencio \\
\hline
US03 & Personalización de Idioma y Tema \\
\hline
\textbf{EP07 (Soporte y Comunicación)} & \textbf{Como} tutor legal, \textbf{quiero} poder comunicarme con el conductor o el administrador, y reportar incidencias, para resolver cualquier problema que surja durante el trayecto. \\
\hline
US01 & Comunicación Directa con el Conductor \\
\hline
US02 & Reporte de Incidencias con Evidencia \\
\hline
US03 & Acceso a Ayuda y Preguntas Frecuentes \\
\hline
\end{longtable}

\newpage

## Impact Mapping.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

## Product Backlog.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.
