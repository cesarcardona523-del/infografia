# Design History — hitos de evolución del sistema visual

Bitácora de decisiones de diseño, en orden cronológico, que cambiaron el estándar del proyecto. Actualizar cada vez que una mejora se generaliza a `INFOGRAFIA-SPEC.md` o a la práctica del proyecto.

## 2026-07 — Fundación

- Definición inicial de `INFOGRAFIA-SPEC.md`: paleta verde+tierra, tipografía, tamaño fijo 1200×627px, branding y firma personal.
- Primer lote grande de piezas (`Cultura_Datos`, 19 piezas) — establece el vocabulario visual base pero con patrones ahora identificados como genéricos (ver `AI_SLOP_REPORT.md`).

## Antes de 2026-09-01 — Excepción de paleta arriesgada

- Se documenta en `INFOGRAFIA-SPEC.md` la excepción que permite una paleta secundaria distinta (una vez por tema, un solo color de familia distinto) para diferenciar piezas del mismo tema entre sí.

## 2026-09-01 — Sección "Aprovechamiento del Espacio"

- Se agrega a `INFOGRAFIA-SPEC.md` la regla explícita contra espacios vacíos >30-40% de una tarjeta, con el ajuste de tipografía como último recurso, no primera respuesta. Motivada por corrección repetida de piezas con huecos visuales durante la revisión del lote `HTML/`.

## 2026-09-01 — Lote de 20 HTML consolidado (flujo alterno)

- Se procesaron 20 piezas entregadas ya resueltas en `HTML/` (flujo alterno de CLAUDE.md): revisión de paleta, corrección de bugs de CSS, verificación de overflow, exportación y publicación.
- Se descubrieron y documentaron 2 bugs de pipeline no conocidos previamente: overflow que oculta el header en Chrome headless cerca del límite de 627px, y `backdrop-filter: blur()` que puede volver invisible contenido hijo (ver `DESIGN_MISTAKES.md` #2-3).
- 1 consolidación real: `PowerBiDesing.html` resultó ser el mismo tópico que una pieza ya publicada (`power-bi-design-files-dashboards`) — se actualizó in-place en vez de duplicar, con archivado de la versión anterior.
- Se creó `design-audit/` como carpeta de auditoría continua (este documento y sus pares), a pedido explícito de una auditoría de diseño estilo Atelier/Claude Banana adaptada al formato real del proyecto (piezas estáticas, no producto React).

## Próximo hito pendiente (ver `DESIGN_EVOLUTION_PLAN.md`)

- Diferenciar más la estructura de fondo entre piezas consecutivas de un mismo tema (detectado: 4 piezas de IA del lote 2026-09-01 comparten estructura bento 2-columnas + 5-tarjetas).
