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

## Contexto específico — Automatización_AgentesIA

**Imagen de referencia:** `../referencias/Automatización/automatizacion-agentesia/AI_Agents_vs_Non-Agentic_Systems.jpeg` (infografía ya existente, fondo oscuro, comparación de dos paneles). No se debe replicar tal cual — **complementarla**: mantener la comparación de dos bloques (No agéntico vs Agéntico) y el diagrama circular del orquestador, pero enriquecer con la lógica técnica de control y la capa de gobernanza que la referencia no explicita, y traducir el estilo al sistema de diseño claro/verde de INFOGRAFIA-SPEC.md (la referencia usa fondo oscuro y rojo/verde — aquí no se usa rojo, se usa gris neutro vs. verde para el contraste).

**Tema:** Diferencia arquitectónica entre sistemas de IA no agénticos (automatización tradicional) y sistemas agénticos (autónomos), y qué se necesita para llevar estos últimos a producción.

**Estructura a mantener (dos paneles + diagrama circular):**

1. **Panel "No Agéntico — Automatización"** (header gris neutro, no rojo):
   - Chatbots basados en LLM — responde preguntas puntuales, sin planificación ni memoria de objetivos.
   - RPA (Automatización Robótica de Procesos) — flujo determinista: gatillo → regla fija → acción.
   - RAG (Generación Aumentada por Recuperación) — recupera contexto de una base de conocimiento antes de responder, pero no decide ni ejecuta acciones por sí mismo.
2. **Panel "Agéntico — Autonomía"** (header verde), diagrama circular/radial:
   - Centro: Orquestador / LLM.
   - Satélites conectados en bucle: Memoria (descompone objetivos y define siguientes pasos), Planificación (diseña el plan de ejecución), Herramientas / APIs (ejecuta acciones sobre sistemas reales), Sub-Agentes (especialistas que colaboran en la tarea).
   - El lazo que conecta los 4 satélites representa los **bucles de retroalimentación**: evalúa resultados y ajusta el plan.

**Cómo complementarla (no solo redibujar igual):**

- Explicitar la diferencia de **flujo de control**: no agéntico = flujo fijo, definido por el desarrollador antes de ejecutarse; agéntico = flujo dinámico, decidido por el propio LLM en cada paso según el resultado anterior. La referencia no lo dice en estos términos.
- Agregar una capa de **gobernanza de IA** como callout transversal (equivalente al callout de seguridad que usamos en la infografía de AWS): observabilidad de cada paso del agente, límites de herramientas/permisos por rol, y guardrails contra alucinación — requisitos antes de delegar acciones autónomas sobre sistemas de producción. La referencia no menciona riesgos ni gobernanza.
- Mantener la frase ancla de la referencia ("La automatización sigue órdenes. La autonomía las resuelve.") como tagline, integrada al header en vez de como bloque aparte.
- No usar rojo para el panel "No agéntico" (fuera de la paleta permitida) — usar gris/neutro para ese contraste, reservando el verde para "Agéntico".

**Paleta:** verde predominante para el panel/diagrama agéntico; gris neutro (no rojo) para el panel no agéntico; ribbon de gobernanza en navy oscuro, igual que el patrón ya usado en la infografía de Arquitectura AWS.

**Título principal sugerido:** "Automatización vs Autonomía: Arquitectura de Sistemas de IA Agénticos".
