# Especificación de Diseño — Infografías Técnicas

(Ver el archivo raíz `INFOGRAFIA-SPEC.md` para el contenido completo compartido por todo el catálogo.)

## Contexto específico — Inteligencia Artificial Jurídica

**Tema**: 4 niveles crecientes de intervención sobre un modelo de lenguaje aplicados al trabajo legal — LLM generalista (usar tal cual), RAG con conocimiento jurídico (contextualizar con fuentes propias), fine-tuning especializado (adaptar con ejemplos jurídicos), y post-training para ejecutar tareas jurídicas complejas de punta a punta (entrenar) — con ejemplos reales de herramientas en cada nivel.

**Referencia** (1 imagen pegada en el chat, marca "Derecho 4.0", estilo editorial serif claro): 4 columnas numeradas (01-04) con diagrama de flujo por columna, ejemplos de herramientas debajo de cada una, y un eje horizontal inferior Usar→Contextualizar→Adaptar→Entrenar (menor a mayor intervención en el modelo).

**No se replica la marca de la referencia** ("Derecho 4.0") — firma habitual del catálogo (LinkedIn + cacm523).

**Archetype aplicado**: blueprint numerado (INFOGRAFIA-SPEC.md → Patrones de Composición Estructurada) — encaja naturalmente con las 4 columnas numeradas 01-04 de la referencia + banda transversal inferior (el eje Usar/Contextualizar/Adaptar/Entrenar).

**Íconos reales usados**: `chatgpt.svg`, `claude.svg`, `gemini.svg` (columna 1, ya en el repo). Para herramientas de nicho legal sin logo disponible (Westlaw, Lexis+ AI, Harvey Knowledge/Tenet, LEGAL-BERT) se usa iconografía semántica genérica (libro, balanza, documento) — no se aproximan logos a mano.

**Paleta**: verde+tierra por defecto del proyecto (no es una pieza de una sola aplicación con marca propia, combina varias herramientas de nicho sin identidad visual estándar en el catálogo).

**Catálogo**: `categoriaPrincipal: "inteligencia-artificial"`, `temas: ["ia", "machine-learning"]` — tema IA, aplica publicación inmediata.
