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

**Excepción — infografías de evento:** si la infografía se crea para un evento específico (variables `Evento` y/o `Realizado por`, ver sección "Branding de Evento"), la paleta puede ser más arriesgada y no está limitada al verde predominante de esta spec — se puede adoptar la paleta del evento o de la organización que lo realiza, siempre manteniendo blanco/gris/negro como neutros de apoyo y sin sacrificar legibilidad ni jerarquía visual.

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

## Branding de Evento (opcional)

Aplica únicamente si el usuario especifica, al crear la infografía, un **Evento** y/o una organización en **Realizado por**.

- Mostrar de forma visible (no como marca de agua casi invisible) el nombre del evento, ej. `Datafest 2026`.
- Mostrar `Realizado por: <Organización>` — ej. `Realizado por: Bancolombia`.
- Buscar el logo oficial de esa organización; si se encuentra uno confiable, usarlo en vez de texto plano. Si no se encuentra, mostrar solo el nombre en texto.
- Esta información es adicional a la marca de agua ("Cesar Cardona" al 5%) y a la firma profesional (LinkedIn + `cacm523`) — ambas se mantienen sin cambios; el branding de evento no las reemplaza.
- Ubicación sugerida: encabezado o pie de la infografía, en un bloque discreto pero legible, sin competir visualmente con el título principal.

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

## Contexto específico — Analisis_Datos_IA

**Evento:** Datafest 2026 — **Realizado por:** Bancolombia (aplica la excepción de paleta y la sección "Branding de Evento" de arriba).

**Imágenes de referencia:** 3 capturas de diapositivas reales presentadas en Datafest 2026 (`../referencias/IA/analisis-datos-ia/Analitica_Datos_1.png`, `_2.png`, `_3.png`). Son contenido genuino de la charla, no una infografía terminada — el trabajo es **traducir las 3 diapositivas a una sola infografía editorial coherente**, no copiarlas como screenshots.

**Tema de la charla:** Evolución del análisis de datos y los cambios que vienen — de registrar datos a delegar tareas en agentes de IA.

**Contenido a fusionar (de las 3 diapositivas):**

1. **Viaje de madurez en 7 etapas** (diapositiva 1): Digitalizar (Capturar) → Datos (Almacenar) → Automatizar (Ejecutar) → Analítica (Entender) → ML (Anticipar) → GenIA (Explicar) → Agentes (Actuar). Mensaje clave: "No todos los procesos necesitan llegar al último nivel."
2. **Regla simple para decidir** (diapositiva 2): tabla de decisión — pasos repetitivos y reglas claras → Automatización/RPA; encontrar patrones o priorizar → Analítica/ML; solo una respuesta o resumen → GenIA; ejecutar un flujo completo → Agente; excepción/ética/riesgo/criterio crítico → Persona experta.
3. **Tres conceptos clave en lenguaje de líder** (diapositiva 3): IA (entiende patrones y apoya decisiones), GenIA (lee, escribe, resume y explica), Agente (ejecuta pasos y gestiona tareas). Cierre: "No debemos enamorarnos de la tecnología. Debemos enamorarnos del problema que queremos resolver."

**Investigación adicional:** se buscó contexto público sobre Datafest 2026 y Bancolombia — no se encontró cobertura pública específica de esta charla (parece un evento interno/no masivamente indexado), por lo que el contenido se basa fielmente en lo que muestran las 3 diapositivas, sin inventar datos adicionales no presentes en ellas.

**Paleta (investigada):** Bancolombia usa negro/blanco como base de marca desde su renovación de 2021, con amarillo como "color de la confianza" y un set de tonos vibrantes adicionales para representar diversidad — exactamente lo que ya usan las diapositivas originales (fondo oscuro, círculos de colores vibrantes: teal, verde, dorado, rojo-naranja, morado, rosa). Mantener ese mismo lenguaje cromático en la infografía final.

**Branding de evento:**
- Mostrar "Datafest 2026" de forma visible (chip/badge, no solo marca de agua).
- Mostrar "Realizado por: Bancolombia" — no se usó un logo descargado de internet (por precaución de derechos de marca de un asset externo); se usa un wordmark de texto "Bancolombia" en su amarillo de marca.
- Mantener la firma personal (LinkedIn + cacm523) y la marca de agua "Cesar Cardona" al 5% sin cambios.

**Título principal sugerido:** "Evolución del Análisis de Datos: de Registrar Datos a Delegar Tareas".
