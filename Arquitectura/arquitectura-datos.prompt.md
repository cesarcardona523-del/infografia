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

## Contexto específico — Arquitectura_Datos

**Imagen de referencia:** `../referencias/Arquitectura/arquitectura-datos/Arquitectura_Datos.jpg` (cuadro comparativo ya existente, formato 3×3, fondo claro). No se debe replicar tal cual — **complementarla**: mantener los 9 patrones y su estructura de comparación, pero traducirla al sistema de diseño de este repositorio y agregar una guía de decisión que la referencia no tiene.

**Tema:** Panorama comparativo de los 9 patrones de arquitectura de datos más usados en la industria.

**Los 9 patrones a mantener (grid 3×3):**

1. **Data Warehouse** — Sources → ETL → Warehouse. Repositorio centralizado para datos estructurados, optimizado para análisis histórico.
2. **Data Lake** — Sources → Ingestion → Lake (Raw/Refined) → Analysis. Almacén flexible para datos crudos y estructurados a gran escala, bajo costo.
3. **Lambda Architecture** — Sources → Batch Layer + Speed Layer → Serving Layer → Queries. Combina procesamiento por lotes y en tiempo real para vistas completas.
4. **Kappa Architecture** — Sources → Speed Layer (Stream) → Serving Layer → Queries. Procesa todo como un flujo continuo, simplificando Lambda.
5. **Data Mesh** — Domain A/B/C Product → Self-Service Platform & Governance. Enfoque descentralizado basado en dominios, tratando los datos como producto.
6. **Data Lakehouse** — Sources → Lakehouse (Metadata, ACID) → BI & AI. Unifica Data Lake y Data Warehouse, soportando BI y ML con gestión transaccional.
7. **Data Fabric** — Sources → Fabric (Integración Inteligente, Metadata Activa) → Consumers. Capa de gestión inteligente y automatizada que conecta datos dispersos.
8. **Event-Driven Architecture** — Producers → Event Broker → Consumer A/B. Arquitectura reactiva donde los servicios se comunican mediante eventos asíncronos.
9. **Streaming Architecture** — Streaming Sources → Stream Processing → Real-time Storage/Action. Procesamiento continuo de datos en movimiento para perspectivas inmediatas.

**Cómo complementar (no solo redibujar):**

- Agregar un bloque final de "cómo elegir" con un criterio real y verificable (no inventado): estos patrones no son mutuamente excluyentes — un Data Lakehouse moderno con frecuencia incorpora ingesta event-driven, y una arquitectura Kappa puede verse como una simplificación de Lambda cuando el batch layer deja de ser necesario. La elección real depende de la latencia requerida, el nivel de gobernanza deseado (centralizada vs. por dominio) y el presupuesto de almacenamiento/cómputo disponible.
- Mantener las 9 tarjetas con igual jerarquía visual (grid 3×3), con encabezados uniformes en verde (paleta estándar del repositorio, sin la paleta arriesgada de las infografías de evento — esta es una publicación regular).
- Usar acentos tierra solo para 1–2 patrones híbridos que convenga destacar (ej. Lambda/Kappa, por combinar batch y streaming).

**Título principal sugerido:** "Arquitecturas de Datos: 9 Patrones que Todo Arquitecto Debe Conocer".
