# Especificación de Diseño — Infografías Técnicas

(Ver el archivo raíz `INFOGRAFIA-SPEC.md` para el contenido completo compartido por todo el catálogo.)

## Contexto específico — Optimización de Tiempos de Ejecución en SQL (Índices)

**Tema**: cómo un índice cambia la forma en que una base de datos encuentra los datos — de revisar fila por fila (escaneo secuencial) a localizar directamente (búsqueda indexada) — con el costo real que tiene indexar (no siempre conviene indexar todo).

**Referencia** (1 imagen pegada en el chat): infografía con comparación "sin índice" (rojo, escaneo de 1.000.000 de filas, ~4.000 ms) vs "con índice" (verde, estructura ordenada tipo B-Tree, ~40 ms), + 3 paneles inferiores (cómo funciona en 4 pasos, por qué no indexar todo — costos reales, cuándo conviene crear un índice) + cierre con frase y ícono de tendencia.

**Corrección aplicada sobre la referencia (regla de "no inventar información técnica")**: la referencia usa cifras específicas (~4.000 ms vs ~40 ms, 1.000.000 de registros) como ilustración pedagógica de una diferencia de orden de magnitud real y bien documentada (escaneo secuencial O(n) vs búsqueda indexada O(log n)) — se mantienen como **ejemplo ilustrativo explícito** (ver nota en el footer), no como benchmark de un sistema real, para no presentarlas como una medición verificada.

**Estándar aplicado**: esta pieza sigue el estándar visual "Dark IDE" del tema SQL (ver `CLAUDE.md` → "Tema SQL — estándar visual Dark IDE"), igual que el resto del catálogo de SQL — fondo oscuro tipo editor de código, bloques de código con sintaxis resaltada, rojo como acento de "problema" y verde como acento de "solución" (coherente con el resto del catálogo, que usa rojo como acento de marca por defecto del tema).

**Paleta**: SQL genérico (ANSI), sin dialecto de motor específico — rojo (`#F07178`/`#EE352E`) para "sin índice" y verde (`#9ECE6A`) para "con índice", sobre la base oscura `#1E1E2E`/`#181825` del estándar.

**Catálogo**: `categoriaPrincipal: "bases-de-datos"`, `temas: ["sql"]`.

## Consolidación (2026-09-25)

El usuario trajo una segunda referencia sobre el mismo tópico exacto (mismo titular "4 segundos → 40 ms", mismo ejemplo `SELECT * FROM clientes WHERE dni = 38750084`, misma nota "Con 1.000.000 de registros...", mismo panel "¿Cómo funciona?/¿Por qué no indexar todo?/¿Cuándo crear uno?") — se trató como actualización in-place (misma regla de "Gestión inteligente de publicaciones e infografías" de CLAUDE.md), no como pieza nueva. Versión anterior archivada en `Construidos/SQL/Archivadas/optimizacion-tiempos-ejecucion-indices-2026-09-25/` y en `paginaweb/publications/Archivadas/`.

**Aporte real incorporado**: se agregaron las dos tablas de ejemplo concretas de la nueva referencia — la tabla de escaneo secuencial (`id/nombre/dni`, fila destacada del registro 1.000.000) y la tabla de estructura de índice (`dni → ubicación`) — que hacen tangible visualmente la diferencia entre "revisar" y "localizar". También se actualizó la frase de cierre a la variante de la nueva referencia ("Un buen índice no se nota cuando todo va bien: se nota cuando tu sistema empieza a crecer"). `fechaPublicacion` actualizada a la fecha/hora de esta actualización por tratarse de un aporte real de contenido, no una corrección menor.
