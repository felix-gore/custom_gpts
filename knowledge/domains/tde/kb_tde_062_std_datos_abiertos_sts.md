# Estándares para la Apertura y Reutilización de Datos Abiertos

ID: GUIDE-STS-MASTER-01
Version: 1.0.0
Status: Draft
Human-Creator: FS
Human-Editor: FS
Model-Collaborator: IA-GEMINI
Creation-Date: 2025-07-06
Modification-Date: 2025-07-06
Primary-Source: kb_062_tde_std_datos_abiertos.md
Ref-STS-Guide: GUIDE-STS-MASTER-01

## 1. Marco General

ID: DA-MARCO-GENERAL-01
Purp: Establecer el contexto, objetivo, alcance y definiciones de los estándares de datos abiertos.

### 1.1. Introducción

ID: DA-INTRODUCCION-01
Cpt: Datos Abiertos (Open Data).

- Mssn: Fomentar la transparencia, el acceso a la información pública, la competitividad y el desarrollo económico.
- Mech: Reutilización de información del sector público.
- Cpt: Iniciativa Chile.
  - ID: datos.gob.cl
  - Purp: Garantizar que los datos públicos generados por el Estado estén disponibles de forma abierta y accesible.
  - Dest: Ciudadanos, entidades interesadas.
- Req: Publicación.
  - Mdl: Digital, estandarizado, estructurado.
  - Purp: Facilitar la comprensión y accesibilidad.
- Cpt: Usos Potenciales.
  - Act: Creación de informes, estadísticas.
  - Res: Beneficio social, investigación científica, oportunidades de negocio.
  - Ctx: Aplicación en salud, seguridad, transporte, educación, medioambiente.
- Cpt: Alineación Internacional.
  - Fnd: Sigue directrices y ejemplos de países líderes.
  - Ref: EEUU (Open Government Directive).
  - Ref: Reino Unido (Opening up Government).
  - Ref: UE (Directiva 2003/98/CE sobre reutilización info sector público).
  - Src: <https://obamawhitehouse.archives.gov/open/documents/open-government-directive>
  - Src: <http://data.gov.uk/>
  - Src: <http://eurlex.europa.eu/LexUriServ/LexUriServ.do?uri=CELEX:32003L0098:ES:HTML>
- Cpt: Rol de datos.gob.cl.
  - Fnd: Pilar fundamental de la Estrategia de Gobierno Digital de Chile.
  - Src: Datos financiados y recopilados con recursos públicos.
  - Req: Disponibles al servicio de la ciudadanía, sin restricciones de uso, en formatos adecuados.
- Cpt: Enfoque Dual.
  - Obj: Potenciar la transparencia y el acceso a la información.
  - Obj: Fomentar el desarrollo de nuevas tecnologías e innovación.
  - Mech: Permitir que terceros agreguen valor a los datos disponibles para generar nuevas soluciones y aplicaciones.

### 1.2. Objetivo

ID: DA-OBJETIVO-01
Purp: Establecer estándares y directrices técnicas para la apertura y reutilización de datos en los órganos de la Administración del Estado, con el fin de facilitar su acceso, uso, reutilización y redistribución para cualquier fin.

### 1.3. Alcance

ID: DA-ALCANCE-01

- Ctx: Aplicabilidad.
  - `- Ctx: Datos abiertos y datasets publicados en el Portal de Datos Abiertos de la SGD.`
  - `- Ctx: Portales o plataformas institucionales de datos abiertos de OAEs.`
- Req: Los OAEs deben garantizar que sus datos estén referenciados y sincronizados en la plataforma de la SGD.

### 1.4. Definiciones

ID: DA-DEFINICIONES-01

- Def: Catálogo de Datos Abiertos.
  - Cpt: Repositorio que centraliza, almacena y disponibiliza conjuntos de datos abiertos estructurados y descritos por metadatos.
- Def: Conjunto de Datos Abiertos.
  - Cpt: Colección de datos relacionados, en formatos de uso común (preferiblemente estructurados), descritos por metadatos.
- Def: Dato.
  - Cpt: Representación de un atributo o variable (cuantitativa/cualitativa) por una secuencia de símbolos, capturable por observación/medición.
- Def: DCAT.
  - Cpt: Estándar internacional de vocabulario para catálogos de datos que facilita la interoperabilidad en la red.
- Def: Dublin Core.
  - Cpt: Vocabulario genérico de 15 propiedades para describir recursos electrónicos (auspiciado por DCMI).
- Def: Dato Abierto.
  - Cpt: Dato digital con características técnicas/jurídicas para ser usado, reutilizado y redistribuido libremente por cualquier persona/entidad, en cualquier momento y lugar.
- Def: Datos Genéricos.
  - Cpt: Datos de uso común que no requieren aplicación especializada.
- Def: Datos Geográficos.
  - Cpt: Datos que refieren a una localización relativa a la Tierra (Fuente: ISO/TC 211).
- Def: Diccionario de Variables.
  - Cpt: Documento que detalla y define las variables en un dataset (naturaleza, tipo, estructura).
- Def: Documentación Administrativa.
  - Cpt: Documentos de respaldo que proporcionan contexto y justificación para su uso y comprensión.

## 2. Estándares Abiertos

ID: DA-ESTANDARES-ABIERTOS-01
Purp: Definir los requisitos técnicos para la publicación de datos abiertos.

### 2.1. Formato Abierto

ID: DA-FORMATO-ABIERTO-01

- Req: Publicación.
  - `- Req: Usar formatos abiertos para máxima reutilización y accesibilidad.`
  - `- Req: Cumplir clasificación "tres estrellas o más" de Tim Berners-Lee. Ref: <https://5stardata.info/en/>`
- Rec: Favorecer formatos no propietarios.
  - Res: Legibilidad por máquinas sin herramientas costosas, facilita integración en aplicaciones.
- Rec: Proveer datos en múltiples formatos para mayor flexibilidad y adaptabilidad.
  - Ex: Para datos tabulares, ofrecer XLS/XLSX junto a CSV.

#### 2.1.1. Datos Genéricos

ID: DA-FORMATO-GENERICOS-01
Purp: Especificar formatos aceptados para datos genéricos.

| Nombre | Uso esperado |
|---|---|
| CSV | Datos con estructura relacional (Tablas). |
| XML | Datos con estructura jerárquica (Árboles). |
| JSON | Datos con estructura jerárquica (Árboles). |
| RDF | Datos con cualquier estructura (Grafos). |
| TSV | Datos con estructura relacional (Tablas), delimitador de tabulación. |
| RAW | Datos en formato bruto, sin esquema estructurado definido. |
| Parquet | Datos con estructura columnar optimizada para analítica y consulta masiva. |

#### 2.1.2. Datos Geográficos

ID: DA-FORMATO-GEOGRAFICOS-01
Purp: Especificar formatos aceptados para datos geográficos.

| Nombre | Uso esperado |
|---|---|
| GeoJSON | Datos geoespaciales basados en JSON. |
| GML | Datos geográficos para servicios WFS (Web Feature Service). |
| GeoPackage | Basado en SQLite para almacenar/transferir datos geoespaciales (vectoriales y raster). |

#### 2.1.3. Documentación Administrativa

ID: DA-FORMATO-DOC-ADMIN-01
Purp: Especificar formatos para documentación administrativa que acompaña a los datasets.

- Ctx: Documentos oficiales que respaldan, explican y contextualizan los datos.
- Req: Formatos.
  - `- Req: PDF (Portable Document Format). Uso: Toda documentación administrativa para preservar contenido y asegurar accesibilidad.`
  - `- Req: ODT (Open Document Text). Uso: Documentos que requieren ser editables manteniendo estandarización.`
- Purp: Proporcionar detalles metodológicos y de origen de los datos para mayor contexto.
- Warn: Documentación administrativa no es metadato; complementa para enriquecer transparencia.

### 2.2. Archivos Grandes

ID: DA-ARCHIVOS-GRANDES-01

- Req: Límite máximo de archivo.
  - `- Ctx: 200 megabytes.`
  - `- Cond: Excepción si la naturaleza del dataset justifica exceder el límite.`
  - `- Act: En caso de excepción, particionar el archivo.`
- Req: Compresión.
  - `- Mdl: ZIP o 7z.`
  - `- Req: Garantizar integridad y accesibilidad total de los datos descomprimidos.`

### 2.3. Lenguaje y Codificación

ID: DA-LENGUAJE-COD-01

- Req: Lenguaje estándar.
  - `- Ctx: Español-Chile (ES_CL).`
- Req: Codificación de caracteres.
  - `- Ctx: UTF-8.`

## 3. Metadatos

ID: DA-METADATOS-ROOT-01
Purp: Detallar los estándares de metadatos para la publicación de datos abiertos.

### 3.1. Principios de Metadatos

ID: DA-METADATOS-PRINCIPIOS-01

- Req: Todo OAE debe publicar sus datasets con metadatos consistentes.
- Req: Formato de metadatos.
  - `- Mdl: Legibles por humanos y por máquinas.`
- Purp: Facilitar la comprensión del origen, procesamiento y significado de los datos.
- Fnd: Estándar base DCAT, complementado con Dublin Core. Ref: DA-DEFINICIONES-01.
- Ctx: Adaptación nacional con modificaciones específicas para el contexto chileno.
- Req: Niveles de metadatos.
  - `- Cpt: Organizados en 4 niveles de descripción y 3 de requerimiento.`
  - `- Cpt: Nivel 1 (Obligatorio): documentación básica homogénea.`
  - `- Cpt: Nivel 2 (Recomendado): mayor calidad de documentación.`
  - `- Cpt: Nivel 3 (Opcional): uso según utilidad para el organismo.`

### 3.2. Niveles de Metadatos

ID: DA-METADATOS-NIVELES-01
Purp: Especificar los metadatos requeridos para cada nivel de descripción.

#### 3.2.1. Nivel Catálogo

ID: DA-METADATOS-CATALOGO-01
Purp: Definir metadatos para la descripción general del catálogo de datos abiertos.

| Nombre del Metadato | Requerimiento | Descripción / Ejemplo |
|---|---|---|
| Identificador del Catálogo | Obligatorio | Código único para identificar el catálogo. Ex: cat_001 |
| Título del Catálogo | Obligatorio | Nombre claro y breve. Ex: Catálogo Datos Abiertos Santiago |
| Descripción del Catálogo | Obligatorio | Detalle de contenido y alcance. Ex: Datasets Municipalidad de Santiago. |
| OAE Asociado | Obligatorio | Órgano del Estado al que pertenece. Ex: Municipalidad de Santiago |
| Código de OAE | Obligatorio | Código Gescode del OAE. Ex: PE-MUN-00432 |
| Correo electrónico OAE | Obligatorio | Email de contacto para el catálogo. Ex: <datos@municipalidad.gob.cl> |
| Fecha de creación | Obligatorio | Fecha oficial de creación del catálogo. Ex: 2023-01-01 |
| Fecha de última actualización | Recomendado | Última modificación del catálogo. Ex: 2023-12-31 |
| Idioma(s) | Recomendado | Lenguaje de metadatos y datasets. Ex: Español, Inglés |
| Licencia | Recomendado | Licencia general (sobrescribible a nivel de recurso). Ex: CC BY 4.0 |
| Cobertura geográfica | Recomendado | Ámbito geográfico. Ref: DA-DEF-NIVELES-GEO-01. Ex: Chile, Región Metropolitana |
| N° visitas | Recomendado | Visitas acumuladas al catálogo. Ex: 1000 |
| Colección Categorías | Recomendado | Lista de categorías temáticas. Ex: Demografía, Transporte |
| Conjuntos de Datos | Opcional | Lista de datasets del catálogo. Ex: dataset_1, dataset_2 |
| Página web del catálogo | Opcional | URL de acceso principal. Ex: <https://datos.gob.cl/> |

#### 3.2.2. Nivel Conjunto de Datos

ID: DA-METADATOS-CONJUNTO-01
Purp: Detallar metadatos para cada conjunto de datos (dataset).

| Nombre del Metadato | Requerimiento | Descripción / Ejemplo |
|---|---|---|
| Identificador del Conjunto de Datos | Obligatorio | ID único del dataset. Ex: dataset_001 |
| Título del Conjunto de Datos | Obligatorio | Nombre claro y abstracto. Ex: Datos de temperatura en Santiago |
| Descripción del Conjunto de Datos | Obligatorio | Resumen de contenido y propósito. Ex: Registros históricos de temp. max/min. |
| Autor | Obligatorio | Responsable de la publicación. Ex: Depto. de Meteorología |
| Correo electrónico de Contacto | Obligatorio | Email del responsable. Ex: <departamento@munidesantiago.gob.cl> |
| OAE Asociado | Obligatorio | Órgano al que pertenece. Ex: Municipalidad de Santiago |
| Código de OAE | Obligatorio | Código Gescode del OAE. Ex: PE-MUN-00432 |
| Departamento de la OAE | Obligatorio | Departamento encargado. Ex: Depto. de Medio Ambiente |
| Recursos | Obligatorio | Lista de recursos del dataset. Ex: archivo_csv, archivo_shp, metadata.json |
| Categoría Temática/s | Obligatorio | Categoría/s global/es. Ex: Meteorología, Medio Ambiente |
| Fecha de Creación | Obligatorio | Fecha de creación del dataset. Ex: 2023-01-01 |
| Fecha de publicación | Obligatorio | Fecha de publicación en portal DDAA. Ex: 2023-02-15 |
| Palabras Claves | Obligatorio | Etiquetas que describen el contenido. Ex: temperatura, santiago, clima |
| Periodo de referencia | Obligatorio | Lapso temporal de la información. Ex: 1980-2023 |
| Licencia | Obligatorio | Licencia de distribución. Ex: CC BY 4.0 |
| Versionamiento | Obligatorio | Versión del dataset. Ex: 1.0 |
| Fecha de la versión | Obligatorio | Fecha de edición de la versión. Ex: 2023-01-01 |
| Fecha de última modificación | Recomendado | Última modificación de datos/metadatos. Ex: 2023-12-31 |
| Frecuencia de actualización | Recomendado | Frecuencia de actualización. Ex: Mensual |
| Ubicación o Enlace Directo (URL) | Recomendado | URL de acceso al dataset. Ex: <https://datos.gob.cl/dataset/encuesta-juventud> |
| Idioma(s) | Recomendado | Lenguaje de descripción. Ex: Español, Inglés |
| Cobertura geográfica | Recomendado | Ámbito geográfico. Ref: DA-DEF-NIVELES-GEO-01. Ex: Chile |
| Visitas al dataset | Recomendado | Número total de visitas. Ex: 500 |
| Descargas | Recomendado | Cantidad de descargas. Ex: 200 |
| Registro de Cambios | Recomendado | Descripción cronológica de modificaciones. Ex: V1.1: Se agregaron nuevas estaciones. |
| Procedencia del conjunto de Datos | Recomendado | Indica si es subconjunto, integración, etc. Ex: Integración |
| Detalle de procedencia | Recomendado | Especifica los datasets originales. Ex: dataset_1, dataset_2 |
| Relación | Opcional | Relación entre dataset y OAE. Ex: autor institucional |
| Tamaño del Dataset | Opcional | Volumen de datos. Ex: 10 MB |

#### 3.2.3. Nivel Recurso

ID: DA-METADATOS-RECURSO-01
Purp: Describir los metadatos para archivos individuales (recursos) dentro de un dataset.

| Nombre del Metadato | Requerimiento | Descripción / Ejemplo |
|---|---|---|
| Identificador | Obligatorio | ID único del recurso. Ex: recurso_001 |
| Título | Obligatorio | Nombre del recurso. Ex: Datos de temperatura_2023.csv |
| Descripción | Obligatorio | Breve descripción. Ex: Archivo CSV con temp. max/min para 2023. |
| Diccionario de variables | Obligatorio | Lista de campos si es una tabla. Ex: fecha, estación, temperatura_max |
| Fecha de última modificación | Recomendado | Fecha de última actualización. Ex: 2023-12-31 |
| Ubicación o Enlace Directo (URL) | Recomendado | URL de acceso directo. Ex: <https://datos.gob.cl/.../resource/b857>... |
| Tamaño del Archivo | Recomendado | Tamaño en bytes (aprox.). Ex: 5 MB |
| Formato del recurso | Recomendado | Formato del archivo. Ex: CSV |
| Visitas al recurso | Recomendado | Cantidad de visitas. Ex: 200 |
| Descargas | Recomendado | Cantidad de descargas. Ex: 100 |

### 3.3. Diccionario de Variables

ID: DA-METADATOS-DICCIONARIO-01

- Req: Cada dataset debe publicarse con su diccionario de variables.
- Purp: Describir detalladamente cada variable para que los usuarios comprendan los datos.

| Nombre | Requerimiento | Descripción / Ejemplo |
|---|---|---|
| Nombre | Obligatorio | Nombre del campo en el encabezado. Ex: Edad |
| Tipo | Obligatorio | Tipo de dato contenido en el campo. Ex: Numérico |
| Descripción | Obligatorio | Información que contiene el campo. Ex: Edad de la persona encuestada. |
| Identificador | Recomendado | Código identificador único del campo. Ex: edad |
| Unidad de medida | Opcional | Unidad de medida para campos numéricos. Ex: Años |

## 4. Definiciones Compartidas

ID: DA-DEF-COMPARTIDAS-01
Purp: Definir elementos comunes referenciables para evitar duplicación.

### 4.1. Niveles de Cobertura Geográfica

ID: DA-DEF-NIVELES-GEO-01

- Nat: Lista enumerada.
- Cpt:
  - `- País`
  - `- Región`
  - `- Provincia`
  - `- Comuna`

## 5. Licenciamiento

ID: DA-LICENCIAMIENTO-ROOT-01
Purp: Definir las políticas de licenciamiento para la publicación de datos abiertos.

### 5.1. Política de Licenciamiento

ID: DA-LICENCIAMIENTO-POLITICA-01

- Req: Disponibilidad.
  - `- Ctx: Datos y datasets deben estar disponibles para todas las personas (naturales/jurídicas).`
- Mech: Licencias de dominio público.
- Req: Licencia predeterminada.
  - `- Ctx: Creative Commons Zero (CC0 1.0) si no se asigna explícitamente otra.`
- Req: Licencia alternativa.
  - `- Ctx: OAEs pueden optar por otras licencias predefinidas según necesidades.`
  - `- Cond: Si se necesita una licencia no predefinida, solicitar y justificar a la SGD.`

### 5.2. Tipos de Licencia

ID: DA-LICENCIAMIENTO-TIPOS-01
Purp: Detallar las licencias predeterminadas y alternativas.

| Licencia | Dominio | Descripción |
|---|---|---|
| Creative Commons Zero (CC0 1.0) | Contenido, Datos | Renuncia a todos los derechos de autor y conexos. Uso libre para cualquier propósito sin restricciones (dominio público). |
| Open Data Commons Public Domain Dedication and Licence (PDDL-1.0) | Datos | Permite usar, modificar y distribuir los datos libremente sin ninguna restricción. |
| Creative Commons Attribution 4.0 (CC-BY-4.0) | Contenido, Datos | Permite copiar, distribuir, exhibir y ejecutar obras derivadas con la condición de dar crédito al creador original. |
| Open Data Commons Attribution License (ODC-By-1.0) | Datos | Permite la copia, distribución y uso de datasets en nuevos productos siempre que se dé atribución al autor. |

## 6. Catálogos Institucionales

ID: DA-CATALOGOS-INST-01
Purp: Establecer los requisitos para los portales o plataformas de datos abiertos institucionales.

- Req: Acceso inmediato, sin requisitos de registro o identificación.
- Req: Contener un listado completo, ordenado y clasificado de todos los datasets disponibles.
- Req: Facilitar navegación, búsqueda de texto y consulta efectiva.
- Req: Mantener operatividad continua del portal y analizar estadísticas de uso para mejorar.
- Req: Proveer APIs para facilitar captura y utilización de datasets por usuarios y su integración en el Portal Nacional de Datos Abiertos.
