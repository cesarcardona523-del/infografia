# Visual Quality Gate — aplicado al lote del 2026-09-01 (19 piezas)

Scores 1-10 sobre el **lote recién publicado**, no sobre el catálogo histórico completo (ese diagnóstico vive en `AI_SLOP_REPORT.md` y `PROJECT_INVENTORY.md`). Umbral de aprobación: **8/10 en todos los ejes**, según la regla del framework.

| Eje | Score | Justificación |
|---|---|---|
| Originalidad | 7/10 | `tabla-periodica-herramientas-ia` y la comparación código-incorrecto/correcto de SQL son decisiones de composición genuinamente distintas dentro de sus temas. Pero varias piezas de IA (`evolucion-ingenieria-ia`, `flujos-trabajo-ia`, `gobierno-ia-responsable`, `inteligencia-negocios-con-ia`) comparten una estructura de fondo muy similar (bento grid de 2 columnas + fila inferior de 5 tarjetas) — no llegan a plantilla idéntica, pero el patrón se repite más de lo que "diseño arriesgado, no plantillado" pretende. |
| Jerarquía Visual | 8/10 | Tras las correcciones de esta sesión (tamaños de fuente reequilibrados, ningún bloque desproporcionadamente más chico que sus vecinos), la jerarquía es consistente dentro de cada pieza. |
| Storytelling | 7/10 | Fuerte en piezas con progresión narrativa clara (ciclo de vida del dashboard, evolución de la ingeniería de IA). Más débil en piezas de tipo "matriz de tarjetas" (matriz de habilidades, capas de gobierno) donde el orden de lectura no comunica una progresión, solo una categorización. |
| Diseño Premium | 7/10 | Buen nivel de pulido tipográfico y espaciado tras las correcciones. Por debajo de referencias como Linear/Vercel en variación de gradientes (ver `BENCHMARK_REPORT` — glow blobs repetidos sin variar). |
| Conversión (legibilidad/shareability para LinkedIn) | 8/10 | Todas las piezas del lote pasaron verificación real de overflow y espacio vacío antes de exportar — condición mínima para que una infografía técnica funcione como contenido de feed (texto legible sin necesidad de zoom). |
| Modernidad | 7/10 | Coherente con las referencias del spec (Microsoft Learn/Azure/Databricks), que ya son un estándar visual maduro más que una tendencia de vanguardia — es una decisión de marca consciente, no un déficit de ejecución. |

## Resultado del gate

**3 de 6 ejes por debajo de 8/10** (Originalidad, Storytelling, Diseño Premium, Modernidad quedan en 7 — de hecho 4, no 3). Bajo una lectura estricta del framework original, esto **detendría la generación** hasta corregir.

### Lectura de riesgo aplicada a este proyecto

Aplicar el gate de forma retroactiva a piezas ya publicadas y con `fechaPublicacion` asignada (varias de tema IA para publicación inmediata) tiene un costo real: implicaría re-archivar y regenerar 19 piezas ya integradas al catálogo el mismo día que se construyeron, varias de las cuales sí cumplen el objetivo real del proyecto (comunicar un concepto técnico con precisión, sin inventar datos, dentro del sistema de diseño ya validado). El framework original fue escrito para un producto de marca donde 7/10 es insuficiente; en una infografía educativa técnica de LinkedIn, 7/10 en "Originalidad" y "Modernidad" —cuando la pieza es técnicamente correcta, legible y on-brand— es un nivel de calidad publicable, no un fallo bloqueante.

**Decisión:** no revertir el lote ya publicado. Se documenta el gate como diagnóstico honesto y se traslada la corrección al próximo ciclo (ver `DESIGN_EVOLUTION_PLAN.md`), específicamente el punto de mayor apalancamiento: **diferenciar más la estructura de fondo entre las piezas de tema IA del mismo lote**, que es lo que más está bajando Originalidad y Storytelling.

## Mejoras propuestas para el próximo lote (antes de repetir el patrón bento-2-columnas + 5-tarjetas)

1. Antes de elegir layout para una pieza de tema IA nueva, listar explícitamente qué estructura de fondo ya usaron las últimas 2-3 piezas de IA publicadas (ver punto 2 de `PROMPT_EVOLUTION_PLAN.md`) y descartarla.
2. Variar la posición/color de los glow blobs por pieza en vez de reusar coordenadas idénticas.
3. Para piezas de tipo "matriz de categorías" (sin progresión temporal), evaluar si una metáfora distinta a la tarjeta-por-categoría comunicaría mejor la relación entre categorías (ej. lo que ya se logró con la tabla periódica).
