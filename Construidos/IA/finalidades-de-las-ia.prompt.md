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

Dispondrás de una imagen principal, una o varias imágenes secundarias, y cualquier combinación de: diagramas, arquitecturas, código fuente, capturas, gráficos, dashboards, SQL, Python, Power BI, JSON, APIs, UML, ETL, Machine Learning, bases de datos, DevOps, Azure, AWS, Docker, Kubernetes.

Toda esta información deberá fusionarse inteligentemente en una única composición.

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

## Paleta de Colores

Utilizar exclusivamente la paleta proporcionada. Extraer automáticamente: color principal, secundarios, acentos, fondos. La imagen debe mantener una identidad cromática uniforme.

No utilizar colores fuera de la paleta excepto blanco, gris y negro. Los verdes serán predominantes. Los tonos tierra funcionarán como colores secundarios.

**Excepción — infografías de evento:** si la infografía se crea para un evento específico (variables `Evento` y/o `Realizado por`, ver sección "Branding de Evento"), la paleta puede ser más arriesgada y no está limitada al verde predominante de esta spec — se puede adoptar la paleta del evento o de la organización que lo realiza, siempre manteniendo blanco/gris/negro como neutros de apoyo y sin sacrificar legibilidad ni jerarquía visual.

## Tipografía

Usar una tipografía similar a Inter, SF Pro, Segoe UI, Roboto, Helvetica o IBM Plex Sans. Mantener excelente legibilidad.

## Fondo

Utilizar un fondo limpio, minimalista, con degradados suaves y texturas muy discretas. Nunca recrear escenarios, habitaciones u oficinas. Nunca utilizar fotografías como fondo.

## Branding

Agregar una marca de agua extremadamente discreta:
- Texto: `Cesar Cardona`
- Ubicación: diagonal o centro
- Opacidad: 5% — debe ser prácticamente invisible.

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
- Esta información es adicional a la marca de agua ("Cesar Cardona" al 5%) y a la firma profesional (LinkedIn + `cacm523`) — ambas se mantienen sin cambios; el branding de evento no las reemplaza.
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

## Contexto específico — Finalidades de las IA

**Evento:** Datafest 2026 — **Realizado por:** Bancolombia (aplica la excepción de paleta y "Branding de Evento").

**Imagen de referencia:** 1 captura de diapositiva real de Datafest 2026 (`../referencias/IA/finalidades-de-las-ia/Fiabilidad_Modelos.png`), estilo terminal/CLI (verde fósforo sobre negro, monoespaciado, esquinas tipo HUD). Es contenido genuino de la charla — traducir la tabla a una infografía editorial, no copiarla como screenshot.

**Tema de la charla:** "Matriz de Fiabilidad de Modelos" — el enfoque/finalidad implícita de cada gran proveedor de IA y qué tan dispuesto está cada modelo a admitir que no sabe algo.

**Contenido a mantener (tabla de 4 filas, Modelo | Enfoque | Diagnóstico):**

1. **Google (Gemini)** — Enfoque: Rigurosidad contextual. Diagnóstico: Excelente para sintetizar textos, pero cuidado si son demasiado grandes.
2. **Anthropic (Claude)** — Enfoque: Honestidad y seguridad. Diagnóstico: Es el modelo que más admite que "no sabe".
3. **OpenAI (Familia GPT)** — Enfoque: "Asertividad Comercial". Diagnóstico: Prioriza responder siempre y no admitir ignorancia.
4. **DeepSeek / Qwen (made in China)** — Enfoque: El bajo costo. Diagnóstico: Resuelve de manera lógica su falta de información.

**Investigación adicional (complemento real, verificado):** se buscó en internet si esta caracterización cualitativa coincide con benchmarks públicos de 2026. Sí coincide: reportes de referencia de hallucination/calibración de 2026 ubican a Claude como el modelo con la tasa más alta de admitir "no lo sé" entre los modelos evaluados, mientras GPT tiende a maximizar la tasa de respuesta (alta cobertura) a costa de una mayor tasa de alucinación. Agregar esto como una nota de respaldo breve, dejando claro que la matriz original es una **lectura cualitativa del expositor**, no un benchmark oficial — no inventar cifras específicas no verificadas directamente por esta sesión, mantenerlo en términos generales.

**Cómo complementar (no solo redibujar):**

- Mantener el lenguaje visual "terminal/matrix" de la referencia (verde fósforo, monoespaciado, esquinas HUD) — es una identidad visual fuerte y coherente con el título "Matriz de Fiabilidad".
- Agregar la nota de respaldo de benchmarks públicos 2026 mencionada arriba, aclarando que la matriz es una lectura cualitativa del expositor.
- Incluir el badge de evento (Datafest 2026 / Realizado por: Bancolombia) igual que en las otras infografías de este mismo evento, para mantener coherencia de marca entre las tres piezas.

**Título principal sugerido:** "Finalidades de las IA: el Enfoque Detrás de Cada Modelo".
