# Especificación de Diseño — Infografías Técnicas

(Ver el archivo raíz `INFOGRAFIA-SPEC.md` para el contenido completo compartido por todo el catálogo.)

## Contexto específico — Desarrollo de Agentes de IA

**Tema**: mapa de las piezas técnicas que intervienen en la construcción de un agente de IA — fundamentos de programación, modelos de lenguaje (LLMs), frameworks de orquestación, habilidades específicas para agentes (herramientas, memoria, RAG), bases de datos (vectoriales y tradicionales), APIs de integración, y despliegue en producción.

**Referencia** (1 imagen pegada en el chat, marca "Nicolas Valenzuela @beto18v"): mapa mental/roadmap con 7 ramas — Fundamentos, LLMs, Frameworks de IA, Habilidades para Agentes de IA, Bases de Datos, APIs, Despliegue — cada una con varios nodos de herramientas/conceptos específicos.

**No se replica la marca de la referencia** ("Nicolas Valenzuela @beto18v") — se mantiene solo la firma profesional habitual del catálogo (LinkedIn + cacm523).

**Reinterpretación de composición (actualizada, 2026-09-25, pedido explícito del usuario)**: en vez de un mapa mental radial literal (ya usado como referencia) o de una grilla de columnas categorizadas, se construye un **dendrograma/árbol jerárquico horizontal** (estilo `d3-hierarchy`/`d3.cluster`, tipo [d3-graph-gallery dendrogram](https://d3-graph-gallery.com/dendrogram.html)) generado programáticamente en Python y embebido como SVG inline en el HTML — no se carga D3.js en tiempo de render para mantener la pieza autocontenida para el pipeline de Chrome headless. Estructura: un nodo raíz (ícono "agente") a la izquierda de cada mitad, conectado mediante enlaces en ángulo recto ("elbow links") a los nodos de categoría, y cada categoría conectada de la misma forma a sus nodos hoja (herramienta/concepto + ícono 21px + etiqueta 16px) a la derecha — el layout vertical de cada hoja y el punto medio de cada categoría/raíz se calculan automáticamente a partir del número de hojas por categoría, evitando solapamientos.

**Ajuste de aprovechamiento de espacio (2026-09-25, corrección pedida por el usuario tras la primera versión)**: el árbol único de 25 hojas, al ajustarse por `preserveAspectRatio` al alto disponible, se downscaleaba por debajo del piso de 14px y dejaba espacio horizontal sin usar junto al tronco raíz. Se dividió en **dos sub-árboles independientes lado a lado** (izquierda: categorías 1-4 — Fundamentos, LLMs, Frameworks, Habilidades; derecha: categorías 5-7 — Bases de Datos, APIs, Despliegue), cada uno con su propio nodo raíz, tamaño de fuente fijo (sin downscale) y centrado verticalmente dentro de su panel — aprovecha el ancho completo del canvas 1200×627 sin comprimir el texto.

**Enlaces curvos (2026-09-25, corrección adicional pedida por el usuario)**: los enlaces en ángulo recto ("elbow links") se reemplazaron por curvas de Bézier cúbicas (estilo `d3.linkHorizontal`), calculadas con un punto de control en el punto medio horizontal entre nodo padre e hijo — look más orgánico, consistente con un dendrograma real. Además, cada etiqueta de categoría lleva un rectángulo blanco de máscara detrás del texto para que la curva pase visualmente por debajo de la etiqueta en vez de atravesarla (bug reportado: "el nombre del paso queda sobre la línea", ej. "6. APIs").

**Colores de marca combinados** (regla "varias marcas en una misma pieza") — paleta base verde+tierra del proyecto para la estructura, con íconos reales de marca donde aplica: Python, JavaScript, Git, Docker, Vercel, FastAPI, Meta (representa Llama), ChromaDB, OpenAI/ChatGPT, Anthropic/Claude, PostgreSQL, AWS.

**Íconos sin logo oficial disponible** (confirmado, ni en dashboardicons.com ni seeklogo.com para estos): LangChain, LangGraph, LlamaIndex, Pinecone, FAISS, GraphQL, MCP (Model Context Protocol), REST API genérico — se usa iconografía semántica genérica (nunca un logo aproximado a mano) para estos nodos específicos.

**Catálogo**: `categoriaPrincipal: "inteligencia-artificial"`, `temas: ["ia", "agentes-ia"]` — tema IA, aplica publicación inmediata.
