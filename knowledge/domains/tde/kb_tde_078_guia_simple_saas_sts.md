# Guía de Uso de Plataforma SIMPLE (SaaS) para OAE

ID: STS-SAAS-GUIDE-MASTER-01
Version: 1.0.0
Status: Published
Human-Creator: FS
Human-Editor: FS
Model-Collaborator: IA-GEMINI
Creation-Date: 2025-07-06
Modification-Date: 2025-07-06
Primary-Source: kb_078_tde_guia_simple_saas.md
Ref-STS-Guide: GUIDE-STS-MASTER-01

## 1. Definiciones Generales

ID: STS-SAAS-GUIDE-DEFINITIONS-01

### 1.1. Antecedentes

ID: STS-SAAS-GUIDE-DEFS-CONTEXT-01
Purp: Contextualizar SIMPLE dentro de la estrategia de Transformación Digital del Estado chileno.

- Mssn: Gobierno Digital debe coordinar y asesorar intersectorialmente a OAE en uso estratégico de tecnologías digitales.
- Obj: Avanzar hacia gestión pública 100% digital.
- Fnd: Ley 21.180. Ref: `GUIDE-STS-PRINCIPLE-TRANSLATION-01`.
- [cite_start]Ctx: Ley 21.180 exige la transición progresiva a procedimientos administrativos en formato electrónico. [cite: 276, 278]
- Role: SIMPLE es una alternativa para OAE para digitalizar procesos de baja complejidad eficientemente.
- Req: Cumplir estándares de calidad definidos.

### 1.2. Concepto SIMPLE

ID: STS-SAAS-GUIDE-DEFS-CONCEPT-01

- Cpt: Acrónimo. Def: Sistema de Implementación de Procesos Ligeramente Estandarizados.
- Cpt: Definición Técnica. Def: Herramienta modeladora de procesos (BPMS - Business Process Management Software).
- Purp: Ayudar a instituciones públicas a digitalizar procedimientos y trámites de forma fácil y eficiente.
- Cpt: Capacidad. Def: Permite definir tareas y aplicar lógica de decisiones de negocio para implementación directa de procesos digitales de baja complejidad.
- Cpt: Solución. Def: Plataforma flexible, amigable y sencilla para digitalización de procedimientos administrativos (internos/externos).

### 1.3. Funcionalidades Principales

ID: STS-SAAS-GUIDE-DEFS-FEATURES-01

- Cpt: Modelamiento gráfico de procesos.
- Cpt: Incorporación de lenguaje para descripción de reglas de negocio.
- Cpt: Diseño de formularios web.
- Cpt: Generación de documentos y certificados.
- Cpt: Gestión de cuentas de usuario, roles y grupos.
- Cpt: Integración con WebServices y salida de datos vía API.
- Cpt: Seguimiento de procesos.
- Cpt: Emisión de reportes.
- Cpt: Envío de notificaciones por correo electrónico.

### 1.4. Integraciones Nativas

ID: STS-SAAS-GUIDE-DEFS-INTEGRATIONS-01

- Cpt: Integración con FirmaGob.
- Purp: Firma electrónica de documentos en modalidad desatendida.
- Ref: Manual de habilitación en `simple.gob.cl/biblioteca/manuales/`.
- Cpt: Integración con ClaveÚnica.
- Purp: Autenticación de ciudadanía para trámites y solicitudes.
- Req: Aceptar condiciones de uso de ClaveÚnica al solicitar la cuenta.
- Cpt: Integración con APIs Externas.
- Purp: Conexión e interoperación de datos.
- Resp: Instituciones deben poner a disposición los servicios API correspondientes.

## 2. Gobernanza y Uso de la Plataforma

ID: STS-SAAS-GUIDE-GOVERNANCE-01

### 2.1. Acceso y Primeros Pasos

ID: STS-SAAS-GUIDE-GOV-ACCESS-01

- Proc: Acceso a la plataforma.
- 1. Act: Ingresar al sitio web de SIMPLE.
- 2. Act: Revisar fases del modelo de acompañamiento.
- 3. Act: Digitalizar y certificar primer procedimiento.
- Res: Entrega de credenciales de ambiente productivo a un encargado institucional.
- Cpt: Responsabilidades del Encargado.
  - Resp: Administrar y gestionar la cuenta (creación de usuarios, reportes, etc.).
  - Resp: Resolver solicitudes de usuarios internos y externos.
- Cpt: Acceso de Gobierno Digital a cuentas institucionales.
  - Cond: Solo para fines de soporte.
  - Req: Requiere autorización previa de la institución.
  - Proc: Seguir protocolos de soporte. Ref: `STS-SAAS-GUIDE-SUPPORT-HELPDESK-01`, `STS-SAAS-GUIDE-SUPPORT-TEAM-01`.

### 2.2. Uso de Ambientes (Desarrollo y Productivo)

ID: STS-SAAS-GUIDE-GOV-ENVIRONMENTS-01

- Ctx: Credenciales de Desarrollo son entregadas tras completar acceso inicial.
- Purp: Ambiente de Desarrollo.
  - Act: Conocer la plataforma.
  - Act: Crear nuevos procesos.
  - Act: Realizar modificaciones y pruebas.
- Resp: Institución debe respaldar procesos creados en ambiente de desarrollo.
- Cpt: Política de Limpieza (Ambiente Desarrollo).
  - Freq: Anual.
  - Dln: Último día hábil de enero.
- Resp: Institución debe administrar y gestionar su cuenta productiva.
- Cpt: Reglas de Uso de Ambientes.
  - [cite_start]Prohib: Usar ambiente productivo como desarrollo o testeo. [cite: 435]
  - [cite_start]Req: Todo desarrollo/modificación debe iniciarse en el ambiente de desarrollo. [cite: 439]
  - [cite_start]Req: Migración a producción requiere aprobación del equipo de Gobierno Digital. [cite: 439]
- Cpt: Sanciones por Incumplimiento.
  - Proc:
  - 1. Act: Informar a los encargados de la institución.
  - 2. Act: Gobierno Digital podrá bloquear credenciales del usuario infractor.
  - Cond: Bloqueo se mantiene hasta resolver la situación.
  - 3. Act: En caso de reincidencia, Gobierno Digital podrá tomar acciones adicionales por motivos de seguridad.

### 2.3. Almacenamiento de Archivos

ID: STS-SAAS-GUIDE-GOV-STORAGE-01

- Cpt: Funcionalidad. Def: `File Transfer` en backend.
- Resp: Institución debe descargar los archivos desde `File Transfer`.
- Cpt: Política de Borrado.
  - Rule: Archivos son eliminados 30 días corridos desde su ingreso.
  - [cite_start]Warn: No existen mecanismos para recuperar archivos después de su eliminación. [cite: 415]

### 2.4. Disponibilidad de la Plataforma

ID: STS-SAAS-GUIDE-GOV-AVAILABILITY-01

- Resp: Gobierno Digital debe realizar tareas para garantizar disponibilidad y accesibilidad de SIMPLE.
- Cpt: Disponibilidad Estándar.
  - Def: Ininterrumpida.
  - Cond: Excepto por mantenciones programadas.
- Cpt: Excepciones a la Disponibilidad.
  - Cause: Mantención de sistemas. [cite_start]Ref: `STS-SAAS-GUIDE-GOV-MAINTENANCE-01`. [cite: 416]
  - [cite_start]Cause: Problemas técnicos, corte operacional, o baja de servicio del proveedor de infraestructura. [cite: 416]
  - [cite_start]Cause: Caso fortuito o fuerza mayor. [cite: 416]
  - [cite_start]Cause: Error, falta u omisión por servicios externos a Gobierno Digital (ej. caída red RCE). [cite: 416]

### 2.5. Mantenciones a la Plataforma

ID: STS-SAAS-GUIDE-GOV-MAINTENANCE-01

- Cpt: Tipo. Def: Mantenciones programadas.
- Res: Deshabilitación de servicios por algunas horas.
- Cpt: Protocolo de Comunicación.
  - Mech: Correo electrónico al Coordinador/a de Transformación Digital.
  - Mech: Aviso en sección "Notificaciones" del backend.
- Resp: Institución debe tomar medidas para asegurar la continuidad de su operación.

## 3. Gobernanza de Funcionalidades Clave

ID: STS-SAAS-GUIDE-KEYFEATURES-GOV-01

### 3.1. Uso General de API SIMPLE

ID: STS-SAAS-GUIDE-KF-API-GENERAL-01

- Nat: API de uso compartido para todos los OAE con cuenta SaaS.
- Req: No generar sobreconsumos en la API.
- Cause: Un sobreconsumo afecta a todas las instituciones usuarias.
- [cite_start]Prohib: No es permitido generar conexiones de consulta a la API SIMPLE usando acciones tipo `rest` desde los procesos digitalizados en la misma plataforma. [cite: 435]
- Cpt: Monitoreo.
  - Mech: Gobierno Digital utiliza herramientas internas para monitorear consumos.
  - Res: En caso de anomalías, se aplica procedimiento de monitoreo. Ref: `STS-SAAS-GUIDE-PROC-MONITORING-01`.

### 3.2. Consumo de API para Procesos Masivos

ID: STS-SAAS-GUIDE-KF-API-BULK-01

- Resp: Institución usuaria.
- [cite_start]Rec: Realizar consumo en horario de baja demanda (00:00 a 05:00 hrs, CL). [cite: 437]
- Cond: Si se detecta consumo mayor al autorizado, se aplica procedimiento. Ref: `STS-SAAS-GUIDE-PROC-MONITORING-01`.

### 3.3. Uso de Funcionalidad de Reportería

ID: STS-SAAS-GUIDE-KF-REPORTS-01

- Cpt: Funcionalidad. Def: Backend permite generar reportes en formato Excel.
- Purp: Obtener información consolidada y específica de transacciones para un periodo acotado.
- [cite_start]Rec: Periodo de consulta no debe ser superior a seis meses. [cite: 437]
- [cite_start]Prohib: No usar esta funcionalidad para obtener toda la información histórica de los trámites. [cite: 435]
- [cite_start]Cause: Ambientes productivos son compartidos; un alto volumen de datos puede impedir la generación del reporte. [cite: 416]
- Cpt: Alternativa para grandes volúmenes de datos.
  - 1. Act: Obtener información a través de API SIMPLE. Ref: `STS-SAAS-GUIDE-KF-API-GENERAL-01`.
  - 2. Act: Almacenar la información en una base de datos propia.
  - 3. Act: Generar reportería según necesidades específicas desde la base de datos propia.
  - Resp: El desarrollo de esta alternativa es responsabilidad de la institución usuaria.

### 3.4. Configuración del Servicio de Correo

ID: STS-SAAS-GUIDE-KF-EMAIL-01

- Cpt: Formato Remitente. Def: `no-reply@digital.gob.cl`.
- Resp: Institución debe generar alertas y directrices con sus equipos de TI.
- Purp: Evitar que las notificaciones de la plataforma sean consideradas SPAM o bloqueadas.
- [cite_start]Warn: Esta configuración es un paso necesario y de absoluta responsabilidad de la institución usuaria. [cite: 415]

### 3.5. Integraciones con Servicios Externos

ID: STS-SAAS-GUIDE-KF-EXTERNAL-INTEGRATIONS-01

- Cond: Aplicable solo para procesos en producción.
- Proc: Solicitud de integración.
  - 1. Act: Llenar formulario "Inscripción de Servicios Externos con SIMPLE".
  - 2. Act: Especificar toda la información requerida.
- Cpt: Información requerida en formulario.
  - Req: Nombre de la Institución.
  - Req: Nombre de la cuenta asignada.
  - Req: Datos de la contraparte técnica (Nombre, Teléfono, Correo).
  - Req: URL / IP del servicio externo.
  - Req: Consumo máximo (TPM).
  - Req: Tipo de servicio.
  - Req: Tipo de seguridad que implementa el servicio.
  - Req: Tiempo promedio de respuesta del servicio externo.
  - Req: ID de los procesos que utilizan el servicio.
  - Req: Nombre de los procesos que utilizan el servicio.
- Req: Se debe actualizar la información si el servicio se incorpora a nuevos procesos.
- Cpt: Consecuencias de Falta de Registro.
  - Cond: Si una integración no registrada presenta problemas operacionales que afectan la plataforma.
  - Acc: Gobierno Digital podrá tomar acciones para garantizar la seguridad hasta que se complete el registro.
- Ctx: Gestión de convenios con proveedores de servicios externos no es responsabilidad de Gobierno Digital.

## 4. Procedimientos y Responsabilidades

ID: STS-SAAS-GUIDE-PROCEDURES-01

### 4.1. Lanzamiento de Nuevos Procedimientos

ID: STS-SAAS-GUIDE-PROC-LAUNCH-01

- Req: Informar a Gobierno Digital con al menos 2 semanas de anticipación a la fecha de lanzamiento.
- Purp: Asegurar la operación óptima de la plataforma.
- [cite_start]Rec: Realizar lanzamientos en días y horarios con soporte de Gobierno Digital operativo. [cite: 437]
- Purp: Contar con apoyo técnico en caso de inconvenientes. Ref: `STS-SAAS-GUIDE-SUPPORT-HELPDESK-01`.
- Proc: Información de lanzamiento.
  - 1. Act: Llenar formulario "Informar publicación de proceso".
  - 2. Act: Especificar toda la información requerida.
- Cpt: Información requerida en formulario.
  - Req: Nombre de la institución.
  - Req: Nombre de la cuenta asignada.
  - Req: URL de producción.
  - Req: Datos de la contraparte técnica-digitalizador (Nombre, Teléfono, Correo).
  - Req: Número máximo de consultas diarias estimadas.
  - Req: URL / IP de servicios externos (si aplica).
  - Req: Nombre del nuevo proceso.
  - Req: ID del nuevo proceso.
- Req: Un proceso no certificado por Gobierno Digital igualmente debe ser informado siguiendo este protocolo.

### 4.2. Modificación de Procesos en Producción

ID: STS-SAAS-GUIDE-PROC-MODIFICATION-01

- Cpt: Modificación Menor.
  - Def: No afecta el funcionamiento del proceso certificado.
  - Req: Actualizar documentación e ingresarla a través del "Formulario actualización de documentación".
- Cpt: Modificación Mayor.
  - Def: Afecta la estructura del proceso certificado.
  - Res: Se considera un nuevo proceso.
  - Req: Debe cumplir con el ciclo completo de desarrollo y aprobación. Ref: `STS-SAAS-GUIDE-GOV-ENVIRONMENTS-01`.

### 4.3. Monitoreo del Uso de SIMPLE

ID: STS-SAAS-GUIDE-PROC-MONITORING-01

- Cpt: Escenario 1.
  - Cond: Consumo mayor al promedio mensual, sin afectar operación o estabilidad.
  - Acc: Gobierno Digital informa a la institución para conocimiento y acciones preventivas.
- Cpt: Escenario 2.
  - Cond: Consumo afecta la operación y/o estabilidad de la plataforma.
  - Proc:
    - 1. Acc: Gobierno Digital informa a la institución para que realice ajustes a la brevedad.
    - 2. Acc: Si no hay ajustes y los problemas persisten, se bloquea la URL de la cuenta institucional.
    - Cond: Desbloqueo se realiza en horario hábil, una vez que la institución informa los ajustes realizados.

## 5. Normas, Soporte y Documentación

ID: STS-SAAS-GUIDE-SUPPORT-01

### 5.1. Soporte Técnico

ID: STS-SAAS-GUIDE-SUPPORT-HELPDESK-01

- Cpt: Canal Oficial. Def: Mesa de Ayuda de Gobierno Digital.
- Purp: Responder consultas técnicas de la plataforma y sobre digitalización de trámites.
- Cpt: Acceso. Def: Formulario online en pie de página de `digital.gob.cl`.
- Cpt: Disponibilidad del Formulario. Def: Ininterrumpida.
- Cpt: Horario de Atención del Soporte.
  - Lunes a Jueves: 08:30 a 17:30 hrs.
  - Viernes: 08:30 a 16:30 hrs.
  - Cond: Excepto días festivos.

### 5.2. Apoyo del Equipo de Digitalización

ID: STS-SAAS-GUIDE-SUPPORT-TEAM-01

- Req: Todo proceso publicado en ambiente productivo debe ser visado previamente por el Equipo de Digitalización.
- Req: Se debe contar obligatoriamente con todos los documentos de evidencia actualizados (descripción, diagramas BPMN, etc.).
- Cpt: Publicación sin Visado.
  - Resp: Absoluta responsabilidad de la institución.
  - Req: La institución debe garantizar el correcto funcionamiento y responder ante problemas.
  - Res: Faculta a Gobierno Digital a no entregar soporte técnico por este incumplimiento.
- Cpt: Responsabilidad de Interoperabilidad.
  - Req: Institución debe informar a Gobierno Digital sobre conexiones. Ref: `STS-SAAS-GUIDE-KF-EXTERNAL-INTEGRATIONS-01`.
  - Req: Institución debe monitorear comportamiento y realizar pruebas de carga.
  - Req: Institución es responsable de generar el manejo de errores y procurar el correcto funcionamiento.
- Resp: La calidad del proceso digitalizado es responsabilidad de la institución.
- Role: Digitalizadores son responsables de comunicar a sus jefaturas que cada proceso publicado debe ser trabajado, revisado y validado internamente.
- Ctx: Consultas sobre procesos en producción deben canalizarse por la Mesa de Ayuda. Ref: `STS-SAAS-GUIDE-SUPPORT-HELPDESK-01`.

### 5.3. Proveedores Externos en Digitalización

ID: STS-SAAS-GUIDE-SUPPORT-PROVIDERS-01

- Ctx: La relación contractual existe solo entre la institución y su proveedor.
- Prohib: No existe relación contractual o de soporte directo entre Gobierno Digital y el proveedor.
- Req: Cualquier solicitud a Gobierno Digital debe ser efectuada por la institución usuaria.
- Resp: Institución debe validar que los procesos digitalizados por el proveedor cumplen los lineamientos.
- Resp: Institución debe asumir el soporte, revisión y actualización de trámites al finalizar la relación con el proveedor.
- Resp: Proveedor debe conocer y capacitarse en la plataforma usando la documentación pública.
- Req: Tickets de soporte deben ser emitidos por la institución usuaria con un correo institucional.
- Prohib: Proveedores no pueden emitir tickets de soporte directamente.

### 5.4. Modificación del Presente Documento

ID: STS-SAAS-GUIDE-DOC-MODIFICATION-01

- Cpt: Política de Actualización.
  - Acc: El documento puede ser actualizado en cualquier momento por Gobierno Digital.
  - Ctx: La última versión estará siempre disponible en el sitio web de SIMPLE y en la comunidad Clúster.

### 5.5. Aceptación del Presente Documento

ID: STS-SAAS-GUIDE-DOC-ACCEPTANCE-01

- Cond: Se considera que todo OAE que solicita una cuenta productiva en SIMPLE ha leído y acepta lo establecido en este documento.
