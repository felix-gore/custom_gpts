# Marco de referencia de gestión de datos Estado

ID: GUIDE-STS-MASTER-01
Version: 1.0.0
Status: Draft
Human-Creator: FS
Human-Editor: FS
Model-Collaborator: IA-GEMINI
Creation-Date: 2025-07-06
Modification-Date: 2025-07-06
Primary-Source: kb_063_tde_guia_marco_datos.md
Ref-STS-Guide: GUIDE-STS-MASTER-01

## 1. Fundamentos del MGDE

ID: GESTDAT-MGDE-FUNDAMENTOS-ROOT-01
Purp: Establecer el contexto, propósito y principios del Marco de Referencia de Gestión de Datos del Estado (MGDE).

### 1.1. Propósito y Contexto

ID: GESTDAT-MGDE-FUNDAMENTOS-PROPOSITO-01

- Obj: Orientar a los Órganos de la Administración del Estado (OAE) en la adopción de buenas prácticas de gestión de datos usando el MGDE.
- Fnd: La gestión de datos es crítica para el éxito organizacional y la generación de valor público.
- Ref: OCDE - Dimensiones de un Gobierno Digital.
  - `- Digital por diseño.`
  - `- Impulsado por los datos.`
  - `- Actúa como plataforma.`
  - `- Abierto por defecto.`
  - `- Dirigido por el usuario.`
  - `- Proactivo.`
- Res: Beneficios de la Gestión de Datos.
  - `- Alinea la gestión de datos con objetivos estratégicos.`
  - `- Mejora la calidad del servicio y la eficiencia de los procesos.`
  - `- Disminuye el tiempo de diseño y desarrollo.`
  - `- Optimiza los costos del ciclo de vida.`
  - `- Define roles y responsabilidades.`
  - `- Facilita sinergias entre personas, procesos, información y tecnología.`
  - `- Homogeniza la comprensión en el Estado.`
- Fnd: Legal.
  - `- Ref: Ley N° 21.658 (Crea Secretaría de Gobierno Digital - SGD).
    - Mssn: Proponer la Estrategia de Gobierno Digital.
    - Mssn: Coordinar, asesorar y apoyar en el uso estratégico de tecnologías digitales, datos e información pública.`
  - `- Ref: Ley N° 18.575 (Orgánica constitucional de bases generales de la administración del Estado).
    - Def: Define a los OAE.`

### 1.2. Principios Orientadores

ID: GESTDAT-MGDE-PRINCIPIOS-01
Purp: Definir los principios base que orientan las prácticas de gestión de datos.
Req: Los OAEs deben suscribir e incluir estos principios en su política de gobernanza de datos.

- Cpt: Principio 1. Req: La gestión de datos debe mejorar los servicios a las personas.
- Cpt: Principio 2. Req: Los datos (internos/externos) son activos estratégicos para metas y objetivos institucionales, incluyendo documentos y otros contenidos digitales.
- Cpt: Principio 3. Req: Todo activo/conjunto de datos será catalogado y documentado con metadatos.
- Cpt: Principio 4. Req: Todo activo/conjunto de datos tendrá un responsable (administrador/custodio) para velar por su actualización, mantenimiento, confiabilidad, precisión, completitud y disponibilidad.
- Cpt: Principio 5. Req: Se promoverá la digitalización, el uso analítico y el trabajo colaborativo en torno a los datos.
- Cpt: Principio 6. Req: Se promoverá la evaluación de la calidad de los datos.
- Cpt: Principio 7. Req: Se promoverá la interoperabilidad de los datos (interna/externa).
- Cpt: Principio 8. Req: Se procurará un uso ético de datos, cumpliendo la normativa vigente (especialmente protección de datos personales).
- Cpt: Principio 9. Req: El acceso a datos debe tener roles y responsabilidades definidos en el contexto de la seguridad institucional.
- Cpt: Principio 10. Req: La gestión de datos se planificará, implementará, evaluará y mejorará de forma integral y continua.

### 1.3. Ciclo de Vida de los Datos

ID: GESTDAT-MGDE-CICLOVIDA-01
Purp: Describir las 8 etapas del ciclo de vida de los datos.

- Cpt: Etapa 1 - Generación. Def: Creación de datos dentro o fuera de la organización.
- Cpt: Etapa 2 - Recolección. Def: Captura de datos (formularios, apps, interoperabilidad, streaming).
- Cpt: Etapa 3 - Procesamiento. Def: Conversiones, compresión, encriptación.
- Cpt: Etapa 4 - Almacenamiento. Def: Guardado de datos para uso posterior.
- Cpt: Etapa 5 - Administración. Def: Gestión de calidad, seguridad y acceso.
- Cpt: Etapa 6 - Análisis. Def: Uso de datos para obtener conocimiento y tomar decisiones (requiere consolidación, resumen, modelos: ciencia de datos, minería de datos, IA, etc.).
- Cpt: Etapa 7 - Visualización. Def: Representaciones gráficas para facilitar la comprensión.
- Cpt: Etapa 8 - Interpretación. Def: Entendimiento de datos para la toma de decisiones.

## 2. Dimensiones y Criterios del MGDE

ID: GESTDAT-MGDE-DIMENSIONES-ROOT-01
Purp: Organizar las buenas prácticas del MGDE en 12 dimensiones, evaluadas por criterios.
Ctx: Cada criterio se evalúa con una o más preguntas (52 en total) para determinar el nivel de madurez.

### 2.1. Resumen de Dimensiones

ID: GESTDAT-MGDE-DIMENSIONES-RESUMEN-01
Purp: Tabla resumen de las 12 dimensiones del MGDE.

|Dimensión|N° Criterios|N° Preguntas|
|---|---|---|
|Visión estratégica|7|7|
|Gobernanza de datos|7|7|
|Arquitectura, diseño y documentación|4|6|
|Almacenamiento y operación|1|1|
|Seguridad y ciberseguridad de datos|4|6|
|Integración e interoperabilidad|2|4|
|Documentos y contenidos|4|4|
|Datos maestros y de referencia|3|3|
|Analítica e inteligencia de negocios|3|3|
|Calidad de datos|2|2|
|Datos abiertos|3|7|
|Aspectos legales y normativos|2|2|

### 2.2. Detalle de Dimensiones

ID: GESTDAT-MGDE-DIMENSIONES-DETALLE-01
Purp: Descripción de cada una de las 12 dimensiones del MGDE.

#### 2.2.1. Visión estratégica

ID: GESTDAT-MGDE-DIM-VISION-01
Purp: Generar compromiso institucional con la gestión de datos, alineada a objetivos y con visión de largo plazo.
Cpt: Criterios.

- `- Visión`
- `- Estrategia`
- `- Presupuesto y recursos`
- `- Capacidades`
- `- Gestión del cambio`
- `- Alianzas y colaboraciones`
- `- Medición y seguimiento`

#### 2.2.2. Gobernanza de datos

ID: GESTDAT-MGDE-DIM-GOBERNANZA-01
Purp: Definir visión, políticas y estrategias para potenciar los datos como activos organizacionales.
Cpt: Criterios.

- `- Política de gobernanza de datos`
- `- Organización`
- `- Implementación`
- `- Herramientas`
- `- Capacitación`
- `- Gestión de riesgos`
- `- Gestión ética de datos`

#### 2.2.3. Arquitectura, diseño y documentación

ID: GESTDAT-MGDE-DIM-ARQUITECTURA-01
Purp: Establecer modelos, documentos y metadatos que describen las estructuras y conjuntos de datos.
Cpt: Criterios.

- `- Arquitectura Institucional de datos`
- `- Catálogo de datos`
- `- Modelos y Documentación`
- `- Metadatos`
Def: Catálogo de Datos. Herramienta para crear y administrar el inventario de activos de datos de una organización. Maneja metadatos para describir/clasificar y capacidades de búsqueda para encontrar/acceder a la información.
Ex: Herramientas. CKAN (código abierto), Magda (código abierto, federado), y otras soluciones de fabricantes de software.

#### 2.2.4. Almacenamiento y operación

ID: GESTDAT-MGDE-DIM-ALMACENAMIENTO-01
Purp: Implementar y operar las plataformas de gestión de datos.
Cpt: Criterios.

- `- Gestión de la operación y almacenamiento`

#### 2.2.5. Seguridad y ciberseguridad de datos

ID: GESTDAT-MGDE-DIM-SEGURIDAD-01
Purp: Gestionar la privacidad, confidencialidad y el acceso apropiado a los datos.
Cpt: Criterios.

- `- Seguridad`
- `- Ciberseguridad`
- `- Protección de Datos Personales`
- `- Recuperación ante desastres`

#### 2.2.6. Integración e interoperabilidad

ID: GESTDAT-MGDE-DIM-INTEROP-01
Purp: Definir e implementar mecanismos para la integración y transferencia de datos (interna/externa).
Cpt: Criterios.

- `- Integración`
- `- Interoperabilidad`

#### 2.2.7. Documentos y contenidos

ID: GESTDAT-MGDE-DIM-DOCS-01
Purp: Establecer políticas y herramientas para datos no estructurados (documentos, etc.).
Cpt: Criterios.

- `- Definiciones`
- `- Metadatos`
- `- Expediente Electrónico`
- `- Repositorio Documental`

#### 2.2.8. Datos maestros y de referencia

ID: GESTDAT-MGDE-DIM-MAESTROS-01
Purp: Estandarizar codificaciones y centralizar información relevante intra e interinstitucional.
Cpt: Criterios.

- `- Datos referenciales`
- `- Datos maestros`
- `- Herramientas`

#### 2.2.9. Analítica e inteligencia de negocios

ID: GESTDAT-MGDE-DIM-ANALITICA-01
Purp: Gestionar el análisis de datos (descriptivo, diagnóstico, predictivo, prescriptivo) como apoyo a la toma de decisiones.
Cpt: Criterios.

- `- Toma de decisiones basada en información`
- `- Información de gestión`
- `- Herramientas`
Def: Data Mart. Subconjunto de bodega de datos enfocado en una línea de negocio, departamento o área temática particular.
Def: Data Lake. Repositorio centralizado para ingerir, almacenar y procesar grandes volúmenes de datos en su formato original.
Def: Data Warehouse. Repositorio centralizado que almacena datos estructurados y semiestructurados con fines de informes y análisis.

#### 2.2.10. Calidad de datos

ID: GESTDAT-MGDE-DIM-CALIDAD-01
Purp: Establecer metodologías y herramientas para definir, controlar y mejorar la calidad de los datos.
Cpt: Criterios.

- `- Definición`
- `- Metodología y Herramientas`

#### 2.2.11. Datos abiertos

ID: GESTDAT-MGDE-DIM-ABIERTOS-01
Purp: Definir e implementar procedimientos y herramientas para la publicación de datos abiertos.
Ref: Carta Internacional de Datos Abiertos.
Ref: DA-ESTANDAR-ROOT-01.
Cpt: Principios Carta Internacional Datos Abiertos.

- `- Principio 1: Abierto por defecto.`
- `- Principio 2: Oportuno y completo.`
- `- Principio 3: Accesible y utilizable.`
- `- Principio 4: Comparable e interoperable.`
- `- Principio 5: Para una mejor gobernanza y participación ciudadana.`
- `- Principio 6: Para el desarrollo inclusivo y la innovación.`
Cpt: Criterios de Evaluación.
- `- Definiciones`
- `- Publicación`
- `- Mecanismos de acceso, formato, documentación y condiciones de uso`

#### 2.2.12. Aspectos legales y normativos

ID: GESTDAT-MGDE-DIM-LEGAL-01
Purp: Establecer exigencias para el área jurídica en la definición de políticas, procedimientos y planes de cumplimiento normativo.
Cpt: Criterios.

- `- Participación del área jurídica`
- `- Cumplimiento aspectos legales y normativos`

## 3. Implementación y Evaluación

ID: GESTDAT-MGDE-IMPL-ROOT-01
Purp: Describir el modelo de madurez, método de evaluación y plan de implementación del MGDE.

### 3.1. Modelo de Madurez

ID: GESTDAT-MGDE-IMPL-MADUREZ-01
Purp: Medir el grado de desarrollo de la gestión de datos en una institución.
Cpt: Niveles de Madurez.

- `- Nivel 1 (Insuficiente): No se cumplen los mínimos deseables.`
- `- Nivel 2 (Básico): Se cumplen los mínimos deseables.`
- `- Nivel 3 (Medio): Se profundiza en cada dimensión.`
- `- Nivel 4 (Avanzado): Se aborda a cabalidad cada dimensión.`

### 3.2. Método de Autoevaluación

ID: GESTDAT-MGDE-IMPL-AUTOEVAL-01
Purp: Definir el método para que un OAE determine su nivel de madurez actual.
Mech: Matriz de evaluación (Anexo N° 1) con preguntas y respuestas por nivel.
Cpt: Cálculo de Puntajes.

- `- Mdl: Puntajes por Respuesta.
  - Insuficiente: 0
  - Básico: 2
  - Medio: 4
  - Avanzado: 6`
- `- Mdl: Intervalos por Nivel.
  - [0, 40%): Insuficiente
  - [40%, 60%): Básico
  - [60%, 80%): Medio`
- `- Mdl: Fórmulas.
  - Pje(D) = ∑Pje(Pi)
  - % Pje(D) = Pje(D) / (6 * NP(D))
  - Pje(OAE) = ∑(Pje(Dj) * P(Dj))`

### 3.3. Plan de Implementación

ID: GESTDAT-MGDE-IMPL-PLAN-01
Purp: Estructurar el proceso de implementación del MGDE en un OAE.
Cpt: Hoja de Ruta.

- `- Purp: Plan de acción para lograr el nivel de madurez esperado, priorizando dimensiones.`
- `- Req: Combinar enfoques top-down y bottom-up.`
- `- Req: Aplicado por equipo especializado con mix de competencias apropiadas.`
- `- Req: Alinear con marcos de trabajo existentes (Gestión Procesos, Calidad, Mejora Continua, TI, Transformación Digital, Gestión Documental, Arquitectura Institucional).`
- `- Def: Arquitectura Empresarial. Buenas prácticas para alinear procesos, sistemas, datos y tecnologías con objetivos estratégicos.`
- `- Def: Gestión del Cambio. Proceso para implementar nuevos modos de hacer y cambiar conductas laborales.`
Cpt: Etapas del Plan.

|Etapa|Duración Referencial|Foco|
|---|---|---|
|Etapa 1: Diagnóstico y Estrategia|4-8 meses|Autoevaluación, definir nivel esperado, elaborar hoja de ruta, priorizar 3 dims.|
|Etapa 2: Implementación Básica|8-12 meses|Implementar gobernanza y dims. priorizadas, ejecutar pilotos, re-evaluar.|
|Etapa 3: Implementación Avanzada|12-18 meses|Consolidar gobernanza, implementar mejores prácticas, evaluar y mejorar continuamente.|

Cpt: Organización y Roles.

- `- Mdl: Esquemas Orgánicos.
  - Equipos-Compartidos: Responsabilidades distribuidas (descentralizado).
  - Equipo-Dedicado: Unidad organizacional única responsable (centralizado).
  - Esquema-Mixto: Red con responsabilidades delimitadas por matriz RACI.`
- `- Rec: Instancias de Trabajo Sugeridas.
  - Comité-Directivo: Jefaturas. Provee direccionamiento, aprueba planes.
  - Comité-Ejecutivo: Jefaturas/Profesionales transversales. Propone políticas, coordina implementación.
  - Mesas-Trabajo: Profesionales. Ejecutan planificación.`
- `- Cpt: Roles Clave.
  - Director-Datos (CDO): Responsable integral de la estrategia y ejecución.
  - Admin/Custodio-Datos (Data Steward): Experto funcional, responsable de metadatos y calidad.
  - Analista-Datos (Data Analyst): Experto funcional en uso y análisis.
  - Arquitecto-Datos (Data Architect): Diseña los "planos" para la gestión de datos.`

Cpt: Ciclo de Mejora Continua.

- `- Purp: Describir el ciclo operativo de mejora continua para la gestión de datos.`
- `- Cpt: Fase 1 - Planificación. Comité Ejecutivo propone Plan Anual de Gestión de Datos al Comité Directivo.`
- `- Cpt: Fase 2 - Implementación. Comité Ejecutivo conforma Mesas de Trabajo para ejecutar el plan.`
- `- Cpt: Fase 3 - Evaluación. Anualmente se evalúa el avance del plan.`
- `- Cpt: Fase 4 - Evolución. Políticas y procesos se revisan y mejoran periódicamente.`

### 3.4. Herramientas de Apoyo

ID: GESTDAT-MGDE-IMPL-HERRAMIENTAS-01
Purp: Describir herramientas de apoyo provistas por la Secretaría de Gobierno Digital.
Cpt: Herramienta 1 - Autoevaluación Automática.

- `- Plat: Google Workspace.`
- `- Func: Permite a OAEs completar formulario, identificar nivel de madurez, y generar propuesta de hoja de ruta automáticamente.`
- `- Cpt: Formulario Google Forms, código Apps Script para procesar, informe Google Sheets con resultados y gráficos.`
Cpt: Ejemplo Resultados Autoevaluación.
- `- Ctx: Institución X.`

|Métrica Global |Puntaje Total |Puntaje Ponderado |Porcentaje |Nivel Madurez Global |
|---|---|---|---|---|
|Institución X |90 |75 |28,8% |Insuficiente |
|Puntaje Máximo |312 |260 |||

|Dimensión |Puntaje Obtenido |% Puntaje / Puntaje Avanzado |Nivel de Madurez |Ponderación |
|---|---|---|---|---|
|Visión estratégica |12 |29% |Insuficiente |8,3% |
|Gobernanza de datos |12 |29% |Insuficiente |8,3% |
|Arquitectura, diseño y documentación |4 |11% |Insuficiente |8,3% |
|Almacenamiento y operación |4 |67% |Medio |8,3% |
|Seguridad y ciberseguridad de datos |4 |11% |Insuficiente |8,3% |
|Integración e interoperabilidad |12 |50% |Básico |8,3% |
|Documentos y contenidos |4 |17% |Insuficiente |8,3% |
|Datos maestros y de referencia |10 |56% |Básico |8,3% |
|Analítica e inteligencia de negocios |6 |33% |Insuficiente |8,3% |
|Calidad de datos |0 |0% |Insuficiente |8,3% |
|Datos abiertos |22 |52% |Básico |8,3% |
|Aspectos legales y normativos |0 |0% |Insuficiente |8,3% |
