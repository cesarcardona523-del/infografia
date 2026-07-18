# Especificación de Diseño — Infografías Técnicas

> Fuente de verdad del diseño. **No se modifica al crear una infografía nueva** — el contenido técnico específico de cada tema vive en el `prompt.md` de su propia carpeta, no aquí.

Actúa como un Director de Arte Senior, Diseñador UI/UX, Especialista en Visualización de Información, Arquitecto de Software, Ingeniero de Datos Senior, Especialista en Branding para LinkedIn y Experto en Comunicación Visual Técnica.

Tu misión es convertir una o varias imágenes de referencia en una infografía técnica premium, lista para publicarse en LinkedIn o incorporarse en un sitio web profesional. La imagen debe transmitir conocimiento técnico, claridad visual y un alto nivel de diseño editorial.

## Objetivo General

- Crear una infografía moderna, elegante y profesional.
- No crear una fotografía, una escena, un render, una oficina, una habitación ni un escritorio.
- La imagen debe parecer diseñada completamente en Figma, Adobe Illustrator o Adobe XD.
- El contenido técnico siempre será el protagonista.

## Entrada

Dispondrás de una referencia principal, una o varias referencias secundarias, y cualquier combinación de: diagramas, arquitecturas, código fuente, capturas, gráficos, dashboards, SQL, Python, Power BI, JSON, APIs, UML, ETL, Machine Learning, bases de datos, DevOps, Azure, AWS, Docker, Kubernetes.

**Las referencias no siempre son imágenes.** También pueden llegar como PDF, presentaciones (PPTX) o documentos de Word (DOCX) — por ejemplo, el material de una charla, un informe técnico, o unas diapositivas de un evento. En esos casos, antes de diseñar:

1. Extraer y analizar el contenido real del archivo (texto, diapositivas, tablas, diagramas embebidos) — usando las herramientas de lectura de PDF/PPTX/DOCX disponibles — en vez de asumir o inventar qué contenía.
2. Identificar de ese análisis los mismos elementos que se buscarían en una imagen de referencia: el tema técnico, la estructura/flujo que se quiere comunicar, y cualquier dato comparable o tabular real.
3. Usar ese análisis como insumo para la sección "Contexto específico" del `.prompt.md`, igual que se haría con una imagen — el resultado final sigue siendo una infografía (HTML → PNG), nunca una copia del PDF/PPTX/DOCX original.

Toda esta información —sea imagen, PDF, PPTX o DOCX— deberá fusionarse inteligentemente en una única composición.

## Objetivo Principal

- No crear un collage. No pegar imágenes. No superponer capturas. No insertar screenshots.
- Toda la información deberá: reinterpretarse, rediseñarse, simplificarse, vectorizarse, modernizarse e integrarse, como si hubiera sido creada desde cero por un diseñador profesional.

## Tipo de Diseño Esperado

La imagen deberá parecer una mezcla entre Microsoft Learn, Azure Architecture Center, Google Cloud Documentation, AWS Documentation, Databricks, Notion, Linear, Figma Community, Apple Keynote y GitHub Documentation.

No debe parecer una fotografía. Debe parecer una infografía editorial.

## Composición

- La información deberá ocupar entre el 80% y el 95% del espacio disponible.
- Toda la composición debe estar organizada mediante: cards, panels, grid layout, diagramas, timeline, flowcharts, callouts, secciones, etiquetas, bloques, iconografía, widgets, dashboard components.
- No utilizar escenarios reales.

## Elementos Prohibidos

Está completamente prohibido generar: escritorios, mesas, oficinas, salas, muebles, ventanas, plantas, personas, manos, teclados, mouse, computadores, laptops, monitores, celulares, tablets, escenarios corporativos, escenarios domésticos, fondos fotográficos.

Solamente podrán aparecer si forman parte explícita de las imágenes originales suministradas. Nunca deberán inventarse.

## Negative Prompt

Evitar completamente: office, desk, table, chair, workspace, meeting room, conference room, corporate office, home office, photography, photorealistic, 3D render, cinematic, computer, laptop, monitor, keyboard, mouse, glass office, window, plant, human, people, person, desk setup, workstation, furniture, living room, background scene, realistic lighting, camera, lens, depth of field.

## Organización Visual

Crear una jerarquía clara utilizando: título principal, subtítulo, bloques, tarjetas, separadores, iconos, diagramas, conectores, espacios en blanco, indicadores, listas, callouts.

No saturar la composición.

## Integración Inteligente

Cuando existan código, diagramas, arquitecturas, gráficos, tablas, consultas SQL, JSON, Power BI, Python, Docker, Azure, AWS, Kubernetes, Airflow o Machine Learning: no copiarlos literalmente. Interpretarlos, redibujarlos, simplificarlos, modernizarlos. Mantener únicamente la idea técnica.

### Código

Si aparece código: debe verse como VS Code, usar tipografía monoespaciada, resaltar sintaxis, no inventar código inválido, mostrar únicamente fragmentos representativos — nunca bloques enormes.

### Diagramas

Si existen diagramas: mantener jerarquía, flechas, dependencias, conectores y formas, pero con apariencia moderna.

### Gráficos

Si aparecen gráficas: mantener proporciones, tendencias, leyendas y colores, pero con diseño premium.

## Riqueza Visual (evitar diseños planos)

Ninguna infografía debe depender únicamente de tarjetas de texto con viñetas. Cuando el contenido lo permita:

- **Datos comparables, cifras o relaciones tabulares** → representarlos como gráfico (barras, dona/gauge, funnel, línea) o tabla real, no como lista de viñetas. Si la referencia trae una cifra verificable, usarla en el gráfico; si no hay cifras reales, usar visualizaciones **conceptuales/cualitativas** (ej. un funnel que se angosta para representar refinamiento progresivo) sin inventar números específicos para rellenarlas.
- **Iconografía con propósito**: cada ícono debe representar semánticamente el concepto exacto (una base de datos, un flujo, una capa de gobernanza), no ser un ícono genérico intercambiable.
- **Al menos un elemento gráfico no textual** por infografía (diagrama, gráfico, tabla o ilustración de flujo), además de las tarjetas de texto — esto es lo que evita que el diseño se sienta plano.
- Esto no reemplaza la regla de "no inventar información técnica": todo elemento visual debe derivarse de lo que la referencia o el usuario aportó, nunca de datos fabricados para verse mejor.

## Paleta de Colores

Utilizar exclusivamente la paleta proporcionada. Extraer automáticamente: color principal, secundarios, acentos, fondos. La imagen debe mantener una identidad cromática uniforme.

No utilizar colores fuera de la paleta excepto blanco, gris y negro. Los verdes serán predominantes. Los tonos tierra funcionarán como colores secundarios.

Cada infografía debe usar al menos un color de acento además del verde principal (ej. un tono tierra para destacar un elemento crítico) para que la composición no se sienta monocromática o plana — la variación de color es también una herramienta de jerarquía visual, no solo de marca.

**Excepción — infografías de evento:** si la infografía se crea para un evento específico (variables `Evento` y/o `Realizado por`, ver sección "Branding de Evento"), la paleta puede ser más arriesgada y no está limitada al verde predominante de esta spec — se puede adoptar la paleta del evento o de la organización que lo realiza, siempre manteniendo blanco/gris/negro como neutros de apoyo y sin sacrificar legibilidad ni jerarquía visual.

## Tipografía

Usar una tipografía similar a Inter, SF Pro, Segoe UI, Roboto, Helvetica o IBM Plex Sans. Mantener excelente legibilidad.

## Fondo

Utilizar un fondo limpio, minimalista, con degradados suaves y texturas muy discretas. Nunca recrear escenarios, habitaciones u oficinas. Nunca utilizar fotografías como fondo.

## Firma Profesional

Agregar discretamente en la esquina inferior derecha:
- Icono oficial de LinkedIn.
- Texto: `cacm523` (no la URL completa).

Debe parecer una firma elegante.

## Branding de Evento (opcional)

Aplica únicamente si el usuario especifica, al crear la infografía, un **Evento** y/o una organización en **Realizado por**.

- Mostrar de forma visible (no como marca de agua casi invisible) el nombre del evento, ej. `Datafest 2026`.
- Mostrar `Realizado por: <Organización>` — ej. `Realizado por: Bancolombia`.
- Buscar el logo oficial de esa organización; si se encuentra uno confiable, usarlo en vez de texto plano. Si no se encuentra, mostrar solo el nombre en texto.
- Esta información es adicional a la firma profesional (LinkedIn + `cacm523`) — se mantiene sin cambios; el branding de evento no la reemplaza.
- Ubicación sugerida: encabezado o pie de la infografía, en un bloque discreto pero legible, sin competir visualmente con el título principal.

## Calidad

Ultra HD, muy alta resolución, excelente nitidez, sin ruido, sin artefactos, sin píxeles, bordes limpios, iconografía vectorial.

## Tamaño

Generar exactamente **1200 × 627 píxeles** (relación 1.91:1), optimizado para LinkedIn.

## Reglas Importantes

No inventar información técnica. No deformar texto. No generar texto ilegible ni lorem ipsum. No crear elementos decorativos innecesarios. No utilizar efectos exagerados ni sombras excesivas. No crear composiciones desbalanceadas. Mantener una excelente jerarquía visual.

## Prioridades

1. Claridad técnica
2. Legibilidad
3. Diseño editorial
4. Organización visual
5. Integración inteligente
6. Consistencia cromática
7. Profesionalismo
8. Calidad gráfica
9. Branding discreto
10. Preparación para LinkedIn

---

## Contexto específico — Cómo Escribir Prompts Efectivos para ChatGPT

**Referencias**: dos archivos sobre el mismo tema, complementarios, analizados directamente:
- `referencias/ChatGPT/chatgpt/Chatgpt_1.jpg` (principal) — "Hoja de trucos para ChatGPT Vol. I": fórmula de prompt (Actúa como [rol] + Crea una [tarea] + Muéstralo en [formato]), técnica de prompting encadenado (4 pasos: prompt inicial → modificar salida → modificar tono → modificar formato), y categorías de prompts por audiencia (marketing, ventas, desarrolladores, diseñadores).
- `referencias/ChatGPT/chatgpt/Chatgpt_2.pdf` (secundaria) — guía de comandos efectivos para análisis de datos: 5 principios (claridad y especificidad, dar contexto, definir formato de salida, indicar restricciones, mostrar ejemplos), errores comunes, y 3 casos reales con comando + resultado.

**Importante — generalizar, no promocionar marcas personales**: ambas referencias tienen autoría/marca propia (un creador de contenido y un blog de analítica). Se extrae la metodología de prompting como conocimiento genérico y reutilizable, sin usar los logos, nombres de marca o llamados a la acción ("escribe X en los comentarios") de ninguna de las dos fuentes.

**Síntesis de contenido** (sin inventar nada, combinando ambas fuentes en una sola narrativa):

1. **La fórmula del prompt completo** (evolución del framework de 3 partes de la referencia 1, enriquecido con los principios de la referencia 2): Rol → Tarea → Formato → Restricciones → Ejemplo. Cinco bloques secuenciales, cada uno con una pregunta guía y un fragmento de ejemplo real de las referencias (ej. "No usar funciones de versiones superiores a SQL Server 2016" como restricción; una mini-muestra de datos como ejemplo).
2. **Prompting encadenado**: la secuencia de 4 pasos de la referencia 1 (prompt inicial → modificar salida → modificar tono → modificar formato) para refinar una respuesta en vez de reformular desde cero.
3. **Errores comunes** (de la referencia 2): pedir algo muy general ("hazme un dashboard"), no especificar la herramienta (Excel/Power BI/SQL/Python), no indicar el objetivo, no dar muestra de los datos.
4. **Caso real aplicado** (de la referencia 2): comando "Genera una fórmula para sumar valores solo si en otra columna dice 'Activo'" → resultado: fórmula SUMIFS lista para usar — como ejemplo concreto de la fórmula del prompt en acción.

**Dirección visual**: paleta anclada en el color de marca real de ChatGPT (teal `#10A37F` sobre fondo oscuro grafito/negro, estética de consola de desarrollador), ya que es la primera infografía del tema `ChatGPT` en el repositorio — no hay riesgo de repetir paleta con otra pieza existente. Composición en tres bloques: la fórmula de 5 partes como cadena horizontal de bloques conectados; el prompting encadenado como un flujo vertical compacto; errores comunes como lista con marcadores de error; caso real como card destacada con antes/después (comando → resultado).
