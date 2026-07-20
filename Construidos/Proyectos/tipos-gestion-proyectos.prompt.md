# Especificación de Diseño — Infografías Técnicas

> Fuente de verdad del diseño — evoluciona con el proyecto (ver "Rol permanente y mejora continua" en CLAUDE.md). **No se modifica con contenido técnico específico de un tema** — eso vive en el `prompt.md` de su propia carpeta. Solo se actualiza aquí cuando una mejora de diseño generaliza a todas las infografías.

Actúa como un Director de Arte Senior, Diseñador UI/UX, Especialista en Visualización de Información, Arquitecto de Software, Ingeniero de Datos Senior, Especialista en Branding para LinkedIn y Experto en Comunicación Visual Técnica.

Tu misión es convertir una o varias imágenes de referencia en una infografía técnica premium, lista para publicarse en LinkedIn o incorporarse en un sitio web profesional. La imagen debe transmitir conocimiento técnico, claridad visual y un alto nivel de diseño editorial.

## Objetivo General

- Crear una infografía moderna, elegante y profesional.
- No crear una fotografía, una escena, un render, una oficina, una habitación ni un escritorio.
- La imagen debe parecer diseñada completamente en Figma, Adobe Illustrator o Adobe XD.
- El contenido técnico siempre será el protagonista.

## Composición

- La información deberá ocupar entre el 80% y el 95% del espacio disponible.
- Toda la composición debe estar organizada mediante: cards, panels, grid layout, diagramas, timeline, flowcharts, callouts, secciones, etiquetas, bloques, iconografía, widgets, dashboard components.
- No utilizar escenarios reales.

## Elementos Prohibidos

Está completamente prohibido generar: escritorios, mesas, oficinas, salas, muebles, ventanas, plantas, personas, manos, teclados, mouse, computadores, laptops, monitores, celulares, tablets, escenarios corporativos, escenarios domésticos, fondos fotográficos.

## Riqueza Visual

Ninguna infografía debe depender únicamente de tarjetas de texto con viñetas. Iconografía con propósito semántico exacto por concepto. Al menos un elemento gráfico no textual además de las tarjetas.

## Firma Profesional

LinkedIn + `cacm523` discreto en la esquina inferior derecha.

## Tamaño

Generar exactamente **1200 × 627 píxeles**, optimizado para LinkedIn.

---

## Contexto específico — 9 Tipos de Gestión de Proyectos

**Referencia principal**: `referencias/Proyectos/tipos-gestion-proyectos/Proyectos.jpeg` — grid 3×3 uniforme de 9 metodologías, cada una con color arbitrario distinto, ícono ilustrativo y descripción de una línea. Se rediseña agrupando por familia real (en vez de repetir el grid uniforme de 9 colores sin relación entre sí) y usando color por función (familia), no arcoíris arbitrario — criterio de `dataviz`.

**Las 9 metodologías, agrupadas en 3 familias reales**:

1. **Marcos predictivos / secuenciales** (planificación por fases, entregables definidos de antemano):
   - **Cascada** — Enfoque lineal y secuencial con fases de proyecto bien definidas.
   - **PRINCE2** — Método basado en procesos con roles definidos y etapas estructuradas.
2. **Marcos ágiles / iterativos** (entrega incremental, adaptación continua):
   - **Ágil** — Enfoque iterativo enfocado en la flexibilidad y la colaboración.
   - **Scrum** — Marco ágil que utiliza sprints para entregar valor incremental.
   - **Kanban** — Enfoque visual que usa tableros para gestionar el trabajo en curso.
3. **Técnicas de optimización y análisis** (no son ciclos de vida completos, se usan para programar o mejorar procesos dentro de cualquier marco):
   - **Lean** — Metodología enfocada en maximizar el valor y minimizar el desperdicio.
   - **Seis Sigma** — Enfoque basado en datos para la mejora de procesos y control de calidad.
   - **Método del Camino Crítico (CPM)** — Técnica para programar tareas basada en las dependencias entre ellas.
   - **PERT** — Método para analizar y representar tareas del proyecto y cronogramas.

**Dirección visual**: 3 franjas horizontales (una por familia), cada una con una etiqueta de familia a la izquierda (color distintivo: azul pizarra para predictivos, verde azulado para ágiles, ámbar para técnicas de análisis) y, a la derecha, las tarjetas de sus metodologías en fila (2, 3 o 4 según la familia — el ancho de cada tarjeta se ajusta a la cantidad real de miembros, sin forzar un grid uniforme de 9 celdas idénticas). Ícono semántico propio por metodología (escalones descendentes para Cascada, ciclo de flechas para Ágil, tablero de 3 columnas para Kanban, ciclo DMAIC para Seis Sigma, árbol jerárquico para PRINCE2, red de nodos para Camino Crítico y PERT, checklist con flecha de reducción para Lean).

**Nota**: la referencia no trae cifras verificables (son descripciones conceptuales de cada metodología) — no se inventan números ni porcentajes; la única "visualización de datos" es la propia agrupación por familia, que es información real derivada del contenido, no fabricada.
