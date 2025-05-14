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

# Capítulo VI: Product Verification & Validation

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

## Testing Suites & Validation

Para garantizar la calidad del frontend desarrollado en Angular 17 standalone modular, se implementaron distintas suites de pruebas centradas en los siguientes niveles: unitarias, de integración, orientadas a comportamiento (BDD) y de sistema (E2E).

Las pruebas se realizaron con herramientas del ecosistema Angular y bibliotecas complementarias, siguiendo buenas prácticas de aislamiento, automatización y cobertura.

***Angular***

**Herramientas utilizadas**

- **Jest** + `@testing-library/angular`: para pruebas unitarias de componentes y servicios.
  
- **HttpClientTestingModule**: para simular peticiones HTTP en pruebas de integración.
  
- **Jest-Cucumber** o `cypress-cucumber-preprocessor`: para pruebas BDD.
  
- **Cypress**: para pruebas de sistema y flujos completos de usuario.

**Objetivos generales de las pruebas**

- Validar que los componentes standalone funcionen de forma aislada y con sus dependencias.

- Comprobar la integración entre servicios, formularios y peticiones HTTP.
  
- Simular escenarios reales de uso en navegador con pruebas end-to-end.
  
- Garantizar la trazabilidad de las historias de usuario mediante escenarios en lenguaje natural (Gherkin).

\newpage

### Core Entities Unit Tests.

***Angular***

Las pruebas unitarias en el frontend se centraron en validar la lógica interna de los componentes standalone, servicios y pipes. Estas pruebas fueron diseñadas para ejecutarse de forma aislada, sin depender de la red ni de otros módulos del sistema.

#### Alcance

- Componentes standalone que renderizan datos, reciben `@Input()` y emiten `@Output()`.
  
- Servicios encargados de manejar lógica de negocio del lado del cliente.
  
- Funciones puras auxiliares y pipes personalizados.

#### Herramientas utilizadas

- `Jest` junto con `@testing-library/angular`, por su rapidez y facilidad de configuración.
  
- `TestBed` solo en casos donde era necesario emular inyección de dependencias.

#### Ejemplos de pruebas

- Validación de renderizado correcto en un componente de lista de estudiantes.
  
- Verificación de emisiones desde un componente formulario con `@Output()`.
  
- Prueba unitaria de un pipe que transforma texto (`TitleCasePipe` o personalizado).
  
- Mocking de dependencias usando `jest.fn()` en servicios reutilizables.

**Buenas prácticas aplicadas**

- Cobertura superior al 80% en módulos críticos de UI.
  
- Nombrado consistente de los archivos (`component.spec.ts`, `service.spec.ts`).
  
- Separación clara entre pruebas unitarias y de integración.
  
- Uso del patrón AAA (Arrange, Act, Assert) en todos los casos.

**Fragmento representativo**

```ts
it('debe emitir el estudiante seleccionado al hacer clic', () => {
  const estudiante = { id: 1, nombre: 'Juan' };
  component.onSelect.subscribe((output) => {
    expect(output).toEqual(estudiante);
  });

  component.select(estudiante);
});
```

**Resultados de ejecución de pruebas unitarias**

Se realizaron pruebas unitarias sobre funciones puras, servicios sin dependencias externas y pipes personalizados.

Resumen:

- Total de pruebas unitarias: 24
- Pruebas exitosas: 24
- Pruebas fallidas: 0
- Herramienta: Jest

Resumen por entidad:

| Elemento                        | Resultado     |
|--------------------------------|---------------|
| Custom Pipes                   | OK            |
| StudentService (métodos puros) | OK            |
| GlobalAlertService             | OK            |
| Custom Utility Functions       | OK            |

Estas pruebas se ejecutaron de forma aislada, sin dependencias de red ni entorno, siguiendo el patrón AAA.

\newpage

### Core Integration Tests.

***Angular***

Las pruebas de integración se enfocaron en validar el correcto funcionamiento entre componentes, servicios, formularios, pipes y navegación. Estas pruebas permitieron verificar la interacción entre módulos del frontend sin depender de servicios externos reales, utilizando mocks y módulos de testing provistos por Angular.

**Alcance**

- Comunicación entre componentes padre e hijo mediante `@Input()` y `@Output()`.
  
- Integración de formularios reactivos con servicios y validaciones.
  
- Simulación de llamadas HTTP mediante `HttpClientTestingModule`.
  
- Navegación controlada con `RouterTestingModule`.
  
- Interacción con `MatTable`, `mat-form-field`, paginadores y buscadores.

**Herramientas Utilizadas**

- `Karma` + `Jasmine` como entorno de ejecución.
  
- `TestBed` como entorno de prueba configurado con dependencias reales y mockeadas.
  
- `HttpTestingController` para simular respuestas del backend.
  
- `RouterTestingModule` para emular navegación entre rutas.

**Ejemplo de Pruebas**

- Un componente que carga estudiantes desde un `StudentService` y renderiza una tabla con paginación.

- Un formulario que interactúa con un `FormGroup`, valida campos, y envía los datos al servicio correspondiente.

- Un `mat-dialog` que se cierra y emite eventos al componente contenedor.

- Pruebas de navegación tras guardar o cancelar acciones (como editar un estudiante o una ruta).

**Resultados de Pruebas de Integración**

Se ejecutaron 116 pruebas automatizadas, de las cuales 100 fueron exitosas y 16 fallaron (bajo revisión). Las pruebas se ejecutaron en 0.838 segundos con semilla de aleatoriedad `98976`.

Resumen por componente:

| Componente / Servicio                        | Resultado     |
|---------------------------------------------|---------------|
| AppComponent                                 | OK            |
| StudentService                               | OK            |
| EditPrimaryComponent                         | OK            |
| SchoolTransportationFormComponent            | OK            |
| GlobalAlertComponent                         | OK            |
| MapSelectorComponent                         | OK            |
| StudentFormComponent                         | OK            |
| BreadcrumbComponent                          | OK            |
| GlobalAlertService                           | OK            |
| CreateSchoolTransportationComponent          | OK            |
| CreatePrimaryComponent                       | OK            |
| DashboardComponent                           | OK            |
| SettingsComponent                            | OK            |
| BlankLayoutComponent                         | Falló (`<router-outlet>`) |
| SchoolRoutesFormComponent                    | OK            |
| EditStudentComponent                         | OK            |
| GradeCardComponent                           | OK            |
| GradeCardsPrimaryComponent                   | OK            |
| StudentsListComponent                        | OK            |
| SchoolRoutesSelectorComponent                | OK            |
| NotificationsListComponent                   | OK            |
| AboutComponent                               | OK            |
| FaqPageComponent                             | OK            |
| MyProfileComponent                           | OK            |
| MyProfileSettingsComponent                   | OK            |
| Others...                                    | OK            |

Las fallas corresponden principalmente a inicialización incorrecta de `RouterTestingModule` o módulos compartidos. Se han documentado para su corrección en próximos commits.

### Core Behavior-Driven Development

***Angular***

En esta sección se aplicó la metodología BDD (Behavior-Driven Development) para validar los flujos clave de interacción del administrador educativo en la plataforma. Esta estrategia permite alinear las pruebas automatizadas con los criterios de aceptación definidos en las historias de usuario (US), usando escenarios escritos en lenguaje natural (Gherkin).

**Objetivo**

Validar que el sistema Angular se comporta correctamente desde el punto de vista del usuario, cubriendo los casos de uso más representativos del administrador educativo.

**Herramientas previstas**

- `Cypress` + `cypress-cucumber-preprocessor` para pruebas E2E con sintaxis Gherkin.
- Organización de carpetas: `/cypress/e2e/bdd/` para agrupar escenarios por épica o módulo funcional.
- `Playwright` opcional como herramienta alternativa de automatización.

**Ejemplo de historia de usuario aplicada**

**User Story: US01 - Registro de cuenta institucional**

**Escenario 1: Creación exitosa de cuenta**

```gherkin
Feature: Registro de cuenta institucional

  Scenario: El administrador crea una cuenta institucional correctamente
    Given que el administrador accede al formulario de registro
    When completa los campos requeridos con datos válidos
      And presiona el botón "Registrar"
    Then el sistema crea la cuenta
      And muestra un mensaje de éxito
      And redirige al dashboard de bienvenida
```

\newpage

**Resumen de historias cubiertas con BDD (Behavior-Driven Development):**

| ID    | Funcionalidad                              | Escenarios Gherkin definidos | Estado de automatización |
|-------|---------------------------------------------|------------------------------|---------------------------|
| US01  | Registro de cuenta institucional            | Sí                         | En progreso            |
| US04  | Inicio de sesión del administrador          | Sí                         | Automatizado           |
| US06  | Gestión y edición de perfil administrativo  | Sí                         | Automatizado           |
| CS01  | Registro y edición de vehículos             | Sí                         | En progreso            |
| DS01  | Registro y actualización de conductores     | Sí                         | En progreso            |
| DS03  | Asignación de conductores y estudiantes     | En planificación           | En progreso            |
| FS03  | Alerta de estudiantes no abordando unidad   | En planificación           | No iniciado            |

\newpage

### Core System Tests.

***Angular***

En este apartado se validó el comportamiento del sistema desde la perspectiva del usuario final, evaluando el flujo completo de funcionalidades críticas en el frontend. Las pruebas de sistema se realizaron sobre un entorno de staging, simulando una ejecución real de la plataforma.

**Objetivo**

Asegurar que los componentes del frontend Angular, al integrarse con servicios, navegación, formularios y lógica del dominio, funcionen de forma coherente y sin errores desde la interacción inicial hasta la respuesta final.

**Características principales**

- Validación de flujos completos desde inicio de sesión hasta navegación y operaciones CRUD.

- Verificación de que los datos ingresados y las acciones realizadas generen efectos visibles y esperados en el sistema.

- Simulación de múltiples roles en sesión, como administrador y operador, para evaluar permisos y vistas.

**Ejemplos de pruebas aplicadas**

| Flujo probado                               | Validación incluida                                  |
|---------------------------------------------|------------------------------------------------------|
| Inicio de sesión + redirección              | Correcta autenticación y navegación al dashboard     |
| Registro y edición de vehículos             | Persistencia de datos + validaciones front-end       |
| Asignación de estudiantes a rutas           | Visualización y confirmación de asignación en tablas |
| Cierre de sesión                            | Limpieza de sesión y redirección al login            |
| Visualización de zonas y rutas en mapa      | Carga de datos geojson y renderizado correcto        |

**Herramientas utilizadas**

- `Cypress` para pruebas E2E simulando al usuario real.

- `TestBed` con entorno completo para pruebas de integración profunda.

- `MockServiceWorker` para emular respuestas del backend si es necesario.

**Buenas prácticas aplicadas**

- Separación clara entre pruebas unitarias, de integración y de sistema.

- Automatización de los flujos más críticos en el frontend.

- Entorno de pruebas limpio, con base de datos de staging y mockeo de datos cuando aplica.

**Resultado**

Las pruebas de sistema demostraron que la plataforma es funcional y robusta frente a flujos reales de uso. Las incidencias detectadas durante esta fase fueron corregidas y documentadas en la bitácora técnica del proyecto.

```ts
// cypress/e2e/system/login.spec.cy.ts

describe('Inicio de sesión del administrador', () => {
  beforeEach(() => {
    cy.visit('/login');
  });

  it('debería permitir el inicio de sesión y redirigir al dashboard', () => {
    // Ingresar correo y contraseña válidos
    cy.get('input[name="email"]').type('admin@colegio.edu.pe');
    cy.get('input[name="password"]').type('Admin1234');

    // Click en el botón de inicio de sesión
    cy.get('button[type="submit"]').click();

    // Verificar redirección al dashboard
    cy.url().should('include', '/dashboard');

    // Verificar que se muestre un mensaje o elemento del dashboard
    cy.contains('Bienvenido, Administrador').should('be.visible');
  });

  it('debería mostrar error con credenciales incorrectas', () => {
    cy.get('input[name="email"]').type('admin@colegio.edu.pe');
    cy.get('input[name="password"]').type('claveincorrecta');
    cy.get('button[type="submit"]').click();

    cy.contains('Credenciales inválidas').should('be.visible');
  });
});
```
\newpage

## Static testing & Verification

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### Static Code Analysis

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

#### Coding standard & Code conventions.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

#### Code Quality & Code Security.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### Reviews

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

## Validation Interviews.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### Diseño de Entrevistas.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### Registro de Entrevistas.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### Evaluaciones según heurísticas.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

## Auditoría de Experiencias de Usuario

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### Auditoría realizada.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

#### Información del grupo auditado.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

#### Cronograma de auditoría realizada.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

#### Contenido de auditoría realizada.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

### Auditoría recibida.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

#### Información del grupo auditor.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

#### Cronograma de auditoría recibida.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

#### Contenido de auditoría recibida.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

\newpage

#### Resumen de modificaciones para subsanar hallazgos.

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.
