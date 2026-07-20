# Especificación de Diseño — Infografías Técnicas

> Ver INFOGRAFIA-SPEC.md para el detalle completo. Sin fotos/escenas/personas, firma LinkedIn + `cacm523`, 1200×627px.

## Contexto específico — Métricas para Evaluar Modelos de IA

**Referencia**: `referencias/IA/metricas-modelos-ia/MetricasModelosIA.jpeg` — pieza de marca de un tercero ("Data&Analytics"). **Se descarta su logo y URL**; se conserva el contenido técnico. La referencia trae 11 métricas con fórmula + intuición visual + uso, una por una en un grid vertical — demasiado denso para replicar íntegro con buena legibilidad en 1200×627px, así que se reagrupa por familia real (Regresión vs. Clasificación), que ya está implícita en el "uso principal" de cada métrica original.

**Contenido real (sin inventar cifras)** — 11 métricas agrupadas en 2 familias:

**Métricas de Regresión** (predicen un valor continuo):
1. **MAE** — promedio del error absoluto entre predicción y valor real. Uso: interpretación directa, error en unidades reales.
2. **MSE** — promedio del error cuadrático; penaliza más los errores grandes. Uso: optimización, castiga errores grandes.
3. **RMSE** — raíz del MSE; devuelve el error a la unidad original. Uso: comparación de modelos.
4. **R²** — mide qué proporción de la variabilidad explica el modelo. Uso: ajuste global, varianza explicada.
5. **R² ajustado** — versión de R² que penaliza variables innecesarias. Uso: comparar modelos, selección de variables.
6. **MAPE** — error porcentual absoluto medio respecto al valor real. Uso: forecasting, ventas y demanda.

**Métricas de Clasificación** (predicen una categoría):
7. **Accuracy** — porcentaje total de predicciones correctas. Uso: escenarios balanceados, visión general.
8. **Precision** — de los positivos predichos, cuántos fueron correctos. Uso: costo de falsos positivos, fraude/alertas.
9. **Recall** — de los positivos reales, cuántos logró detectar el modelo. Uso: costo de falsos negativos, diagnóstico/riesgo.
10. **F1-score** — media armónica entre precision y recall. Uso: clases desbalanceadas, evaluación integral.
11. **ROC-AUC** — mide la capacidad del modelo para separar clases a distintos umbrales. Uso: clasificación binaria, comparar discriminación.

**5 conceptos clave de la referencia**: Residual (diferencia entre predicción y valor real), Matriz de confusión (TP/FN/FP/TN), Umbral (cambia la decisión en clasificación), Desbalance (puede volver engañosa la accuracy), Overfitting (memoriza en vez de generalizar).

**Dirección visual**: dos tablas de referencia rápida lado a lado (Regresión | Clasificación), cada fila con métrica + qué mide + uso principal — color por función (una familia = un color), no arcoíris. Franja inferior con los 5 conceptos clave como chips compactos.
