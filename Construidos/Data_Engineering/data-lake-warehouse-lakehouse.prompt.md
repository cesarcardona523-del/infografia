# Especificación de Diseño — Infografías Técnicas

> Fuente de verdad del diseño — evoluciona con el proyecto (ver "Rol permanente y mejora continua" en CLAUDE.md). **No se modifica con contenido técnico específico de un tema** — eso vive en el `prompt.md` de su propia carpeta. Solo se actualiza aquí cuando una mejora de diseño generaliza a todas las infografías.

Actúa como un Director de Arte Senior, Diseñador UI/UX, Especialista en Visualización de Información, Arquitecto de Software, Ingeniero de Datos Senior, Especialista en Branding para LinkedIn y Experto en Comunicación Visual Técnica.

Tu misión es convertir una o varias imágenes de referencia en una infografía técnica premium, lista para publicarse en LinkedIn o incorporarse en un sitio web profesional. La imagen debe transmitir conocimiento técnico, claridad visual y un alto nivel de diseño editorial.

(Ver el archivo raíz `INFOGRAFIA-SPEC.md` para el contenido completo compartido por todo el catálogo — paleta, tipografía, composición, elementos prohibidos, branding, firma, tamaño 1200×627px.)

## Contexto específico — Data Lake vs Data Warehouse vs Data Lakehouse

**Tema**: los tres enfoques principales para almacenar y trabajar con datos en una organización — mismo objetivo (convertir datos en información útil), distinto enfoque de estructura y gobierno.

**Referencias suministradas por el usuario** (2 imágenes pegadas en el chat, sin archivo guardado en disco — contenido analizado directamente de la conversación):
1. Infografía "¿Qué es un Data Lake?" — metáfora de lago con fuentes de datos entrando desde la izquierda (bases de datos, apps, APIs, archivos, documentos, logs, IoT, multimedia), formatos de archivo flotando dentro del lago (CSV, JSON, TXT, PDF, imágenes, video, código), usos saliendo a la derecha (BI, análisis exploratorio, ML, IA/agentes, data warehouse, gobierno), atributos clave (escalable, económico, flexible), y un flujo de 4 pasos (ingesta → almacenamiento → procesamiento → consumo).
2. Infografía "3 formas de trabajar con datos" — comparativa de 3 columnas (Data Lake "El Lago", Data Warehouse "El Depósito Ordenado", Data Lakehouse "La Casa Inteligente"), cada una con: mini-diagrama de entrada/salida de datos, lista de características, y un panel "Ideal para". Cierra con una fila "En simple" resumiendo cada enfoque en una frase.

**Decisión de composición**: no existía ninguna pieza en el catálogo que comparara los 3 enfoques (`Data_Engineering/` solo tenía ETL/ELT/ETLT/Reverse ETL y la matriz de habilidades) — se crea una pieza nueva en vez de modificar una existente. Se combina el contenido de las 2 referencias (la definición de Data Lake de la imagen 1 + la comparativa de 3 vías de la imagen 2) en una sola infografía enfocada en la comparación de los 3 enfoques, ya que es el ángulo con más valor diferencial para el catálogo — la definición aislada de "qué es un Data Lake" queda cubierta como la primera de las 3 columnas.

**Estructura elegida** (variante del "blueprint numerado" de INFOGRAFIA-SPEC.md, adaptada a comparación de 3 vías en vez de arquitectura en capas):
- Header con eyebrow + título + subtítulo + callout de cita con la idea-fuerza ("Data Lake = guardás todo. Data Warehouse = entendés y organizás. Data Lakehouse = ambas, a la vez").
- 3 columnas iguales, cada una con insignia numerada (1, 2, 3) y color propio dentro de la familia verde+tierra (Data Lake = verde principal, Data Warehouse = tierra/naranja acento, Data Lakehouse = verde oscuro/teal que combina ambos, transmitiendo visualmente "combina lo mejor de los dos").
- Cada columna: nombre + metáfora ("El Lago" / "El Depósito Ordenado" / "La Casa Inteligente"), 3-4 características reales (no inventadas — tomadas de ambas referencias), un panel "Ideal para" con remate.
- Banda transversal inferior "En Simple" con las 3 frases resumen, una por columna, separadas visualmente.
- Firma profesional (LinkedIn + cacm523) en la esquina inferior derecha del footer.

**Paleta**: verde+tierra por defecto (pieza comparativa entre 3 conceptos genéricos de arquitectura de datos, no sobre una herramienta con marca propia — no aplica la excepción de "Colores de marca por aplicación").

**Iconografía**: íconos semánticos genéricos (base de datos, nube, API, documento, IoT, gráfico de barras, cerebro/ML, escudo de gobierno, casa) — ninguno de estos es una marca comercial, por lo que se dibujan como SVG simple en vez de requerir `assets/iconos-apps/`.

**Catálogo**: `categoriaPrincipal: "ingenieria-de-datos"`, `temas: ["data-engineering", "arquitectura-datos"]` — mismo tema de carpeta `Data_Engineering` usado por la pieza ETL/ELT/ETLT/Reverse ETL ya existente.
