# Base de Datos de Costos de Referencia para Proyectos de Telecomunicaciones

ID: KB-GN-303-COSTOS-TELECOM-V1.0
Version: 1.0.0
Status: Published
Human-Creator: FS
Human-Editor: FS
Model-Collaborator: IA-GEMINI
Creation-Date: 2025-07-07
Modification-Date: 2025-07-07
Primary-Source: kb_gn_303_costos_referencia_telecom_sts.md
Ref-STS-Guide: GUIDE-STS-MASTER-01

## 1. Marco Analítico

ID: KB-GN-303-FRAMEWORK-01

### 1.1. Propósito y Metodología

ID: KB-GN-303-FRAMEWORK-PURP-01
Purp: Apoyar la fase de formulación de proyectos de telecomunicaciones en la Región de Ñuble.
Mssn: Servir como herramienta cuantitativa para estimaciones presupuestarias realistas, consistentes y verificables.
Fnd: Metodología del Sistema Nacional de Inversiones (SNI).
Warn: No es una lista de precios de mercado fijos.
Def: Compendio de valores referenciales para el año 2025, destinados a la planificación y evaluación de perfiles de proyectos.
Mech: Triangulación de datos de múltiples fuentes para obtener valores robustos y contextualizados.
Cpt: Fuentes Utilizadas

- Src: Licitaciones Públicas Adjudicadas (Mercado Público). Ctx: Montos de adjudicación como indicador de costo final para el Estado. Ref: SRC-01.
- Src: Proyectos del Fondo de Desarrollo de las Telecomunicaciones (FDT). Ctx: Presupuestos y subsidios de proyectos SUBTEL. Ref: SRC-03.
- Src: Catálogos de distribuidores y proveedores en Chile. Ctx: Precios de lista que internalizan costos de importación, logística y garantía. Ref: SRC-05.
- Src: Precios de Retail y E-commerce. Ctx: Cota superior y componentes de menor escala. Ref: SRC-08.
- Src: Encuestas Salariales y Ofertas Laborales. Ctx: Derivación de tarifas horarias para servicios profesionales. Ref: SRC-11.
- Src: Índices Sectoriales (CChC). Ctx: Contextualización de tendencias de costos en obras civiles (ej. IPMIC). Ref: SRC-15.
Req: Todos los costos son referenciales y deben ser ajustados en la etapa de ingeniería de detalle del proyecto.
Cpt: Factores de Ajuste Específicos
- Cpt: Economías de escala.
- Cpt: Condiciones geográficas particulares.
- Cpt: Estacionalidad.
- Cpt: Evolución de la inflación.

### 1.2. Factores Clave de Costos

ID: KB-GN-303-FRAMEWORK-FACTORS-01
Ctx: Chile y Región de Ñuble.

- Cpt: Impacto de Proyectos Nacionales
  - ID: KB-GN-303-FACTOR-NATL-PROJ-01
  - Ex: Fibra Óptica Nacional (FON), Fibra Óptica Austral (FOA). Ref: SRC-16, SRC-17.
  - Res: Establecen benchmarks de costos a nivel macro y modifican el ecosistema de infraestructura.
  - Ex: Un proyecto en Ñuble puede apalancar la existencia de un POI del FON, reduciendo costos marginales de conexión a la red troncal.
  - Data: Costo por kilómetro (FON) ~8.6 millones CLP. Src: SRC-16.
  - Purp: Servir como validador para estimaciones regionales.

- Cpt: Geografía y Ruralidad
  - ID: KB-GN-303-FACTOR-GEOGRAPHY-01
  - Ctx: Diversidad geográfica de la Región de Ñuble (valles pre-cordilleranos, zonas costeras, secano interior).
  - Res: Incremento de costos de obras civiles en terrenos rocosos o con pendientes.
  - Res: Variación en soluciones de última milla según dispersión poblacional (FTTH en cabeceras comunales vs. radioenlaces/satélite en zonas aisladas).

- Cpt: Logística y Cadena de Suministro
  - ID: KB-GN-303-FACTOR-LOGISTICS-01
  - Dep: Alta dependencia de importación de equipamiento tecnológico (OLTs, ONTs, radios, switches). Src: SRC-18.
  - Res: Costos expuestos a volatilidad del tipo de cambio, aranceles y costos logísticos.
  - Cpt: Rol de distribuidores locales. Src: SRC-05.
    - Res: Ofrecen disponibilidad inmediata, facturación local, soporte técnico y gestión de garantías.
    - Warn: Precios pueden ser mayores a los de plataformas mayoristas internacionales.

- Cpt: Marco Regulatorio y de Licitaciones
  - ID: KB-GN-303-FACTOR-REGULATION-01
  - Fnd: Marco de compras del Estado (Mercado Público). Ref: SRC-21.
  - Res: Precios de adjudicación son el indicador más fiable del costo real que enfrentará el GORE.
  - Ctx: Reflejan condiciones competitivas del mercado y costos indirectos internalizados por proveedores (garantías, seguros, etc.). Src: SRC-01.
  - Res: Estructura de bases de licitación y criterios de evaluación pueden influir en el precio final.

## 2. Costos Referenciales: Obras Civiles

ID: KB-GN-303-COSTS-CIVIL-01

### 2.1. Análisis del Subsector

ID: KB-GN-303-ANALYSIS-CIVIL-01
Cpt: Partida de inversión más significativa en despliegue de infraestructura física.
Req: Diferenciar entre costo de materiales y costo "llave en mano".
Rec: Utilizar costo "llave en mano" para formulación de proyectos (integra ingeniería, permisos, maquinaria, mano de obra, etc.).
Cpt: Referencia Clave (Ñuble)

- Proj: "Transferencia Fondo de Desarrollo de las Telecomunicaciones Fibra Óptica Ñuble – Última Milla" (FDT-2022-02).
- Data: Subsidio estatal de $5,234,400,000 CLP. Src: SRC-03.
- Data: Infraestructura troncal de ~591 km (primera etapa). Src: SRC-04.
- Res: Costo referencial de $8,856,853 CLP por kilómetro.
- Just: Benchmark de alta fiabilidad para troncales de fibra óptica rural en la región.
- Valid: Consistente con promedio nacional de FON (~$8.6 millones CLP/km). Src: SRC-16.
Cpt: Construcción de Nodos/Salas de Equipos
- Mech: Costo compuesto.
- Cpt: Costo Base (Obra Civil)
  - Data: ~12 UF/m² (~$450,000 CLP/m²). Src: SRC-15.
  - Def: Estructura segura (bodega, recinto de albañilería).
- Cpt: Costos Adicionales (Habilitación Técnica)
  - Def: Climatización de precisión (HVAC), sistemas de energía (UPS, generadores), puesta a tierra, seguridad física.
  - Mdl: Presupuestar como costo base + "add-ons" técnicos por m², según criticidad del nodo.

### 2.2. Tabla de Costos: Obras Civiles

ID: KB-GN-303-TABLE-CIVIL-01

|Componente/Servicio|Unidad|Costo Referencia (CLP)|Notas|Fuente|
|-|-|-|-|-|
|Despliegue Fibra Óptica Troncal Rural (Ñuble)|km|8.900.000|Ctx: Costo todo incluido. Fnd: Proyecto FDT-2022-02. Def: Incluye obras civiles, materiales, ingeniería, gestión. Req: No incluye costo de última milla FTTH.|Src: SRC-03, SRC-04|
|Zanja en terreno blando (tierra/maicillo)|metro lineal|15.000|Ctx: Profundidad 0.8-1.2m. Def: Incluye excavación, cama de arena, cinta advertencia, relleno. Req: No incluye reposición de superficies complejas (pavimento, hormigón).|Src: SRC-46|
|Zanja con reposición de acera/pavimento|metro lineal|45.000|Ctx: Costo mayor por corte, retiro escombros, reconstrucción según normativa municipal.|Src: SRC-48|
|Tendido aéreo en postación existente|km|3.500.000|Def: Incluye cable ADSS 48 hilos, herrajes, mano de obra. Req: No incluye costo de arriendo del poste a compañía eléctrica.|Src: SRC-24|
|Instalación Torre Ventada|24 mts|17.500.000|Def: Incluye torre, fundación, instalación, puesta a tierra. Ctx: Basado en licitación para sitio único; costo unitario disminuye con volumen.|Src: SRC-49|
|Instalación Torre Autosoportada|30 mts|28.000.000|Def: Incluye torre, fundación robusta, instalación, puesta a tierra. Req: No incluye balizaje nocturno (DGAC).|Src: SRC-50|
|Construcción Sala de Equipos (Obra Civil)|m²|450.000|Ctx: Equivalente a 12 UF/m². Def: Costo base de recinto seguro (radier, albañilería, techumbre). Req: No incluye habilitación técnica.|Src: SRC-15|
|Habilitación Técnica Sala de Equipos|m²|250.000|Ctx: Costo adicional a obra civil. Def: Incluye climatización básica, tablero eléctrico dedicado, puesta a tierra para telecomunicaciones.|Src: SRC-51|

## 3. Costos Referenciales: Equipamiento de Red

ID: KB-GN-303-COSTS-EQUIPMENT-01

### 3.1. Análisis del Subsector

ID: KB-GN-303-ANALYSIS-EQUIPMENT-01
Cpt: Estructura de Mercado Dual

- Cpt: Distribuidores locales autorizados. Src: SRC-05.
  - Res: Ofrecen garantía, soporte, facturación nacional. Internalizan costos de importación.
- Cpt: Importación directa (plataformas mayoristas). Src: SRC-18.
  - Res: Precios unitarios potencialmente más bajos.
  - Warn: Introduce complejidades logísticas, aduaneras y de riesgo técnico.
- Rec: Canales locales preferidos para proyectos públicos por trazabilidad y respaldo.
Cpt: Estratificación de Precios
- Just: El precio varía significativamente según calidad, software, garantía, soporte y costos de importación.
- Ex: OLT GPON 8-port genérica (~1.050 USD, importación directa) vs. OLT Ubiquiti 4-port (~1,422,600 CLP, distribuidor local). Src: SRC-27, SRC-05.
- Rec: Presentar opciones de costos por "niveles" (ej. Entry-Level, Enterprise, Carrier-Grade) según criticidad del proyecto.
Cpt: Equipos de Acceso Radioeléctrico Móvil (BBU, RRU)
- Warn: Costos opacos; precios de lista no representativos para despliegues nuevos. Src: SRC-19.
- Ctx: Grandes operadores negocian contratos marco masivos no públicos con vendors (Ericsson, Nokia, Huawei).
- Clarification: Costo de licencia 5G (~453M USD) es por uso de espectro, no por CAPEX de equipamiento. Src: SRC-29.
- Rec: Estimar un "costo por sitio" o "costo por celda" agregado, negociado con integrador/vendor.

### 3.2. Tabla de Costos: Equipamiento de Red

ID: KB-GN-303-TABLE-EQUIPMENT-01

|Componente|Especificación Clave|Costo Referencia (CLP)|Notas|Fuente|
|-|-|-|-|-|
|OLT GPON|8 Puertos, 2xSFP+ 10G Uplink|1.700.000|Ctx: Equipo tipo "pizza-box" para despliegues medianos. Def: Marca Ubiquiti o similar con soporte/garantía local.|Src: SRC-27|
|ONT GPON|1 Puerto GE, modo bridge|18.000|Ctx: Unidad de cliente final básica. Req: Precio por volumen puede ser menor.|Src: SRC-06|
|ONT GPON con WiFi|4 Puertos GE, WiFi AC1200|43.000|Ctx: Unidad de cliente final con funcionalidades de router doméstico integrado.|Src: SRC-55|
|Antena Microondas|5 GHz, 30 dBi, hasta 20km|190.000|Ctx: Enlace punto a punto (PtP) en banda no licenciada. Def: Precio por unidad (se requieren dos).|Src: SRC-08|
|Radioenlace Carrier Grade|Banda licenciada, 400 Mbps|7.000.000|Ctx: Equipo de alta disponibilidad para backhaul. Def: Precio por enlace completo (2 radios, 2 antenas), incluye redundancia 1+1 (Hot Standby).|Src: SRC-57|
|BBU+RRU (Sitio 4G/5G)|3 sectores, 1 banda (ej. 700MHz)|25.000.000|Ctx: Rango estimado para sitio nuevo. Warn: No es precio de lista; es parte de contrato mayor con vendor y es altamente negociable.|Src: SRC-19|
|Switch Agregación L2+|24x1G PoE, 4x10G SFP+|620.000|Ctx: Para agregar tráfico de múltiples sitios/OLTs. Def: Ofrece capa 2 avanzada y Power over Ethernet.|Src: SRC-07|
|Switch Agregación L3|8x2.5G PoE++, 2x10G SFP+|1.260.000|Ctx: Con capacidades de enrutamiento avanzadas. Def: Adecuado para núcleo de red regional pequeña, soporta interfaces de mayor velocidad.|Src: SRC-07|

## 4. Costos Referenciales: Sistemas de Energía

ID: KB-GN-303-COSTS-ENERGY-01

### 4.1. Análisis del Subsector

ID: KB-GN-303-ANALYSIS-ENERGY-01
Cpt: Categorías de Costo

- Cpt: Costo regulado de conexión a red eléctrica pública. Ref: CGE es el operador principal. Src: SRC-31.
- Cpt: CAPEX en sistemas de respaldo y autonomía energética.
Cpt: Costo de Empalme Eléctrico
- Warn: Presupuestar "Costo Total Instalado", no solo "Costo Compañía".
- Cpt: Costo Compañía
  - Def: Valor regulado cobrado por la distribuidora por la conexión física.
  - Ex: Empalme trifásico aéreo hasta 27 kW ~3.57 UF. Src: SRC-33.
- Cpt: Costo Total Instalado
  - Def: Incluye costo compañía + honorarios de instalador certificado SEC (proyecto TE1, instalación interior, tramitación).
  - Data: Rango estimado $280,000 - $890,000 CLP. Src: SRC-34.
Cpt: Arquitectura de Respaldo Energético
- Def: Sistema integrado, no soluciones alternativas.
- Cpt: UPS (Sistema de Alimentación Ininterrumpida). Src: SRC-09.
  - Purp: Respaldo instantáneo de corta duración (minutos) para mantener operación mientras arranca generador.
- Cpt: Generador Diésel. Src: SRC-36.
  - Purp: Respaldo de larga duración (horas/días).
  - Req: Tablero de Transferencia Automática (ATS) para sitios remotos y desatendidos.
- Cpt: Sistemas Solares Fotovoltaicos. Src: SRC-41.
  - Purp: Reducir costos operativos (OPEX).
  - Cpt: Combinado con banco de baterías. Src: SRC-42.
    - Res: Puede proveer autonomía energética completa, valioso en zonas rurales.
Rec: Presentar costos de forma modular para diseñar solución según criticidad y ubicación del sitio.

### 4.2. Tabla de Costos: Sistemas de Energía

ID: KB-GN-303-TABLE-ENERGY-01

|Componente/Servicio|Unidad/Capacidad|Costo Referencia (CLP)|Notas|Fuente|
|-|-|-|-|-|
|Empalme Eléctrico Trifásico (Costo Compañía)|hasta 27 kW|140.000|Ctx: Valor referencial 3.6 UF. Def: Solo cobro de la distribuidora. Req: No incluye proyecto TE1 ni instalación interior.|Src: SRC-33|
|Empalme Eléctrico Trifásico (Costo Total Instalado)|hasta 27 kW|550.000|Def: Incluye costo compañía, proyecto TE1, materiales y mano de obra de instalador certificado SEC para instalación estándar.|Src: SRC-34|
|UPS Online Rackeable|3 kVA / 2700 W|570.000|Ctx: UPS de doble conversión. Def: Ideal para proteger equipos de telecomunicaciones sensibles.|Src: SRC-09|
|Generador Diésel con ATS|10 kVA|3.300.000|Def: Equipo insonorizado con tablero de transferencia automática (ATS) para operación desatendida.|Src: SRC-36|
|Sistema Solar Fotovoltaico|por Watt-pico instalado|1.200|Ctx: Costo para sistemas on-grid >3 kWp. Def: Incluye paneles, inversor, montaje, instalación. Req: No incluye baterías.|Src: SRC-43|
|Batería de Litio para Respaldo Solar|por kWh de almacenamiento|500.000|Ctx: Costo para sistemas off-grid/híbridos. Ex: Una batería de 5 kWh para autonomía nocturna costaría ~2,500,000 CLP.|Src: SRC-42|

## 5. Costos Referenciales: Servicios Profesionales

ID: KB-GN-303-COSTS-SERVICES-01

### 5.1. Análisis del Subsector

ID: KB-GN-303-ANALYSIS-SERVICES-01
Warn: La tarifa horaria no es el salario mensual dividido por horas.
Mech: Cálculo de Tarifa Cargada (de venta)

- Fml: (Salario Bruto + Costos de Leyes Sociales + Gastos Generales + Margen de Utilidad).
- Ctx: Se usa un multiplicador (factor de 2.5x a 3x) sobre el costo salarial base.
- Ex: Ingeniero de Redes Semi-Senior.
  - Data: Salario promedio ~$1,038,011 CLP mensual. Src: SRC-13.
  - Res: Tarifa cargada realista se sitúa en torno a los $16,000 CLP/hora.
Cpt: Experiencia como Modulador de Costo
- Data: Salario de Ing. Telecomunicaciones recién titulado ($956k - $1.6M) vs. 5+ años de exp ($1.3M - $2.3M). Src: SRC-11.
- Data: Ofertas laborales para perfiles con 3-5 años de exp. en $2.1M. Src: SRC-45.
Rec: Segmentar base de datos por nivel de experiencia (Junior, Semi-Senior, Senior) para presupuestación granular.

### 5.2. Tabla de Costos: Servicios Profesionales

ID: KB-GN-303-TABLE-SERVICES-01

|Rol Profesional|Nivel de Experiencia|Tarifa Referencia (CLP/hora)|Notas|Fuente|
|-|-|-|-|-|
|Ingeniero de Redes|Semi-Senior (2-5 años)|16.000|Ctx: Tarifa cargada para consultoría externa. Def: Profesional para configuración, implementación, soporte.|Src: SRC-11|
|Ingeniero de Redes|Senior (5+ años)|25.000|Ctx: Profesional para diseño de arquitecturas complejas, planificación estratégica, liderazgo técnico.|Src: SRC-11|
|Jefe de Proyecto|Senior (5+ años)|28.000|Ctx: Profesional con experiencia en gestión de proyectos de infraestructura. Resp: Plazos, costos, calidad, stakeholders.|Src: SRC-12|
|Técnico de Campo|Semi-Senior (2-5 años)|10.000|Ctx: Personal técnico para instalación y mantenimiento en terreno.|Src: SRC-60|

## 6. Consideraciones Estratégicas y Recomendaciones

ID: KB-GN-303-STRATEGY-01

### 6.1. Aplicación de Factores de Ajuste

ID: KB-GN-303-STRATEGY-ADJUSTMENTS-01

- Rec: Inflación y Variación de Precios
  - Instr: Ajustar costos de obras civiles con el IPMIC (CChC). Src: SRC-15.
  - Instr: Monitorear volatilidad del tipo de cambio CLP/USD para equipamiento importado.
- Rec: Economías de Escala
  - Instr: Para despliegues masivos (>10-15 unidades), aplicar factor de reducción de costos unitarios del 10% al 15%.
- Rec: Factor Geográfico Ñuble
  - Instr: Para proyectos en zonas de difícil acceso, aplicar contingencia presupuestaria del 15% al 20% sobre partidas de obras civiles y logística.

### 6.2. Estructura de Costos para Licitaciones Públicas

ID: KB-GN-303-STRATEGY-BIDDING-01

- Rec: Estructurar anexos económicos de licitaciones en consistencia con las categorías de este informe.
- Just: Facilita la comparación objetiva de ofertas y la evaluación de su razonabilidad económica. Src: SRC-01.
- Rec: Exigir en TDR un desglose claro de Costos de Operación y Mantenimiento (OPEX) proyectados a 5+ años, además del CAPEX.
- Just: Evaluar sostenibilidad financiera a largo plazo y Costo Total de Propiedad (TCO), un criterio fundamental del SNI.

### 6.3. Conclusión para el Agente IA

ID: KB-GN-303-STRATEGY-AGENT-INSTR-01
Purp: Proveer una base cuantitativa robusta para el agente IA "Asesor de Proyectos de Conectividad (SNI)".

- Instr: Presentar los datos como un punto de partida para formulación en etapa temprana (perfil/prefactibilidad). Warn: No sustituyen una cotización de mercado detallada.
- Instr: Guiar interactivamente al usuario en la aplicación de factores de ajuste por escala y geografía.
- Instr: Fomentar un enfoque de Costo Total de Propiedad (TCO), recordando considerar el OPEX.
- Instr: Mantener la trazabilidad de cada costo a su fuente y fecha, reforzando la verificabilidad y auditabilidad de las estimaciones.

## 7. Fuentes Citadas

ID: KB-GN-303-SOURCES-01

- SRC-01: Licitación - cableado fibra optica - Mercado Público
- SRC-03: INFORME NACIONAL - Subtel
- SRC-04: MEMORANDO DJ N - Cámara de Diputados
- SRC-05: OLT GPON con 4 Puertos GPON... - spdigital.cl
- SRC-06: XPON - Lk-Distribuidor...
- SRC-07: Lk-Distribuidor...
- SRC-08: Antena Microonda Para Enlaces | MercadoLibre
- SRC-09: UPS Respaldo eléctrico | Transworld
- SRC-11: Función y Sueldo - Ingenieros en telecomunicaciones - Tusalario.org
- SRC-12: Salarios de Jefe/a de proyecto en 2025 - Computrabajo
- SRC-13: Sueldos de ingeniero red... - Chiletrabajos
- SRC-15: Apoyo y Crecimiento para la Construcción en Chile - CChC
- SRC-16: El proyecto de Fibra Óptica Nacional... - factchecking.cl
- SRC-17: Chile resuelve licitación para instalar fibra óptica en la zona austral - El Mostrador
- SRC-18: 10g Gpon Olt Mini FTTH... - made-in-china.com
- SRC-19: Innovative Solutions for Efficient bbu rru... - Alibaba.com
- SRC-21: La plataforma de compras públicas... - Mercado Público
- SRC-24: Cable Fibra Óptica - Comdiel Ltda.
- SRC-27: GPON OLT 8PON ports... - AliExpress
- SRC-29: Licitación 5G en Chile... - dplnews.com
- SRC-31: Mapa de zonas afectadas por cortes de suministro - CGE
- SRC-33: PRECIOS DE SERVICIOS INFORMADOS - Enel Chile
- SRC-34: ¿Cuál es el costo de un empalme eléctrico completo? - habitissimo
- SRC-36: Generador Toyaki Diesel Trifasico 10KVA + ATS...
- SRC-41: ¿Cuánto se cobra por instalar paneles solares en Chile? - EnerLife
- SRC-42: Kit Solar Off Grid Fotovoltaico...
- SRC-43: ¿Cuánto Cuesta Instalar Paneles Fotovoltaicos? - Helius Solar
- SRC-45: Trabajo Ingeniero en Conectividad y Redes... - Duoclaboral.cl
- SRC-46: Zanjado - Hidra
- SRC-48: PRESUPUESTO - descargas.merida.es
- SRC-49: Ficha Licitación - Mercado Público
- SRC-50: ¿Cuánto cuesta instalar una torre? - Reddit
- SRC-51: Apu Instal Especiales - Scribd
- SRC-55: sistemas GPON - Compratecno
- SRC-57: Licitación - equipos de radioenlaces de microondas - Mercado Público
- SRC-60: Función y Sueldo - Técnicos de ingeniería de las telecomunicaciones - Tusalario.org
