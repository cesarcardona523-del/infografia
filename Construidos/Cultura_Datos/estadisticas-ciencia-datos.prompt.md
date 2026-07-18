# Especificación de Diseño — Infografías Técnicas

> Ver INFOGRAFIA-SPEC.md para el detalle completo (composición editorial, sin fotos/escenas/personas, firma LinkedIn + `cacm523`, 1200×627px).

---

## Contexto específico — Estadística Práctica para Científicos de Datos

**Referencia**: `referencias/Cultura_Datos/estadisticas-ciencia-datos/EstadisticaCienciaDato.jpg` (NotebookLM) — resumen del libro "Estadística Práctica para Científicos de Datos" (Bruce & Bruce), dos columnas: EDA y Muestreo/Distribuciones.

**Contenido real** (conceptos estadísticos estándar, no propietarios):
- EDA: datos numéricos (continuos/discretos) vs categóricos (binarios/ordinales) — determinan el tipo de análisis/visualización correcta.
- Media (sensible a outliers) vs Mediana (robusta).
- Desviación estándar (dispersión promedio) vs IQR (más robusto ante outliers).
- Histograma y Boxplot para visualizar la distribución.
- Muestreo aleatorio: clave para evitar sesgo, obtener una muestra representativa.
- Distribución muestral: el estadístico de una muestra (ej. la media) tiene su propia distribución, que tiende a ser normal.
- Bootstrap: remuestreo con reemplazo para estimar la variabilidad del muestreo (error estándar, intervalos de confianza).

**Dirección visual**: split de dos columnas (EDA en azul, Muestreo y Distribuciones en naranja, sobre fondo blanco), con diagramas conceptuales reales (balanza para media/mediana, curva de campana para desviación estándar, histograma/boxplot, nube de puntos para muestreo, curva de distribución muestral, flujo de remuestreo bootstrap) — sin inventar cifras, todo conceptual/cualitativo tal como permite la sección "Riqueza Visual" del spec.
