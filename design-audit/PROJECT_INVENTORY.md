# Project Inventory — infografia

> Nota de alcance: este repositorio **no** es un producto React/Tailwind con design system compartido. Es una fábrica de piezas estáticas 1200×627px (HTML+CSS → PNG vía Chrome headless), una por infografía, sin runtime ni componentes compartidos en tiempo de ejecución. Las 11 fases del framework original (React/TS/Tailwind, wireframes de sitemap, etc.) se adaptan aquí a lo que el proyecto realmente es — ver [CLAUDE.md](../CLAUDE.md).

## Cifras generales (2026-09-01)

- **106 piezas** publicadas en 28 carpetas `Construidos/<Tema>/`.
- Fuente de verdad de diseño: [INFOGRAFIA-SPEC.md](../INFOGRAFIA-SPEC.md) (brief visual) + [INFOGRAFIA-INVESTIGAR.md](../INFOGRAFIA-INVESTIGAR.md) (metadata).
- Paleta fija: verde (`--primary` / `--primary-dark`) + un acento tierra/ámbar, con excepción documentada de paleta arriesgada por pieza.
- Sin librería de componentes compartida — cada HTML repite (o reinventa) sus propias clases `.card`, `.badge`, `.kpi`, etc.

## Inventario por Tema

| Tema | Piezas | Antigüedad relativa | Observación de calidad visual |
|---|---|---|---|
| Cultura_Datos | 19 | Antigua (lote fundacional) | Mezcla de piezas muy genéricas (grid de 5 iconos + flechas, ver `AI_SLOP_REPORT`) con algunas más trabajadas. Es el tema con más deuda visual. |
| IA | 12 | Mixta (fundacional + hoy) | Fuerte salto de calidad entre las piezas antiguas (`terminos-ia`, `finalidades-de-las-ia`) y las de hoy (`tabla-periodica-herramientas-ia`, `gobierno-ia-responsable`), que usan metáforas visuales concretas en vez de grids genéricos. |
| Arquitectura | 10 | Mixta | Buen uso de diagramas de flujo reales (medallón, AWS/Azure/GCP). Es el tema con mejor aprovechamiento de diagramación real vs. tarjetas. |
| Escuela_IA | 7 | Media | Serie con identidad consistente (marca Uniremington), buena disciplina de plantilla educativa. |
| Claude | 6 | Reciente | Buen nivel técnico (árbol de modelos, stack), coherente con el tema. |
| SQL | 5 | Mixta | Piezas de hoy (`errores-comunes-group-by`, `7-trucos-sql-optimizacion`) usan comparación código incorrecto/correcto lado a lado — patrón fuerte, digno de reutilizar. |
| Roles | 5 | Mixta | Las 2 rutas de carrera nuevas usan flujo de pasos con "por qué importa" — mejor que las 3 piezas antiguas de solo bullets. |
| Bigdata | 4 | Antigua | Buen uso de sidebar oscuro tipo pila de capas + casos reales con cifra grande (`bigdata-grandes-empresas`), pero paleta ámbar/marrón se aleja del verde base — revisar consistencia. |
| Excel | 4 | Antigua | No auditada en profundidad esta pasada — candidata a revisión futura. |
| Automatización, Calidad_Datos_Gobierno, Dashboard, Gobernanza_Tableros_BI, Gobierno_de_Datos, Proyectos, PowerBI | 2–3 c/u | Mixta | Temas donde el lote de hoy (ISO 8000/9001, ciclo de vida de dashboard, madurez de proyectos) eleva notablemente el promedio del tema. |
| Adopcion_IA, BI, Base_de_Datos, ChatGPT, Ciencia_Datos, Comparacion_Herramientas_IA_Desarrollo, Data_Engineering, Data_Governance_MDM, Docencia, Estrategia_de_Datos, Liderazgo, Metricas_Modelos_IA, Modelos | 1 c/u | Mixta | Temas de una sola pieza — no hay aún patrón de tema que auditar, cada uno es su propio precedente. |

## Artefactos de proceso (no piezas finales)

| Artefacto | Objetivo | Estado |
|---|---|---|
| `INFOGRAFIA-SPEC.md` | Design system vivo (paleta, tipografía, composición, "Riqueza Visual", "Aprovechamiento del Espacio") | Activo, evoluciona con cada mejora generalizable |
| `INFOGRAFIA-INVESTIGAR.md` | Prompt de generación de metadata JSON desde imagen de referencia | Activo, no se toca por tema puntual |
| `taxonomia.json` | Taxonomía cerrada de categorías/temas/tipos | Activo, gobernanza exclusiva del usuario |
| `publicaciones.json` | Catálogo incremental de metadata (105 entradas) | Activo |
| `Construidos/<Tema>/Archivadas/` | Versiones previas de piezas consolidadas | 1 entrada archivada (`power-bi-design-files-dashboards`) |
| `HTML/` | Carpeta de intake para piezas entregadas ya resueltas (flujo alterno) | Vaciada hoy — 20 piezas procesadas y movidas a `Construidos/` |

## Dependencias transversales detectadas

- Todas las piezas comparten el mismo signature block (LinkedIn + `cacm523`) — repetido literalmente en cada HTML, sin componente compartido. Es la única "consistencia de marca" garantizada estructuralmente hoy.
- El pipeline de export (Chrome headless 2x + crop PIL en offset fijo `(64,64)`/`(2400,1254)`) asume `padding: 32px` en `.canvas` — cualquier pieza que cambie ese padding sin ajustar el offset produce un crop incorrecto. Es la dependencia técnica más frágil del proyecto.
- No existe un linter ni test automatizado que valide paleta, overflow o clases CSS huérfanas — toda la auditoría de calidad depende hoy de revisión visual manual (ver hallazgos recurrentes en `DESIGN_MISTAKES.md`).
