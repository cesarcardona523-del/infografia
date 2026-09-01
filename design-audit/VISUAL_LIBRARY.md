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

### PIECE_ID: evolucion-ingenieria-ia [REDISEÑADA 2026-09-01]
**TITLE:** Evolución de la Ingeniería de IA: Prompt → Loop → Graph
**TOPIC:** IA
**VISUAL_CONCEPT:** 3 paradigmas con mini-diagrama SVG propio + matriz comparativa
**COMPOSITION:** Grid de 3 columnas iguales, cada una con diagrama de nodos SVG, ejemplo real y riesgo de omitirla; matriz comparativa de 3×3 debajo
**DOMINANT_ELEMENT:** Los 3 mini-diagramas SVG (Prompt→Respuesta / Agente en bucle / Router→Agentes)
**COLOR_STRATEGY:** Verde base, tercera columna en acento tierra
**TYPOGRAPHY:** Estándar + monoespaciada en la matriz
**LAYOUT:** System diagram + comparison matrix — **corrección de auditoría previa: NO era bento, ya era distinta de las otras 3; se corrigió un bug real (texto SVG con stroke heredado ilegible) y el espacio vacío bajo cada columna con líneas de "Ejemplo real" y "Riesgo de saltarla"**
**SIMILAR_PIECES:** ninguna directa tras la corrección
**UNIQUENESS_SCORE:** 7/10 (subió de 5 tras el rediseño)

---

### PIECE_ID: flujos-trabajo-ia [REDISEÑADA 2026-09-01]
**TITLE:** Evolución de Flujos de IA (No-Agente → Agente → Sistemas Autónomos)
**TOPIC:** IA
**VISUAL_CONCEPT:** Escalera ascendente de autonomía
**COMPOSITION:** 3 tarjetas de ancho y tamaño creciente (0.78fr/1fr/1.3fr), alineadas al final (bottom) con línea base degradada verde→ámbar
**DOMINANT_ELEMENT:** La tarjeta 3 ("Sistemas Autónomos"), notablemente más grande y en acento — jerarquía por tamaño, no por posición
**COLOR_STRATEGY:** Verde base, tercera tarjeta en acento tierra con mayor peso tipográfico
**TYPOGRAPHY:** Escala progresiva (10.5px→13px) según nivel de autonomía — tipografía como jerarquía real, no decorativa
**LAYOUT:** Asymmetric composition / Progression — **corrección de auditoría previa: el contenido real es progresión de autonomía (No-Agente/Agente/Autónomo), no "patrones de orquestación" (la metadata del catálogo tenía ese error y fue corregida); rediseñada de 3 columnas iguales a escalera ascendente asimétrica**
**SIMILAR_PIECES:** ninguna directa
**UNIQUENESS_SCORE:** 8/10 (subió de 5 tras el rediseño — la más distintiva del lote junto con tabla-periodica-herramientas-ia)

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

### PIECE_ID: gobierno-ia-responsable [REDISEÑADA 2026-09-01]
**TITLE:** Cómo Definir el Gobierno de IA
**TOPIC:** IA · gobierno
**VISUAL_CONCEPT:** Dos pilares arquitectónicos literales + ciclo radial de 5 fases
**COMPOSITION:** Asimétrica: columna izquierda (39%) con 2 "pilares" apilados (franja tipo capitel arriba, tags de área abajo) + columna derecha (61%) con diagrama radial SVG (círculo con 5 nodos numerados, flechas de flujo clockwise, centro "Gobierno Continuo") y su leyenda de 2×3
**DOMINANT_ELEMENT:** El diagrama radial — único elemento circular de todo el catálogo de IA, visual hero inequívoco
**COLOR_STRATEGY:** Verde + acento tierra en pilar 2 y nodo 5
**TYPOGRAPHY:** Estándar
**LAYOUT:** Central metaphor (arquitectura) + Radial diagram — **era la única pieza realmente bento del lote; rediseñada por completo, ya no comparte esqueleto con ninguna otra pieza de IA**
**SIMILAR_PIECES:** ninguna
**UNIQUENESS_SCORE:** 9/10 (subió de 6 tras el rediseño — empata con tabla-periodica-herramientas-ia como la más original del catálogo de IA)

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

### PIECE_ID: inteligencia-negocios-con-ia [REDISEÑADA 2026-09-01]
**TITLE:** De los Datos a la Inteligencia que Genera Valor
**TOPIC:** IA · BI
**VISUAL_CONCEPT:** Escalera ascendente de 5 etapas + barras de "acumulación de valor" alineadas
**COMPOSITION:** 5 columnas de ancho y tipografía crecientes (Data más pequeña → Value más grande y en acento), cada una con una barra de progreso horizontal al pie (20%→100%) que en conjunto forman un mini-gráfico de barras ascendente unificado
**DOMINANT_ELEMENT:** La fila de barras "Acumulación de Valor" al pie — convierte 5 tarjetas sueltas en un solo gráfico de lectura horizontal
**COLOR_STRATEGY:** Verde base, última barra y tarjeta en acento tierra
**TYPOGRAPHY:** Escala progresiva (8.3px→15px) siguiendo el crecimiento de la etapa
**LAYOUT:** Asymmetric composition + data visualization — **ya no comparte tratamiento uniforme de tarjeta con las demás; la fila de barras es un elemento de dataviz genuino, no decorativo**
**SIMILAR_PIECES:** flujos-trabajo-ia (comparten la técnica de "escalera ascendente", pero aplicada a 3 vs. 5 elementos y con dataviz añadido aquí — variación aceptable, no plantilla idéntica)
**UNIQUENESS_SCORE:** 8/10 (subió de 6 tras el rediseño)

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

- **Corrección de auditoría (2026-09-01, segunda pasada):** la primera versión de este documento afirmaba que 4 piezas de IA compartían un esqueleto "bento 2-columnas + 5-tarjetas". Al releer el HTML real antes de rediseñar, solo `gobierno-ia-responsable` coincidía con esa descripción — `evolucion-ingenieria-ia` ya era un grid de 3 columnas con diagramas SVG + tabla comparativa, y `flujos-trabajo-ia` ya eran 3 tarjetas verticales de nivel de autonomía. El error quedó documentado en `DESIGN_MISTAKES.md` como lección: describir composición de memoria en vez de releer el archivo final es exactamente el tipo de fallo que este sistema existe para prevenir.
- **Las 4 piezas fueron rediseñadas igualmente**, no solo por la repetición real sino porque las 4 tenían espacio vacío significativo (>30% de card) y en 2 casos (`evolucion-ingenieria-ia`, `flujos-trabajo-ia`) también un error de metadata/contenido real. Resultado: Uniqueness Score subió en las 4 (5→7, 5→8, 6→9, 6→8).
- **Técnica compartida entre `flujos-trabajo-ia` e `inteligencia-negocios-con-ia`:** ambas usan "escalera ascendente" (columnas de ancho/tipografía creciente, alineadas al mismo baseline). Es una variación deliberada de la misma técnica aplicada a contenidos distintos (3 niveles de autonomía vs. 5 etapas con dataviz de barras) — vigilar que una tercera pieza futura no la use por defecto sin justificación, o pasaría a ser plantilla.
- **Mejor pieza en Originalidad tras el rediseño:** `gobierno-ia-responsable` (9/10, diagrama radial) empata con `tabla-periodica-herramientas-ia` (9/10, metáfora de tabla periódica) como las más distintivas del catálogo de IA.
- **Peor pieza en Originalidad (sin cambios, fuera de alcance de este rediseño):** `matriz-habilidades-data-engineering` (4/10) — grid uniforme sin visual hero, candidata a rediseño futuro si se vuelve a tocar ese tema.
