# Especificación de Diseño — Infografías Técnicas

> Ver INFOGRAFIA-SPEC.md para el detalle completo (composición editorial, sin fotos/escenas/personas, firma LinkedIn + `cacm523`, 1200×627px).

---

## Contexto específico — Tipos de Normalización en Ciencia de Datos

**Referencia**: `referencias/Cultura_Datos/normalizacion-ciencia-datos/NormalizaciónCienciasDatos.jpeg` — tabla técnica de 8 métodos de normalización (marca "Data&Analytics", se generaliza sin usar su branding).

**Los 8 métodos** (contenido técnico real, estándar de la disciplina):
1. Z-Score (Standard Score) — variables numéricas continuas; cuando los datos siguen una distribución aproximadamente normal o el algoritmo usa distancias (K-Means, PCA, SVM). Ventaja: centra en media 0 y desviación 1. Límite: sensible a outliers.
2. Min-Max Scaling — cuando se requiere que todos los valores estén entre 0 y 1. Ventaja: fácil interpretación, útil para redes neuronales. Límite: muy sensible a outliers.
3. Robust Scaling — variables con outliers. Ventaja: poco afectado por atípicos. Límite: no garantiza un rango específico.
4. Decimal Scaling — cuando solo se desea reducir la magnitud de los datos. Ventaja: muy simple. Límite: poco utilizado actualmente.
5. Log Transformation — datos financieros, ventas, población con fuerte asimetría. Ventaja: reduce sesgo y comprime grandes valores. Límite: no admite valores negativos.
6. Power Transformation (Box-Cox) — cuando se desea aproximar la distribución a una normal. Ventaja: mejora modelos lineales. Límite: solo admite datos positivos.
7. Yeo-Johnson Transformation — igual que Box-Cox pero admite valores negativos. Ventaja: muy flexible. Límite: requiere estimación del parámetro.
8. Unit Vector (L2 Normalization) — procesamiento de texto, NLP, sistemas de recomendación. Ventaja: conserva la dirección del vector. Límite: no elimina la influencia de outliers.

**Dirección visual**: grid 4×2 de tarjetas técnicas de referencia, navy/teal (distinto del azul-blueprint ya usado en `Arquitectura/arquitectura-datos.html` y del azul-oscuro de `estadisticas-ciencia-datos`), cada tarjeta con ícono, nombre, fórmula simplificada, cuándo aplicarlo, y un par ventaja/límite.
