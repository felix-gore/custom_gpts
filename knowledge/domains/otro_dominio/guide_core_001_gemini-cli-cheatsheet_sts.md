# Cheat Sheet para Gemini CLI

## Parte 1: Fundamentos y Configuración Inicial (El "Día Cero")

Esta primera parte es la más crucial. Una configuración robusta y bien pensada es la base sobre la que se construyen todos los flujos de trabajo avanzados. Invertir tiempo aquí te ahorrará incontables horas en el futuro. El objetivo es hacer que la interacción con `gemini-cli` sea rápida, fluida y potente.

---

### 1.1. Instalación y Actualización (`npm`)

`gemini-cli` es una aplicación de Node.js, por lo que se gestiona a través de `npm` (el gestor de paquetes de Node.js). La instalación se realiza de forma "global" para que puedas llamar al comando `gemini` desde cualquier directorio en tu sistema.

Para Instalar:
Abre tu terminal y ejecuta el siguiente comando. Esto descargará e instalará la última versión oficial de `gemini-cli`.

```bash
npm install -g @google/gemini-cli
```

Para Verificar la Instalación:
Una vez completado, verifica que se ha instalado correctamente pidiendo su versión.

```bash
gemini --version
```

Para Actualizar:
Los modelos y herramientas de IA evolucionan rápidamente. Es una buena práctica actualizar `gemini-cli` periódicamente para acceder a las últimas funcionalidades y correcciones. El comando es el mismo que el de instalación.

```bash
npm install -g @google/gemini-cli
```

---

### 1.2. Configuración Esencial del Entorno (`~/.zshrc`)

En lugar de escribir tus claves y preferencias en cada comando, las estableces como "variables de entorno". En macOS, el lugar estándar para esto es el archivo `~/.zshrc` (si usas Zsh, que es el shell por defecto) o `~/.bash_profile` (para shells Bash más antiguos).

¿Por qué es esencial?

* Seguridad: No expones tus claves secretas en el historial de tu shell.
* Eficiencia: Estableces valores por defecto (como el modelo a usar) una sola vez.

Comandos para Editar tu Configuración:

1. Abre el archivo de configuración en un editor de texto (usaremos `nano` por su simplicidad):

    ```bash
    nano ~/.zshrc
    ```

2. Añade las siguientes líneas al final del archivo.

    ```bash
    # --- Configuración para Gemini CLI ---

    # [OBLIGATORIO] Tu clave de API para los modelos de Gemini.
    # Consíguela en Google AI Studio. Trátala como una contraseña.
    export GEMINI_API_KEY="tu_clave_de_api_aqui"

    # [RECOMENDADO] Modelo de IA a usar por defecto.
    # Usa el más potente que tengas disponible para obtener los mejores resultados.
    # "gemini-1.5-pro-latest" es una excelente opción por su gran ventana de contexto y capacidades.
    export GEMINI_MODEL="gemini-1.5-pro-latest"
    ```

3. Guarda los cambios y cierra el editor (`Ctrl+O`, `Enter`, `Ctrl+X` en `nano`).
4. Aplica los cambios en tu sesión de terminal actual sin necesidad de reiniciarla:

    ```bash
    source ~/.zshrc
    ```

---

### 1.3. Personalización del Entorno (`settings.json` y Alias)

Aquí es donde pasas de tener una configuración funcional a una configuración personalizada y de alta velocidad.

#### Ajuste de Parámetros del Modelo (`settings.json`)

`gemini-cli` permite una configuración más granular a través de un archivo `settings.json`. Puedes tener uno global en `~/.gemini/` y/o uno por proyecto en `ruta/a/tu/proyecto/.gemini/` (la configuración del proyecto siempre sobreescribe la global).

El parámetro más útil para ajustar es la `temperature`, que controla la "creatividad" del modelo.

* `temperature: 0.0 - 0.2`: Modo Preciso. Para tareas que requieren respuestas deterministas y factuales: extracción de datos, formateo de código, respuestas basadas estrictamente en un texto.
* `temperature: 0.7 - 1.0`: Modo Creativo. Para brainstorming, redacción de borradores, generación de múltiples ideas, y tareas donde quieres respuestas más variadas y "sorprendentes".

Ejemplo de `settings.json` para un proyecto que requiere precisión:

1. Crea el directorio y el archivo en la raíz de tu proyecto:

    ```bash
    mkdir .gemini
    nano .gemini/settings.json
    ```

2. Añade el siguiente contenido:

    ```json
    {
      "generationConfig": {
        "temperature": 0.2
      }
    }
    ```

#### Creación de Alias de Productividad (en `~/.zshrc`)

Los alias son atajos para tus comandos más largos y repetitivos. Son el pilar de un flujo de trabajo rápido en la terminal.

Abre de nuevo `nano ~/.zshrc` y añade esta sección:

```bash
 --- Alias para potenciar Gemini CLI ---

 Atajo principal para llamar a gemini. Simple y rápido.
alias g="gemini"

 "Gemini-Clipboard": Chatea directamente con el contenido de tu portapapeles.
 Uso: Copias un texto y en la terminal escribes `gclip "resume este texto"`.
alias gclip="pbpaste | gemini -p"

 "Gemini-Commit": El generador de mensajes de commit definitivo.
 Uso: Haces `git add .` y luego ejecutas `gcommit`.
alias gcommit="git diff --staged | gemini -p 'Basado en este diff, escribe un mensaje de commit claro y profesional siguiendo la norma de Conventional Commits.'"

 "Gemini-File": Pasa el contenido de un archivo a Gemini de forma limpia.
 Es una función para poder pasar argumentos.
 Uso: gfile ./mi_script.js "Encuentra bugs en este código"
gfile() {
    cat "$1" | gemini -p "$2"
}
```

No olvides ejecutar `source ~/.zshrc` después de guardar para que tus nuevos superpoderes estén disponibles inmediatamente.

Con esta configuración inicial completada, tu entorno de terminal está ahora optimizado para interactuar con `gemini-cli` de la manera más eficiente posible.
¡Por supuesto! Continuemos con el desarrollo de la Super Cheat Sheet, construyendo sobre la base sólida que ya hemos establecido.

---

## Parte 2: El Arte del Prompting (Estrategias de Mando)

La calidad de tu interacción con Gemini no depende de la "magia", sino de la ingeniería de tus instrucciones. Un prompt bien diseñado es la diferencia entre una respuesta genérica y una solución precisa.

### 2.1. Principios Fundamentales para Resultados de Alta Calidad

1. Claridad y Especificidad: Sé directo, no ambiguo. El modelo no puede leer tu mente.
    * Mal: `Háblame de Git.`
    * Bien: `Explica la diferencia entre 'git fetch' y 'git pull' con una analogía para un desarrollador junior.`

2. Define un Rol (Persona): Obliga al modelo a adoptar una perspectiva y un estilo específicos.
    * `Actúa como un CTO revisando la arquitectura de un proyecto...`
    * `Eres un abogado experto en propiedad intelectual. Revisa esta cláusula...`
    * `Asume el rol de un copywriter creativo y genera 5 eslóganes para...`

3. Proporciona Ejemplos (Few-shot Prompting): Si quieres una salida con un formato específico, muéstrale exactamente cómo es.
    * `Traduce al inglés en formato 'español -> inglés': coche -> car, casa -> house, árbol ->`

4. Divide Tareas Complejas (Chain of Thought / Cadena de Pensamiento): Para problemas complejos, pide al modelo que "piense en voz alta" antes de dar la respuesta final.
    * `Analiza este código JavaScript. Primero, explica su propósito general. Segundo, identifica posibles optimizaciones de rendimiento. Tercero, escribe la versión optimizada del código.`

### 2.2. El Proceso de Iteración: Cómo Refinar tus Prompts

Rara vez el primer prompt es el perfecto. La maestría reside en la iteración rápida.

* Reformula tu Pregunta: Si el resultado no es el esperado, exprésalo de otra manera. "Crea un script" puede dar un resultado diferente a "Dame los comandos para...".
* Cambia el Orden del Contenido: El orden importa. A veces, poner los ejemplos al principio funciona mejor. Experimenta con la estructura: `[Instrucción][Contexto][Ejemplo]` vs. `[Contexto][Instrucción][Ejemplo]`.
* Ajusta la `temperature`: Usa tu archivo `settings.json` para controlar la creatividad vs. la precisión, como vimos en la Parte 1.

---

## Parte 3: `gemini-cli` - El Panel de Control Interactivo

Una vez dentro de una sesión de `gemini`, estos comandos son tu navaja suiza.

### 3.1. Comandos de Sesión (`/`)

| Comando | Descripción y Uso |
| :--- | :--- |
| `/help` o `/?` | Muestra todos los comandos. Úsalo si tienes dudas. |
| `/chat save <tag>` | Guarda la sesión actual (ej. `/chat save refactor-login`). |
| `/chat resume <tag>` | Carga una sesión guardada y continúa donde la dejaste. |
| `/chat list` | Muestra todas tus sesiones guardadas. |
| `/compress` | Resume la conversación actual. Ideal para conversaciones largas antes de cambiar de tema. |
| `/memory show` | Crucial para depurar. Muestra el contexto completo que `gemini` ha cargado desde los archivos `GEMINI.md`. |
| `/memory refresh` | Vuelve a cargar los archivos `GEMINI.md` sin reiniciar la sesión. |

### 3.2. Dominio del Contexto

| Método | Descripción y Cuándo Usarlo |
| :--- | :--- |
| Contexto de un solo uso (`@`) | Pasa el contenido de un archivo para una consulta específica. Perfecto para analizar, resumir o transformar archivos.<br>Ejemplo: `> Compara @contrato_v1.md y @contrato_v2.md` |
| Contexto Persistente (`GEMINI.md`) | Define la personalidad y reglas base del asistente. `gemini-cli` los carga jerárquicamente desde el directorio actual hacia arriba, siendo el local el más específico. |

---

## Parte 4: La Trinidad de la Productividad (`gemini-cli`, Terminal, Git)

### 4.1. Comandos Indispensables de la Terminal (macOS)

| Herramienta | Comando | Ejemplo de Uso con `gemini-cli` |
| :--- | :--- | :--- |
| Piping | `\|` | `git diff \| gemini -p "Resume estos cambios"` |
| Redirección | `>` y `>>` | `gemini -p "Escribe un script" > script.sh` |
| Portapapeles | `pbcopy` / `pbpaste` | `pbpaste \| gemini -p "Resume este texto que copié"` |
| Búsqueda | `find` / `grep` | `find . -name "*.js" \| xargs cat \| gemini -p "Analiza todo este código"` |
| Datos Estructurados | `jq` | `... \| gemini -p "Genera un JSON" \| jq '.data[0].name'` |

### 4.2. Integración Maestra con Git y GitHub

| Comando Git | Descripción | Cómo Potenciarlo con `gemini-cli` |
| :--- | :--- | :--- |
| `git diff` | Muestra diferencias. | `git diff HEAD~1 \| gemini -p "Explica los últimos cambios para un no-desarrollador."` |
| `git log` | Muestra el historial. | `git log --oneline -n 5 \| gemini -p "Resume el progreso del proyecto basado en estos 5 commits."` |
| `git commit` | Guarda un cambio. | Flujo Atómico: `gcommit` (usando el alias que creamos). |

---

## Parte 5: Técnicas de Orquestación Avanzada (Prompt Chaining)

### 5.1. Encadenamiento con Scripts (Variables `$()`)

Para flujos complejos donde necesitas "recordar" varios resultados.

* Patrón 1: Refinamiento Progresivo: `idea=$(gemini ...)` -> `esquema=$(gemini -p "$idea ...")` -> `gemini -p "$esquema ..."`
* Patrón 2: Análisis y Generación: `analisis=$(gemini ...)` -> `gemini -p "Basado en este análisis: $analisis, genera..."`
* Patrón 3: Crítica y Refinamiento: `borrador=$(gemini ...)` -> `critica=$(gemini -p "Critica este borrador: $borrador")` -> `gemini -p "Reescribe el borrador '$borrador' incorporando esta crítica: '$critica'"`

### 5.2. Encadenamiento con Tuberías (`|`)

Para flujos lineales y rápidos directamente en la consola.

* `gemini (idea) | gemini (esquema) | gemini (párrafo)`
* Recuerda: Cada comando solo ve la salida del inmediatamente anterior. No funciona para el patrón de Crítica y Refinamiento.

---

## Parte 6: Playbooks - Flujos de Trabajo Prácticos

### 6.1. Playbook: El Desarrollador de Software

* Ciclo de Feature: `gemini -p "Resume el Issue #123"` -> Escribe código con ayuda de `gemini` -> `gcommit` -> `git diff main | gemini -p "Redacta el PR"` -> `git push`.

### 6.2. Playbook: El Arquitecto de Asistentes GPT (Tu Flujo)

* Auditoría de Instrucciones: `gfile ./asistentes/gore_estratega/custom_gpt.md "Revisa este prompt. ¿Es ambiguo? Sugiere mejoras."`
* Gestión de KB: `gclip "Convierte este texto en un documento para mi KB con el ID kb_052..." > kb/kb_052...`

---

## Parte 7: Apéndice - Comandos Atómicos para Copiar y Pegar

| Objetivo | Comando de Una Línea (usando tus alias) |
| :--- | :--- |
| Generador de Mensajes de Commit | `git add . && gcommit` |
| Asistente de Resumen Instantáneo | `gclip "Resume este texto en 3 puntos clave"` |
| Documentador de Código | `gfile mi_funcion.js "Genera la documentación JSDoc para esta función"` |
| Auditor Rápido de Archivos | `gfile mi_script.py "Revisa este código y busca posibles bugs"` |
