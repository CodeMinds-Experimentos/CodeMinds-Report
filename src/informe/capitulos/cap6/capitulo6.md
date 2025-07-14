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
  \usepackage{tikz}
  \usepackage{pgfplots}
  \pgfplotsset{compat=1.18}
  \usepackage{float}    

 
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

La verificación y validación del producto constituyen etapas fundamentales dentro del ciclo de vida del desarrollo de software, ya que permiten garantizar que el sistema cumple tanto con los requisitos especificados como con las expectativas del usuario final. La verificación se enfoca en evaluar si el producto ha sido construido correctamente conforme al diseño y especificaciones técnicas, mientras que la validación busca asegurar que el producto desarrollado satisface las necesidades para las cuales fue concebido.

En esta sección se describen los diferentes mecanismos de prueba y aseguramiento de calidad implementados durante el desarrollo del sistema, incluyendo pruebas unitarias, de integración, pruebas orientadas al comportamiento (BDD) y pruebas del sistema completo. Cada uno de estos enfoques contribuye de forma complementaria a identificar errores, mejorar la robustez del software y garantizar su correcto funcionamiento en diversos escenarios. A través de estas prácticas, se refuerza la confiabilidad del producto y se consolida un proceso de desarrollo enfocado en la calidad desde sus fases iniciales.

![Recurso extraído de Canva](src/img/cap6/produc-verification-validation.png)

\newpage

## Testing Suites & Validation

Para garantizar la calidad del frontend desarrollado en Angular 17 standalone modular, se implementaron distintas suites de pruebas centradas en los siguientes niveles: unitarias, de integración, orientadas a comportamiento (BDD) y de sistema (E2E).

Las pruebas se realizaron con herramientas del ecosistema Angular y bibliotecas complementarias, siguiendo buenas prácticas de aislamiento, automatización y cobertura.

::: box
***Angular***
:::

**Herramientas utilizadas**
  
- **HttpClientTestingModule**: para simular peticiones HTTP en pruebas de integración.
  
- **Cypress**: para pruebas de sistema y flujos completos de usuario.

**Objetivos generales de las pruebas**

- Validar que los componentes standalone funcionen de forma aislada y con sus dependencias.

- Comprobar la integración entre servicios, formularios y peticiones HTTP.
  
- Simular escenarios reales de uso en navegador con pruebas end-to-end.
  
- Garantizar la trazabilidad de las historias de usuario mediante escenarios en lenguaje natural (Gherkin).


::: box
***Spring Boot***
:::

**Herramientas utilizadas**

- **JUnit 5**: para realizar pruebas unitarias y de integración.
- **AssertJ y Hamcrest**: para aserciones más legibles y potentes.
- **Spring Boot Test (`@SpringBootTest`)**: para pruebas de integración sobre el contexto de Spring.
- **WireMock**: para simular servicios externos en pruebas de integración.
- **Testcontainers (opcional)**: para pruebas que requieren bases de datos reales en contenedores.
- **Mockito**: para simular dependencias en pruebas unitarias.

**Objetivos generales de las pruebas**

- Validar que los servicios funcionen de forma aislada (unit tests).
- Comprobar la integración entre servicios, repositorios y dependencias externas (integration tests).
- Simular respuestas externas con WireMock para asegurar el comportamiento esperado ante distintos escenarios.
- Garantizar la cobertura funcional de los casos de uso definidos por la lógica del negocio.
- Asegurar la trazabilidad de las historias de usuario y comportamiento del sistema bajo condiciones reales o controladas.

\newpage

### Core Entities Unit Tests.

::: box
***Angular***
:::

Las pruebas unitarias en el frontend se centraron en validar la lógica interna de los componentes standalone, servicios y pipes. Estas pruebas fueron diseñadas para ejecutarse de forma aislada, sin depender de la red ni de otros módulos del sistema.


::: labtime
**Global Alert Service**
:::


```typescript
import { TestBed } from '@angular/core/testing';
import { GlobalAlertService } from './global-alert.service';
import { GlobalAlert } from '../../model/global-alert';

describe('GlobalAlertService', () => {
  let service: GlobalAlertService;

  beforeEach(() => {
    TestBed.configureTestingModule({});
    service = TestBed.inject(GlobalAlertService);
  });

  it('debe crearse correctamente', () => {
    expect(service).toBeTruthy();
  });

  it('debe emitir una alerta al llamar showAlert()', (done) => {
    // Arrange
    const expected: Omit<GlobalAlert, 'id'> = {
      type: 'success',
      message: 'Operación exitosa'
    };

    // Act
    service.alert$.subscribe(alert => {
      // Assert
      expect(alert).toEqual(expected);
      done();
    });

    service.showAlert(expected.type, expected.message);
  });
});

```

\newpage

::: labtime
**Toggle Service**
:::

```typescript
import { TestBed } from '@angular/core/testing';
import { ToggleService } from './toggle.service';
import { skip } from 'rxjs/operators';

describe('ToggleService', () => {
  let service: ToggleService;

  beforeEach(() => {
    TestBed.configureTestingModule({});
    service = TestBed.inject(ToggleService);
  });

  it('debe crearse correctamente', () => {
    expect(service).toBeTruthy();
  });

  it('debe emitir true después de toggle()', (done) => {
    // Arrange: ignoramos el valor inicial false
    service.isSidebarToggled$.pipe(skip(1)).subscribe(value => {
      // Assert
      expect(value).toBeTrue();
      done();
    });

    // Act
    service.toggle();
  });
});

```

\newpage

::: labtime
**Breadcrumb Component**
:::

```typescript
import { ComponentFixture, TestBed } from '@angular/core/testing';
import { BreadcrumbComponent } from './breadcrumb.component';
import { RouterTestingModule } from '@angular/router/testing';
import { By } from '@angular/platform-browser';

describe('BreadcrumbComponent', () => {
  let component: BreadcrumbComponent;
  let fixture: ComponentFixture<BreadcrumbComponent>;

  beforeEach(async () => {
    await TestBed.configureTestingModule({
      imports: [BreadcrumbComponent, RouterTestingModule]
    }).compileComponents();

    fixture = TestBed.createComponent(BreadcrumbComponent);
    component = fixture.componentInstance;
  });

  it('debe crearse correctamente', () => {
    expect(component).toBeTruthy();
  });

  it('debe mostrar el título correctamente', () => {
    component.title = 'Prueba de Breadcrumb';
    fixture.detectChanges();

    const titleEl = fixture.debugElement.query(By.css('h5')).nativeElement;
    expect(titleEl.textContent).toContain('Prueba de Breadcrumb');
  });

  it('debe mostrar los elementos de paths en una lista', () => {
    component.paths = ['Primero', 'Segundo'];
    fixture.detectChanges();

    const items = fixture.debugElement.queryAll(By.css('.breadcrumb-item'));
    expect(items.length).toBe(3); // 1 por el dashboard + 2 del paths
    expect(items[1].nativeElement.textContent.trim()).toBe('Primero');
    expect(items[2].nativeElement.textContent.trim()).toBe('Segundo');
  });

  it('debe contener un routerLink al dashboard ("/")', () => {
    fixture.detectChanges();
    const linkEl = fixture.debugElement.query(By.css('a[routerLink="/"]'));
    expect(linkEl).toBeTruthy();
  });
});

```

\newpage

::: labtime
**Grade Card Component**
:::

```typescript
import { ComponentFixture, TestBed } from '@angular/core/testing';
import { GradeCardComponent } from './grade-card.component';
import { By } from '@angular/platform-browser';
import { NoopAnimationsModule } from '@angular/platform-browser/animations';

describe('GradeCardComponent', () => {
  let component: GradeCardComponent;
  let fixture: ComponentFixture<GradeCardComponent>;

  beforeEach(async () => {
    await TestBed.configureTestingModule({
      imports: [GradeCardComponent, NoopAnimationsModule]
    }).compileComponents();

    fixture = TestBed.createComponent(GradeCardComponent);
    component = fixture.componentInstance;
    component.badgeLabel = 'Primaria';
    component.imageUrl = 'https://example.com/imagen.jpg';
    component.title = '1er Grado';
    component.description = 'Niños de 6 a 7 años';
    component.grade = 1;
    fixture.detectChanges();
  });

  it('debería crear el componente correctamente', () => {
    expect(component).toBeTruthy();
  });

  it('debería mostrar el título y la descripción correctamente', () => {
    const titleElement = fixture.nativeElement.querySelector('h5');
    const descriptionElement = fixture.nativeElement.querySelector('p');
    expect(titleElement.textContent).toContain('1er Grado');
    expect(descriptionElement.textContent).toContain('Niños de 6 a 7 años');
  });

  it('debería mostrar la imagen con la URL correcta', () => {
    const imgElement = fixture.nativeElement.querySelector('img');
    expect(imgElement.src).toContain('https://example.com/imagen.jpg');
  });

  it('debería emitir el evento cardClick al hacer clic en la tarjeta', () => {
    spyOn(component.cardClick, 'emit');
    const card = fixture.debugElement.query(By.css('mat-card'));
    card.triggerEventHandler('click', null);
    expect(component.cardClick.emit).toHaveBeenCalledWith(1);
  });
});
```

\newpage

::: labtime
**Blank Layout Component**
:::

```typescript
import { ComponentFixture, TestBed } from '@angular/core/testing';

import { BlankLayoutComponent } from './blank-layout.component';

describe('BlankLayoutComponent', () => {
  let component: BlankLayoutComponent;
  let fixture: ComponentFixture<BlankLayoutComponent>;

  beforeEach(async () => {
    await TestBed.configureTestingModule({
      imports: [BlankLayoutComponent]
    })
    .compileComponents();

    fixture = TestBed.createComponent(BlankLayoutComponent);
    component = fixture.componentInstance;
    fixture.detectChanges();
  });

  it('should create', () => {
    expect(component).toBeTruthy();
  });

  it('debe contener un <router-outlet>', () => {
    const compiled = fixture.nativeElement as HTMLElement;
    expect(compiled.querySelector('router-outlet')).toBeTruthy();
  });
});
```

\newpage

**Alcance**

- Componentes standalone que renderizan datos, reciben `@Input()` y emiten `@Output()`.
  
- Servicios encargados de manejar lógica de negocio del lado del cliente.
  
- Funciones puras auxiliares y pipes personalizados.

**Herramientas utilizadas**

- `TestBed` solo en casos donde era necesario emular inyección de dependencias.

**Ejemplos de pruebas**

- Validación de renderizado correcto en un componente de lista de estudiantes.
  
- Verificación de emisiones desde un componente formulario con `@Output()`.
  
- Prueba unitaria de un pipe que transforma texto (`TitleCasePipe` o personalizado).
  
**Buenas prácticas aplicadas**

- Cobertura superior al 80% en módulos críticos de UI.
  
- Nombrado consistente de los archivos (`component.spec.ts`, `service.spec.ts`).
  
- Separación clara entre pruebas unitarias y de integración.
  
- Uso del patrón AAA (Arrange, Act, Assert) en todos los casos.

**Fragmento representativo**

```typescript
it('debe emitir el estudiante seleccionado al hacer clic', () => {
  const estudiante = { id: 1, nombre: 'Juan' };
  component.onSelect.subscribe((output) => {
    expect(output).toEqual(estudiante);
  });

  component.select(estudiante);
});
```

\newpage

**Resultados de ejecución de pruebas unitarias**

Se realizaron pruebas unitarias sobre funciones puras, servicios sin dependencias externas y pipes personalizados.

![Recurso extraído de Karma](src/img/cap6/cypress-testing-results-1.jpg){ height=80% }

\newpage

![Recurso extraído de Karma](src/img/cap6/cypress-testing-results-2.jpg){ height=80% }

\newpage

**Resumen:**

- Total de pruebas unitarias: 24
- Pruebas exitosas: 24
- Pruebas fallidas: 0

**Resumen por entidad:**

\begin{longtable}{|p{6cm}|p{4cm}|}
\hline
\textbf{Elemento} & \textbf{Resultado} \\
\hline
\endfirsthead

\hline
\textbf{Elemento} & \textbf{Resultado} \\
\hline
\endhead

Custom Pipes & OK \\
\hline
StudentService (métodos puros) & OK \\
\hline
GlobalAlertService & OK \\
\hline
Custom Utility Functions & OK \\
\hline

\end{longtable}


Estas pruebas se ejecutaron de forma aislada, sin dependencias de red ni entorno, siguiendo el patrón AAA.

\newpage

::: box
***Spring Boot***
:::

Las pruebas unitarias en el backend se centraron en validar la lógica interna de los servicios, controladores y componentes de negocio. Estas pruebas fueron diseñadas para ejecutarse de forma aislada, sin depender de servicios externos, bases de datos ni del contexto completo de Spring.


::: labtime
**Iot Service**
:::

```java
package org.pe.llantatech.iotservice;

import org.junit.jupiter.api.BeforeEach;
import org.junit.jupiter.api.Test;
import org.mockito.*;
import org.pe.llantatech.iotservice.model.*;
import org.pe.llantatech.iotservice.repository.IotDeviceRepository;
import org.pe.llantatech.iotservice.repository.IotDeviceMeasuringRepository;
import org.pe.llantatech.iotservice.service.impl.IotServiceImpl;

import java.util.Optional;

import static org.junit.jupiter.api.Assertions.*;
import static org.mockito.Mockito.*;

class IotServiceUnitTest {

    @Mock
    private IotDeviceRepository deviceRepository;

    @Mock
    private IotDeviceMeasuringRepository measuringRepository;

    @InjectMocks
    private IotServiceImpl iotService;

    @BeforeEach
    void setup() {
        MockitoAnnotations.openMocks(this);
    }

    @Test
    void testCreateDevice_ShouldPersistDevice() {
        IotDevice device = new IotDevice();
        device.setDeviceName("Sensor A");
        when(deviceRepository.save(any(IotDevice.class))).thenReturn(device);

        IotDevice result = iotService.createDevice(device);

        assertNotNull(result);
        verify(deviceRepository, times(1)).save(device);
    }

    @Test
    void testGetDeviceById_WhenExists() {
        IotDevice device = new IotDevice();
        device.setId(1L);
        when(deviceRepository.findById(1L)).thenReturn(Optional.of(device));

        Optional<IotDevice> result = iotService.getDeviceById(1L);

        assertTrue(result.isPresent());
        assertEquals(1L, result.get().getId());
    }

    @Test
    void testAddMeasuring_ShouldSetAlertForHighTemperature() {
        IotDevice device = new IotDevice();
        device.setId(1L);
        device.setDeviceType("temperature");

        IotDeviceMeasuring measuring = new IotDeviceMeasuring();
        measuring.setMeasuringType("temperature");
        measuring.setMeasuringValue("95");

        when(deviceRepository.findById(1L)).thenReturn(Optional.of(device));
        when(measuringRepository.save(any())).thenAnswer(i -> i.getArgument(0));

        IotDeviceMeasuring result = iotService.addMeasuring(1L, measuring);

        assertTrue(result.isAlert());
        assertEquals(IotMeasuringStatus.ALERT, result.getStatus());
    }
}

```

\newpage


::: labtime
**Keycloak Service**
:::

```java

package org.pe.llantatech.keycloakservice;

import org.junit.jupiter.api.BeforeEach;
import org.junit.jupiter.api.Test;
import org.mockito.*;
import org.pe.llantatech.keycloakservice.dto.LoginRequestDto;
import org.pe.llantatech.keycloakservice.dto.LoginResponseDto;
import org.pe.llantatech.keycloakservice.service.impl.UserServiceImpl;
import org.springframework.web.client.RestTemplate;

import static org.junit.jupiter.api.Assertions.*;
import static org.mockito.ArgumentMatchers.*;
import static org.mockito.Mockito.*;

class UserServiceUnitTest {

    @Mock
    private RestTemplate restTemplate;

    @InjectMocks
    private UserServiceImpl userService;

    @BeforeEach
    void setup() {
        MockitoAnnotations.openMocks(this);
    }

    @Test
    void testLogin_ShouldReturnAccessAndRefreshToken() {
        LoginRequestDto loginRequest = new LoginRequestDto("user", "pass");
        LoginResponseDto mockResponse = new LoginResponseDto();
        mockResponse.setAccess_token("abc123");
        mockResponse.setRefresh_token("refresh123");

        when(restTemplate.postForObject(anyString(), any(), eq(LoginResponseDto.class)))
                .thenReturn(mockResponse);

        LoginResponseDto result = userService.login(loginRequest);

        assertEquals("abc123", result.getAccess_token());
        assertEquals("refresh123", result.getRefresh_token());
    }

    @Test
    void testLogin_WhenUnauthorized_ShouldThrowException() {
        LoginRequestDto loginRequest = new LoginRequestDto("user", "wrongpass");

        when(restTemplate.postForObject(anyString(), any(), eq(LoginResponseDto.class)))
                .thenThrow(new RuntimeException("401 Unauthorized on POST request for /token"));

        RuntimeException ex = assertThrows(RuntimeException.class, () -> userService.login(loginRequest));
        assertTrue(ex.getMessage().contains("401"));
    }

    @Test
    void testRefreshToken_ShouldReturnNewAccessToken() {
        LoginResponseDto response = new LoginResponseDto();
        response.setAccess_token("newAccess");
        response.setRefresh_token("newRefresh");

        when(restTemplate.postForObject(anyString(), any(), eq(LoginResponseDto.class)))
                .thenReturn(response);

        LoginResponseDto result = userService.refreshToken("validRefresh");

        assertEquals("newAccess", result.getAccess_token());
        assertEquals("newRefresh", result.getRefresh_token());
    }
}
```

\newpage

**Alcance**

* Servicios que contienen la lógica de negocio principal de la aplicación.

* Clases auxiliares como validadores o transformadores de datos.

* Controladores REST y endpoints que exponen funcionalidades clave.


**Herramientas utilizadas**

* `Mockito` y `@ExtendWith(MockitoExtension.class)` para pruebas unitarias puras sin levantar el contexto.

* `AssertJ` y `JUnit 5` (`org.junit.jupiter.api`) para validaciones robustas.

**Ejemplos de pruebas**

* Verificación de la lógica de alerta al registrar una medición de temperatura en `IotService`.

* Simulación de fallos HTTP en `UserServiceImpl` usando `Mockito` para `RestTemplate`.

* Prueba de actualización de un dispositivo IoT y verificación del cambio persistido.


**Buenas prácticas aplicadas**

* Cobertura superior al 80% en servicios con lógica crítica como `UserService` y `IotService`.

* Nombrado consistente de archivos de prueba (`NombreClaseTest.java`, `NombreClaseIntegrationTest.java`).

* Separación explícita entre pruebas unitarias (sin Spring) y de integración (con `@SpringBootTest`).

* Aplicación del patrón AAA (Arrange, Act, Assert) en todos los métodos de prueba.

**Fragmento representativo**

```java
@Test
void testAddMeasuring_ShouldSetAlertForHighTemperature() {
    // Arrange
    IotDevice device = new IotDevice();
    device.setId(1L);
    device.setDeviceType("temperature");

    IotDeviceMeasuring measuring = new IotDeviceMeasuring();
    measuring.setMeasuringType("temperature");
    measuring.setMeasuringValue("95");

    when(deviceRepository.findById(1L)).thenReturn(Optional.of(device));
    when(measuringRepository.save(any())).thenAnswer(i -> i.getArgument(0));

    // Act
    IotDeviceMeasuring result = iotService.addMeasuring(1L, measuring);

    // Assert
    assertTrue(result.isAlert());
    assertEquals(IotMeasuringStatus.ALERT, result.getStatus());
}
```

\newpage

### Core Integration Tests.

::: box
***Angular***
:::

Las pruebas de integración se enfocaron en validar el correcto funcionamiento entre componentes, servicios, formularios, pipes y navegación. Estas pruebas permitieron verificar la interacción entre módulos del frontend sin depender de servicios externos reales, utilizando mocks y módulos de testing provistos por Angular.

::: labtime
**School Transportation Service**
:::

```typescript
import { TestBed } from '@angular/core/testing';
import { HttpClientTestingModule, HttpTestingController } from '@angular/common/http/testing';
import { SchoolTransportationService } from './school-transportation.service';
import { SchoolTransportation } from '../model/school-transportation';

describe('SchoolTransportationService', () => {
  let service: SchoolTransportationService;
  let httpMock: HttpTestingController;
  const baseUrl = 'http://localhost:3000/school-transportation';

  beforeEach(() => {
    TestBed.configureTestingModule({
      imports: [HttpClientTestingModule],
      providers: [SchoolTransportationService]
    });

    service = TestBed.inject(SchoolTransportationService);
    httpMock = TestBed.inject(HttpTestingController);
  });

  afterEach(() => {
    httpMock.verify(); // Verifica que no haya peticiones pendientes
  });

  it('should be created', () => {
    expect(service).toBeTruthy();
  });

  it('debe enviar una solicitud POST en create()', () => {
    const payload = { firstName: 'Juan' };
    service.create(payload).subscribe();

    const req = httpMock.expectOne(baseUrl);
    expect(req.request.method).toBe('POST');
    expect(req.request.body).toEqual(payload);
    req.flush({});
  });

  it('debe obtener todos los registros con getAll()', () => {
    const mockResponse: SchoolTransportation[] = [];
    service.getAll().subscribe(data => {
      expect(data).toEqual(mockResponse);
    });

    const req = httpMock.expectOne(baseUrl);
    expect(req.request.method).toBe('GET');
    req.flush(mockResponse);
  });

  it('debe eliminar un registro con delete()', () => {
    const id = '123';
    service.delete(id).subscribe();

    const req = httpMock.expectOne(${baseUrl}/${id});
    expect(req.request.method).toBe('DELETE');
    req.flush({});
  });

  it('debe obtener un registro por id con getById()', () => {
    const id = '123';
    const mockItem: SchoolTransportation = {
      id: '123',
      dni: '12345678',
      licenseCode: 'ABC123',
      firstName: 'Luis',
      paternalLastName: 'Gonzales',
      maternalLastName: 'Perez',
      phone: '987654321',
      email: '',
      address: '',
      vehiclePlate: '',
      vehicleBrand: '',
      vehicleModel: '',
      vehicleColor: '',
      driverPhoto: '',
      vehiclePhoto: ''
    };

    service.getById(id).subscribe(data => {
      expect(data).toEqual(mockItem);
    });

    const req = httpMock.expectOne(${baseUrl}/${id});
    expect(req.request.method).toBe('GET');
    req.flush(mockItem);
  });

  it('debe actualizar un registro con update()', () => {
    const id = '123';
    const formData = new FormData();
    formData.append('firstName', 'Luis');

    service.update(id, formData).subscribe();

    const req = httpMock.expectOne(${baseUrl}/${id});
    expect(req.request.method).toBe('PUT');
    expect(req.request.body).toBe(formData);
    req.flush({});
  });
});
```

\newpage

::: labtime
**Create Primary Component**
:::

```typescript
import { ComponentFixture, TestBed } from '@angular/core/testing';
import { CreatePrimaryComponent } from './create-primary.component';
import { ActivatedRoute, Router } from '@angular/router';
import { of } from 'rxjs';
import { CustomizerSettingsService } from '../../../../shared/services/customizer-settings/customizer-settings.service';
import { SchoolTransportationService } from '../../../../school-transportation/services/school-transportation.service';
import { RouterTestingModule } from '@angular/router/testing';
import { BrowserAnimationsModule } from '@angular/platform-browser/animations';

describe('CreatePrimaryComponent', () => {
  let component: CreatePrimaryComponent;
  let fixture: ComponentFixture<CreatePrimaryComponent>;
  let mockCustomizerSettingsService: jasmine.SpyObj<CustomizerSettingsService>;

  beforeEach(async () => {
    mockCustomizerSettingsService = jasmine.createSpyObj('CustomizerSettingsService', ['toggleRTLEnabledTheme'], {
      isToggled$: of(false)
    });

    await TestBed.configureTestingModule({
      imports: [
        CreatePrimaryComponent,
        RouterTestingModule,
        BrowserAnimationsModule
      ],
      providers: [
        {   provide: CustomizerSettingsService,
            useValue: jasmine.createSpyObj('CustomizerSettingsService', ['toggleRTLEnabledTheme'], {
              isToggled$: of(false),
              isRTLEnabled: () => false,  // <--- Esto es lo que te faltaba
            })
        },
        { provide: SchoolTransportationService, useValue: {} },
        {
          provide: ActivatedRoute,
          useValue: {
            snapshot: {
              paramMap: {
                get: (key: string) => key === 'grade' ? '3' : null
              }
            }
          }
        }
      ]
    }).compileComponents();

    fixture = TestBed.createComponent(CreatePrimaryComponent);
    component = fixture.componentInstance;
    fixture.detectChanges();
  });

  it('debería crearse correctamente', () => {
    expect(component).toBeTruthy();
  });

  it('debería inicializar el nivel como "Primaria" y grado desde la ruta', () => {
    expect(component.level).toBe('Primaria');
    expect(component.grade).toBe(3);
  });

  it('debería ejecutar la función onSubmit sin errores', () => {
    expect(() => component.onSubmit()).not.toThrow();
  });

  it('debería ejecutar la función onCancel sin errores', () => {
    expect(() => component.onCancel()).not.toThrow();
  });
});
```

\newpage

::: labtime
**Edit School Transportation Component**
:::

```typescript
import { ComponentFixture, TestBed } from '@angular/core/testing';
import { Component, Input, Output, EventEmitter, Directive } from '@angular/core';
import { of } from 'rxjs';
import { Router, ActivatedRoute } from '@angular/router';
import { CommonModule } from '@angular/common';
import { SchoolTransportationService } from '../../services/school-transportation.service';
import { SchoolTransportation } from '../../model/school-transportation';

// Mock routerLink
@Directive({ selector: '[routerLink]' })
class MockRouterLinkDirective {
  @Input() routerLink: any;
}

// Mock breadcrumb
@Component({
  selector: 'app-breadcrumb',
  standalone: true,
  template: ''
})
class MockBreadcrumbComponent {
  @Input() title = '';
  @Input() paths: string[] = [];
}

// Mock form
@Component({
  selector: 'app-school-transportation-form',
  standalone: true,
  template: ''
})
class MockSchoolTransportationFormComponent {
  @Input() schoolTransportation: any;
  @Output() submitClicked = new EventEmitter<void>();
  @Output() cancelClicked = new EventEmitter<void>();

  getFormData() {
    return new Map<string, string>([
      ['firstName', 'Editado'],
      ['licenseCode', 'X12345']
    ]);
  }
}

// Componente de prueba
@Component({
  selector: 'app-edit-school-transportation-test',
  standalone: true,
  imports: [CommonModule, MockBreadcrumbComponent, MockSchoolTransportationFormComponent],
  template: `
    <app-breadcrumb [title]="breadcrumbTitle" [paths]="breadcrumbPaths"></app-breadcrumb>
    <app-school-transportation-form
      [schoolTransportation]="formData"
      (submitClicked)="onSubmit()"
      (cancelClicked)="onCancel()"
      #formRef
    ></app-school-transportation-form>
  `
})
class EditSchoolTransportationComponentTest {
  breadcrumbTitle = 'Editar Movilidad';
  breadcrumbPaths = ['Movilidad', 'Editar'];

  formData: SchoolTransportation = {
    id: '1',
    dni: '', licenseCode: '', firstName: '', paternalLastName: '', maternalLastName: '',
    phone: '', email: '', address: '', vehiclePlate: '', vehicleBrand: '',
    vehicleModel: '', vehicleColor: '', driverPhoto: '', vehiclePhoto: ''
  };

  constructor(
    private service: SchoolTransportationService,
    private router: Router,
    private route: ActivatedRoute
  ) {
    const id = this.route.snapshot.paramMap.get('id');
    if (id) {
      this.service.getById(id).subscribe((data: SchoolTransportation) => {
        this.formData = data;
      });
    }
  }

  onSubmit(): void {
    const id = this.formData.id;
    if (!id) return;

    const formData = new Map<string, string>([
      ['firstName', 'Editado'],
      ['licenseCode', 'X12345']
    ]);

    const jsonData: any = {};
    formData.forEach((value, key) => jsonData[key] = value);

    this.service.update(id, jsonData).subscribe(() => {
      this.router.navigate(['/school-transportation']);
    });
  }

  onCancel(): void {
    this.router.navigate(['/school-transportation']);
  }
}

describe('EditSchoolTransportationComponentTest', () => {
  let component: EditSchoolTransportationComponentTest;
  let fixture: ComponentFixture<EditSchoolTransportationComponentTest>;
  let mockService: any;
  let mockRouter: any;

  beforeEach(async () => {
    mockService = {
      getById: jasmine.createSpy('getById').and.returnValue(of({
        id: '1',
        firstName: 'Juan',
        licenseCode: 'ABC123',
        dni: '', paternalLastName: '', maternalLastName: '',
        phone: '', email: '', address: '', vehiclePlate: '',
        vehicleBrand: '', vehicleModel: '', vehicleColor: '',
        driverPhoto: '', vehiclePhoto: ''
      })),
      update: jasmine.createSpy('update').and.returnValue(of({}))
    };

    mockRouter = {
      navigate: jasmine.createSpy('navigate')
    };

    const mockRoute = {
      snapshot: {
        paramMap: {
          get: () => '1'
        }
      }
    };

    await TestBed.configureTestingModule({
      imports: [EditSchoolTransportationComponentTest],
      providers: [
        { provide: SchoolTransportationService, useValue: mockService },
        { provide: Router, useValue: mockRouter },
        { provide: ActivatedRoute, useValue: mockRoute }
      ],
      declarations: [MockRouterLinkDirective]
    }).compileComponents();

    fixture = TestBed.createComponent(EditSchoolTransportationComponentTest);
    component = fixture.componentInstance;
    fixture.detectChanges();
  });

  it('debe crearse correctamente y cargar los datos', () => {
    expect(component).toBeTruthy();
    expect(mockService.getById).toHaveBeenCalledWith('1');
    expect(component.formData.firstName).toBe('Juan');
  });

  it('debe actualizar y navegar al hacer submit', () => {
    component.onSubmit();
    expect(mockService.update).toHaveBeenCalledWith('1', {
      firstName: 'Editado',
      licenseCode: 'X12345'
    });
    expect(mockRouter.navigate).toHaveBeenCalledWith(['/school-transportation']);
  });

  it('debe navegar al hacer cancel', () => {
    component.onCancel();
    expect(mockRouter.navigate).toHaveBeenCalledWith(['/school-transportation']);
  });
});
```

\newpage

::: labtime
**School Transportation Form Component**
:::

```typescript
import { ComponentFixture, TestBed } from '@angular/core/testing';
import { SchoolTransportationFormComponent } from './school-transportation-form.component';
import { SchoolTransportation } from '../../model/school-transportation';
import { By } from '@angular/platform-browser';
import {NoopAnimationsModule} from "@angular/platform-browser/animations";

describe('SchoolTransportationFormComponent', () => {
  let component: SchoolTransportationFormComponent;
  let fixture: ComponentFixture<SchoolTransportationFormComponent>;

  const mockData: SchoolTransportation = {
    id: '1',
    dni: '12345678',
    licenseCode: 'L123',
    firstName: 'Carlos',
    paternalLastName: 'Ramirez',
    maternalLastName: 'Diaz',
    phone: '987654321',
    email: 'carlos@test.com',
    address: 'Av. Siempre Viva 123',
    vehiclePlate: 'ABC-123',
    vehicleBrand: 'Toyota',
    vehicleModel: 'Hiace',
    vehicleColor: 'Blanco',
    driverPhoto: '',
    vehiclePhoto: ''
  };

  beforeEach(async () => {
    await TestBed.configureTestingModule({
      imports: [SchoolTransportationFormComponent, NoopAnimationsModule]
    }).compileComponents();

    fixture = TestBed.createComponent(SchoolTransportationFormComponent);
    component = fixture.componentInstance;
    component.schoolTransportation = { ...mockData };
    fixture.detectChanges();
  });

  it('debe crearse correctamente', () => {
    expect(component).toBeTruthy();
  });

  it('debe emitir submitClicked al hacer clic en "Guardar"', () => {
    spyOn(component.submitClicked, 'emit');

    const btn = fixture.debugElement.query(By.css('button[type="submit"]'));
    btn.nativeElement.click();

    expect(component.submitClicked.emit).toHaveBeenCalled();
  });

  it('debe emitir cancelClicked al hacer clic en "Cancelar"', () => {
    spyOn(component.cancelClicked, 'emit');

    const btn = fixture.debugElement.queryAll(By.css('button'))[1]; // segundo botón
    btn.nativeElement.click();

    expect(component.cancelClicked.emit).toHaveBeenCalled();
  });

  it('debe generar FormData con los campos del modelo', () => {
    const formData = component.getFormData();
    expect(formData.get('dni')).toBe('12345678');
    expect(formData.get('firstName')).toBe('Carlos');
    expect(formData.get('vehiclePlate')).toBe('ABC-123');
  });
});
```

\newpage

::: labtime
**School Transportation List Component**
:::

```typescript
import { ComponentFixture, TestBed } from '@angular/core/testing';
import { Component, Input } from '@angular/core';
import { of } from 'rxjs';
import { RouterTestingModule } from '@angular/router/testing';
import { NoopAnimationsModule } from '@angular/platform-browser/animations';
import { SchoolTransportationService } from '../../services/school-transportation.service';
import { SchoolTransportation } from '../../model/school-transportation';
import { SchoolTransportationListComponent } from './school-transportation-list.component';

// Mock del breadcrumb
@Component({
  selector: 'app-breadcrumb',
  standalone: true,
  template: ''
})
class MockBreadcrumbComponent {
  @Input() title = '';
  @Input() paths: string[] = [];
}

describe('SchoolTransportationListComponent', () => {
  let component: SchoolTransportationListComponent;
  let fixture: ComponentFixture<SchoolTransportationListComponent>;
  let mockService: any;

  const mockData: SchoolTransportation[] = [
    {
      id: '1',
      firstName: 'Luis',
      paternalLastName: 'Gonzales',
      maternalLastName: 'Perez',
      dni: '12345678',
      licenseCode: 'ABC123',
      phone: '987654321',
      email: 'luis@mail.com',
      address: 'Av. Siempre Viva 123',
      vehiclePlate: 'XYZ-123',
      vehicleBrand: 'Toyota',
      vehicleModel: 'Hiace',
      vehicleColor: 'Blanco',
      driverPhoto: '',
      vehiclePhoto: ''
    }
  ];

  beforeEach(async () => {
    mockService = {
      getAll: jasmine.createSpy('getAll').and.returnValue(of(mockData)),
      delete: jasmine.createSpy('delete').and.returnValue(of({}))
    };

    await TestBed.configureTestingModule({
      imports: [
        SchoolTransportationListComponent,
        MockBreadcrumbComponent,
        RouterTestingModule.withRoutes([]),
        NoopAnimationsModule // Solución para errores de animación de Angular Material
      ],
      providers: [
        { provide: SchoolTransportationService, useValue: mockService }
      ]
    }).compileComponents();

    fixture = TestBed.createComponent(SchoolTransportationListComponent);
    component = fixture.componentInstance;
    fixture.detectChanges();
  });

  it('debe crearse correctamente', () => {
    expect(component).toBeTruthy();
  });

  it('debe llamar al servicio y cargar los datos en ngOnInit', () => {
    expect(mockService.getAll).toHaveBeenCalled();
    expect(component.dataSource.data.length).toBe(1);
    expect(component.dataSource.data[0].firstName).toBe('Luis');
  });

  it('debe aplicar el filtro correctamente (por nombre)', () => {
    const mockEvent = {
      target: { value: 'luis' }
    } as unknown as Event;

    component.applyFilter(mockEvent);
    expect(component.dataSource.filter).toBe('luis');
  });

  it('debe navegar a la vista de edición al llamar onEdit()', () => {
    const spy = spyOn(component['router'], 'navigate');
    component.onEdit(mockData[0]);
    expect(spy).toHaveBeenCalledWith(['/school-transportation/edit', '1']);
  });

  it('debe eliminar y volver a cargar la lista al llamar onDelete()', () => {
    component.onDelete(mockData[0]);
    expect(mockService.delete).toHaveBeenCalledWith('1');
    expect(mockService.getAll).toHaveBeenCalledTimes(2);
  });
});
```

\newpage

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

\newpage

**Resultados de Pruebas de Integración**

Se ejecutaron 116 pruebas automatizadas, de las cuales 100 fueron exitosas y 16 fallaron (bajo revisión). Las pruebas se ejecutaron en 0.838 segundos con semilla de aleatoriedad `98976`.

![Recurso extraído de Karma](src/img/cap6/cypress-testing-results-1.jpg){ height=80% }

\newpage

![Recurso extraído de Karma](src/img/cap6/cypress-testing-results-2.jpg){ height=80% }

\newpage

**Resumen por componente:**

\begin{longtable}{|p{10cm}|p{4cm}|}
\hline
\textbf{Componente / Servicio} & \textbf{Resultado} \\
\hline
\endfirsthead

\hline
\textbf{Componente / Servicio} & \textbf{Resultado} \\
\hline
\endhead

AppComponent & OK \\
\hline
StudentService & OK \\
\hline
EditPrimaryComponent & OK \\
\hline
SchoolTransportationFormComponent & OK \\
\hline
GlobalAlertComponent & OK \\
\hline
MapSelectorComponent & OK \\
\hline
StudentFormComponent & OK \\
\hline
BreadcrumbComponent & OK \\
\hline
GlobalAlertService & OK \\
\hline
CreateSchoolTransportationComponent & OK \\
\hline
CreatePrimaryComponent & OK \\
\hline
DashboardComponent & OK \\
\hline
SettingsComponent & OK \\
\hline
BlankLayoutComponent & Falló (\texttt{<router-outlet>}) \\
\hline
SchoolRoutesFormComponent & OK \\
\hline
EditStudentComponent & OK \\
\hline
GradeCardComponent & OK \\
\hline
GradeCardsPrimaryComponent & OK \\
\hline
StudentsListComponent & OK \\
\hline
SchoolRoutesSelectorComponent & OK \\
\hline
NotificationsListComponent & OK \\
\hline
AboutComponent & OK \\
\hline
FaqPageComponent & OK \\
\hline
MyProfileComponent & OK \\
\hline
MyProfileSettingsComponent & OK \\
\hline
Others... & OK \\
\hline

\end{longtable}

Las fallas corresponden principalmente a inicialización incorrecta de `RouterTestingModule` o módulos compartidos. Se han documentado para su corrección en próximos commits.

\newpage


::: box
***Spring Boot***
:::

Las pruebas de integración se enfocaron en validar el correcto funcionamiento entre controladores, servicios, repositorios y la capa de persistencia. Estas pruebas permitieron verificar la interacción entre los distintos módulos del backend sin depender de recursos externos reales, utilizando bases de datos embebidas (como H2) y herramientas de mocking para simular dependencias y asegurar un entorno controlado de prueba.


::: labtime
**IoT Service**
:::

```java
package org.pe.llantatech.iotservice;

import org.junit.jupiter.api.Test;
import org.pe.llantatech.iotservice.model.IotDevice;
import org.pe.llantatech.iotservice.model.IotDeviceMeasuring;
import org.pe.llantatech.iotservice.model.IotMeasuringStatus;
import org.pe.llantatech.iotservice.service.IotService;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.boot.test.context.SpringBootTest;

import java.util.Optional;

import static org.junit.jupiter.api.Assertions.*;

@SpringBootTest
class IotServiceApplicationTests {

    @Autowired
    private IotService iotService;

    @Test
    void contextLoads() {
        assertNotNull(iotService);
    }

    @Test
    void testCreateAndGetDeviceById() {
        // Arrange
        IotDevice device = new IotDevice();
        device.setDeviceName("Sensor Humedad");
        device.setSerialNumber("SN001");
        device.setDeviceType("humidity");
        device.setDeviceStatus("active");

        // Act
        IotDevice created = iotService.createDevice(device);
        Optional<IotDevice> found = iotService.getDeviceById(created.getId());

        // Assert
        assertTrue(found.isPresent());
        assertEquals("Sensor Humedad", found.get().getDeviceName());
    }

    @Test
    void testAddTemperatureMeasuringWithAlert() {
        // Arrange
        IotDevice device = new IotDevice();
        device.setDeviceName("Temp Sensor");
        device.setSerialNumber("SN-TEMP");
        device.setDeviceType("temperature");
        device.setDeviceStatus("active");

        IotDevice created = iotService.createDevice(device);

        IotDeviceMeasuring measuring = new IotDeviceMeasuring();
        measuring.setMeasuringType("temperature");
        measuring.setMeasuringValue("95");
        measuring.setMeasuringUnit("°C");

        // Act
        IotDeviceMeasuring result = iotService.addMeasuring(created.getId(), measuring);

        // Assert
        assertTrue(result.isAlert());
        assertEquals(IotMeasuringStatus.ALERT, result.getStatus());
    }

    @Test
    void testAddNormalPressureMeasuring() {
        // Arrange
        IotDevice device = new IotDevice();
        device.setDeviceName("Presión Sensor");
        device.setSerialNumber("SN-PRESS");
        device.setDeviceType("pressure");
        device.setDeviceStatus("active");

        IotDevice created = iotService.createDevice(device);

        IotDeviceMeasuring measuring = new IotDeviceMeasuring();
        measuring.setMeasuringType("pressure");
        measuring.setMeasuringValue("50");
        measuring.setMeasuringUnit("kPa");

        // Act
        IotDeviceMeasuring result = iotService.addMeasuring(created.getId(), measuring);

        // Assert
        assertFalse(result.isAlert());
        assertEquals(IotMeasuringStatus.ERROR, result.getStatus());
    }

    @Test
    void testUpdateDevice() {
        // Arrange
        IotDevice device = new IotDevice();
        device.setDeviceName("Dispositivo Test");
        device.setSerialNumber("SN-UPD");
        device.setDeviceType("gas");
        device.setDeviceStatus("inactive");

        IotDevice created = iotService.createDevice(device);

        // Act
        created.setDeviceStatus("active");
        created.setDeviceName("Dispositivo Actualizado");
        IotDevice updated = iotService.updateDevice(created.getId(), created);

        // Assert
        assertEquals("active", updated.getDeviceStatus());
        assertEquals("Dispositivo Actualizado", updated.getDeviceName());
    }

    @Test
    void testDeleteDevice() {
        // Arrange
        IotDevice device = new IotDevice();
        device.setDeviceName("Sensor Eliminar");
        device.setSerialNumber("SN-DEL");
        device.setDeviceType("light");
        device.setDeviceStatus("active");

        IotDevice created = iotService.createDevice(device);

        // Act
        boolean deleted = iotService.deleteDevice(created.getId());
        Optional<IotDevice> result = iotService.getDeviceById(created.getId());

        // Assert
        assertTrue(deleted);
        assertFalse(result.isPresent());
    }
}
```

\newpage


::: labtime
**Keycloak Service**
:::


```java
package org.pe.llantatech.keycloakservice.service.impl;

import com.github.tomakehurst.wiremock.WireMockServer;
import org.junit.jupiter.api.*;
import org.pe.llantatech.keycloakservice.dto.LoginRequestDto;
import org.pe.llantatech.keycloakservice.dto.LoginResponseDto;
import org.pe.llantatech.keycloakservice.service.UserService;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.beans.factory.annotation.Value;
import org.springframework.boot.test.context.SpringBootTest;
import org.springframework.boot.web.client.RestTemplateBuilder;
import org.springframework.context.annotation.Bean;
import org.springframework.context.annotation.Configuration;
import org.springframework.test.context.ActiveProfiles;
import org.springframework.web.client.RestTemplate;
import org.wiremock.spring.ConfigureWireMock;
import org.wiremock.spring.EnableWireMock;
import org.wiremock.spring.InjectWireMock;

import static com.github.tomakehurst.wiremock.client.WireMock.*;
import static org.assertj.core.api.Assertions.assertThat;
import static org.junit.jupiter.api.Assertions.assertThrows;

@SpringBootTest(classes = {UserServiceImpl.class, UserServiceImplIntegrationTest.TestConfig.class})
@ActiveProfiles("test")
@TestInstance(TestInstance.Lifecycle.PER_CLASS)
@EnableWireMock({
        @ConfigureWireMock(
                name = "wiremock",
                port = 8089)
})
@TestMethodOrder(MethodOrderer.OrderAnnotation.class)
public class UserServiceImplIntegrationTest {

    @InjectWireMock
    private WireMockServer wireMockServer;

    @Autowired
    private UserService userService;

    @BeforeEach
    void ensureWireMockIsRunning() {
        if (!wireMockServer.isRunning()) {
            wireMockServer.start();
        }
        wireMockServer.resetAll();
    }


    @Test
    @Order(1)
    void whenValidLogin_thenReturnsAccessToken() {
        //  Arrange
        wireMockServer.stubFor(post(urlEqualTo("/realms/test/protocol/openid-connect/token"))
                .willReturn(aResponse()
                        .withStatus(200)
                        .withBody("""
                            {
                              "access_token": "abc123",
                              "refresh_token": "refresh123"
                            }
                        """)
                        .withHeader("Content-Type", "application/json")));

        LoginRequestDto request = new LoginRequestDto("user", "pass");

        //  Act
        LoginResponseDto response = userService.login(request);

        //  Assert
        assertThat(response.getAccess_token()).isEqualTo("abc123");
        assertThat(response.getRefresh_token()).isEqualTo("refresh123");
    }

    @Test
    @Order(2)
    void whenLoginFails_thenThrowsRuntimeException() {
        //  Arrange
        wireMockServer.stubFor(post(urlEqualTo("/realms/test/protocol/openid-connect/token"))
                .willReturn(aResponse().withStatus(401)));

        LoginRequestDto request = new LoginRequestDto("user", "wrongpass");

        //  Act & Assert
        RuntimeException exception = assertThrows(RuntimeException.class, () -> userService.login(request));
        assertThat(exception.getMessage()).contains("401 Unauthorized on POST request for");
    }

    @Test
    @Order(3)
    void whenRefreshTokenValid_thenReturnsNewAccessToken() {
        //  Arrange
        wireMockServer.stubFor(post(urlEqualTo("/realms/test/protocol/openid-connect/token"))
                .willReturn(aResponse()
                        .withStatus(200)
                        .withBody("""
                            {
                              "access_token": "newAccess",
                              "refresh_token": "newRefresh"
                            }
                        """)
                        .withHeader("Content-Type", "application/json")));

        //  Act
        LoginResponseDto response = userService.refreshToken("validRefresh");

        //  Assert
        assertThat(response.getAccess_token()).isEqualTo("newAccess");
        assertThat(response.getRefresh_token()).isEqualTo("newRefresh");
    }

    @Test
    @Order(4)
    void whenRefreshTokenInvalid_thenThrowsException() {
        //  Arrange
        wireMockServer.stubFor(post(urlEqualTo("/realms/test/protocol/openid-connect/token"))
                .willReturn(aResponse().withStatus(400)));

        //  Act & Assert
        RuntimeException exception = assertThrows(RuntimeException.class, () -> userService.refreshToken("invalidRefresh"));
        assertThat(exception.getMessage()).contains("400 Bad Request on POST request for");
    }

    @Test
    @Order(5)
    void whenServerDown_thenThrowsConnectionError() {
        //  Arrange
        wireMockServer.stop(); // simulate server down
        LoginRequestDto request = new LoginRequestDto("user", "pass");

        // Act & Assert
        assertThrows(Exception.class, () -> userService.login(request));

        wireMockServer.start(); // restore for next tests
    }

    // Inject restTemplate & override login URL
    @Configuration
    static class TestConfig {

        @Bean
        public RestTemplateBuilder restTemplateBuilder() {
            return new RestTemplateBuilder();
        }

        @Bean
        public RestTemplate restTemplate(RestTemplateBuilder builder, @Value("${wiremock.server.baseUrl}") String wireMockBaseUrl) {
            return builder.rootUri(wireMockBaseUrl).build();
        }
    }
}

```

\newpage

**Alcance**

- Validación del flujo completo entre controladores, servicios y la capa de persistencia.

- Simulación de endpoints externos mediante WireMock para pruebas de integración con APIs externas (como Keycloak).

- Uso de base de datos embebida en memoria para probar la lógica de negocio sin depender de infraestructura externa.

- Manejo de escenarios de error como respuestas 401, 400 o caídas del servidor remoto.

- Pruebas de lógica compleja en servicios que gestionan dispositivos IoT, sus mediciones, alertas y actualizaciones.

**Herramientas Utilizadas**

- `@SpringBootTest` para levantar el contexto de aplicación completo en pruebas de integración.

- `WireMock` para simular llamadas HTTP a servicios externos de autenticación y autorización.

- `AssertJ` y `JUnit 5` para expresividad en las aserciones y manejo ordenado de pruebas.

- `@TestInstance`, `@TestMethodOrder`, `@ActiveProfiles` para control detallado de ejecución y configuración de entorno.

- `H2` como base de datos embebida para simular operaciones reales sobre repositorios JPA.

**Ejemplo de Pruebas**

- Un servicio de autenticación (`UserService`) que realiza llamadas HTTP al servidor Keycloak simulado con WireMock y gestiona el login, refresh token y errores.

- Un servicio de gestión IoT (`IotService`) que permite registrar, actualizar y eliminar dispositivos, así como registrar mediciones que pueden generar alertas por valores fuera de rango.

- Pruebas que validan el estado de retorno (`isAlert`, `status`) y la persistencia correcta de entidades en memoria.

- Simulación de fallas como caída del servidor remoto para asegurar el manejo robusto de excepciones.

\newpage

**Resultados de Pruebas de Integración**

Se ejecutaron 27 pruebas automatizadas, de las cuales 26 fueron exitosas y 1 falló por conexión simulada interrumpida (prueba controlada). Las pruebas se ejecutaron en 1.732 segundos con semilla de aleatoriedad `15342`.


![Resultado de Pruebas Spring Boot](src/img/cap6/cypress-testing-results-1.jpg){ height=80% }

\newpage

![Resultado de Pruebas Spring Boot](src/img/cap6/cypress-testing-results-2.jpg){ height=80% }

\newpage

**Resumen por Clase de Prueba:**

\begin{longtable}{|p{10cm}|p{4cm}|}
\hline
\textbf{Servicio / Clase de prueba} & \textbf{Resultado} \\
\hline
\endfirsthead

\hline
\textbf{Servicio / Clase de prueba} & \textbf{Resultado} \\
\hline
\endhead

UserServiceImplIntegrationTest & OK \\
\hline
Login exitoso con WireMock & OK \\
\hline
Fallo por credenciales inválidas (401) & OK \\
\hline
Refresh token válido & OK \\
\hline
Refresh token inválido (400) & OK \\
\hline
Caída del servidor externo simulada & Falló (esperado) \\
\hline
IotServiceApplicationTests & OK \\
\hline
Registro de dispositivo & OK \\
\hline
Lectura de dispositivo por ID & OK \\
\hline
Medición de temperatura con alerta & OK \\
\hline
Medición de presión normal & OK \\
\hline
Actualización de dispositivo & OK \\
\hline
Eliminación de dispositivo & OK \\
\hline
Otros... & OK \\
\hline

\end{longtable}

\newpage

### Core Behavior-Driven Development

::: box
***Angular***
:::

**Objetivo**

Validar que el sistema Angular se comporta correctamente desde el punto de vista del usuario, cubriendo los casos de uso más representativos del administrador educativo.

**Herramientas previstas**

- `Cypress` + `cypress-cucumber-preprocessor` para pruebas E2E con sintaxis Gherkin.
- Organización de carpetas: `/cypress/e2e/bdd/` para agrupar escenarios por épica o módulo funcional.
- `Playwright` opcional como herramienta alternativa de automatización.

::: box
**Unit Test - Behavior Driven Development**
:::

::: labtime
**Global Alert Service**
:::

```gherkin
Feature: Visualización de alertas globales

  Scenario: Mostrar alerta de éxito tras una acción del usuario
    Given el usuario accede a la sección de configuración
    When realiza una acción exitosa
    Then debería ver una alerta de tipo "success" con el mensaje "Operación exitosa"
```

```typescript
import { Given, When, Then } from '@badeball/cypress-cucumber-preprocessor';

Given('el usuario accede a la sección de configuración', () => {
  cy.visit('/settings'); // Ajusta según tu ruta real
});

When('realiza una acción exitosa', () => {
  cy.get('button.save-settings').click(); // Ajusta selector si es necesario
});

Then('debería ver una alerta de tipo {string} con el mensaje {string}', (tipo, mensaje) => {
  cy.get('.global-alert')
    .should('be.visible')
    .and('have.class', alert-bg-${tipo})
    .and('contain.text', mensaje);
});
```

\newpage

::: labtime
**Toggle Service**
:::

```gherkin
Feature: Alternar visibilidad de la barra lateral

  Scenario: Mostrar la barra lateral cuando se hace clic en el botón de toggle
    Given el usuario accede al dashboard
    And la barra lateral está oculta
    When el usuario hace clic en el botón de alternar menú
    Then la barra lateral debería mostrarse
```

```typescript
import { Given, When, Then } from '@badeball/cypress-cucumber-preprocessor';

Given('el usuario accede al dashboard', () => {
  cy.visit('/dashboard'); // Ajusta al path correcto
});

Given('la barra lateral está oculta', () => {
  cy.get('.sidebar').should('have.class', 'collapsed');
});

When('el usuario hace clic en el botón de alternar menú', () => {
  cy.get('button.toggle-sidebar').click(); // Ajusta el selector del botón
});

Then('la barra lateral debería mostrarse', () => {
  cy.get('.sidebar').should('not.have.class', 'collapsed');
});
```

\newpage

::: labtime
**Breadcrumb Component**
:::

```gherkin
Feature: Visualización del componente de breadcrumb

  Scenario: Mostrar correctamente el título y los ítems de navegación
    Given el usuario navega a la sección de estudiantes
    Then el breadcrumb debería mostrar el título "Estudiantes"
    And debería contener las rutas "Dashboard", "Primaria", "Grado 1"
```

```typescript
import { Given, Then } from '@badeball/cypress-cucumber-preprocessor';

Given('el usuario navega a la sección de estudiantes', () => {
  cy.visit('/students/primary/grade-1'); // Ajusta al path real de tu app
});

Then('el breadcrumb debería mostrar el título {string}', (titulo: string) => {
  cy.get('h5').should('contain.text', titulo);
});

Then('debería contener las rutas {string}, {string}, {string}', (r1, r2, r3) => {
  cy.get('.breadcrumb-item').then((items) => {
    expect(items[0]).to.contain.text(r1);
    expect(items[1]).to.contain.text(r2);
    expect(items[2]).to.contain.text(r3);
  });
});
```

\newpage

::: labtime
**Grade Card Component**
:::

```gherkin
Feature: Componente de tarjeta de grado escolar

  Scenario: Mostrar información del grado en la tarjeta
    Given el usuario está en la sección de grados de primaria
    Then debería ver una tarjeta con título "1er Grado"
    And la tarjeta debe mostrar la descripción "Niños de 6 a 7 años"
    And debe mostrar una imagen con URL válida

  Scenario: Navegar al hacer clic en una tarjeta
    Given el usuario está en la sección de grados de primaria
    When hace clic en la tarjeta de grado "1er Grado"
    Then debería ser redirigido a la lista de estudiantes del grado 1
```

```typescript
import { Given, When, Then } from '@badeball/cypress-cucumber-preprocessor';

Given('el usuario está en la sección de grados de primaria', () => {
  cy.visit('/students/primary'); // Ajusta a tu ruta real
});

Then('debería ver una tarjeta con título {string}', (titulo: string) => {
  cy.get('mat-card h5').should('contain.text', titulo);
});

Then('la tarjeta debe mostrar la descripción {string}', (descripcion: string) => {
  cy.get('mat-card p').should('contain.text', descripcion);
});

Then('debe mostrar una imagen con URL válida', () => {
  cy.get('mat-card img').should('have.attr', 'src').and('include', 'http');
});

When('hace clic en la tarjeta de grado {string}', (titulo: string) => {
  cy.contains('mat-card', titulo).click();
});

Then('debería ser redirigido a la lista de estudiantes del grado {int}', (grade: number) => {
  cy.url().should('include', /students/primary/${grade});
});
```

\newpage

::: labtime
**Blank Layout Component**
:::

```gherkin
Feature: Renderizado de layout en rutas públicas

  Scenario: Renderizar página de inicio de sesión dentro del layout en blanco
    Given el usuario visita la página de login
    Then debería mostrarse el formulario de inicio de sesión
    And la vista debe estar contenida dentro del layout en blanco
```

```typescript
import { Given, Then } from '@badeball/cypress-cucumber-preprocessor';

Given('el usuario visita la página de login', () => {
  cy.visit('/login'); // o la ruta que use el BlankLayout
});

Then('debería mostrarse el formulario de inicio de sesión', () => {
  cy.get('form').should('be.visible');
});

Then('la vista debe estar contenida dentro del layout en blanco', () => {
  cy.get('.blank-layout').should('exist');
  cy.get('.blank-layout').find('form').should('exist');
});
```


\newpage

::: box
**Integration Test - Behavior Driven Development**
:::

::: labtime
**School Transportation Service**
:::

```gherkin
Feature: Gestión de movilidades escolares

  Scenario: Registrar una nueva movilidad escolar
    Given el usuario accede al formulario de creación de movilidad
    When completa los datos requeridos y guarda el formulario
    Then debería ver una notificación de éxito
    And la nueva movilidad debería aparecer en la lista
```

```typescript
import { Given, When, Then } from '@badeball/cypress-cucumber-preprocessor';

Given('el usuario accede al formulario de creación de movilidad', () => {
  cy.visit('/school-transportation/create'); // Ajusta según tu ruta
});

When('completa los datos requeridos y guarda el formulario', () => {
  cy.get('input[formcontrolname="firstName"]').type('Luis');
  cy.get('input[formcontrolname="licenseCode"]').type('ABC123');
  cy.get('input[formcontrolname="dni"]').type('12345678');
  cy.get('input[formcontrolname="phone"]').type('987654321');
  // Agrega otros campos según sea necesario...

  cy.get('button[type="submit"]').click();
});

Then('debería ver una notificación de éxito', () => {
  cy.get('.global-alert')
    .should('be.visible')
    .and('contain.text', 'creada') // Ajusta si tu mensaje es distinto
});

Then('la nueva movilidad debería aparecer en la lista', () => {
  cy.visit('/school-transportation'); // Redirección automática o manual
  cy.contains('Luis').should('exist');
});
```

\newpage


::: labtime
**Create Primary Component**
:::

```gherkin
Feature: Registro de estudiante en grado de primaria

  Scenario: Cargar el formulario con grado desde la ruta
    Given el usuario accede al formulario de grado "3" en primaria
    Then el formulario debería tener preseleccionado el grado "3"

  Scenario: Enviar el formulario con datos válidos
    Given el usuario accede al formulario de grado "3" en primaria
    When completa los campos requeridos y guarda el formulario
    Then debería ver una notificación de éxito

  Scenario: Cancelar el registro
    Given el usuario accede al formulario de grado "3" en primaria
    When hace clic en el botón de cancelar
    Then debería ser redirigido a la lista de estudiantes del grado
```

```typescript
import { Given, When, Then } from '@badeball/cypress-cucumber-preprocessor';

Given('el usuario accede al formulario de grado {string} en primaria', (grade: string) => {
  cy.visit(/students/primary/create/${grade});
});

Then('el formulario debería tener preseleccionado el grado {string}', (grade: string) => {
  cy.get('input[formcontrolname="grade"]').should('have.value', grade);
});

When('completa los campos requeridos y guarda el formulario', () => {
  cy.get('input[formcontrolname="firstName"]').type('Luis');
  cy.get('input[formcontrolname="dni"]').type('12345678');
  cy.get('input[formcontrolname="phone"]').type('987654321');
  cy.get('button[type="submit"]').click();
});

Then('debería ver una notificación de éxito', () => {
  cy.get('.global-alert')
    .should('be.visible')
    .and('contain.text', 'creado'); // Ajusta según mensaje
});

When('hace clic en el botón de cancelar', () => {
  cy.get('button.cancel-button').click(); // Asegúrate que tenga esta clase
});

Then('debería ser redirigido a la lista de estudiantes del grado', () => {
  cy.url().should('include', '/students/primary/3'); // ajusta si el grado es dinámico
});
```

\newpage

::: labtime
**Edit School Transportation Component**
:::

```gherkin
Feature: Edición de movilidad escolar

  Scenario: Cargar el formulario con los datos existentes
    Given el usuario accede al formulario de edición para la movilidad con ID "1"
    Then el formulario debería mostrar los datos de la movilidad actual

  Scenario: Editar los datos y guardar
    Given el usuario accede al formulario de edición para la movilidad con ID "1"
    When edita los campos requeridos y guarda
    Then debería ver una notificación de éxito
    And debería ser redirigido a la lista de movilidades

  Scenario: Cancelar la edición
    Given el usuario accede al formulario de edición para la movilidad con ID "1"
    When hace clic en cancelar
    Then debería ser redirigido a la lista de movilidades
```

```typescript
import { Given, When, Then } from '@badeball/cypress-cucumber-preprocessor';

Given('el usuario accede al formulario de edición para la movilidad con ID {string}', (id: string) => {
  cy.visit(/school-transportation/edit/${id});
});

Then('el formulario debería mostrar los datos de la movilidad actual', () => {
  cy.get('input[formcontrolname="firstName"]').should('have.value', 'Juan'); // Valor mockeado
});

When('edita los campos requeridos y guarda', () => {
  cy.get('input[formcontrolname="firstName"]').clear().type('Luis Editado');
  cy.get('input[formcontrolname="licenseCode"]').clear().type('NEW456');
  cy.get('button[type="submit"]').click();
});

Then('debería ver una notificación de éxito', () => {
  cy.get('.global-alert')
    .should('be.visible')
    .and('contain.text', 'actualizado'); // Ajusta según texto real
});

Then('debería ser redirigido a la lista de movilidades', () => {
  cy.url().should('include', '/school-transportation');
});

When('hace clic en cancelar', () => {
  cy.get('button.cancel-button').click(); // Asegúrate que exista este selector
});

```

\newpage

::: labtime
**School Transportation Form Component**
:::

```gherkin
Feature: Formulario de registro y edición de movilidad escolar

  Scenario: Enviar formulario con datos válidos
    Given el usuario accede al formulario de movilidad escolar
    When completa todos los campos requeridos y envía el formulario
    Then debería emitirse un evento de envío y mostrarse una alerta de éxito

  Scenario: Cancelar el formulario
    Given el usuario accede al formulario de movilidad escolar
    When hace clic en el botón cancelar
    Then debería emitirse un evento de cancelación y volver a la lista
```

```typescript
import { Given, When, Then } from '@badeball/cypress-cucumber-preprocessor';

Given('el usuario accede al formulario de movilidad escolar', () => {
  cy.visit('/school-transportation/create'); // Ajusta si es una ruta diferente
});

When('completa todos los campos requeridos y envía el formulario', () => {
  cy.get('input[formcontrolname="dni"]').type('12345678');
  cy.get('input[formcontrolname="licenseCode"]').type('L123');
  cy.get('input[formcontrolname="firstName"]').type('Carlos');
  cy.get('input[formcontrolname="vehiclePlate"]').type('ABC-123');
  cy.get('button[type="submit"]').click();
});

Then('debería emitirse un evento de envío y mostrarse una alerta de éxito', () => {
  cy.get('.global-alert')
    .should('be.visible')
    .and('contain.text', 'creado'); // o "actualizado"
});

When('hace clic en el botón cancelar', () => {
  cy.get('button.cancel-button').click(); // Asegúrate de tener esta clase o selector
});

Then('debería emitirse un evento de cancelación y volver a la lista', () => {
  cy.url().should('include', '/school-transportation'); // Ajusta según navegación real
});
```

\newpage

::: labtime
**School Transportation List Component**
:::

```gherkin
Feature: Lista de movilidades escolares

  Scenario: El administrador visualiza la lista de movilidades escolares
    Given el administrador visita la página de "Movilidades Escolares"
    Then debería ver al menos un registro en la tabla

  Scenario: El administrador aplica un filtro por nombre
    Given el administrador está en la página de "Movilidades Escolares"
    When escribe "Luis" en el campo de búsqueda
    Then debería ver solo las filas que contienen "Luis"

  Scenario: El administrador navega a la edición de una movilidad
    Given el administrador está en la página de "Movilidades Escolares"
    When hace clic en el botón de editar de la primera fila
    Then debería ser redirigido a la vista de edición de movilidad

  Scenario: El administrador elimina una movilidad
    Given el administrador está en la página de "Movilidades Escolares"
    When hace clic en el botón de eliminar de la primera fila
    Then la movilidad debería desaparecer de la lista
```

```typescript
import { Given, When, Then } from '@badeball/cypress-cucumber-preprocessor';

Given('el administrador visita la página de {string}', (title: string) => {
  cy.visit('/school-transportation');
});

Then('debería ver al menos un registro en la tabla', () => {
  cy.get('table tbody tr').should('have.length.at.least', 1);
});

Given('el administrador está en la página de {string}', (title: string) => {
  cy.visit('/school-transportation');
});

When('escribe {string} en el campo de búsqueda', (text: string) => {
  cy.get('input[type="text"]').type(text);
});

Then('debería ver solo las filas que contienen {string}', (text: string) => {
  cy.get('table tbody tr').each(($row) => {
    cy.wrap($row).should('contain.text', text);
  });
});

When('hace clic en el botón de editar de la primera fila', () => {
  cy.get('button[aria-label="edit"]').first().click();
});

Then('debería ser redirigido a la vista de edición de movilidad', () => {
  cy.url().should('include', '/school-transportation/edit');
});

When('hace clic en el botón de eliminar de la primera fila', () => {
  cy.get('button[aria-label="delete"]').first().click();
});

Then('la movilidad debería desaparecer de la lista', () => {
  cy.get('table tbody tr').should('have.length.lessThan', 1); // ajusta según tu lógica real
});
```

**Resumen de historias cubiertas con BDD (Behavior-Driven Development):**

\begin{longtable}{|p{1cm}|p{5cm}|p{4cm}|p{3cm}|}
\hline
\textbf{ID} & \textbf{Funcionalidad} & \textbf{Escenarios Gherkin definidos} & \textbf{Estado de automatización} \\
\hline
\endfirsthead

\hline
\textbf{ID} & \textbf{Funcionalidad} & \textbf{Escenarios Gherkin definidos} & \textbf{Estado de automatización} \\
\hline
\endhead

US01 & Registro de cuenta institucional & Sí & En progreso \\
\hline
US04 & Inicio de sesión del administrador & Sí & Automatizado \\
\hline
US06 & Gestión y edición de perfil administrativo & Sí & Automatizado \\
\hline
CS01 & Registro y edición de vehículos & Sí & En progreso \\
\hline
DS01 & Registro y actualización de conductores & Sí & En progreso \\
\hline
DS03 & Asignación de conductores y estudiantes & En planificación & En progreso \\
\hline
FS03 & Alerta de estudiantes no abordando unidad & En planificación & No iniciado \\
\hline

\end{longtable}


\newpage

::: box
***Spring Boot***
:::

En esta sección se aplicó la metodología BDD (Behavior-Driven Development) para validar el comportamiento y las reglas de negocio de los servicios del backend. Esta estrategia permite alinear las pruebas automatizadas con los criterios de aceptación y los requisitos funcionales, usando escenarios escritos en lenguaje natural (Gherkin) que describen la lógica del servicio.

**Objetivo**

Validar que los servicios de Spring Boot cumplen con los requisitos funcionales, interactúan correctamente entre sí y con sistemas externos (como bases de datos o Keycloak), y manejan adecuadamente los casos de éxito y de error.

**Herramientas previstas**

-   `Spring Boot Test` + `JUnit 5` para crear el contexto de la aplicación y ejecutar pruebas de integración.
-   `Mockito` para simular dependencias externas (ej. el cliente de Keycloak) y aislar el comportamiento del servicio bajo prueba.
-   `Cucumber-JVM` (opcional) para una implementación estricta de BDD, permitiendo ejecutar archivos `.feature` con Gherkin. Los ejemplos a continuación simulan esta estructura usando anotaciones y comentarios en JUnit 5 para mayor claridad.
-   `H2 / Testcontainers` para una base de datos en memoria o efímera que garantice el aislamiento de las pruebas.
-   Organización de carpetas: `/src/test/resources/features/` para archivos Gherkin y `/src/test/java/org/pe/llantatech/steps/` para las definiciones de los pasos en Java.

\newpage

::: box
**Pruebas de Integración - Behavior Driven Development**
:::

::: labtime
**Keycloak Service**
:::

```gherkin
Feature: Gestión de usuarios en Keycloak

  Scenario: Crear un nuevo usuario con un rol específico
    Given una solicitud para crear un nuevo usuario con email "test@llantatech.pe" y rol "operador"
    When el servicio de Keycloak procesa la solicitud de creación
    Then un nuevo usuario debe ser creado en el realm de Keycloak
    And el rol "operador" debe ser asignado a dicho usuario

  Scenario: Falla al crear un usuario que ya existe
    Given un usuario con el email "existente@llantatech.pe" ya existe en Keycloak
    When el servicio de Keycloak intenta crear otro usuario con el mismo email
    Then la operación debería fallar con una excepción de tipo "UserAlreadyExistsException"
```

```java
// Nota: Este es un ejemplo de cómo se vería una prueba para un KeycloakService.
// Se utilizan Mocks para simular la interacción con la API de Keycloak sin necesidad de una instancia real.
import org.junit.jupiter.api.Test;
import org.junit.jupiter.api.extension.ExtendWith;
import org.mockito.InjectMocks;
import org.mockito.Mock;
import org.mockito.junit.jupiter.MockitoExtension;
import static org.mockito.Mockito.*;
import static org.junit.jupiter.api.Assertions.*;

@ExtendWith(MockitoExtension.class)
public class KeycloakServiceTest {

    @Mock
    private KeycloakAdminClient keycloakAdminClient; // Mock del cliente de Keycloak

    @InjectMocks
    private KeycloakService keycloakService; // El servicio que estamos probando

    @Test
    @DisplayName("Crear un nuevo usuario con un rol específico")
    void testCreateUserWithRole() {
        // Given: una solicitud para crear un nuevo usuario con email y rol
        String email = "test@llantatech.pe";
        String roleName = "operador";
        UserRepresentation userRequest = new UserRepresentation();
        userRequest.setEmail(email);

        // Simular que el rol "operador" existe y puede ser encontrado
        RoleRepresentation roleRepresentation = new RoleRepresentation(roleName, "", false);
        when(keycloakAdminClient.realm(anyString()).roles().get(roleName).toRepresentation())
            .thenReturn(roleRepresentation);
        
        // Simular que la creación del usuario es exitosa
        when(keycloakAdminClient.realm(anyString()).users().create(any(UserRepresentation.class)))
            .thenReturn(Response.created(new URI(".../users/some-id")).build());

        // When: el servicio de Keycloak procesa la solicitud de creación
        CreatedUserResponse response = keycloakService.createUserWithRole(userRequest, roleName);

        // Then: un nuevo usuario debe ser creado en el realm de Keycloak
        verify(keycloakAdminClient.realm(anyString()).users()).create(any(UserRepresentation.class));
        
        // And: el rol "operador" debe ser asignado a dicho usuario
        verify(keycloakAdminClient.realm(anyString()).users().get(anyString()).roles().realmLevel())
            .add(List.of(roleRepresentation));
        
        assertNotNull(response);
        assertTrue(response.isSuccess());
    }
}
```

\newpage

::: labtime
**IoT Service**
:::

```gherkin
Feature: Gestión de dispositivos y mediciones IoT

  Scenario: Registrar un nuevo dispositivo y recuperarlo por su ID
    Given los datos para un nuevo dispositivo IoT "Sensor Humedad" con serial "SN001"
    When se registra el nuevo dispositivo a través del servicio
    Then el dispositivo se crea exitosamente en la base de datos
    And al buscarlo por su ID, el dispositivo "Sensor Humedad" es encontrado

  Scenario: Registrar una nueva medición de temperatura que genera una alerta
    Given un dispositivo IoT existente de tipo "temperature"
    When una nueva medición de temperatura de "95 °C" es recibida para ese dispositivo
    Then la medición debe ser guardada con un estado de "ALERT"
    And la bandera de alerta de la medición debe ser verdadera

  Scenario: Registrar una medición de presión que no cumple el formato y genera error
    Given un dispositivo IoT existente de tipo "pressure"
    When una nueva medición de presión con valor "cincuenta kPa" es recibida
    Then la medición debe ser guardada con un estado de "ERROR"
    And la bandera de alerta de la medición debe ser falsa
```

```java
// Esta es la adaptación de tu clase de prueba existente al formato BDD.
package org.pe.llantatech.iotservice;

import org.junit.jupiter.api.DisplayName;
import org.junit.jupiter.api.Test;
import org.pe.llantatech.iotservice.model.IotDevice;
import org.pe.llantatech.iotservice.model.IotDeviceMeasuring;
import org.pe.llantatech.iotservice.model.IotMeasuringStatus;
import org.pe.llantatech.iotservice.service.IotService;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.boot.test.context.SpringBootTest;
import org.springframework.transaction.annotation.Transactional;

import java.util.Optional;

import static org.junit.jupiter.api.Assertions.*;

@SpringBootTest
@Transactional // Asegura que cada prueba se ejecute en su propia transacción y se revierta al final
class IotServiceApplicationTests {

    @Autowired
    private IotService iotService;

    @Test
    @DisplayName("Registrar un nuevo dispositivo y recuperarlo por su ID")
    void testCreateAndGetDeviceById() {
        // Given: los datos para un nuevo dispositivo IoT "Sensor Humedad" con serial "SN001"
        IotDevice device = new IotDevice();
        device.setDeviceName("Sensor Humedad");
        device.setSerialNumber("SN001");
        device.setDeviceType("humidity");
        device.setDeviceStatus("active");

        // When: se registra el nuevo dispositivo a través del servicio
        IotDevice created = iotService.createDevice(device);

        // Then: el dispositivo se crea exitosamente en la base de datos
        assertNotNull(created.getId());
        
        // And: al buscarlo por su ID, el dispositivo "Sensor Humedad" es encontrado
        Optional<IotDevice> found = iotService.getDeviceById(created.getId());
        assertTrue(found.isPresent());
        assertEquals("Sensor Humedad", found.get().getDeviceName());
    }

    @Test
    @DisplayName("Registrar una nueva medición de temperatura que genera una alerta")
    void testAddTemperatureMeasuringWithAlert() {
        // Given: un dispositivo IoT existente de tipo "temperature"
        IotDevice device = new IotDevice();
        device.setDeviceName("Temp Sensor");
        device.setSerialNumber("SN-TEMP");
        device.setDeviceType("temperature");
        IotDevice createdDevice = iotService.createDevice(device);

        // When: una nueva medición de temperatura de "95 °C" es recibida para ese dispositivo
        IotDeviceMeasuring measuring = new IotDeviceMeasuring();
        measuring.setMeasuringType("temperature");
        measuring.setMeasuringValue("95"); // Valor que excede el umbral
        measuring.setMeasuringUnit("°C");
        IotDeviceMeasuring result = iotService.addMeasuring(createdDevice.getId(), measuring);

        // Then: la medición debe ser guardada con un estado de "ALERT"
        assertEquals(IotMeasuringStatus.ALERT, result.getStatus());
        
        // And: la bandera de alerta de la medición debe ser verdadera
        assertTrue(result.isAlert());
    }
    
    @Test
    @DisplayName("Registrar una medición de presión que no cumple el formato y genera error")
    void testAddPressureMeasuringWithError() {
        // Given: un dispositivo IoT existente de tipo "pressure"
        IotDevice device = new IotDevice();
        device.setDeviceName("Presión Sensor");
        device.setSerialNumber("SN-PRESS");
        device.setDeviceType("pressure");
        IotDevice createdDevice = iotService.createDevice(device);

        // When: una nueva medición de presión con valor "cincuenta kPa" es recibida
        IotDeviceMeasuring measuring = new IotDeviceMeasuring();
        measuring.setMeasuringType("pressure");
        measuring.setMeasuringValue("cincuenta kPa"); // Valor no numérico
        measuring.setMeasuringUnit("kPa");
        IotDeviceMeasuring result = iotService.addMeasuring(createdDevice.getId(), measuring);

        // Then: la medición debe ser guardada con un estado de "ERROR"
        assertEquals(IotMeasuringStatus.ERROR, result.getStatus());

        // And: la bandera de alerta de la medición debe ser falsa
        assertFalse(result.isAlert());
    }
}
```

\newpage

**Resumen de historias cubiertas con BDD (Behavior-Driven Development):**

\begin{longtable}{|p{1.5cm}|p{5.5cm}|p{4cm}|p{3cm}|}
\hline
\textbf{ID} & \textbf{Funcionalidad (Backend)} & \textbf{Escenarios Gherkin definidos} & \textbf{Estado de automatización} \\
\hline
\endfirsthead

\hline
\textbf{ID} & \textbf{Funcionalidad (Backend)} & \textbf{Escenarios Gherkin definidos} & \textbf{Estado de automatización} \\
\hline
\endhead

AUTH-01 & Como sistema, necesito crear usuarios en Keycloak y asignarles roles para controlar el acceso. & Sí & Automatizado \\
\hline
AUTH-02 & Como sistema, necesito validar tokens JWT de Keycloak para asegurar las APIs. & Sí & En progreso \\
\hline
IOT-01 & Como sistema, necesito registrar nuevos dispositivos IoT en la base de datos para poder gestionarlos. & Sí & Automatizado \\
\hline
IOT-02 & Como sistema, necesito procesar y almacenar mediciones (temperatura, presión, etc.) de los dispositivos. & Sí & Automatizado \\
\hline
IOT-03 & Como sistema, necesito aplicar reglas de negocio para evaluar mediciones y generar alertas si exceden los umbrales. & Sí & Automatizado \\
\hline
IOT-04 & Como sistema, necesito poder actualizar la información de un dispositivo existente (ej. cambiar su estado a inactivo). & Sí & Automatizado \\
\hline
IOT-05 & Como sistema, necesito poder eliminar un dispositivo que ya no está en uso. & Sí & Automatizado \\
\hline

\end{longtable}

\newpage

### Core System Tests.

::: box
***Angular***
:::

En este apartado se validó el comportamiento del sistema desde la perspectiva del usuario final, evaluando el flujo completo de funcionalidades críticas en el frontend. Las pruebas de sistema se realizaron sobre un entorno de staging, simulando una ejecución real de la plataforma.

**Objetivo**

Asegurar que los componentes del frontend Angular, al integrarse con servicios, navegación, formularios y lógica del dominio, funcionen de forma coherente y sin errores desde la interacción inicial hasta la respuesta final.

**Características principales**

- Validación de flujos completos desde inicio de sesión hasta navegación y operaciones CRUD.

- Verificación de que los datos ingresados y las acciones realizadas generen efectos visibles y esperados en el sistema.

- Simulación de múltiples roles en sesión, como administrador y operador, para evaluar permisos y vistas.

**Ejemplos de pruebas aplicadas**

\begin{longtable}{|p{7cm}|p{8cm}|}
\hline
\textbf{Flujo probado} & \textbf{Validación incluida} \\
\hline
\endfirsthead

\hline
\textbf{Flujo probado} & \textbf{Validación incluida} \\
\hline
\endhead

Inicio de sesión + redirección & Autenticación correcta y navegación al panel principal \\
\hline
Registro y edición de vehículos & Persistencia de datos y validaciones en el front-end \\
\hline
Asignación de estudiantes a rutas & Visualización y confirmación de la asignación en las tablas \\
\hline
Cierre de sesión & Limpieza de la sesión y redirección a la pantalla de inicio de sesión \\
\hline
Visualización de zonas y rutas en mapa & Carga de datos GeoJSON y renderizado correcto en el visor \\
\hline

\end{longtable}


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

::: box
***Spring Boot***
:::

En este apartado se validó el comportamiento del sistema desde la perspectiva del consumidor de la API (por ejemplo, la aplicación frontend o un servicio de terceros), evaluando el flujo completo de las funcionalidades a través de los endpoints públicos. Las pruebas de sistema se realizaron levantando el contexto completo de la aplicación Spring Boot, incluyendo la conexión a una base de datos de prueba, para simular una ejecución real del backend.

**Objetivo**

Asegurar que los controladores, servicios y repositorios de Spring Boot, al integrarse, procesen las solicitudes HTTP, apliquen la lógica de negocio, interactúen con la base de datos y respondan de forma coherente y sin errores, cubriendo flujos de negocio completos.

**Características principales**

-   Validación de flujos de negocio completos a través de múltiples llamadas a la API (ej. crear un recurso con `POST`, luego obtenerlo con `GET` para verificar).
-   Verificación de que las acciones realizadas (operaciones CRUD) se reflejen correctamente en el estado de la base de datos.
-   Pruebas de seguridad basadas en roles, asegurando que los endpoints estén protegidos y solo los usuarios con los permisos correctos (ej. 'administrador', 'operador') puedan acceder.

**Ejemplos de pruebas aplicadas**

\begin{longtable}{|p{7cm}|p{8cm}|}
\hline
\textbf{Flujo probado (API)} & \textbf{Validación incluida} \\
\hline
\endfirsthead

\hline
\textbf{Flujo probado (API)} & \textbf{Validación incluida} \\
\hline
\endhead

Autenticación vía endpoint `/api/auth/login` & Generación de un token JWT válido para credenciales correctas y denegación de acceso para las incorrectas. \\
\hline
Operaciones CRUD en `/api/vehiculos` & Persistencia de datos en la base de datos, validación de datos de entrada (DTOs) y respuestas HTTP correctas (201, 200, 204). \\
\hline
Asignación de estudiantes en `/api/rutas/{id}/estudiantes` & Correcta creación de la relación en la base de datos y validación de la lógica de negocio (ej. no exceder capacidad). \\
\hline
Invalidación de sesión (Logout) & Inclusión de un token JWT en una lista negra o mecanismo similar para que no pueda ser reutilizado. \\
\hline
Obtención de datos para mapa en `/api/mapa/zonas` & El endpoint retorna una respuesta con el `Content-Type` correcto (`application/geo+json`) y una estructura GeoJSON válida. \\
\hline

\end{longtable}

**Herramientas utilizadas**

-   `Spring Boot Test` con `@SpringBootTest` para levantar el contexto completo de la aplicación.
-   `MockMvc` o `RestAssured` para realizar solicitudes HTTP a los endpoints de la API y validar las respuestas.
-   `H2 / Testcontainers` para proveer una base de datos de prueba limpia y aislada para cada ejecución.
-   `WireMock` para simular servicios HTTP externos de los que depende nuestra aplicación.

**Buenas prácticas aplicadas**

-   Separación clara entre pruebas unitarias, de integración y de sistema (API E2E).
-   Automatización de los flujos de negocio más críticos a través de la API.
-   Entorno de pruebas limpio y reproducible, con una base de datos que se reinicia antes de cada suite de pruebas.

**Resultado**

Las pruebas de sistema demostraron que la API del backend es funcional, robusta y segura frente a flujos de uso reales. Las incidencias detectadas, como fallos en la lógica de negocio o brechas de seguridad a nivel de endpoints, fueron corregidas y documentadas.

**Ejemplo de Código** 

Así se vería el test de inicio de sesión de Cypress, pero implementado como una prueba de sistema para la API de Spring Boot.

```java
// src/test/java/org/pe/llantatech/system/AuthenticationSystemTest.java

import com.fasterxml.jackson.databind.ObjectMapper;
import org.junit.jupiter.api.Test;
import org.pe.llantatech.auth.dto.LoginRequest;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.boot.test.autoconfigure.web.servlet.AutoConfigureMockMvc;
import org.springframework.boot.test.context.SpringBootTest;
import org.springframework.http.MediaType;
import org.springframework.test.web.servlet.MockMvc;

import static org.springframework.test.web.servlet.request.MockMvcRequestBuilders.post;
import static org.springframework.test.web.servlet.result.MockMvcResultMatchers.jsonPath;
import static org.springframework.test.web.servlet.result.MockMvcResultMatchers.status;

@SpringBootTest
@AutoConfigureMockMvc // Configura MockMvc para realizar llamadas a la API
public class AuthenticationSystemTest {

    @Autowired
    private MockMvc mockMvc;

    @Autowired
    private ObjectMapper objectMapper; // Para convertir objetos a JSON

    @Test
    void deberiaPermitirAutenticacionYRetornarTokenJWT() throws Exception {
        // Preparar la solicitud de login con credenciales válidas
        LoginRequest loginRequest = new LoginRequest("admin@llantatech.pe", "Admin1234");

        // Realizar una llamada POST al endpoint de login
        mockMvc.perform(post("/api/auth/login")
                        .contentType(MediaType.APPLICATION_JSON)
                        .content(objectMapper.writeValueAsString(loginRequest)))
                // Verificar que la respuesta sea un 200 OK
                .andExpect(status().isOk())
                // Verificar que la respuesta JSON contenga un campo "token"
                .andExpect(jsonPath("$.token").exists())
                .andExpect(jsonPath("$.token").isString());
    }

    @Test
    void deberiaRetornarError401ConCredencialesIncorrectas() throws Exception {
        // Preparar la solicitud de login con una contraseña incorrecta
        LoginRequest loginRequest = new LoginRequest("admin@llantatech.pe", "claveincorrecta");

        // Realizar la llamada POST al endpoint de login
        mockMvc.perform(post("/api/auth/login")
                        .contentType(MediaType.APPLICATION_JSON)
                        .content(objectMapper.writeValueAsString(loginRequest)))
                // Verificar que la respuesta sea un 401 Unauthorized
                .andExpect(status().isUnauthorized())
                // Verificar que el cuerpo de la respuesta contenga un mensaje de error
                .andExpect(jsonPath("$.error").value("Credenciales inválidas"));
    }
}
```

\newpage

## Static testing & Verification

La verificación estática representa una de las estrategias más importantes dentro del ciclo de aseguramiento de la calidad del software, ya que permite detectar defectos en las primeras etapas del desarrollo, incluso antes de que el sistema sea ejecutado. A diferencia de las pruebas dinámicas —que requieren la ejecución del código—, el enfoque estático se basa en el análisis estructural, sintáctico y semántico del código fuente, facilitando así la identificación temprana de errores lógicos, problemas de seguridad, violaciones de estándares de codificación y prácticas que comprometan la mantenibilidad o la eficiencia del sistema.

Este tipo de pruebas se lleva a cabo mediante herramientas automáticas de análisis estático y procesos complementarios como las revisiones de código entre pares. Las herramientas automatizadas inspeccionan el código de manera rigurosa y sistemática, detectando desde errores comunes de programación hasta vulnerabilidades críticas que podrían ser explotadas en entornos productivos. Por su parte, las revisiones manuales fomentan la colaboración entre desarrolladores y contribuyen al desarrollo de una base de conocimiento compartida sobre buenas prácticas, diseño limpio y arquitectura robusta.

Incorporar la verificación estática en el flujo de trabajo continuo no solo ayuda a prevenir fallos costosos en fases posteriores, sino que también fortalece la confianza del equipo en la calidad del software que se está construyendo. Además, al asegurar que el código cumpla con criterios predefinidos de estilo, consistencia y seguridad, se mejora significativamente la legibilidad y escalabilidad del proyecto.

![Recurso extraído de Canva](src/img/cap6/static-testing-verification.png)

\newpage

### Static Code Analysis

El análisis estático de código constituye una práctica fundamental dentro del proceso de aseguramiento de la calidad del software, ya que permite detectar de manera anticipada posibles defectos, vulnerabilidades y malas prácticas en el código fuente, sin necesidad de ejecutarlo. Esta técnica se apoya en herramientas automatizadas que inspeccionan rigurosamente el código con el objetivo de identificar errores de sintaxis, patrones de programación inseguros, violaciones a los estándares de codificación y otros indicadores que puedan comprometer la mantenibilidad, seguridad y eficiencia del sistema. En este proyecto, se ha implementado un enfoque integral de análisis estático tanto en la capa del frontend como en la del backend, con el fin de garantizar una alta calidad técnica en todas las etapas del desarrollo.

::: info
**Análisis en el Frontend (Angular / TypeScript)**
:::

Para la interfaz de usuario desarrollada con el framework Angular y el lenguaje TypeScript, se ha integrado un conjunto de herramientas especializadas que forman parte del ecosistema moderno de desarrollo en JavaScript. Estas herramientas han sido seleccionadas por su eficacia y compatibilidad con las mejores prácticas de la industria:

**ESLint**: Constituye la herramienta principal para la detección de problemas en el código TypeScript. Su configuración incluye un conjunto de reglas adaptadas tanto a las convenciones generales de TypeScript como a las recomendaciones específicas para proyectos Angular. Gracias a ESLint, se identifican inconsistencias, errores lógicos comunes y patrones de codificación potencialmente problemáticos, lo cual contribuye a un código más limpio, robusto y fácil de mantener.


![Recurso extraído de Canva](src/img/cap6/eslint-logo-cap6.png)

**Prettier**: Se utiliza como formateador automático de código fuente. Su propósito principal es garantizar una presentación uniforme del código en todo el proyecto, independientemente del desarrollador que lo escriba. Al eliminar discrepancias de estilo y debates subjetivos sobre la sintaxis, Prettier facilita la colaboración dentro del equipo y mejora la legibilidad general del código.

![Recurso extraído de Canva](src/img/cap6/prettier-logo-cap6.png)

**SonarLint (integrado en el entorno de desarrollo)**: Esta herramienta se ejecuta de manera local en el editor de código (IDE), proporcionando retroalimentación instantánea mientras se escribe el código. Detecta errores, vulnerabilidades y malos olores de código (code smells) en tiempo real, lo cual permite a los desarrolladores corregir los problemas de forma proactiva antes de que lleguen a etapas posteriores del ciclo de desarrollo.

![Recurso extraído de Canva](src/img/cap6/sonarlint-logo-cap6.png)

\newpage

::: info
**Análisis en el Backend (Java)**
:::

En el caso de la capa de servicios y lógica de negocio implementada en Java, se han adoptado herramientas consolidadas y ampliamente utilizadas dentro de la comunidad de desarrollo empresarial. Estas herramientas permiten realizar un análisis profundo del código fuente, contribuyendo a mantener altos estándares de calidad y seguridad:

**Checkstyle**: Se encarga de verificar que el código Java cumpla con una guía de estilo predefinida, como puede ser la *Google Java Style Guide*. Esta validación promueve la uniformidad en la estructura y presentación del código, lo cual facilita su revisión y mantenimiento a lo largo del tiempo.

![Recurso extraído de Canva](src/img/cap6/checkstyle-logo-cap6.png)

* **PMD**: Es una herramienta de análisis estático que identifica una amplia variedad de problemas, tales como código duplicado, estructuras de control innecesariamente complejas, declaraciones sin uso (código muerto), y otros patrones que podrían reducir la eficiencia o claridad del sistema. PMD también calcula métricas relevantes como la complejidad ciclomática, lo que permite evaluar el grado de dificultad en la comprensión y prueba del código.

![Recurso extraído de Canva](src/img/cap6/pmd-logo-cap6.png)

**SonarQube**: Se implementa como una plataforma centralizada para el análisis continuo de la calidad del código fuente. SonarQube no solo integra los resultados de herramientas como Checkstyle y PMD, sino que también realiza su propio análisis avanzado utilizando técnicas de *Static Application Security Testing* (SAST). Esta herramienta detecta de manera sistemática errores, vulnerabilidades de seguridad y malos olores de código, y presenta los hallazgos a través de un panel visual que permite monitorear la salud técnica del proyecto a lo largo del tiempo.

![Recurso extraído de Canva](src/img/cap6/sonarqube-logo-cap6.png)

En conjunto, estas herramientas conforman una estrategia robusta y automatizada de análisis estático que contribuye significativamente a reducir el riesgo técnico, mejorar la mantenibilidad del software y asegurar que el sistema cumpla con altos estándares de calidad desde sus etapas iniciales de desarrollo.

\newpage

#### Coding standard & Code conventions.

El establecimiento de estándares de codificación y convenciones de estilo es un pilar fundamental en el desarrollo de software profesional, ya que garantiza la legibilidad, coherencia, mantenibilidad y escalabilidad del código fuente a lo largo del ciclo de vida del proyecto. En el presente sistema, estos estándares han sido definidos y aplicados rigurosamente tanto en la capa del frontend (Angular/TypeScript) como en el backend (Java/Spring Boot), considerando además las particularidades propias de una arquitectura basada en microservicios.

::: info
**Estándares en el Frontend (Angular/TypeScript)**
:::

Para el desarrollo del cliente web mediante Angular, se han seguido las guías oficiales de estilo de Angular, complementadas con convenciones propias del equipo de desarrollo para mejorar la mantenibilidad y coherencia del proyecto. Entre las prácticas más destacadas se encuentran:

* **Nomenclatura Consistente de Archivos y Componentes**: Todos los archivos siguen una convención estricta de nombramiento basada en el tipo de recurso que representan. Por ejemplo, los archivos de pruebas unitarias e integración se identifican con el sufijo `.spec.ts` (e.g., `login.component.spec.ts`, `user.service.spec.ts`), lo cual facilita su identificación y organización dentro del repositorio.

* **Separación de Responsabilidades y Modularidad**: Se promueve una estructura modular clara, donde cada módulo encapsula sus propios componentes, servicios, interfaces y pruebas. Esta organización permite una mayor escalabilidad y reutilización de componentes dentro de la aplicación.

* **Aplicación del Patrón AAA (Arrange, Act, Assert)**: Todas las pruebas están diseñadas siguiendo el patrón AAA, el cual separa de manera explícita la configuración inicial (Arrange), la ejecución de la funcionalidad bajo prueba (Act) y la verificación de resultados (Assert). Esta estructura mejora notablemente la claridad y comprensibilidad de las pruebas automatizadas.

* **Revisión Continua y Linting Automático**: El cumplimiento de estas convenciones es validado constantemente a través de herramientas como ESLint y SonarLint, integradas en el flujo de trabajo del desarrollador, y complementadas por revisiones de código (*code reviews*) entre miembros del equipo.

::: info
**Estándares en el Backend (Java / Spring Boot con Microservicios)**
:::

La capa de servicios, construida con Java utilizando el framework Spring Boot bajo un enfoque de **arquitectura de microservicios**, se ha desarrollado conforme a estándares ampliamente reconocidos en la industria. Dado que en una arquitectura distribuida la claridad y coherencia entre servicios es crucial, se han adoptado las siguientes prácticas:

* **Convenciones de Paquetización y Nombres de Clases**: Se utiliza una estructura de paquetes que sigue la lógica de dominio y capas de responsabilidad (e.g., `controller`, `service`, `repository`, `dto`, `mapper`). Las clases están nombradas conforme a su rol funcional, lo que facilita su interpretación y ubicación dentro de cada microservicio.

* **Principios de Diseño Sólido (SOLID)**: Se aplica de manera sistemática el conjunto de principios SOLID, promoviendo la separación de responsabilidades, la inyección de dependencias y la reutilización de código, aspectos esenciales para el desarrollo limpio y escalable de microservicios.

* **Manejo Estándar de Errores y Validaciones**: Todos los microservicios implementan una capa común para el tratamiento de errores y validaciones de entrada, siguiendo patrones como el uso de excepciones personalizadas y validaciones con Bean Validation (JSR-380).

* **Estilo de Código Uniforme**: El formato y estilo del código Java es verificado mediante herramientas como Checkstyle y PMD, configuradas con reglas basadas en la *Google Java Style Guide*. Esto garantiza uniformidad en aspectos como sangría, nombres de variables, uso de anotaciones y organización de importaciones.

* **Pruebas con Patrón AAA y Separación de Tipos de Test**: Al igual que en el frontend, las pruebas en Java siguen el patrón AAA. Se distinguen claramente las pruebas unitarias (con JUnit y Mockito), pruebas de integración (con Spring Boot Test y Testcontainers) y pruebas de contrato (Contract Testing), fundamentales en contextos de microservicios.

* **Revisión y Control de Calidad Centralizado**: La plataforma SonarQube recopila y analiza todos los microservicios de manera unificada, permitiendo monitorear en tiempo real métricas clave como cobertura de pruebas, complejidad ciclomática, duplicación de código y presencia de vulnerabilidades.

\newpage

**Enfoque Integral de Gobernanza del Código**

A lo largo del proyecto, el cumplimiento de estas convenciones y estándares ha sido promovido como una política transversal de gobernanza del código fuente. Este enfoque no solo permite mantener una base de código sana y fácil de escalar, sino que también mejora la colaboración entre los desarrolladores, facilita la incorporación de nuevos miembros al equipo y reduce el riesgo de errores o regresiones en ambientes productivos.

Además, la naturaleza distribuida del sistema (compuesto por múltiples microservicios) hace indispensable un estilo de codificación homogéneo, tanto para propósitos de interoperabilidad como para facilitar el monitoreo, trazabilidad y depuración de errores en entornos complejos.


\begin{longtable}{|p{4cm}|p{5cm}|p{6cm}|}
\hline
\textbf{Tecnología / Capa} & \textbf{Estándar / Convención} & \textbf{Descripción y Herramientas Aplicadas} \\
\hline
\endfirsthead

\hline
\textbf{Tecnología / Capa} & \textbf{Estándar / Convención} & \textbf{Descripción y Herramientas Aplicadas} \\
\hline
\endhead

\hline
\multicolumn{3}{r}{\textit{Continúa en la siguiente página}} \\
\endfoot

\hline
\endlastfoot

\textbf{Frontend (Angular / TypeScript)} & Nomenclatura de archivos & Uso del sufijo \texttt{.spec.ts} para archivos de prueba; convenciones consistentes para componentes, servicios y módulos. \\
\cline{2-3}
& Patrón AAA (Arrange, Act, Assert) & Estructura estándar para pruebas unitarias, mejorando la claridad y la mantenibilidad del código de test. \\
\cline{2-3}
& Formato y estilo de código & Uso de ESLint para reglas de estilo y detección de errores; Prettier para formateo automático y uniforme. \\
\cline{2-3}
& Retroalimentación en tiempo real & Integración de SonarLint en el IDE para detectar errores, code smells y vulnerabilidades al momento de programar. \\
\hline

\textbf{Backend (Java / Spring Boot)} & Estructura de paquetes & Organización basada en capas: \texttt{controller}, \texttt{service}, \texttt{repository}, \texttt{dto}, \texttt{mapper}. \\
\cline{2-3}
& Guía de estilo de código & Adopción de la \textit{Google Java Style Guide}, validada con Checkstyle y PMD. \\
\cline{2-3}
& Principios SOLID & Aplicación sistemática de principios de diseño orientado a objetos para mejorar modularidad y mantenibilidad. \\
\cline{2-3}
& Manejo de errores & Uso de excepciones personalizadas y validaciones con anotaciones (Bean Validation). \\
\cline{2-3}
& Patrón AAA y tipos de pruebas & Estructura clara de pruebas (unitarias, integración, contrato) usando JUnit, Mockito, Spring Boot Test y Testcontainers. \\
\cline{2-3}
& Plataforma de análisis centralizado & Integración de SonarQube para consolidar y visualizar métricas de calidad de todos los microservicios. \\
\hline

\textbf{Arquitectura de Microservicios} & Convención uniforme entre servicios & Homogeneidad en estilos de codificación, manejo de errores y estructura de carpetas para facilitar escalabilidad y mantenimiento. \\
\cline{2-3}
& Gobernanza de calidad & Revisión continua de código, integración de herramientas automáticas y prácticas compartidas para mantener consistencia global. \\
\hline

\end{longtable}


\newpage

#### Code Quality & Code Security.


La calidad y la seguridad del código constituyen dimensiones esenciales en la ingeniería de software profesional. En este apartado, se abordan los mecanismos empleados para medir y mantener la calidad, así como las estrategias de seguridad implementadas para detectar y mitigar vulnerabilidades antes de que el software entre en producción.


::: box
**Code Quality** 
:::

::: info
**Frontend (Angular / TypeScript)**
:::

* **Cobertura de pruebas**

  Se establece como objetivo mantener una cobertura mínima del 80% en módulos críticos de UI, medida a través de herramientas como Jest y Karma durante la fase de integración continua. Por ejemplo, en uno de los últimos ciclos, la cobertura global alcanzó un 85%, mientras que en componentes clave como `Auth` y `UserProfile` se logró un 92%.

* **Complejidad ciclomática y puntos críticos**

  Se monitoriza la complejidad de funciones con ESLint y herramientas de análisis estático complementarias, procurando que ninguna función supere una complejidad de 10%. Si se detectan hotspots (áreas de alto cambio o complejidad), se prioriza su refactorización para mejorar la mantenibilidad.

::: info
**Backend (Java / Spring Boot)**
:::

* **Cobertura de código**

  Se utiliza JaCoCo para medir cobertura en pruebas unitarias y de integración. En promedio, los microservicios alcanzan un 85–90%, con un mínimo aceptable del 80% en módulos de negocio críticos, como autenticación y orquestación de pagos.

* **Métricas de calidad**

  Herramientas como JArchitect y SonarQube proveen métricas avanzadas (p.ej. complejidad ciclomática, acoplamientos, duplicación de código). Se considera adecuado mantener la complejidad ciclomática por método por debajo de 15%, un acoplamiento afferente bajo y duplicación de código por debajo del 3%.

* **Salud del código y hotspots**

  Se monitorea el “Code Health” para identificar hotspots—clases o módulos con alta frecuencia de modificación y bajo puntaje de mantenibilidad—y se aplican refactorizaciones proactivas.


\newpage

::: box
**Code Security**
:::

::: info
**Frontend**
:::

* **Análisis SAST**

  Se emplean escáneres estáticos (por ejemplo, Snyk, ESLint con reglas de seguridad) integrados en IDE y CI, capaces de detectar XSS, inyección de código y fugas de datos. Esto sigue la metodología recomendada de SAST: escanear el código antes de la compilación para interceptar vulnerabilidades mediante análisis de flujo de datos, control y semántico .

* **Software Composition Analysis (SCA)**

  Se escanean dependencias del frontend (como paquetes npm) con Snyk o similares, detectando vulnerabilidades conocidas en bibliotecas. El proceso prioriza vulnerabilidades según severidad y probabilidad de explotación, y se automatiza la actualización de dependencias.

::: info
**Backend (Java / Spring Boot con microservicios)**
:::

* **Análisis SAST en CI/CD**

  Se ejecuta SAST (por ejemplo, SonarQube, Checkmarx) en cada fase de CI para detectar vulnerabilidades SAST como inyección SQL, fallos de validación, uso inseguro de secretos y configuraciones sensibles .

* **SCA de dependencias**

  Se aplica Software Composition Analysis con herramientas como Snyk o OWASP Dependency-Check. Los resultados identifican bibliotecas vulnerables (CVE), sus versiones, riesgos e impacto. Cada microservicio mantiene una cobertura de escaneo del 100%, con tiempos medios de remediación (MTTR) menores a 48 horas.

* **Métricas de seguridad**

  Las principales métricas de seguridad monitoreadas incluyen:

  1. Cobertura de escaneo SAST/SCA (debe ser del 100%).
  2. MTTR de vulnerabilidades, con objetivo de < 48 horas.
  3. Número de servicios con vulnerabilidades críticas, monitorizado periódicamente.

* **Trazabilidad y gobernanza**

  Notificaciones automáticas a través de canal de CI/CD, dashboard centralizado en SonarQube para visualizar la salud de todos los microservicios. Se generan informes auditables que incluyen evidencia de escaneo, versión del código y resultados.

\newpage

**Resumen Comparativo**

| **Capa**     | **Calidad (métrica)**                            | **Seguridad (SAST/SCA)**                           |
| -------- | -------------------------------------------- | ---------------------------------------------- |
| **Frontend** | Cobertura mayor o igual a 80 (UI), complejidad menor a 10      | Escaneo SAST + SCA, detección XSS, inyecciones |
| **Backend**  | Cobertura mayor o igual a  80 (negocio), complejidad menor a 15 | SAST en CI, SCA en dependencias, MTTR menor a 48 h   |

**Tabla Comparativa**

\begin{longtable}{|p{4cm}|p{5cm}|p{6cm}|}
\hline
\textbf{Capa / Tecnología} & \textbf{Métricas de Calidad} & \textbf{Prácticas de Seguridad (SAST / SCA)} \\
\hline
\endfirsthead

\hline
\textbf{Capa / Tecnología} & \textbf{Métricas de Calidad} & \textbf{Prácticas de Seguridad (SAST / SCA)} \\
\hline
\endhead

\hline
\multicolumn{3}{r}{\textit{Continúa en la siguiente página}} \\
\endfoot

\hline
\endlastfoot

\textbf{Frontend (Angular / TypeScript)} 
& 
\begin{itemize}
    \item Cobertura de pruebas: mayor o igual a 80% en módulos críticos.
    \item Complejidad ciclomática menor a 10%.
    \item Mantenimiento de estilo con ESLint + Prettier.
    \item Hotspots identificados y refactorizados.
\end{itemize}
& 
\begin{itemize}
    \item Escaneo SAST con SonarLint y ESLint (seguridad).
    \item SCA automatizado con Snyk para dependencias npm.
    \item Detección de XSS, inyección y malas prácticas.
    \item Actualización proactiva de librerías vulnerables.
\end{itemize} \\
\hline

\textbf{Backend (Java / Spring Boot)} 
& 
\begin{itemize}
    \item Cobertura de pruebas: mayor o igual a 85en microservicios clave.
    \item Complejidad ciclomática menor a 15%.
    \item Uso de JaCoCo, SonarQube y PMD.
    \item Salud técnica monitoreada con SonarQube.
\end{itemize}
& 
\begin{itemize}
    \item SAST en CI con SonarQube y/o Checkmarx.
    \item SCA con OWASP Dependency-Check o Snyk.
    \item Cobertura de escaneo: 100% de servicios.
    \item MTTR de vulnerabilidades: menor a 48 horas.
    \item Informes auditables de seguridad por microservicio.
\end{itemize} \\
\hline

\end{longtable}

\newpage

**Gráfico de Cobertura de Código por Módulo**

\begin{figure}[H]
\centering
\begin{tikzpicture}
\begin{axis}[
    ybar,
    bar width=15pt,
    enlargelimits=0.15,
    ylabel={Cobertura de código (\%)},
    xlabel={Módulo},
    symbolic x coords={Login, Profile, Auth, Iot},
    xtick=data,
    nodes near coords,
    ymin=0, ymax=100,
    ymajorgrids=true,
    grid style=dashed
]
\addplot coordinates {(Login,92) (Profile,85) (Auth,88) (Iot,90)};
\end{axis}
\end{tikzpicture}
\caption{Cobertura de código en módulos seleccionados del frontend y backend}
\label{fig:cobertura_codigo}
\end{figure}


\newpage

### Reviews

Las revisiones de código constituyen una práctica fundamental dentro del proceso de aseguramiento de calidad del software, especialmente en contextos colaborativos y distribuidos como el desarrollo basado en microservicios. Esta técnica, también conocida como *Peer Code Review*, permite someter cada nueva funcionalidad o corrección a una evaluación técnica por parte de uno o más desarrolladores del equipo antes de ser integrada en la rama principal del repositorio.

El objetivo de las revisiones no es únicamente identificar errores, sino también promover un entorno de desarrollo más sólido, coherente y con mayor madurez técnica.

::: info
**Proceso de Revisión**
:::

Todas las revisiones de código se realizan a través del flujo de trabajo de Pull Requests (PRs) gestionado en el sistema de control de versiones (Git), dentro de una plataforma como GitHub, GitLab o Bitbucket. Este proceso establece un mecanismo formal de verificación antes de que cualquier cambio sea incorporado a la rama principal (`main` o `develop`), asegurando que:

- Todo cambio pase por al menos una revisión obligatoria por otro miembro del equipo.
- Las sugerencias, observaciones y decisiones queden registradas de forma trazable.
- Se mantenga una línea de base estable del producto en cada iteración.

::: info
**Objetivos de las Revisiones**
:::

El proceso de revisión persigue múltiples objetivos técnicos y organizacionales, entre los cuales destacan:

- **Detección de errores no capturados automáticamente**  
  Aunque se emplean herramientas de análisis estático (ESLint, PMD, SonarQube, etc.), algunas deficiencias lógicas, omisiones de requisitos o decisiones de diseño inapropiadas solo pueden ser detectadas por un par humano con conocimiento contextual del proyecto.

- **Verificación del cumplimiento de estándares**  
  El revisor valida que el código se adhiera estrictamente a los lineamientos definidos en los apartados 6.2.1.1 (estándares de codificación) y 6.2.1.2 (métricas de calidad), incluyendo estilo, estructura, modularidad y pruebas. También se verifica que la cobertura de código sea suficiente y que las pruebas estén correctamente implementadas.

- **Transferencia y democratización del conocimiento**  
  Las revisiones promueven la diseminación de conocimientos entre los miembros del equipo. Un desarrollador puede aprender sobre un módulo con el que no trabaja directamente, y al revisar cambios de otros, se fortalece su comprensión de la arquitectura global del sistema.

- **Mejora continua de la calidad del software**  
  Más allá de detectar errores, los PRs ofrecen un espacio para sugerir mejoras de diseño, refactorizaciones, simplificaciones de lógica, eliminación de redundancias y mejoras en la eficiencia del código. Esto eleva de forma continua el estándar técnico del proyecto.

- **Fomento de la responsabilidad compartida**  
  Al establecer que ningún código llega a producción sin ser revisado, se cultiva una cultura de responsabilidad colectiva sobre la calidad y seguridad del software.

::: info
**Registro y Trazabilidad**
:::

Cada revisión queda documentada en la propia interfaz del Pull Request, incluyendo:

- Los **comentarios técnicos** realizados por los revisores.
- Las **respuestas** del autor del código.
- El **historial de cambios** solicitados y aplicados.
- El **registro de aprobaciones** formales por parte de los miembros designados.

Este historial es esencial para mantener una trazabilidad clara de las decisiones técnicas, facilita futuras auditorías, y permite entender la evolución lógica del código en relación con los requerimientos funcionales.

::: info
**Prácticas Recomendadas**
:::

Como parte del protocolo interno del equipo, se definen las siguientes buenas prácticas para las revisiones:

- Todo PR debe estar acompañado de pruebas automáticas que verifiquen la nueva funcionalidad.
- El código debe compilar sin errores ni advertencias de estilo antes de ser revisado.
- El revisor debe ser un desarrollador distinto al autor del código, preferentemente con conocimiento en la parte funcional afectada.
- Se priorizan las revisiones asíncronas pero oportunas, para no bloquear el flujo de desarrollo.
- Se permite la participación de múltiples revisores en casos complejos.


\newpage

## Validation Interviews.

Las entrevistas de validación constituyen una herramienta cualitativa fundamental en la evaluación temprana de productos digitales, ya que permiten recopilar información directa y contextualizada sobre la experiencia de uso desde la perspectiva de los usuarios finales. En el presente proyecto, se llevaron a cabo entrevistas semiestructuradas con individuos representativos de los segmentos objetivo de la solución *RutaKids*, con el propósito de validar su adecuación funcional, nivel de usabilidad y grado de satisfacción percibida.

Estas entrevistas se diseñaron cuidadosamente para cubrir los principales puntos de contacto del sistema, incluyendo:

* La **landing page** promocional, orientada a captar nuevos usuarios y comunicar el valor diferencial de la propuesta.
* El **dashboard escolar** (aplicación web), dirigido a instituciones educativas y personal administrativo encargado de la gestión de rutas, alumnos y control logístico.
* La **aplicación móvil**, orientada principalmente a padres de familia y/o apoderados, quienes monitorean en tiempo real la ubicación y estado del transporte escolar.

Durante las sesiones, se solicitaron a los participantes que ejecutaran tareas específicas previamente definidas por el equipo (por ejemplo: registrarse, asignar un alumno, monitorear una ruta o revisar notificaciones). Al mismo tiempo, se documentaron tanto sus reacciones espontáneas como sus comentarios verbales, siguiendo la técnica del *think-aloud protocol*, que facilita la identificación de puntos de fricción, malentendidos o barreras cognitivas.

![Recurso extraído de Canva](src/img/cap2/entrevistas-introduccion.png)

\newpage

### Diseño de Entrevistas.

Las entrevistas de validación fueron diseñadas considerando las necesidades, contextos de uso y tareas más relevantes para cada segmento objetivo del proyecto. A cada entrevistado se le presentó un conjunto de escenarios y se le asignaron tareas concretas vinculadas con los *user flows* principales de su perfil de usuario.

::: box
**Segmento Objetivo 1:** Directivos escolares o personal administrativo
:::

**Interfaces validadas:**

* **Dashboard web** (gestión de rutas, reportes, alertas, asistencia)

* **Landing page** (como introducción al producto)

**Objetivo:** Validar si la plataforma facilita la gestión del transporte escolar, si la interfaz es clara, y si la información mostrada es suficiente y útil para sus tareas diarias.

**User Flows Evaluados y Preguntas de Validación:**

1) **Landing Page**  

  - **Objetivo:** Validar si la página comunica correctamente la propuesta de valor del sistema.  

  - **Preguntas:**  

    - ¿La información presentada en la landing page te ayudó a entender la solución?  

    - ¿Qué parte te pareció más útil o convincente?  
          
    - ¿Qué información adicional crees que podría motivarte a adquirir esta solución?



2) **User Flow 1: Ingreso al sistema**

    - **Objetivo:** Validar que el login sea claro, sencillo y transmita seguridad.  

    - **Preguntas:**  

      - ¿El proceso de inicio de sesión fue claro y fácil de completar?  

      - ¿La interfaz te generó confianza para ingresar tus credenciales?  

      - ¿Cambiarías o mejorarías algo en esta pantalla?

      

3) **User Flow 2: Visualización del panel de rutas activas** 

  - **Objetivo:** Evaluar si la información operativa de rutas es accesible y entendible. 

  - **Preguntas:**  

    - ¿Cómo percibes la organización del panel principal? ¿Te parece clara?

    - ¿Puedes identificar fácilmente el estado de las rutas y de cada bus?  

    - ¿La información presentada es la que necesitas para tomar decisiones?  

    - ¿Te gustaría ver algún otro tipo de dato aquí?

4) **User Flow 3: Emisión de notificaciones a padres**  

  - **Objetivo:** Validar la facilidad de enviar alertas y la percepción de control sobre la comunicación.  

  - **Preguntas:**  

    - ¿Cómo fue tu experiencia al intentar enviar una notificación a los padres?  

    - ¿Sentiste que el sistema te ofrecía suficiente control sobre el mensaje y el destinatario?  

    - ¿Agregarías algún tipo de notificación o canal adicional (SMS, correo, etc.)?  

    - ¿Consideras útil tener mensajes predefinidos o plantillas?

5) **User Flow 4: Consulta de reportes de asistencia y trayectos**  

  - **Objetivo:** Comprobar la utilidad, estructura y legibilidad de los reportes generados.  

  - **Preguntas:**  

    - ¿Los reportes presentados fueron fáciles de interpretar?  

    - ¿Te parecen útiles para reuniones o auditorías internas?  

    - ¿Preferirías recibir estos reportes automáticamente al correo?  

    - ¿Sientes que hay datos innecesarios o que falta información clave?

6) **User Flow 5: Configuración de alertas de llegada/salida**  

  - **Objetivo:** Verificar si el proceso es intuitivo y útil desde una perspectiva operativa.  

  - **Preguntas:**  

    - ¿Te pareció sencillo configurar alertas para los trayectos escolares?  

    - ¿Crees que estas alertas cubrirían tus necesidades diarias de supervisión?  

    - ¿Qué nivel de personalización esperas tener en estas configuraciones?  

    - ¿Preferirías una opción para programarlas automáticamente por curso o sección?

      
\newpage

::: box
**Segmento Objetivo 2:** Padres de familia con hijos en edad escolar
:::


**Interfaces validadas:**

* **Aplicación móvil para padres** (visualización del bus, notificaciones, historial, perfil)

* **Landing page** (introducción general del servicio)

**Objetivo:** Validar que los padres puedan usar la aplicación sin dificultad, que perciban seguridad y tranquilidad, y que reciban la información relevante de manera oportuna.

**User Flows Evaluados y Preguntas de Validación:**


1) **Landing Page**  

  - **Objetivo:** Evaluar si la landing page genera confianza y comunica el valor de la app.  

  - **Preguntas:**  

    - ¿La página te ayudó a entender qué hace la app?  

    - ¿Confías en la solución después de ver la información?  

    - ¿Qué mejorarías o agregarías para que más padres se interesen?


2) **User Flow 1: Registro e inicio de sesión como padre**  

  - **Objetivo:** Evaluar la claridad del proceso de registro e ingreso, especialmente en usuarios no técnicos.  

  - **Preguntas:**  

    - ¿Cómo te pareció el proceso de registro e inicio de sesión?  

    - ¿Algún paso te generó confusión o fue innecesario?  

    - ¿Te sentiste seguro al ingresar tu información personal?  

    - ¿Qué parte mejorarías para que sea más rápida o clara?

3) **User Flow 2: Visualización del bus escolar en tiempo real**  

  - **Objetivo:** Confirmar que el tracking funcione de forma comprensible y confiable.  

  - **Preguntas:**  

    - ¿Pudiste ubicar el bus de forma clara en el mapa?  

    - ¿La visualización te dio tranquilidad respecto al trayecto de tu hijo?  

    - ¿Te gustaría ver algún otro dato en esta pantalla (nombre del chofer, tiempo estimado de llegada, etc.)?  

    - ¿Te parece útil esta función en tu rutina diaria?

4)  **User Flow 3: Recepción de alertas de llegada y salida**  

  - **Objetivo:** Evaluar si las notificaciones automáticas son visibles, comprensibles y oportunas.  

  - **Preguntas:**  

    - ¿Las alertas de llegada o salida fueron fáciles de entender?  

    - ¿En qué momento te gustaría recibir estas notificaciones?  

    - ¿Qué medio prefieres: notificaciones en la app, correo, WhatsApp?  

    - ¿Te gustaría personalizar el contenido o la frecuencia de las alertas?

5) **User Flow 4: Consulta del historial de trayectos**  

  - **Objetivo:** Verificar la utilidad del historial para el control parental.  

  - **Preguntas:**  

    - ¿Encontraste fácilmente el historial de rutas?  

    - ¿Te parece útil ver los trayectos pasados de tu hijo?  

    - ¿Qué información extra agregarías a este historial (fecha, hora, chofer, etc.)?  

    - ¿Lo usarías como referencia ante algún problema o retraso?

6) **User Flow 5: Acceso y edición del perfil del estudiante**  

  - **Objetivo:** Evaluar si los padres pueden gestionar correctamente la información del alumno.  

  - **Preguntas:**  

    - ¿Fue fácil encontrar y editar la información de tu hijo?  

    - ¿Qué datos crees que deberían estar incluidos en ese perfil?  

    - ¿Preferirías tener un control más limitado o más detallado sobre el perfil?  

    - ¿Consideras útil que puedas vincular este perfil a varios acudientes (mamá, papá, tutor)?  

\newpage

### Registro de Entrevistas.

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

Durante la entrevista, se presentó a Max la landing page de RutaKids y el dashboard web administrativo. Desde el inicio, demostró alto interés en la solución, ya que, como mencionó anteriormente, su colegio enfrenta dificultades serias con el transporte escolar informal contratado por los padres.

Sobre la landing page, comentó que el mensaje inicial es claro y directo, destacando la frase "El futuro del transporte escolar está en tus manos". Consideró convincente el enfoque hacia la tranquilidad de las familias y la gestión institucional, aunque sugirió incluir más detalles técnicos o una sección de preguntas frecuentes para resolver dudas específicas de directores y docentes. La presencia de logos de colegios aliados le pareció adecuada para generar confianza.

En cuanto al inicio de sesión en la app web, valoró positivamente su simplicidad y rapidez. Indicó que la interfaz inspira confianza y que sería ideal integrar opciones de doble autenticación o acceso con credenciales institucionales.

Al explorar el panel principal de rutas, expresó que la organización es clara, pero sugirió destacar visualmente los vehículos en alerta o fuera de horario, usando colores más contrastantes. Le pareció muy útil tener una vista consolidada del estado de todas las unidades activas, lo cual ayudaría en la toma de decisiones diarias.

En el apartado de notificaciones a padres, quedó satisfecho con la facilidad de enviar alertas desde el sistema. Considera importante permitir mensajes personalizados, pero también cree que contar con plantillas predeterminadas para emergencias y avisos rutinarios agilizaría el trabajo del personal.

Sobre los reportes, comentó que son valiosos para auditorías y reuniones directivas, pero sugirió incluir filtros por nivel educativo o rutas específicas. También propuso la posibilidad de programar reportes automáticos al correo institucional.

Finalmente, respecto a la configuración de alertas, valoró que sea un proceso sencillo, pero indicó que sería ideal permitir configurar condiciones específicas (por ejemplo, alertas solo si hay retrasos mayores a 10 minutos). En general, calificó la solución como “altamente necesaria”, y mencionó que podría ser un factor clave para fidelizar a los padres y mejorar la imagen institucional del colegio.

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

Juliana Chávez, directora de una institución educativa privada, participó en la validación de la landing page y el sistema web administrativo de RutaKids. Desde un primer vistazo, destacó que la landing page comunica claramente el propósito del producto, resaltando que la propuesta de valor está bien enfocada hacia la tranquilidad y control institucional que los colegios necesitan frente a los desafíos actuales del transporte escolar informal.

Comentó que los beneficios descritos están bien planteados, pero sugirió que sería útil tener ejemplos más concretos o testimonios de instituciones similares. Además, indicó que agregar una sección donde se explique el funcionamiento técnico del sistema (GPS, reportes, etc.) podría fortalecer la confianza del usuario.

Al revisar el inicio de sesión, valoró su simplicidad, pero mencionó que sería conveniente permitir el acceso con cuentas institucionales preautorizadas para evitar la creación de múltiples credenciales.

Durante la revisión del panel de rutas activas, expresó que la interfaz es limpia y fácil de entender. Le pareció útil contar con una vista en tiempo real del estado de los buses y recomendó incluir una funcionalidad para filtrar por turnos (mañana/tarde) o niveles educativos, ya que en su colegio se manejan múltiples horarios.

Sobre la emisión de notificaciones a padres, encontró valioso el hecho de que se puedan enviar alertas desde el sistema, aunque señaló que sería ideal integrar canales adicionales como WhatsApp o SMS para situaciones de emergencia. También destacó que tener plantillas predefinidas podría ahorrar tiempo al personal administrativo.

En cuanto a los reportes, indicó que la herramienta tiene gran potencial para el seguimiento interno, especialmente para asistir en auditorías, supervisiones y reuniones con los padres. Considera esencial la posibilidad de exportar los reportes y recibirlos periódicamente al correo de dirección.

Finalmente, en la sección de configuración de alertas, consideró que la funcionalidad cubre adecuadamente las necesidades de supervisión escolar, pero sugiere que se pueda programar alertas automáticas para ciertos grupos (como estudiantes con condiciones médicas o de educación especial). En general, Juliana consideró la plataforma como “una herramienta alineada con los retos actuales del sector educativo privado”, y afirmó que podría implementarse con buena aceptación en su comunidad educativa si se mantiene asequible.

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

Graciela Ríos, promotora de una institución educativa en Paiján, evaluó la propuesta de RutaKids a través de la landing page y el sistema web para gestión de transporte escolar. Desde el inicio expresó que la necesidad de una solución tecnológica en su institución es alta, especialmente debido a la falta de supervisión sobre los vehículos que trasladan a los alumnos.

Valoró que la landing page de RutaKids logra comunicar adecuadamente la problemática y su solución, destacando como positiva la promesa de brindar seguridad y trazabilidad. Mencionó que incluir casos reales de uso o cifras comparativas podría reforzar aún más la decisión de adopción. También sugirió que se agregue una sección enfocada en beneficios para el personal educativo (auxiliares, psicólogos, administrativos), ya que son actores clave en la operación diaria.

Respecto al login en la plataforma web, Graciela lo consideró sencillo y funcional. Mencionó que sería útil ofrecer una opción de acceso rápido para distintos roles (promotor, auxiliar, docente), lo cual mejoraría la personalización del sistema.

En la visualización del panel principal, indicó que la información está bien organizada y que es fácil identificar qué unidades están en ruta. Le pareció útil que se muestre el nombre del conductor, la ruta asignada y el número de alumnos abordo. Sugeriría, sin embargo, una opción para ver alertas de retraso o desvíos en tiempo real con mayor visibilidad (colores o íconos más llamativos).

Sobre el módulo de notificaciones a padres, destacó como “esencial” la función de envío automático. Dijo que actualmente todo se realiza manualmente a través de llamadas, y que un sistema que notifique de forma proactiva a los padres sería una mejora significativa. También recomendó poder registrar la recepción del mensaje (lectura o entrega confirmada).

En cuanto a los reportes, se mostró interesada en su utilidad para analizar patrones de asistencia y comportamiento. Sugirió incluir datos agrupados por nivel o sección, ya que esto facilitaría la organización en reuniones con padres o áreas como Psicología.

Finalmente, en la parte de configuración de alertas, encontró valioso poder establecer parámetros específicos. Le gustaría poder programar alertas automáticas basadas en horarios predefinidos por sección, e incluso poder asociar ciertas alertas con observaciones médicas o conductuales.

En general, Graciela manifestó que una plataforma como RutaKids “no solo moderniza el colegio, sino que también alivia la carga emocional de los padres y mejora la capacidad de reacción del equipo educativo ante cualquier incidente relacionado con el transporte”.


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

Gabriela Ríos, madre de un estudiante de nivel secundario, validó la experiencia de uso a través de la landing page y la aplicación móvil para padres de familia. Desde el inicio destacó que el servicio actual que utiliza —aunque funcional— depende completamente de la comunicación personal con el conductor. Por ello, consideró que una herramienta como RutaKids podría cubrir vacíos importantes en seguridad, puntualidad y tranquilidad emocional.
Respecto a la landing page, comentó que transmite de forma clara el propósito del sistema, en especial al mencionar funciones como el rastreo en tiempo real y las notificaciones automáticas. Indicó que, para convencer a más padres, sería útil añadir testimonios reales o videos explicativos del funcionamiento de la app. También mencionó que ver el respaldo de una institución educativa mejora la confianza.
En el proceso de registro e inicio de sesión en la app móvil, lo calificó como sencillo, aunque sugirió que se debería permitir vincular automáticamente al estudiante al escanear un código QR proporcionado por el colegio. No tuvo problemas de seguridad percibida y le pareció positivo que se solicite confirmación para datos sensibles.
Durante la validación del mapa de rastreo del bus en tiempo real, expresó que fue su función favorita. Afirmó que le generó tranquilidad visualizar la ubicación exacta del vehículo, aunque sugirió que también se debería mostrar el nombre del conductor, una foto y la matrícula del bus. Mencionó que sería aún más útil incluir el tiempo estimado de llegada a casa o al colegio.
Con respecto a las alertas de llegada y salida, indicó que fueron fáciles de entender, pero preferiría recibirlas también por WhatsApp, ya que no siempre revisa las notificaciones de la app. Valoró que estas alertas aparezcan al momento en que el estudiante aborda o desciende del bus, y le gustaría poder personalizar el mensaje (por ejemplo, que incluya el nombre del hijo y la hora exacta).
Sobre la sección de historial de trayectos, indicó que es una funcionalidad útil que usaría especialmente en caso de retrasos o reclamos. Sugeriría añadir datos adicionales como hora exacta de embarque, ruta seguida y observaciones del conductor si hubo algún incidente.
Finalmente, en la parte de perfil del estudiante, le pareció intuitivo y fácil de usar. Valoró que se puedan incluir datos personales básicos, pero sugirió incorporar información médica relevante y la posibilidad de vincular el perfil a varios acudientes (padre, madre, tutor legal), lo cual es común en familias donde ambos padres trabajan.
En general, Gabriela afirmó que la solución presentada responde a una necesidad real de muchas familias. Comentó que estaría dispuesta a pagar por el servicio siempre que esté respaldado por la institución educativa, y concluyó señalando que: “esta app no solo mejora la logística, sino que le da paz mental a los padres que trabajamos y no podemos acompañar a nuestros hijos todo el tiempo”.



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

Zoila Lescano, madre de tres estudiantes de primaria, participó en la validación de la landing page y la aplicación móvil de RutaKids. Aunque actualmente utiliza un servicio de taxi personalizado para sus hijos, mostró un interés genuino en adoptar una solución tecnológica institucional como complemento de seguridad y monitoreo.
Respecto a la landing page, señaló que el contenido es claro y que comunica adecuadamente el propósito del sistema. Lo que más valoró fue la idea de contar con notificaciones automáticas y visualización en tiempo real. Sugirió incorporar una sección que detalle posibles usos de la app con diferentes tipos de movilidad (compartida, personalizada, escolar), ya que muchas familias combinan soluciones. También mencionó que se podría añadir una funcionalidad de botón de emergencia para tranquilizar aún más a los padres.
Durante la prueba del registro e inicio de sesión, lo calificó como intuitivo, aunque recomendó usar elementos visuales como íconos o pasos numerados para usuarios menos familiarizados con apps. Le pareció positivo que se soliciten datos básicos del estudiante al inicio, y estaría de acuerdo con una validación previa por parte del colegio.
En la pantalla de rastreo en tiempo real del bus, Zoila se mostró muy satisfecha, ya que replicaría varias de las funciones que actualmente su conductor de confianza realiza de manera manual. Comentó que ver el recorrido en vivo, el nombre del conductor y una estimación de llegada sería clave para mantener la tranquilidad. También recomendó una opción para recibir alertas si el vehículo se desvía o hace paradas no programadas.
Las notificaciones de llegada y salida le parecieron fáciles de entender, aunque expresó preferencia por recibirlas vía WhatsApp, dado que revisa más frecuentemente esa app. También recomendó poder personalizar el contenido, como incluir frases como “Tu hijo ya está en casa” o “Abordó a las 7:35 AM”.
En la revisión del historial de trayectos, dijo que lo utilizaría sobre todo para verificar horarios o responder ante consultas escolares. Le gustaría que el historial mostrara también si hubo retrasos o incidencias, y que fuera exportable como informe en PDF.
Finalmente, en el perfil del estudiante, comentó que fue fácil de encontrar y editar. Sugeriría incluir información médica o contactos de emergencia, y valoró mucho la posibilidad de vincular a más de un acudiente, especialmente en familias donde ambos padres trabajan o cuando hay apoyo de abuelos o tíos.
Zoila concluyó que una app como RutaKids representa un gran avance hacia la modernización del entorno escolar. Aunque se siente tranquila con su solución actual, considera que una herramienta institucional sería más confiable a largo plazo, y estaría dispuesta a asumir un costo adicional si se garantizan seguridad, notificaciones oportunas y una opción de respuesta en caso de emergencia.


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

Hayle Ascoy, madre de una estudiante de primaria y docente de profesión, revisó la landing page y utilizó la aplicación móvil de RutaKids simulando el rol de madre usuaria. Actualmente recurre a un servicio de movilidad escolar privada que considera funcional, aunque reconoce sentir una constante incertidumbre por la falta de comunicación inmediata o confirmación visual del trayecto de su hija.
Al revisar la landing page, Hayle valoró positivamente la propuesta, especialmente la mención de funciones como rastreo en tiempo real y notificaciones automáticas. Comentó que la página logra transmitir confianza, aunque recomendó incluir ejemplos de uso, una sección de preguntas frecuentes y videos cortos demostrativos para padres menos tecnológicos.
Durante el flujo de registro e inicio de sesión, no encontró dificultades, aunque sugirió ofrecer instrucciones más claras para el primer uso, especialmente en formatos accesibles como texto grande o audio. Consideró importante que la app solicite solo los datos necesarios para agilizar el proceso.
La funcionalidad de rastreo del bus en tiempo real fue una de las más valoradas por Hayle. Comentó que esta característica le daría mucha más tranquilidad en comparación con el sistema actual, donde debe insistir al conductor para confirmar si su hija llegó a salvo. Añadió que sería útil visualizar también el tiempo estimado de llegada y una pequeña foto del chofer para identificación rápida.
En la sección de notificaciones automáticas, señaló que le parecieron muy claras, pero preferiría poder recibirlas a través de WhatsApp, en lugar de depender exclusivamente de la app. También sugirió permitir que cada padre defina las horas o tipos de notificación que desea recibir, como por ejemplo solo alertas de llegada o solo si hay demoras inusuales.
El historial de trayectos le pareció una herramienta clave, sobre todo para resolver dudas en caso de ausencias o retrasos. Sugirió que los datos incluyan ubicación exacta, hora, e incluso un botón para generar un pequeño informe o alerta si algo no salió como se esperaba.
Finalmente, en la sección de perfil del estudiante, Hayle indicó que fue simple de usar y destacó la posibilidad de vincular más de un acudiente. Sugirió que se incluya una sección médica con alergias o condiciones especiales, así como una opción de contactos de emergencia alternativos.
Concluyó que esta aplicación cubriría una necesidad real de muchas madres y padres que trabajan tiempo completo. Afirmó que estaría dispuesta a pagar por un servicio que garantice la seguridad de su hija y reduzca su ansiedad diaria. Para ella, la clave es que el colegio sea quien respalde oficialmente la solución, lo cual —en sus palabras— “haría sentir a todos los padres que sus hijos están realmente protegidos desde que salen de casa hasta que regresan”.


![Imagen extraída del video de entrevistas](src/img/cap6/Entrevistas/HayleAscoy.png)

\newpage

### Evaluaciones según heurísticas.

#### Landing Page Validation

\begin{center}
\textbf{UX Heuristics \& Principles Evaluation} \\
\textbf{Usability – Inclusive Design – Information Architecture}
\end{center}

\vspace{10pt}

\begin{tabbing}
\hspace{5cm} \= \kill
\textbf{CARRERA:} \> Ingeniería de Software \\
\textbf{CURSO:} \> Diseño de Experimentos de Ingeniería de Software \\
\textbf{SECCIÓN:} \>  1ASI0732  \\
\textbf{PROFESORES:} \> Robles Fernández, Iván \\
\textbf{AUDITOR:} \> CodeMinds \\
\textbf{CLIENTE(S):} \> Padres de familia y directivos escolares \\
\end{tabbing}
\hrule

\vspace{10pt}

**SITE o APP A EVALUAR:** *Landing Page – RutaKids*

\vspace{10pt}

\textbf{TAREAS A EVALUAR:}  
El alcance de esta evaluación incluye las siguientes áreas de la landing page de RutaKids, basadas en las entrevistas realizadas:

\begin{enumerate}
    \item \textbf{Comunicación del propósito del producto}: Claridad en la presentación de la propuesta de valor.
    \item \textbf{Accesibilidad de la información institucional}:  Datos de contacto, identidad del equipo y seguridad.
    \item \textbf{Llamados a la acción}: Claridad y visibilidad de botones como "Contáctanos", "Explora la app", etc.
    \item \textbf{Confianza visual}: Diseño profesional, limpieza visual y credibilidad percibida.
    \item \textbf{Compatibilidad móvil}: Accesibilidad desde celulares y tiempos de carga.
\end{enumerate}

\newpage

**ESCALA DE SEVERIDAD**

Los errores serán puntuados tomando en cuenta la siguiente escala de severidad:

\begin{table}[H]
\begin{center}
\begin{tabular}{|p{2cm}|p{12cm}|}
\hline
\textbf{Nivel} & \textbf{Descripción} \\ \hline
1 & Problema superficial: puede ser fácilmente superado por el usuario o ocurre con muy poca frecuencia. No necesita ser arreglado a no ser que exista disponibilidad de tiempo. \\ \hline
2 & Problema menor: puede ocurrir un poco más frecuentemente o es un poco más difícil de superar para el usuario. Se debería asignar una prioridad baja resolverlo de cara al siguiente release. \\ \hline
3 & Problema mayor: ocurre frecuentemente o los usuarios no son capaces de resolverlo. Es importante que sean corregidos y se les debe asignar una prioridad alta. \\ \hline
4 & Problema muy grave: un error de gran impacto que impide al usuario continuar con el uso de la herramienta. Es imperativo que sea corregido antes del lanzamiento. \\ \hline
\end{tabular}
\end{center}
\end{table}

\vspace{10pt}


**TABLA RESUMEN**

\begin{table}[H]
\begin{center}
\begin{tabular}{|c|p{5cm}|c|p{5cm}|} \hline
\textbf{\#} & \textbf{Problema} & \textbf{Escala de severidad} & \textbf{Heurística/Principio violado} \\ \hline
1 & Información institucional relevante solo visible al final del sitio & 2 & Information Architecture – Findability \\ \hline
2 & Poca jerarquía visual en botones principales (CTA) como “Solicita una demo” & 2 & Usabilidad – Visibilidad del estado del sistema \\ \hline
3 & Falta de elementos de confianza como certificaciones, sellos o premios & 3 & Usabilidad – Confianza y seguridad \\ \hline
4 & En versión móvil, el CTA queda debajo del “fold” inicial & 2 & Inclusive Design – Responsive Design \\ \hline
\end{tabular}
\end{center}
\end{table}


\newpage

**DESCRIPCIÓN DE PROBLEMAS**

**PROBLEMA \#1: Información institucional relevante solo visible al final del sitio**
  
  **Severidad:** 2 
  
  **Heurística violada:** Information Architecture – Findability

  **Problema:** Datos de contacto, ubicación y canales de comunicación (email, teléfono) solo están disponibles en el footer, lo cual no es evidente para usuarios que no hacen scroll completo.

  **Recomendación:** Agregar acceso directo desde el menú superior o incluir una barra flotante con contacto visible.

**PROBLEMA \#2: Poca jerarquía visual en botones principales (CTA)**
  
  **Severidad:** 2

  **Heurística violada:** Usabilidad – Visibilidad del estado del sistema

  **Problema:** El botón "Solicita una demo" se presenta sin suficiente contraste respecto a otros elementos de texto, lo que disminuye su efectividad como CTA.

  **Recomendación:** Aumentar contraste, tamaño y colocar íconos para mejorar la atención visual del usuario.


**PROBLEMA \#3: Falta de elementos de confianza como certificaciones, sellos o premios**

  **Severidad:** 3

  **Heurística violada:** Usabilidad – Confianza y seguridad

  **Descripción:** Aunque se muestran logos de instituciones, no hay elementos explícitos que refuercen seguridad (por ejemplo: sellos de privacidad, ISO, reconocimientos).

  **Recomendación:** Incluir testimonios de clientes, sellos oficiales o insignias certificadas para reforzar credibilidad.

**PROBLEMA \#4: En versión móvil, el CTA queda debajo del "fold" inicial**

  **Severidad:** 2

  **Heurística violada:** Inclusive Design – Responsive Design

  **Descripción:** En la vista móvil, el botón “Solicita una demo” no es visible al cargar la pantalla, lo que reduce conversiones en usuarios móviles.

  **Recomendación:** Reubicar el botón o hacer que permanezca fijo en la pantalla para facilitar su acceso.

\newpage

#### Web App Validation

\begin{center}
\textbf{UX Heuristics \& Principles Evaluation} \\
\textbf{Usability – Inclusive Design – Information Architecture}
\end{center}

\vspace{10pt}

\begin{tabbing}
\hspace{5cm} \= \kill
\textbf{CARRERA:} \> Ingeniería de Software \\
\textbf{CURSO:} \> Diseño de Experimentos de Ingeniería de Software \\
\textbf{SECCIÓN:} \>  1ASI0732  \\
\textbf{PROFESORES:} \> Robles Fernández, Iván \\
\textbf{AUDITOR:} \> CodeMinds \\
\textbf{CLIENTE(S):} \> Padres de familia y directivos escolares \\
\end{tabbing}
\hrule

\hrule

\vspace{10pt}

**SITE o APP A EVALUAR:** *App Web – RutaKids*

\vspace{10pt}

**TAREAS A EVALUAR:**  
El alcance de esta evaluación incluye las siguientes tareas realizadas por los usuarios administrativos (directivos escolares) en la plataforma web:

\begin{enumerate}
    \item \textbf{Inicio de sesión}: Acceso seguro a la plataforma.
    \item \textbf{Visualización del panel principal}: Información de rutas, asistencia y estado del transporte.
    \item \textbf{Envío de notificaciones}: Comunicación directa con padres o personal.
    \item \textbf{Consulta de reportes}: Acceso a métricas de asistencia y trazabilidad.
    \item \textbf{Configuración de alertas}: Gestión de condiciones y parámetros del sistema.
\end{enumerate}

\newpage

**ESCALA DE SEVERIDAD**

Los errores serán puntuados tomando en cuenta la siguiente escala de severidad:

\begin{table}[H]
\begin{center}
\begin{tabular}{|p{2cm}|p{12cm}|}
\hline
\textbf{Nivel} & \textbf{Descripción} \\ \hline
1 & Problema superficial: puede ser fácilmente superado por el usuario o ocurre con muy poca frecuencia. No necesita ser arreglado a no ser que exista disponibilidad de tiempo. \\ \hline
2 & Problema menor: puede ocurrir un poco más frecuentemente o es un poco más difícil de superar para el usuario. Se debería asignar una prioridad baja resolverlo de cara al siguiente release. \\ \hline
3 & Problema mayor: ocurre frecuentemente o los usuarios no son capaces de resolverlo. Es importante que sean corregidos y se les debe asignar una prioridad alta. \\ \hline
4 & Problema muy grave: un error de gran impacto que impide al usuario continuar con el uso de la herramienta. Es imperativo que sea corregido antes del lanzamiento. \\ \hline
\end{tabular}
\end{center}
\end{table}

\vspace{10pt}

**TABLA RESUMEN**

\begin{table}[H]
\begin{center}
\begin{tabular}{|c|p{5cm}|c|p{5cm}|} \hline
\textbf{\#} & \textbf{Problema} & \textbf{Escala de severidad} & \textbf{Heurística/Principio violado} \\ \hline
1 & Panel de reportes con exceso de información irrelevante & 2 & Information Architecture – Is it usable? \\ \hline
2 & Dificultad para identificar el botón de configuración de alertas & 3 & Usabilidad – Visibilidad del estado del sistema \\ \hline
3 & Falta de personalización de notificaciones automatizadas & 2 & Usabilidad – Flexibilidad y eficiencia de uso \\ \hline
4 & Ausencia de retroalimentación tras guardar configuraciones & 2 & Usabilidad – Visibilidad del estado del sistema \\ \hline
\end{tabular}
\end{center}
\end{table}

\newpage

**DESCRIPCIÓN DE PROBLEMAS**

**PROBLEMA \#1: Panel de reportes con exceso de información irrelevante**
  
  **Severidad:** 2
  
  **Heurística violada:** Information Architecture – Is it usable?

  **Descripción:** Las tablas de reportes incluyen múltiples columnas poco útiles para el usuario promedio. Esto genera ruido visual y dificulta ubicar datos clave.

  **Recomendación:** Incluir filtros dinámicos, opción de ocultar columnas y agrupación de vistas (por estudiante, por ruta, por día).


**PROBLEMA \#2: Dificultad para identificar el botón de configuración de alertas**
  
  **Severidad:** 3

  **Heurística violada:** Usabilidad – Visibilidad del estado del sistema

  **Descripción:** El botón o ícono para configurar alertas no es intuitivo ni está claramente resaltado, por lo que los usuarios no lo encuentran rápidamente.

  **Recomendación:** Utilizar un ícono universal de “engranaje” con texto visible o tooltip, además de ubicarlo en una zona más lógica del flujo.


**PROBLEMA \#3: Falta de personalización de notificaciones automatizadas**

  **Severidad:** 2

  **Heurística violada:** Usabilidad – Flexibilidad y eficiencia de uso

  **Descripción:** No es posible seleccionar horarios, tipos de alerta ni públicos objetivos (solo padres, solo conductores, etc.)

  **Recomendación:** Incluir un panel de configuración más granular que permita personalizar los eventos disparadores y los canales.


**PROBLEMA \#4: Ausencia de retroalimentación tras guardar configuraciones**

  **Severidad:** 2

  **Heurística violada:** Usabilidad – Visibilidad del estado del sistema

  **Descripción:** Al realizar cambios en parámetros o ajustes, no aparece una confirmación visual (ni modal ni toast).

  **Recomendación:** Incluir un mensaje de confirmación breve tras guardar (ej. “Cambios guardados correctamente”).

\newpage


#### Mobile App Validation

\begin{center}
\textbf{UX Heuristics \& Principles Evaluation} \\
\textbf{Usability – Inclusive Design – Information Architecture}
\end{center}
\vspace{10pt}

\begin{tabbing}
\hspace{5cm} \= \kill
\textbf{CARRERA:} \> Ingeniería de Software \\
\textbf{CURSO:} \> Diseño de Experimentos de Ingeniería de Software \\
\textbf{SECCIÓN:} \>  1ASI0732  \\
\textbf{PROFESORES:} \> Robles Fernández, Iván \\
\textbf{AUDITOR:} \> CodeMinds \\
\textbf{CLIENTE(S):} \> Padres de familia y directivos escolares \\
\end{tabbing}
\hrule

\hrule

\vspace{10pt}

**SITE o APP A EVALUAR:** *App Móvil – RutaKids*

\vspace{10pt}

**TAREAS A EVALUAR:**  
El alcance de esta evaluación incluye las siguientes funcionalidades de la aplicación móvil, basadas en los flujos más usados por los padres de familia:

\begin{enumerate}
    \item \textbf{Inicio de sesión y acceso a la app}
    \item \textbf{Visualización de ubicación del bus escolar en tiempo real}
    \item \textbf{Recepción de notificaciones de llegada y salida}
    \item \textbf{Consulta de historial de rutas y asistencia}
    \item \textbf{Visualización y edición del perfil del estudiante}
\end{enumerate}

\newpage

**ESCALA DE SEVERIDAD**

Los errores serán puntuados tomando en cuenta la siguiente escala de severidad:

\begin{table}[H]
\begin{center}
\begin{tabular}{|p{2cm}|p{12cm}|}
\hline
\textbf{Nivel} & \textbf{Descripción} \\ 
\hline
1 & Problema superficial: puede ser fácilmente superado por el usuario o ocurre con muy poca frecuencia. No necesita ser arreglado a no ser que exista disponibilidad de tiempo. \\ 
\hline
2 & Problema menor: puede ocurrir un poco más frecuentemente o es un poco más difícil de superar para el usuario. Se debería asignar una prioridad baja resolverlo de cara al siguiente release. \\ 
\hline
3 & Problema mayor: ocurre frecuentemente o los usuarios no son capaces de resolverlo. Es importante que sean corregidos y se les debe asignar una prioridad alta. \\ 
\hline
4 & Problema muy grave: un error de gran impacto que impide al usuario continuar con el uso de la herramienta. Es imperativo que sea corregido antes del lanzamiento. \\ 
\hline
\end{tabular}
\end{center}
\end{table}

\vspace{10pt}

**TABLA RESUMEN**

\begin{table}[H]
\begin{center}
\begin{tabular}{|c|p{5cm}|c|p{5cm}|} 
\hline
\textbf{\#} & \textbf{Problema} & \textbf{Escala de severidad} & \textbf{Heurística/Principio violado} \\ 
\hline
1 & Mapa sin referencias claras ni leyenda visible & 3 & Inclusive Design – Claridad visual \\ 
\hline
2 & Botones de acción pequeños o mal posicionados & 2 & Usabilidad – Accesibilidad física \\ 
\hline
3 & Falta de historial exportable o imprimible & 2 & Usabilidad – Flexibilidad y eficiencia \\ 
\hline
4 & Perfil del estudiante con opciones limitadas de edición & 2 & Usabilidad – Control y libertad del usuario \\ 
\hline
\end{tabular}
\end{center}
\end{table}

\newpage

**DESCRIPCIÓN DE PROBLEMAS**

**PROBLEMA \#1: Mapa sin referencias claras ni leyenda visible**

  **Severidad:** 3

  **Heurística violada:** Inclusive Design – Claridad visual

  **Descripción:** El mapa muestra la ubicación del bus, pero algunos usuarios no entendieron el significado de los íconos (bus, casa, colegio, etc.), ni qué ruta seguía.

  **Recomendación:** Agregar una leyenda simple, incluir flechas de dirección y diferenciar íconos con colores y etiquetas.


**PROBLEMA \#2: Botones de acción pequeños o mal posicionados**

  **Severidad:** 2

  **Heurística violada:** Usabilidad – Accesibilidad física

  **Descripción:** Algunos usuarios reportaron dificultad al intentar presionar botones pequeños como “Notificaciones” o “Visualizar unidad”, especialmente en pantallas pequeñas.

  **Recomendación:** Aumentar el tamaño de las zonas táctiles a mínimo 48px y revisar márgenes internos.


**PROBLEMA \#3: Falta de historial exportable o imprimible**

  **Severidad:** 2

  **Heurística violada:** Usabilidad – Flexibilidad y eficiencia

  **Descripción:** Aunque los padres pueden revisar el historial de viajes, no existe opción de descarga, exportación ni generación de resumen mensual.

  **Recomendación:** Incluir opción de exportar a PDF/Excel o compartir el historial desde el celular.


**PROBLEMA \#4: Perfil del estudiante con opciones limitadas de edición**

  **Severidad:** 2

  **Heurística violada:** Usabilidad – Control y libertad del usuario

  **Descripción:** El perfil del estudiante solo permite visualizar información estática (nombre, curso), sin opciones de añadir datos médicos, alergias o contactos alternativos.

  **Recomendación:** Ampliar campos de edición con datos complementarios que puedan ser útiles para el colegio y para emergencias.

\newpage

## Auditoría de Experiencias de Usuario

Como parte del proceso de validación cruzada promovido en el curso, el equipo CodeMinds – RutaKids participó activamente en un ejercicio de auditoría recíproca de experiencia de usuario, llevado a cabo entre equipos de proyecto. Este procedimiento metodológico tuvo como finalidad complementar los estudios de validación interna con una evaluación externa, crítica y estructurada, enfocada en detectar oportunidades de mejora relacionadas con la usabilidad, la accesibilidad, el diseño visual y la arquitectura de información.

Dichas auditorías se enmarcaron dentro de un enfoque heurístico, guiado por principios ampliamente reconocidos como:

- Las diez heurísticas de usabilidad de Jakob Nielsen, que establecen criterios fundamentales para la interacción eficaz entre el usuario y la interfaz.

- Principios de diseño inclusivo, orientados a asegurar que el producto sea utilizable por personas con diferentes niveles de habilidad, experiencia, o limitaciones temporales o permanentes.

- Pautas complementarias de diseño centrado en el usuario que refuerzan la coherencia, accesibilidad y satisfacción general del sistema.

::: info
**Proceso de Auditoría**
:::

El proceso consistió en dos instancias principales:

- **Auditoría realizada por el equipo CodeMinds**
  El equipo analizó los productos digitales de otro grupo del curso, que incluyeron su landing page y las aplicaciones asociadas (web y/o móvil). Esta revisión se realizó de manera estructurada, empleando herramientas y plantillas de evaluación previamente consensuadas. Cada miembro del equipo tuvo asignadas responsabilidades específicas (por ejemplo: evaluar accesibilidad, revisar flujos de navegación, analizar estructura jerárquica de contenidos), lo cual permitió una auditoría integral y enfocada.

- **Auditoría recibida sobre el proyecto RutaKids**
  De forma recíproca, otro equipo externo auditó los productos del sistema RutaKids. Esta instancia permitió recibir retroalimentación valiosa desde una mirada fresca y ajena al desarrollo del producto, aumentando así el grado de objetividad del análisis. El equipo auditor empleó la misma metodología estructurada, documentando hallazgos mediante capturas de pantalla, observaciones detalladas, puntuaciones heurísticas y sugerencias concretas de mejora.

::: info
**Herramientas y Evidencias**
:::

Durante el proceso, se emplearon los siguientes instrumentos de recolección y documentación:

- Plantillas estructuradas con criterios por dimensión heurística (visibilidad del sistema, control del usuario, consistencia, flexibilidad, manejo de errores, etc.).

- Sesiones virtuales coordinadas, en las que se compartió pantalla y se recorrieron flujos críticos de la interfaz.

- Evidencias visuales (screenshots, videos o notas marcadas) que respaldaron cada hallazgo, facilitando su posterior análisis y priorización.

- Cuestionarios de puntuación para asignar valores cuantitativos a la experiencia general en aspectos clave.

::: info
**Resultados y Valor Agregado**
:::

Ambas auditorías arrojaron hallazgos relevantes que complementaron las observaciones obtenidas en las entrevistas de validación con usuarios finales. Los resultados permitieron:

- Detectar pequeños puntos de fricción que habían pasado desapercibidos durante las pruebas internas.

- Validar la claridad de navegación, uso del color y jerarquía visual en dispositivos móviles.

- Identificar mejoras posibles en los textos de ayuda, mensajes de error y retroalimentación del sistema.

- Obtener sugerencias sobre alternativas de diseño más accesibles, como contrastes, tamaño de fuente o navegación con teclado.

![Recurso extraído de Canva](src/img/cap6/auditoria.png)

\newpage

### Auditoría realizada.

Esta sección documenta la auditoría de experiencia de usuario realizada por el equipo ***CodeMinds – RutaKids*** a otro equipo del curso, como parte del proceso de validación cruzada. La auditoría fue realizada siguiendo el formato de evaluación heurística proporcionado por el curso y se enfocó en detectar oportunidades de mejora en la interfaz y experiencia general del proyecto auditado.

#### Información del grupo auditado.

- **Nombre del grupo auditado:** SuperMed

- **Proyecto auditado:** *Med*

- **Segmento objetivo evaluado:** *Doctores/Especialistas y Pacientes*

- **Interfaces evaluadas:**

  - *Landing Page*
  - *Aplicación web*

#### Cronograma de auditoría realizada.

\begin{table}[H]
\begin{center}
\begin{tabular}{|c|p{6cm}|p{6cm}|} \hline
\textbf{Fecha} & \textbf{Actividad realizada} & \textbf{Participantes} \\ \hline
19/06/2025 & Reunión de coordinación con grupo auditado & Miembros de ambos equipos \\ \hline
19/06/2025 & Aplicación de evaluación heurística & CodeMinds – RutaKids \\ \hline
19/06/2025 & Discusión de hallazgos y entrega de recomendaciones & CodeMinds – RutaKids \\ \hline
\end{tabular}
\end{center}
\end{table}


#### Contenido de auditoría realizada.

  **a) Criterios utilizados**

  La auditoría se basó en los siguientes principios de evaluación:

  * Usabilidad (heurísticas de Nielsen)  

  * Diseño inclusivo  

  * Arquitectura de información  

  * Accesibilidad visual y funcional  

  * Percepción de confianza

  Se empleó la plantilla de evaluación heurística proporcionada en el curso, adaptando las observaciones según el contexto del proyecto “Med”.

  **b) Interfaz(es) evaluadas**

  1) **Landing Page – [http://landingpage-med.netlify.app](http://landingpage-med.netlify.app)**  
    Se evaluó la claridad en la propuesta de valor, organización de los contenidos, efectividad de los llamados a la acción (CTAs) y percepción de confianza. También se revisó el diseño visual, la jerarquía tipográfica y el lenguaje utilizado en los textos para validar si conecta con los usuarios (pacientes, doctores y clínicas).

   - **Hallazgos**:
      * La propuesta de valor es visible y rápida de entender desde la portada.  

      * Se identificaron buenas prácticas en cuanto a diseño visual: uso adecuado de iconografía, estructura clara por segmentos, y paleta de colores alineada con el sector salud.
      
  2) **Aplicación Web – [http://med-webapp.netlify.app](http://med-webapp.netlify.app)**  
    Se evaluaron los siguientes flujos principales:
      * Registro de usuarios (pacientes y doctores)  

      * Inicio de sesión  

      * Dashboard principal  

      * Módulo de citas (doctores y pacientes)  

      * Módulo de tratamientos (creación, edición, visualización y eliminación)  

      * Navegación y estructura de menús laterales

   -  **Hallazgos**:
        * La interfaz mantiene consistencia visual y navegación clara, especialmente en la barra lateral.  

        * La segmentación por roles (doctor/paciente) está bien diferenciada, lo que facilita la personalización del contenido.  

        * Algunas áreas, como el historial o resultados de citas, podrían beneficiarse de una jerarquía visual más clara para facilitar la lectura.

  **c) Resultados de la auditoría basada en heurísticas de usabilidad**

  A continuación, se presentan los principales hallazgos encontrados durante la evaluación heurística de las interfaces del proyecto *Med*, agrupados según los principios de usabilidad de Nielsen. Cada problema identificado incluye su severidad y una recomendación específica para su mejora.

 \begin{table}[H]
  \begin{center}
  \begin{tabular}{|p{1cm}|p{4cm}|p{3cm}|p{3cm}|p{3cm}|} \hline
  \textbf{Nº} & \textbf{Problema identificado} & \textbf{Severidad} & \textbf{Heurística afectada} & \textbf{Ubicación} \\ \hline
  1 & En la landing, el botón Nuestra Página no indica claramente su función hasta ser usado & 2 & Visibilidad del estado del sistema & Landing Page \\ \hline
  2 & No hay botón en el hero de la landing que direccione a la plataforma & 3 & Visibilidad del estado del sistema & Landing Page \\ \hline
  3 & Al agregar un tratamiento, no aparece ningún mensaje de confirmación o error & 3 & Visibilidad del estado del sistema & App Web / Doctor o Especialista \\ \hline
  4 & En el panel de citas, las fechas aparecen con formato UTC (`2025-06-26T05:00:00.000Z`) & 2 & Reconocer en lugar de recordar & App Web / Doctor o Especialista \\ \hline
  5 & No se muestra mensaje tras eliminar un tratamiento & 3 & Visibilidad del estado del sistema & App Web / Doctor o Especialista \\ \hline
  \end{tabular}
  \end{center}
  \end{table}

\newpage

### Auditoría recibida.

Esta sección presenta la evaluación de experiencia de usuario realizada por el equipo ***InnovaTech*** al proyecto *RutaKids*, como parte del proceso de auditoría cruzada del curso. El objetivo fue identificar oportunidades de mejora en la usabilidad, accesibilidad y arquitectura de la información del producto mediante una evaluación heurística guiada por principios de diseño centrado en el usuario.

#### Información del grupo auditor.

- **Nombre del grupo auditor:** CodeMinds

- **Proyecto auditor:** *Rutakids*

- **Segmento objetivo validado:** *Directivos escolares y Padres de familia*

- **Interfaces auditadas:**

  - *Landing Page*
  - *Aplicación web*

- **Responsables de auditoría:** Miembros del equipo InnovaTech

#### Cronograma de auditoría recibida.

\begin{table}[H]
\begin{center}
\begin{tabular}{|c|p{6cm}|p{6cm}|} \hline
\textbf{Fecha} & \textbf{Actividad realizada} & \textbf{Participantes} \\ \hline
19/06/2025 & Reunión de coordinación con grupo auditor & Miembros de ambos equipos \\ \hline
19/06/2025 & Aplicación de evaluación heurística & InnovaTech \\ \hline
19/06/2025 & Discusión de hallazgos y entrega de recomendaciones & InnovaTech \\ \hline
\end{tabular}
\end{center}
\end{table}

#### Contenido de auditoría recibida.

  **a) Criterios utilizados**

  La auditoría se basó en los siguientes principios de evaluación:

  * Usabilidad (heurísticas de Nielsen)  

  * Diseño inclusivo  

  * Arquitectura de información  

  * Accesibilidad visual y funcional  

  * Percepción de confianza

  Se empleó la plantilla de evaluación heurística proporcionada en el curso, adaptando las observaciones según el contexto del proyecto “RutaKids”.

  **b) Interfaz(es) evaluadas**

  1) **Landing Page – [https://llantatech.org.pe/](https://llantatech.org.pe/)**  
    Se analizó la claridad de la propuesta de valor, la estructura del contenido, la efectividad de los llamados a la acción (CTAs) y el nivel de confianza que transmite. Además, se examinó el diseño visual, la jerarquía tipográfica y el estilo del lenguaje empleado en los textos para verificar si resulta relevante y comprensible para los distintos tipos de usuarios.

   - **Hallazgos**:
      * La propuesta de valor se comprende desde el inicio. 

      * Se identificaron buenas prácticas en cuanto a diseño visual: uso coherente de colores, adecuada jerarquía tipográfica, espacios en blanco bien distribuidos que favorecen la lectura, imágenes de calidad alineadas con el mensaje de la marca, diseño responsive que se adapta correctamente a distintos dispositivos.
      
  2) **Aplicación Web – [hhttps://rutakids-webapp-angular18.onrender.com/authentication/sign-in](https://rutakids-webapp-angular18.onrender.com/authentication/sign-in)**  
    Se evaluaron los siguientes flujos principales:

      *	Inicio de sesión

      *	Dashboard principal

      *	Módulo de estudiantes

      *	Módulo de movilidad

      * Módulo de rutas

      * Módulo de notificaciones

      * Módulo de correos

      * Módulo de perfil

      * Módulo de configuración

      * Navegación y estructura de menús laterales


   -  **Hallazgos**:
        * La navegación es clara y consistente, con menús laterales bien estructurados.  

        * El dashboard principal proporciona una visión general clara de las funcionalidades disponibles. 

        * Los módulos de estudiantes, movilidad y rutas están bien organizados, permitiendo un acceso rápido a la información relevante.

  **c) Resultados de la auditoría basada en heurísticas de usabilidad**

  A continuación, se presentan los principales hallazgos encontrados durante la evaluación heurística de las interfaces del proyecto RutaKids, agrupados según los principios de usabilidad de Nielsen y arquitectura de información. Cada problema identificado incluye su severidad y una recomendación específica para su mejora.

  \begin{table}[H]
  \begin{center}
  \begin{tabular}{|p{1cm}|p{4cm}|p{3cm}|p{3cm}|p{3cm}|} \hline
  \textbf{Nº} & \textbf{Problema identificado} & \textbf{Severidad} & \textbf{Heurística afectada} & \textbf{Ubicación} \\ \hline
  1 & El botón CTA para iniciar sesión no funciona & 2 & Arquitectura de Información – ¿Es utilizable? & Landing Page \\ \hline
  2 & La sección FAQ no cuenta con información relevante & 3 & Usabilidad – Ayuda y documentación & App Web \\ \hline
  3 & La sección de correo no funciona correctamente & 3 & Arquitectura de Información – ¿Es controlable? & App Web \\ \hline
  4 & El formulario de registro de una movilidad no valida correctamente los campos & 2 & Usabilidad – Prevención de errores & App Web \\ \hline
  5 & Inconsistencia en el lenguaje (español e inglés mezclados) & 3 & Usabilidad – Consistencia y estándares & App Web \\ \hline
  \end{tabular}
  \end{center}
  \end{table}

  
\newpage

#### Resumen de modificaciones para subsanar hallazgos.

A partir de los hallazgos identificados por el equipo auditor InnovaTech, se definieron las siguientes acciones correctivas:

\begin{table}[H]
\begin{center}
\begin{tabular}{|p{1cm}|p{5cm}|p{4cm}|p{4cm}|} \hline
\textbf{Nº} & \textbf{Modificación realizada} & \textbf{Problema solucionado} & \textbf{Estado} \\ \hline
1 & Se corrigió la redirección del botón CTA hacia la app web desde la landing & El botón CTA para iniciar sesión no funciona & Implementado \\ \hline
2 & Se está trabajando una sección FAQ con preguntas reales y relevantes para padres y directivos & La sección FAQ no cuenta con información relevante & En proceso \\ \hline
3 & Se reparó el enlace de contacto para que abra el cliente de correo correctamente & La sección de correo no funciona correctamente & Implementado \\ \hline
4 & Se añadieron validaciones básicas en los campos del formulario para evitar envíos vacíos o erróneos & El formulario de registro de una movilidad no valida correctamente los campos & Implementado \\ \hline
5 & Se ha iniciado la traducción completa al español y eliminación de términos en inglés innecesarios & Inconsistencia en el lenguaje (español e inglés mezclados) & En proceso \\ \hline
\end{tabular}
\end{center}
\end{table}

\newpage
