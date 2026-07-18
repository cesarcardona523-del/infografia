# Especificación de Diseño — Infografías Técnicas

> Fuente de verdad del diseño. Ver INFOGRAFIA-SPEC.md para el detalle completo (composición editorial, sin fotografías/escenas/personas, firma LinkedIn + `cacm523`, tamaño 1200×627px).

---

## Contexto específico — El Ciclo de Vida de un Proyecto de Ciencia de Datos

**Referencia**: `referencias/Cultura_Datos/ciclo-vida-ciencia-datos/CienciasDato.jpeg` (generada con NotebookLM) — rueda circular de 6 etapas con un ejemplo recurrente de predicción de fuga de clientes (churn).

**Las 6 etapas** (contenido real de la referencia, condensado):
1. Entendimiento del Negocio — definir el objetivo, alinear con KPIs estratégicos, planificar en sprints cortos (4-6 semanas).
2. Entendimiento de los Datos — recolectar la "materia prima" (bases de datos, APIs, web scraping), analizar calidad, usar un diccionario de datos.
3. Preparación y Exploración de Datos (EDA) — limpiar valores nulos/erróneos, convertir variables categóricas a numéricas, explorar patrones y correlaciones.
4. Modelado y Evaluación — seleccionar variables predictivas, segmentar 70/30 entrenamiento/prueba, aplicar algoritmos (árbol de decisión, XGBoost), evaluar con matriz de confusión.
5. Implementación y Despliegue — contenerizar con Docker, exponer vía API, automatizar con CI/CD, desplegar y orquestar con Kubernetes.
6. Comunicación y Monitoreo — monitorear rendimiento en producción, detectar "model drifting", usar herramientas de visualización (Power BI, Tableau), documentar y versionar.

**Enriquecimiento**: se conserva la estructura circular (es un ciclo real, no lineal — el monitoreo retroalimenta el entendimiento del negocio) pero se simplifica el detalle textual de cada etapa (la referencia trae sub-viñetas extensas por etapa) y se usa el ejemplo de churn una sola vez, como hilo conductor en el cierre, en vez de repetirlo en cada etapa.

**Dirección visual**: rueda hexagonal de 6 nodos conectados en círculo con flechas curvas que cierran el ciclo, un color categórico fijo por etapa (azul, naranja, púrpura, teal, ámbar, verde — sin repetir orden), centro con ícono de ciclo continuo. Cierre con el caso guía de churn como ejemplo aplicado a las 6 etapas en una frase.
