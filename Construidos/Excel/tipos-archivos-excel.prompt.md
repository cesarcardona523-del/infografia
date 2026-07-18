# Especificación de Diseño — Infografías Técnicas

> Ver INFOGRAFIA-SPEC.md para el detalle completo (composición editorial, sin fotos/escenas/personas, firma LinkedIn + `cacm523`, 1200×627px).

---

## Contexto específico — XLSX vs. TXT/CSV vs. Parquet

**Referencia**: `referencias/Excel/tipos-archivos-excel/ArchivosExcel.jpeg` — infografía ya bien estructurada: comparación de 3 formatos de archivo para análisis masivo (500 mil a 1 millón de filas), ranking de preferencia, flujo recomendado de 5 pasos y regla práctica de cierre. Se rediseña conservando la estructura completa (es la forma correcta de comunicar esta comparación), con iconografía y paleta propias.

**Contenido real**:
- **XLSX** — "Para personas". Fácil de revisar, límite de 1,048,576 filas, no ideal para procesos masivos.
- **TXT/CSV** — "Buena fuente cruda". Muy compatible, soporta millones de filas, requiere limpieza y tipado.
- **PARQUET** — "Mejor opción analítica". Lectura rápida, menor peso, conserva tipos de datos.
- **¿Cuál conviene más?** (ranking): 1) Parquet — mejor opción general, 2) TXT/CSV — buen origen, 3) XLSX — solo revisión y entrega.
- **Flujo recomendado**: ERP/Sistema → TXT/CSV crudo → Limpieza → Parquet limpio → Power BI/Python. Nota: "Excel queda como validación o reporte, no como almacén principal."
- **Regla práctica** (cierre, verbatim): "XLSX para revisar, TXT/CSV para extraer, PARQUET para analizar."

**Dirección visual**: 3 colores diferenciados por formato (verde real de Excel, verde azulado para TXT/CSV, azul para Parquet — inspirado en el azul real del logo de Apache Parquet), 3 columnas comparativas, fila de ranking numerado, diagrama de flujo horizontal de 5 pasos con flechas, franja de regla práctica al cierre.
