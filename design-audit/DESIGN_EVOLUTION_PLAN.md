# Design Evolution Plan — próximos pasos accionables

Síntesis final de las 8 fases del audit, convertida en un checklist de acción concreta. Consultar antes de construir la siguiente pieza de cualquier tema.

> Gobernanza vigente desde 2026-09-01: el workflow completo de creación (7 preguntas antes de escribir HTML, Content→Visual Mapping, Repetition Score, Image Quality Gate) vive en [IMAGE_FIRST_SYSTEM.md](IMAGE_FIRST_SYSTEM.md) — este checklist es un resumen operativo, no lo sustituye.

## Checklist obligatorio antes de construir una pieza nueva

1. Consultar `VISUAL_LIBRARY.md` — identificar las composiciones ya usadas en el mismo tema y descartarlas explícitamente (Repetition Score).
2. Leer `DESIGN_MISTAKES.md` — verificar que ninguno de los 10 errores listados se repita.
3. Leer `DESIGN_PATTERNS.md` y el Content→Visual Mapping de `IMAGE_FIRST_SYSTEM.md` — elegir una estructura acorde al tipo de contenido, no la primera que venga a la mente.
4. Responder las 7 preguntas de dirección artística de `IMAGE_FIRST_SYSTEM.md` antes de escribir una sola línea de HTML.
5. Si la pieza usa "glow blobs" decorativos, variar posición/color respecto a la última pieza del mismo tema — no copiar coordenadas.
6. Antes de exportar, correr el chequeo de clases CSS huérfanas (usadas en HTML, no definidas en `<style>`) y el chequeo visual real de espacio vacío por tarjeta.
7. Aplicar el Image Quality Gate (5 tests + score final) sobre el PNG renderizado, no sobre el HTML.
8. Registrar la pieza en `VISUAL_LIBRARY.md` y actualizar `DESIGN_HISTORY.md` si introduce un patrón nuevo digno de generalizarse.

## Prioridad 1 — cerrar la brecha de Originalidad/Storytelling del lote 2026-09-01

Las 4 piezas de tema IA que comparten estructura bento 2-columnas + fila de 5 tarjetas (`evolucion-ingenieria-ia`, `flujos-trabajo-ia`, `gobierno-ia-responsable`, `inteligencia-negocios-con-ia`) no se regeneran ahora (no gana lo suficiente frente al costo, y ya están publicadas y catalogadas), pero **la próxima pieza de tema IA que se construya no debe repetir esa estructura** — usar una metáfora distinta (pipeline horizontal, comparación binaria, tabla de categorías) según el contenido específico.

## Prioridad 2 — generalizar el patrón "comparación binaria lado a lado"

Validado en SQL (código incorrecto/correcto). Candidato natural para la próxima pieza de gobierno de datos o seguridad que tenga un contraste binario claro (configuración segura/insegura, antes/después de un control).

## Prioridad 3 — auditoría de deuda histórica (no urgente, incremental)

No auditar los 17 temas restantes de una sola vez (regla vigente de CLAUDE.md: "no hace falta auditar los demás temas en esa misma tarea"). En su lugar, cuando se vuelva a tocar un tema específico:
- `Cultura_Datos` (19 piezas): candidato de mayor impacto — es el tema con más patrones de `AI_SLOP_REPORT.md` sin corregir.
- `Bigdata` (4 piezas): verificar consistencia de paleta (ámbar/marrón dominante vs. verde base del proyecto).
- Cualquier pieza con `@import`/`<link>` a Google Fonts remanente (riesgo técnico real, no solo estético).

## Métrica de éxito para el próximo lote

Repetir el `VISUAL_QUALITY_GATE.md` sobre el próximo lote de piezas nuevas y confirmar mejora medible en Originalidad y Storytelling (hoy 7/10) sin sacrificar Conversión/legibilidad (hoy 8/10, no bajar de ahí).
