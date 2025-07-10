# Guía de Apoyo a Norma Técnica de Seguridad y Ciberseguridad

ID: GUIA-CIBER-MASTER-01
Version: 1.0.0
Status: Published
Human-Creator: STSador
Human-Editor: STSador
Model-Collaborator: IA-GEMINI
Creation-Date: 2025-07-06
Modification-Date: 2025-07-06
Primary-Source: G4-GUIA-SEG-CIBER-01
Ref-STS-Guide: GUIDE-STS-MASTER-01

## 1. Introducción

ID: GUIA-CIBER-INTRO-01
Purp: Establecer el marco de aplicación de la guía y guiar la implementación de controles de seguridad/ciberseguridad en OAE.
Dest: Órganos de la Administración del Estado (OAE).
Fnd: Cumplimiento del Art. 12, Norma Técnica de Seguridad de la Información y Ciberseguridad.
Fnd: Buenas prácticas internacionales, NCH-ISO 27000, marco NIST, D.S. N°83/2015 MINSEGPRES.
Cpt: Flexibilidad.

- Def: OAEs pueden usar otros estándares si son consistentes y tienen efectos equivalentes.
Req: Consistencia con Política Nacional Ciberseguridad, Ley Marco Ciberseguridad y directrices SEGOBDI.

## 2. Definiciones

ID: GUIA-CIBER-DEFINITIONS-01
Purp: Complementar las definiciones de la Norma Técnica.

- Cpt: Apetito de Riesgo. Def: Cantidad de riesgo que una organización asume para alcanzar objetivos estratégicos.
- Cpt: Ataque de Día Cero. Def: Ataque basado en vulnerabilidad desconocida por el proveedor, sin parche existente. Ctx: Probabilidad de éxito es alta.
- Cpt: Custodio. Def: Encargado de otorgar y supervisar accesos a activos de información bajo su custodia.
- Cpt: Dueño de Activo. Def: Encargado de velar por inventario, clasificación y actualización de activos según esquema institucional.
- Cpt: Evento Precursor. Def: Indicio de que puede ocurrir un incidente en el futuro.
- Cpt: Plan de Continuidad. Def: Plan con lineamientos para mantener continuidad operativa de plataformas electrónicas ante fallas.
- Cpt: Planes de Recuperación. Def: Planes con acciones para restaurar normalidad de funcionamiento post-disrupción en el menor tiempo posible.
- Cpt: Planes de Respuesta. Def: Planes con procedimientos para enfrentar un incidente inmediatamente ocurrido. Ctx: Activación post-confirmación de incidente.
- Cpt: Redundancia. Def: Duplicación de componentes (software/hardware) para asegurar disponibilidad ante fallas.
- Cpt: Tolerancia al Riesgo. Def: Cantidad de riesgo del entorno (ej. volatilidad) que una institución puede tolerar.

## 3. Política de Seguridad y Ciberseguridad

ID: GUIA-CIBER-POLICY-01
Purp: Establecer directrices generales de seguridad y ciberseguridad en el OAE.
Req: Cada OAE debe elaborar una Política de Seguridad de la Información y Ciberseguridad.
Fnd: Art. 5, Norma Técnica de Seguridad de la Información y Ciberseguridad.

- Obj: Establecer directrices generales.
- Obj: Velar por seguridad de componentes (SW, HW, sistemas) y datos.
- Obj: Contener visión estratégica del OAE en la materia.
- Obj: Definir lineamientos para alcanzar objetivos.
Req: Realizar diagnóstico del estado actual (sistemas, activos, procesos) para generar línea base.
Ctx: Diagnóstico es la base para la Función de Identificación. Ref: GUIA-CIBER-FN-IDENTIFY-01.
Req: Aprobación por Jefe(a) de Servicio para asegurar compromiso directivo.
Req: Política debe indicar procedimiento y frecuencia de actualización. Rec: Anual.
Cause: Actualización impulsada por cambios de entorno, nuevas hipótesis de escenario u otros factores.
Fnd: Pilares de resguardo, confidencialidad, integridad, disponibilidad de la información.
Mech: Propiciar desarrollo seguro y privacidad desde el diseño.
Req: La política debe identificar y desarrollar los puntos mínimos definidos en las siguientes secciones.

### 3.1. Objetivos de la Política

ID: GUIA-CIBER-POLICY-OBJECTIVES-01
Purp: Definir metas y métricas de la política.
Req: Contener objetivos esenciales y los indicadores para medir su cumplimiento.

- Cpt: Objetivos Generales.
  - Ex: Asegurar confidencialidad, integridad y disponibilidad de activos de información.
  - Ex: Reflejar compromiso y fomento de cultura de seguridad.
- Cpt: Objetivos Específicos.
  - Ex: Gestionar adecuadamente tratamiento de incidentes de seguridad.
  - Ex: Generar capacitación y sensibilización para funcionarios.

### 3.2. Alcance de la Política

ID: GUIA-CIBER-POLICY-SCOPE-01
Purp: Determinar el ámbito de aplicación de la política.
Def: Activo de Información. Ctx: Datos cuyo tratamiento es esencial para el funcionamiento del OAE.

- Req: Activos deben ser identificados, descritos y clasificados.
- Req: Asignar un dueño y un custodio a cada activo. Ref: GUIA-CIBER-FN-IDENTIFY-ASSETS-MANAGEMENT-01.
Act: OAE debe implementar acciones para alcanzar estándares de seguridad apropiados.

### 3.3. Marco Regulatorio

ID: GUIA-CIBER-POLICY-LEGISLATION-01
Purp: Identificar el marco normativo aplicable.
Req: Identificar, definir y comprender el contexto regulatorio (actual y previsto) aplicable al OAE.

### 3.4. Roles y Responsabilidades

ID: GUIA-CIBER-POLICY-ROLES-01
Purp: Especificar roles y responsabilidades institucionales.
Req: Considerar y coordinar roles de responsable institucional de seguridad y responsable de activos de información.
Decision-OAE: Determinar si ambos roles se unifican en una persona.
Rec: Dependencia preferible de Jefatura de Servicio, no de áreas de tecnología.
Just: Cumplirán funciones de auditoría y directrices transversales.
Prohib: El desempeño de estas funciones no puede ser externalizado.

- Cpt: Rol de Responsable Institucional.
  - Mssn: Velar por la seguridad y ciberseguridad en el OAE.
  - Resp: Asegurar desarrollo, cumplimiento y actualización de la Política.
  - Resp: Gestionar la administración de la seguridad.
  - Ctx: Equivalencias definidas en Inst. Presidencial N°8 (2018), D.S. N°7 (2023), Ley N°21.663.
- Cpt: Rol de Responsable de Activos.
  - Mssn: Realizar identificación, clasificación y priorización de activos.
  - Resp: Gestionar el riesgo y niveles de seguridad asociados.
  - Resp: Designar roles específicos (dueño, custodio) para cada activo individual. Ref: GUIA-CIBER-FN-IDENTIFY-ASSETS-MANAGEMENT-01.

### 3.5. Clasificación de la Información

ID: GUIA-CIBER-POLICY-INFO-CLASSIFICATION-01
Purp: Definir métodos para clasificar la información.
Req: Contener métodos para identificar criticidad de cada activo de información.
Obj: Proveer seguridad y restricción de acceso concordante. Ref: GUIA-CIBER-POLICY-ACCESS-CONTROL-01.
Req: La clasificación debe vincularse a nivel de sensibilidad y criticidad para el OAE.

### 3.6. Gestión de Riesgos

ID: GUIA-CIBER-POLICY-RISK-MANAGEMENT-01
Purp: Establecer lineamientos para la gestión de riesgos.
Req: Contener aspectos generales para evaluación y tratamiento de riesgos.
Req: Indicar objetivos del órgano, forma de rendición de cuentas y métricas del proceso.

### 3.7. Gestión de Vulnerabilidades

ID: GUIA-CIBER-POLICY-VULN-MANAGEMENT-01
Purp: Definir directrices para el manejo de vulnerabilidades técnicas.

- Req: Incluir medidas adecuadas para identificación de vulnerabilidades técnicas.
- Req: Incluir directrices para determinar funciones y responsabilidades internas para la gestión (monitoreo, evaluación, tratamiento).

### 3.8. Control de Acceso

ID: GUIA-CIBER-POLICY-ACCESS-CONTROL-01
Purp: Regular el acceso a sistemas y datos.

- Req: Procedimientos de acceso y distribución de identidades para reducir riesgos (suplantación, accesos no autorizados).
- Req: Definición de responsabilidades de funcionarios/asesores sobre los accesos.
- Req: Procedimiento de recuperación de control de credenciales en caso de compromiso.

### 3.9. Respaldos y Restauración

ID: GUIA-CIBER-POLICY-BACKUPS-01
Purp: Definir el proceso de copias de seguridad.

- Req: Mecanismos, procesos y requisitos para copias de seguridad (información, programas, configuraciones).
- Req: Proceso de restauración de software relevante.
- Req: Verificar consistencia de respaldos periódicamente para asegurar calidad.
- Req: Dejar registro de los chequeos de consistencia.
- Req: Contener definiciones del proceso de restauración post-incidente.
- Req: Procedimiento debe ceñirse a controles criptográficos y de eliminación. Ref: GUIA-CIBER-POLICY-CRYPTOGRAPHY-01, GUIA-CIBER-POLICY-ELIMINATION-01.

### 3.10. Continuidad Operacional

ID: GUIA-CIBER-POLICY-CONTINUITY-01
Purp: Establecer lineamientos para la continuidad operativa.
Req: Contener lineamientos y alcances para construir el plan de continuidad operativa y contingencia.
Obj: Mantener continuidad de plataformas ante fallas.
Req: Plan debe cubrir desde la identificación del equipo de respuesta hasta la aprobación de planes de recuperación y respuesta.
Warn: Operadores de importancia vital (Ley 21.663) tienen obligación de elaborar e implementar planes de continuidad. Incumplimiento es infracción sancionable.

### 3.11. Criptografía

ID: GUIA-CIBER-POLICY-CRYPTOGRAPHY-01
Purp: Definir directrices para el uso de criptografía.

- Req: Directrices para uso eficiente y adecuado de mecanismos criptográficos.
- Obj: Proteger confidencialidad, integridad, no-repudio y autenticación.
- Resp: Dueño del Activo debe definir nivel de protección necesario por cada activo, según riesgo.
- Req: Contener directrices para uso de criptografía en todo el ciclo de vida de la información (transporte, almacenamiento).

### 3.12. Privacidad y Protección de Datos

ID: GUIA-CIBER-POLICY-PRIVACY-01
Purp: Establecer lineamientos para protección de datos personales.
Req: Contener lineamientos para adoptar resguardos desde el diseño para protección de datos personales.
Req: Debe ser conforme a la normativa vigente de protección de datos.

### 3.13. Eliminación Segura de Información

ID: GUIA-CIBER-POLICY-ELIMINATION-01
Purp: Definir procesos para la eliminación segura de información.
Req: Contener procesos formales para eliminación segura de elementos (cuando no son útiles, por exigencia legal, etc.).

- Req: Respetar requerimientos de retención de información legalmente aplicables.
- Req: Considerar mecanismos de registro de cada eliminación.
- Req: Considerar directrices de Norma Técnica de Documentos y Expedientes Electrónicos (registro de trazabilidad, incorporación a política de gestión documental).

## 4. Marco de Trabajo

ID: GUIA-CIBER-FRAMEWORK-01
Purp: Estructurar la implementación de la política a través de funciones, categorías y subcategorías.
Obj: Resguardar la confidencialidad, integridad y disponibilidad de la información, documentos y comunicaciones.
Fnd: Principalmente estructura de dominios NIST.
Cpt: Se complementa con estándares como CIS, COBIT 5, ISO 27001/27002 (versiones NCH/INN).

## 5. Función: Identificar

ID: GUIA-CIBER-FN-IDENTIFY-01
Def: Acciones para lograr entendimiento organizacional y administrar riesgos de seguridad para procesos, personas y tecnología.
Req: Realizar diagnóstico inicial (auditoría interna, entrevistas, etc.) para establecer línea base.
Rec: Usar herramientas de apoyo como MITRE ATT&CK, NIST CSF, CIS Controls, ISO/IEC 27001.

### 5.1. Comprensión del Contexto Organizacional

ID: GUIA-CIBER-FN-IDENTIFY-CONTEXT-01
Purp: Comprender el entorno interno y externo del OAE.
Act: Analizar, evaluar y comunicar aspectos internos/externos que afecten el desempeño en seguridad.

- Act: Considerar necesidades y misiones de actores vinculados en materia de seguridad.
- Act: Analizar aspectos legales/regulatorios, obligaciones contractuales, definiciones estratégicas, interdependencias.
Req: Generar artefacto como un diagrama de entorno con identificación de actores relevantes.

### 5.2. Gobernanza

ID: GUIA-CIBER-FN-IDENTIFY-GOVERNANCE-01
Purp: Establecer un marco de gestión y relaciones entre actores.
Obj: Comprender políticas, procedimientos y procesos para monitorear y gestionar requisitos y riesgos.
Res: Permite gestión adecuada, supervisión de planes y protección de activos de información.

### 5.3. Gestión de Activos

ID: GUIA-CIBER-FN-IDENTIFY-ASSETS-MANAGEMENT-01
Purp: Identificar y definir roles y responsabilidades para la protección de activos.
Cpt: Subcategorías: Inventario, Dueños, Custodios, Clasificación, Mapeo de comunicación.

#### 5.3.1. Inventario de Activos

ID: GUIA-CIBER-FN-IDENTIFY-ASSETS-INVENTORY-01
Req: OAEs deben inventariar activos de información (dispositivos físicos, software, BBDD, etc.).
Req: Activos deben documentarse y etiquetarse en un inventario de actualización periódica.
Rec: Se pueden usar definiciones de ITIL v4 para un CMDB.

#### 5.3.2. Dueños de Activos

ID: GUIA-CIBER-FN-IDENTIFY-ASSETS-OWNERS-01
Req: Cada activo inventariado debe tener un dueño asignado.
Mssn: Velar por el inventario, clasificación y actualización de los activos a su cargo.

- Resp: Clasificar según sensibilidad/criticidad.
- Resp: Establecer y revisar restricciones de acceso.
- Resp: Asegurar gestión en todo el ciclo de vida del activo.
- Resp: Tomar resguardos para la eliminación del activo.
Rec: Catalogar características adicionales (ubicación, tamaño, unidades responsables).

#### 5.3.3. Custodios de Activos

ID: GUIA-CIBER-FN-IDENTIFY-ASSETS-CUSTODIANS-01
Cpt: Rol. Def: Responsables de custodiar accesos a activos de información.
Mssn: Ocuparse de aspectos técnicos y de seguridad para permitir solo accesos autorizados, garantizando integridad, disponibilidad y confidencialidad.

#### 5.3.4. Clasificación de Activos

ID: GUIA-CIBER-FN-IDENTIFY-ASSETS-CLASSIFICATION-01
Resp: Responsable de los activos de información del OAE.
Act: Elaborar un esquema de clasificación y priorización.
Fnd: Basado en criticidad, sensibilidad, valor comercial, normativa.
Req: Aplicación transversal al órgano y consistente.

- Cpt: Ejemplo de Esquema (NCH27002). Fnd: Basado en impacto de revelación.
  - Nivel-1: Revelación sin daño.
  - Nivel-2: Revelación con perjuicio menor.
  - Nivel-3: Revelación con impacto significativo a corto plazo.
  - Nivel-4: Revelación con impacto serio (sanciones).
- Cpt: Ejemplo de Esquema (DS83). Fnd: Basado en confidencialidad.
  - Tipo-Publicos: No reservados ni secretos.
  - Tipo-Reservados: Conocimiento circunscrito a unidad específica.
  - Tipo-Secretos: Carácter secreto por legislación vigente (ej. Ley 20.285).
Req: OAEs deben mantener índice actualizado de actos secretos/reservados, según Ley de Transparencia.

#### 5.3.5. Mapeo de Flujo de Datos

ID: GUIA-CIBER-FN-IDENTIFY-ASSETS-DATAFLOW-01
Req: Desarrollar e implementar mecanismos para monitorear y controlar comunicación y flujo de datos.
Obj: Mitigar riesgos de revelación/modificación no autorizada.
Act: Mantener registro de emisores/receptores, privilegios y generar controles y respaldos.

### 5.4. Evaluación de Riesgos

ID: GUIA-CIBER-FN-IDENTIFY-RISK-ASSESSMENT-01
Purp: Establecer un proceso formal de gestión de riesgos.
Proc: Primero comprender vulnerabilidades/riesgos; luego establecer procesos de gestión según prioridades y tolerancias.
Rec: Usar herramientas de apoyo como Documento Técnico N°70 (C.A.I.G.G.), toolkits (OWASP, AGESIC).
Req: Proceso debe incluir como mínimo los siguientes puntos.

- SubCat-Contexto-Riesgo-01: Establecer a partir de evaluación de ámbitos internos/externos.
- SubCat-Tolerancia-Riesgo-01: Determinar y comunicar claramente criterios de tolerancia y apetito al riesgo. Ctx: Medidas de mitigación deben basarse en estos criterios.
- SubCat-Identificacion-Riesgo-01: Definir y documentar todos los riesgos de pérdida potencial. Identificar activos, procesos, amenazas, controles, vulnerabilidades, consecuencias. Incluir riesgos de servicios de terceros.
- SubCat-Analisis-Riesgo-01: Determinar impacto de pérdida potencial mediante análisis de escenarios (probabilidad x consecuencias). Ctx: Se pueden usar metodologías cualitativas o cuantitativas.
- SubCat-Evaluacion-Riesgo-01: Contrastar estimaciones de riesgo con niveles de tolerancia establecidos. Ctx: Base para toma de decisiones.
- SubCat-Tratamiento-Riesgo-01: Identificar y priorizar la mejor opción para abordar el riesgo.
  - Opcion-1: Tolerar/aceptar.
  - Opcion-2: Mitigar (con procedimiento o control).
  - Opcion-3: Transferir (a un tercero).
  - Opcion-4: Evitar (eliminando la fuente).
  - Req: Justificar opciones. Aceptación de riesgo requiere aprobación formal.
- SubCat-Comunicacion-Monitoreo-01: Hacer seguimiento y mantener registro actualizado de riesgos. Comunicar cambios. Mantener registro permanente con tratamiento especificado.

### 5.5. Gestión de la Cadena de Suministro

ID: GUIA-CIBER-FN-IDENTIFY-SUPPLY-CHAIN-01
Purp: Gestionar los riesgos asociados a la cadena de suministro y proveedores.
Req: Contratos con proveedores deben alinearse a la Política de Seguridad del OAE.
Req: Implementar políticas de gestión de contratos.

- Act: Inventario de Contratos. Ctx: Identificar proveedores, contrapartes técnicas, servicios, plazos.
- Act: Gestión de Riesgo. Ctx: Identificar, evaluar y establecer procesos de gestión de riesgo para la cadena de suministro cibernética.
- Act: Gestión de Servicio. Ctx: Monitorear, revisar y auditar regularmente provisión de servicios (vía SLAs).
Req: Para servicios en la nube:
- Req: Acuerdo de Servicio debe especificar roles y responsabilidades.
- Req: Acuerdo debe contener:
  - Protección de info al término del contrato.
  - Revisiones periódicas de cumplimiento técnico.
  - Pruebas periódicas de seguridad.
  - Auditorías periódicas.
  - Recolección y protección de evidencia.
- Req: Proveedor de nube debe especificar claramente en contrato las medidas de seguridad implementadas.
- Req: Modelo de Responsabilidades Compartidas debe indicarse claramente en el acuerdo.

## 6. Función: Proteger

ID: GUIA-CIBER-FN-PROTECT-01
Def: Acciones para desarrollar e implementar medidas de seguridad adecuadas para garantizar la entrega de servicios.

### 6.1. Gestión de Infraestructura y Accesos

ID: GUIA-CIBER-FN-PROTECT-INFRA-MGMT-01
Purp: Gestionar servidores, redes, identidad, autenticación y control de acceso.
Req: Acceso a activos (físicos, lógicos) debe restringirse a usuarios, procesos y dispositivos autorizados.

#### 6.1.1. Gestión de Servidores

ID: GUIA-CIBER-FN-PROTECT-SERVER-MGMT-01

- Req: Administración por usuarios con roles definidos y/o dispositivos autorizados.
- Req: Mantener registro de eventos (autenticaciones, operaciones) por mínimo 12 meses.
- Req: Mantener separación entre entornos de producción, pruebas, pre-producción y desarrollo.
- Req: Acceso seguro habilitado solo mediante redes seguras (ej. VPN), favoreciendo llaves criptográficas.
- Req: Configuración segura, no por defecto. Debe ser adecuada a necesidades y documentada.
- Req: Sincronización horaria con hora oficial chilena (SHOA).
- Req: Revisar, evaluar y mejorar continuamente capacidades de HW/SW.
- Req: Contar con redundancia para garantizar disponibilidad. Probar mecanismos frecuentemente.
- Req: Aplicaciones restringidas y justificadas, con parches y licenciamiento vigente. Establecer política de actualizaciones.
- Req: Mantenimiento realizado solo por personal autorizado y con registro.
- Req: Mantener SO y aplicativos actualizados según recomendaciones del fabricante.
  - Req: Solo instalar actualizaciones autorizadas y probadas.
  - Req: Ejecución por usuario competente.
  - Req: Mantener y actualizar plan de vuelta atrás (rollback).

#### 6.1.2. Gestión de Redes

ID: GUIA-CIBER-FN-PROTECT-NETWORK-MGMT-01

- Req: Correcta administración manteniendo separación de entornos.
- Req: Adecuada monitorización de eventos para identificar incidentes.
- Req: Accesos a redes internas monitoreados y solo para personal autorizado. Usar multifactor (2FA) para sistemas críticos.
- Req: Utilizar VPN para conexiones a redes internas. Rec: con segunda validación (ej. OTP).
- Req: Monitorear continuamente uso de puertos, protocolos y servicios.
- Req: Usar cortafuegos actualizado, con configuración adaptada (no de fábrica) y monitoreado.

#### 6.1.3. Gestión de Credenciales y Autenticación

ID: GUIA-CIBER-FN-PROTECT-CREDENTIAL-MGMT-01
Req: Implementar medios para distribuir autorizaciones con mínimo privilegio y según rol.

- Cpt: Gestión de Credenciales y Privilegios.
  - Req: Contar con procedimientos para otorgamiento, revocamiento y revisión continua de accesos.
  - Req: Proceso formal de entrega de accesos.
  - Req: Especificar mecanismos de mantención de llaves/contraseñas.
  - Rec: Tender a un modelo de roles, no asignación directa a usuarios.
- Cpt: Mecanismos de Autenticación y Contraseñas.
  - Req: Diseño del sistema debe considerar protección contra ataques en línea o fuera de línea.
  - Req: Política de contraseñas debe ser concordante con confidencialidad de la información. Rec: Usar estándar NIST sobre niveles de autenticación.
  - Req: Requerir claves largas (10+ caracteres) o prohibir claves de diccionarios públicos.
  - Req: Almacenamiento siempre cifrado, idealmente con One-Way Function.
  - Req: Evaluar implementación de Multi-Factor según confidencialidad.
  - Req: No requerir/forzar cambio periódico, a menos que haya sospecha de compromiso.
  - Req: Para autenticación con terceros, usar estándares como OAuth2, no almacenar credenciales temporalmente.
  - Req: Usar siempre comunicación encriptada.
  - Req: Nunca entregar credenciales por medios inseguros. Forzar cambio al primer uso.

### 6.2. Conciencia y Formación

ID: GUIA-CIBER-FN-PROTECT-AWARENESS-TRAINING-01
Purp: Capacitar al personal en seguridad y ciberseguridad.
Resp: OAE debe procurar capacitación a funcionarios y asesores según su rol.
Req: Desarrollar y mantener plan de capacitación anual.

- Req: El plan debe contener:
  - a. Campañas y registro de actividades de difusión.
  - b. Detalles de responsabilidades y compromisos de seguridad.
  - c. Declaración explícita del impacto potencial de una falla de seguridad.
  - d. Mecanismos para reforzar procedimientos y políticas internas.
Req: Plan debe ser revisado anualmente y su efectividad evaluada frecuentemente.
Req: Plan debe activarse ante nuevos funcionarios o cambios de funciones.

### 6.3. Seguridad de los Datos

ID: GUIA-CIBER-FN-PROTECT-DATA-SECURITY-01
Purp: Salvaguardar la confidencialidad, integridad y disponibilidad de los datos.
Ctx: Aplicable a todos los datos del OAE (personales o no).

#### 6.3.1. Encriptación y Criptografía

ID: GUIA-CIBER-FN-PROTECT-DATASEC-CRYPTO-01

- Obj: Usar cifrado para proteger confidencialidad de información sensible.
- Obj: Usar firmas electrónicas para verificar autenticidad e integridad.
- Obj: Usar técnicas criptográficas para resguardar autenticación.
- Ex: Estándares AES (simétrico), RSA (asimétrico), SHA (hash).
- Rec: No usar SHA-1. Usar SHA-2 o SHA-3.
- Ctx: Elección de estándar debe considerar costo de procesamiento y usos.

#### 6.3.2. Eliminación de Datos

ID: GUIA-CIBER-FN-PROTECT-DATASEC-DELETION-01
Req: Adoptar procedimientos formales para eliminación segura.
Obj: Preservar confidencialidad y reducir riesgo de filtración.
Req: Considerar tiempo reglamentario de mantención de datos.

#### 6.3.3. Interoperabilidad de Datos

ID: GUIA-CIBER-FN-PROTECT-DATASEC-INTEROP-01

- a. Req: Resguardar información de interceptación, modificación o copia no autorizada en transferencias. Garantizar no repudio.
- b. Req: Procedimientos de intercambio deben definir responsabilidades, niveles de acceso y protocolos. Cada OAE es responsable de que la info que disponibiliza esté libre de malware.
- c. Req: Interoperar con cifrado punto a punto. No usar protocolos obsoletos.
- d. Req: Autenticar de manera segura a nodos y servicios.
- e. Req: Interoperar información sensible bajo cifrado alto.
- f. Req: Cumplir con Norma Técnica de Interoperabilidad.

### 6.4. Políticas y Procedimientos de Protección

ID: GUIA-CIBER-FN-PROTECT-PROCESSES-01
Purp: Implementar políticas y procesos orientados a la protección.

#### 6.4.1. Desarrollo Seguro

ID: GUIA-CIBER-FN-PROTECT-PROCESS-SECDEV-01
Req: Involucrar seguridad en todo el ciclo de vida de desarrollo.

- Act: Capacitar a personal de desarrollo.
- Act: Mantener ambientes separados (desarrollo, testing, producción) y controlar acceso a producción.
- Act: Implementar seguridad en repositorios de código.
- Act: Usar pautas de codificación segura (ej. OWASP).
- Act: Definir requisitos de seguridad al inicio del ciclo.
- Act: Realizar hitos de seguridad (ethical hacking, análisis de vulnerabilidades, revisión de código).
- Act: Propender a contar con herramientas de análisis de código automatizadas (SAST).

#### 6.4.2. Control de Cambios

ID: GUIA-CIBER-FN-PROTECT-PROCESS-CHANGE-CTRL-01
Req: Registrar todos los cambios sobre las plataformas. Planificar y comunicar implantación.

- Req: Proceso debe incluir revisión de pertinencia, autorización, pruebas, registro de actividades, evaluación de riesgo de seguridad, planes de rollback, proceso de hotfix y uso de gestores de versionamiento.

#### 6.4.3. Gestión de Respaldos

ID: GUIA-CIBER-FN-PROTECT-PROCESS-BACKUPS-01
Req: Realizar respaldos según plan de continuidad.

- Act: Frecuencia de ejecución definida y documentada.
- Act: Pruebas de integridad de cada respaldo.
- Act: Procedimiento documentado de restauración.
- Act: Almacenar respaldos en locación geográfica distinta.
- Act: Aplicar mismas medidas de protección física/lógica que al servidor.
- Act: Cifrar respaldos. Ref: GUIA-CIBER-POLICY-CRYPTOGRAPHY-01.

#### 6.4.4. Gestión de Vulnerabilidades Técnicas

ID: GUIA-CIBER-FN-PROTECT-PROCESS-VULN-MGMT-01
Req: Resolver vulnerabilidades de manera oportuna.
Req: Proceso de resolución debe categorizar vulnerabilidades por riesgo.

- Req: Proceso debe definir líneas de acción (roles, tiempos), gestionar aplicación de medidas correctivas y aplicarlas según urgencia.

#### 6.4.5. Plan de Continuidad

ID: GUIA-CIBER-FN-PROTECT-PROCESS-CONTINUITY-01
Req: Identificar amenazas y riesgos para la continuidad.

- Act: Definir estructura de trabajo interna (Equipo de Respuesta a Incidentes).
- Act: Si es incidente, seguir punto de Gestión de Incidentes. Ref: GUIA-CIBER-FN-RECOVER-INCIDENT-MGMT-01.
- Act: Conocer riesgos tolerables y tiempo máximo de recuperación (RTO).
- Act: Desarrollar/actualizar planes de respuesta y recuperación.
- Act: Desarrollar planes de prueba.

### 6.5. Seguridad en Recursos Humanos

ID: GUIA-CIBER-FN-PROTECT-HR-SECURITY-01
Purp: Establecer cláusulas de seguridad en contratos y nombramientos.
Req: Incluir cláusulas de seguridad en actos administrativos.

- Req: Cláusulas deben incluir compromiso de confidencialidad, responsabilidades legales, responsabilidad sobre clasificación, responsabilidad con info de externos y acciones/sanciones por omisión.
Ctx: Vigencia durante el contrato. Obligaciones de confidencialidad pueden extenderse post-contrato.

### 6.6. Registro y Monitoreo de Eventos

ID: GUIA-CIBER-FN-PROTECT-LOGGING-01
Purp: Registrar actividad relevante para seguridad.
Req: Registrar regularmente actividad de usuarios administradores, excepciones, fallas, eventos de seguridad.

- Req: Información mínima a registrar: ID de usuario, origen (IP), registro horario, intentos de acceso (fallidos, exitosos), acciones/transacciones, información accedida.

## 7. Función: Detectar

ID: GUIA-CIBER-FN-DETECT-01
Def: Acciones para la detección oportuna de eventos de seguridad.

### 7.1. Análisis de Eventos y Anomalías

ID: GUIA-CIBER-FN-DETECT-ANALYSIS-01
Purp: Analizar eventos para identificar anomalías o precursores de incidentes.

- Req: Análisis debe incluir identificación de causa de origen, posible motivo, correlación con eventos anteriores y determinación de impacto potencial.
- Req: Disponer de herramientas de correlación de logs y alertas tempranas.
Req: Implementar mecanismo para separar eventos sin riesgo de aquellos que requieren análisis profundo.

### 7.2. Monitoreo Continuo de Seguridad

ID: GUIA-CIBER-FN-DETECT-CONTINUOUS-MONITORING-01
Purp: Supervisar continuamente la seguridad de sistemas y redes.

#### 7.2.1. Gestión de Código Malicioso

ID: GUIA-CIBER-FN-DETECT-MONITOR-MALWARE-01

- Act: Instalar y actualizar protección anti-malware.
- Act: Realizar revisiones rutinarias de plataformas y red.
- Act: Incluir recuperación post-malware en plan de continuidad.
- Act: Analizar características de malware detectado.
- Act: Detectar ejecución de comandos no autorizados.

#### 7.2.2. Monitoreo de Red

ID: GUIA-CIBER-FN-DETECT-MONITOR-NETWORK-01

- Req: Acceso solo a personal/plataformas autorizadas.
- Req: Usar cortafuegos con configuración no por defecto.
- Req: Registrar y monitorear tráfico de red.
- Req: Monitorear uso de puertos, protocolos y servicios.
- Req: Mantener puertos cerrados por defecto; abrir solo si es estrictamente necesario y controlado.
- Req: Definir criterios para segregación de redes.

### 7.3. Proceso de Detección

ID: GUIA-CIBER-FN-DETECT-PROCESS-01
Purp: Establecer un proceso formal de detección.

- Req: Establecer roles y responsabilidades.
- Req: Cumplir requisitos de seguridad de la Política.
- Req: Comunicar eventos detectados a interesados.
- Req: Medir efectividad del proceso para mejora continua.

## 8. Función: Responder

ID: GUIA-CIBER-FN-RESPOND-01
Def: Acciones para tomar medidas ante un incidente de seguridad detectado.

### 8.1. Planes de Respuesta

ID: GUIA-CIBER-FN-RESPOND-PLANNING-01
Purp: Contar con planes de respuesta inmediata ante incidentes.
Cond: Se activa una vez confirmado un incidente.
Req: El plan debe contener los siguientes elementos.

- Act: Notificación. Ctx: Notificar a ANCi y regulador si corresponde.
- Act: Identificación y Evaluación. Ctx: Identificar activos, controles, roles, responsabilidades; evaluar impacto, compromiso de red, compromiso de datos, daño a servidores.
- Act: Mitigación. Ctx: Contener y aislar el incidente.
- Act: Restablecimiento.
  - Act: Erradicar el riesgo de seguridad.
  - Act: Actualizar sistemas, parches, blindar infraestructura.
  - Act: Cerrar accesos, modificar contraseñas.
  - Act: Erradicar archivos infectados, reconfigurar/reemplazar HW si es necesario.
  - Act: Restaurar nivel de servicio.
  - Act: Comprobar si hubo exfiltración de datos.
- Act: Comunicación. Ctx: Definir canales y preparar/publicar declaraciones internas/públicas.
- Act: Evidencia. Ctx: Asegurar obtención de evidencias para análisis forense.
- Act: Seguimiento. Ctx: Registrar y dar seguimiento al incidente.
- Act: Documentación. Ctx: Realizar informe de respuesta a incidentes.
- Act: Mejora Continua. Ctx: Basada en lecciones aprendidas.
- Act: Contingencia de Personal. Ctx: Activar protocolos de reemplazo si es necesario.

### 8.2. Análisis Forense

ID: GUIA-CIBER-FN-RESPOND-FORENSICS-01
Purp: Investigar un incidente post-mortem.
Cond: Se realiza después de un incidente y aplicación de planes de respuesta.

- Obj: Recopilar información y evidencia, manteniendo cadena de custodia.
- Obj: Resolver la debilidad o vulnerabilidad causal.
- Obj: Actualizar procedimientos de respuesta con lecciones aprendidas.

## 9. Función: Recuperar

ID: GUIA-CIBER-FN-RECOVER-01
Def: Acciones para mantener planes y restablecer capacidades afectadas por un incidente.

### 9.1. Gestión de Incidentes

ID: GUIA-CIBER-FN-RECOVER-INCIDENT-MGMT-01
Purp: Implementar un proceso para gestionar incidentes de forma eficiente y coordinada.
Req: El proceso debe incluir las siguientes etapas mínimas.

- Act: Usar escala de la Guía de Notificación de Incidentes de ANCi.
- Act: Determinar activos involucrados e impacto.
- Act: Describir inicio de ejecución de planes de respuesta/continuidad.
- Act: Notificar al CSIRT de Gobierno.

## 10. Gobernanza de la Guía

ID: GUIA-CIBER-GOVERNANCE-01
Purp: Definir el ciclo de vida y control de versiones de este documento guía.

### 10.1. Actualización de la Guía

ID: GUIA-CIBER-GOVERNANCE-UPDATE-01
Req: Revisar la guía al menos cada año para determinar necesidad de actualización.
Ctx: Actualización basada en aprendizajes, dificultades de aplicación y buenas prácticas.
Req: Dejar registro de todas las versiones y adecuaciones.

### 10.2. Control de Versiones

ID: GUIA-CIBER-GOVERNANCE-VERSIONS-01
Purp: Mantener un registro de las versiones del documento.

| Version | Fecha | Desc |
|---|---|---|
| 1.0 | 2025-03-24 | Versión inicial. |
