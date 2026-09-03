# Reference-Based Redesign — sistema de trabajo con imagen de referencia + Markdown

> Adoptado 2026-09-01. Se aplica cada vez que el usuario entrega **una imagen de referencia visual + el contenido en Markdown** de una infografía (nueva o existente) para que ese par gobierne el rediseño. Complementa — no reemplaza — [IMAGE_FIRST_SYSTEM.md](IMAGE_FIRST_SYSTEM.md) y [INFOGRAFIA-SPEC.md](../INFOGRAFIA-SPEC.md).

## Principio fundamental

La imagen de referencia **nunca** es una plantilla para copiar ni una fuente de contenido, color, dimensiones o tipografía exacta. Solo representa un modelo de:

- Organización visual y jerarquización de la información
- Distribución de bloques y ritmo de lectura
- Balance visual, escalado tipográfico y agrupación de elementos

**Se extrae la lógica de diseño, nunca el diseño literal.** El color, la tipografía exacta y el branding siguen las reglas ya vigentes del proyecto (paleta verde+tierra por defecto, o colores de marca por aplicación cuando corresponda — ver CLAUDE.md).

## Restricción crítica 1 — el lienzo no se toca

El canvas del proyecto ya está fijo (1200×627px, ver INFOGRAFIA-SPEC.md). Prohibido: cambiar width/height/aspect-ratio, crear múltiples páginas o imágenes, generar scroll vertical u horizontal, o dejar contenido fuera del viewport. **Se adapta el diseño al contenido — nunca el contenido al diseño.**

## Restricción crítica 2 — no se elimina información

Todo el contenido presente en el Markdown de origen debe permanecer: cifras, ejemplos, citas, fuentes, notas, referencias, llamados de atención. Prohibido resumir, condensar u omitir para que quepa — si no cabe, se resuelve por el sistema de rebalanceo (abajo), nunca cortando contenido.

## Proceso obligatorio antes de escribir HTML

1. **Análisis** — contar secciones, métricas, cifras, gráficos, insights, referencias; identificar contenido principal / secundario / de soporte / crítico.
2. **Jerarquización** en 4 niveles:
   - Nivel 1 — atención inmediata (título, hallazgo principal, resultado principal)
   - Nivel 2 — estratégico (subtítulos, KPIs, estadísticas clave)
   - Nivel 3 — explicativo (descripciones, metodología, contexto)
   - Nivel 4 — complementario (notas, referencias, bibliografía)
3. **Composición por zonas** (adaptando la lógica de la referencia, no su literalidad):
   - Zona 1 — Encabezado: categoría, autor, fecha, etiquetas — poco espacio
   - Zona 2 — Hero principal: título + mensaje/insight principal — foco visual dominante
   - Zona 3 — Resumen ejecutivo: tarjetas/KPIs/indicadores en fila horizontal
   - Zona 4 — Desarrollo: grid/cards/comparaciones a todo el ancho disponible
   - Zona 5 — Insights: bloques destacados para hallazgos, recomendaciones, riesgos u oportunidades
   - Zona 6 — Cierre: conclusiones, referencias, fuentes, firma/CTA

## Aprovechamiento del espacio

La composición debe ocupar entre 90% y 98% del canvas, sin zonas muertas ni columnas angostas innecesarias — resultado compacto, editorial, ejecutivo. Esto es una versión más estricta de la sección "Aprovechamiento del Espacio" ya existente en INFOGRAFIA-SPEC.md; cuando ambas aplican, rige el umbral más exigente (90-98%).

## Sistema de rebalanceo automático

Si el contenido no cabe, ajustar **en este orden**: 1) grid/número de columnas, 2) padding, 3) gaps, 4) tamaño de tarjetas, 5) tamaños tipográficos secundarios, 6) espaciados internos. **Nunca**: eliminar u ocultar contenido, bajar opacidad, o dejar contenido fuera del canvas.

## Iconografía obligatoria

Cada bloque debe tener apoyo visual (SVG inline, iconos contextuales, badges, chips, separadores) — la pieza nunca es solo texto. Si hay mucho texto en una sección, convertirlo en tarjetas/grid/callouts/listas visuales escaneables en vez de párrafos largos.

## Checklist de validación antes de entregar

- [ ] Todo el contenido del Markdown de origen está presente
- [ ] Sin scroll vertical ni horizontal, nada fuera del canvas
- [ ] Sin superposiciones ni textos cortados/truncados
- [ ] ≥90% de ocupación del espacio disponible
- [ ] Jerarquía visual clara (los 4 niveles se distinguen a simple vista)
- [ ] Apoyo visual en cada bloque (no solo texto)
- [ ] La distribución sigue la lógica estructural de la referencia (no su literalidad)
- [ ] Colores y tipografía siguen las reglas del proyecto (verde+tierra o marca de aplicación), no los de la imagen de referencia

## Alcance de aplicación (definido por el usuario, 2026-09-01)

Se usa **de aquí en adelante** para: (a) las piezas todavía pendientes de este batch de revisión, y (b) toda infografía nueva que se construya — no está atado a una pieza puntual. Cuando el usuario entregue una imagen de referencia sin Markdown adjunto, o sin indicar a qué pieza aplica, preguntar antes de proceder (ver ejemplo de esta misma sesión).
