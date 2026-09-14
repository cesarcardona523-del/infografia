# Especificación de Diseño — Infografías Técnicas

> Fuente de verdad del diseño — evoluciona con el proyecto (ver "Rol permanente y mejora continua" en CLAUDE.md). **No se modifica con contenido técnico específico de un tema** — eso vive en el `prompt.md` de su propia carpeta.

(Ver el archivo raíz `INFOGRAFIA-SPEC.md` para el contenido completo compartido por todo el catálogo — paleta, tipografía, composición, elementos prohibidos, branding, firma, tamaño 1200×627px.)

## Contexto específico — ¿Por qué Power BI si ya hay IA que crea dashboards?

**Tema**: hoy varios modelos de IA generan dashboards funcionales en HTML/CSS/JS a partir de un prompt (ChatGPT Canvas, Claude con Artifacts, herramientas tipo v0, entre otras) — el usuario mismo ha construido algunos así. La pregunta real no es "IA o Power BI", sino qué aporta cada uno y cuándo conviene cada camino.

**Referencia suministrada por el usuario** (1 imagen pegada en el chat, sin archivo guardado en disco): infografía de marca personal con header grande (título en 4 líneas) + panel superior "la IA puede generar dashboards, pero Power BI da control/calidad/escalabilidad" con 4 atributos (Confiable, Flexible, Escalable, Colaborativo) + bloque VS (robot vs ícono Power BI) + grid de 6 razones numeradas para elegir Power BI + comparación final "IA genera un dashboard" vs "Power BI te da resultados sostenibles" + cierre "la clave no es IA vs Power BI, es IA + Power BI".

**Corrección de diseño aplicada** (misma corrección ya pedida antes para otras piezas): header compacto — eyebrow pequeño y alargado + título + subtítulo, sin el bloque de título gigante de 4 líneas de la referencia.

**Aporte pedido por el usuario**: reconocer explícitamente, con contenido real (sin inventar cifras), que ya existen múltiples modelos de IA que generan dashboards con HTML/CSS/JS directamente desde un prompt — se nombra esta capacidad en el panel "Ejemplo en la práctica" en vez de tratarla como una amenaza hipotética, y se usa como punto de partida real para explicar en qué momento conviene pasar a una herramienta de BI dedicada como Power BI.

**Estructura elegida** (variante del "blueprint numerado"): header compacto con callout de cita → bloque VS (IA genérica vs Power BI, con 4 atributos de Power BI) → grid de 6 razones numeradas (1-6) → comparación final de 2 columnas ("IA genera un dashboard" vs "Power BI da resultados sostenibles") → banda de cierre con la idea integradora "no es IA vs Power BI, es IA + Power BI".

**Paleta**: Power BI tiene identidad de marca propia y es el tema central de la pieza (junto a la IA genérica) → aplica la excepción de "Colores de marca por aplicación": amarillo/negro de Power BI (`#F2C811`, `#000000`) como acento del lado Power BI, combinado con el verde+tierra por defecto del proyecto para el resto de la composición y el lado de "IA genérica" (no hay una marca de IA específica protagonista, es un concepto genérico).

**Iconografía**: ícono oficial de Power BI (`assets/iconos-apps/power-bi.svg`, ya en el repo). Para "IA genérica" se usa un ícono vectorial de robot/circuito simple (no fotorrealista, no es una marca comercial).

**Catálogo**: `categoriaPrincipal: "powerbi-y-visualizacion"`, `temas: ["power-bi", "ia"]` — incluye tema IA por el ángulo central de la pieza, por lo que aplica la regla de publicación inmediata (mañana).
