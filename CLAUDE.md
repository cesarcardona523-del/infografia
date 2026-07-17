# infografia — Contexto del proyecto

Repositorio de infografías técnicas premium para LinkedIn (Arquitectura, Python, Power BI, etc.), organizado por tema. Tiene dos sistemas de trabajo, cada uno con su spec fija:

- [INFOGRAFIA-SPEC.md](INFOGRAFIA-SPEC.md) — brief de diseño visual (paleta, tipografía, composición, elementos prohibidos, branding, firma, tamaño 1200×627px). Define cómo se ve la infografía.
- [INFOGRAFIA-INVESTIGAR.md](INFOGRAFIA-INVESTIGAR.md) — prompt de análisis que convierte la imagen de referencia en el objeto de metadata (JSON) de la publicación. Define cómo se describe la infografía.

Ninguna de las dos se modifica al trabajar un tema puntual — son la fuente de verdad compartida por todos los temas. Si el usuario pide cambiar el diseño o el formato de metadata en sí, ese cambio va en el spec correspondiente, no en un archivo individual de un tema.

## Estructura de carpetas

```
referencias/<Tema>/<topico-slug>/   → imágenes de referencia de UNA infografía puntual (input): imagen principal + secundarias
<Tema>/                              → carpeta de salida en la raíz, mismo nombre que el tema (output, incremental)
publicaciones.json                   → catálogo único e incremental de metadata de TODAS las infografías, todos los temas
```

`<Tema>` es una categoría amplia (ej. `Arquitectura`, `Python`, `Power BI`), no un slug único por infografía — coincide con el valor `es.tema` del schema de metadata. Dentro de una misma carpeta de tema conviven, a lo largo del tiempo, varias infografías (distintos tópicos), cada una incremental respecto a las anteriores — nunca se sobreescribe el trabajo previo.

**Varias imágenes de referencia para una misma infografía** van juntas en `referencias/<Tema>/<topico-slug>/` (una imagen principal + secundarias, tal como lo permite la sección "Entrada" de INFOGRAFIA-SPEC.md). El subfolder por tópico es lo que evita ambigüedad cuando un mismo tema acumula referencias de varias infografías distintas con el tiempo.

**Si el usuario deja las imágenes sueltas** directamente en `referencias/<Tema>/` con un prefijo común (ej. `Arquitectura_AWS_1.jpg`, `Arquitectura_AWS_2.png`, `Arquitectura_AWS_3.gif`), en vez de preguntar, agruparlas automáticamente:
- Derivar el `<topico-slug>` del prefijo común, en kebab-case (`Arquitectura_AWS` → `arquitectura-aws`).
- Mover esos archivos a `referencias/<Tema>/<topico-slug>/`, conservando sus nombres originales, para dejar la carpeta organizada según la convención.
- Tratar el número más bajo (`_1`) como imagen principal y el resto como secundarias, salvo que el usuario indique otra cosa explícitamente.
- La extensión no importa para el agrupamiento (jpg/png/gif/webp... todas cuentan si comparten el prefijo).

## Flujo para crear una infografía nueva

El usuario da el tema y el `<topico-slug>`, y adjunta o lista una o varias imágenes de referencia. Si no da un topico-slug explícito, se deriva del tema/contexto de las imágenes. Opcionalmente puede indicar **Evento** y **Realizado por** (ver sección "Branding de evento" más abajo). A partir de ahí:

1. Crear (o reutilizar si ya existe) la carpeta `/<Tema>/` en la raíz.
2. Guardar todas las imágenes de referencia de esta infografía en `referencias/<Tema>/<topico-slug>/` (creando la carpeta si no existe) — todas juntas, sin mezclarlas con las de otro tópico del mismo tema.
3. Generar `/<Tema>/<topico-slug>.prompt.md`: el contenido completo de INFOGRAFIA-SPEC.md tal cual + una sección final `## Contexto específico — <Topico>` con la descripción del tema, el contenido técnico particular, y qué imágenes de referencia usar (cuál es la principal y cuáles las secundarias, si aplica). Si el usuario dio Evento y/o Realizado por, incluirlos en esta sección también.
   - **Siempre complementar, nunca solo replicar.** Si la referencia ya es una infografía o diagrama terminado, no pedir una copia idéntica: describir su estructura y pedir explícitamente enriquecerla (más detalle técnico, elementos relacionados que falten, mejor jerarquía), manteniendo siempre el sistema de diseño de INFOGRAFIA-SPEC.md.
4. Entregable final de la infografía, en `/<Tema>/`:
   - Si el usuario trae la imagen ya generada (vía herramienta externa de generación de imágenes), guardarla como `/<Tema>/<topico-slug>.png`.
   - Si no hay imagen externa, construir el HTML de la infografía ("infografía bonita") en `/<Tema>/<topico-slug>.html`, siguiendo el mismo sistema de diseño de INFOGRAFIA-SPEC.md (paleta, tipografía, composición, branding) con HTML/CSS puro, con el contenedor principal en una clase `.canvas` de tamaño fijo 1200×627px.
   - Antes de exportar, revisar la sección "Riqueza Visual" de INFOGRAFIA-SPEC.md: si hay datos comparables o tabulares, usar un gráfico o tabla real (no solo viñetas); usar iconos con propósito semántico; incluir al menos un elemento gráfico no textual; y un color de acento además del verde principal.
   - Exportar automáticamente ese HTML a `/<Tema>/<topico-slug>.png` (no hace falta pedírselo al usuario ni depender de una herramienta externa):
     1. Renderizar con Chrome headless a 2x escala, viewport `1264×691` (1200×627 + 32px de margen por lado, si el HTML mantiene ese padding de body): `"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless --disable-gpu --hide-scrollbars --force-device-scale-factor=2 --window-size=1264,691 --screenshot=raw.png file:///ruta/al/<topico-slug>.html`
     2. Recortar exactamente el `.canvas` con PIL: offset `(64,64)` (32px de margen × 2 de escala) y tamaño `(2400,1254)` — ajustar el offset si el padding del body del HTML cambia.
     3. Guardar el recorte como `/<Tema>/<topico-slug>.png`.
   - El HTML y el PNG conviven — el HTML es la fuente editable, el PNG es el asset final listo para publicar.
5. Ejecutar el prompt de INFOGRAFIA-INVESTIGAR.md sobre la(s) imagen(es) de referencia de este tópico, para generar el objeto de metadata, y agregarlo a `publicaciones.json` (ver reglas abajo).
6. Publicar en el sitio real (siempre, como último paso, sin que el usuario tenga que pedirlo cada vez):
   - Copiar `/<Tema>/<topico-slug>.png` a `/Users/caesar/Documents/GitHub/paginaweb/publications/`, con un nombre de archivo distintivo en `Title_Case_Con_Guion_Bajo` (ej. `Arquitectura_AWS_Big_Data_Pipeline.png`), sin sobreescribir archivos existentes de ese folder.
   - Agregar una entrada al final del arreglo `publicaciones` en `/Users/caesar/Documents/GitHub/paginaweb/publications/publicaciones.js` (variable global `window.PUBLICACIONES_DATA`, no un `.json` puro). Mismo objeto que en `publicaciones.json`, pero:
     - `imagen` siempre con el prefijo `publications/`, ej. `"publications/Arquitectura_AWS_Big_Data_Pipeline.png"`.
     - `fechaPublicacion` = fecha de la última entrada existente **en ese archivo** (no en `publicaciones.json`) + 2 días — son dos catálogos independientes, cada uno con su propia secuencia de fechas. Seguir el formato de offset que use la entrada más reciente de ese archivo (a la fecha de este documento: `-05:00`, no `Z`).
   - Validar el JS antes de darlo por terminado: extraer el objeto tras `window.PUBLICACIONES_DATA = ` y parsearlo como JSON para confirmar que sigue siendo válido.
   - Si ya existe una entrada de tema/tópico muy similar en `publicaciones.js` (mismo asunto, otra imagen), **no reemplazarla ni borrarla** — agregar la nueva de todas formas (regla explícita del usuario: siempre incremental) y avisar al usuario que ambas quedaron.

## Branding de evento (opcional)

El usuario puede indicar, junto con el tema/tópico/referencias, dos variables adicionales:

- **Evento** — nombre del evento para el que se crea la infografía (ej. `Datafest 2026`).
- **Realizado por** — organización o empresa que presenta/patrocina (ej. `Bancolombia`).

Si se especifican, aplican las reglas de la sección "Branding de Evento" de INFOGRAFIA-SPEC.md, además del branding personal habitual (no en su lugar):

1. Mostrar de forma visible en la infografía el nombre del evento y "Realizado por: `<Organización>`".
2. Buscar el logo oficial de esa organización (vía búsqueda web) para usarlo en vez de texto plano; si no se encuentra un logo confiable, usar solo el nombre en texto.
3. **Complementar el contenido investigando en internet** sobre el evento/la presentación/la organización, para enriquecer el tema técnico más allá de lo que muestra la imagen de referencia. Si la búsqueda no arroja suficiente información para entender bien de qué trataba, **preguntarle al usuario** en vez de inventar o asumir — el usuario asistió al evento y puede aclarar qué quiso decir el expositor.
4. **Colores**: buscar los colores de marca oficiales de la organización en "Realizado por" y usarlos como base de la paleta. Si no se encuentra información de marca confiable, decidir una paleta propia y arriesgada (dentro del criterio de la excepción de paleta de INFOGRAFIA-SPEC.md) — no hace falta preguntarle al usuario por esto en particular.
5. **`fechaPublicacion` siempre es la fecha/hora actual** (hoy), tanto en `publicaciones.json` como en `paginaweb/publications/publicaciones.js` — no sigue la regla de +2 días de la última entrada del catálogo, porque es contenido de coyuntura ligado a un evento puntual, no una publicación programada.
6. La firma personal (LinkedIn + `cacm523`) se mantiene sin cambios — el branding de evento convive con ella, no la reemplaza.

## Reglas del catálogo `publicaciones.json`

- Un único archivo JSON en la raíz: un arreglo `[ ... ]` de objetos, cada uno con exactamente el schema de INFOGRAFIA-INVESTIGAR.md (`id`, `imagen`, `fechaPublicacion`, `es{tema,topico,descripcion}`, `en{tema,topico,descripcion}`, `baseStats{views,likes,shares}`).
- `imagen` apunta al asset final publicable, ruta relativa a la raíz del repo: `<Tema>/<topico-slug>.png` (no al archivo de referencia de `referencias/`).
- Cada infografía nueva agrega un objeto **al final** del arreglo — nunca se reescribe ni se borra una entrada existente.
- `fechaPublicacion` de la entrada nueva = fecha de la última entrada existente en el arreglo + 2 días (ISO 8601). Si el catálogo está vacío, usar la fecha/hora actual. **Esta suma es siempre relativa a la última fecha ya guardada en el catálogo, nunca a la fecha real de hoy** — si la última entrada quedó con una fecha de hace un mes (porque el catálogo va "adelantado" respecto al calendario real), la siguiente sigue siendo esa fecha + 2 días, no la fecha de hoy + 2 días. Esta regla es para publicaciones normales; **las infografías de evento son la única excepción** y siempre usan la fecha/hora actual (ver "Branding de evento" arriba).
- Nunca debe haber más de dos entradas con la misma fecha en el catálogo completo — verificarlo antes de agregar (el espaciado de +2 días ya lo garantiza en el flujo normal).
- `baseStats` siempre inicia en `{ "views": 0, "likes": 0, "shares": 0 }` — nunca inventar valores.
- No agregar propiedades fuera del schema fijo.

## Reglas generales

- No modificar INFOGRAFIA-SPEC.md ni INFOGRAFIA-INVESTIGAR.md al trabajar un tema — son compartidos por todos los temas.
- No inventar contexto técnico, cifras ni métricas que no estén respaldadas por la imagen de referencia o por el usuario.
- Nombre de carpeta de tema consistente entre `referencias/<Tema>/`, `<Tema>/` y el valor `es.tema` usado en `publicaciones.json` para esa misma familia de infografías.
- Si falta el tema, el contexto, o no está claro el topico-slug, preguntar antes de crear carpetas o agregar al catálogo.
