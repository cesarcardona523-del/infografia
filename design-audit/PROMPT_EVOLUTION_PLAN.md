# Prompt Evolution Plan — infografia

Auditoría de los dos prompts fuente ([INFOGRAFIA-SPEC.md](../INFOGRAFIA-SPEC.md) e [INFOGRAFIA-INVESTIGAR.md](../INFOGRAFIA-INVESTIGAR.md)) y del prompt implícito de "Contexto específico" que se agrega por pieza.

## Debilidades detectadas en el prompt de diseño (SPEC)

| Debilidad | Evidencia | Riesgo |
|---|---|---|
| Ausencia histórica de regla anti-espacio-vacío (corregida hoy) | Piezas de `Cultura_Datos` con 30-40% de área muerta bajo íconos decorativos | Ya mitigado — sección "Aprovechamiento del Espacio" agregada en esta sesión |
| Sin regla explícita sobre variación de los "glow blobs" | Coordenadas idénticas copiadas entre `TablaPeriodicaIA`, `TrucosSQL`, `VejesDashboard` | Riesgo de que se vuelvan un default sin pensar (ver `AI_SLOP_REPORT` #4) |
| "Diseño arriesgado, no plantillado" es una instrucción cualitativa sin checklist verificable | Se depende de que quien construye la pieza recuerde compararla mentalmente contra las anteriores del mismo tema | Falta un paso explícito de "listar los layouts ya usados en este tema antes de elegir el de la pieza nueva" |
| No hay vocabulario de metáforas visuales pre-aprobadas más allá de los 4 ejemplos citados (pirámide, iceberg, zigzag, báscula) | Un modelo tiende a repetir el primer ejemplo que reconoce (pirámide) cuando no tiene más opciones concretas | Ampliar el banco de metáforas reduce la regresión a la media |

## Debilidades detectadas en el prompt de investigación/metadata (INVESTIGAR)

| Debilidad | Evidencia | Riesgo |
|---|---|---|
| Optimizado para analizar una imagen de referencia, no para describir una pieza ya construida por el propio proyecto (flujo alterno) | En la sesión de hoy, las 19 descripciones se redactaron manualmente sin ejecutar el prompt literal sobre una imagen — funcionó, pero el prompt no documenta ese caso de uso | Falta una nota explícita: "si la pieza ya fue construida por el proyecto (no es una referencia externa), interpretar el HTML/contenido final en vez de una imagen" |
| No fija un mínimo de especificidad técnica anti-genérica en la descripción | Ninguna evidencia de descripciones vagas en el catálogo actual, pero el prompt no lo previene estructuralmente | Bajo, pero fácil de agregar: exigir al menos una mención de tecnología/técnica nombrada explícitamente, no solo "buenas prácticas" |

## Prompts históricos vagos/genéricos (inferidos del inventario, no de logs literales)

Sin acceso a los prompts de contexto-específico literales de cada pieza histórica, la evidencia indirecta más fuerte es el propio artefacto resultante: piezas como `analisis-datos.png` (ver `AI_SLOP_REPORT` #1-2) son consistentes con un contexto-específico que solo listó el contenido a cubrir sin indicar una metáfora visual concreta ni una referencia de composición — el resultado es el layout por defecto del modelo.

**Patrón de prompt débil inferido:** "Tema: X. Contenido: [lista de bullets]. Usa el spec." — sin dirección artística.

**Patrón de prompt fuerte, ya validado hoy:** las piezas nuevas de este lote que mejor resolvieron el espacio fueron las que en su corrección recibieron una instrucción concreta de metáfora ("tabla periódica", "ciclo de fases retroalimentado", "comparación código incorrecto/correcto") en vez de "rellena el espacio vacío" genérico.

## Plan de evolución del prompt de contexto-específico (paso 3 del flujo de creación)

A partir de ahora, la sección `## Contexto específico — <Topico>` de cada `.prompt.md` nuevo debe incluir, además de lo ya exigido por CLAUDE.md:

1. **Metáfora visual elegida y por qué** (no solo "usa una metáfora visual") — una frase explícita: *"Se usa una tabla periódica porque el contenido es una taxonomía cerrada de herramientas por categoría, no un proceso secuencial."*
2. **Layouts ya usados en ese Tema** (lista corta) para que la pieza nueva declare explícitamente en qué se diferencia — operacionaliza la regla ya existente de "diseño arriesgado, no plantillado".
3. **Un ejemplo de dato/comparación real que anclará al menos un elemento gráfico no textual** (tabla, comparación lado a lado, gráfico) — evita que "Riqueza Visual" se resuelva solo con íconos decorativos.

## Próxima acción concreta

Incorporar los 3 puntos anteriores como checklist obligatorio en el paso 3 de "Flujo para crear una infografía nueva" en `CLAUDE.md`, la próxima vez que se construya una pieza desde cero (no requiere tocar `INFOGRAFIA-SPEC.md`, que ya es lo suficientemente genérico para todos los temas).
