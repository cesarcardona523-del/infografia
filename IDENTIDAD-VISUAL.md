# Identidad Visual — Revisión Integral (2026-07-16)

Este documento registra la revisión integral de identidad gráfica solicitada para que cada infografía tenga personalidad propia sin perder coherencia entre todas. Es una capa de contexto sobre [INFOGRAFIA-SPEC.md](INFOGRAFIA-SPEC.md) (que sigue siendo la fuente de verdad para tamaño, firma y reglas de contenido) — no la reemplaza.

## 1. Skills evaluadas

El usuario pidió evaluar e instalar, si aportaban valor: Canvas Design, Diagram/SVG (Claude Code), Infographic-Outline-Creator, Skills de Presentaciones, Skills de Documentos, web-artifacts-builder, theme-factory y algorithmic-art.

**Ninguna de esas ocho estaba disponible para instalar desde esta sesión.** Instalar una Skill de Claude Code es una acción del lado del usuario (vía configuración de plugins/marketplace de Claude Code), no algo que se pueda ejecutar desde dentro de una conversación con las herramientas disponibles aquí. Se descartaron por falta de acceso, no por falta de mérito — si el usuario quiere probarlas, tendría que instalarlas él mismo fuera de esta sesión y se podría reevaluar su aporte real en ese momento.

**Sí estaban disponibles y se usaron dos Skills ya cargadas en el entorno:**

- **`artifact-design`** — guía de diseño general (paleta, tipografía, layout, "evitar clichés de diseño generado por IA"). Se usó como checklist activo: confirmó que el patrón repetido en todas las infografías anteriores (tarjeta blanca redondeada + barra de acento de color + header en píldora de color) es *literalmente* uno de los clichés que la skill señala como genérico. Esa fue la base objetiva para decidir rediseñar, no solo una preferencia estética.
- **`dataviz`** — procedimiento para gráficos honestos (elegir la forma según el trabajo del dato, asignar color por función, validar paleta, specs de marcas). Se aplicó al criterio de las tablas/gráficos ya existentes (heatmap de cobertura, barras, specs de latencia/gobernanza), pero **el script de validación automática (`validate_palette.js`) no se pudo ejecutar** porque este sandbox no tiene Node.js instalado (`which node` → no encontrado). Las paletas se revisaron manualmente contra los criterios documentados de la skill (contraste, no usar rueda de colores arbitraria, jerarquía de tinta vs. color) en vez de con el script — es una limitación real, no un paso omitido en silencio.

`artifact-design` se aplicó a las 9 piezas rediseñadas (paleta, tipografía, layout, anti-clichés). `dataviz` se aplicó específicamente donde había un gráfico o tabla de datos real que codificar — ver la columna "Skills aplicadas" en la tabla de la sección 3 para el detalle pieza por pieza.

## 2. Principios de diseño adoptados

1. **Anclar cada pieza en su sujeto real**, no en una paleta "de la casa" repetida. Si el tema es un proveedor con marca propia (AWS, Azure, Oracle, Google, Python), usar sus colores de marca reales. Si el tema es neutral respecto a proveedor (patrones de arquitectura, Medallion, automatización con agentes), anclar en una metáfora literal del propio contenido en vez de inventar una paleta arbitraria.
2. **Variar la composición, no solo el color.** Cada pieza usa una estructura distinta: pipeline horizontal oscuro, torre vertical en cascada, Venn de fusión, pipeline multicolor, ficha técnica tipo blueprint, medallas metálicas, panel comparativo de dos columnas.
3. **Evitar los clichés de IA señalados por `artifact-design`**: sin tarjeta blanca + barra de acento única repetida en todo; sin paleta "seguridad" (Inter + acento neón sobre negro); neutros elegidos a propósito, no por defecto.
4. **Estructura como información** (no decoración): la numeración solo se usa donde el contenido es genuinamente una secuencia o catálogo enumerable (los 9 patrones de arquitectura de datos), no como adorno.
5. **Gráficos y tablas con criterio de `dataviz`**: color por función (categórico vs. secuencial vs. estado), nunca arcoíris arbitrario; las tablas de specs (ej. Latencia/Gobernanza en Arquitectura_Datos) se agregaron porque aportan comparación real, no para rellenar espacio.
6. **Un solo hilo conductor entre todas las piezas**: el ribbon inferior de callout (icono + texto en una franja de acento oscuro) y la firma personal (LinkedIn + `cacm523`) se mantienen en todas — es la familia visual compartida; todo lo demás (paleta, layout, tipografía de soporte) puede variar libremente por tema.

## 3. Estrategia visual por infografía

| Archivo | Anclaje | Paleta | Layout distintivo | Skills aplicadas |
|---|---|---|---|---|
| `Arquitectura/arquitectura-aws.html` | Marca real AWS | Squid Ink navy `#0F1621`/`#16202C` + AWS Orange `#FF9900` | Consola oscura, pipeline horizontal de 5 etapas | `artifact-design` + `dataviz` (heatmap "Cobertura por etapa") |
| `Arquitectura/arquitectura-azure.html` | Marca real Azure | Azure Blue `#0078D4` sobre fondo claro, Segoe UI | Torre vertical en cascada (Bronze→Silver→Gold desplazados) | `artifact-design` + `dataviz` (tabla de capacidades Purview + barras Power BI) |
| `Arquitectura/arquitectura-oracle.html` | Marca real Oracle + concepto "lakehouse = unión" | Oracle Red `#C74634` sobre paper cálido | Venn de dos círculos superpuestos (Object Storage ∩ Autonomous Database = Data Catalog) | `artifact-design` + `dataviz` (barras "ejemplo de dashboard") |
| `Arquitectura/arquitectura-google.html` | Marca real Google (4 colores) | Blanco/gris Material + azul/rojo/amarillo/verde como acento por etapa | Pipeline horizontal con cada tarjeta coloreada según el orden del wordmark de Google | `artifact-design` + `dataviz` (tabla de cobertura real-time/batch + barras por región) |
| `Arquitectura/arquitectura-datos.html` | Metáfora: catálogo técnico de referencia | Azul blueprint `#1B3A6B` sobre papel cuadriculado | Grid 3×3 estilo hoja de ingeniería, con numeración (P01–P09) y specs Latencia/Gobernanza | `artifact-design` + `dataviz` (specs Latencia/Gobernanza por patrón) |
| `Arquitectura/arquitectura-medallon.html` | Metáfora literal: metales bronce/plata/oro | Gradientes metálicos reales (bronce/ámbar-fuego/plata/oro) sobre grafito oscuro | Medallas circulares + tarjetas con acabado metálico, fondo tipo vitrina/fundición | `artifact-design` + `dataviz` (barras de volumen del embudo Bronze→Gold) |
| `Automatización/automatizacion-python.html` | Marca real Python | Python Blue `#306998` + Python Yellow `#FFD43B` | Pipeline horizontal + sidebar de métricas (gauge, antes/después, casos de uso) | `artifact-design` + `dataviz` (gauge de eficiencia 75%) |
| `Automatización/automatizacion-python-programada.html` | Marca real Python (mismo sistema que el anterior, layout distinto) | Python Blue + Yellow | Código + diagrama de flujo de 4 pasos en dos columnas | `artifact-design` (diagrama de flujo, no hay dato tabular que graficar) |
| `Automatización/automatizacion-agentesia.html` | Metáfora: rígido vs. adaptativo | Grafito neutro (no agéntico) vs. ámbar cálido (agéntico) | Panel comparativo de dos columnas: lista estática vs. diagrama circular de retroalimentación | `artifact-design` (diagrama de flujo, no hay dato tabular que graficar) |

**Piezas de evento (Datafest 2026) sin tocar**, porque ya tienen identidad propia justificada por su propio branding de marca patrocinadora: `IA/analisis-datos-ia.html` y `IA/finalidades-de-las-ia.html` (Bancolombia, dorado/oscuro) e `IA/ia-agentes.html` (AWS, púrpura/magenta).

## 4. Reglas de estilo para desarrollo futuro

- Antes de diseñar una infografía nueva de un proveedor con marca propia, investigar sus colores de marca reales — no reutilizar la paleta de otra infografía del repositorio.
- Para temas sin proveedor (conceptos, patrones, metodologías), elegir una metáfora visual literal del propio contenido y construir la paleta alrededor de ella.
- No repetir la misma composición de tarjetas en dos infografías consecutivas del mismo tema — variar entre pipeline, torre, Venn, grid, panel comparativo, etc. según lo que el contenido realmente representa.
- Revisar cualquier diseño nuevo contra la lista de clichés de IA de `artifact-design` (tarjeta blanca + barra de acento única, Inter/Space Grotesk como fuente "segura", todo centrado, emoji como marcador de sección) antes de darlo por terminado.
- Si una tarjeta o columna se ve con mucho espacio vacío al fondo, no forzar una altura fija arbitraria: usar `margin-top:auto` en el último elemento o `justify-content:space-between` en un contenedor flex para que el contenido se distribuya en el alto real disponible.
- Mantener el ribbon de callout inferior y la firma LinkedIn/`cacm523` como el hilo conductor de familia — son los únicos elementos que deben verse "iguales" entre todas las piezas.
- Validar paletas contra los criterios de `dataviz` (contraste, color por función) manualmente si Node.js no está disponible en el entorno de ejecución — dejar constancia de que se hizo así, no omitir el paso en silencio.

## 5. Cambios realizados en esta revisión

Rediseño completo (HTML + PNG re-exportado con el pipeline headless-Chrome + recorte PIL de siempre) de:

- `Arquitectura/arquitectura-aws.html` / `.png`
- `Arquitectura/arquitectura-azure.html` / `.png`
- `Arquitectura/arquitectura-oracle.html` / `.png`
- `Arquitectura/arquitectura-google.html` / `.png`
- `Arquitectura/arquitectura-datos.html` / `.png`
- `Arquitectura/arquitectura-medallon.html` / `.png`
- `Automatización/automatizacion-python.html` / `.png`
- `Automatización/automatizacion-python-programada.html` / `.png`
- `Automatización/automatizacion-agentesia.html` / `.png`

De paso se corrigió un bug preexistente (no relacionado con el color) en `automatizacion-agentesia.html`: el selector CSS `.diagram svg` no estaba delimitado a la capa de conectores, así que también capturaba los íconos SVG dentro de cada círculo de nodo y los sacaba de su posición centrada. Se corrigió agregando `class="connectors"` al SVG de líneas y delimitando el selector a `.diagram svg.connectors`.

Los 9 PNG resultantes se recopiaron a `paginaweb/publications/` sobre los nombres de archivo existentes (sin cambios de metadata en `publicaciones.json` / `publicaciones.js`, ya que el contenido y los nombres de archivo no cambiaron, solo el diseño visual).

## 6. Recomendaciones a futuro

- Si en algún momento se instalan Skills adicionales de diseño (Canvas Design, theme-factory, etc.) fuera de esta sesión, reevaluar su aporte real contra lo ya logrado aquí antes de adoptarlas — el criterio de "anclaje real + variedad de composición" ya cubre buena parte de lo que esas skills prometen.
- Cuando el catálogo de temas crezca (Power BI, nuevos proveedores cloud, etc.), aplicar el mismo criterio de esta revisión desde el primer diseño, no como corrección posterior.
- Si se agrega Node.js al entorno, ejecutar `scripts/validate_palette.js` de la skill `dataviz` sobre cada paleta nueva en vez de la validación manual usada aquí.
