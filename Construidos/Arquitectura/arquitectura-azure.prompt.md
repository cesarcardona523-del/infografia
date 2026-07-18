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

## Branding

Agregar una marca de agua extremadamente discreta:
- Texto: `Cesar Cardona`
- Ubicación: diagonal o centro
- Opacidad: 5% — debe ser prácticamente invisible.

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

## Contexto específico — Arquitectura_Azure

**Imagen de referencia:** `../referencias/Arquitectura/arquitectura-azure/Arquitectura_Azure_Cloud.jpeg` (diagrama ya existente, "Modern Azure Data Pipeline & Medallion Architecture"). No se debe replicar tal cual — **complementarla**: mantener las 5 secciones y la arquitectura Medallón (Bronze/Silver/Gold), pero corregir el código ilegible de la referencia y agregar gobernanza que no tiene.

**Tema:** Arquitectura moderna de datos en Azure basada en el patrón Medallón (Bronze/Silver/Gold), de la ingesta hasta la visualización en Power BI.

**Estructura a mantener (5 secciones):**

1. **Data Sources** — APIs, Webhooks, dispositivos IoT.
2. **Ingestion & Staging** — Azure Data Factory (orquesta la copia), Azure Data Lake Storage Gen2 (landing zone).
3. **Medallion Processing** — tres capas apiladas: Bronze (raw, sin modelar), Silver (limpia, estructurada y validada) y Gold (agregada, lista para negocio), con Apache Spark ejecutando la limpieza/transformación entre capas.
4. **Analysis & Transform** — Azure Synapse Analytics (SQL pool dedicado).
5. **Presentation & Insights** — Power BI (dashboards interactivos).

**Cómo complementarla (no solo redibujar igual):**

- **Corregir el código ilegible de la referencia**: los bloques de código de Bronze/Silver/Gold en la referencia muestran texto corrupto/no funcional (ej. "nzore_dskes", "sicons:noueration"). Reemplazar por un único snippet SQL real y coherente en la capa Gold (ej. una tabla de KPIs agregada por región).
- **Agregar gobernanza que falta en la referencia**: incluir Microsoft Purview como capa de catalogación y linaje de datos entre las tres capas del Medallón — la referencia no menciona ningún mecanismo de gobernanza.
- **Explicitar el patrón de ingesta**: este flujo es batch vía Azure Data Factory; anotar que para ingesta en tiempo real el equivalente en Azure es Event Hubs + Stream Analytics (la referencia no distingue esto, y todo el diagrama sugiere solo batch).
- Mantener las 3 capas del Medallón visualmente diferenciadas con su color convencional (bronze = tono tierra cálido, silver = gris neutro, gold = tono dorado/tierra), dentro de la paleta permitida.

**Paleta:** verde predominante para el resto de la composición (Data Sources, Ingestion, Synapse, Power BI), con los tres acentos tierra (bronze/plata-gris/dorado) reservados exclusivamente para diferenciar las tres capas del Medallón.

**Título principal sugerido:** "Arquitectura de Datos en Azure: Patrón Medallón de Extremo a Extremo".
