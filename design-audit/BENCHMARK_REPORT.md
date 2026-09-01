# Benchmark Report — infografia vs. referencias premium

Comparación honesta contra los productos citados en el prompt original. Aclaración de contexto obligatoria: comparar una infografía estática de LinkedIn 1200×627px contra un *producto de software interactivo* (Stripe, Linear, Notion, Figma) mide cosas distintas — se ajusta la comparación a lo que sí es comparable: **densidad de información, jerarquía tipográfica, disciplina de paleta, y calidad editorial**, no interactividad ni arquitectura de producto.

| Referencia | Qué hace mejor que infografia hoy | Qué ya iguala infografia hoy | Score de brecha (1-10, 10=sin brecha) |
|---|---|---|---|
| **Microsoft Learn / Azure Architecture Center** *(referencia declarada en el spec)* | Sistema de iconografía oficial reconocible al instante; grosor de línea y esquinas 100% consistentes entre diagramas | Piezas de `Arquitectura/` (medallón, AWS/Azure/GCP) ya siguen la misma lógica de nodos+flujo con color por capa | 7/10 |
| **Stripe** (docs/marketing) | Tipografía con jerarquía de peso muy marcada (un solo elemento domina la lectura); espacio negativo generoso como herramienta, no como sobra | Piezas de hoy con metáfora visual concreta (tabla periódica IA) se acercan en foco de un solo concepto por pieza | 5/10 |
| **Linear** | Micro-contraste de superficie (bordes de 1px casi invisibles, sombras de 1-2px) que da sensación "premium" sin gradientes vistosos | La paleta verde+tierra + tarjetas blancas sobre fondo `--bg-canvas` ya usa esa lógica de contraste sutil en el lote reciente | 6/10 |
| **Notion** | Densidad de información alta sin sensación de saturación, gracias a tipografía monoespaciada bien dosificada para código/datos | Los bloques de código en `TrucosSQL`, `VejesDashboard`, `ErroresGroupBy` usan la misma lógica (fondo oscuro, syntax highlighting real) | 7/10 |
| **Vercel** | Uso de gradientes de un solo color con transición muy sutil, nunca dos colores compitiendo | Los "glow blobs" del lote reciente (ver `AI_SLOP_REPORT` #4) son el intento más cercano, pero aún genéricos en vez de compuestos | 4/10 |
| **Apple** (keynote/producto) | Un solo mensaje por pantalla, jerarquía tipográfica de 3-4 niveles máximo, cero ruido decorativo | La mayoría de piezas de infografia comunican 5-7 sub-mensajes por pieza (es el formato — infografía técnica densa, no landing) — **brecha estructural, no de ejecución** | 3/10 (brecha esperable por formato) |
| **Tableau / Bloomberg** | Uso de datos reales con precisión de cifra (no aproximaciones "arriesgadas") y gráficos que son la pieza central, no decoración | `bigdata-grandes-empresas.png` (73M artículos, 8.4M galones) ya sigue esta disciplina; el lote de hoy evita fabricar cifras (ver regla del proyecto) | 8/10 |
| **Airtable** | Colores de estado (success/warning/error) semánticamente consistentes en toda la plataforma | `ErroresGroupBy` usa rojo/verde consistente para incorrecto/correcto — mismo principio, aplicado puntualmente, no como sistema | 5/10 |
| **Figma / Framer** | Motion y micro-interacción como parte de la identidad | No aplica — el formato es una imagen estática exportada una sola vez, sin runtime (ver limitación estructural en `CLAUDE.md`) | N/A — brecha no cerrable por diseño del proyecto |

## Lectura general

El repositorio está más cerca del nivel "documentación técnica premium" (Microsoft Learn, Notion, Tableau) que del nivel "producto SaaS con identidad de marca fuerte" (Stripe, Linear, Vercel) — lo cual es coherente con su propósito real: son infografías educativas para LinkedIn, no la home de un producto. La brecha más honesta y accionable es **Vercel-style restraint en gradientes** (hoy los glow blobs son genéricos) y **Apple-style foco de un solo mensaje** — pero esta última es una tensión real con el formato (una infografía técnica de LinkedIn necesita comunicar varios sub-puntos para justificar el share), no un déficit de ejecución a corregir ciegamente.

## Recomendación priorizada

1. Generalizar el patrón "comparación binaria lado a lado" (SQL) a otros temas con contraste natural (seguro/inseguro, antes/después, correcto/incorrecto) — es el patrón más cercano al nivel Stripe/Linear de foco.
2. Variar deliberadamente posición/color de los glow blobs por pieza en vez de reusar coordenadas — cierra parte de la brecha con Vercel sin rediseñar nada.
3. No perseguir el minimalismo tipo Apple a costa de recortar contenido técnico real — el formato infografía-densa es la propuesta de valor del proyecto, no un defecto a corregir.
