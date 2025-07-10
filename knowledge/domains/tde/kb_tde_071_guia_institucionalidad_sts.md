# Guía Implementación Institucionalidad TIC

ID: GUIDE-GOV-ICT-IMPLEMENTATION-01
Version: 1.0.0
Status: Draft
Human-Creator: STSador
Human-Editor: STSador
Model-Collaborator: IA-GEMINI
Creation-Date: 2025-07-06
Modification-Date: 2025-07-06
Primary-Source: kb_071_tde_guia_institucionalidad.md
Ref-STS-Guide: GUIDE-STS-MASTER-01

## 1. Desafíos TIC en Instituciones Nuevas

ID: GUIDE-GOV-ICT-CHALLENGES-01
Purp: Describir los desafíos tecnológicos fundamentales para nuevas instituciones públicas.
Src: `a_11_g9.md`

- Cpt: Desafíos
  - Cpt: Aportar valor a objetivos estratégicos institucionales con tecnología.
  - Cpt: Facilitar entrega de servicios a personas usuarias.
  - Cpt: Asegurar cumplimiento de normativa y estándares técnicos.
- Cpt: Requerimientos Estratégicos
  - Purp: Asegurar coherencia en decisiones tecnológicas y gestión eficiente.
  - Req:
    - Def: Definir estrategia TIC alineada con objetivos estratégicos institucionales.
    - Def: Implementar infraestructura tecnológica adecuada.
    - Ctx: Opciones: on-premise, nube.
    - Def: Gestionar datos con políticas y gobernanza claras.
    - Def: Contar con personal calificado.
    - Def: Asegurar interoperabilidad con otras entidades del Estado.

## 2. Marco Institucional para el Gobierno Digital

ID: GUIDE-GOV-ICT-FRAMEWORK-01

### 2.1. Institucionalidad

ID: GUIDE-GOV-ICT-FRAMEWORK-INSTITUTION-01

#### 2.1.1. Secretaría de Gobierno Digital (SGD)

ID: GUIDE-GOV-ICT-FRAMEWORK-SGD-01
Cpt: Órgano Rector.
Nat: Continuadora legal de la ex División de Gobierno Digital (SEGPRES).
Dep: Subsecretaría de Hacienda.
Fnd: Ley N° 21.658.
Ctx: Fecha de inicio de funciones: 2024-03-01.

- Cpt: Funciones Principales de la SGD
  - ID: GUIDE-GOV-ICT-FRAMEWORK-SGD-FUNCTIONS-01
  - Purp: Proponer Estrategia de Gobierno Digital al Ministro/a de Hacienda.
  - Purp: Coordinar implementación de Estrategia de Gobierno Digital.
  - Ctx: Enfoque integrado.
  - Purp: Coordinar, asesorar y apoyar intersectorialmente en uso estratégico de tecnologías digitales, datos e información pública.
  - Obj: Mejorar gestión de órganos de la Administración del Estado y entrega de servicios.
  - Purp: Desarrollar y operar plataformas y servicios compartidos.
  - Req: Plataformas mínimas deben cubrir Interoperabilidad e Identidad digital.

- Cpt: Alcance del Reglamento
  - ID: GUIDE-GOV-ICT-FRAMEWORK-SGD-REGULATION-01
  - Purp: Regular materias para el adecuado ejercicio de las competencias de la SGD.
  - Ctx: El reglamento regulará:
    - Mecanismos e instrumentos para implementar la Estrategia de Gobierno Digital.
    - Mecanismos e instrumentos para coordinar y apoyar a órganos del Estado.
    - Medios para monitoreo, seguimiento y evaluación de medidas.
    - Forma de solicitar información necesaria para sus fines.

### 2.2. Ley de Transformación Digital del Estado (LTDE)

ID: GUIDE-GOV-ICT-FRAMEWORK-LTDE-01
Fnd: Ley N° 21.180 (LTDE).
Resp: Rol de la SGD es coordinar la implementación de la LTDE.
Req: Órganos del Estado (excepto empresas públicas) deben interoperar y gestionar trámites electrónicos.
Dln: Plazo máximo para la implementación es diciembre de 2027.
Mech: Implementación gradual en 7 fases.
    - Fnd: DFL N° 1 de 2020.
    - Ctx: Criterio de fases se aplica según madurez digital de cada grupo institucional.
Cpt: Reglamento de la LTDE
    - Fnd: Decreto Supremo Nº 4 de 2020, SEGPRES.
    - Purp: Regular tramitación electrónica de procedimientos administrativos.
    - Ctx: Incluye excepciones, notificaciones, estándares.
Cpt: Normas Técnicas
    - Ctx: Existen 6 normas técnicas.
    - Purp: Regular interoperabilidad, seguridad, documentos electrónicos, notificaciones, calidad y autenticación.

## 3. Estrategia TIC

ID: GUIDE-GOV-ICT-STRATEGY-01
Purp: Alinear tecnología con objetivos institucionales, planificar, evaluar servicios, aplicar buenas prácticas, incorporar indicadores para medir avances y mejorar gestión.

### 3.1. Objetivos Estratégicos de TIC

ID: GUIDE-GOV-ICT-STRATEGY-OBJECTIVES-01
Req:
    - Definir objetivos TIC de largo plazo.
    - Definir relación de objetivos TIC con objetivos institucionales estratégicos.
    - Definir cómo los proyectos contribuyen a los objetivos.

### 3.2. Modelo de Arquitectura Institucional

ID: GUIDE-GOV-ICT-STRATEGY-ARCHITECTURE-01
Req:
    - Indicar principales elementos de arquitectura de referencia.
    - Indicar si existe base de datos de configuración (CMDB).
    - Describir estructura de hardware, software y redes.
    - Ex: on premise, cloud, IaaS, PaaS, SaaS.

### 3.3. Modelo de Planificación de TIC

ID: GUIDE-GOV-ICT-STRATEGY-PLANNING-01
Req:
    - Describir cómo se identifican, priorizan y gestionan los proyectos TIC.
    - Indicar existencia, composición y funcionamiento del Comité TIC.

### 3.4. Evaluación de los Servicios de TIC

ID: GUIDE-GOV-ICT-STRATEGY-EVALUATION-01
Req:
    - Indicar principales indicadores de desempeño (KPI) de los servicios TIC.
    - Describir si existe proceso de mejora continua.
    - Purp: Capturar oportunidades y resolver problemas.

## 4. Estructura Organizacional TIC

ID: GUIDE-GOV-ICT-STRUCTURE-01
Purp: Asegurar que decisiones técnicas y estratégicas sean tomadas por personas competentes e idóneas.
Cpt: Criterio de Dimensión.
    - Def: Personas y perfiles deben ser proporcionales al tamaño y complejidad de operaciones del OAE.

### 4.1. Roles Clave y Mejores Prácticas

ID: GUIDE-GOV-ICT-STRUCTURE-ROLES-01
Cpt: Lista de roles clave.

- Cpt: Comité TIC
  - Purp: Gestionar temas TIC estratégicos por la alta dirección.
  - Ctx: En instituciones pequeñas, puede ser el Comité de Calidad, Experiencia Usuaria y Transformación Digital.
  - Ref: Guía Metodológica del PMG de Transformación Digital.
- Cpt: Coordinador de Transformación Digital (CTD)
  - Purp: Ser el enlace institucional con la SGD y liderar la transformación digital.
  - Req: Nombramiento formal por la máxima autoridad del servicio.
  - Req: Registrarse junto a subrogante en plataforma Cero Filas.
  - Req: Inscribirse en capacitaciones en `https://gobdigital.cerofilas.gob.cl/`.
- Cpt: Jefatura TIC
  - Purp: Liderar estrategias y proyectos tecnológicos.
  - Req: Perfil profesional en ingeniería o informática.
  - Req: Conocimientos ideales en gestión de proyectos, arquitectura de información, nube.
- Cpt: Equipo Responsable TIC
  - Dep: Su composición depende de la estrategia (desarrollo externo, SaaS, on-premise, cloud).
  - Cpt: Perfiles de Infraestructura
    - Ex: Ingenieros/as en nube, operaciones, redes, telecomunicaciones, seguridad.
  - Cpt: Perfiles de Desarrollo Propio
    - Ex: Desarrolladores, administradores de bases de datos, diseñadores UX/UI, especialistas en QA.
  - Cpt: Perfiles de Analítica/BI
    - Ex: Analistas, científicos e ingenieros de datos.
  - Cpt: Perfiles Geoespaciales
    - Ex: Expertos en SIG.
- Cpt: Oficial de Seguridad de la Información (Ciberseguridad)
  - Purp: Definir políticas, gestionar riesgos, atender incidentes, cumplir regulaciones.
  - Req: Actuar en coordinación con la Agencia Nacional de Ciberseguridad (ANCI).
- Cpt: Encargado de Protección de Datos (DPO)
  - Purp: Garantizar cumplimiento normativo, asesorar, capacitar, supervisar, ser enlace con autoridades.
- Cpt: Otras Contrapartes
  - Cpt: Perfil Legal
    - Def: Abogado/a experto/a en datos personales, tecnología y transformación digital.
  - Cpt: Perfil de Compras
    - Def: Especialista en compras TIC.
    - Purp: Gestionar inversiones coordinando con áreas técnicas y legales.

## 5. Infraestructura Digital Básica

ID: GUIDE-GOV-ICT-INFRASTRUCTURE-01
Purp: Garantizar continuidad operacional, trazabilidad y eficiencia.
Obj: Cubrir objetivos documentales, transaccionales y de gestión mínimos en cada OAE.
Cpt: Requerimientos de Infraestructura.

- Cpt: Nube
  - Act: Contratar infraestructura de nube (almacenamiento, procesamiento).
  - Purp: Asegurar escalabilidad, redundancia y disponibilidad.
- Cpt: SIEM
  - Act: Contratar un SIEM (Sistema de monitoreo y alertas de seguridad).
- Cpt: Ofimática
  - Act: Contratar una solución de aplicaciones de ofimática.
  - Ex: Google Workspace, Microsoft 365.
- Cpt: Gestión Documental
  - Rec: Definir estrategia y seleccionar herramienta de gestión documental.
  - Obj: Garantizar trazabilidad de trámites.
  - Ctx: Opciones: SaaS o soluciones públicas (según urgencia, recursos, complejidad).
  - Ref: "Pauta de evaluación de sistemas de gestión documental y expedientes electrónicos en el Estado".
- Cpt: Gestión de Personas
  - Act: Identificar y contratar un sistema de información para gestión transaccional de personas.
  - Rec: Modalidad ideal es SaaS.
  - Ctx: Alcance: Pago de remuneraciones, registro de asistencias, permisos, viáticos, vacaciones.
- Cpt: Normativa
  - Act: Ocupar servicios normativos de la Biblioteca del Congreso Nacional para organizar y consultar regulación sectorial.
  - Instr: Usar las "Funcionalidades de Ley Chile" para clasificar contenidos.
  - Ref: <https://www.bcn.cl/leychile>
- Cpt: Gestión de Proyectos
  - Rec: Implementar idealmente un gestor colaborativo de proyectos y tareas.
  - Ex: ASANA, JIRA, Redmine.
- Cpt: Desarrollo de Sistemas
  - Act: Seguir lineamientos de diseño de sitio web y servicios digitales.
  - Ref: "Guía de uso Instrumento de evaluación de calidad en sitios webs y servicios digitales del Estado".
- Cpt: Atención Ciudadana
  - Act: Implementar sistemas tipo CRM para cumplir con exigencias del Sistema de Información y Atención Ciudadana (SIAC).

## 6. Integración con Plataformas Transversales SGD

ID: GUIDE-GOV-ICT-PLATFORMS-SGD-01
Purp: Cumplir normas, estandarizar procesos, asegurar validez, facilitar interoperabilidad, ofrecer servicios seguros y accesibles.

- Cpt: Catálogo de Procedimientos Administrativos y Otras Tramitaciones (CPAT)
  - Def: Herramienta oficial de identificación y caracterización de trámites.
  - Req: Completar el CPAT.
  - Ref: "Guía rápida CPAT para cumplir fase de preparación".
- Cpt: Plataformas Transversales
  - Req: Ocupar plataformas transversales de la SGD.
  - Cpt: Lista de Plataformas
    - Cpt: ClaveÚnica. Purp: Habilitar sistemas que requieran verificar identidad digital de personas usuarias.
    - Cpt: FirmaGob. Purp: Permitir que funcionarios firmen documentos con firma electrónica avanzada.
    - Cpt: DocDigital. Purp: Facilitar comunicaciones oficiales con otros órganos, conectando oficinas de partes.
    - Cpt: SIMPLE. Purp: Digitalizar procesos orientados a las personas.
    - Cpt: PISEE. Purp: Permitir interoperabilidad de datos y documentos entre OAE, evitando solicitar información ya en poder del Estado.
    - Cpt: Notificador. Purp: Habilitar notificaciones a un domicilio digital único de las personas usuarias.
- Cpt: Soporte para Plataformas
  - Ctx: Canal de soporte es la Mesa de Servicios de la SGD.
  - Ref: `https://gobdigitalcl.freshdesk.com/support/home`.

## 7. Gestión de Proyectos TIC

ID: GUIDE-GOV-ICT-PROJECT-MANAGEMENT-01
Purp: Priorizar iniciativas alineadas con objetivos institucionales y optimizar uso de recursos.
Cpt: Soporte de SGD

- Cpt: Asesoría en formulación de proyectos para proceso EVALTIC.
  - Ref: `https://wikiguias.digital.gob.cl/guias/guias/guia_evaltic`
- Cpt: Provisión de guía para la gestión de proyectos TIC.
  - Ref: `https://wikiguias.digital.gob.cl/es/guias/Gestion_de_proyectos_TIC`

## 8. Gestión de Temas Avanzados TIC

ID: GUIDE-GOV-ICT-ADVANCED-TOPICS-01
Purp: Anticipar desafíos, asegurar calidad de datos, impulsar innovación.
Cpt: Recomendaciones

- Cpt: Estrategia de Datos
  - Act: Definir una estrategia de datos.
  - Cpt: Componentes
    - Ex: Modelo, infraestructura, tecnología, estructura organizacional, datos críticos, uso de datos maestros, interoperabilidad, calidad, gestión del dato.
  - Req: Seguir marco de referencia SGD para la gestión de datos en los OAE.
  - Ref: "guía introductoria a la anonimización de datos".
- Cpt: Analítica e IA
  - Instr: Para aplicar analítica de datos, big data e inteligencia de negocios, usar el repositorio de algoritmos públicos para análisis de línea base.
- Cpt: Uso de IA
  - Act: Explorar uso de IA para automatizar procesos y gestionar conocimiento.
  - Req: Realizar iniciativas en el marco de la política nacional de inteligencia artificial y su plan de acciones.
  - Ctx: Ejes de la política: Factores Habilitantes, Desarrollo y Adopción, Gobernanza y Ética.
- Cpt: Datos Abiertos
  - Act: Usar el portal de datos abiertos para todos los datos requeribles por transparencia.
  - Res: Reduce solicitudes vía Ley de Transparencia.
  - Res: Fomenta investigación académica con alto valor público.
- Cpt: Continuidad Operacional
  - Act: Desarrollar un plan de continuidad operacional (BCP) y un plan de recuperación de desastres (DRP).
  - Obj: Garantizar la continuidad y recuperación de los servicios TIC.
- Cpt: Dashboards
  - Act: Facilitar paneles o dashboards interactivos con indicadores clave y visualización dinámica de información.

## 9. Ruta de Implementación y Priorización en la Gestión de TIC

ID: GUIDE-GOV-ICT-IMPLEMENTATION-ROADMAP-01
Purp: Priorizar acciones según contexto institucional, definiendo etapas (esencial, estratégico, largo plazo).
Obj: Lograr una adopción tecnológica ordenada, sostenible y alineada a los objetivos.
Fnd: Es fundamental establecer una ruta que permita avanzar desde condiciones básicas hacia la mejora continua, considerando urgencias operativas y objetivos estratégicos.

### 9.1. Consideraciones para la Priorización

ID: GUIDE-GOV-ICT-ROADMAP-PRIORITIZATION-01
Cpt: Recomendaciones

- Cpt: Cumplimiento Legal
  - Rec: Priorizar siempre acciones que aseguren cumplimiento de Ley 21.180 y otras normativas obligatorias.
- Cpt: Seguridad
  - Rec: Proteger plataformas y servicios es clave para continuidad operacional y protección de datos.
- Cpt: Riesgos Operativos
  - Rec: Atender primero brechas que pongan en riesgo la continuidad de los servicios.
- Cpt: Capacidades Internas
  - Rec: Avanzar según disponibilidad y competencias del equipo, solicitando apoyo externo si es necesario.
- Cpt: Flexibilidad
  - Rec: Adaptar la ruta sugerida según el contexto, urgencia y necesidades particulares de la institución.
