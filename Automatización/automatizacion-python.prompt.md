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

## Contexto específico — Automatizacion_Python

**Imagen de referencia:** `../referencias/Automatización/automatizacion-python/Automatizacion_Python.jpeg` (infografía ya existente, fondo oscuro). No se debe replicar tal cual — **complementarla**: mantener el flujo general (Excel → carga estructurada → procesamiento en Python → salida dual a SQL y Email) y la métrica de eficiencia visible en la referencia, pero corrigiendo un bug real del snippet de código y agregando buenas prácticas de producción que la referencia no tiene.

**Tema:** Pipeline de automatización ETL con Python que reemplaza procesos manuales en hojas de cálculo.

**Estructura a mantener (4 etapas en flujo horizontal):**

1. **Origen de Datos** — archivo Excel/CSV con datos de ventas u operación diaria.
2. **Carga Estructurada** — pandas lee y valida el archivo antes de procesar.
3. **Procesamiento (Python)** — limpieza, transformación y reglas de negocio, con snippet de código.
4. **Salida dual** — Base de Datos (SQL), almacenamiento seguro; y Comunicación (Email), envío automático de alertas/reportes.

**Panel lateral (mantener las 3 tarjetas de la referencia, pero 2 de ellas rediseñadas):**

- **Impacto/Eficiencia** — mantener la cifra "75%" de reducción de tiempo operativo visible en la referencia (es un dato que trae la propia imagen, no se inventa), enmarcada como comparación frente al proceso manual.
- **Calidad de datos**: la referencia trae un gráfico de barras ambiguo (ejes/leyenda poco claros, "Errores" vs. una serie sin etiqueta legible) — **no reproducir ese gráfico** (sería inventar datos que no se pueden leer con certeza). Reemplazar por una comparación cualitativa **Antes vs. Después**: manual/propenso a error humano vs. automatizado/validado programáticamente.
- **Casos de Uso** — mantener igual que la referencia: Dashboards Activos, Reportes Diarios, Limpieza de Datos.

**Cómo complementarla (no solo redibujar igual):**

- **Corregir el bug del snippet**: la referencia repite la misma línea de filtro dos veces (`df_clean = df[df['Ventas'] > 1000]` aparece duplicada) — en la versión nueva, mostrar el snippet correcto y coherente (filtro una sola vez, cálculo de `Ganancia`, guardado en SQL).
- **Agregar buena práctica de seguridad que falta en la referencia**: la referencia muestra el connection string de la base de datos con usuario y contraseña en texto plano (`postgresql://usr:pwd@host/db`) directamente en el código — corregir esto en el snippet nuevo usando una variable de entorno (`os.environ["DATABASE_URL"]`), y explicitarlo como práctica recomendada en un callout de gobernanza (mismo patrón que las infografías anteriores de Arquitectura/Automatización): credenciales vía variables de entorno o secret manager, manejo de excepciones con reintentos, y logging estructurado de cada corrida.
- Mantener la recomendación de escalabilidad ya usada para este mismo tema en el sitio: para volúmenes grandes, considerar Apache Airflow o Apache Spark en vez de un script aislado.

**Paleta:** verde predominante (coherente con el resto de infografías de este repo), evitar el fondo oscuro de la referencia — usar el fondo claro/editorial de INFOGRAFIA-SPEC.md.

**Título principal sugerido:** "Automatización de Reportes con Python: de Excel a Producción".
