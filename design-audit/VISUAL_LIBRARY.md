# Visual Library — registro de composición por pieza

Consultar **antes** de elegir la estructura visual de una pieza nueva (ver `IMAGE_FIRST_SYSTEM.md`). Cada entrada resume la pieza en términos de concepto visual, no de contenido — para eso ya existe `publicaciones.json`.

**Estado de cobertura:** sembrado con las 20 piezas procesadas el 2026-09-01 (todas las que este auditor construyó/revisó con detalle). Las 86 piezas previas del catálogo **no están registradas todavía** — se backfilling de forma incremental la próxima vez que se toque cada tema (mismo criterio de "no auditar todo de una sola vez" ya vigente en el proyecto), no en un barrido dedicado.

---

### PIECE_ID: power-bi-design-files-dashboards
**TITLE:** Power BI Design Files & Architecture
**TOPIC:** Power BI · diseño de dashboards
**VISUAL_CONCEPT:** Checklist editorial de 6 frentes técnicos
**COMPOSITION:** Grid 3×2 de tarjetas, cada una con lista de sub-ítems etiquetados (badge + descripción)
**DOMINANT_ELEMENT:** Los 6 títulos de panel numerados (jerarquía por número + ícono)
**COLOR_STRATEGY:** Verde base + acento tierra en panel 5 (Gobernanza)
**TYPOGRAPHY:** Estándar del proyecto, sin variación experimental
**LAYOUT:** Grid uniforme 3×2 — **patrón "grid de tarjetas" de referencia, no repetir sin variación en la próxima pieza de PowerBI**
**SIMILAR_PIECES:** matriz-habilidades-data-engineering (mismo concepto de checklist en grid)
**UNIQUENESS_SCORE:** 5/10 — funcional y denso, pero estructuralmente genérico frente al mapping de `IMAGE_FIRST_SYSTEM.md`

---

### PIECE_ID: blueprint-arquitectura-datos-contratos
**TITLE:** Blueprint de Arquitectura de Datos: Contratos y Confianza
**TOPIC:** Arquitectura de datos · data contracts
**VISUAL_CONCEPT:** Pipeline horizontal de 6 nodos con línea de flujo de fondo
**COMPOSITION:** Blueprint técnico — nodos conectados por línea punteada, panel de detalle inferior
**DOMINANT_ELEMENT:** La línea de flujo horizontal (Origen → Gold)
**COLOR_STRATEGY:** Verde+tierra (recoloreado desde una paleta azul/cian de "blueprint" fuera de sistema)
**TYPOGRAPHY:** Estándar
**LAYOUT:** Pipeline/Flow — alineado al Content→Visual Mapping para "Arquitectura"
**SIMILAR_PIECES:** ciclo-vida-dashboard (pipeline horizontal similar, tema distinto)
**UNIQUENESS_SCORE:** 7/10

---

### PIECE_ID: ruta-analista-datos
**TITLE:** Ruta de Carrera: De Cero a Analista de Datos
**TOPIC:** Roles · carrera profesional
**VISUAL_CONCEPT:** Journey de pasos progresivos con sub-habilidades
**COMPOSITION:** Secuencia vertical/horizontal de pasos con detalle expandido por paso
**DOMINANT_ELEMENT:** La numeración de pasos como columna vertebral
**COLOR_STRATEGY:** Verde base estándar
**TYPOGRAPHY:** Estándar
**LAYOUT:** Journey — mejora sobre la versión anterior de bullets planos (ver `AI_SLOP_REPORT.md`)
**SIMILAR_PIECES:** ruta-cientifico-datos-2026 (mismo concepto de journey, tema hermano — riesgo de similitud si se comparan directamente)
**UNIQUENESS_SCORE:** 6/10 — bueno en sí mismo, pero comparte estructura casi 1:1 con su pieza hermana

---

### PIECE_ID: ruta-cientifico-datos-2026
**TITLE:** Ruta de Carrera: Científico de Datos 2026
**TOPIC:** Roles · carrera profesional
**VISUAL_CONCEPT:** Journey de pasos + flujo de progresión resumido al final
**COMPOSITION:** Secuencia de pasos + diagrama de 5 nodos circulares conectados por flechas al cierre
**DOMINANT_ELEMENT:** El flujo circular de cierre (Fundamentos→ML→IA Generativa→Negocio)
**COLOR_STRATEGY:** Verde base, acento tierra en el nodo de IA Generativa
**TYPOGRAPHY:** Estándar
**LAYOUT:** Journey + Progression combinados
**SIMILAR_PIECES:** ruta-analista-datos (ver nota arriba)
**UNIQUENESS_SCORE:** 6/10

---

### PIECE_ID: arquitectura-claude-code
**TITLE:** Arquitectura de Claude Code: Cómo Funciona el CLI de Anthropic
**TOPIC:** IA · Claude · herramientas de desarrollo
**VISUAL_CONCEPT:** Diagrama de sistema (bucle agéntico) + flujo de sesión
**COMPOSITION:** Bloques de arquitectura + secuencia de flujo típico
**DOMINANT_ELEMENT:** El diagrama del ciclo leer-planificar-ejecutar-verificar
**COLOR_STRATEGY:** Verde base
**TYPOGRAPHY:** Bloques de código con syntax highlighting
**LAYOUT:** System diagram — alineado al mapping para contenido de arquitectura
**SIMILAR_PIECES:** ninguna directa en el tema Claude
**UNIQUENESS_SCORE:** 7/10

---

### PIECE_ID: matriz-habilidades-data-engineering
**TITLE:** Matriz de Habilidades: Data Engineering
**TOPIC:** Ingeniería de datos · roles
**VISUAL_CONCEPT:** Matriz de 9 bloques de habilidad con justificación
**COMPOSITION:** Grid uniforme de 9 tarjetas
**DOMINANT_ELEMENT:** Ninguno marcado — los 9 bloques pesan igual
**COLOR_STRATEGY:** Verde base
**TYPOGRAPHY:** Estándar
**LAYOUT:** Grid uniforme — **candidato a rediseño la próxima vez que se toque este tema; no tiene visual hero claro (falla el Thumbnail Test de `IMAGE_FIRST_SYSTEM.md`)**
**SIMILAR_PIECES:** power-bi-design-files-dashboards (mismo patrón de grid-checklist)
**UNIQUENESS_SCORE:** 4/10 — el más genérico del lote 2026-09-01

---

### PIECE_ID: datos-faltantes-tecnicas
**TITLE:** Datos Faltantes: Técnicas de Diagnóstico e Imputación
**TOPIC:** Ciencia de datos · estadística
**VISUAL_CONCEPT:** 6 paneles temáticos con listas de técnica
**COMPOSITION:** Grid 3×2 de paneles con `.item-row` repetidos
**DOMINANT_ELEMENT:** No hay un elemento dominante único — información distribuida uniformemente
**COLOR_STRATEGY:** Verde base
**TYPOGRAPHY:** Estándar
**LAYOUT:** Grid de paneles — mismo riesgo que matriz-habilidades-data-engineering
**SIMILAR_PIECES:** matriz-habilidades-data-engineering, power-bi-design-files-dashboards
**UNIQUENESS_SCORE:** 4/10

---

### PIECE_ID: errores-comunes-group-by
**TITLE:** 6 Errores Comunes con GROUP BY en SQL
**TOPIC:** SQL
**VISUAL_CONCEPT:** Comparación binaria código incorrecto/correcto
**COMPOSITION:** 6 filas, cada una con número + descripción + 2 bloques de código enfrentados (rojo/verde)
**DOMINANT_ELEMENT:** El contraste rojo/verde de cada par de código
**COLOR_STRATEGY:** Verde base + rojo/verde semántico dentro de las filas (única excepción de color con propósito funcional, no decorativo)
**TYPOGRAPHY:** Monoespaciada para código, alto contraste
**LAYOUT:** Split composition / Before-After — **patrón de referencia para reutilizar en otros temas con contraste binario**
**SIMILAR_PIECES:** 7-trucos-sql-optimizacion (mismo tema, estructura distinta — bien diferenciado)
**UNIQUENESS_SCORE:** 8/10 — el mejor del lote en Originalidad + Topic Relevance

---

### PIECE_ID: evolucion-ingenieria-ia
**TITLE:** La Evolución de la Ingeniería de IA
**TOPIC:** IA
**VISUAL_CONCEPT:** Timeline de eras con rasgos distintivos
**COMPOSITION:** Bento 2 columnas superior + fila de 5 tarjetas inferior
**DOMINANT_ELEMENT:** No claramente definido — compite con el resto de piezas de IA del lote
**COLOR_STRATEGY:** Verde base
**TYPOGRAPHY:** Estándar
**LAYOUT:** Bento 2-col + 5-cards — **estructura repetida 4 veces en este lote (ver abajo), marcada como prioridad de corrección en `DESIGN_EVOLUTION_PLAN.md`**
**SIMILAR_PIECES:** flujos-trabajo-ia, gobierno-ia-responsable, inteligencia-negocios-con-ia (alto Repetition Score entre las 4, estimado >60%)
**UNIQUENESS_SCORE:** 5/10

---

### PIECE_ID: flujos-trabajo-ia
**TITLE:** Flujos de Trabajo con IA: Patrones de Orquestación
**TOPIC:** IA
**VISUAL_CONCEPT:** Catálogo de patrones de orquestación
**COMPOSITION:** Bento 2 columnas + fila inferior
**DOMINANT_ELEMENT:** No definido
**COLOR_STRATEGY:** Verde base
**TYPOGRAPHY:** Estándar
**LAYOUT:** Bento 2-col + 5-cards (repetido, ver arriba)
**SIMILAR_PIECES:** evolucion-ingenieria-ia, gobierno-ia-responsable, inteligencia-negocios-con-ia
**UNIQUENESS_SCORE:** 5/10

---

### PIECE_ID: capas-gobierno-datos
**TITLE:** Las Capas del Gobierno de Datos
**TOPIC:** Gobierno de datos
**VISUAL_CONCEPT:** Capas jerárquicas de gobierno
**COMPOSITION:** Grid de capas con propósito + resultado esperado
**DOMINANT_ELEMENT:** No fuertemente definido
**COLOR_STRATEGY:** Verde base
**TYPOGRAPHY:** Estándar
**LAYOUT:** Layers — coherente con el mapping para gobierno/arquitectura, pero ejecutado como grid plano en vez de composición apilada real
**SIMILAR_PIECES:** ninguna directa
**UNIQUENESS_SCORE:** 5/10

---

### PIECE_ID: gobierno-ia-responsable
**TITLE:** Cómo Definir el Gobierno de IA
**TOPIC:** IA · gobierno
**VISUAL_CONCEPT:** 2 pilares + ciclo de 5 fases retroalimentado
**COMPOSITION:** Bento 2 columnas superior (pilares) + fila de 5 círculos numerados con badge de cadencia
**DOMINANT_ELEMENT:** El ciclo de 5 fases con badges de frecuencia (Mensual/Continuo/etc.)
**COLOR_STRATEGY:** Verde + acento tierra en pilar 2
**TYPOGRAPHY:** Estándar
**LAYOUT:** Bento 2-col + ciclo retroalimentado — mismo esqueleto que evolucion-ingenieria-ia/flujos-trabajo-ia, pero el badge de cadencia le da un elemento dominante más claro que sus pares
**SIMILAR_PIECES:** evolucion-ingenieria-ia, flujos-trabajo-ia, inteligencia-negocios-con-ia
**UNIQUENESS_SCORE:** 6/10 — el mejor ejecutado de las 4 piezas bento-IA, pero sigue compartiendo esqueleto

---

### PIECE_ID: iso-8000-calidad-datos
**TITLE:** ISO 8000: Las Dimensiones de la Calidad de Datos
**TOPIC:** Gobierno de datos · calidad
**VISUAL_CONCEPT:** Dimensiones de calidad con definición + ejemplo de medición
**COMPOSITION:** Filas con `grid-template-rows` desiguales por dimensión
**DOMINANT_ELEMENT:** No definido con fuerza
**COLOR_STRATEGY:** Verde base
**TYPOGRAPHY:** Estándar
**LAYOUT:** Matrix/lista estructurada
**SIMILAR_PIECES:** iso-9001-vs-business-intelligence (mismo tema ISO, estructura de comparación distinta — bien diferenciado)
**UNIQUENESS_SCORE:** 5/10

---

### PIECE_ID: iso-9001-vs-business-intelligence
**TITLE:** ISO 9001 y Business Intelligence: Paralelos de Gestión de Calidad
**TOPIC:** Gobierno de datos · calidad · BI
**VISUAL_CONCEPT:** Comparación de principio ISO 9001 ↔ equivalente en BI
**COMPOSITION:** Pares enfrentados por principio + resumen de síntesis final
**DOMINANT_ELEMENT:** El paralelo explícito principio↔equivalente
**COLOR_STRATEGY:** Verde base
**TYPOGRAPHY:** Estándar
**LAYOUT:** Split composition / comparación — buen uso del mapping para "Comparaciones"
**SIMILAR_PIECES:** errores-comunes-group-by (mismo espíritu de comparación binaria, tema distinto)
**UNIQUENESS_SCORE:** 7/10

---

### PIECE_ID: inteligencia-negocios-con-ia
**TITLE:** Inteligencia de Negocios con IA: El Pipeline de Valor
**TOPIC:** IA · BI
**VISUAL_CONCEPT:** Pipeline de 5 etapas (Data→Govern→Trust→Intelligence→Value)
**COMPOSITION:** Fila de 5 tarjetas de etapa (pipeline-grid)
**DOMINANT_ELEMENT:** La secuencia de 5 etapas en sí
**COLOR_STRATEGY:** Verde base
**TYPOGRAPHY:** Estándar
**LAYOUT:** Pipeline horizontal — más cercano al mapping correcto que sus 3 pares de IA del lote, pero visualmente similar en tratamiento de tarjeta
**SIMILAR_PIECES:** evolucion-ingenieria-ia, flujos-trabajo-ia, gobierno-ia-responsable
**UNIQUENESS_SCORE:** 6/10

---

### PIECE_ID: potenciar-dashboards-con-ia
**TITLE:** Cómo la IA Potencia el Diseño de Dashboards
**TOPIC:** IA · dashboards
**VISUAL_CONCEPT:** 5 pasos del flujo de construcción de dashboard asistido por IA
**COMPOSITION:** Timeline horizontal (pipeline-track) + 2 paneles inferiores (código + features)
**DOMINANT_ELEMENT:** El timeline de 5 pasos con línea punteada
**COLOR_STRATEGY:** Verde base
**TYPOGRAPHY:** Bloque de código JSON con syntax highlighting
**LAYOUT:** Timeline + paneles — buena combinación, no repite el esqueleto bento-2col de las otras piezas de IA
**SIMILAR_PIECES:** ninguna directa (estructura distinguida dentro del lote)
**UNIQUENESS_SCORE:** 7/10

---

### PIECE_ID: niveles-madurez-gestion-proyectos
**TITLE:** Niveles de Madurez en Gestión de Proyectos
**TOPIC:** Profesión · gestión de proyectos
**VISUAL_CONCEPT:** 3 niveles de madurez con límite explícito + 5 fases del ciclo de vida
**COMPOSITION:** 3 tarjetas de nivel + fila de 5 fases
**DOMINANT_ELEMENT:** Los 3 niveles de madurez como progresión central
**COLOR_STRATEGY:** Verde base
**TYPOGRAPHY:** Estándar
**LAYOUT:** Progression — alineado al mapping para "Evolución"
**SIMILAR_PIECES:** ninguna directa
**UNIQUENESS_SCORE:** 6/10

---

### PIECE_ID: tabla-periodica-herramientas-ia
**TITLE:** Tabla Periódica de Herramientas de IA para Negocios
**TOPIC:** IA · herramientas empresariales
**VISUAL_CONCEPT:** Metáfora de tabla periódica — 6 categorías × 3 herramientas
**COMPOSITION:** Grid de 6 categorías, cada una con 3 "elementos" (símbolo + nombre + tag + descripción + caso de uso)
**DOMINANT_ELEMENT:** La metáfora de tabla periódica en sí (símbolo de 2-3 letras por herramienta)
**COLOR_STRATEGY:** Verde + acento tierra en categoría "Ingeniería de Software"
**TYPOGRAPHY:** Monoespaciada para los símbolos, estándar para el resto
**LAYOUT:** Central metaphor / Ecosystem — el más fuerte del lote en Originalidad
**SIMILAR_PIECES:** ninguna en el catálogo — metáfora inédita
**UNIQUENESS_SCORE:** 9/10 — mejor pieza del lote 2026-09-01 en el eje de originalidad

---

### PIECE_ID: 7-trucos-sql-optimizacion
**TITLE:** 7 Trucos SQL para Código Óptimo
**TOPIC:** SQL
**VISUAL_CONCEPT:** 7 tarjetas técnica + código + tarjeta de resumen de impacto con barras
**COMPOSITION:** Grid 4×2 con 1 tarjeta de resumen visual (barras direccionales)
**DOMINANT_ELEMENT:** La tarjeta de resumen de impacto (única con fondo oscuro, contraste fuerte)
**COLOR_STRATEGY:** Verde base + tarjeta resumen en verde oscuro sólido
**TYPOGRAPHY:** Código monoespaciado con syntax highlighting completo
**LAYOUT:** Grid + data visualization combinados — bien ejecutado, aunque la estructura de grid en sí es convencional
**SIMILAR_PIECES:** errores-comunes-group-by (mismo tema, tratamiento distinto — bien diferenciado)
**UNIQUENESS_SCORE:** 7/10

---

### PIECE_ID: ciclo-vida-dashboard
**TITLE:** El Ciclo de Vida de un Dashboard
**TOPIC:** Gobierno de datos · dashboards
**VISUAL_CONCEPT:** Pipeline de 5 fases + panel de impacto + panel de metadata (código)
**COMPOSITION:** Timeline horizontal de 5 fases + 2 paneles inferiores
**DOMINANT_ELEMENT:** El timeline de 5 fases con línea punteada de fondo
**COLOR_STRATEGY:** Verde base, última fase en acento tierra (Retirar)
**TYPOGRAPHY:** Bloque de código JSON de metadata de gobierno
**LAYOUT:** Timeline + paneles — mismo esqueleto que potenciar-dashboards-con-ia (ambos: timeline + 2 paneles inferiores)
**SIMILAR_PIECES:** potenciar-dashboards-con-ia (Repetition Score moderado — misma estructura general, contenido y color de énfasis distintos)
**UNIQUENESS_SCORE:** 6/10

---

## Lectura agregada del lote 2026-09-01

- **Estructura más repetida:** Bento 2-columnas + fila de 5 tarjetas — 4 ocurrencias (`evolucion-ingenieria-ia`, `flujos-trabajo-ia`, `gobierno-ia-responsable`, `inteligencia-negocios-con-ia`). Todas del tema IA, todas construidas en la misma sesión — el caso de manual más claro de por qué existe la regla de Repetition Score.
- **Segunda estructura más repetida:** Timeline horizontal + 2 paneles inferiores — 2 ocurrencias (`potenciar-dashboards-con-ia`, `ciclo-vida-dashboard`).
- **Mejor pieza en Originalidad:** `tabla-periodica-herramientas-ia` (9/10) — única con una metáfora central inédita en todo el catálogo conocido.
- **Peor pieza en Originalidad:** `matriz-habilidades-data-engineering` (4/10) — grid uniforme sin visual hero, candidata a rediseño futuro si se vuelve a tocar ese tema.
