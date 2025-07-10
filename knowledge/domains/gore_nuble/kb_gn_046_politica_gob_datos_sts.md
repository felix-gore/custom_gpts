# Política de Gobernanza de Datos del Gobierno Regional de Ñuble

ID: KB-GN-046
Version: 1.0.0
Status: Draft
Human-Creator: Consultora de Estudios de Mercado y Gestión Pública
Human-Editor: FS
Model-Collaborator: IA-GEMINI
Creation-Date: 2024-10-27
Modification-Date: 2025-07-29
Primary-Source: N/A
Ref-STS-Guide: GUIDE-STS-MASTER-01

## 1. Fundamentos y Ámbito de Aplicación

ID: POL-DATAGOV-GN-FND-01

### 1.1. Propósito Estratégico

ID: POL-DATAGOV-GN-FND-PURP-01

- Purp: Transformar datos de subproducto operativo a activo estratégico.
- Obj: Fundamentar toma de decisiones basada en evidencia.
- Obj: Optimizar procesos.
- Obj: Generar valor público para habitantes de Región de Ñuble.
- Fnd: Alineado con Estrategia de Datos de la Administración del Estado. Ref: SRC-01, SRC-02.
- Just: Gobernanza de datos es prerrequisito para implementación de flota de agentes IA del GORE Ñuble.
- Req: Proveer datos de calidad, seguros y confiables para operación de agentes IA.

### 1.2. Alcance de Aplicación

ID: POL-DATAGOV-GN-FND-SCOPE-01

- Req: Aplicación obligatoria y transversal.
  - Dest: Todas las Divisiones, Departamentos, Unidades y funcionarios del GORE Ñuble.
  - Dest: Contratistas o terceros que gestionen datos en nombre de la institución.
- Ctx: Cobertura.
  - Def: Todos los datos generados, gestionados, almacenados o procesados por el GORE.
  - Cpt: Incluye formatos digitales y físicos, cualquier sistema de almacenamiento o ubicación.
- Ctx: Extensión.
  - Def: Aplica a todo el ciclo de vida de los datos.
  - Cpt: Desde creación/recolección hasta archivo/eliminación segura.

### 1.3. Marco Normativo y Estratégico

ID: POL-DATAGOV-GN-FND-FRAMEWORK-01

- Fnd: Marco legal y estratégico vigente en Chile para gestión y protección de datos.
- Cpt: Base Legal Primaria.
  - Def: Ley N° 19.628 sobre Protección de la Vida Privada. Ref: SRC-03.
  - Ctx: Regula tratamiento de datos personales por organismos públicos.
- Cpt: Base Estratégica Nacional.
  - Def: Marco para la Gestión de Datos del Estado (MGDE). Ref: SRC-05.
  - Ctx: Impulsado por Secretaría de Gobierno Digital.
  - Ctx: Adapta prácticas internacionales (DAMA) al sector público chileno.
- Cpt: Contexto de Infraestructura.
  - Def: Plan Nacional de Data Centers. Ref: SRC-06.
  - Purp: Fortalecer infraestructura digital del país.
  - Purp: Habilitar gestión de datos robusta, segura y sostenible.
- Cpt: Implicancia de Adopción.
  - Res: GORE Ñuble se posiciona como adoptante temprano de estándares nacionales emergentes.
  - Res: Facilita interoperabilidad futura con otros organismos del Estado.
  - Res: Asegura alineación con dirección estratégica nacional en transformación digital.
  - Res: Prepara la institución para integración fluida con futuras herramientas y plataformas. Ref: SRC-05.

## 2. Principios Rectores

ID: POL-DATAGOV-GN-PRINCIPLES-01

- Cpt: Principio 1: Dato como Activo Estratégico.
  - Def: Datos son un recurso institucional valioso, propiedad del GORE Ñuble.
  - Req: Su gestión, protección y explotación deben ser planificadas con rigor.
  - Just: Justifica inversión en recursos (humanos, tecnológicos, procesos) para maximizar su valor.
- Cpt: Principio 2: Licitud y Finalidad.
  - Req: Todo tratamiento de datos debe tener base de licitud clara.
  - Req: Fines deben ser específicos, explícitos y legítimos.
  - Fnd: Derivado de artículos 4, 9 y 20 de la Ley N° 19.628. Ref: SRC-04.
  - Prohib: Recolectar y usar datos para fines distintos a los informados o establecidos por ley.
- Cpt: Principio 3: Calidad de los Datos.
  - Req: Datos deben ser exactos, actualizados, completos y consistentes.
  - Fnd: Basado en artículo 9 de la Ley N° 19.628. Ref: SRC-04.
  - Dep: Calidad es prerrequisito para que el dato sea un activo estratégico.
  - Warn: Datos sin calidad pueden inducir a decisiones erróneas.
- Cpt: Principio 4: Seguridad y Confidencialidad.
  - Req: Implementar medidas técnicas y organizativas para proteger los datos.
  - Fnd: Mandatado por artículos 7 y 11 de la Ley N° 19.628. Ref: SRC-04.
  - Ctx: Incluye seguridad de infraestructura (Data Custodian) y obligación de confidencialidad (todos los usuarios).
- Cpt: Principio 5: Responsabilidad Proactiva (Accountability).
  - Req: El GORE debe ser capaz de demostrar cumplimiento de la política y la ley.
  - Mech: Documentación de políticas, asignación de responsabilidades, registro de actividades, evaluaciones periódicas.
  - Just: Genera confianza en ciudadanía, órganos de control y otros organismos del Estado.
- Cpt: Principio 6: Privacidad desde el Diseño y por Defecto.
  - Req: Protección de datos debe ser componente integral en el diseño de nuevos sistemas y procesos.
  - Fnd: Buena práctica promovida por el Consejo para la Transparencia. Ref: SRC-09.
  - Ctx: Adopción prepara al GORE para futuras leyes más exigentes y mitiga riesgo de obsolescencia. Ref: SRC-11.

## 3. Modelo de Gobernanza: Roles y Responsabilidades

ID: POL-DATAGOV-GN-MODEL-01

### 3.1. Estructura de Roles

ID: POL-DATAGOV-GN-MODEL-ROLES-STRUCT-01

- Mdl: Adopta modelo de tres niveles basado en framework DAMA. Ref: SRC-13.
- Purp: Asegurar clara separación de responsabilidades (estratégicas, tácticas, operacionales).

### 3.2. Definición de Roles

ID: POL-DATAGOV-GN-MODEL-ROLES-DEF-01

- Cpt: Rol: Data Owner (Dueño del Dato).
  - Def: Ejecutivo de alto nivel (Jefe/a de División) con máxima autoridad sobre un dominio de datos.
  - Resp: Calidad, seguridad y valor de negocio de los datos en su dominio. Ref: SRC-14.
  - Ctx: Enfoque estratégico.
  - Act: Aprobar políticas de acceso.
  - Act: Definir reglas de calidad de datos.
  - Act: Autorizar clasificación de la información.
- Cpt: Rol: Data Steward (Custodio Funcional).
  - Def: Experto en la materia (Jefe/a de Departamento o profesional) que gestiona activos de datos.
  - Resp: Gestión táctica y del día a día de los datos. Ref: SRC-15.
  - Ctx: Enfoque táctico y de negocio.
  - Act: Definir y mantener metadatos.
  - Act: Monitorear y reportar calidad de datos.
- Cpt: Rol: Data Custodian (Custodio Técnico).
  - Def: Rol técnico (Unidad TIC) responsable de la infraestructura y sistemas.
  - Resp: Ejecuta las políticas definidas por Owners y Stewards.
  - Ctx: Enfoque operacional y tecnológico.
  - Act: Implementar controles de acceso técnico.
  - Act: Realizar respaldos y recuperaciones.

### 3.3. Estructura de Gobierno

ID: POL-DATAGOV-GN-MODEL-GOV-01

- Cpt: Comité de Gobernanza de Datos.
  - Purp: Instancia formal de coordinación y toma de decisiones estratégicas.
  - Resp: Presidido por Administrador/a Regional.
  - Cpt: Integrantes. Def: Todos los Data Owners y Jefe de Unidad TIC.
  - Ctx: Frecuencia. Def: Reuniones ordinarias trimestrales.
  - Fnd: Mitiga riesgo de que prioridades de una división (DAF) primen sobre las necesidades de toda la organización. Ref: SRC-16.

### 3.4. Mapeo de Dominios de Datos a Data Owners

ID: POL-DATAGOV-GN-MODEL-MAP-01

- Req: Se asignan dominios de datos a roles de Data Owner según estructura orgánica. Ref: SRC-16.

| Dominio de Datos | Descripción del Dominio | Data Owner (Cargo Responsable) |
|-|-|-|
| Proyectos y Presupuesto | Cpt: BIP, FNDR, ejecución presupuestaria. | Jefe/a, División de Presupuesto e Inversión Regional |
| Beneficiarios | Cpt: Personas (naturales/jurídicas) receptoras de subvenciones. | Jefe/a, División de Desarrollo Social y Humano |
| Finanzas y Proveedores | Cpt: Facturas, decretos de pago, proveedores, contabilidad (SIGFE). | Jefe/a, División de Administración y Finanzas |
| Funcionarios | Cpt: Personal, remuneraciones, desarrollo de personas. | Jefe/a, División de Administración y Finanzas |
| Planificación Territorial| Cpt: Geoespaciales, planes reguladores, instrumentos de ordenamiento. | Jefe/a, División de Planificación y Desarrollo Regional |
| Fomento Productivo | Cpt: Empresas, proyectos de innovación, desarrollo económico. | Jefe/a, División de Fomento e Industria |
| Infraestructura | Cpt: Proyectos de vialidad, transporte, telecomunicaciones. | Jefe/a, División de Infraestructura y Transportes |

## 4. Lineamientos para la Calidad de Datos

ID: POL-DATAGOV-GN-QUALITY-01

- Req: Data Stewards son responsables de implementar y monitorear estas dimensiones.
- Cpt: Dimensión: Exactitud.
  - Req: Datos deben reflejar correctamente el objeto o evento del mundo real.
- Cpt: Dimensión: Completitud.
  - Req: Identificar atributos críticos y impedir registros incompletos en ellos.
- Cpt: Dimensión: Consistencia.
  - Req: Usar formatos estandarizados y catálogos de datos maestros.
- Cpt: Dimensión: Actualidad (Timeliness).
  - Req: Definir y documentar la frecuencia de actualización requerida.
- Cpt: Dimensión: Unicidad.
  - Prohib: Creación de registros duplicados para una misma entidad.
- Cpt: Dimensión: Validez.
  - Req: Valores deben ajustarse a dominios y reglas de negocio predefinidos.
- Cpt: Enfoque de Proceso.
  - Def: Gestión de calidad de datos es un proceso continuo, no un proyecto.

## 5. Lineamientos para la Seguridad y Protección de Datos

ID: POL-DATAGOV-GN-SECURITY-01

### 5.1. Clasificación de la Información

ID: POL-DATAGOV-GN-SEC-CLASSIFY-01

- Req: Todo activo de información debe ser clasificado por su Data Owner.
- Cpt: Categorías.
  - Def: Público.
  - Def: Interno.
  - Def: Confidencial.
  - Def: Sensible. Ref: SRC-09.
- Just: Permite aplicar controles de seguridad proporcionales al riesgo.

### 5.2. Control de Acceso Basado en Rol (RBAC)

ID: POL-DATAGOV-GN-SEC-RBAC-01

- Cpt: Principio. Def: Mínimo privilegio.
- Req: Acceso se concede en función del rol y responsabilidades.
- Proc: Data Steward define perfiles; Data Custodian los implementa.
- Req: Permisos deben ser revisados periódicamente (mínimo anual).

### 5.3. Tratamiento de Datos Personales y Sensibles

ID: POL-DATAGOV-GN-SEC-PERSONAL-01

- Req: Cumplir estrictamente con Ley N° 19.628. Ref: SRC-03.
- Cpt: Deber de Información.
  - Req: Informar al titular sobre finalidad del tratamiento al recolectar datos. Ref: SRC-09.
- Cpt: Tratamiento de Datos Sensibles.
  - Prohib: Tratamiento de datos sensibles salvo excepciones legales. Ref: SRC-09.
- Cpt: Deber de Secreto.
  - Req: Todo funcionario que trate datos personales está obligado a guardar secreto. Ref: SRC-04.

### 5.4. Seguridad en el Ciclo de Vida del Dato

ID: POL-DATAGOV-GN-SEC-LIFECYCLE-01

- Cpt: Fases.
  - Recolección: Usar canales seguros.
  - Almacenamiento: Cifrar datos Confidenciales o Sensibles en reposo.
  - Transmisión: Usar protocolos cifrados (HTTPS, SFTP).
  - Eliminación: Usar métodos de borrado seguro. Ref: SRC-11.

### 5.5. Gestión de Incidentes de Seguridad

ID: POL-DATAGOV-GN-SEC-INCIDENTS-01

- Resp: Unidad TIC (Data Custodian) debe desarrollar y mantener Plan de Respuesta a Incidentes.
- Req: Plan debe incluir procedimientos para detección, notificación, contención, análisis y recuperación.

## 6. Fuentes Citadas

ID: POL-DATAGOV-GN-SOURCES-01

- ID: SRC-01
  Cpt: Estrategia de Datos del Gobierno.
  Src: <https://digital.gob.cl/biblioteca/estrategias/estrategias-de-datos-del-gobierno/>
- ID: SRC-02
  Cpt: Estrategia de Datos de la Administración del Estado | Wiki Guías.
  Src: <https://wikiguias.digital.gob.cl/Estrategias/Estrategia_Datos>
- ID: SRC-03
  Cpt: Ley N° 19.628, sobre protección de la vida privada - Gobierno Digital.
  Src: <https://digital.gob.cl/biblioteca/regulacion/ley-n-19628-sobre-proteccion-de-la-vida-privada/>
- ID: SRC-04
  Cpt: Ley 19628 - Biblioteca del Congreso Nacional de Chile - BCN.
  Src: <https://www.bcn.cl/leychile/navegar?idNorma=141599>
- ID: SRC-05
  Cpt: Marco de Referencia de Datos del Estado (MGDE) - GobLab UAI.
  Src: <https://goblab.uai.cl/marco-de-referencia-de-datos-del-estado-mgde/>
- ID: SRC-06
  Cpt: Plan Nacional de Data Centers - Ministerio de Ciencia, Tecnología, Conocimiento e Innovación.
  Src: <https://minciencia.gob.cl/uploads/filer_public/95/6b/956b8c9f-d937-4b4d-8f6c-a871495a52ff/plan_nacional_de_data_centers_pdata.pdf>
- ID: SRC-07
  Cpt: Hub Digital: Chile lanza Plan Nacional de Data Centers - InvestChile Blog.
  Src: <https://blog.investchile.gob.cl/bloges/plan-nacional-data-centers-chile>
- ID: SRC-08
  Cpt: GobLab inicia proyecto de elaboración de marco de referencia de datos para el Estado.
  Src: <https://goblab.uai.cl/goblab-inicia-proyecto-de-elaboracion-de-marco-de-referencia-de-datos-para-la-dgd/>
- ID: SRC-09
  Cpt: GUIA PROTECCIÓN DATOS PERSONALES PARA INSTITUCIONES PÚBLICAS.
  Src: <https://www.consejotransparencia.cl/wp-content/uploads/instruccion/2024/05/Guia-proteccio%CC%81n-datos-personales-para-instituciones-pu%CC%81blicas.pdf>
- ID: SRC-10
  Cpt: Compromiso 10 – Política de Datos Abiertos y Protección de Datos.
  Src: <https://www.ogp.gob.cl/compromisos/c8-politica-de-datos-abiertos-y-proteccion-de-datos/>
- ID: SRC-11
  Cpt: Guía Completa Ley 19.628 de Chile. Protección de Datos Personales - Delete Technology.
  Src: <https://www.deletetechnology.com/blog/gu%C3%ADa-completa-ley-19.628-de-chile.-protecci%C3%B3n-de-datos-personales>
- ID: SRC-12
  Cpt: LEY 19.628 SOBRE PROTECCIÓN DE LOS DATOS PERSONALES - Bitlaw.
  Src: <https://bitlaw.cl/ley-19-628-sobre-proteccion-de-los-datos-personales/>
- ID: SRC-13
  Cpt: ¿Qué es el Gobierno de Datos (Data Governance) y para qué sirve? - Enigmia.
  Src: <https://enigmia.es/noticias/gobierno-de-datos-data-governance/>
- ID: SRC-14
  Cpt: DO (Data Owner) - Data Universe.
  Src: <https://data-universe.org/do-data-owner/>
- ID: SRC-15
  Cpt: Gobierno de procesos cloud - Universidad Pontificia Comillas.
  Src: <https://repositorio.comillas.edu/xmlui/bitstream/handle/11531/55148/TFM%20-%20Ocon%20Galilea%2C%20Alicia.pdf?sequence=1>
- ID: SRC-16
  Cpt: Organigrama Final - Gobierno Regional de Ñuble.
  Src: <https://goredenuble.cl/wp-content/themes/portal/elementos/interactivos/Organigrama.pdf>
- ID: SRC-17
  Cpt: El Gobierno Regional de Ñuble (GORE) es el encargado de la administración superior de la Región.
  Src: <https://goredenuble.cl/gobiernoregional/>
