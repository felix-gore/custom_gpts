# Guía de Anonimización de Datos

ID: TDE-KB-080-ANON-GUIA
Version: 1.0.0
Status: Draft
Human-Creator: FS
Human-Editor: FS
Model-Collaborator: STSador
Creation-Date: 2025-07-07
Modification-Date: 2025-07-07
Primary-Source: kb_080_tde_guia_anonimizacion.md
Ref-STS-Guide: GUIDE-STS-MASTER-01

## 1. Introducción

ID: TDE-KB-080-INTRO-01
Cpt: Guía introductoria.
Obj: Ofrecer una introducción básica y concisa a la anonimización de datos.
Dest: Entidades y organizaciones que gestionan datos personales.
Purp: Servir como primera aproximación a conceptos, riesgos, técnicas y complejidad.
Ctx: Foco en anonimización de bases de datos estructuradas.
Warn: No es un manual exhaustivo; no aborda aspectos técnicos detallados.
Src: Guía Anonimización AEPD, Informe Anonimización Min. Asuntos Económicos (ES), Criterios Disociación AGESIC, otros.
Fnd: Contenido sin perjuicio de reglamentos futuros del Proyecto de Ley de Protección de Datos Personales de Chile.

## 2. Marco Conceptual

ID: TDE-KB-080-CONCEPTOS-01
Purp: Definir conceptos clave para la comprensión de la anonimización.

### 2.1. Acrónimos y Fuentes

ID: TDE-KB-080-CONCEPTOS-ACRONIMOS-01

- Def: Acron-PDL. Ctx: Proyecto de Ley que regula la Protección y el Tratamiento de los Datos Personales y crea la Agencia de Protección de Datos Personales (Chile).

### 2.2. Conceptos Fundamentales

ID: TDE-KB-080-CONCEPTOS-FUNDAMENTALES-01

- Cpt: Dato Personal.
- ID: TDE-KB-080-DEF-DATO-PERSONAL-01
- Def: Cualquier información vinculada/referida a una persona natural identificada o identificable.
- Src: PDL.
- Ctx: Criterio-Identificable. Posibilidad de determinar identidad (directa/indirecta) mediante identificadores (nombre, RUT) o elementos propios (físicos, fisiológicos, etc.).
- Cond: Excepción por esfuerzo de identificación desproporcionado.

- Cpt: Dato Sensible.
- ID: TDE-KB-080-DEF-DATO-SENSIBLE-01
- Def: Datos personales que revelan origen étnico/racial, afiliación política/sindical/gremial, hábitos personales, convicciones ideológicas/filosóficas, creencias religiosas, datos de salud, perfil biológico, datos biométricos, vida sexual, orientación sexual, identidad de género.
- Src: PDL.

- Cpt: Tratamiento de Datos.
- ID: TDE-KB-080-DEF-TRATAMIENTO-DATOS-01
- Def: Cualquier operación o procedimiento técnico (automatizado o no) sobre datos personales.
- Ctx: Acciones. recolectar, almacenar, grabar, organizar, elaborar, seleccionar, extraer, confrontar, interconectar, disociar, comunicar, ceder, transferir, transmitir, cancelar o utilizar.
- Src: PDL.

### 2.3. Conceptos de Identificación

ID: TDE-KB-080-CONCEPTOS-IDENTIFICACION-01

- Cpt: Identificación.
- ID: TDE-KB-080-DEF-IDENTIFICACION-01
- Def: Proceso de reconocimiento o determinación de la identidad específica de una persona usando datos únicos asociados a ella.

- Cpt: Reidentificación.
- ID: TDE-KB-080-DEF-REIDENTIFICACION-01
- Def: Proceso de identificar a las personas específicas a las que pertenecen los datos a partir de un conjunto de datos tratado.
- Ctx: Riesgo clave a mitigar en procesos de anonimización.

- Cpt: Persona Identificada.
- ID: TDE-KB-080-DEF-PERSONA-IDENTIFICADA-01
- Def: Persona cuya identidad ya se conoce.
- Ex: "Juan Pérez".

- Cpt: Persona Identificable.
- ID: TDE-KB-080-DEF-PERSONA-IDENTIFICABLE-01
- Def: Persona cuya identidad es desconocida pero determinable (directa/indirectamente) mediante identificadores.

### 2.4. Tipos de Atributos

ID: TDE-KB-080-CONCEPTOS-ATRIBUTOS-01

- Cpt: Identificadores Directos.
- ID: TDE-KB-080-DEF-ID-DIRECTO-01
- Def: Datos que identifican de manera unívoca a una persona.
- Ex: Nombres, números de identificación, direcciones exactas.

- Cpt: Identificadores Indirectos (Seudoidentificadores/Cuasi-identificadores).
- ID: TDE-KB-080-DEF-ID-INDIRECTO-01
- Def: Datos que, al combinarse con la misma u otras fuentes, pueden permitir identificar a un individuo.
- Ex: Datos sociodemográficos, configuración de navegador, ubicación geográfica.

- Cpt: Atributos Objetivos.
- ID: TDE-KB-080-DEF-ATRIBUTO-OBJETIVO-01
- Def: Atributos de datos que se pretenden analizar, esenciales para el propósito del procesamiento.

- Cpt: Registro.
- ID: TDE-KB-080-DEF-REGISTRO-01
- Def: Colección de atributos relacionados con un individuo, formando una unidad en un conjunto de datos.

- Cpt: Tabla de Ejemplos de Atributos.
- ID: TDE-KB-080-DEF-TABLA-EJEMPLOS-ATRIBUTOS-01
- [cite_start]Req: La estructura de tabla se preserva según la guía STS [cite: 316-317].

| Tipo de Atributo | Ejemplos Comunes | Ejemplos Adicionales |
| :--- | :--- | :--- |
| Identificadores Directos | - Nombre<br>- Email<br>- Teléfono móvil<br>- RUT<br>- Pasaporte<br>- Certificado de nacimiento<br>- Nombre de usuario | N/A |
| Identificadores Indirectos | - Edad<br>- Género<br>- Carrera<br>- Fecha de nacimiento<br>- Dirección<br>- Código postal<br>- Dirección laboral<br>- Nombre empresa<br>- Estado civil | - Altura<br>- Peso<br>- Dirección IP<br>- Matrícula vehículo<br>- N° bastidor vehículo<br>- Localización GPS |
| Atributos Objetivos | - Origen étnico<br>- Afiliación política/sindical<br>- Situación socioeconómica<br>- Convicciones ideológicas/filosóficas<br>- Creencias religiosas | - Datos de salud/perfil biológico<br>- Datos biométricos<br>- Datos vida sexual/orientación/identidad de género<br>- Transacciones (compras)<br>- Sueldo<br>- Calificación crediticia<br>- Póliza de seguro<br>- Diagnóstico médico<br>- Estado de vacunación |

### 2.5. Estados de los Datos

ID: TDE-KB-080-CONCEPTOS-ESTADOS-DATOS-01

- Cpt: Datos Desidentificados.
- ID: TDE-KB-080-DEF-DATO-DESIDENTIFICADO-01
- Def: Datos procesados para eliminar/modificar identificadores directos.
- Ctx: Posibilidad de reidentificación minimizada, no eliminada. Podrían ser reidentificados bajo ciertas condiciones.

- Cpt: Datos Anonimizados.
- ID: TDE-KB-080-DEF-DATO-ANONIMIZADO-01
- Def: Datos que originalmente permitían identificar, pero tras proceso de anonimización, la reidentificación es imposible.
- Res: Deja de ser un dato personal.

- Cpt: Datos Seudonimizados.
- ID: TDE-KB-080-DEF-DATO-SEUDONIMIZADO-01
- Def: Tratamiento de datos personales que impide atribuirlos a un titular sin usar información adicional.
- Req: Información adicional debe figurar por separado y estar sujeta a medidas técnicas/organizativas de seguridad.

- Cpt: Dato Sintético.
- ID: TDE-KB-080-DEF-DATO-SINTETICO-01
- Def: Datos generados artificialmente, sin correspondencia directa con datos reales.
- Purp: Uso en análisis y procesos sin comprometer privacidad.

- Cpt: Datos Abiertos.
- ID: TDE-KB-080-DEF-DATO-ABIERTO-01
- Def: Dato digital con características técnicas/jurídicas para ser usado, reutilizado y redistribuido libremente por cualquier persona/entidad.

### 2.6. Procesos de Tratamiento

ID: TDE-KB-080-CONCEPTOS-PROCESOS-01

- Cpt: Desidentificar.
- ID: TDE-KB-080-DEF-PROCESO-DESIDENTIFICAR-01
- Def: Eliminación de identificadores directos (nombre, RUT, etc.).
- Warn: Erróneamente confundido con anonimización. Es solo el primer paso.

- Cpt: Anonimización.
- ID: TDE-KB-080-DEF-PROCESO-ANONIMIZACION-01
- Def: Procedimiento irreversible donde un dato personal no puede vincularse/asociarse a una persona determinada.
- Mech: Destrucción/eliminación del nexo con la información identificatoria.
- Ctx: Riesgo Residual. Siempre subsiste un riesgo residual de reidentificación.
- Cause: (a) Posible combinación de datos o nuevas tecnologías; (b) Errores o modificaciones en el manejo de datos.
- Res: Un dato anonimizado deja de ser un dato personal.
- Src: PDL.

- Cpt: Seudonimización.
- ID: TDE-KB-080-DEF-PROCESO-SEUDONIMIZACION-01
- Def: Tratamiento de datos personales para que no puedan atribuirse a un titular sin información adicional.
- Req: Información adicional debe estar separada y protegida.
- Src: PDL.

- Cpt: Minimización de Datos.
- ID: TDE-KB-080-DEF-PROCESO-MINIMIZACION-01
- Def: Limitar recolección, almacenamiento y uso de datos personales a lo estrictamente necesario para el propósito especificado.
- Res: Reduce riesgo de violaciones de privacidad.

- Cpt: Clase de Equivalencia.
- ID: TDE-KB-080-DEF-CLASE-EQUIVALENCIA-01
- Def: Grupo de registros en una base de datos modificados para ser idénticos.
- Purp: Evitar vinculación directa de un registro a un individuo.
- Mech: Cada registro es indistinguible de al menos 'k-1' otros registros en el mismo conjunto.
- Ref: TDE-KB-080-TECNICAS-GENERALIZACION-01.

## 3. Riesgos de Reidentificación

ID: TDE-KB-080-RIESGOS-01
Def: Riesgos que surgen al tratar de proteger la identidad en conjuntos de datos.

- Cpt: Singularización.
- ID: TDE-KB-080-RIESGOS-SINGULARIZACION-01
- Def: Posibilidad de que los datos puedan usarse para identificar a una persona basándose en información única o una combinación de atributos.

- Cpt: Vinculabilidad.
- ID: TDE-KB-080-RIESGOS-VINCULABILIDAD-01
- Def: Capacidad de conectar dos o más registros (dentro del mismo o diferentes conjuntos de datos) que, combinados, pueden identificar a una persona.

- Cpt: Inferencia.
- ID: TDE-KB-080-RIESGOS-INFERENCIA-01
- Def: Posibilidad de deducir detalles específicos (a menudo sensibles) sobre una persona utilizando los datos disponibles, incluso si están modificados.

## 4. Framework del Proceso de Anonimización

ID: TDE-KB-080-PROCESO-01
Cpt: Etapas generales y orientativas.
Warn: No aborda aspectos técnicos detallados ni metodologías específicas.

### 4.1. Fase 1: Identificar Objetivos

ID: TDE-KB-080-PROCESO-FASE1-01
Req: Diseño del proceso debe estar orientado a objetivos específicos.
Ex: Publicación como datos abiertos, uso interno restringido.
Cpt: Gobernanza.

- Req: Para uso restringido, incorporar acuerdos de confidencialidad con cláusulas sobre reidentificación y protección.
- Req: Definir claramente la unidad y funcionarios responsables del proceso.
- Req: Responsables deben tener conocimiento profundo de los contenidos de la base de datos.

### 4.2. Fase 2: Clasificación de Atributos

ID: TDE-KB-080-PROCESO-FASE2-01
Purp: Clasificar adecuadamente los atributos de datos antes de la desidentificación.
Proc: Flujo de Decisión.

- 1. Pregunta: ¿Atributo es vital para el caso de uso?
- - Res: No -> Eliminar atributo. Ref: TDE-KB-080-DEF-PROCESO-MINIMIZACION-01.
- - Res: Si -> Proceder al paso 2.
- 2. Pregunta: ¿Atributo es un valor único?
- - Res: Si -> Clasificación probable: Identificador Directo. Ref: TDE-KB-080-DEF-ID-DIRECTO-01.
- - Res: No -> Proceder al paso 3.
- 3. Pregunta: ¿Atributo puede encontrarse en otras fuentes de datos (públicas/privadas)?
- - Res: Si -> Proceder al paso 4.
- - Res: No -> Clasificación probable: Identificador Indirecto. Ref: TDE-KB-080-DEF-ID-INDIRECTO-01.
- 4. Resultado: Clasificación probable -> Atributo Objetivo. Ref: TDE-KB-080-DEF-ATRIBUTO-OBJETIVO-01.

### 4.3. Fase 3: Desidentificación de Datos

ID: TDE-KB-080-PROCESO-FASE3-01
Obj: Balancear utilidad de datos con necesidad de privacidad.
Act: Eliminación/modificación de identificadores (directos e indirectos).
Dep: Nivel de privacidad requerido y contexto de uso determinan el alcance.
Warn: Remover solo identificadores directos puede ser insuficiente.
Req: Evaluar y ajustar identificadores indirectos para prevenir reidentificación por interrelación con otras fuentes.
Cpt: Uso de Seudónimos.

- Cond: Útil en situaciones específicas para mantener vínculos con individuo original sin comprometer identidad.
- Ctx: Casos de Uso.
- - Purp: Fusión de Datos. Ctx: Permite combinar registros de diversas fuentes.
- - Purp: Análisis Múltiples Registros. Ctx: Permite análisis profundo manteniendo confidencialidad.
- - Purp: Generación Datos Sintéticos. Ctx: Permite desarrollar/probar aplicaciones sin datos reales.
- Req: Requisitos del Seudónimo.
- - Req: Debe ser único para cada identificador directo.
- - Req: Diseño debe impedir reversión por terceros no autorizados.
- - Ex: Código generado aleatoriamente, sin relación matemática/lógica con dato original (e.g., "José" -> "A3#m9Z!").
- Req: Gobernanza. Mantener una tabla segura (cifrada, acceso restringido) que vincule identificadores directos con seudónimos para gestión y cumplimiento legal.

Cpt: Ejemplos de Desidentificación.

- ID: TDE-KB-080-PROCESO-FASE3-EJEMPLOS-01
- Cpt: Ejemplo 1 - Eliminación de Identificador Directo.
- - Act: Se elimina la columna 'Nombre'.
- - Warn: Individuos podrían ser reidentificados al cruzar con otras fuentes públicas (e.g., perfiles redes sociales).
| Edad | Serie Favorita |
| :--- | :--- |
| 54 | The Big Bang Theory |
| 30 | Friends |
| 23 | Stranger things |
- Cpt: Ejemplo 2 - Seudonimización con Token.
- - Act: Se reemplaza 'Nombre' por 'Token' único y robusto.
- - Purp: Permitir vinculación interna sin revelar identidad.
| Token | Edad | Serie Favorita |
| :--- | :--- | :--- |
| 1234 | 54 | The Big Bang Theory |
| A3#m9Z! | 30 | Friends |
| 98gv$$M | 23 | Stranger things |

### 4.4. Fase 4: Aplicación de Técnicas

ID: TDE-KB-080-PROCESO-FASE4-01
Act: Seleccionar y aplicar técnicas específicas para tratar identificadores indirectos y atributos objetivos.
Obj: Impedir asociación fácil con datos personales identificables.
Req: Equilibrar protección de privacidad vs. capacidad analítica de los datos.

### 4.5. Fase 5: Finalización y Mantenimiento

ID: TDE-KB-080-PROCESO-FASE5-01

- Act: Realizar evaluación rigurosa de la utilidad de los datos anonimizados.
- Act: Documentar meticulosamente el balance privacidad/utilidad, técnicas aplicadas y ajustes.
- Purp: Documentación para auditoría y replicabilidad.
- Req: Cada entidad debe definir y aplicar su propio método para evaluar y monitorear constantemente el riesgo de identificación.
- Just: Asegurar efectividad continua frente a cambios en tecnología y contextos de uso.

## 5. Catálogo de Técnicas de Anonimización

ID: TDE-KB-080-TECNICAS-01
Obj: Minimizar riesgos de reidentificación.
Warn: La aplicabilidad y efectividad dependen del tipo de dato, contexto y legislación.
Rec: Consultar con expertos para determinar la técnica más adecuada.

### 5.1. Enfoque: Enmascaramiento (Masking)

ID: TDE-KB-080-TECNICAS-ENMASCARAMIENTO-01
Def: Ocultar o eliminar información para evitar identificación directa.

- Cpt: Supresión de Registros
- ID: TDE-KB-080-TECNICAS-ENMASC-SUPRESION-01
| Propiedad | Descripción |
| :--- | :--- |
| Def | Eliminación de un registro completo. Afecta a múltiples atributos simultáneamente. |
| Ctx | Útil para eliminar registros atípicos (outliers) que son únicos o no cumplen otros criterios. Atípicos son más fáciles de reidentificar. |
| Instr | Eliminar por completo el registro. La supresión debe ser permanente, no un ocultamiento temporal. |
| Rec | Considerar impacto en análisis de datos (e.g., afecta precisión estadística de promedio, mediana). |

- Cpt: Enmascaramiento de Caracteres
- ID: TDE-KB-080-TECNICAS-ENMASC-CARACTERES-01
| Propiedad | Descripción |
| :--- | :--- |
| Def | Sustitución de caracteres originales por alternativos (e.g., asteriscos, "X") para ocultar información sensible sin alterar estructura. |
| Ctx | Útil para proteger datos donde solo una parte es sensible (e.g., números de ID, emails) y el resto puede ser visible. |
| Instr | Reemplazar caracteres específicos manteniendo el formato original. |
| Rec | Asegurar que el método no sea predecible. Considerar enmascaramiento completo para ocultar totalmente la información. |

- Cpt: Cifrados
- ID: TDE-KB-080-TECNICAS-ENMASC-CIFRADOS-01
| Propiedad | Descripción |
| :--- | :--- |
| Def | Convierte datos legibles a formato codificado, reversible solo con una clave específica. |
| Ctx | Útil para transmisión de datos sensibles en redes inseguras o almacenamiento en sistemas vulnerables. |
| Instr | Cifrar datos antes de transmitir/almacenar con algoritmos robustos. Gestionar claves adecuadamente. |
| Rec | Revisar robustez de algoritmos periódicamente. Implementar políticas de rotación de claves. |

### 5.2. Enfoque: Aleatorización

ID: TDE-KB-080-TECNICAS-ALEATORIZACION-01
Def: Modificar o alterar la veracidad de los datos a nivel individual, respetando la distribución global.
Obj: Reducir vinculabilidad e inferencia.
Warn: Por sí sola no garantiza protección.
Rec: Combinar con otros métodos (e.g., filtrado, generalización).

- Cpt: Adición de Ruido
- ID: TDE-KB-080-TECNICAS-ALEAT-RUIDO-01
| Propiedad | Descripción |
| :--- | :--- |
| Def | Modifica datos originales con variaciones aleatorias para disociarlos de identificadores. |
| Ctx | Útil cuando los datos deben mantener estructura básica para análisis, pero requieren reducción de precisión. |
| Instr | Aplicar ruido de manera uniforme y precisa. Ajustar nivel de ruido para no comprometer calidad analítica. |
| Rec | Asegurar que la calidad y utilidad de los datos no se vean comprometidas. |

- Cpt: Permutación o Intercambio
- ID: TDE-KB-080-TECNICAS-ALEAT-PERMUTACION-01
| Propiedad | Descripción |
| :--- | :--- |
| Def | Mezcla valores de atributos en un conjunto de datos, asignándolos aleatoriamente a diferentes registros. |
| Ctx | Útil en análisis estadísticos donde es crucial ocultar identidades (e.g., datos financieros, médicos). |
| Instr | Asegurar que la permutación preserve correlaciones lógicas y estructura. Evitar permutar atributos objetivo con riesgo de identificación. |
| Rec | Validar que no se introducen distorsiones. Combinar con otras técnicas para mayor robustez. |

- Cpt: Privacidad Diferencial
- ID: TDE-KB-080-TECNICAS-ALEAT-PRIVACIDAD-DIFERENCIAL-01
| Propiedad | Descripción |
| :--- | :--- |
| Def | Añade ruido deliberadamente a los datos/consultas para que los resultados de análisis sean menos identificables a nivel individual. |
| Ctx | Ideal para compartir datos agregados sin revelar identidades. |
| Instr | Determinar cantidad de ruido necesaria para equilibrar privacidad e integridad. Supervisar y ajustar el nivel de ruido continuamente. |
| Rec | Mantener registro detallado de consultas. Evitar motores de búsqueda abiertos que permitan trazabilidad. Limitar resultados a datos estadísticos. |

### 5.3. Enfoque: Generalización

ID: TDE-KB-080-TECNICAS-GENERALIZACION-01
Def: Diluir atributos específicos ajustando sus escalas o magnitudes.
Ex: Reemplazar ciudad por región; fecha específica por mes.
Warn: No garantiza anonimización completa por sí sola. Requiere aplicación adecuada y conjunta con otras técnicas.

- Cpt: K-Anonimidad
- ID: TDE-KB-080-TECNICAS-GENERAL-K-ANONIMIDAD-01
| Propiedad | Descripción |
| :--- | :--- |
| Def | Asegura que cada registro sea indistinguible de al menos 'k-1' otros registros (Clase de Equivalencia). Ref: TDE-KB-080-DEF-CLASE-EQUIVALENCIA-01. |
| Ctx | Útil para compartir datos dentro de un grupo sin revelar identidades, especialmente en grandes volúmenes. |
| Instr | Establecer un valor de 'k' que equilibre privacidad y utilidad. Ajustar registros para que cada clase de equivalencia sea uniforme. |
| Rec | Monitorear eficacia regularmente. Un 'k' muy alto puede reducir utilidad; un 'k' muy bajo compromete privacidad. |

- Cpt: Diversidad-L y Proximidad-T
- ID: TDE-KB-080-TECNICAS-GENERAL-L-DIVERSIDAD-T-PROXIMIDAD-01
| Propiedad | Descripción |
| :--- | :--- |
| Def | Extensiones de K-anonimato para mejorar protección contra inferencia. Diversidad-L: asegura 'L' valores únicos para atributos sensibles. Proximidad-T: ajusta distribución de atributos a la distribución general. |
| Ctx | Útil en bases de datos donde la preservación de atributos estadísticos es importante. |
| Instr | Elegir valores de L y T cuidadosamente. Verificar y ajustar clases de equivalencia para cumplir los estándares. |
| Rec | Asegurar que valores dentro de cada grupo sean uniformes. Revisar y actualizar periódicamente. |

### 5.4. Enfoque: Seudonimización

ID: TDE-KB-080-TECNICAS-SEUDONIMIZACION-01
Ref: TDE-KB-080-DEF-PROCESO-SEUDONIMIZACION-01.

| Propiedad | Descripción |
| :--- | :--- |
| Def | Sustituye identificadores por valores alterados (tokens, hashes, etc.). No elimina totalmente la posibilidad de identificación, pero la dificulta. |
| Ctx | Útil cuando es crucial mantener cierto grado de vinculación entre datos sin revelar la identidad. |
| Mech | - Cifrado con clave secreta.<br>- Función hash (difícil de revertir).<br>- Función hash con clave almacenada.<br>- Descomposición en tokens. |
| Rec | Usar diferentes claves/seudónimos en distintos conjuntos de datos. Proteger las claves de acceso no autorizado. |

## 6. Gobernanza del Proceso

ID: TDE-KB-080-GOBERNANZA-01
Purp: Evaluar y gestionar los riesgos y aplicaciones de las técnicas de anonimización.

### 6.1. Matriz de Mitigación de Riesgo por Técnica

ID: TDE-KB-080-GOBERNANZA-MATRIZ-RIESGO-01
Cpt: Niveles de Mitigación.

- Def: Eficaz. La técnica es efectiva para mitigar el riesgo.
- Def: Parcial. La técnica puede mitigar el riesgo en ciertas circunstancias.
- Def: Ineficaz. La técnica NO mitiga eficazmente el riesgo.

| Tipo de técnica | Técnica | Riesgo de Singularización | Riesgo de Vinculabilidad | Riesgo de Inferencia |
| :--- | :--- | :--- | :--- | :--- |
| Enmascaramiento | Supresión de registros | Ineficaz | Ineficaz | Ineficaz |
| | Enmascaramiento de caracteres | Ineficaz | Ineficaz | Ineficaz |
| | Cifrados | Ineficaz | Ineficaz | Parcial |
| Aleatorización | Adición de ruido | Ineficaz | Parcial | Parcial |
| | Permutación o intercambio | Ineficaz | Parcial | Parcial |
| | Privacidad diferencial | Parcial | Parcial | Parcial |
| Generalización | K-Anonimidad | Eficaz | Ineficaz | Ineficaz |
| | Diversidad-L | Eficaz | Ineficaz | Parcial |
| | Proximidad-T | Eficaz | Ineficaz | Parcial |
| Seudonimización | Cifrado por hash | Ineficaz | Ineficaz | Parcial |
| | Tokenización | Ineficaz | Ineficaz | Ineficaz |

### 6.2. Matriz de Aplicación por Caso de Uso

ID: TDE-KB-080-GOBERNANZA-MATRIZ-APLICACION-01
Warn: Ejemplos ilustrativos. La elección final depende del contexto específico.

| Casos de uso | Técnicas de anonimización sugeridas |
| :--- | :--- |
| Publicación de Datos Abiertos | Supresión de registros, K-Anonimidad, Diversidad-L, Proximidad-T |
| Compartir datos entre Organizaciones| Supresión de registros, K-Anonimidad, Diversidad-L, Proximidad-T |
| Intercambio interno (datos desidentificados) | Supresión de registros, Enmascaramiento, Cifrado, Seudonimización |
| Intercambio interno (datos anonimizados) | Supresión de registros, Enmascaramiento de caracteres, Adición de ruido, Permutación o intercambio, Privacidad Diferencial |

### 6.3. Recomendaciones Adicionales

ID: TDE-KB-080-GOBERNANZA-RECOMENDACIONES-01

- Rec: Calcular el riesgo de identificación ANTES de aplicar técnicas de anonimización.
- Purp: Entender el potencial de reidentificación original y cómo se modifica.
- Res: Ayuda a seleccionar la técnica más adecuada; guía la configuración de parámetros; maximiza protección sin comprometer excesivamente la utilidad.
- Req: Realizar evaluación continua del riesgo durante y después del proceso.
- Just: Asegurar que los datos permanezcan seguros frente a nuevas vulnerabilidades y técnicas de análisis.

## 7. Herramientas de Código Abierto

ID: TDE-KB-080-HERRAMIENTAS-01
Purp: Facilitar el proceso de anonimización de datos personales sin costo.

| Herramienta | Descripción | URL |
| :--- | :--- | :--- |
| ARX | Software de código abierto para anonimizar datos personales. | <https://arx.deidentifier.org/> |
| Amnesia | Herramienta local de anonimización de datos. Soporta garantías de k-anonimidad y km-anonimidad. | <https://amnesia.openaire.eu/> |

## 8. Casos de Uso

ID: TDE-KB-080-CASOS-USO-01
Purp: Describir contextos fundamentales donde se aplican técnicas de anonimización.

- Cpt: Caso 1: Publicación de Datos Abiertos
- ID: TDE-KB-080-CASOS-USO-DATOS-ABIERTOS-01
- Obj: Permitir a organizaciones compartir información valiosa sin comprometer la privacidad.

- Cpt: Caso 2: Compartir Datos entre Organizaciones
- ID: TDE-KB-080-CASOS-USO-INTER-ORG-01
- Obj: Proteger datos personales durante colaboraciones o servicios tercerizados.

- Cpt: Caso 3: Intercambio Interno de Datos
- ID: TDE-KB-080-CASOS-USO-INTRA-ORG-01
- Obj: Utilizar datos anonimizados para intercambio interno.
- Cond: El intercambio no requiere datos personales detallados (e.g., análisis de tendencias).
- Cond: Los datos involucrados son de naturaleza sensible (e.g., información financiera).

## 9. Conclusión

ID: TDE-KB-080-CONCLUSION-01

- Cpt: Resumen de la Guía
- ID: TDE-KB-080-CONCLUSION-RESUMEN-01
- Purp: Proporcionar visión general de técnicas de anonimización para gestión segura de datos personales.
- Ctx: Explora enfoques y herramientas (libres/sin costo) para implementación efectiva.

- Cpt: Advertencia sobre Alcance
- ID: TDE-KB-080-CONCLUSION-ADVERTENCIA-01
- Warn: La guía no propone una metodología específica para evaluación de riesgo ni detalla la aplicación técnica en profundidad.
- Rec: Colaborar con expertos para adaptar técnicas a necesidades y contextos específicos.

- Cpt: Mensaje Final
- ID: TDE-KB-080-CONCLUSION-MENSAJE-FINAL-01
- Ctx: La guía es un punto de partida para la educación y concienciación sobre la protección de la privacidad.
- Req: Compromiso continuo y adaptación a nuevos desafíos son esenciales para la efectividad.
- Obj: Cumplir regulaciones, respetar derecho a la privacidad y mantenerse efectivo ante cambios.
