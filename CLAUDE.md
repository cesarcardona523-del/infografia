# infografia — Contexto del proyecto

Repositorio de infografías técnicas premium para LinkedIn (Arquitectura, Python, Power BI, etc.), organizado por tema. Tiene dos sistemas de trabajo, cada uno con su spec fija:

- [INFOGRAFIA-SPEC.md](INFOGRAFIA-SPEC.md) — brief de diseño visual (paleta, tipografía, composición, elementos prohibidos, branding, firma, tamaño 1200×627px). Define cómo se ve la infografía.
- [INFOGRAFIA-INVESTIGAR.md](INFOGRAFIA-INVESTIGAR.md) — prompt de análisis que convierte la imagen de referencia en el objeto de metadata (JSON) de la publicación. Define cómo se describe la infografía.

Ninguna de las dos se modifica **con contenido específico de un tema puntual** — ese contenido vive en el `prompt.md` de cada tema, no aquí. INFOGRAFIA-SPEC.md sí puede evolucionar como design system vivo (ver "Rol permanente y mejora continua" abajo): cuando una mejora de diseño generaliza a todas las infografías, se incorpora directamente al spec, no solo a pedido explícito del usuario.

## Rol permanente y mejora continua

Además del flujo puntual de cada infografía, se asume permanentemente el rol de Lead Product Designer, UX Engineer, Frontend Architect y Data Visualization Specialist para este repositorio. Aplica a todo el código existente y a cualquier infografía futura, no solo a la solicitud del momento.

**Qué no cambia:** el proyecto produce piezas estáticas de 1200×627px (HTML → PNG), una por infografía, sin runtime compartido entre piezas — cada HTML es autocontenido para poder renderizarse aislado con Chrome headless. Por eso no aplican patrones de producto web con estado (navbar, sidebar, dashboard interactivo, modales, tabs, accordions, dark-mode toggle): no hay dónde vivirían. Tampoco hay selección automática de modelo Claude por tarea — eso lo controla la interfaz/usuario, no algo que se pueda decidir desde el código.

- **Mejora continua**: al modificar un archivo, evaluar oportunidades objetivas de mejorar jerarquía visual, espaciado, composición, alineación, consistencia, contraste, legibilidad y organización del CSS/HTML dentro de ese mismo HTML, y aplicarlas directamente sin romper INFOGRAFIA-SPEC.md ni la pieza.
- **Revisión antes de construir, mejora incremental de piezas existentes**: antes de trabajar una infografía nueva en un `<Tema>`, revisar **todas** las piezas ya construidas de ese mismo tema (no hace falta auditar los demás temas en esa misma tarea). Para cada una:
  - Si tiene una mejora objetiva real (diseño, legibilidad, jerarquía visual, iconografía, composición, accesibilidad, calidad gráfica o consistencia con INFOGRAFIA-SPEC.md), regenerarla: mismo nombre de archivo, reemplazar el PNG anterior (en `Construidos/<Tema>/` y, si ya estaba copiado, en `paginaweb/publications/`), sin dejar duplicados ni temporales, y actualizar cualquier referencia necesaria para que el proyecto siga funcionando sin pasos adicionales.
  - Si su calidad ya es consistente con el estándar actual del proyecto, **no tocarla** — evita gastar tiempo/tokens regenerando piezas que no ganan nada.
  - Esto puede incluir piezas ya publicadas — la regla de "nunca sobreescribir" del catálogo aplica solo a las **entradas de metadata** de `publicaciones.json`/`publicaciones.js` (nunca tocar `fechaPublicacion`, `id` ni el orden del arreglo al regenerar una imagen), no a los assets de imagen en sí.
  - Si una mejora detectada generaliza claramente a otros temas, propagarla la próxima vez que se trabaje en ellos (no hace falta salir a tocar los 17 temas de una vez).
- **Patrones reutilizables**: como no hay stylesheet compartido en runtime, la reutilización se logra manteniendo consistentes los patrones de CSS entre piezas (tarjetas, KPI tiles, badges, tablas, timeline, gráficos) documentados en la sección "Riqueza Visual" de INFOGRAFIA-SPEC.md — partir de esos patrones ya validados en vez de reinventar cada card/badge/tabla desde cero.
- **Visualización de datos**: para cualquier gráfico dentro de una infografía, aplicar las recomendaciones del skill `dataviz` (claridad, jerarquía, escalas, color, etiquetas) antes de exportar.
- **Estilo visual**: la base es el lenguaje ya definido en INFOGRAFIA-SPEC.md (paleta verde + acento tierra, referencias tipo Microsoft Learn/Azure Architecture Center/Databricks). Se admite glassmorphism moderado en tarjetas/paneles y layouts tipo Bento Grid como una opción más de composición, siempre sin contradecir esas reglas. No se adopta dark-mode (no aplica a una imagen exportada una sola vez) ni paletas tipo Apple/Vercel/Linear/Stripe/OpenAI por defecto — son referencias de producto web, no del brief editorial ya validado.
- **Calidad de código**: al modificar un HTML, eliminar CSS/JS muerto o no usado en el render final y evitar duplicación dentro del mismo archivo.
- **Flujo de commit/documentación rutinario, sin pedir autorización cada vez**: comitear cambios, actualizar el `README.md` de ambos repositorios (incluida su sección de estadísticas vía `git log`/`git shortlog`), y validar que `publicaciones.js` siga siendo JSON válido son tareas rutinarias de mantenimiento — no requieren confirmación previa. Sí requieren confirmación explícita: cambios destructivos (borrar/sobreescribir catálogo, eliminar infografías o referencias), `git push`, o cambios importantes de arquitectura del proyecto.

## Estructura de carpetas

```
referencias/<Tema>/<topico-slug>/   → imágenes de referencia de UNA infografía puntual (input): imagen principal + secundarias
Construidos/<Tema>/                 → carpeta de salida, mismo nombre que el tema (output, incremental) — TODO lo construido vive aquí, nunca en la raíz
publicaciones.json                   → catálogo único e incremental de metadata de TODAS las infografías, todos los temas
```

**Toda infografía ya construida (HTML, PNG, prompt.md) vive dentro de `Construidos/<Tema>/`, nunca directamente en la raíz del repositorio.** Esta es una convención fija del proyecto — no crear carpetas de tema sueltas en la raíz.

`<Tema>` es una categoría amplia (ej. `Arquitectura`, `Python`, `Power BI`), no un slug único por infografía — coincide con el valor `es.tema` del schema de metadata. Dentro de una misma carpeta de tema conviven, a lo largo del tiempo, varias infografías (distintos tópicos), cada una incremental respecto a las anteriores — nunca se sobreescribe el trabajo previo.

**Varias referencias para una misma infografía** van juntas en `referencias/<Tema>/<topico-slug>/` (una referencia principal + secundarias, tal como lo permite la sección "Entrada" de INFOGRAFIA-SPEC.md). El subfolder por tópico es lo que evita ambigüedad cuando un mismo tema acumula referencias de varias infografías distintas con el tiempo.

**Las referencias no siempre son imágenes.** El usuario puede adjuntar PDF, presentaciones (PPTX) o documentos de Word (DOCX) en vez de (o junto a) imágenes — ej. el material de una charla o un informe técnico. En ese caso, guardar el archivo tal cual en `referencias/<Tema>/<topico-slug>/` igual que una imagen, pero antes de escribir el `.prompt.md` hay que **analizar su contenido real** (extraer texto/diapositivas/tablas con las herramientas de lectura de PDF/PPTX/DOCX disponibles) — nunca asumir de qué trataba solo por el nombre del archivo. Ver la sección "Entrada" de INFOGRAFIA-SPEC.md para el detalle de este análisis.

**Si el usuario deja las imágenes sueltas** directamente en `referencias/<Tema>/` con un prefijo común (ej. `Arquitectura_AWS_1.jpg`, `Arquitectura_AWS_2.png`, `Arquitectura_AWS_3.gif`), en vez de preguntar, agruparlas automáticamente:
- Derivar el `<topico-slug>` del prefijo común, en kebab-case (`Arquitectura_AWS` → `arquitectura-aws`).
- Mover esos archivos a `referencias/<Tema>/<topico-slug>/`, conservando sus nombres originales, para dejar la carpeta organizada según la convención.
- Tratar el número más bajo (`_1`) como imagen principal y el resto como secundarias, salvo que el usuario indique otra cosa explícitamente.
- La extensión no importa para el agrupamiento (jpg/png/gif/webp... todas cuentan si comparten el prefijo).

**`Construidos/<Tema>/Archivadas/`** guarda versiones anteriores de una infografía que fue consolidada/actualizada en el mismo lugar (ver "Gestión inteligente de publicaciones e infografías" abajo) — nunca se borra una versión previa, se archiva.

## Gestión inteligente de publicaciones e infografías (consolidación)

Antes de arrancar el flujo de creación de abajo, si llega información nueva (un documento, una investigación, una noticia, un artículo, una explicación), analizar `publicaciones.json` (que `paginaweb/publications/publicaciones.js` siempre debe reflejar) para decidir si esa información amplía, corrige, actualiza o complementa una publicación ya existente, o si es un tema genuinamente nuevo.

**Criterio de coincidencia — conservador.** Comparar por tema, tópico, conceptos principales y palabras clave, no solo por título literal. Pero solo se considera "la misma publicación" cuando es el mismo tópico exacto: una corrección, una ampliación directa del mismo asunto, datos actualizados del mismo tema, o el mismo contenido retocado. Ante la duda de si son temas relacionados pero distintos, **crear una publicación nueva**, no fusionar — evita perder cobertura de temas por sobre-consolidar.

Esta regla reemplaza la anterior de "nunca reemplazar una entrada similar, siempre agregar una nueva" — la preservación de historial ahora se logra archivando los archivos (paso 1 abajo), no duplicando entradas de catálogo.

**Si es la misma publicación → actualizar en el mismo lugar, nunca crear una entrada nueva:**

1. **Archivar la versión anterior antes de tocar nada.** Mover `Construidos/<Tema>/<topico-slug>.html`, `.png` y `.prompt.md` a `Construidos/<Tema>/Archivadas/<topico-slug>-<fecha-de-hoy>/` (fecha ISO corta, ej. `2026-07-19`, para no perder historial si se archiva más de una vez). Si la imagen ya estaba copiada en `paginaweb/publications/`, archivar también esa copia en `paginaweb/publications/Archivadas/` con el mismo sufijo de fecha antes de reemplazarla.
2. **Contenido**: complementar sin perder información válida ya construida; integrar solo lo nuevo relevante; eliminar redundancia; reorganizar para mejorar claridad; enriquecer la explicación cuando aporte. Nunca inventar cifras o contexto no respaldado.
3. **Traducciones sincronizadas**: si se actualiza `es`, actualizar `en` en la misma pasada, con el mismo significado técnico y nivel de detalle.
4. **Regenerar la infografía**: mismo estilo del proyecto (INFOGRAFIA-SPEC.md), mismo nombre de archivo cuando sea posible, reemplazando el asset activo en `Construidos/<Tema>/` y en `paginaweb/publications/` si ya existía ahí. Si el motivo de la regeneración es un aporte real de contenido (la misma condición del punto 6, no una corrección menor), agregar la insignia `Actualizada` en la parte superior de la pieza — ver "Insignia de Actualización" en INFOGRAFIA-SPEC.md.
5. **Catálogo — editar in-place en ambos archivos** (`publicaciones.json` y `paginaweb/publications/publicaciones.js`): mismo `id`, misma ruta de imagen, misma posición en el arreglo. Nunca tocar `baseStats`.
6. **`fechaPublicacion`**: actualizar a la fecha/hora actual **solo si hay aporte real de contenido** (amplía, corrige, actualiza datos, agrega ejemplos o buenas prácticas, mejora la explicación) — mismo tratamiento que una infografía de evento (fecha/hora actual, no la regla de +2 días). No tocar la fecha ante correcciones menores: ortografía, formato, CSS, estilo, redacción menor. Verificar después que no queden más de dos entradas con esa misma fecha en el catálogo.
7. Si el aporte nuevo trae material de referencia propio (documento, PDF, artículo, captura), guardarlo como referencia secundaria adicional en `referencias/<Tema>/<topico-slug>/` — no crear un subfolder de tópico nuevo.

**Si es un tema genuinamente distinto** que no puede integrarse razonablemente en ninguna publicación existente: seguir el flujo normal de creación de abajo.

## Flujo para crear una infografía nueva

El usuario da el tema y el `<topico-slug>`, y adjunta o lista una o varias imágenes de referencia. Si no da un topico-slug explícito, se deriva del tema/contexto de las imágenes. Opcionalmente puede indicar **Evento** y **Realizado por** (ver sección "Branding de evento" más abajo). A partir de ahí:

1. Crear (o reutilizar si ya existe) la carpeta `Construidos/<Tema>/`.
2. Guardar todas las imágenes de referencia de esta infografía en `referencias/<Tema>/<topico-slug>/` (creando la carpeta si no existe) — todas juntas, sin mezclarlas con las de otro tópico del mismo tema.
3. Generar `Construidos/<Tema>/<topico-slug>.prompt.md`: el contenido completo de INFOGRAFIA-SPEC.md tal cual + una sección final `## Contexto específico — <Topico>` con la descripción del tema, el contenido técnico particular, y qué imágenes de referencia usar (cuál es la principal y cuáles las secundarias, si aplica). Si el usuario dio Evento y/o Realizado por, incluirlos en esta sección también.
   - **Siempre complementar, nunca solo replicar.** Si la referencia ya es una infografía o diagrama terminado, no pedir una copia idéntica: describir su estructura y pedir explícitamente enriquecerla (más detalle técnico, elementos relacionados que falten, mejor jerarquía), manteniendo siempre el sistema de diseño de INFOGRAFIA-SPEC.md.
   - **Diseño arriesgado, no plantillado.** Cada infografía nueva debe tomar al menos una decisión de composición o metáfora visual distinta a las ya usadas en el mismo tema — evitar reciclar la misma estructura de grid/columnas de la pieza anterior. Preferir metáforas visuales concretas ligadas al contenido (pirámides de dependencia, icebergs, caminos en zigzag, básculas, etc.) sobre el genérico "grid de tarjetas" cuando el contenido lo permita.
4. Entregable final de la infografía, en `Construidos/<Tema>/`:
   - Si el usuario trae la imagen ya generada (vía herramienta externa de generación de imágenes), guardarla como `Construidos/<Tema>/<topico-slug>.png`.
   - Si no hay imagen externa, construir el HTML de la infografía ("infografía bonita") en `Construidos/<Tema>/<topico-slug>.html`, siguiendo el mismo sistema de diseño de INFOGRAFIA-SPEC.md (paleta, tipografía, composición, branding) con HTML/CSS puro, con el contenedor principal en una clase `.canvas` de tamaño fijo 1200×627px.
   - Antes de exportar, revisar la sección "Riqueza Visual" de INFOGRAFIA-SPEC.md: si hay datos comparables o tabulares, usar un gráfico o tabla real (no solo viñetas); usar iconos con propósito semántico; incluir al menos un elemento gráfico no textual; y un color de acento además del verde principal.
   - Exportar automáticamente ese HTML a `Construidos/<Tema>/<topico-slug>.png` (no hace falta pedírselo al usuario ni depender de una herramienta externa):
     1. Renderizar con Chrome headless a 2x escala, viewport `1264×691` (1200×627 + 32px de margen por lado, si el HTML mantiene ese padding de body): `"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless --disable-gpu --hide-scrollbars --force-device-scale-factor=2 --window-size=1264,691 --screenshot=raw.png file:///ruta/al/<topico-slug>.html`
     2. Recortar exactamente el `.canvas` con PIL: offset `(64,64)` (32px de margen × 2 de escala) y tamaño `(2400,1254)` — ajustar el offset si el padding del body del HTML cambia.
     3. Guardar el recorte como `Construidos/<Tema>/<topico-slug>.png`.
   - El HTML y el PNG conviven — el HTML es la fuente editable, el PNG es el asset final listo para publicar.
5. Ejecutar el prompt de INFOGRAFIA-INVESTIGAR.md sobre la(s) imagen(es) de referencia de este tópico, para generar el objeto de metadata, y agregarlo a `publicaciones.json` (ver reglas abajo).
6. Publicar en el sitio real (siempre, como último paso, sin que el usuario tenga que pedirlo cada vez):
   - Copiar `Construidos/<Tema>/<topico-slug>.png` a `/Users/caesar/Documents/GitHub/paginaweb/publications/`, con un nombre de archivo distintivo en `Title_Case_Con_Guion_Bajo` (ej. `Arquitectura_AWS_Big_Data_Pipeline.png`), sin sobreescribir archivos existentes de ese folder.
   - Agregar una entrada al final del arreglo `publicaciones` en `/Users/caesar/Documents/GitHub/paginaweb/publications/publicaciones.js` (variable global `window.PUBLICACIONES_DATA`, no un `.json` puro). Mismo objeto que en `publicaciones.json`, pero:
     - `imagen` siempre con el prefijo `publications/`, ej. `"publications/Arquitectura_AWS_Big_Data_Pipeline.png"`.
     - `fechaPublicacion` = fecha de la última entrada existente **en ese archivo** (no en `publicaciones.json`) + 2 días — son dos catálogos independientes, cada uno con su propia secuencia de fechas. Seguir el formato de offset que use la entrada más reciente de ese archivo (a la fecha de este documento: `-05:00`, no `Z`).
   - Validar el JS antes de darlo por terminado: extraer el objeto tras `window.PUBLICACIONES_DATA = ` y parsearlo como JSON para confirmar que sigue siendo válido.
   - Si en este punto se descubre que el tema ya tenía una entrada muy similar que se pasó por alto en el análisis inicial, no seguir agregando — volver al flujo de consolidación de "Gestión inteligente de publicaciones e infografías".

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

- Un único archivo JSON en la raíz: un arreglo `[ ... ]` de objetos, cada uno con exactamente el schema de INFOGRAFIA-INVESTIGAR.md (`id`, `imagen`, `fechaPublicacion`, `categoriaPrincipal`, `temas[]`, `tipoContenido`, `es{topico,descripcion}`, `en{topico,descripcion}`, `baseStats{views,likes,shares}`).
- `categoriaPrincipal`/`temas`/`tipoContenido` usan las claves fijas de [`taxonomia.json`](taxonomia.json) — ver "Gobernanza de la taxonomía" abajo. **No confundir con el `<Tema>` de carpeta** (`Construidos/<Tema>/`, `referencias/<Tema>/`): esa es la organización física de archivos construidos (libre, la decide quien crea la infografía); `categoriaPrincipal`/`temas` es la clasificación del catálogo público del sitio (cerrada, requiere autorización para crecer). Una misma carpeta `<Tema>` no tiene que coincidir con una `categoriaPrincipal` — por ejemplo, `Construidos/Escuela_IA/` clasifica sus piezas bajo `categoriaPrincipal: inteligencia-artificial`.
- `imagen` apunta al asset final publicable, ruta relativa a la raíz del repo: `Construidos/<Tema>/<topico-slug>.png` (no al archivo de referencia de `referencias/`).
- Cada infografía nueva agrega un objeto **al final** del arreglo — nunca se reescribe ni se borra una entrada existente, salvo consolidación de contenido relacionado (ver "Gestión inteligente de publicaciones e infografías"), donde se edita in-place por `id` conservando su posición, y la versión anterior de los archivos se archiva en vez de perderse.
- `fechaPublicacion` de la entrada nueva = fecha de la última entrada existente en el arreglo + 2 días (ISO 8601). Si el catálogo está vacío, usar la fecha/hora actual. **Esta suma es siempre relativa a la última fecha ya guardada en el catálogo, nunca a la fecha real de hoy** — si la última entrada quedó con una fecha de hace un mes (porque el catálogo va "adelantado" respecto al calendario real), la siguiente sigue siendo esa fecha + 2 días, no la fecha de hoy + 2 días. Esta regla es para publicaciones normales; **las infografías de evento son la única excepción** y siempre usan la fecha/hora actual (ver "Branding de evento" arriba).
- Nunca debe haber más de dos entradas con la misma fecha en el catálogo completo — verificarlo antes de agregar (el espaciado de +2 días ya lo garantiza en el flujo normal).
- `baseStats` siempre inicia en `{ "views": 0, "likes": 0, "shares": 0 }` — nunca inventar valores.
- No agregar propiedades fuera del schema fijo.

## Gobernanza de la taxonomía (`taxonomia.json`)

[`taxonomia.json`](taxonomia.json) es la fuente de verdad de tres listas cerradas — `categorias` (10), `temas` (45+) y `tiposContenido` (13) — que también vive espejada en `paginaweb/publications/taxonomia.js` (`window.TAXONOMIA_DATA`), igual que `publicaciones.json`/`publicaciones.js`. Reemplazó por completo el antiguo `es.tema`/`en.tema` de texto libre (migración 2026-07-20).

**La taxonomía la administra exclusivamente el usuario.** Queda prohibido crear, renombrar, fusionar, dividir, reorganizar o eliminar cualquier `categoriaPrincipal`, `tema` o `tipoContenido` sin autorización explícita — para cada infografía nueva, usar únicamente claves ya existentes en `taxonomia.json`.

- Cada publicación tiene **una única** `categoriaPrincipal` (nunca dos) y **uno o más** `temas` (un mismo tema puede repetirse en categorías distintas).
- Si el contenido de una infografía nueva no encaja claramente en ninguna categoría/tema/tipo existente, **no forzar la clasificación ni crear uno nuevo** — presentar una propuesta (nombre sugerido, justificación, impacto en la estructura, beneficios, alternativas con la taxonomía actual) y esperar aprobación antes de tocar `taxonomia.json`.
- Los eventos no son una categoría ni un tema — se clasifican con `tipoContenido: "evento"` dentro de la `categoriaPrincipal`/`temas` que ya les correspondan por contenido (ver "Branding de evento" arriba).
- Las "Escuelas" (ej. Escuela de IA, Escuela de Python) no son parte de la taxonomía — son vistas del sitio que agrupan publicaciones por filtro dinámico sobre `temas` ya existentes, nunca una `categoriaPrincipal` ni un `tema` nuevos.

## Reglas generales

- No agregar contenido específico de un tema puntual a INFOGRAFIA-SPEC.md ni INFOGRAFIA-INVESTIGAR.md — son compartidos por todos los temas. Sí se actualizan cuando una mejora de diseño generaliza (ver "Rol permanente y mejora continua").
- No inventar contexto técnico, cifras ni métricas que no estén respaldadas por la referencia (imagen, PDF, PPTX, DOCX) o por el usuario.
- Nombre de carpeta de tema consistente entre `referencias/<Tema>/`, `Construidos/<Tema>/` y el valor `es.tema` usado en `publicaciones.json` para esa misma familia de infografías.
- Si falta el tema, el contexto, o no está claro el topico-slug, preguntar antes de crear carpetas o agregar al catálogo.
- **Diseño arriesgado, no plantillado** (pedido explícito del usuario): al crear cada infografía nueva, evaluar si la composición se siente repetida respecto a piezas anteriores del mismo tema y, si es así, cambiar deliberadamente el layout, la metáfora visual o la paleta antes de construir. La corrección de "queda mucho espacio vacío" nunca debe resolverse solo agrandando fuentes — primero considerar si un elemento visual más audaz (un diagrama real, una metáfora nueva) resuelve mejor el espacio y el mensaje.
- **Legibilidad del texto dentro de cajas/tarjetas** (pedido explícito del usuario, corregido repetidamente en `prompts-iso-9001` y `arbol-modelos-claude`): cuando una infografía tiene mucho contenido de texto repartido en cajas (prompts, preguntas de un árbol de decisión, celdas de tabla, etc.), el tamaño de fuente nunca debe reducirse agresivamente solo para que quepa todo — se prioriza que el texto se lea cómodamente. Antes de exportar, revisar que:
  - Ninguna caja de texto quede con letra visiblemente más pequeña que el resto de elementos de la misma pieza (ej. las preguntas de un diagrama no deben verse más chicas que las tarjetas de resultado que dependen de ellas — deben sentirse en la misma escala visual).
  - Si hay secciones con menos contenido (menos filas, menos bullets) que otras en la misma grilla, no dejarlas con texto minúsculo para "que quepa igual que las demás": o se agranda esa sección específica, o se le agrega contenido real adicional (nunca inventado) para ocupar el espacio, o se ajusta el layout para que esa sección tenga más espacio proporcional.
  - Si dos secciones consecutivas de la misma pieza (ej. una fila de tarjetas y una fila de "tipos" o categorías debajo) quedan visualmente pegadas sin separación clara, agregar espacio (`margin`/`gap`) o una etiqueta de sección entre ellas.
  - Esta regla aplica tanto a piezas nuevas como al revisar piezas ya construidas cuando el usuario señale que el texto quedó muy pequeño.
- **Cada vez que se cree o modifique algo en este proyecto** (una infografía nueva, un rediseño, una regla de este CLAUDE.md, etc.), actualizar el `README.md` correspondiente **en ambos repositorios**: este (`infografia/README.md`) y `/Users/caesar/Documents/GitHub/paginaweb/README.md`, no solo uno de los dos — son dos catálogos públicos independientes que deben quedar consistentes con el estado real del trabajo.
- **La sección "📈 Estadísticas del Repositorio" de cada README (infografia y paginaweb) se debe recalcular y actualizar** en esa misma pasada, con `git log`/`git shortlog` sobre el git de ese repositorio (commits, archivos, líneas +/-, primer/último commit, commits por autor) — nunca dejarla con una cifra vieja. Si el cambio en curso no se ha comiteado todavía, recalcular después de comitear, no antes.
