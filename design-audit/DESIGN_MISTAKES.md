# Design Mistakes — errores ya identificados, no repetir

Registro de errores técnicos y de diseño encontrados durante la revisión de piezas existentes. Revisar antes de construir o corregir una pieza nueva.

## Errores técnicos (rompen el render, no solo la estética)

1. **Clases CSS referenciadas en el HTML pero nunca definidas en `<style>`** (`.col-5`, `.col-7`, `.col-3`, `.col-12` faltantes) — causa overlap/corte de texto severo. Detectado en 4 piezas distintas del lote 2026-09-01 (`CarreraDeAnalisisDeDatos`, `GobiernoDatos`, `ISO8000`, `ProjectManager`). **Chequeo obligatorio antes de exportar:** diff de clases usadas en el body vs. clases definidas en el `<style>`.
2. **`backdrop-filter: blur()`** puede volver invisible contenido hijo (SVG y texto plano) en el pipeline de Chrome headless usado para exportar, de forma inconsistente entre archivos. **Evitarlo en este proyecto por completo**, no solo cuando falle.
3. **Overflow cerca del límite de 627px** puede causar que el primer hijo flex (ej. `<header>`) se renderice completamente invisible en el `--screenshot` de Chrome headless, pese a que `getBoundingClientRect()` reporte valores normales. Es un bug del pipeline de render, no del CSS. **Mitigación:** mantener contenido cómodamente por debajo de 627px y verificar siempre con una captura real, no solo con medición inyectada.
4. **`position: absolute` en el footer/firma** puede superponerse y ocultar contenido real si la pieza crece (visto en `PotenciaDashboardconIA.html` y `VejesDashboard.html`). Preferir flujo normal (`margin-top: auto` o similar) sobre posicionamiento absoluto para el footer salvo que el espacio disponible esté garantizado.
5. **`@import`/`<link>` a Google Fonts** dentro del HTML de una pieza — riesgo de fallo silencioso si el render headless no tiene red disponible en ese momento. Usar siempre system fonts / fallback local.

## Errores de diseño (rompen la calidad, no el render)

6. **Espacio vacío resuelto agrandando la fuente en vez de agregar contenido real** — ya prohibido explícitamente en `INFOGRAFIA-SPEC.md` ("Aprovechamiento del Espacio"), pero fue el error más recurrente de esta sesión antes de esa regla existir. Ver ejemplos corregidos en `GobiernoIA.html` (3 iteraciones hasta cumplir).
7. **`justify-content: space-between` en una tarjeta con contenido corto** — separa el contenido en extremos con un vacío enorme en el medio, en vez de agruparlo naturalmente arriba. Cambiar a `flex-start` + `gap` fijo cuando el contenido no llena la tarjeta.
8. **Grid con filas `1fr`/altura fija que no corresponde al contenido real** (`grid-template-rows: 270px 1fr` con contenido mucho más corto que 270px, o al revés) — genera huecos verticales grandes. Ajustar las proporciones de fila al contenido real antes de exportar, no dejarlas en valores heredados de una plantilla anterior.
9. **Barra de progreso / métrica visual sin fuente real detrás del ancho mostrado** — riesgo de fabricar precisión falsa. Si no hay una cifra real, usar una escala cualitativa (Bajo/Medio/Alto) o un indicador direccional sin pretensión de precisión numérica, nunca un porcentaje inventado.
10. **Reciclar la misma estructura de fondo (bento 2 columnas + fila de 5 tarjetas) entre piezas consecutivas del mismo tema** — detectado como patrón repetido entre 4 piezas de IA del lote 2026-09-01 (ver `VISUAL_QUALITY_GATE.md`). No es un error de render, pero sí de la regla "diseño arriesgado, no plantillado" — corregir en el próximo lote de ese tema.

11. **Describir la composición de una pieza de memoria en vez de releer el HTML final antes de auditar.** La primera versión de `VISUAL_LIBRARY.md` afirmó que 4 piezas de IA compartían el esqueleto "bento 2-columnas + 5-tarjetas"; al releer el HTML real antes de rediseñarlas, solo 1 de las 4 coincidía — las otras 3 ya tenían composiciones distintas (grid de 3 columnas con SVG+tabla, 3 tarjetas de autonomía, pipeline de 5 etapas). **Siempre releer el archivo final antes de escribir una entrada de `VISUAL_LIBRARY.md` o de decidir un rediseño — nunca describir de memoria o desde un resumen de sesión anterior.**
12. **Describir el contenido de una pieza en la metadata del catálogo sin releer el HTML final.** La metadata publicada de `flujos-trabajo-ia` describía "patrones de orquestación" (prompt chaining, routing, etc.) cuando el HTML real trataba de "niveles de autonomía" (No-Agente/Agente/Autónomo) — un tema relacionado pero distinto. Mismo origen que el error 11: confiar en memoria/resumen en vez de releer la fuente antes de escribir sobre ella.

## Soluciones ya descartadas (no volver a intentar sin una razón nueva)

- Rellenar espacio vacío únicamente con más íconos decorativos sin texto informativo — no resuelve el problema real (falta de contenido), solo lo disfraza. La solución validada es agregar una línea de contenido genuino (ver `DESIGN_PATTERNS.md`, micro-patrones de relleno).
