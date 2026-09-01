# Image-First Design System — metodología de gobierno

> Regla fundamental adoptada 2026-09-01: **el HTML es el medio de producción, la imagen PNG es el producto final.** Toda evaluación de calidad se hace sobre la imagen renderizada, no sobre el código que la generó. Este documento gobierna cómo se construye y aprueba cada infografía nueva de aquí en adelante. Complementa — no reemplaza — [INFOGRAFIA-SPEC.md](../INFOGRAFIA-SPEC.md) (qué reglas visuales fijas tiene el proyecto) y los demás documentos de `design-audit/` (qué se aprendió de piezas anteriores).

## Orden de evaluación obligatorio

1. Imagen final 2. Composición visual 3. Jerarquía de información 4. Storytelling 5. Dirección artística 6. Legibilidad 7. Originalidad 8. Coherencia con el tema 9. HTML utilizado para producirla.

Nunca invertir este orden — un HTML técnicamente limpio con una imagen final mediocre es un fallo del proyecto; un HTML con CSS imperfecto que produce una imagen final excelente no lo es (aunque igual conviene limpiarlo por la regla de calidad de código de `CLAUDE.md`).

## Workflow obligatorio por pieza nueva

```
CONTENIDO → MENSAJE PRINCIPAL → STORYTELLING → CONCEPTO VISUAL →
DIRECCIÓN ARTÍSTICA → COMPOSICIÓN → HTML → RENDER → IMAGEN FINAL → VISUAL QA → APROBACIÓN
```

**No escribir HTML hasta responder, explícitamente y por escrito en el `.prompt.md` de la pieza (ver punto 1-3 de `PROMPT_EVOLUTION_PLAN.md`, que ya exigía esto parcialmente):**

1. ¿Cuál es la idea principal?
2. ¿Qué debe entender el usuario en 3 segundos?
3. ¿Cuál es el elemento visual dominante?
4. ¿Cuál es la historia que cuenta la composición (entrada → desarrollo → conclusión)?
5. ¿Qué hace diferente esta pieza frente a las últimas del mismo tema? (consultar `VISUAL_LIBRARY.md` primero)
6. ¿Qué elemento visual representa realmente el tema (no genérico)?
7. ¿Qué estructura sería inesperada pero apropiada para este contenido?

Si estas 7 preguntas no tienen respuesta concreta, no se genera HTML.

## Content → Visual Mapping (sustituye la elección de layout por defecto)

| Tipo de contenido | Estructuras a considerar (no agotan la lista) |
|---|---|
| Procesos | Timeline, Flow, Journey, Pipeline |
| Comparaciones | Split composition, Before/After, Matrix, Visual balance |
| Conceptos | Central metaphor, Radial diagram, Ecosystem, Layers |
| Datos | Data visualization, Editorial charts, Visual statistics |
| Evolución | Timeline, Transformation, Before/After, Progression |
| Arquitectura | Layers, System diagram, Network, Blueprint |
| Personas/roles | Persona cards, Journey, Narrative composition |

**Prohibido por defecto** (no eliminado del repertorio, pero exige justificación explícita si se reusa dos veces seguidas dentro del mismo tema): bento grid genérico, 2 columnas + 5 cards, header+cards+footer sin variación, KPI cards genéricas, icon+title+paragraph repetido, grid uniforme sin jerarquía.

## Anti-AI-Slop: Repetition Score

Antes de aprobar una pieza nueva, compararla contra la última pieza del mismo tema (registrada en `VISUAL_LIBRARY.md`) en 5 ejes, cada uno 1-10 (10 = idéntico):

- Estructura repetida
- Composición repetida
- Tratamiento tipográfico repetido
- Patrón de componentes repetido
- Dirección artística repetida

**Si el promedio supera 60% de similitud → rechazar esa dirección y elegir otra estructura del mapping de arriba.** Cambiar solo colores/texto/íconos sobre la misma estructura NO cuenta como pieza nueva.

## Visual Hero

Cada pieza debe tener una respuesta clara a "¿dónde mira primero el usuario?" — el elemento dominante puede ser una ilustración, un diagrama, una cifra grande, una metáfora visual o una composición tipográfica. **El título no es automáticamente el elemento dominante por defecto** — decidirlo activamente.

## Densidad de información

Clasificar todo el contenido de la pieza en:
- **Primary message** — lo que se entiende en 3 segundos.
- **Secondary message** — lo que refuerza al primario.
- **Supporting information** — detalle que solo lee quien se detiene.

Recortar o reducir lo que no aporte a ninguna de las tres capas, en vez de intentar caber todo el material de referencia. Esto no contradice la regla existente de "Aprovechamiento del Espacio" (que prohíbe huecos vacíos) — ambas reglas conviven: **no hay espacio vacío, pero tampoco hay texto que solo llena espacio sin jerarquía.**

## Image Quality Gate (5 tests + score final)

Aplicar sobre el **PNG final**, no sobre el HTML:

1. **3-Second Test** — mirar 3 segundos, ¿qué se entendió? Sin respuesta clara → rechazar.
2. **Thumbnail Test** — reducir a ~300px de ancho. Si todo pesa igual (sin jerarquía visible) → rechazar.
3. **Squint Test** — desenfocar/entrecerrar los ojos. Debe verse una jerarquía clara de masas.
4. **Grayscale Test** — evaluar sin depender del color. Contraste y lectura deben sostenerse igual.
5. **Uniqueness Test** — comparar contra las últimas piezas del mismo tema en `VISUAL_LIBRARY.md`. ¿Se reconocería sin leer el título? Si no → revisar.

### Final Visual Score (promedio de 8 ejes, 1-10 cada uno)

Composition · Storytelling · Originality · Visual Hierarchy · Readability · Topic Relevance · Brand Consistency · Information Design

| Promedio | Acción |
|---|---|
| 9–10 | Publicar |
| 8–8.9 | Publicar con ajustes menores |
| 7–7.9 | Revisar |
| <7 | Rechazar y rediseñar |

**Nota de aplicación en este proyecto** (ver precedente en `VISUAL_QUALITY_GATE.md`): el gate se aplica de forma prospectiva a partir de este documento. No se revierte retroactivamente una pieza ya publicada y catalogada solo por no alcanzar el umbral si el costo de regenerarla no se justifica frente a la ganancia real — esa decisión se documenta explícitamente en `DESIGN_EVOLUTION_PLAN.md`, no se aplica en silencio.

## Corrección quirúrgica, no regeneración completa

Cuando el Quality Gate marque una falla, identificar primero si el problema es de composición, tipografía, spacing, color, contenido, ilustración o jerarquía — y corregir únicamente ese elemento. Regenerar la pieza completa solo cuando el concepto visual de fondo (no un detalle) sea el problema.

## Optimización de tokens — qué consultar antes de crear, y en qué orden

1. `VISUAL_LIBRARY.md` — qué composiciones ya se usaron en este tema, para descartarlas.
2. `DESIGN_MISTAKES.md` — errores técnicos y de diseño ya identificados, no repetir.
3. `DESIGN_PATTERNS.md` — metáforas y micro-patrones ya validados, como punto de partida (no plantilla).
4. `DESIGN_HISTORY.md` — hitos recientes del sistema, por si algo cambió desde la última pieza.

**No re-auditar todo el repositorio para cada pieza nueva** — estos 4 documentos (+ `VISUAL_LIBRARY.md`) son la memoria persistente que reemplaza ese análisis repetido.

## Prioridad de generación de elementos gráficos

1. SVG 2. CSS 3. Canvas 4. ThreeJS 5. Imagen generativa — usar generación pesada solo cuando aporte valor visual real y cumpla una función narrativa, nunca "porque se ve bonita". (Nota de contexto: hoy el pipeline de este proyecto no incluye generación de imágenes IA ni ThreeJS — todas las piezas son HTML/CSS/SVG puro exportado a PNG vía Chrome headless. Esta prioridad queda documentada para el día en que se evalúe incorporar esas capas.)
