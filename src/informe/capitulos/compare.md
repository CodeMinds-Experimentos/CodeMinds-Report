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

::: box
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

\newpage

### Build & Test Suite Pipeline Components.

::: box
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

## Continuous Delivery

La entrega continua (CD, por sus siglas en inglés) es una práctica clave dentro del enfoque DevOps que representa la evolución natural de la integración continua. Esta metodología busca garantizar que cualquier versión del sistema que haya superado las pruebas automatizadas pueda ser entregada de forma automática y segura a entornos de prueba intermedios, como staging o QA, sin intervención manual significativa. El objetivo principal es reducir el tiempo que transcurre desde que un cambio es confirmado en el repositorio hasta que puede ser validado en un entorno que simula fielmente la producción.

En el contexto de este proyecto, la entrega continua se aplica principalmente sobre el frontend desarrollado en Angular, permitiendo validar visual y funcionalmente los cambios antes de realizar el despliegue final. Esta práctica contribuye significativamente a la detección temprana de errores, mejora la colaboración entre equipos y fortalece la calidad del software entregado al usuario final.

Actualmente, si bien el proyecto aún se encuentra en una fase temprana de automatización completa del proceso de despliegue, se ha definido una arquitectura de trabajo basada en ramas estructuradas como develop y main. Esta organización permite implementar un flujo de entrega escalonado y controlado. A nivel técnico, se ha planteado un pipeline automatizado que incluye la compilación en modo servidor (Server-Side Rendering, SSR), ejecución de pruebas end-to-end mediante la herramienta Cypress, verificación del estado del sistema y posterior despliegue mediante transferencia segura (SSH) a servidores externos de validación.

A medida que el sistema evolucione y los pipelines se refuercen, se espera incorporar etapas adicionales que incluyan validaciones de accesibilidad, control de versiones semántico, análisis de seguridad automatizado y notificaciones integradas con herramientas colaborativas, todo con el propósito de garantizar entregas frecuentes, confiables y sin fricciones.

![Recurso extraído de Canva](src/img/cap7/continuous-delivery.png)

\newpage

### Tools and Practices.

::: box
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


\newpage

### Stages Deployment Pipeline Components.

::: box
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

## Continuous deployment

El despliegue continuo (CD, por sus siglas en inglés) constituye el nivel más avanzado y maduro dentro de la cadena de prácticas DevOps. A diferencia de la entrega continua, donde la entrega a producción aún requiere una decisión manual, el despliegue continuo automatiza completamente este último paso, permitiendo que las versiones del sistema que hayan superado todas las validaciones y pruebas sean desplegadas directamente en el entorno de producción sin intervención humana. Esta estrategia no solo acorta drásticamente los ciclos de entrega de software, sino que también promueve una cultura de confianza, calidad continua y retroalimentación inmediata.

En el marco de este proyecto, el despliegue continuo aún no ha sido implementado de forma activa; sin embargo, se ha trazado una hoja de ruta clara para su incorporación progresiva. Este plan considera una arquitectura robusta para el frontend desarrollado en Angular, que incluirá mecanismos de revisión automática, auditorías de seguridad, generación de versiones con control semántico y despliegue seguro a través de protocolos como SSH o integraciones con servicios en la nube.

El objetivo a futuro es lograr un pipeline completamente automatizado que, al detectar un merge exitoso a la rama main, ejecute una secuencia de validaciones automatizadas, construcción optimizada del artefacto, pruebas funcionales finales y despliegue inmediato al entorno productivo. Este flujo garantizará que cada cambio relevante llegue a los usuarios finales de manera ágil, fiable y trazable.

Además de reducir los tiempos de entrega y eliminar cuellos de botella operativos, el despliegue continuo contribuye a minimizar los errores humanos y facilita una respuesta más rápida ante incidentes. También habilita prácticas de monitoreo post-despliegue y rollback automatizado en caso de fallos críticos, fortaleciendo así la resiliencia del sistema. La implementación futura de esta práctica representará un paso fundamental hacia una operación DevOps completamente integrada y eficiente.

![Recurso extraído de Canva](src/img/cap7/continuous-deployment.png)

\newpage

### Tools and Practices.

::: box
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

\newpage

### Production Deployment Pipeline Components.

::: box
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
