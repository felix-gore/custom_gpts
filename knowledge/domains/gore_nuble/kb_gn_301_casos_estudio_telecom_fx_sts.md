# Repositorio de Casos de Estudio para Proyectos de Telecomunicaciones

ID: GUIDE-STS-METADATA-01
Version: 1.0.0
Status: Draft
Human-Creator: FS
Human-Editor: FS
Model-Collaborator: IA-GEMINI
Creation-Date: 2025-07-07
Modification-Date: 2025-07-07
Primary-Source: N/A
Ref-STS-Guide: GUIDE-STS-MASTER-01


ID: GORE-NUBLE-TELECOM-CASES-REPO-01
Purp: Consolidar casos de estudio de proyectos de telecomunicaciones relevantes para el GORE Ñuble, analizando problemas, soluciones y lecciones aprendidas para informar la formulación de futuras iniciativas.

## Caso 01: Proyecto Estratégico de Conectividad Troncal - Fibra Óptica Austral (FOA)

ID: GORE-CASO-001

### Resumen Ejecutivo

ID: GORE-CASO-001-SUMMARY

- Def: Proyecto de infraestructura de telecomunicaciones de alta capacidad.
- Fnd: Subsidiado por el Estado a través del Fondo de Desarrollo de las Telecomunicaciones (FDT).
- Obj: Conectar las regiones de Los Lagos, Aysén y Magallanes.
- Mech: Despliegue de una troncal submarina y tres troncales terrestres de fibra óptica.
- Mdl: Operación bajo modelo de acceso abierto y no discriminatorio como servicio intermedio.
- Ctx: Código de proyecto FDT-2017-01.
- Ctx: Inversión subsidiada > 57 mil millones CLP.
- Ctx: Adjudicado en 2017; operación por fases.
- Obj: Resolver el aislamiento digital histórico de la zona austral.
- Obj: Mejorar la soberanía en comunicaciones.
- Obj: Crear una base para futuros servicios de última milla.
- Src: Ref: GORE-CASO-SRC-01

### Problema Original y Brecha de Conectividad Estratégica

ID: GORE-CASO-001-PROBLEM

- Cause: Aislamiento digital crónico en regiones australes de Chile.
- Dep: Conectividad dependía de enlaces terrestres por territorio argentino.
- Res: Riesgos de soberanía, altos costos y baja resiliencia ante fallas.
- Cause: Ausencia de infraestructura de alta capacidad (backbone) en territorio nacional.
- Res: Impedimento para el desarrollo de servicios de telecomunicaciones modernos.
- Res: Limitación al crecimiento económico, la integración territorial y el acceso a servicios públicos digitales.
- Ctx: Afecta a casi medio millón de habitantes.
- Ctx: Falla de mercado estructural.
- Just: Altos costos de inversión y baja densidad poblacional hacían inviable el proyecto para el sector privado sin subsidio estatal.
- Src: Ref: GORE-CASO-SRC-04

### Solución Implementada

ID: GORE-CASO-001-SOLUTION

#### Descripción Técnica General

ID: GORE-CASO-001-SOLUTION-TECH

- Cpt: Troncal Submarina Austral (~2,870 km).
- Cpt: Tres Troncales Terrestres (Magallanes, Aysén, Los Lagos).
- Mech: Cable de fibra óptica submarino con repetidores ópticos.
- Mech: Trazado soterrado y aéreo en tramos terrestres.
- Mech: Habilitación de Puntos de Operación e Interconexión de Infraestructura Óptica de Telecomunicaciones (POIIT).
- Def: POIIT son nodos de acceso que permiten a cualquier empresa de telecomunicaciones conectarse a la troncal de manera abierta y no discriminatoria.
- Src: Ref: GORE-CASO-SRC-01

#### Modelo de Servicio

ID: GORE-CASO-001-SOLUTION-MODEL

- Mdl: Concesión como "servicio intermedio de telecomunicaciones que únicamente provea infraestructura física".
- Resp: Empresas adjudicatarias no venden servicios al cliente final.
- Resp: Rol es construir, operar, mantener y arrendar capacidad de la infraestructura física (hilos de fibra).
- Dest: Arrendatarios son otros operadores (Entel, Movistar, GTD, etc.) que llevan sus servicios a usuarios finales.
- Fnd: Modelo de acceso abierto para fomentar la competencia en el mercado de servicios finales.
- Ctx: Empresas adjudicatarias incluyen Comunicación y Telefonía Rural S.A. y Conductividad Austral Ltda.
- Src: Ref: GORE-CASO-SRC-01

### Estructura de Costos

ID: GORE-CASO-001-COSTS

- Def: Inversión total subsidiada por el Estado (FDT) > 60 mil millones CLP.
- Just: Subsidio máximo de ~100 millones de dólares para cubrir brecha entre costo real y financiación privada.
- Resp: Costos operativos son de las empresas concesionarias durante el periodo de concesión.
- Src: Ref: GORE-CASO-SRC-01

|ID Tramo|Descripción Tramo|Empresa Adjudicataria|Subsidio Asignado (M CLP)|Fuente de Datos y Fecha|
|-|-|-|-|-|
|FDT-2017-01-AUS|Troncal Submarina Austral|Comunicación y Telefonía Rural S.A. (CTR)|52,691,970|Ctx: Informe SUBTEL 4T 2021. Src: Ref: GORE-CASO-SRC-01|
|FDT-2017-01-MAG|Troncal Terrestre Magallanes|Conductividad Austral Ltda.|4,888,861|Ctx: Informe SUBTEL 4T 2021. Src: Ref: GORE-CASO-SRC-01|
|FDT-2018-02-AYS|Troncal Terrestre Aysén|Silica Networks Chile S.A.|4,317,990|Ctx: Informe SUBTEL 1T 2022. Src: Ref: GORE-CASO-SRC-02|
|FDT-2018-02-LAG|Troncal Terrestre Los Lagos|Silica Networks Chile S.A.|1,820,085|Ctx: Informe SUBTEL 1T 2022. Src: Ref: GORE-CASO-SRC-02|

### Fuente de Financiamiento

ID: GORE-CASO-001-FUNDING

- Fnd: Subsidio directo del Fondo de Desarrollo de las Telecomunicaciones (FDT).
- Resp: FDT es administrado por la Subsecretaría de Telecomunicaciones (SUBTEL).
- Purp: Promover inversión en zonas no rentables para privados, corrigiendo fallas de mercado y reduciendo brecha digital.
- Src: Ref: GORE-CASO-SRC-06

### Lecciones Aprendidas

ID: GORE-CASO-001-LESSONS

#### Estructuración de Licitaciones y Atractivo para el Sector Privado

ID: GORE-CASO-001-LESSON-BIDDING

- Ctx: Primer intento de licitación (2016) declarado desierto por falta de postulantes.
- Cause: Subsidio ofrecido considerado insuficiente para los riesgos y costos del proyecto.
- Cause: Condiciones del Estado (reserva de capacidad, tarifas reguladas) consideradas demasiado restrictivas.
- Res: Desincentivo a la inversión privada.
- Rec: Proyectos públicos con co-inversión privada deben equilibrar interés público y viabilidad comercial.
- Rec: La formulación debe considerar el caso de negocio desde la perspectiva del inversionista.
- Src: Ref: GORE-CASO-SRC-10

#### Sostenibilidad del Modelo de Negocio a Largo Plazo

ID: GORE-CASO-001-LESSON-SUSTAINABILITY

- Ctx: Concesión por 30 años.
- Warn: Regulación de tarifas máximas solo cubre los primeros 20 años.
- Res: Incertidumbre regulatoria y económica para la última década del proyecto.
- Warn: Riesgo de que el concesionario ejerza poder de mercado y aumente precios post-regulación.
- Rec: La planificación de la sostenibilidad a largo plazo, incluyendo el marco regulatorio post-subsidio, es crucial.
- Src: Ref: GORE-CASO-SRC-06

#### Interdependencia entre Infraestructura Troncal y Última Milla

ID: GORE-CASO-001-LESSON-LASTMILE

- Ctx: FOA es un proyecto de infraestructura troncal ("middle mile").
- Warn: Su construcción es una condición necesaria pero no suficiente para la conectividad de usuarios finales.
- Rec: La inversión en infraestructura troncal debe ser planificada y coordinada con futuras inversiones en redes de "última milla".
- Rec: Un proyecto troncal debe tener un plan de capilaridad para llegar a los usuarios.
- Instr: La existencia de proyectos como Fibra Óptica Nacional (FON) en Ñuble debe ser el punto de partida para diseños de conectividad local.
- Obj: Identificar POIIT más cercanos para minimizar costos de interconexión.
- Src: Ref: GORE-CASO-SRC-02

## Caso 02: Conectividad Comunitaria en Zonas Rurales - Red Digital APR La Araucanía

ID: GORE-CASO-002

### Resumen Ejecutivo

ID: GORE-CASO-002-SUMMARY

- Def: Iniciativa colaborativa para desplegar una red de conectividad digital en zonas rurales de La Araucanía.
- Resp: Gobierno Regional (GORE) de La Araucanía y Fundación Desafío Levantemos Chile.
- Mech: Aprovechamiento de infraestructura y organización de sistemas de Agua Potable Rural (APR) para instalar 278 puntos de acceso WiFi gratuitos.
- Ctx: Inversión regional de más de 4.5 mil millones de pesos.
- Cpt: Provisión de infraestructura.
- Cpt: Alfabetización y capacitación digital.
- Obj: Abordar tanto la brecha de acceso como la de uso.
- Src: Ref: GORE-CASO-SRC-12

### Problema Original y Brecha de Acceso y Adopción Digital

ID: GORE-CASO-002-PROBLEM

- Cause: La Araucanía presenta la tasa más baja de acceso a internet fijo en Chile (33%).
- Cause: La Araucanía tiene la mayor proporción de población rural del país.
- Res: Profunda brecha digital de infraestructura y habilidades.
- Res: Exclusión digital limita acceso a tele-educación, telemedicina, oportunidades laborales, comercio electrónico y trámites estatales.
- Obj: Solucionar la falta de puntos de conexión en la ruralidad y la falta de capacidades en la población para usar herramientas digitales.
- Src: Ref: GORE-CASO-SRC-12

### Solución Implementada

ID: GORE-CASO-002-SOLUTION

#### Descripción Técnica

ID: GORE-CASO-002-SOLUTION-TECH

- Mech: Despliegue de una red distribuida de 278 puntos de acceso WiFi.
- Ctx: Equipamiento instalado en sedes de comités de Agua Potable Rural (APR).
- Purp: Un punto WiFi para la gestión administrativa del APR (habilita telemetría y sensorización).
- Purp: Un punto WiFi orientado a la comunidad, proveyendo acceso gratuito a internet en un espacio público ("plaza digital").
- Src: Ref: GORE-CASO-SRC-12

#### Componente de Capacitación y Adopción

ID: GORE-CASO-002-SOLUTION-TRAINING

- Cpt: Integración de capacitación y acompañamiento a comunidades como componente central.
- Act: Diseño e impartición de talleres de alfabetización digital.
- Dest: Habitantes, especialmente adultos mayores y emprendedores.
- Obj: Que las comunidades aprovechen la conectividad para desarrollar su potencial productivo y social.
- Src: Ref: GORE-CASO-SRC-12

### Estructura de Costos

ID: GORE-CASO-002-COSTS

- Ctx: Presupuesto total aprobado por el GORE de $4.578.711.816 CLP.
- Ctx: El monto cubre inversión en equipamiento, instalación y costos de gestión social y capacitación.
- Src: Ref: GORE-CASO-SRC-12

|Componente|Costo Total (M CLP)|Costo Promedio por Punto de Acceso (CLP)|Notas|
|-|-|-|-|
|Inversión Total del Programa|4,578.7|16,470,186|Ctx: Costo total aprobado por el GORE La Araucanía.|
|Infraestructura (Hardware y Despliegue)|3,205.1|11,529,130|Ctx: Estimado 70%. Basado en benchmarks de proyectos similares.|
|Capacitación y Gestión Social|1,373.6|4,941,056|Ctx: Estimado 30%. Incluye alfabetización digital y acompañamiento.|

### Fuente de Financiamiento

ID: GORE-CASO-002-FUNDING

- Fnd: Aprobado en su totalidad por el Consejo Regional de La Araucanía con fondos del Fondo Nacional de Desarrollo Regional (FNDR).
- Mdl: Colaboración donde una OSC (Fundación Desafío Levantemos Chile) presenta un proyecto financiado con fondos públicos regionales.
- Src: Ref: GORE-CASO-SRC-12

### Lecciones Aprendidas

ID: GORE-CASO-002-LESSONS

#### Sinergia con Infraestructura Comunitaria Existente (APR)

ID: GORE-CASO-002-LESSON-SYNERGY

- Ctx: Uso de comités de APR como ancla para el despliegue fue una decisión estratégica clave.
- Just: En el mundo rural, la logística (ubicación, energía, seguridad) y la aceptación social son desafíos mayores.
- Ctx: APRs son organizaciones con legitimidad, presencia física y necesidad propia de conectividad.
- Res: Se resolvió el problema de la ubicación física de los equipos.
- Res: Se aseguró el suministro eléctrico.
- Res: Se generó un doble beneficio (gestión del agua y conectividad comunitaria).
- Res: Se facilitó la apropiación del proyecto por parte de la comunidad.
- Rec: Buscar sinergias con infraestructura y capital social preexistente para acelerar el despliegue y maximizar el impacto.
- Src: Ref: GORE-CASO-SRC-12

#### La Adopción Digital como Componente Central del Proyecto

ID: GORE-CASO-002-LESSON-ADOPTION

- Ctx: El proyecto integra la capacitación como componente central y presupuestariamente significativo.
- Fnd: Reconoce que la brecha digital tiene dos componentes: acceso (infraestructura) y uso (capacidades).
- Rec: La inversión pública en conectividad debe ir acompañada de inversión planificada en desarrollo de habilidades digitales.
- Just: Permite que el retorno social de la inversión se materialice plenamente.
- Def: Un proyecto exitoso no solo conecta lugares, sino que empodera a las personas.
- Src: Ref: GORE-CASO-SRC-13

## Caso 03: Conectividad Satelital para Zonas Aisladas - Piloto HughesNet en Colmuyao (Cobquecura, Ñuble)

ID: GORE-CASO-003

### Resumen Ejecutivo

ID: GORE-CASO-003-SUMMARY

- Def: Proyecto piloto de conectividad satelital gestionado por el GORE de Ñuble.
- Fnd: Originado a partir de una donación de la empresa Hughes.
- Mech: Proveyó acceso a internet gratuito a cuatro puntos estratégicos en Colmuyao (Cobquecura).
- Dest: Escuela básica, posta de salud rural, cuartel de bomberos y sede vecinal.
- Obj: Probar la viabilidad de la tecnología satelital (VSAT) como solución rápida y efectiva para zonas remotas de la región.
- Just: Zonas donde la infraestructura terrestre es inexistente o su despliegue es inviable.
- Src: Ref: GORE-CASO-SRC-16

### Problema Original y Aislamiento Digital Extremo

ID: GORE-CASO-003-PROBLEM

- Cause: Localidad de Colmuyao carecía de acceso a servicios de telecomunicaciones estables por aislamiento geográfico.
- Res: Afectación crítica de servicios públicos esenciales.
- Res: Limitación de recursos educativos en la escuela.
- Res: Impedimento para que la posta de salud accediera a información o telemedicina.
- Res: Dificultad en la coordinación de emergencias de bomberos.
- Res: Obstaculización de la organización comunitaria.
- Ctx: Caso representativo de "brecha digital dura", donde soluciones convencionales (fibra, móvil) no llegan.
- Src: Ref: GORE-CASO-SRC-17

### Solución Implementada

ID: GORE-CASO-003-SOLUTION

#### Descripción Técnica

ID: GORE-CASO-003-SOLUTION-TECH

- Mech: Instalación de cuatro terminales de internet satelital con tecnología VSAT (Very Small Aperture Terminal).
- Cpt: Cada terminal consiste en una antena parabólica que establece comunicación con un satélite geoestacionario (GEO).
- Ctx: Servicio opera a través del satélite "Hughes 63 West".
- Res: Conexión a internet completamente independiente de la infraestructura terrestre.
- Src: Ref: GORE-CASO-SRC-17

#### Modelo de Gestión

ID: GORE-CASO-003-SOLUTION-MODEL

- Mdl: Colaboración público-privada basado en una donación.
- Resp: Empresa Hughes proveyó equipamiento y servicio de forma gratuita.
- Resp: GORE Ñuble actuó como gestor y articulador, identificando necesidades y facilitando la implementación.
- Ctx: Coordinación con el municipio de Cobquecura.
- Src: Ref: GORE-CASO-SRC-17

### Estructura de Costos

ID: GORE-CASO-003-COSTS

- Fnd: Donación, sin desembolso directo de fondos públicos para la inversión inicial.
- Ctx: Para planificación, es posible valorizar el aporte.
- Src: Ref: GORE-CASO-SRC-17

|Ítem|Cantidad|Costo Unitario Estimado (CLP)|Costo Total Estimado (CLP)|Notas|
|-|-|-|-|-|
|Kit Satelital (Antena, Modem)|4|450,000|1,800,000|Ctx: Basado en precios de mercado para equipos LEO/GEO.|
|Servicio Anual (4 puntos)|1|1,680,000|1,680,000|Ctx: Basado en plan de $35.000/mes x 4 puntos x 12 meses.|
|Total Valorizado (Año 1)|-|-|3,480,000|Warn: No incluye costos de instalación ni gestión del GORE.|

### Fuente de Financiamiento

ID: GORE-CASO-003-FUNDING

- Fnd: Donación directa de la empresa privada Hughes.
- Ctx: Gestionado por GORE Ñuble, pero no utilizó fondos FNDR ni FDT.
- Src: Ref: GORE-CASO-SRC-17

### Lecciones Aprendidas

ID: GORE-CASO-003-LESSONS

#### Viabilidad de Soluciones Satelitales para Servicios Públicos Críticos

ID: GORE-CASO-003-LESSON-VIABILITY

- Res: Piloto demostró que la tecnología satelital GEO es una solución viable y efectiva para servicios públicos críticos en zonas de extremo aislamiento.
- Ctx: A pesar de tener latencia mayor que la fibra óptica.
- Res: Evaluación de la estabilidad de la señal por parte del GORE fue positiva.
- Rec: Validar esta tecnología como herramienta clave en el portafolio de soluciones de conectividad de la región.
- Src: Ref: GORE-CASO-SRC-17

#### Agilidad de Implementación y Rol del GORE como Articulador

ID: GORE-CASO-003-LESSON-AGILITY

- Res: La implementación del piloto fue notablemente ágil.
- Rec: Proyectos de menor escala con gestión clara y colaboración público-privada pueden generar impacto rápido.
- Rec: El GORE puede jugar un rol proactivo como catalizador y articulador, buscando alianzas con el sector privado.
- Purp: Implementar soluciones tácticas y de alto impacto en el corto plazo.
- Just: Estos pilotos permiten probar tecnologías y generar beneficios inmediatos mientras avanzan proyectos estratégicos de largo ciclo.
- Src: Ref: GORE-CASO-SRC-17

## Caso 04: Proyecto de Última Milla para Conectividad Rural - Región de La Araucanía

ID: GORE-CASO-004

### Resumen Ejecutivo

ID: GORE-CASO-004-SUMMARY

- Def: Proyecto de inversión regional para llevar conectividad de "última milla" a 65 localidades rurales y aisladas.
- Fnd: Financiado por el GORE de La Araucanía con un presupuesto > 14 mil millones de pesos.
- Resp: Diseñado en conjunto con la Subsecretaría de Telecomunicaciones (SUBTEL).
- Purp: Complementar la infraestructura troncal de la Fibra Óptica Nacional (FON).
- Obj: Construir "rampas de acceso" a la autopista digital, proveyendo servicios directos (telefonía, datos, internet) a comunidades marginadas.
- Src: Ref: GORE-CASO-SRC-03

### Problema Original y la Paradoja de la "Carretera Digital"

ID: GORE-CASO-004-PROBLEM

- Cause: A pesar de la existencia de la red troncal FON, gran cantidad de localidades rurales permanecen desconectadas.
- Cause: Falta de capilaridad de la red.
- Warn: La infraestructura troncal por sí sola no genera beneficios directos si no existen redes de acceso ("última milla").
- Res: Se crea la paradoja de tener una "carretera digital" cercana pero sin "rampas de acceso".
- Res: Se perpetúa la brecha digital local y se subutiliza la inversión nacional.
- Src: Ref: GORE-CASO-SRC-03

### Solución Implementada

ID: GORE-CASO-004-SOLUTION

#### Descripción Técnica

ID: GORE-CASO-004-SOLUTION-TECH

- Mech: Solución tecnológica mixta y adaptada a la geografía de cada una de las 65 localidades.
- Cpt: Extensiones de fibra óptica desde los nodos FON hasta los centros poblados.
- Cpt: Instalación de nuevas antenas y estaciones base para servicios móviles (4G/5G).
- Cpt: Posible uso de radioenlaces de microondas o enlaces satelitales en zonas de difícil acceso.
- Obj: Entregar conectividad de alta velocidad directamente a hogares, escuelas y servicios públicos locales.
- Src: Ref: GORE-CASO-SRC-03

### Estructura de Costos

ID: GORE-CASO-004-COSTS

- Ctx: Costo total aprobado por el Consejo Regional > $14.500 millones de pesos.
- Ctx: Se aprobó un primer traspaso de fondos por $9.413 millones.
- Purp: Financiamiento se destina a subsidiar, vía licitación pública, a empresas que se adjudiquen el despliegue, operación y mantenimiento.
- Src: Ref: GORE-CASO-SRC-03

|Hito de Financiamiento|Monto (M CLP)|Estado|Fuente de Datos y Fecha|
|-|-|-|-|
|Presupuesto Total Aprobado|14,500|Aprobado|Src: Ref: GORE-CASO-SRC-03|
|Primer Traspaso para Ejecución|9,413|Aprobado|Src: Ref: GORE-CASO-SRC-03|

### Fuente de Financiamiento

ID: GORE-CASO-004-FUNDING

- Fnd: Financiado íntegramente con fondos del GORE de La Araucanía a través del FNDR.
- Ctx: Caso de inversión regional directa y descentralizada para resolver una necesidad local.
- Ctx: Actúa en coordinación y como complemento a la política nacional de telecomunicaciones de SUBTEL.
- Src: Ref: GORE-CASO-SRC-03

### Lecciones Aprendidas

ID: GORE-CASO-004-LESSONS

#### Rol Protagónico de los Gobiernos Regionales en el Cierre de Brechas

ID: GORE-CASO-004-LESSON-GORE-ROLE

- Res: GOREs tienen un rol protagónico e insustituible en la planificación y financiamiento de la conectividad de última milla.
- Just: El nivel central se enfoca en las grandes autopistas digitales (FON, FOA).
- Just: Las administraciones regionales poseen el conocimiento detallado del territorio para identificar "puntos ciegos".
- Rec: La proactividad regional y la planificación territorial son claves para que la política nacional de conectividad tenga impacto real y equitativo.
- Ctx: GOREs no son meros ejecutores, sino diseñadores estratégicos de la conectividad a escala humana.
- Src: Ref: GORE-CASO-SRC-03

#### Complementariedad de Fondos y Estrategias (FDT y FNDR)

ID: GORE-CASO-004-LESSON-COMPLEMENTARITY

- Ctx: El proyecto es un ejemplo de complementariedad financiera y estratégica entre niveles de gobierno.
- Mech: Inversión nacional (FDT en FON) crea las condiciones para que la inversión regional (FNDR) sea más eficiente.
- Warn: Sin la red FON, el costo de este proyecto de última milla sería prohibitivamente mayor.
- Rec: La planificación de la inversión pública debe ser multi-escalar, coordinando fondos nacionales (FDT) con regionales (FNDR).
- Obj: Maximizar el impacto de cada peso invertido y evitar la duplicación de esfuerzos.
- Rec: Un proyecto regional de última milla bien formulado debe apalancar la inversión nacional ya realizada.
- Src: Ref: GORE-CASO-SRC-03

## Fuentes Citadas

ID: GORE-CASO-SOURCES-01

- ID: GORE-CASO-SRC-01. Def: INFORME NACIONAL - Subtel. Ctx: Consulta Jul-2025. URL: <https://www.subtel.gob.cl/wp-content/uploads/2022/01/Informe_Nacional_4T_2021.pdf>
- ID: GORE-CASO-SRC-02. Def: INFORME NACIONAL - Subtel. Ctx: Consulta Jul-2025. URL: <https://www.subtel.gob.cl/wp-content/uploads/2022/04/Informe_Nacional_1T2022.pdf>
- ID: GORE-CASO-SRC-03. Def: Aprueban recursos para proyecto de conectividad a localidades apartadas en La Araucanía. Ctx: Consulta Jul-2025. URL: <https://www.soychile.cl/temuco/sociedad/2023/11/13/835495/aprueban-proyecto-conectividad-araucania.html>
- ID: GORE-CASO-SRC-04. Def: Chile resuelve licitación para instalar fibra óptica en la zona austral - El Mostrador. Ctx: Consulta Jul-2025. URL: <https://www.elmostrador.cl/agenda-pais/2017/10/17/chile-resuelve-licitacion-para-instalar-fibra-optica-en-la-zona-austral/>
- ID: GORE-CASO-SRC-05. Def: INTERNET BANDA ANCHA EN LAS ÁREAS RURALES DE CHILE - Subtel. Ctx: Consulta Jul-2025. URL: <https://www.subtel.gob.cl/internet-banda-ancha-en-las-areas-rurales-de-chile/>
- ID: GORE-CASO-SRC-06. Def: RESUMEN EJECUTIVO FONDO DE DESARROLLO DE ... - Dipres. Ctx: Consulta Jul-2025. URL: <http://www.dipres.cl/597/articles-285481_r_ejecutivo_institucional.pdf>
- ID: GORE-CASO-SRC-07. Def: Gobierno e Industria de las Telecomunicaciones anuncian Acuerdo Nacional para reducir la brecha digital - Gob.cl. Ctx: Consulta Jul-2025. URL: <https://www.gob.cl/noticias/gobierno-e-industria-de-las-telecomunicaciones-anuncian-acuerdo-nacional-para-reducir-la-brecha-digital/>
- ID: GORE-CASO-SRC-08. Def: INFORME RESULTADO DEL PROCESO DE EVALUACIÓN SUBTEL Y ADJUDICACIÓN... Ctx: Consulta Jul-2025. URL: <https://www.subtel.gob.cl/wp-content/uploads/2017/11/Informe_Resumen_Adjudicacion_Proyeto_Fibra_Optica_Austral.pdf>
- ID: GORE-CASO-SRC-09. Def: Sección 1: Antecedentes PROGRAMA NUEVO 2023. Ctx: Consulta Jul-2025. URL: <https://www.dipres.gob.cl/597/articles-285562_doc_pdf1.pdf>
- ID: GORE-CASO-SRC-10. Def: Fracasa licitación de fibra óptica austral - Diario Financiero. Ctx: Consulta Jul-2025. URL: <https://www.df.cl/empresas/telecom-tecnologia/fracasa-licitacion-de-fibra-optica-austral>
- ID: GORE-CASO-SRC-11. Def: Desarrollo de las Telecomunicaciones en Chile - ITU. Ctx: Consulta Jul-2025. URL: <https://www.itu.int/en/ITU-D/Regional-Presence/Americas/Documents/EVENTS/2014/0804-PY-Cnntvity/8_S3_Present_Pedro_Huichalaf_COSIPLAN-CHILE.pdf>
- ID: GORE-CASO-SRC-12. Def: Gore aprueba programa que llevará internet a sectores rurales de ... Ctx: Consulta Jul-2025. URL: <https://novenadigital.cl/gore-aprueba-programa-que-llevara-internet-a-sectores-rurales-de-la-araucania/>
- ID: GORE-CASO-SRC-13. Def: Presentación de PowerPoint - Asociación Chilena de Municipalidades. Ctx: Consulta Jul-2025. URL: <https://www.achm.cl/wp-content/uploads/2023/12/Programas-de-Conectividad-Rural.pdf>
- ID: GORE-CASO-SRC-14. Def: Lanzan programa que entregará internet a familias rurales de la región - Tiempo21. Ctx: Consulta Jul-2025. URL: <https://www.tiempo21.cl/lanzan-programa-que-entregara-internet-a-familias-rurales-de-la-region/>
- ID: GORE-CASO-SRC-15. Def: Sistema Nacional de Inversiones - Asociación Chilena de Municipalidades. Ctx: Consulta Jul-2025. URL: <https://www.achm.cl/wp-content/uploads/2023/08/IGNACIO-CANALES-1.pdf>
- ID: GORE-CASO-SRC-16. Def: Internet satelital de HughesNet está presente en la Región de Ñuble - SanCarlosOnline. Ctx: Consulta Jul-2025. URL: <https://www.sancarlosonline.cl/2021/05/internet-satelital-de-hughesnet-esta.html>
- ID: GORE-CASO-SRC-17. Def: Inauguran proyecto de conexión a internet gratuita para Colmuyao. Ctx: Consulta Jul-2025. URL: <https://goredenuble.cl/inauguran-proyecto-de-conexion-a-internet-gratuita-para-colmuyao/>
- ID: GORE-CASO-SRC-18. Def: Satélites GEO JUPITER - Hughes Network Systems. Ctx: Consulta Jul-2025. URL: <https://www.hughes.com/cl/soluciones/servicios-satelitales-systems-terrestre/flota-satelites-de-jupiter>
- ID: GORE-CASO-SRC-19. Def: Internet Satelital - Claro Chile. Ctx: Consulta Jul-2025. URL: <https://www.clarochile.cl/personas/servicios/servicios-hogar/internet/internet-satelital/>
- ID: GORE-CASO-SRC-20. Def: 65 localidades aisladas de La Araucanía se beneficiarán con proyecto de conectividad digital | Subtel. Ctx: Consulta Jul-2025. URL: <https://www.subtel.gob.cl/65-localidades-aisladas-de-la-araucania-se-beneficiaran-con-proyecto-de-conectividad-digital/>
- ID: GORE-CASO-SRC-21. Def: Localidades aisladas de La Araucanía se beneficiarán con proyecto de conectividad digital. Ctx: Consulta Jul-2025. URL: <https://www.elmostrador.cl/agenda-pais/agenda-digital/2023/11/16/localidades-aisladas-de-la-araucania-se-beneficiaran-con-proyecto-de-conectividad-digital/>
