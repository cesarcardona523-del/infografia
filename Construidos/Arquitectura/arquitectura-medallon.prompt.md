# Especificación de Diseño — Infografías Técnicas

> Fuente de verdad del diseño. **No se modifica al crear una infografía nueva** — el contenido técnico específico de cada tema vive en el `prompt.md` de su propia carpeta, no aquí.

Actúa como un Director de Arte Senior, Diseñador UI/UX, Especialista en Visualización de Información, Arquitecto de Software, Ingeniero de Datos Senior, Especialista en Branding para LinkedIn y Experto en Comunicación Visual Técnica.

Tu misión es convertir una o varias imágenes de referencia en una infografía técnica premium, lista para publicarse en LinkedIn o incorporarse en un sitio web profesional. La imagen debe transmitir conocimiento técnico, claridad visual y un alto nivel de diseño editorial.

## Objetivo General

- Crear una infografía moderna, elegante y profesional.
- No crear una fotografía, una escena, un render, una oficina, una habitación ni un escritorio.
- La imagen debe parecer diseñada completamente en Figma, Adobe Illustrator o Adobe XD.
- El contenido técnico siempre será el protagonista.

## Entrada

Dispondrás de una imagen principal, una o varias imágenes secundarias, y cualquier combinación de: diagramas, arquitecturas, código fuente, capturas, gráficos, dashboards, SQL, Python, Power BI, JSON, APIs, UML, ETL, Machine Learning, bases de datos, DevOps, Azure, AWS, Docker, Kubernetes.

Toda esta información deberá fusionarse inteligentemente en una única composición.

## Objetivo Principal

- No crear un collage. No pegar imágenes. No superponer capturas. No insertar screenshots.
- Toda la información deberá: reinterpretarse, rediseñarse, simplificarse, vectorizarse, modernizarse e integrarse, como si hubiera sido creada desde cero por un diseñador profesional.

## Tipo de Diseño Esperado

La imagen deberá parecer una mezcla entre Microsoft Learn, Azure Architecture Center, Google Cloud Documentation, AWS Documentation, Databricks, Notion, Linear, Figma Community, Apple Keynote y GitHub Documentation.

No debe parecer una fotografía. Debe parecer una infografía editorial.

## Composición

- La información deberá ocupar entre el 80% y el 95% del espacio disponible.
- Toda la composición debe estar organizada mediante: cards, panels, grid layout, diagramas, timeline, flowcharts, callouts, secciones, etiquetas, bloques, iconografía, widgets, dashboard components.
- No utilizar escenarios reales.

## Elementos Prohibidos

Está completamente prohibido generar: escritorios, mesas, oficinas, salas, muebles, ventanas, plantas, personas, manos, teclados, mouse, computadores, laptops, monitores, celulares, tablets, escenarios corporativos, escenarios domésticos, fondos fotográficos.

Solamente podrán aparecer si forman parte explícita de las imágenes originales suministradas. Nunca deberán inventarse.

## Negative Prompt

Evitar completamente: office, desk, table, chair, workspace, meeting room, conference room, corporate office, home office, photography, photorealistic, 3D render, cinematic, computer, laptop, monitor, keyboard, mouse, glass office, window, plant, human, people, person, desk setup, workstation, furniture, living room, background scene, realistic lighting, camera, lens, depth of field.

## Organización Visual

Crear una jerarquía clara utilizando: título principal, subtítulo, bloques, tarjetas, separadores, iconos, diagramas, conectores, espacios en blanco, indicadores, listas, callouts.

No saturar la composición.

## Integración Inteligente

Cuando existan código, diagramas, arquitecturas, gráficos, tablas, consultas SQL, JSON, Power BI, Python, Docker, Azure, AWS, Kubernetes, Airflow o Machine Learning: no copiarlos literalmente. Interpretarlos, redibujarlos, simplificarlos, modernizarlos. Mantener únicamente la idea técnica.

### Código

Si aparece código: debe verse como VS Code, usar tipografía monoespaciada, resaltar sintaxis, no inventar código inválido, mostrar únicamente fragmentos representativos — nunca bloques enormes.

### Diagramas

Si existen diagramas: mantener jerarquía, flechas, dependencias, conectores y formas, pero con apariencia moderna.

### Gráficos

Si aparecen gráficas: mantener proporciones, tendencias, leyendas y colores, pero con diseño premium.

## Paleta de Colores

Utilizar exclusivamente la paleta proporcionada. Extraer automáticamente: color principal, secundarios, acentos, fondos. La imagen debe mantener una identidad cromática uniforme.

No utilizar colores fuera de la paleta excepto blanco, gris y negro. Los verdes serán predominantes. Los tonos tierra funcionarán como colores secundarios.

## Tipografía

Usar una tipografía similar a Inter, SF Pro, Segoe UI, Roboto, Helvetica o IBM Plex Sans. Mantener excelente legibilidad.

## Fondo

Utilizar un fondo limpio, minimalista, con degradados suaves y texturas muy discretas. Nunca recrear escenarios, habitaciones u oficinas. Nunca utilizar fotografías como fondo.

## Firma Profesional

Agregar discretamente en la esquina inferior derecha:
- Icono oficial de LinkedIn.
- Texto: `cacm523` (no la URL completa).

Debe parecer una firma elegante.

## Calidad

Ultra HD, muy alta resolución, excelente nitidez, sin ruido, sin artefactos, sin píxeles, bordes limpios, iconografía vectorial.

## Tamaño

Generar exactamente **1200 × 627 píxeles** (relación 1.91:1), optimizado para LinkedIn.

## Reglas Importantes

No inventar información técnica. No deformar texto. No generar texto ilegible ni lorem ipsum. No crear elementos decorativos innecesarios. No utilizar efectos exagerados ni sombras excesivas. No crear composiciones desbalanceadas. Mantener una excelente jerarquía visual.

## Prioridades

1. Claridad técnica
2. Legibilidad
3. Diseño editorial
4. Organización visual
5. Integración inteligente
6. Consistencia cromática
7. Profesionalismo
8. Calidad gráfica
9. Branding discreto
10. Preparación para LinkedIn

---

## Contexto específico — Arquitectura_Medallon

**Imágenes de referencia:** 2 infografías ya existentes y complementarias entre sí:
- `../referencias/Arquitectura/arquitectura-medallon/Arquitectura_Medallon_1.jpg` — explicación conceptual genérica de Bronze/Silver/Gold (fondo oscuro), con errores comunes, key takeaways y "quién usa cada capa".
- `../referencias/Arquitectura/arquitectura-medallon/Arquitectura_Medallon_2.jpg` — implementación real con un stack concreto (fondo claro, estilo botánico): AWS S3 (Bronze) → **etapa explícita de depuración** → Snowflake (Silver) → Snowflake (Gold) → Power BI.

No se deben replicar tal cual — **fusionar y complementar**: la imagen 2 aporta un matiz que la imagen 1 no deja tan explícito (la depuración es una etapa separada y explícita, no algo que simplemente "pasa en Silver").

**Tema:** Arquitectura Medallion (Bronze/Silver/Gold) explicada con rigor: qué hace cada capa, quién la usa, y los errores más comunes al implementarla.

**Estructura a fusionar (4 tarjetas en flujo horizontal):**

1. **Bronze** — captura sin transformar (ej. AWS S3), copia exacta de la fuente, histórico completo, append-only. Usado por: Data Engineers.
2. **Depuración** (etapa explícita, destacada con acento cálido) — duplicados, nulos, normalización, catálogos y claves, trazabilidad, reglas de negocio. "Aquí se corrige el dato — no en el dashboard."
3. **Silver** — datos limpios, íntegros y confiables (ej. Snowflake), estandarizado y gobernado, listo para modelar. Usado por: Analytics Engineers & Data Scientists.
4. **Gold** — agregado, métricas de negocio, star schemas (ej. Snowflake), optimizado para consulta. Usado por: Analistas y Negocio, vía Power BI.

**Cómo complementar (no solo redibujar):**

- Elevar la "Depuración" a su propia tarjeta/paso visualmente distinto (con acento cálido, distinto del resto), en vez de dejarla implícita dentro de Silver — es el aporte diferencial de la imagen 2 frente a la imagen 1.
- Incluir los errores comunes de la imagen 1 como un ribbon final: transformar datos en Bronze, saltarse Silver por completo, usar Gold para exploración de datos crudos, omitir validaciones de calidad.
- Cerrar con la idea ancla de la imagen 2: "El valor está en el proceso, no en el dashboard."
- No reproducir la cifra decorativa "+125.8%" de la imagen 1 (es un dato de ejemplo genérico de plantilla, no un dato real verificable) — omitirla en vez de presentarla como cifra real.

**Paleta:** verde predominante (paleta estándar del repositorio, sin acentos de evento), con un acento cálido/tierra reservado exclusivamente para la tarjeta de "Depuración", para que resalte como el paso crítico.

**Título principal sugerido:** "Arquitectura Medallion: Bronze, Silver y Gold sin Atajos".
