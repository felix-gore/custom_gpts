# Guía Técnica: Metadatos para Documentos y Expedientes Electrónicos

Version: 1.0.0
Status: Draft
Human-Creator: STSador
Human-Editor: STSador
Model-Collaborator: IA-GEMINI
Creation-Date: 2025-07-06
Modification-Date: 2025-07-06
Primary-Source: kb_064_tde_guia_metadatos_docs.md
Ref-STS-Guide: GUIDE-STS-MASTER-01

ID: GDE-META-ROOT-01
Purp: Definir metadatos (obligatorios, condicionales, sugeridos) para la gestión e interoperabilidad de documentos y expedientes electrónicos de los Órganos de la Administración del Estado (OAE).

## 1. Introducción y Fundamentos

ID: GDE-META-INTRO-01
Purp: Establecer el contexto legal, normativo y técnico para el uso de metadatos en la gestión documental del Estado.

### Contexto Legal y Normativo

ID: GDE-META-INTRO-LEGAL-01
Fnd: Ley N° 21.180 (Transformación Digital del Estado).

- Cpt: Modificación. Act: Modifica Ley N° 19.880.
- Cpt: Obj-Modificación. Purp: Incorporar digitalización y transformación del ciclo de procedimientos administrativos.
Fnd: Decreto Supremo N° 4, 2020, MINSEGPRES.
- Cpt: Obj-Reglamento. Purp: Regular expresión de procedimientos administrativos por medios electrónicos.
- Cpt: Mandato-Reglamento. Req: Dictar 6 normas técnicas (interoperabilidad, seguridad, docs/expedientes, notificaciones, calidad, autenticación).
Fnd: Decreto Supremo N° 10, 2023, MINSEGPRES.
- Cpt: Obj-Norma. Purp: Establecer norma técnica de documentos y expedientes electrónicos.
- Cpt: Dependencia. Def: Esta guía técnica facilita la implementación de dicha norma.
Req: Para correcta interpretación, seguir definiciones del Art. 2° de la Norma Técnica de Documentos y Expedientes Electrónicos.

### Base de Buenas Prácticas

ID: GDE-META-INTRO-PRACTICAS-01
Purp: Fundamentar la guía en estándares internacionales.
Fnd: Base Normativa ISO.

- Ref: `ISO-15489`. Ctx: Gestión de documentos.
  - Purp: Asegurar protección de docs; permitir recuperación normalizada y eficaz de info.
- Ref: `ISO-23081`. Ctx: Metadatos para gestión de docs.
  - Purp: Proporcionar orientación sobre principios y elementos para implantar/evaluar conjuntos de metadatos.
Ref: Otros-Estandares.
- Cpt: `Australian-Government-Recordkeeping-Metadata-Standard`
- Cpt: `e-EMGDE` (Esquema de Metadatos para la Gestión del Documento Electrónico) de España.
Cpt: Proyeccion. Act: Versiones futuras de la norma y guía se incorporarán según avance del cumplimiento.

### Principios de Gestión de Metadatos

ID: GDE-META-INTRO-PRINCIPIOS-01
Purp: Definir los principios rectores de los metadatos en el ciclo de vida documental.
Cpt: Rol-Metadatos. Fnd: Fundamental para descripción precisa, gestión, tramitación, interoperabilidad y eficiencia.
Cpt: Indivisibilidad. Def: Metadatos son parte indivisible de la identidad de expedientes y documentos.
Cpt: Funcion-Descriptiva. Act: Proporcionan info sobre estructura, contenido y contexto (autor, fecha, lugar).
Obj: Garantizar disponibilidad, recuperación, accesibilidad, conservación e interoperabilidad.
Cpt: Ciclo-Vida. Def: Metadatos se incorporan y enriquecen a lo largo de las etapas del procedimiento.

- Req: Inclusión desde creación, durante gestión, hasta transferencia a Archivo Nacional.
Cpt: Persistencia. Def: Metadatos son de registro permanente.
- Req: Deben conservarse sin sobrescribirse, resguardados por el organismo custodio.
Cpt: Implementacion-OAE. Def: Cada institución dispone cómo implementar el registro (repositorios, BBDD, etc.).
- Req: Obligatoria la existencia de metadatos asociados a cada doc/expediente.
- Req: Obligatoria su generación en formato estandarizado para interoperabilidad.

## 2. Esquema General de Metadatos

ID: GDE-META-ESQUEMA-ROOT-01
Purp: Presentar la estructura y resumen cuantitativo de los metadatos para expedientes y documentos.

### Estructura y Entidades

ID: GDE-META-ESQUEMA-ENTIDADES-01
Mdl: Entidad-Relación.
Cpt: Entidades-Principales.

- `Documento`
- `Expediente`
- `Actor`: Institución, persona física/jurídica responsable o involucrada.
- `Relacion`: Asociación entre dos o más entidades.
Cpt: Multiplicidad. Def: Esquema permite relaciones múltiples entre expediente/documento y actores.

### Cuantificación del Esquema

ID: GDE-META-ESQUEMA-CUANT-01
Cpt: Total-Elementos-Expediente. Res: 29.

- `Obligatorios`: 18.
- `Condicionales`: 5.
- `Sugeridos`: 6.
Cpt: Total-Elementos-Documento. Res: 46.
- `Obligatorios`: 12.
- `Condicionales`: 16.
- `Sugeridos`: 18.

### Leyenda de Clasificación

ID: GDE-META-ESQUEMA-LEYENDA-01
Purp: Definir la simbología usada en las tablas de metadatos.

- Cpt: `Color-Verde`. Def: Metadato Obligatorio.
- Cpt: `Color-Amarillo`. Def: Metadato Condicional (obligatorio si se cumple condición).
- Cpt: `Color-Blanco`. Def: Metadato Sugerido (pertinencia a discreción del OAE).
- Cpt: `AN`. Def: Metadato requerido por Archivo Nacional para transferencia digital.
- Cpt: `MU`. Def: Metadato múltiple (permite múltiples registros).

## 3. Metadatos para Expedientes Electrónicos

ID: GDE-META-EXPEDIENTES-ROOT-01
Purp: Definir el conjunto de metadatos aplicables a un expediente electrónico.

### Tabla Resumen: Metadatos de Expedientes

ID: GDE-META-EXPEDIENTES-TABLA-01

| Codificación | N° | Sub N° | Grupo/Rótulo | Definición | Flags |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | | | Identificación | Def: Info de identificación unívoca del expediente. | |
| MGDEE1_1 | 1 | 1.1 | Identificador de expediente | Def: Número único (ID) asignado auto a un expediente. | `AN` |
| MGDEE1_2 | 2 | 1.2 | Código serie | Def: Código serie del cuadro de clasificación documental del OAE. | |
| MGDEE1_3 | 3 | 1.3 | Número del expediente | Def: N° de orden interno dentro de una serie documental. | |
| MGDEE1_4 | 4 | 1.4 | Estado | Def: Estado de generación del expediente por el OAE productor. | |
| MGDEE1_5 | 5 | 1.5 | Título del expediente | Def: Palabra/frase para denominar el expediente (formal o atribuido). | `AN` |
| 2 | | | Descripción | Def: Texto referencial del contenido global. | |
| MGDEE2_1 | 6 | 2.1 | Resumen | Def: Relato sintético del contenido global del expediente. | |
| MGDEE2_2 | 7 | 2.2 | Asunto del expediente | Def: Materia/tema que trata, reflejo de los fines perseguidos. | `AN` |
| 3 | | | Temporalidad | Def: Atributos de tiempo específicos. | |
| MGDEE3_1 | 8 | 3.1 | Fecha de creación | Def: Fecha en que es generado el expediente. | `AN` |
| MGDEE3_2 | 9 | 3.2 | Fecha de finalización | Def: Fecha de finalización o cierre del expediente. | `AN` |
| 4 | | | Caracterización documental | Def: Identificación por tipo de expediente. | |
| MGDEE4_1 | 10 | 4.1 | Mecanismo de incorporación | Def: Cómo se incorporó al sistema de gestión documental. | |
| MGDEE4_2 | 11 | 4.2 | URI de expediente | Def: Enlace a expediente en repositorio/plataforma. | |
| 5 | | | Relaciones | Def: Relaciones del expediente con OAE o personas. | |
| | | 5.1 | OAE Asociado | Def: Identificación de relaciones con OAEs. | |
| MGDEE51_1 | 12 | 5.1.1 | Código de OAE productor | Def: OAE que genera el expediente en cumplimiento de sus funciones. | `AN` |
| MGDEE51_2 | 13 | 5.1.2 | Nombre OAE productor | Def: Nombre institucional si OAE no está en codificador. | |
| MGDEE51_3 | 14 | 5.1.3 | Tipo Relación OAE | Def: Relación entre el expediente y el OAE. | `MU` |
| MGDEE51_4 | 15 | 5.1.4 | Código de OAE relacionado | Def: OAE que custodia, respalda o está involucrado. | `MU` |
| MGDEE51_5 | 16 | 5.1.5 | Nombre OAE relacionado | Def: Nombre institucional si OAE relacionado no está en codificador. | `MU` |
| | | 5.2 | Otros actores | Def: Relaciones del expediente con otros actores. | |
| MGDEE52_1 | 17 | 5.2.1 | Tipo de relación otros actores | Def: Tipo de relación existente con el actor y el expediente. | `MU` |
| MGDEE52_2 | 18 | 5.2.2 | Tipo de actor relacionado | Def: Identifica tipo de actor para determinar pertinencia de ID. | `MU` |
| MGDEE52_3 | 19 | 5.2.3 | RUN/RUT relacionado | Def: RUN/RUT/Pasaporte del actor relacionado. | `MU` |
| MGDEE52_4 | 20 | 5.2.4 | Nombre del actor relacionado | Def: Nombre si no se cuenta con RUN/RUT. | `MU` |
| | | 5.3 | Índice de Documentos Asociados| Def: Docs/expedientes que forman parte del presente expediente. | |
| MGDEE53_1 | 21 | 5.3.1 | Identificador vinculado | Def: ID del expediente o documento que conforma el presente exp. | `AN, MU` |
| MGDEE53_2 | 22 | 5.3.2 | Fecha de incorporación | Def: Fecha/hora en que se incorpora el doc/exp vinculado. | `AN, MU` |
| 6 | | | Seguridad | Def: Niveles de seguridad para la gestión del expediente. | |
| MGDEE6_1 | 23 | 6.1 | Nivel de acceso | Def: Indicación relativa al acceso y consulta del expediente. | `AN` |
| MGDEE6_2 | 24 | 6.2 | Fecha fin restricción | Def: Fecha que determina el desbloqueo del expediente. | |
| MGDEE6_3 | 25 | 6.3 | Texto Advertencia | Def: Texto a presentar si un usuario intenta acceder. | |
| MGDEE6_4 | 26 | 6.4 | Carácter sensible/privado | Def: Identificación si contiene info sensible/privada. | |
| 7 | | | Procedimiento asociado | Def: Identificación del Procedimiento Administrativo. | |
| MGDEE7_1 | 27 | 7.1 | Código CPAT asociado | Def: Código del procedimiento en Catálogo de Proc. Adm. y Tram. (CPAT). | |
| MGDEE7_2 | 28 | 7.2 | Nombre procedimiento asociado | Def: Nombre del procedimiento si no está en CPAT. | |
| 8 | | | Versión | Def: Identificación de la versión del esquema. | |
| MGDEE8_1 | 29 | 8.1 | Versión MDGEE | Def: Versión del esquema de metadatos utilizado. | |

### Especificaciones Detalladas: Metadatos de Expedientes

ID: GDE-META-EXPEDIENTES-ESPECIFICACIONES-01
Purp: Detallar cada metadato para expedientes.
Ref: AUDIT-ETE-INFORME-01

#### 1. Identificador de expediente (MGDEE1_1)

ID: GDE-META-EXP-SPEC-01
Ref: MGDEE1_1
Mech: Automático. Sistema asigna ID único institucional para acceso.
Cpt: Tipo-Dato. Def: Alfanumérico.
Ctx: Asegurar unicidad, persistencia y estandarización de codificación.
Ex: `EXP-20230925-001`

#### 2. Código serie (MGDEE1_2)

ID: GDE-META-EXP-SPEC-02
Ref: MGDEE1_2
Mech: Automático. Sistema asigna código de serie a cada expediente creado.
Cpt: Tipo-Dato. Def: Alfanumérico.

#### 3. Número del expediente (MGDEE1_3)

ID: GDE-META-EXP-SPEC-03
Ref: MGDEE1_3
Mech: Automático. Sistema asigna número de orden interno dentro de una serie documental.
Cpt: Tipo-Dato. Def: Alfanumérico.

#### 4. Estado (MGDEE1_4)

ID: GDE-META-EXP-SPEC-04
Ref: MGDEE1_4
Mech: Automático/Manual. Generado por sistema o manualmente para reflejar estado.
Cpt: Tipo-Dato. Def: Alfanumérico.
Ctx: Puede referirse al estado de creación o fase del ciclo de vida.

#### 5. Título del expediente (MGDEE1_5)

ID: GDE-META-EXP-SPEC-05
Ref: MGDEE1_5
Mech: Manual. Título formal adjudicado por creador; puede ser automatizable.
Cpt: Tipo-Dato. Def: Texto.
Ctx: Usar mayúsculas solo al inicio y en nombres propios.
Ex: `Asignación de presupuesto para compra de insumos.`

#### 6. Resumen (MGDEE2_1)

ID: GDE-META-EXP-SPEC-06
Ref: MGDEE2_1
Mech: Manual.
Cpt: Tipo-Dato. Def: Texto.

#### 7. Asunto del expediente (MGDEE2_2)

ID: GDE-META-EXP-SPEC-07
Ref: MGDEE2_2
Mech: Manual y/o desde vocabulario controlado para destacar materia no extraíble de otros metadatos.
Cpt: Tipo-Dato. Def: Texto.
Ctx: Representa el contenido amplio del expediente.
Ex: `Compra de insumos tecnológicos para el año 2023.`

#### 8. Fecha de creación (MGDEE3_1)

ID: GDE-META-EXP-SPEC-08
Ref: MGDEE3_1
Mech: Automático. Generado según formato `aaaa-mm-dd hh:mm:ss` (ISO 8601).
Cpt: Tipo-Dato. Def: Fecha/Hora (ISO 8601).
Ctx: Debe permitir modificación, pero registrando el cambio.
Ex: `2023-20-10:11:56:57`

#### 9. Fecha de finalización (MGDEE3_2)

ID: GDE-META-EXP-SPEC-09
Ref: MGDEE3_2
Mech: Automático. Generado según formato `aaaa-mm-dd hh:mm:ss` (ISO 8601).
Cpt: Tipo-Dato. Def: Fecha/Hora (ISO 8601).
Ctx: Debe permitir modificación, pero registrando el cambio.
Ex: `2023-20-11:16:56:57`

#### 10. Mecanismo de incorporación de expediente (MGDEE4_1)

ID: GDE-META-EXP-SPEC-10
Ref: MGDEE4_1
Mech: Automático/Manual. Seleccionar de lista controlada. Ref: `GDE-META-LISTAS-MEC-INCORP-01`.
Cpt: Tipo-Dato. Def: Texto.
Cpt: Valor-Defecto. Def: 1 (Incorporación manual).
Ex: `1`

#### 11. URI de expediente (MGDEE4_2)

ID: GDE-META-EXP-SPEC-11
Ref: MGDEE4_2
Mech: Automático. Generado automáticamente por la plataforma.
Cpt: Tipo-Dato. Def: URI.
Ctx: Institución puede usar servicios propios de URIs persistentes o los que disponga el Estado.
Ex: `https://dominio-institución/servicio-persistente/20.500.13034/401`

#### 12. Código de OAE productor (MGDEE51_1)

ID: GDE-META-EXP-SPEC-12
Ref: MGDEE51_1
Mech: Automático. Sistema incorpora código y nombre del productor desde Gestor de Códigos (GESCODE).
Cpt: Tipo-Dato. Def: Numérico.
Ctx: Valor requerido por Archivo Nacional (AN).
Ex: `46` (Gobierno Regional de la Región de La Araucanía)

#### 13. Nombre OAE productor (MGDEE51_2)

ID: GDE-META-EXP-SPEC-13
Ref: MGDEE51_2
Mech: Automático/Manual.
Cond: Requerido si OAE productor no está registrado en GESCODE.
Cpt: Forma-Ingreso. Def: Registro manual del nombre institucional.
Cpt: Tipo-Dato. Def: Texto.
Ex: `Gobierno Regional de la Región de La Araucanía`

#### 14. Tipo Relación OAE (MGDEE51_3)

ID: GDE-META-EXP-SPEC-14
Ref: MGDEE51_3
Mech: Automático/Manual. Selección de lista predefinida. Ref: `GDE-META-LISTAS-TIPO-REL-OAE-01`.
Cpt: Tipo-Dato. Def: Numérico.
Ctx: Obligatorio identificar al menos OAE custodio.
Cpt: Valor-Defecto. Def: 1 (custodia).
Ex: `1`

#### 15. Código de OAE relacionado (MGDEE51_4)

ID: GDE-META-EXP-SPEC-15
Ref: MGDEE51_4
Mech: Automático/Manual. Código desde Gestor de Códigos (GESCODE).
Cpt: Tipo-Dato. Def: Numérico.
Ctx: Obligatorio identificar al menos OAE custodio.
Ex: `46` (Gobierno Regional de la Región de La Araucanía)

#### 16. Nombre de OAE relacionado (MGDEE51_5)

ID: GDE-META-EXP-SPEC-16
Ref: MGDEE51_5
Mech: Automático/Manual.
Cond: Requerido si OAE relacionado no está registrado en GESCODE.
Cpt: Forma-Ingreso. Def: Registro manual del nombre institucional.
Cpt: Tipo-Dato. Def: Texto.
Ex: `Gobierno Regional de la Región de La Araucanía`

#### 17. Tipo de relación con otros actores (MGDEE52_1)

ID: GDE-META-EXP-SPEC-17
Ref: MGDEE52_1
Mech: Automático/Manual.
Cond: Obligatorio para identificación de interesados.
Cpt: Forma-Ingreso. Def: Selección de lista predefinida. Ref: `GDE-META-LISTAS-TIPO-REL-ACTORES-01`.
Cpt: Tipo-Dato. Def: Numérico.
Ctx: Obligatorio asignar al menos un funcionario responsable. Campo múltiple.
Cpt: Valor-Defecto. Def: 1 (Responsable).
Ex: `2` (Interesado)

#### 18. Tipo de actor relacionado (MGDEE52_2)

ID: GDE-META-EXP-SPEC-18
Ref: MGDEE52_2
Mech: Automático/Manual.
Cond: Obligatorio para identificación de interesados.
Cpt: Forma-Ingreso. Def: Selección de lista predefinida. Ref: `GDE-META-LISTAS-TIPO-ACTOR-01`.
Cpt: Tipo-Dato. Def: Numérico.
Ctx: Obligatorio especificar el funcionario responsable inicial.
Cpt: Valor-Defecto. Def: 4 (Funcionario).
Ex: `1` (Ciudadano)

#### 19. RUN/RUT Relacionado (MGDEE52_3)

ID: GDE-META-EXP-SPEC-19
Ref: MGDEE52_3
Mech: Automático/Manual.
Cond: Obligatorio para identificación de interesados.
Cpt: Forma-Ingreso. Def: Registro al momento de identificar al actor (RUN/RUT/Pasaporte).
Cpt: Tipo-Dato. Def: Alfanumérico.
Ex: `60100003-2`

#### 20. Nombre del actor relacionado (MGDEE52_4)

ID: GDE-META-EXP-SPEC-20
Ref: MGDEE52_4
Mech: Automático/Manual.
Cond: Obligatorio para interesados si no se cuenta con RUN/RUT/Pasaporte.
Cpt: Forma-Ingreso. Def: Registro del nombre de la persona natural o jurídica.
Cpt: Tipo-Dato. Def: Texto.
Ex: `Entel Chile`, `Julian Santelices Machuca`

#### 21. Identificador de expediente/documento vinculado (MGDEE53_1)

ID: GDE-META-EXP-SPEC-21
Ref: MGDEE53_1
Mech: Automático. Sistema registra ID o URI de docs/expedientes incorporados al índice.
Cpt: Tipo-Dato. Def: Alfanumérico.
Ctx: Requerido si el documento forma parte de un expediente.

#### 22. Fecha de la incorporación del expediente / documento (MGDEE53_2)

ID: GDE-META-EXP-SPEC-22
Ref: MGDEE53_2
Mech: Automático. Sistema registra fecha/hora de incorporación (`aaaa-mm-dd hh:mm:ss`).
Cpt: Tipo-Dato. Def: Fecha/Hora (ISO 8601).
Ex: `2023-20-11:16:56:57`

#### 23. Nivel de acceso (MGDEE6_1)

ID: GDE-META-EXP-SPEC-23
Ref: MGDEE6_1
Mech: Manual. Selección de lista controlada o asociación automática por tipo de expediente según política institucional. Ref: `GDE-META-LISTAS-NIVEL-ACCESO-01`.
Cpt: Tipo-Dato. Def: Numérico.
Cpt: Valor-Defecto. Def: 1 (Público).
Ex: `1`

#### 24. Fecha fin restricción (MGDEE6_2)

ID: GDE-META-EXP-SPEC-24
Ref: MGDEE6_2
Mech: Manual. Ingreso manual de fecha de desbloqueo.
Cpt: Tipo-Dato. Def: Fecha.

#### 25. Texto de advertencia (MGDEE6_3)

ID: GDE-META-EXP-SPEC-25
Ref: MGDEE6_3
Mech: Manual. Ingreso manual del texto a presentar.
Cpt: Tipo-Dato. Def: Texto.

#### 26. Información de carácter sensible y/o privado (MGDEE6_4)

ID: GDE-META-EXP-SPEC-26
Ref: MGDEE6_4
Mech: Manual. Plataforma OAE debe tener registro de marca (Sí/No).
Cpt: Tipo-Dato. Def: Numérico (Lista Controlada `1-SI / 2-NO`).
Ctx: OAE puede definir categorías controladas para este tipo de info.
Cpt: Valor-Defecto. Def: 2 (NO).
Ex: `2`

#### 27. Código CPAT asociado (MGDEE7_1)

ID: GDE-META-EXP-SPEC-27
Ref: MGDEE7_1
Mech: Automático. Código desde Catálogo de Procedimientos Administrativos y Tramitaciones (CPAT).
Cpt: Tipo-Dato. Def: Alfanumérico.
Ctx: Disponibilizado por CPAT.
Ex: `5076 (PA-UNI00002-00001- Convalidación de Programa de Perfeccionamiento Académico)`

#### 28. Nombre del procedimiento administrativo asociado (MGDEE7_2)

ID: GDE-META-EXP-SPEC-28
Ref: MGDEE7_2
Mech: Manual.
Cond: Obligatorio si el PA no está codificado en CPAT o el OAE decide registrarlo para referencia directa.
Cpt: Forma-Ingreso. Def: Registro manual del nombre del PA.
Cpt: Tipo-Dato. Def: Alfanumérico.
Ex: `Convalidación de Programa de Perfeccionamiento Académico`

#### 29. Versión MDGEE (MGDEE8_1)

ID: GDE-META-EXP-SPEC-29
Ref: MGDEE8_1
Mech: Automático. Registro automático de la versión de la guía de metadatos.
Cpt: Tipo-Dato. Def: Numérico.
Cpt: Valor-Defecto. Def: `001`.
Ex: `001`

## 4. Metadatos para Documentos Electrónicos

ID: GDE-META-DOCUMENTOS-ROOT-01
Purp: Definir el conjunto de metadatos aplicables a un documento electrónico.

### Tabla Resumen: Metadatos de Documentos

ID: GDE-META-DOCUMENTOS-TABLA-01

| Codificación | N° | Sub N° | Grupo/Rótulo | Definición | Flags |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | | | Identificación | Def: Info de identificación unívoca del documento. | |
| MGDDE1_1 | 1 | 1.1 | Identificador | Def: Código único asignado auto a un documento. | `AN` |
| MGDDE1_2 | 2 | 1.2 | Código serie | Def: Código serie del doc. según cuadro de clasificación OAE. | `AN` |
| MGDDE1_3 | 3 | 1.3 | Número del documento | Def: N° de orden interno dentro de una serie documental. | |
| MGDDE1_4 | 4 | 1.4 | Estado | Def: Estado de generación del doc. por la institución productora. | |
| MGDDE1_5 | 5 | 1.5 | Versión | Def: Número de versión del documento. | |
| MGDDE1_6 | 6 | 1.6 | Título del documento | Def: Palabra/frase para denominar el doc. (formal o atribuido). | `AN` |
| MGDDE1_7 | 7 | 1.7 | Resolución de captura | Def: Nivel de resolución de imagen (si es microforma). | `AN` |
| MGDDE1_8 | 8 | 1.8 | Nombre archivo asociado | Def: Nombre del archivo digital referenciado. | |
| 2 | | | Características Técnicas | Def: Caracterización técnica del documento. | |
| MGDDE2_1 | 9 | 2.1 | Tamaño | Def: Volumen del documento en Kb. | |
| MGDDE2_2 | 10 | 2.2 | Cantidad de páginas | Def: N° total de páginas o extensión. | `AN` |
| MGDDE2_3 | 11 | 2.3 | Formato | Def: Extensión del archivo electrónico. | |
| MGDDE2_4 | 12 | 2.4 | Nombre y Versión del software | Def: Software usado para generar el documento. | |
| 3 | | | Descripción | Def: Texto referencial del contenido. | |
| MGDDE3_1 | 13 | 3.1 | Resumen | Def: Relato sintético del contenido global. | |
| MGDDE3_2 | 14 | 3.2 | Palabras claves | Def: Materias o temas representativos del contenido. | `AN` |
| MGDDE3_3 | 15 | 3.3 | Idioma | Def: Idioma en que se encuentra el documento. | |
| MGDDE3_4 | 16 | 3.4 | Comunas | Def: Ubicación geográfica del resguardo del doc. | |
| 4 | | | Temporalidad | Def: Atributos de tiempo específicos. | |
| MGDDE4_1 | 17 | 4.1 | Fecha de creación | Def: Fecha en que es generado el documento. | `AN` |
| MGDDE4_2 | 18 | 4.2 | Fecha de modificación | Def: Fecha de la última modificación del documento. | |
| MGDDE4_3 | 19 | 4.3 | Fecha de captura | Def: Fecha de incorporación al repositorio (docs no generados internamente). | `AN` |
| MGDDE4_4 | 20 | 4.4 | Cobertura temporal | Def: Periodo de tiempo al que hace referencia el acto del doc. | |
| 5 | | | Caracterización documental | Def: Identificación específica por tipo de documento. | |
| MGDDE5_1 | 21 | 5.1 | Tipo documental | Def: Nombre y/o código del tipo documental estandarizado. | |
| MGDDE5_2 | 22 | 5.2 | Origen del documento | Def: Caracterización del origen de incorporación. | `AN` |
| MGDDE5_3 | 23 | 5.3 | Mecanismo de incorporación | Def: Mecanismo de incorporación al repositorio. | |
| MGDDE5_4 | 24 | 5.4 | URI documento externo | Def: Enlace a documento/recurso en repositorio externo. | |
| MGDDE5_5 | 25 | 5.5 | Ubicación física | Def: Código de almacenamiento físico (si existe original en papel). | |
| MGDDE5_6 | 26 | 5.6 | Estado de conservación microforma | Def: Estado del doc. original del cual se generó microforma. | `AN` |
| MGDDE5_7 | 27 | 5.7 | Disposición | Def: Destino planificado del documento (valoración documental). | |
| 6 | | | Relaciones | Def: Relaciones con otros docs, OAEs, personas. | |
| | | 6.1 | OAE Asociada | Def: Relaciones específicas con OAEs. | |
| MGDDE61_1 | 28 | 6.1.1 | Código OAE | Def: OAE que genera, gestiona o custodia el documento. | `AN, MU` |
| MGDDE61_2 | 29 | 6.1.2 | Nombre OAE | Def: Nombre institucional si no hay código de OAE. | `MU` |
| MGDDE61_3 | 30 | 6.1.3 | Tipo de relación doc-OAE | Def: Relación entre el doc. y el OAE (autor, custodio, etc.). | `AN, MU` |
| | | 6.2 | Otros actores | Def: Relaciones con personas naturales o jurídicas. | |
| MGDDE62_1 | 31 | 6.2.1 | Tipo de relación otros actores | Def: Tipo de relación entre el actor y el documento. | `AN, MU` |
| MGDDE62_2 | 32 | 6.2.2 | Tipo de actor relacionado | Def: Tipo de actor para determinar pertinencia del ID. | `MU` |
| MGDDE62_3 | 33 | 6.2.3 | Identificación de actor | Def: RUN/RUT/Pasaporte del actor relacionado. | `AN, MU` |
| MGDDE62_4 | 34 | 6.2.4 | Nombre del actor relacionado | Def: Nombre si no se cuenta con RUN/RUT. | `MU` |
| 7 | | | Seguridad | Def: Niveles de seguridad para la gestión. | |
| MGDDE7_1 | 35 | 7.1 | Nivel de Acceso | Def: Indicación relativa al acceso y consulta. | `AN` |
| MGDDE7_2 | 36 | 7.2 | Fecha fin restricción | Def: Fecha hasta la cual se presenta texto de advertencia. | |
| MGDDE7_3 | 37 | 7.3 | Texto Advertencia | Def: Texto a presentar si un usuario intenta acceder. | |
| MGDDE7_4 | 38 | 7.4 | Carácter sensible | Def: Identificación si el doc. contiene info sensible. | |
| 8 | | | Firma | Def: Tipo de firma electrónica utilizada. | |
| MGDDE8_1 | 39 | 8.1 | Tipo Firma | Def: Identificación del tipo de firma electrónica (simple/avanzada). | `MU` |
| MGDDE8_2 | 40 | 8.2 | Proveedor | Def: Proveedor del servicio de firma electrónica. | `MU` |
| MGDDE8_3 | 41 | 8.3 | Firma Electrónica Avanzada | Def: Indica si el doc. cuenta con FEA (Sí/No). | |
| | | 8.4 | Firmantes | | |
| MGDDE84_1 | 42 | 8.4.1 | Nombre/Cargo Representación | Def: Nombre y cargo de la persona que firma. | `MU` |
| MGDDE84_2 | 43 | 8.4.2 | RUN firmante | Def: RUN de la persona que firma. | `MU` |
| 9 | | | Procedimiento Asociado | Def: Identificación del PAT asociado. | |
| MGDDE9_1 | 44 | 9.1 | Código PAT asociado | Def: Código del PAT en CPAT asociado al documento. | |
| MGDDE9_2 | 45 | 9.2 | Nombre PAT asociado | Def: Nombre del PAT si no tiene código CPAT. | |
| 10 | | | Versión | Def: Versión del esquema de metadatos. | |
| MGDDE10_1 | 46 | 10.1| Versión MGDDE | Def: Versión del esquema de metadatos utilizado. | |

### Especificaciones Detalladas: Metadatos de Documentos

ID: GDE-META-DOCUMENTOS-ESPECIFICACIONES-01
Purp: Detallar cada metadato para documentos.
Ref: AUDIT-ETE-INFORME-01

#### 1. Identificador (MGDDE1_1)

ID: GDE-META-DOC-SPEC-01
Ref: MGDDE1_1
Mech: Automático. Sistema asigna ID único a cada documento ingresado.
Cpt: Tipo-Dato. Def: Alfanumérico.
Ctx: Asegurar unicidad, persistencia y estandarización de codificación.
Ex: `DOCU-20230925-001-XYZ`

#### 2. Código de serie (MGDDE1_2)

ID: GDE-META-DOC-SPEC-02
Ref: MGDDE1_2
Mech: Manual/Automático. Generado por sistema o manualmente según cuadro de clasificación OAE.
Cond: Obligatorio para transferencia al Archivo Nacional.
Cpt: Tipo-Dato. Def: Alfanumérico.

#### 3. Número de documento (MGDDE1_3)

ID: GDE-META-DOC-SPEC-03
Ref: MGDDE1_3
Mech: Manual/Automático. Número de orden interno recursivo dentro de una serie documental.
Cpt: Tipo-Dato. Def: Alfanumérico.

#### 4. Estado (MGDDE1_4)

ID: GDE-META-DOC-SPEC-04
Ref: MGDDE1_4
Mech: Manual/Automático. Identifica el estado de generación del documento.
Cpt: Tipo-Dato. Def: Alfanumérico.

#### 5. Versión (MGDDE1_5)

ID: GDE-META-DOC-SPEC-05
Ref: MGDDE1_5
Mech: Manual/Automático. Identificación del número de versión.
Cpt: Tipo-Dato. Def: Alfanumérico.
Ex: `1.1`

#### 6. Título del documento (MGDDE1_6)

ID: GDE-META-DOC-SPEC-06
Ref: MGDDE1_6
Mech: Manual. Título formal (automatizable) o atribuido (texto libre) si el tipo documental no lo incluye.
Cpt: Tipo-Dato. Def: Texto.
Ctx: Usar mayúsculas solo al inicio y en nombres propios.
Ex: `Resolución exenta asigna presupuesto para compra de insumos`

#### 7. Resolución de captura (MGDDE1_7)

ID: GDE-META-DOC-SPEC-07
Ref: MGDDE1_7
Mech: Automático. Sistema extrae info de metadatos embebidos del archivo.
Cond: Obligatorio para documentos de tipo Microforma.
Cpt: Tipo-Dato. Def: Texto.
Ctx: Cantidad de píxeles (horizontal x vertical).
Ex: `3000x2000`

#### 8. Nombre archivo asociado (MGDDE1_8)

ID: GDE-META-DOC-SPEC-08
Ref: MGDDE1_8
Mech: Automático. Sistema extrae el nombre del archivo.
Cpt: Tipo-Dato. Def: Texto.

#### 9. Tamaño (MGDDE2_1)

ID: GDE-META-DOC-SPEC-09
Ref: MGDDE2_1
Mech: Automático. Sistema extrae el volumen del archivo.
Cpt: Tipo-Dato. Def: Numérico (Kb).

#### 10. Cantidad de páginas o extensión (MGDDE2_2)

ID: GDE-META-DOC-SPEC-10
Ref: MGDDE2_2
Mech: Automático. Sistema extrae número de páginas o puede ser ingresado manualmente.
Cond: Obligatorio para documentos de tipo Microforma.
Cpt: Tipo-Dato. Def: Numérico.
Ex: `104`

#### 11. Formato (MGDDE2_3)

ID: GDE-META-DOC-SPEC-11
Ref: MGDDE2_3
Mech: Automático. Sistema extrae la extensión del archivo.
Cpt: Tipo-Dato. Def: Texto.
Ex: `pdf`

#### 12. Nombre y versión del software (MGDDE2_4)

ID: GDE-META-DOC-SPEC-12
Ref: MGDDE2_4
Mech: Automático. Sistema extrae info de metadatos embebidos del archivo.
Cpt: Tipo-Dato. Def: Texto.
Ex: `Microsoft Word 2019`

#### 13. Resumen (MGDDE3_1)

ID: GDE-META-DOC-SPEC-13
Ref: MGDDE3_1
Mech: Manual. Relato sintético del contenido.
Cpt: Tipo-Dato. Def: Texto.

#### 14. Palabras claves documento (MGDDE3_2)

ID: GDE-META-DOC-SPEC-14
Ref: MGDDE3_2
Mech: Manual o mediante selector de vocabulario controlado.
Cpt: Tipo-Dato. Def: Texto.
Ctx: Palabras cortas, simples o compuestas que expresen lo más relevante.
Ex: `Resolución de compra tecnológica`, `Adquisición de licencias de software`

#### 15. Idioma (MGDDE3_3)

ID: GDE-META-DOC-SPEC-15
Ref: MGDDE3_3
Mech: Manual.
Cpt: Tipo-Dato. Def: Texto.

#### 16. Comuna (MGDDE3_4)

ID: GDE-META-DOC-SPEC-16
Ref: MGDDE3_4
Mech: Automático. Código de comuna según sistema de codificación.
Cpt: Tipo-Dato. Def: Numérico.

#### 17. Fecha de creación (MGDDE4_1)

ID: GDE-META-DOC-SPEC-17
Ref: MGDDE4_1
Mech: Automático. Generado según formato `aaaa-mm-dd hh:mm:ss` (ISO 8601).
Cpt: Tipo-Dato. Def: Fecha/Hora (ISO 8601).
Ctx: Modificable, con registro de historial de cambios.
Ex: `2023-20-11:16:56:57`

#### 18. Fecha de modificación (MGDDE4_2)

ID: GDE-META-DOC-SPEC-18
Ref: MGDDE4_2
Mech: Automático. Generado en cada actualización en repositorio (`aaaa-mm-dd hh:mm:ss`).
Cpt: Tipo-Dato. Def: Fecha/Hora (ISO 8601).
Ctx: Modificable, con registro de historial de cambios.
Ex: `2023-20-11:16:56:57`

#### 19. Fecha de captura (MGDDE4_3)

ID: GDE-META-DOC-SPEC-19
Ref: MGDDE4_3
Mech: Automático/Manual. Fecha de incorporación de docs no generados internamente (`aaaa-mm-dd hh:mm:ss`).
Cond: Obligatorio para Microformas.
Cpt: Tipo-Dato. Def: Fecha/Hora (ISO 8601).
Ex: `2023-20-11:16:56:57`

#### 20. Cobertura temporal (MGDDE4_4)

ID: GDE-META-DOC-SPEC-20
Ref: MGDDE4_4
Mech: Automático/Manual. Periodo de tiempo (fechas) al que hace referencia el acto del documento.
Cpt: Tipo-Dato. Def: Fecha.

#### 21. Tipo documental (MGDDE5_1)

ID: GDE-META-DOC-SPEC-21
Ref: MGDDE5_1
Mech: Manual. Selección de lista controlada. Ref: `GDE-META-LISTAS-TIPO-DOC-01`.
Cond: Obligatorio si se cuenta con la tipificación del documento.
Cpt: Tipo-Dato. Def: Numérico.
Cpt: Valor-Defecto. Def: 3 (Antecedente).
Ex: `30` (Oficio)

#### 22. Origen del documento (MGDDE5_2)

ID: GDE-META-DOC-SPEC-22
Ref: MGDDE5_2
Mech: Automático. Selección de lista controlada. Ref: `GDE-META-LISTAS-ORIGEN-DOC-01`.
Cond: Obligatorio para Microformas.
Cpt: Tipo-Dato. Def: Numérico.
Cpt: Valor-Defecto. Def: 1.
Ex: `1` (repositorio externo)

#### 23. Mecanismo de incorporación del documento (MGDDE5_3)

ID: GDE-META-DOC-SPEC-23
Ref: MGDDE5_3
Mech: Automático/Manual. Selección de lista controlada. Ref: `GDE-META-LISTAS-MEC-INCORP-01`.
Cpt: Tipo-Dato. Def: Numérico.
Cpt: Valor-Defecto. Def: 2 (Digital).
Ex: `2`

#### 24. URI de documento externo (MGDDE5_4)

ID: GDE-META-DOC-SPEC-24
Ref: MGDDE5_4
Mech: Automático/Manual. URL o URI persistente del recurso.
Cond: Obligatorio para documentos externos referenciados.
Cpt: Tipo-Dato. Def: Alfanumérico.
Ex: `http://bibliotecadigital.dipres.gob.cl/handle/11626/19183`

#### 25. Ubicación física de documento referenciado (MGDDE5_5)

ID: GDE-META-DOC-SPEC-25
Ref: MGDDE5_5
Mech: Manual. Registro manual de la ubicación física según política de codificación institucional.
Cond: Obligatorio para documentos físicos referenciados (expediente híbrido, microforma).
Cpt: Tipo-Dato. Def: Alfanumérico.
Ex: `space_40_archivador_20.5.10_oae_33706`

#### 26. Estado de conservación microforma (MGDDE5_6)

ID: GDE-META-DOC-SPEC-26
Ref: MGDDE5_6
Mech: Automático/Manual. Selección de lista controlada. Ref: `GDE-META-LISTAS-ESTADO-MICROFORMA-01`.
Cond: Obligatorio para documentos tipo microforma.
Cpt: Tipo-Dato. Def: Numérico.
Cpt: Valor-Defecto. Def: 1 (Muy Bueno).
Ex: `1`

#### 27. Disposición (MGDDE5_7)

ID: GDE-META-DOC-SPEC-27
Ref: MGDDE5_7
Mech: Manual/Automático. Destino planificado del documento según proceso de valoración documental.
Cpt: Tipo-Dato. Def: Texto.
Ex: `Preservación Institucional`

#### 28. Código OAE (MGDDE61_1)

ID: GDE-META-DOC-SPEC-28
Ref: MGDDE61_1
Mech: Automático. Sistema incorpora al menos código de OAE productor desde GESCODE.
Cpt: Tipo-Dato. Def: Numérico.
Ex: `46` (Gobierno Regional de la Región de La Araucanía)

#### 29. Nombre OAE (MGDDE61_2)

ID: GDE-META-DOC-SPEC-29
Ref: MGDDE61_2
Mech: Automático/Manual. Registro manual del nombre institucional.
Cond: Obligatorio si no se identifica por código OAE o por resolución del OAE.
Cpt: Tipo-Dato. Def: Alfanumérico.
Ex: `Gobierno Regional de la Región de La Araucanía`

#### 30. Tipo de relación entre documento y OAE (MGDDE61_3)

ID: GDE-META-DOC-SPEC-30
Ref: MGDDE61_3
Mech: Automático. Selección de lista controlada. Ref: `GDE-META-LISTAS-TIPO-REL-OAE-01`.
Cpt: Tipo-Dato. Def: Numérico.
Ctx: Obligatorio registrar al menos autor institucional y custodio.
Cpt: Valor-Defecto. Def: 1 (Autor institucional).
Ex: `1`

#### 31. Tipo de relación con otros actores (MGDDE62_1)

ID: GDE-META-DOC-SPEC-31
Ref: MGDDE62_1
Mech: Automático/Manual. Selección de lista controlada. Ref: `GDE-META-LISTAS-TIPO-REL-ACTORES-01`.
Cond: Obligatorio al registrar una relación con el documento.
Cpt: Tipo-Dato. Def: Numérico.
Ctx: Al menos se debe registrar al autor/creador.
Cpt: Valor-Defecto. Def: 3 (Autor/creador).
Ex: `3`

#### 32. Tipo de actor relacionado (MGDDE62_2)

ID: GDE-META-DOC-SPEC-32
Ref: MGDDE62_2
Mech: Automático. Selección de lista controlada para indicar tipo de ID requerido. Ref: `GDE-META-LISTAS-TIPO-ACTOR-01`.
Cond: Obligatorio al registrar una relación con el documento.
Cpt: Tipo-Dato. Def: Numérico.
Cpt: Valor-Defecto. Def: 1 (Ciudadano).
Ex: `1`

#### 33. Identificación de actor relacionado (MGDDE62_3)

ID: GDE-META-DOC-SPEC-33
Ref: MGDDE62_3
Mech: Automático/Manual. RUN/RUT/Pasaporte.
Cond: Obligatorio al registrar una relación con el documento.
Cpt: Tipo-Dato. Def: Alfanumérico.
Ex: `677368373-5`

#### 34. Nombre del actor relacionado (MGDDE62_4)

ID: GDE-META-DOC-SPEC-34
Ref: MGDDE62_4
Mech: Manual. Registro del nombre de la persona natural o jurídica.
Cond: Obligatorio al registrar una relación si no se cuenta con ID (RUN/RUT/Pasaporte).
Cpt: Tipo-Dato. Def: Alfanumérico.
Ex: `Entel Chile`, `Julian Santelices Machuca`

#### 35. Nivel de acceso (MGDDE7_1)

ID: GDE-META-DOC-SPEC-35
Ref: MGDDE7_1
Mech: Manual. Selección de vocabulario controlado. Ref: `GDE-META-LISTAS-NIVEL-ACCESO-01`.
Cpt: Tipo-Dato. Def: Numérico.
Cpt: Valor-Defecto. Def: 1 (Público).
Ex: `1`

#### 36. Fecha fin restricción (MGDDE7_2)

ID: GDE-META-DOC-SPEC-36
Ref: MGDDE7_2
Mech: Manual. Fecha hasta cuando se debe presentar el texto de advertencia.
Cpt: Tipo-Dato. Def: Fecha.

#### 37. Texto Advertencia (MGDDE7_3)

ID: GDE-META-DOC-SPEC-37
Ref: MGDDE7_3
Mech: Manual. Texto a presentar si un usuario intenta acceder.
Cpt: Tipo-Dato. Def: Texto.

#### 38. Información de carácter sensible (MGDDE7_4)

ID: GDE-META-DOC-SPEC-38
Ref: MGDDE7_4
Mech: Manual. Plataforma debe manejar registro de marca (Sí/No).
Cpt: Tipo-Dato. Def: Numérico (Lista controlada `1-SI / 2-NO`).
Cpt: Valor-Defecto. Def: 2 (NO).
Ex: `1`

#### 39. Tipo Firma (MGDDE8_1)

ID: GDE-META-DOC-SPEC-39
Ref: MGDDE8_1
Mech: Automático. Selección de lista controlada (ej. simple, avanzada).
Cpt: Tipo-Dato. Def: Numérico.
Cpt: Valor-Defecto. Def: 1 (AVANZADA).
Ex: `2` (SIMPLE)

#### 40. Proveedor (MGDDE8_2)

ID: GDE-META-DOC-SPEC-40
Ref: MGDDE8_2
Mech: Automático. Detección automática del proveedor de firma.
Cpt: Tipo-Dato. Def: Texto.

#### 41. Firma electrónica avanzada (MGDDE8_3)

ID: GDE-META-DOC-SPEC-41
Ref: MGDDE8_3
Mech: Automático. Detección automática si cuenta con FEA (Sí/No).
Cpt: Tipo-Dato. Def: Numérico (Lista controlada `1-SI / 2-NO`).
Cpt: Valor-Defecto. Def: 2 (NO).
Ex: `1` (SI)

#### 42. Nombre/Cargo Representación (MGDDE84_1)

ID: GDE-META-DOC-SPEC-42
Ref: MGDDE84_1
Mech: Automático/Manual. Detección automática o registro manual del firmante y su cargo.
Cpt: Tipo-Dato. Def: Texto.

#### 43. RUN firmante (MGDDE84_2)

ID: GDE-META-DOC-SPEC-43
Ref: MGDDE84_2
Mech: Manual/Automático. Registro del RUN al identificar al actor firmante.
Cpt: Tipo-Dato. Def: Alfanumérico (Formato RUN).

#### 44. Código procedimiento administrativo asociado (MGDDE9_1)

ID: GDE-META-DOC-SPEC-44
Ref: MGDDE9_1
Mech: Automático/Manual. Código desde Catálogo de Procedimientos Administrativos y Tramitaciones (CPAT).
Cond: Obligatorio si el documento está vinculado a un PA específico.
Cpt: Tipo-Dato. Def: Alfanumérico.
Ex: `5076`

#### 45. Nombre procedimiento administrativo asociado (MGDDE9_2)

ID: GDE-META-DOC-SPEC-45
Ref: MGDDE9_2
Mech: Manual. Registro manual del nombre del PA.
Cond: Obligatorio si el PA no se encuentra creado en CPAT.
Cpt: Tipo-Dato. Def: Texto.
Ex: `Convalidación de Programa de Perfeccionamiento Académico`

#### 46. Versión MGDDE (MGDDE10_1)

ID: GDE-META-DOC-SPEC-46
Ref: MGDDE10_1
Mech: Automático. Registro automático de la versión de la guía de metadatos.
Cpt: Tipo-Dato. Def: Numérico.
Cpt: Valor-Defecto. Def: 1.
Ex: `1`

## 5. Listas Controladas

ID: GDE-META-LISTAS-CONTROLADAS-ROOT-01
Purp: Definir los vocabularios controlados para estandarizar el registro de información en metadatos específicos.
Ctx: Disponible en Gestor de Códigos (GESCODE) para uso por OAEs.

### Lista 1: Tipo Documental

ID: GDE-META-LISTAS-TIPO-DOC-01
Ref: MGDDE5_1
Cpt: Valores.

- `1`: Acta. Ex: Acta de Sesión, de evaluación, de consejo.
- `2`: Acuerdo. Ex: Acuerdo de comité, complementario, de compromiso.
- `3`: Antecedente. Ex: Antecedentes legales, personales, profesionales.
- `4`: Autorización. Ex: Autorización de apertura, de constitución, sanitaria.
- `5`: Base. Ex: Bases técnicas, de concurso, de licitación.
- `40`: Solicitud. Ex: Solicitud de permiso, de licencia, de subsidio.
- `41`: Términos de referencia. Ex: Para licitaciones, proyectos, estudios.
- `42`: Transcripción. Ex: De reuniones, de entrevistas, de audiencias.

### Lista 2: Mecanismo de Incorporación

ID: GDE-META-LISTAS-MEC-INCORP-01
Ref: MGDDE5_3
Cpt: Valores.

- `1`: Físico
- `2`: Digital
- `3`: Digitalización

### Lista 3: Estado Conservación Microforma

ID: GDE-META-LISTAS-ESTADO-MICROFORMA-01
Ref: MGDDE5_6
Cpt: Valores.

- `1`: Muy Bueno. Def: Sin deterioros. Fácil manipulación.
- `2`: Bueno. Def: Deterioros menores sin comprometer info. Fácil manipulación.
- `3`: Regular. Def: Hojas sueltas, manchas, rasgados menores. Manipular con cuidado.
- `4`: Malo. Def: Rasgados y faltantes >50%, daño biológico. Manipular con mucho cuidado.
- `5`: Muy Malo. Def: Deterioros extremos, incompletitud, microorganismos activos. Manipulación con extremo cuidado.

### Lista 4: Tipo Relación OAE

ID: GDE-META-LISTAS-TIPO-REL-OAE-01
Ref: MGDEE51_3, MGDDE61_3
Cpt: Valores.

- `1`: Autor institucional
- `2`: Destinatario
- `3`: Productor / generador
- `4`: Custodia

### Lista 5: Tipo Relación Otros Actores

ID: GDE-META-LISTAS-TIPO-REL-ACTORES-01
Ref: MGDEE52_1, MGDDE62_1
Cpt: Valores.

- `1`: Responsable
- `2`: Interesado
- `3`: Autor/creador
- `4`: Referido
- `5`: Destinatario
- `6`: Ministro de Fe

### Lista 6: Tipo Actor Relacionado

ID: GDE-META-LISTAS-TIPO-ACTOR-01
Ref: MGDEE52_2, MGDDE62_2
Cpt: Valores.

- `1`: Ciudadano
- `2`: Extranjero
- `3`: Institución privada
- `4`: Funcionario

### Lista 7: Nivel de Acceso

ID: GDE-META-LISTAS-NIVEL-ACCESO-01
Ref: MGDEE6_1, MGDDE7_1
Cpt: Valores.

- `1`: Público
- `2`: Restringido
- `3`: Secreto
- `4`: Reservado

### Lista 8: Origen del Documento

ID: GDE-META-LISTAS-ORIGEN-DOC-01
Ref: MGDDE5_2
Cpt: Valores.

- `1`: Repositorio Externo
- `2`: Interoperabilidad
- `3`: Plataforma ciudadana
- `4`: Repositorio Ciudadano
