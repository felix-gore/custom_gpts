# Guía Técnica: Adquisición de Servicios de Nube Pública en OAE

ID: GORE-GUIA-CLOUD-01
Purp: Servir de guía técnico-operativa para la adquisición de servicios de Cloud Pública por parte de los Órganos de la Administración del Estado (OAE).
Src: `a_09_g7.md` (Recomendaciones técnicas para la adquisición de servicios de nube pública en los OAE)
Cpt: Autor. Def: Secretaría de Gobierno Digital (SGD)
Version: 2.0
Ref-STS-Guide: GUIDE-STS-MASTER-01

## 1. Fundamentos y Contexto

ID: GORE-GUIA-CLOUD-FUNDAMENTOS-01

### 1.1. Propósito y Alcance

ID: GORE-GUIA-CLOUD-PROPOSITO-01
Purp: Entregar recomendaciones técnicas para la adquisición de servicios de Cloud Pública.
Dest: Profesionales TI de los OAE involucrados en etapa de precompra.
Def: Precompra. Ctx: Proceso de preparación de la contratación administrativa.
Cpt: Incluye.

- Consideraciones generales para elección de proveedor.
- Elementos para definir Acuerdos de Nivel de Servicio (SLA).
Cpt: Alcance.
- Nat: Consultivo.
- Obj: Orientar toma de decisiones en requerimiento técnico para adquisición de Nube Pública.
- Contribucion: Apoyar formulación de proyectos en marco del proceso EvalTI.
Cpt: Excluye.
- Problemáticas de preservación digital.
- Problemáticas de seguridad de la información.
- Determinación de mecanismos de compra.

### 1.2. Agradecimientos y Consideraciones

ID: GORE-GUIA-CLOUD-AGRADECIMIENTOS-01
Cpt: Agradecimientos.

- Consejo de Política de Suministro TI.
- ChileTec.
- ACTI A.G.
Cpt: Consideraciones.
- Cpt: Estado-Doc. Def: En permanente revisión.
- Cpt: Actualizacion. Def: Periódica, según uso, reformas normativas, disponibilidad de nuevas tecnologías.
- Cpt: Mecanismos-Consulta. Def: Incluyen OAE, expertos, sociedad civil, industria.

### 1.3. Conceptos Clave

ID: GORE-GUIA-CLOUD-CONCEPTOS-01

- Cpt: Conc. Def: Cloud Computing
  - ID: GORE-GUIA-CLOUD-CONCEPTO-COMPUTING-01
  - Def: Modelo de acceso bajo demanda y por red a conjunto de recursos compartidos y configurables (redes, servidores, almacenamiento, apps, servicios).
  - Cpt: Ventaja. Def: Asignación y liberación con mínima gestión del proveedor.
  - Src: Nigro (2022), NIST (2011).
- Cpt: Conc. Def: Nube Primero (Cloud First)
  - ID: GORE-GUIA-CLOUD-CONCEPTO-FIRST-01
  - Def: Principio que apunta a que órganos públicos evalúen uso preferente de servicios en la nube para arquitecturas tecnológicas.
  - Cpt: Prioridad. Def: Mayor prioridad que infraestructuras propias (On-Premise, housing).
  - Cpt: Principios-Observados. Def: Eficiencia, legalidad, neutralidad tecnológica, seguridad.
  - Src: Legal. Ctx: Instructivo Presidencial No. 1 (2018).
- Cpt: Conc. Def: Nube Inteligente (Cloud Smart)
  - ID: GORE-GUIA-CLOUD-CONCEPTO-SMART-01
  - Def: Principio que apunta a que órganos públicos deben considerar objetivos estratégicos, modelos de operación, consideraciones financieras y protección de datos al adoptar y operar soluciones en la nube.
  - Cpt: Armonizacion. Def: Puede armonizarse con Cloud First para estrategia gradual, integral y efectiva.
- Cpt: Conc. Def: Territorialidad de los Datos
  - ID: GORE-GUIA-CLOUD-CONCEPTO-TERRITORIALIDAD-01
  - Ctx: Uso de Cloud Pública implica conexión vía internet, sin reconocer territorialidad.
  - Cpt: Regla-General-CHL. Def: Normativa chilena no exige que datos deban estar ubicados dentro de fronteras nacionales.
  - Cpt: Habilitacion. Def: Permite uso de Cloud Pública por OAE.
  - Cpt: Excepcion. Def: Salvo existencia de normativa sectorial o interna que disponga lo contrario.

### 1.4. Criterios Generales para Uso de Cloud Pública

ID: GORE-GUIA-CLOUD-CRITERIOS-GENERALES-01

- Cpt: Implicancia-Decision. Def: Mover cargas a Cloud Pública es más que contratar infraestructura externa.
- Req: Estrategia-Minima.
  - Evaluación de necesidades reales.
  - Definición de expectativas.
  - Disponibilidad de capacidades profesionales (internas/externas).
  - Planificación detallada.
  - Diseño de un nuevo modelo de operación.
- Cpt: Caracteristicas-Esenciales-Cloud.
  - Autoservicio bajo demanda.
  - Amplio acceso a la red.
  - Agrupación de recursos.
  - Elasticidad rápida.
  - Servicio medido.
- Cpt: Oportunidades-Cloud.
  - Actualización tecnológica permanente.
  - Disminución de personal dedicado a operación.
  - Respaldos.
  - Gestión permanente de seguridad.
  - Flexibilidad.
  - Escalabilidad.
  - Continuidad operacional.
  - Menores montos de inversión.
- Req: Personal. Ctx: Conocimientos más específicos en diversos temas.
- Req: Planificacion. Ctx: Diseño con mayor detalle del plan de migración y cobertura de roles.
- Cpt: Perspectiva-Financiera.
  - Cpt: Modelo-Base. Def: OPEX (gastos de operación) vs. CAPEX (inversión).
  - Cpt: Beneficio. Def: Facilita asignación de recursos para servicios Cloud.
- Cpt: Propiedad-Datos.
  - Req: Contratacion. Ctx: Verificar que términos de servicio (especialmente en SaaS) sean explícitos.
  - Cpt: Declaracion-Explicita. Def: Datos son propiedad del OAE contratante.
  - Prohib: Transferencia. Ctx: No se transfiere propiedad ni derecho a uso de datos al proveedor.
  - Cpt: Acceso-Datos. Def: OAE puede solicitar datos y metadata en cualquier momento.
  - Cpt: Formato-Transferencia. Def: Estándar.
  - Req: Adicional. Ctx: Detalle explicativo de la data recibida si es requerido.
  - Cpt: Foco-Critico. Def: Observar estrictamente al término del contrato de servicios.

## 2. Proceso de Decisión para Adopción Cloud

ID: GORE-GUIA-CLOUD-PROCESO-DECISION-01
Purp: Ayudar a proceso interno de decisión y diseño de compra.
Obj: Dar respuestas precisas para migración o uso de Cloud Pública.
Fnd: Experiencia y buenas prácticas.
Mech: Cuestionario de respuesta Sí/No para verificar madurez institucional.
Rec: Principal. Ctx: Cumplir condiciones para asegurar un "Sí" a las preguntas.
Cpt: Natur-Preguntas. Def: De carácter higiénico; contemplan aspectos que deben estar resueltos (interna/externamente).
Cpt: Paso-Siguiente. Def: Si resultado es exitoso, pasar a Capítulo 2 del documento original (Sección 3 de este KB).

### 2.1. Árbol de Decisiones

ID: GORE-GUIA-CLOUD-ARBOL-DECISIONES-01

- Cpt: Pregunta. Def: Equipo de trabajo.
  - ID: GORE-GUIA-CLOUD-PREGUNTA-1-01
  - Cpt: Pregunta. Def: ¿Cuenta con equipo de al menos dos profesionales (internos/externos) con experiencia en control y gestión de Cloud (Admin Sistemas, Devops, SREs)?
  - Cond: Si-Sí. Ctx: Ir a Pregunta 2.
  - Cond: Si-No.
    - Rec: Diseñar mecanismo para contar con al menos 2 profesionales idóneos.
    - Act: Ir a Pregunta 2.
- Cpt: Pregunta. Def: Sistemas legacy críticos.
  - ID: GORE-GUIA-CLOUD-PREGUNTA-2-01
  - Cpt: Pregunta. Def: ¿Tiene sistemas productivos legacy que son críticos y no puede migrar aún a tecnologías modernas?
  - Cond: Si-Sí.
    - Cond: Requiere migración urgente por obsolescencia de infraestructura, seguridad u operación.
    - Act: Evaluar. Ctx: Migración "lift and shift" a la Nube como medida temporal y parcial hasta lograr actualización.
    - Act: Ir a Pregunta 3.
  - Cond: Si-No. Ctx: Ir a Pregunta 3.
- Cpt: Pregunta. Def: Necesidad de escalabilidad.
  - ID: GORE-GUIA-CLOUD-PREGUNTA-3-01
  - Cpt: Pregunta. Def: ¿Los sistemas que administra deben escalar de manera repentina y a veces no predecible?
  - Def: Escalar. Ctx: Capacidad de cómputo/almacenamiento sujeta a crecimientos temporales y bruscos o a crecimiento sostenido y predecible.
  - Cond: Si-Sí. Ctx: Ir a Pregunta 4.
  - Cond: Si-No.
    - Rec: Evaluar Cloud Pública contemplando sólo capacidades actuales, considerando a lo más crecimiento vegetativo.
    - Rec: Alt. Ctx: Evaluar opciones de housing/hosting que permitan crecimiento moderado y predecible.
    - Act: Ir a Pregunta 4.
- Cpt: Pregunta. Def: Documentación de sistemas.
  - ID: GORE-GUIA-CLOUD-PREGUNTA-4-01
  - Cpt: Pregunta. Def: ¿Tiene documentadas sus aplicaciones, infraestructura y sistemas?
  - Req: Instrumentos.
    - Diagrama de infraestructura.
    - CMDB (base de datos de configuración).
    - Diagramas de despliegue o equivalentes.
    - Demanda de transacciones por unidad de tiempo (segundo, minuto).
    - RTO y RPO para sistemas críticos.
    - Mapa de procesos y su vinculación con sistemas.
  - Cond: Si-Sí (6 de 6). Ctx: Ir a Pregunta 5.
  - Cond: Si-No (a alguno).
    - Rec: Establecer Proyecto de Migración que incluya estrategia y plan para definir y documentar estos instrumentos.
    - Act: Ir a Pregunta 5 una vez documentado.
- Cpt: Pregunta. Def: Plan de migración.
  - ID: GORE-GUIA-CLOUD-PREGUNTA-5-01
  - Cpt: Pregunta. Def: ¿Tiene conocido y planificado (ej. Gantt) las actividades y tiempo para migrar al Cloud, con recursos propios o externalizados?
  - Cond: Si-Sí. Ctx: Ir a Pregunta 6.
  - Cond: Si-No.
    - Rec: Establecer planificación y documentar plan de migración (recursos, tiempos, gestión del cambio).
    - Cpt: Apoyo. Def: Proveedores especializados pueden apoyar.
    - Req: Previo. Ctx: Tener resueltos los puntos de la Pregunta 4.
    - Act: Ir a Pregunta 6 una vez planificado.
- Cpt: Pregunta. Def: Área de ciberseguridad y CISO.
  - ID: GORE-GUIA-CLOUD-PREGUNTA-6-01
  - Cpt: Pregunta. Def: ¿Posee un área de ciberseguridad y un CISO, con recursos propios o externalizados?
  - Cond: Si-Sí. Ctx: Pasar a la siguiente sección.
  - Cond: Si-No.
    - Rec: Identificar cómo resolverá estas funciones durante adopción y operación en Cloud.
    - Cpt: Rol-CISO. Def: Debe ser un rol interno.
    - Cpt: Apoyo-Externo. Def: Labores técnicas y operativas pueden ser resueltas externamente.
    - Act: Pasar a la siguiente sección una vez cubiertas las funciones.

## 3. Guía de Adquisición de Servicios ("Qué comprar")

ID: GORE-GUIA-CLOUD-QUE-COMPRAR-01

- Cpt: Escenario. Def: Capacidades técnicas limitadas y necesidad de software específico (ERP, CRM, etc.).
  - Rec: Preferir soluciones Cloud en modalidad SaaS (Software as a Service).
  - Prohib: Rec. Ctx: No comprar Cloud Pública para instalar aplicaciones desde cero.
  - Just: Prohib. Ctx: Requiere capacidades de adm. y op. similares a On-Premise, no se aprovechan todos los beneficios de Cloud.
  - Ex: SaaS. Ctx: Plataformas de ofimática como Google Workspace, Office 365, Zimbra.
- Cpt: Escenario. Def: Gestionar aplicaciones propias/terceros que requieren escalar y se dispone de recursos profesionales.
  - Def: Capacidad para gestionar, modificar, desarrollar, migrar, asignar espacio, bases de datos, balanceo de carga, etc.
  - Cond: Compra. Ctx: Puede comprar infraestructura (IaaS) y plataformas (PaaS) en Cloud Pública.
- Cpt: Modelo-Cobro-Cloud.
  - Fnd: Mensual variable (pago por uso).
  - Cpt: Gestion. Def: Autónoma vía paneles de control provistos por el proveedor (se debe exigir).
  - Req: Dinamico. Ctx: Adquirir servicios dinámicamente.
- Cpt: Modelo-Compra-Creditos.
  - Mech: Proveedor ofrece "créditos" equivalentes a suma de dinero para adquirir servicios Cloud.
  - Cpt: Incluye-Opcional. Def: Servicios de soporte del proveedor.
- Cpt: Detalle-Compra.
  - Req: Explicitar los distintos servicios en que se usarán los créditos.
  - Cpt: Lista-Servicios-No-Excluyente (IaaS, PaaS, BaaS, CaaS, SaaS):
    - Máquina virtual.
    - Repositorios de almacenamiento.
    - Sistema de archivos distribuidos.
    - Servicio de Kubernetes elástico.
    - Servicio de balanceo de tráfico.
    - Servicio de bases datos relacional.
    - Servicio de DNS.
    - Servicio de red de distribución de contenidos estáticos (CDN).
    - Servicio de correos.
    - Monitoreo de infraestructura.
    - Servicio de WAF.
    - Servicio de bases datos no relacional (ej. Mongo Atlas).
    - Servicio de encolamiento.
    - Servicios de ETL.
    - Servicio de data streams.
    - Servicio de Datawarehouse.
    - Servicio de detección de amenazas.
    - Servicio automático de evaluación de seguridad (ej. Inspector).
    - Bases de datos como servicio.
    - Inteligencia artificial como servicio.
    - Plataforma de desarrollo de aplicaciones móviles como servicio (MBaaS).
    - Servicio de gestión de API.
    - Servicio de identidad y acceso como servicio.
- Cpt: Nomenclatura-Proveedor. Def: Cada proveedor usa nombres y categorías diferentes.

## 4. Selección de Proveedores

ID: GORE-GUIA-CLOUD-SELECCION-PROVEEDOR-01

### 4.1. Tipos de Proveedores Cloud

ID: GORE-GUIA-CLOUD-TIPOS-PROVEEDOR-01

- Cpt: Criterio-Caracterizacion. Def: Tamaño, alcance, cobertura de la empresa y servicios.
- Cpt: Tipo. Def: Hyperscalers.
  - Cpt: Escala. Def: Global.
  - Cpt: Asociacion. Def: Corporaciones globales de tecnología.
- Cpt: Tipo. Def: Proveedores Regionales.
  - Cpt: Escala. Def: Continental.
  - Cpt: Asociacion. Def: Empresas de servicios tecnológicos y telecomunicaciones.
- Cpt: Tipo. Def: Proveedores Locales.
  - Cpt: Escala. Def: Nacional.
  - Cpt: Oferta. Def: Modelo de servicios más específicos o de alcance local.
- Cpt: Respuesta-A-Priori. Def: No existe. La selección depende de factores específicos de la institución.
- Cpt: Factores-Seleccion.
  - Especificidad de servicios solicitados.
  - Nivel de disponibilidad (SLA) requerido. Ref: GORE-GUIA-CLOUD-GESTION-SLA-01
  - Capacidad y conocimiento de la institución para administrar.
  - Recursos financieros disponibles.

### 4.2. Consideraciones para la Elección del Proveedor

ID: GORE-GUIA-CLOUD-CONSIDERACIONES-ELECCION-01
Cpt: Lista-No-Exhaustiva. Def: 5 características clave a considerar en requerimientos técnicos.

- Cpt: Caracteristica. Def: Fiabilidad y Disponibilidad.
  - Cpt: Uptime. Def: Nivel de disponibilidad adecuado a los requerimientos de la institución (especificado en SLA). Incluye respaldo de infraestructura física y capacidades de adm./op. Ref: GORE-GUIA-CLOUD-GESTION-SLA-01
  - Cpt: Centros de Datos Redundantes. Def: Para garantizar continuidad ante fallas. Se aprovecha implementando procedimientos de continuidad operacional.
- Cpt: Caracteristica. Def: Seguridad.
  - Cpt: Cumplimiento Normativo. Def: Para asegurar cumplimiento con estándares y regulaciones de seguridad.
  - Cpt: Gestión de Identidad y Acceso. Def: Mecanismos y servicios robustos para proteger recursos Cloud. Incluye procedimientos de coordinación con la institución.
  - Cpt: Determinación de Responsabilidades. Def: Modelo claro de responsabilidades entre proveedor y la institución.
  - Ref: GORE-GUIA-CLOUD-PREGUNTA-6-01
- Cpt: Caracteristica. Def: Escalabilidad y Flexibilidad.
  - Cpt: Escalabilidad Automática. Def: Para manejar cargas de trabajo variables.
  - Cpt: Variedad de Servicios. Def: Amplia gama de servicios para satisfacer diversas necesidades (almacenamiento, IA, etc.).
- Cpt: Caracteristica. Def: Rendimiento.
  - Cpt: Redes de Entrega de Contenidos (CDN). Def: Verificar si proveedor ofrece CDN si se requiere para acelerar carga de datos/apps.
  - Cpt: Localización de Centros de Datos. Def: Proximidad geográfica puede influir en latencia.
- Cpt: Caracteristica. Def: Soporte y Servicio al Cliente.
  - Cpt: Niveles de Soporte. Def: Evaluar distintos niveles de soporte ante incidentes.
  - Cpt: Recursos de Ayuda y Documentación. Def: Disponibilidad de documentación detallada y comunidad activa facilita gestión.
- Adv: Final. Ctx: Antes de decidir, evaluar cómo estas características se alinean con objetivos institucionales, y considerar costos y términos contractuales.

### 4.3. El Rol de los Partners o Socios de Negocios

ID: GORE-GUIA-CLOUD-ROL-PARTNERS-01

- Cpt: Modelo-Provision. Def: No siempre hay relación directa entre institución y proveedor base.
- Cpt: Modo-Indirecto. Def: A través de reseller, partner, socio comercial o distribuidor.
- Cpt: Rol-Partner. Def: Realiza oferta, firma contrato, mantiene relación técnico-comercial.
- Cpt: Aplicabilidad. Def: Casi todos los Hyperscalers o empresas regionales en Chile.
- Cpt: Cond-Partner. Def: Cada marca de nube tiene condiciones/restricciones (capacidades, certificaciones, volumen de negocios) para seleccionar sus partners, complementarias a las de Mercado Público.
- Cpt: Impacto-Potencial. Def: En definición del requerimiento, selección instrumento de compra, proceso de habilitación.
- Req: Legal. Ctx: (Ley 19.886, Art. 35 bis) En contrataciones complejas, usar mecanismos de análisis técnico, financiero, de ciclo de vida, y consulta al mercado.
- Cpt: Causa-Diferencia-Costos. Def: Modelo comercial (marca) y de provisión (reseller) explica diferencias entre consumo en consola y monto final a pagar.
- Cpt: Factores-Costo-Adicional. Def: Márgenes de comercialización, impuestos, conversión de monedas.
- Cpt: Impacto-Procesos. Def: Presupuesto, facturación, pago.
- Cpt: Soporte-Tecnico. Def: Primer nivel generalmente provisto por el partner; escalado si es necesario al proveedor global.
- Req: Construccion-Compra.
  - Expectativas técnicas y comerciales del modelo de operación.
  - Modelo comercial (tasas adicionales, precios, cobros, impuestos).
  - Modelo de servicios (definir roles y responsabilidades de institución, partner y proveedor base).
  - Modelo de control de la consola de servicios y distribución de responsabilidades.

## 5. Gestión de Niveles de Servicio (SLA)

ID: GORE-GUIA-CLOUD-GESTION-SLA-01

### 5.1. Concepto de SLA

ID: GORE-GUIA-CLOUD-SLA-CONCEPTO-01
Def: Acuerdo de Nivel de Servicio (SLA) es parte de la relación contractual proveedor-cliente.
Obj: Establecer términos y condiciones de calidad, disponibilidad y rendimiento de servicios.
Cpt: Define-Metricas. Def: Tiempo de actividad, tiempos de respuesta, capacidad de almacenamiento.
Cpt: Proposito.

- Establecer expectativas claras.
- Garantizar transparencia.
- Permitir a usuarios medir eficiencia y confiabilidad.
- Proporcionar base objetiva para resolución de problemas y compensaciones.
- Establecer relación sólida.
Req: Institucion. Ctx: Definir SLAs acordes a su misión, objetivos y tipo de servicios para optimizar operación y recursos.

### 5.2. Ejemplo de Valores de SLA

ID: GORE-GUIA-CLOUD-SLA-EJEMPLOS-01

- Cpt: Escenario. Def: Servicio crítico, uso mayoritario en horario hábil.
  - Cpt: SLA-Habil. Def: Más estricto (ej. 99.5% disponibilidad, 30 min tiempo respuesta soporte).
  - Cpt: SLA-No-Habil. Def: Más permisivo (ej. 97% disponibilidad, 4 horas respuesta soporte).

### 5.3. Elementos de un SLA

ID: GORE-GUIA-CLOUD-SLA-ELEMENTOS-01
Cpt: Lista-No-Taxativa.

- Disponibilidad o Tiempo de actividad (uptime): Porcentaje de tiempo de disponibilidad (ej. 99.9%).
- Rendimiento: Compromiso de desempeño (límites y capacidades) de recursos contratados.
- Tiempo de respuesta: Período máximo en que proveedor responde a solicitud/incidencia.
- Mantenimiento programado: Periodos en que servicio puede estar offline por mantenimiento.
- Compensación por incumplimiento: Medidas correctivas o compensaciones (créditos, extensiones).
- Seguridad y cumplimiento normativo: Medidas de seguridad y estándares de cumplimiento.
- Escalación y resolución de problemas: Procedimientos para informar y resolver problemas.
- Backup y recuperación de datos: Políticas de copia de seguridad, frecuencia y procedimientos de recuperación.

### 5.4. Establecimiento e Implementación de SLAs

ID: GORE-GUIA-CLOUD-SLA-ESTABLECIMIENTO-01
Req: Critico. Ctx: Establecer SLA claro en requerimiento técnico y controlar su implementación.
Cpt: Pasos-Consideraciones.

- Objetivos y requisitos claros: Definir objetivos institucionales y requisitos específicos.
- Establecer expectativas claras: Definir métricas y condiciones comprensibles para ambas partes.
- Personalización del SLA: Buscar adaptar el SLA a necesidades específicas.
- Negociación proactiva: Proporcionar métricas y datos de uso proyectado para fundamentar solicitudes.
- Establecer multas y compensaciones claras: Proporcionales al impacto del incumplimiento.
- Incluir cláusulas de revisión: Integrar cláusulas de revisión periódica para ajustar el SLA.
- Considerar la escalabilidad: Anticipar necesidades futuras de escalabilidad.
- Mantenimiento de una relación de colaboración: Fomentar trabajo conjunto y comunicación abierta (ej. reuniones periódicas).

### 5.5. Seguimiento y Cumplimiento de SLAs

ID: GORE-GUIA-CLOUD-SLA-SEGUIMIENTO-01
Rec: Seguimiento-Efectivo.

- Establecer un equipo de gestión: Dedicado a supervisar cumplimiento (representantes de áreas técnica, legal, gestión).
- Definir métricas de monitoreo: Identificar métricas clave para evaluar rendimiento.
- Implementar herramientas de monitoreo: Para seguimiento en tiempo real.
- Programar revisiones periódicas: Reuniones regulares con el proveedor para análisis y planificación.
- Automatizar informes de cumplimiento: Implementar sistemas de generación automática de informes claros y detallados.
- Establecer auditorías periódicas: Para evaluar cumplimiento en profundidad (internas o externas).
- Gestión proactiva de problemas: Desarrollar proceso para identificar desviaciones recurrentes.
- Establecer un sistema de seguimiento de incidentes: Para registrar, clasificar y analizar interrupciones.
- Revisar y actualizar el SLA: Mantener el SLA actualizado y ajustarlo según sea necesario.
- Fomentar la comunicación abierta: Establecer canales efectivos para resolución rápida de problemas.
