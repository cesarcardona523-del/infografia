# Design Patterns — biblioteca de patrones validados

Patrones ya probados en el repositorio que se pueden reutilizar como punto de partida (no como plantilla literal — adaptar al contenido). Complementa la sección "Riqueza Visual" de [INFOGRAFIA-SPEC.md](../INFOGRAFIA-SPEC.md); no la reemplaza.

## Metáforas de composición validadas

| Metáfora | Cuándo usarla | Ejemplo real |
|---|---|---|
| Tabla periódica (grid de categorías con sub-elementos) | Contenido = taxonomía cerrada de herramientas/conceptos agrupados por categoría, sin orden secuencial | `IA/tabla-periodica-herramientas-ia.html` |
| Comparación código incorrecto/correcto lado a lado | Contenido = errores comunes con su corrección, en cualquier lenguaje o configuración | `SQL/errores-comunes-group-by.html` |
| Ciclo de fases retroalimentado (círculos numerados en fila, última fase apunta a la primera) | Contenido = proceso continuo de gobierno/calidad, no un pipeline lineal con fin | `IA/gobierno-ia-responsable.html`, `Gobernanza_Tableros_BI/ciclo-vida-dashboard.html` |
| Pila de capas verticales (sidebar oscuro apilado) | Contenido = arquitectura en capas donde el orden importa (stack técnico) | `Bigdata/bigdata-grandes-empresas.html` |
| Pipeline horizontal con nodos + línea punteada de fondo | Contenido = flujo de datos con etapas discretas (ingesta → transformación → consumo) | `Arquitectura/blueprint-arquitectura-datos-contratos.html`, `Gobernanza_Tableros_BI/ciclo-vida-dashboard.html` |
| Niveles de madurez con "límite" explícito por nivel | Contenido = escalas de madurez organizacional | `Proyectos/niveles-madurez-gestion-proyectos.html` |

## Micro-patrones de relleno de espacio (técnica, no metáfora)

- **Línea "Ideal para:" / "En la práctica:" / "Resultado:"** con separador `border-top: 1px dashed` — añade una segunda capa de información genuina (no relleno decorativo) cuando una tarjeta queda corta de contenido. Usado en 10+ piezas del lote 2026-09-01.
- **Badge de frecuencia/cadencia** (`Mensual`, `Continuo`, `Antes de desplegar`) en tarjetas de proceso — comunica información real y ocupa espacio vertical sin inflar el texto principal. Validado en `gobierno-ia-responsable.html`.
- **Fila de tags de "También citadas"** para listas largas de ejemplos que no ameritan tarjeta propia — usado en `bigdata-grandes-empresas.html`.

## Convención de nombres de clase a converger (deuda pendiente, ver `DESIGN_SYSTEM_AUDIT.md`)

No hay una convención única todavía. Nombres observados para el mismo propósito visual:
- Badge/pill de metadato corto: `.tag`, `.badge`, `.pillar-freq`, `.cat-num`, `.elem-tag`
- Tarjeta base: `.card`, `.panel`, `.step-card`, `.category-card`

**Recomendación:** la próxima vez que se cree una pieza nueva, preferir `.tag` para badges cortos y `.card` para el contenedor base, salvo que el nombre semántico local sea más claro para ese HTML específico — no es obligatorio renombrar piezas existentes solo por consistencia (regla de "no gastar tiempo regenerando piezas que no ganan nada").
