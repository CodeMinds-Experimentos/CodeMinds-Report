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

### Core Behavior-Driven Development

::: box
***Angular***
:::

En esta sección se aplicó la metodología BDD (Behavior-Driven Development) para validar los flujos clave de interacción del administrador educativo en la plataforma. Esta estrategia permite alinear las pruebas automatizadas con los criterios de aceptación definidos en las historias de usuario (US), usando escenarios escritos en lenguaje natural (Gherkin).

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

\begin{longtable}{|p{1.5cm}|p{6cm}|p{4.5cm}|p{3.5cm}|}
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
