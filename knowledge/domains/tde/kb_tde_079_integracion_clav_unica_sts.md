# Guía de Integración ClaveÚnica

ID: TDE-CU-GUIA-INTEGRACION-01
Version: 1.0.0
Status: Published
Human-Creator: STSador
Human-Editor: STSador
Model-Collaborator: IA-GEMINI
Creation-Date: 2025-07-06
Modification-Date: 2025-07-06
Primary-Source: kb_079_tde_integracion_clav_unica.md
Ref-STS-Guide: GUIDE-STS-MASTER-01

## 1. Contexto General

ID: TDE-CU-CTX-GENERAL-01
Purp: Guiar técnica y administrativamente la integración de ClaveÚnica en plataformas del Estado chileno.

### 1.1. Definición y Propósito

ID: TDE-CU-CTX-DEFINICION-01
Cpt: ClaveÚnica.

- Type: Proveedor de identidad digital (IdP).
- Func: Mecanismo de autenticación centralizado.
- Purp-Citizen: Acceso a múltiples servicios estatales con credencial única.
- Role: Base del Modelo de Identidad Digital de Chile.

### 1.2. Ámbito de Aplicación

ID: TDE-CU-CTX-AMBITO-01
Resp: Organismos de la Administración del Estado.
Cpt: Alcance.

- `- Scope: Plataformas y aplicaciones web y mobile.`
- `- Cost: Gratuito para instituciones del Estado.`
- `- Usage-Internal: Permitida para autenticación de funcionarios en sistemas internos.`
- `- Warn: El foco principal del mandato no es el uso interno.`

### 1.3. Política de Autenticación

ID: TDE-CU-CTX-POLITICA-01
Fnd: Instructivo Presidencial de Transformación Digital.
Req: ClaveÚnica debe ser el ÚNICO medio de autenticación para personas naturales en trámites estatales.
Act: Instituciones con sistemas preexistentes deben gestionar la migración a ClaveÚnica.

- `- Req: Establecer etapas y plazos para migración.`

## 2. Proceso de Integración End-to-End

ID: TDE-CU-PROC-OVERVIEW-01

### 2.1. Fases del Proceso

ID: TDE-CU-PROC-FASES-01
Proc:

- `1. Solicitud de Credenciales.`
- `2. Desarrollo de la Integración.`
- `3. Certificación.`
- `4. Activación.`

### 2.2. Tiempos Estimados

ID: TDE-CU-PROC-TIEMPOS-01

- `Dln: ~3 días hábiles. Ctx: Revisión de solicitud de credenciales.`
- `Dln: ~6 días hábiles. Ctx: Certificación.`
- `Dln: ~3 días hábiles. Ctx: Actualización de URIs.`

## 3. Detalle Técnico de Implementación

ID: TDE-CU-TEC-IMPLEMENTACION-01

### 3.1. Protocolo y Flujo

ID: TDE-CU-TEC-PROTOCOLO-01

- `Fnd: OpenID Connect (sobre OAuth 2.0).`
- `Mech: Authorization Code Flow.`

### 3.2. Tipos de Credenciales

ID: TDE-CU-TEC-CREDENCIALES-01
Def: Cada solicitud aceptada recibe un archivo ZIP.

- `Cpt: Contenido.`
- `- Def: 3 pares de credenciales (client_id, client_secret).`
- `- Cpt: Ambiente-Sandbox. Purp: Pruebas con RUN de test.`
- `- Cpt: Ambiente-QA. Purp: Idéntico a Sandbox.`
- `- Cpt: Ambiente-Produccion. Purp: Uso con ciudadanos reales.`
- `- Warn: Credenciales de producción deshabilitadas hasta completar certificación. Ref: TDE-CU-ADM-SOL-CERTIFICACION-01.`
- `Cpt: Contraseña-ZIP.`
- `- Def: Incluida en el correo de aceptación. Ref: TDE-CU-ADM-SOL-GESTION-01.`

### 3.3. Pasos del Flujo de Autenticación

ID: TDE-CU-TEC-FLUJO-PASOS-01

#### 3.3.1. Generar Token Anti-CSRF

ID: TDE-CU-TEC-FLUJO-P1-CSRF-01
Act: Crear un token de sesión único (`state`).
Purp: Prevenir ataques CSRF; mantener estado entre ciudadano y aplicación.

#### 3.3.2. Solicitud de Autorización

ID: TDE-CU-TEC-FLUJO-P2-AUTH-GET-01
Act: Redirigir al usuario al endpoint de autorización.

- `Mdl: Metodo. Def: GET.`
- `Mdl: URL-Base. Def: https://accounts.claveunica.gob.cl/openid/authorize/`
- `Req: Uso exclusivo de HTTPS en producción.`
- `Cpt: Query-Params.`
- `- Param: client_id. Def: Tu client_id.`
- `- Param: response_type. Def: code.`
- `- Param: scope. Def: "openid run name".`
- `- Param: redirect_uri. Def: Tu redirect_uri registrada.`
- `- Param: state. Def: Token CSRF. Ref: TDE-CU-TEC-FLUJO-P1-CSRF-01.`

#### 3.3.3. Confirmar Token de Estado

ID: TDE-CU-TEC-FLUJO-P3-STATE-VERIFY-01
Act: Corroborar que el parámetro `state` recibido en `redirect_uri` coincide con el token CSRF original.
Purp: Confirmar que la respuesta no es forjada.

#### 3.3.4. Canjear Código por Token de Acceso

ID: TDE-CU-TEC-FLUJO-P4-TOKEN-POST-01
Act: Intercambiar el `code` de autorización por un `access_token`.
Req: La llamada debe realizarse desde el backend, nunca desde el cliente.

- `Mdl: Metodo. Def: POST.`
- `Mdl: Endpoint. Def: https://accounts.claveunica.gob.cl/openid/token/`
- `Cpt: Header.`
- `- Header: ContentType. Def: application/x-www-form-urlencoded; charset=UTF-8.`
- `Cpt: Body.`
- `- Param: client_id. Def: Tu client_id.`
- `- Param: client_secret. Def: Tu client_secret.`
- `- Param: redirect_uri. Def: Tu redirect_uri.`
- `- Param: grant_type. Def: authorization_code.`
- `- Param: code. Def: Código de autorización recibido.`
- `- Param: state. Def: Token CSRF original.`

#### 3.3.5. Autenticar Usuario con id_token

ID: TDE-CU-TEC-FLUJO-P5-ID-TOKEN-01
Src: Respuesta del endpoint `token/`. Ref: TDE-CU-TEC-FLUJO-P4-TOKEN-POST-01.
Cpt: Contenido.

- `- Def: JSON con access_token, token_type, expires_in, id_token.`
Act: Decodificar y validar el `id_token` (JWT) para autenticar al usuario.

#### 3.3.6. Obtener Información del Ciudadano

ID: TDE-CU-TEC-FLUJO-P6-USERINFO-POST-01
Act: Obtener datos del usuario (nombre, RUN).
Req: La llamada debe realizarse desde el backend.

- `Mdl: Metodo. Def: POST.`
- `Mdl: Endpoint. Def: https://accounts.claveunica.gob.cl/openid/userinfo/`
- `Cpt: Header.`
- `- Header: Authorization. Def: Bearer ACCESS_TOKEN.`
- `Cpt: Respuesta-Ejemplo.`
- `- Key: sub. Def: Identificador único del usuario.`
- `- Key: RolUnico. Def: Objeto con DV, numero (RUN sin DV), tipo (RUN).`
- `- Key: name. Def: Array con nombres.`
- `- Key: apellidos. Def: Array con apellidos.`

#### 3.3.7. Cierre de Sesión

ID: TDE-CU-TEC-FLUJO-P7-LOGOUT-01
Purp: Invalidar la sesión en el IdP de ClaveÚnica.
Mech:

- `- Cpt: Metodo-1-Redirect. Instr: Llamar vía GET a https://accounts.claveunica.gob.cl/api/v1/accounts/app/logout?redirect=LOGOUT_URI.`
- `- Cpt: Metodo-2-JS. Instr: Usar window.location.href para redirigir a .../logout y luego a LOGOUT_URI con setTimeout.`

## 4. Detalle Administrativo: Solicitudes

ID: TDE-CU-ADM-SOLICITUDES-01

### 4.1. Solicitud de Credenciales de Integración

ID: TDE-CU-ADM-SOL-CREDENCIALES-01
Mech: Portal claveunica.gob.cl -> sección Instituciones.
Proc:

- `1. Enviar solicitud.`
- `2. Autenticar con ClaveÚnica.`
- `3. Iniciar trámite "Solicitud Credenciales de Integración a ClaveÚnica".`
Warn: Trámite exclusivo para Instituciones Públicas.

### 4.2. Formulario de Solicitud de Credenciales

ID: TDE-CU-ADM-FORM-CREDENCIALES-01
Cpt: A continuación se detalla la estructura del formulario de solicitud, usando el estándar SFD.

BEGIN_EMBEDDED_BLOCK:: GUIDE-SFD-STS-MASTER-01 FORM-CU-SOL-CREDENCIALES-01

# Formulario: Solicitud Credenciales de Integración a ClaveÚnica

ID: FORM-CU-SOL-CREDENCIALES-01
Version: 1.0.0
Status: Published
Ref-SFD-Guide: GUIDE-SFD-STS-MASTER-01

### Sección 1: Datos de la Institución y Contactos

ID: FORM-CU-S1-CONTACTO-01

#### Institución

ID: FORM-CU-S1-INSTITUCION-01
Field-Label: "Nombre de la institución pública"
Field-Type: Text
Field-Constraint: "Req: mandatory."

#### Contacto Administrativo

ID: FORM-CU-S1-CONTACTOADM-01
Field-Label: "Funcionario responsable"
Field-Type: Text
Field-Constraint: "Req: mandatory."
Field-Instr: "Debe ser un correo institucional."

#### Contacto Técnico

ID: FORM-CU-S1-CONTACTOTEC-01
Field-Label: "Contraparte técnica"
Field-Type: Text
Field-Constraint: "Req: optional."
Field-Instr: "Puede ser el mismo que el Contacto Administrativo."

### Sección 2: Datos de la Aplicación

ID: FORM-CU-S2-APLICACION-01

#### Nombre de la Aplicación

ID: FORM-CU-S2-NOMBREAPP-01
Field-Label: "Nombre de la aplicación"
Field-Type: Text
Field-Constraint: "Req: mandatory."
Field-Instr: "Debe ser un identificador claro de institución y plataforma."

#### Descripción de la Aplicación

ID: FORM-CU-S2-DESCAPP-01
Field-Label: "Descripción de la aplicación"
Field-Type: TextArea
Field-Constraint: "Req: mandatory."
Field-Instr: "Indicar el propósito de la integración."

#### Público Objetivo

ID: FORM-CU-S2-PUBLICO-01
Field-Label: "Público Objetivo"
Field-Type: Radio
Field-Constraint: "Req: mandatory."

- Field-Option: "Público (ciudadanía)"
- Field-Option: "Interno (institución)"

#### URL de la Aplicación

ID: FORM-CU-S2-URLAPP-01
Field-Label: "URL de la aplicación"
Field-Type: Text
Field-Constraint: "Req: mandatory. Format: url."
Field-Instr: "El dominio debe ser .gob.cl según norma técnica."

#### Redirect URIs

ID: FORM-CU-S2-REDIRECTURI-01
Field-Label: "Redirect URIs"
Field-Type: TextArea
Field-Constraint: "Req: mandatory. Format: url."
Field-Instr: "URLs de callback para testing, QA y producción. Sin query ni fragmento. Dominio .gob.cl requerido en producción."

#### Logout URIs

ID: FORM-CU-S2-LOGOUTURI-01
Field-Label: "Logout URIs"
Field-Type: TextArea
Field-Constraint: "Req: optional. Format: url."
Field-Instr: "URLs de redirección post-logout. Múltiples URIs deben ser separadas por comas."

#### Términos y Condiciones

ID: FORM-CU-S2-TERMINOS-01
Field-Label: "Aceptación de Términos y Condiciones"
Field-Type: Checkbox
Field-Constraint: "Req: mandatory."
END_EMBEDDED_BLOCK:: FORM-CU-SOL-CREDENCIALES-01

### 4.3. Gestión de la Solicitud de Credenciales

ID: TDE-CU-ADM-SOL-GESTION-01
Cpt: Notificación de Recepción.

- `Src: no-reply@digital.gob.cl.`
- `Rec: Añadir a lista segura.`
Cpt: Notificación de Respuesta.
- `Type: Aceptación o Rechazo.`
- `Cpt: Contenido-Aceptacion. Def: Email con 'Número de solicitud' y archivo ZIP adjunto. Ref: TDE-CU-TEC-CREDENCIALES-01.`
- `Cpt: Contenido-Rechazo. Def: Email con motivo del rechazo.`
Cpt: Seguimiento.
- `Mech: Mesa de Ayuda en digital.gob.cl/mesadeayuda.`

### 4.4. Solicitud de Certificación y Activación

ID: TDE-CU-ADM-SOL-CERTIFICACION-01
Mech: Portal Cerofilas.
Cpt: Trámite.

- `Name: Solicitud de Certificación / Activación de Credenciales de Producción.`
- `Cpt: Inputs.`
- `- Input: client_id. Def: client_id del ambiente de producción.`
- `- Input: MetodoRevision. Def: 'URL pública' o 'Videoconferencia'.`
- `- Input: Evidencia. Def: Capturas de configuración de endpoints y variables de entorno.`
- `- Input: InfoAdicional. Def: Opcional.`

### 4.5. Requisitos de Certificación

ID: TDE-CU-ADM-REQ-CERTIFICACION-01
Req:

- `- Uso del botón oficial de ClaveÚnica.`
- `- Uso de HTTPS en ambiente de producción.`
- `- Prohibido uso de IFRAME o popups para el formulario (req: pantalla completa).`
- `- Parámetro 'state' debe ser generado dinámicamente. Ref: TDE-CU-TEC-FLUJO-P1-CSRF-01.`
- `- Scope debe ser "openid run name".`
- `- Llamadas a 'token/' y 'userinfo/' deben originarse desde el backend. Ref: TDE-CU-TEC-FLUJO-P4-TOKEN-POST-01, TDE-CU-TEC-FLUJO-P6-USERINFO-POST-01.`
- `- 'client_id' y 'client_secret' deben estar en variables de entorno (prohib: hardcodeo).`
- `- Implementación funcional del cierre de sesión. Ref: TDE-CU-TEC-FLUJO-P7-LOGOUT-01.`

### 4.6. Solicitud de Actualización de Datos

ID: TDE-CU-ADM-SOL-ACTUALIZACION-01
Cpt: Caso de Uso.

- `Def: Modificar 'Redirect URI' u otro dato de la integración.`
Mech: Portal Cerofilas.
Cpt: Trámite.
- `Name: “Actualización de URIs de Credenciales de Integración ClaveÚnica”.`

## 5. Recursos y Soporte

ID: TDE-CU-REC-SOPORTE-01

### 5.1. Ejemplos de Implementación

ID: TDE-CU-REC-EJEMPLOS-01
Src:

- `- Cpt: Código Fuente. Def: Ejemplos en Python, PHP, .NET, Java.`
- `- Cpt: Testing. Def: Colección de Postman.`
- `- Cpt: Frontend. Def: HTML/CSS del botón oficial.`
- `- Cpt: CURL-Token. Ex: curl -i https://accounts.claveunica.gob.cl/openid/token/ -H "content-type: application/x-www-form-urlencoded; charset=UTF-8" --data "client_id=...&..."`
- `- Cpt: CURL-UserInfo. Ex: curl -i https://accounts.claveunica.gob.cl/openid/userinfo/ -X POST -H "authorization: Bearer ACCESS_TOKEN"`

### 5.2. Canales de Comunicación

ID: TDE-CU-REC-CANALES-01
Mech:

- `- Canal-1: Mesa de Servicio institucional SGD.`
- `- Canal-2: Correo claveunica@digital.gob.cl.`
Req: Tickets deben crearse con cuenta institucional.

### 5.3. Capacitaciones

ID: TDE-CU-REC-CAPACITACION-01
Act: Inscripción vía portal Cerofilas.
Cpt: Trámite.

- `Name: ‘Inscripción a capacitaciones de productos de Gobierno Digital’.`
