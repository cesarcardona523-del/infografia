# Especificación de Diseño — Infografías Técnicas

> Fuente de verdad del diseño — evoluciona con el proyecto (ver "Rol permanente y mejora continua" en CLAUDE.md). **No se modifica con contenido técnico específico de un tema** — eso vive en el `prompt.md` de su propia carpeta. Solo se actualiza aquí cuando una mejora de diseño generaliza a todas las infografías.

Actúa como un Director de Arte Senior, Diseñador UI/UX, Especialista en Visualización de Información, Arquitecto de Software, Ingeniero de Datos Senior, Especialista en Branding para LinkedIn y Experto en Comunicación Visual Técnica.

Tu misión es convertir una o varias imágenes de referencia en una infografía técnica premium, lista para publicarse en LinkedIn o incorporarse en un sitio web profesional. La imagen debe transmitir conocimiento técnico, claridad visual y un alto nivel de diseño editorial.

## Objetivo General

- Crear una infografía moderna, elegante y profesional.
- No crear una fotografía, una escena, un render, una oficina, una habitación ni un escritorio.
- La imagen debe parecer diseñada completamente en Figma, Adobe Illustrator o Adobe XD.
- El contenido técnico siempre será el protagonista.

## Entrada

Dispondrás de una referencia principal, una o varias referencias secundarias, y cualquier combinación de: diagramas, arquitecturas, código fuente, capturas, gráficos, dashboards, SQL, Python, Power BI, JSON, APIs, UML, ETL, Machine Learning, bases de datos, DevOps, Azure, AWS, Docker, Kubernetes.

**Las referencias no siempre son imágenes.** También pueden llegar como PDF, presentaciones (PPTX) o documentos de Word (DOCX) — por ejemplo, el material de una charla, un informe técnico, o unas diapositivas de un evento. En esos casos, antes de diseñar:

1. Extraer y analizar el contenido real del archivo (texto, diapositivas, tablas, diagramas embebidos) — usando las herramientas de lectura de PDF/PPTX/DOCX disponibles — en vez de asumir o inventar qué contenía.
2. Identificar de ese análisis los mismos elementos que se buscarían en una imagen de referencia: el tema técnico, la estructura/flujo que se quiere comunicar, y cualquier dato comparable o tabular real.
3. Usar ese análisis como insumo para la sección "Contexto específico" del `.prompt.md`, igual que se haría con una imagen — el resultado final sigue siendo una infografía (HTML → PNG), nunca una copia del PDF/PPTX/DOCX original.

Toda esta información —sea imagen, PDF, PPTX o DOCX— deberá fusionarse inteligentemente en una única composición.

## Objetivo Principal

- No crear un collage. No pegar imágenes. No superponer capturas. No insertar screenshots.
- Toda la información deberá: reinterpretarse, rediseñarse, simplificarse, vectorizarse, modernizarse e integrarse, como si hubiera sido creada desde cero por un diseñador profesional.

## Tipo de Diseño Esperado

La imagen deberá parecer una mezcla entre Microsoft Learn, Azure Architecture Center, Google Cloud Documentation, AWS Documentation, Databricks, Notion, Linear, Figma Community, Apple Keynote y GitHub Documentation.

No debe parecer una fotografía. Debe parecer una infografía editorial.

## Composición

- La información deberá ocupar entre el 80% y el 95% del espacio disponible.
- Toda la composición debe estar organizada mediante: cards, panels, grid layout, diagramas, timeline, flowcharts, callouts, secciones, etiquetas, bloques, iconografía, widgets, dashboard components.
- Opcionalmente, dentro de tarjetas o paneles: glassmorphism moderado (blur sutil + borde translúcido) y layouts tipo Bento Grid (bloques de distinto tamaño en una misma grilla) son composiciones válidas, siempre que no compitan con la paleta verde dominante ni con la legibilidad.
- No utilizar escenarios reales.

## Elementos Prohibidos

Está completamente prohibido generar: escritorios, mesas, oficinas, salas, muebles, ventanas, plantas, personas, manos, teclados, mouse, computadores, laptops, monitores, celulares, tablets, escenarios corporativos, escenarios domésticos, fondos fotográficos.

Solamente podrán aparecer si forman parte explícita de las imágenes originales suministradas. Nunca deberán inventarse.

## Negative Prompt

Evitar completamente: office, desk, table, chair, workspace, meeting room, conference room, corporate office, home office, photography, photorealistic, 3D render, cinematic, computer, laptop, monitor, keyboard, mouse, glass office, window, plant, human, people, person, desk setup, workstation, furniture, living room, background scene, realistic lighting, camera, lens, depth of field.

## Organización Visual

Crear una jerarquía clara utilizando: título principal, subtítulo, bloques, tarjetas, separadores, iconos, diagramas, conectores, espacios en blanco, indicadores, listas, callouts.

No saturar la composición.

## Aprovechamiento del Espacio (sin espacios vacíos)

El canvas de 1200×627px debe sentirse lleno y equilibrado — nunca con franjas grandes de fondo vacío ni tarjetas con mucho más padding del que su contenido necesita. Antes de dar una pieza por terminada, verificar explícitamente:

- **Ninguna tarjeta o panel debe quedar con más de ~30-40% de su alto en blanco** debajo de su contenido. Si una tarjeta tiene mucho más espacio del que su texto ocupa, es señal de que falta contenido real (un dato derivado, un ejemplo, un mini-diagrama, un detalle técnico adicional) — nunca de que hay que agrandar el espaciado para "llenarla".
- **Contenido antes que espaciado.** Si una sección se ve vacía, la solución por defecto es sumar información real y verificable relacionada con el tema (un ejemplo concreto, una cifra ya mostrada en otra parte de la pieza, una consecuencia práctica, un "por qué importa") — no estirar `padding`, `gap` ni usar `justify-content: center/space-between` para distribuir dos o tres líneas de texto en un contenedor mucho más alto que ellas.
- **El tamaño de fuente es una herramienta de ajuste fino, no la primera respuesta.** Está permitido y es válido ajustar tamaños de letra, iconos y espaciados para que el contenido llene mejor su contenedor (ni tan grande que desborde el canvas, ni tan chico que dejen huecos) — pero ese ajuste se hace *después* de asegurar que hay suficiente contenido real, nunca en su lugar. Igual de importante: nunca reducir agresivamente una fuente solo para que quepa más texto forzado — ver la regla de legibilidad en CLAUDE.md.
- **Verificar antes de exportar** (con el mismo método de medición real contra Chrome headless que se usa para detectar overflow): además de que nada se salga del canvas, que ninguna tarjeta/columna quede con un vacío inferior o central obviamente mayor al de sus tarjetas vecinas — si una columna de una grilla queda visiblemente más corta que las demás, es la misma señal de contenido faltante.
- Esto aplica tanto a piezas nuevas como a piezas ya construidas que se estén regenerando por mejora continua.

## Integración Inteligente

Cuando existan código, diagramas, arquitecturas, gráficos, tablas, consultas SQL, JSON, Power BI, Python, Docker, Azure, AWS, Kubernetes, Airflow o Machine Learning: no copiarlos literalmente. Interpretarlos, redibujarlos, simplificarlos, modernizarlos. Mantener únicamente la idea técnica.

### Código

Si aparece código: debe verse como VS Code, usar tipografía monoespaciada, resaltar sintaxis, no inventar código inválido, mostrar únicamente fragmentos representativos — nunca bloques enormes.

### Diagramas

Si existen diagramas: mantener jerarquía, flechas, dependencias, conectores y formas, pero con apariencia moderna.

### Gráficos

Si aparecen gráficas: mantener proporciones, tendencias, leyendas y colores, pero con diseño premium.

## Riqueza Visual (evitar diseños planos)

Ninguna infografía debe depender únicamente de tarjetas de texto con viñetas. Cuando el contenido lo permita:

- **Datos comparables, cifras o relaciones tabulares** → representarlos como gráfico (barras, dona/gauge, funnel, línea) o tabla real, no como lista de viñetas. Si la referencia trae una cifra verificable, usarla en el gráfico; si no hay cifras reales, usar visualizaciones **conceptuales/cualitativas** (ej. un funnel que se angosta para representar refinamiento progresivo) sin inventar números específicos para rellenarlas.
- **Iconografía con propósito**: cada ícono debe representar semánticamente el concepto exacto (una base de datos, un flujo, una capa de gobernanza), no ser un ícono genérico intercambiable.
- **Al menos un elemento gráfico no textual** por infografía (diagrama, gráfico, tabla o ilustración de flujo), además de las tarjetas de texto — esto es lo que evita que el diseño se sienta plano.
- Esto no reemplaza la regla de "no inventar información técnica": todo elemento visual debe derivarse de lo que la referencia o el usuario aportó, nunca de datos fabricados para verse mejor.

## Paleta de Colores

Utilizar exclusivamente la paleta proporcionada. Extraer automáticamente: color principal, secundarios, acentos, fondos. La imagen debe mantener una identidad cromática uniforme.

No utilizar colores fuera de la paleta excepto blanco, gris y negro. Los verdes serán predominantes. Los tonos tierra funcionarán como colores secundarios.

Cada infografía debe usar al menos un color de acento además del verde principal (ej. un tono tierra para destacar un elemento crítico) para que la composición no se sienta monocromática o plana — la variación de color es también una herramienta de jerarquía visual, no solo de marca.

**Excepción — infografías de evento:** si la infografía se crea para un evento específico (variables `Evento` y/o `Realizado por`, ver sección "Branding de Evento"), la paleta puede ser más arriesgada y no está limitada al verde predominante de esta spec — se puede adoptar la paleta del evento o de la organización que lo realiza, siempre manteniendo blanco/gris/negro como neutros de apoyo y sin sacrificar legibilidad ni jerarquía visual.

**Excepción — paleta arriesgada por diferenciación dentro de un mismo tema:** cuando varias infografías conviven en la misma carpeta `Construidos/<Tema>/` (ej. varias piezas sobre "Dashboard" o "Bigdata"), usar verde+tierra en todas hace que se vean intercambiables entre sí. En ese caso está permitido asignarle a una pieza puntual una paleta secundaria distinta y arriesgada (ej. azul petróleo + coral, grafito + ámbar, teal + violeta) en vez de verde+tierra, siempre que:
- Se mantenga **una sola paleta secundaria por pieza** (no mezclar tres o más familias de color en la misma infografía) y blanco/gris/negro como neutros de apoyo.
- No se reutilice la misma paleta secundaria ya usada por otra pieza del mismo `<Tema>` — el objetivo es que cada una se distinga de un vistazo dentro de esa carpeta, no acumular colores al azar.
- La firma personal (LinkedIn + `cacm523`) y la calidad de contraste/legibilidad se mantengan sin cambios.
- Esta excepción es una decisión de diseño consciente para esa pieza puntual, no un default — la mayoría de las infografías del catálogo sigue usando verde+tierra; se reserva para cuando de verdad hace falta distinguir piezas muy similares entre sí dentro del mismo tema.

## Tipografía

Usar una tipografía similar a Inter, SF Pro, Segoe UI, Roboto, Helvetica o IBM Plex Sans. Mantener excelente legibilidad.

## Fondo

Utilizar un fondo limpio, minimalista, con degradados suaves y texturas muy discretas. Nunca recrear escenarios, habitaciones u oficinas. Nunca utilizar fotografías como fondo.

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
- Esta información es adicional a la firma profesional (LinkedIn + `cacm523`) — se mantiene sin cambios; el branding de evento no la reemplaza.
- Ubicación sugerida: encabezado o pie de la infografía, en un bloque discreto pero legible, sin competir visualmente con el título principal.

## Insignia de Actualización (opcional)

Aplica únicamente cuando una infografía **ya existente** se regenera con aporte real de contenido nuevo, dentro del flujo de consolidación (ver "Gestión inteligente de publicaciones e infografías" en CLAUDE.md) — la misma condición que activa la actualización de `fechaPublicacion`. No aplica a correcciones menores de estilo, ortografía, formato o CSS.

- Mostrar una insignia pequeña con el texto `Actualizada` (opcionalmente con fecha corta, ej. `Actualizada · Jul 2026`) en la parte superior de la infografía, cerca del encabezado.
- Estilo: badge tipo pill, consistente con los demás badges/etiquetas de la pieza (paleta verde o acento tierra), discreto y legible — nunca un sello dramático ni una marca de agua.
- Ubicación sugerida: esquina superior derecha o izquierda del canvas, junto al eyebrow o al título — nunca superpuesta al título principal ni compitiendo con él.
- Es independiente de la firma profesional y del branding de evento — las tres pueden convivir en la misma pieza si corresponde.
- Al archivar una versión previa (paso 1 de la consolidación), la insignia no se agrega retroactivamente a la copia archivada — solo aparece en el asset activo regenerado.

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

## Contexto específico — Encuesta Gen Z y Millennials 2026 (Deloitte Global)

**Fuente**: Deloitte Global, *Encuesta Gen Z y Millennials 2026 — "Progreso en sus propios términos"*. 15.º aniversario de la investigación (iniciada como "The Voice of Millennials"). Carta introductoria firmada por **Elizabeth Faber**, Deloitte Global Chief People & Purpose Officer. Más de **22,500 encuestados** de Gen Z (nacidos 1995–2007) y millennials (nacidos 1983–1994) en **44 países**, más entrevistas cualitativas a líderes empresariales. Archivo de referencia: `referencias/Liderazgo/encuesta-genz-millennials-2026-deloitte/2026_GenZ_millennials_espanol.md` (extraído del PDF original de Deloitte).

**Autoría — obligatorio dejarla visible en la pieza**: toda cifra y hallazgo pertenece a Deloitte Global; la infografía debe atribuir la fuente de forma clara y legible (ej. "Fuente: Deloitte Global — Encuesta Gen Z y Millennials 2026", con mención a Elizabeth Faber como firma del informe), nunca presentarse como investigación propia.

**Tipo de pieza**: no hay imagen de referencia visual — el insumo es enteramente el contenido en Markdown del informe. Se construye la infografía interpretando y jerarquizando ese contenido (ver metodología `design-audit/REFERENCE_BASED_REDESIGN.md` para jerarquización en 4 niveles y composición por zonas, aplicada aquí sin imagen de referencia, solo con el Markdown).

### Hallazgos clave a comunicar (cifras reales del informe, no inventar ninguna adicional)

**1. Presión financiera (Cap. 1)**
- El costo de vida es la principal preocupación por 5.º año consecutivo: 38% Gen Z / 42% millennials.
- 55% de Gen Z y 52% de millennials han retrasado decisiones de vida importantes (casarse, familia, negocio, estudios) por su situación financiera.
- 69% de Gen Z y 64% de millennials dicen que la vivienda impacta directamente sus decisiones de carrera.
- 51% de Gen Z y 40% de millennials no pueden costear una casa propia.
- Señal de mejora: 53% de Gen Z y 45% de millennials esperan que su situación financiera mejore en 12 meses (vs. 49%/41% en 2025); vivir "de sueldo a sueldo" bajó de 52% a 47% en ambas generaciones.

**2. Liderazgo reconsiderado (Cap. 2)**
- Solo 6% de Gen Z y millennials dice que llegar a un puesto de liderazgo es su principal objetivo de carrera.
- Pero 76% de Gen Z y 67% de millennials sí están interesados en liderazgo ejecutivo en algún momento de su carrera (80%/73% en roles de supervisión/gestión) — no es rechazo, es condicionamiento.
- Barreras principales para no priorizar liderazgo: estrés/burnout (50%/49%), responsabilidad excesiva (50%/48%), balance vida-trabajo (41%/46%).
- Lo que aumentaría el interés: mayor compensación (53%/57%), esquemas flexibles (42%/44%), claridad de ruta a liderazgo (36%/35%).
- 69% de ambas generaciones cree que puede impulsar cambios en su organización aunque no ocupe un cargo de liderazgo.

**3. Aprendizaje continuo y adaptabilidad (Cap. 3)**
- Fortalezas actuales: ética de trabajo, colaboración, empatía, adaptabilidad, pensamiento crítico.
- Habilidades que más quieren desarrollar: hablar en público, liderazgo, fluidez en IA, comunicación, creatividad (Gen Z); fluidez en IA/alfabetización digital lidera en millennials (42%).
- 1 de cada 3 experimentó más de 15 cambios laborales importantes en el último año (Deloitte Human Capital Trends 2026).

**4. IA y brecha de preparación (Cap. 4)**
- 74% de Gen Z y 74% de millennials ya usan IA en su trabajo diario (frente a 57%/56% hace un año) — fuerte aceleración.
- Uso más allá de productividad: identificar aprendizaje/desarrollo (79%/79%), consejo profesional (72%/69%), afrontar estrés laboral (67%/65%).
- Pero ~30% cree que su organización no está preparada para los cambios que traerá la IA (30% Gen Z / 31% millennials).
- 84% de las empresas no han rediseñado los puestos en torno a las capacidades de IA (Deloitte State of AI in the Enterprise 2026).
- Confianza: 68%/66% se siente capaz de usar IA por sí mismo, pero solo 60%/60% confía en la capacidad de sus líderes senior.

**5. Bienestar como infraestructura (Cap. 5)**
- Salud mental "buena o extremadamente buena": 63% Gen Z (vs 52% en 2025), 66% millennials (vs 58% en 2025) — mejora clara.
- Pero ~1 de cada 3 se siente ansioso/estresado la mayor parte del tiempo o todo el tiempo; ~48%/45% se siente "quemado" (burnout).
- Fatiga digital: 58% Gen Z / 54% millennials.
- Progreso institucional: 69% siente que su empleador toma en serio la salud mental (+14/+15 pts desde 2024); 65% dice que su empleador tiene políticas de apoyo (+14/+12 pts).

**6. Propósito y conexión (Cap. 6)**
- 96% de Gen Z y 97% de millennials dice que el propósito en el trabajo es importante para su satisfacción laboral y bienestar.
- ~40% ha rechazado una asignación o un empleador potencial por ética/creencias personales.
- 68% Gen Z / 72-73% millennials sienten que su trabajo actual les permite hacer una contribución significativa a la sociedad.
- Amistades cercanas en el trabajo se asocian con mayor permanencia: +15 puntos porcentuales en Gen Z, +18 en millennials, en la probabilidad de planear quedarse más de 5 años.

### Metáfora visual y composición sugerida

Evitar el genérico "grid de tarjetas iguales". Se sugiere una metáfora de **"balanza" o "brújula generacional"**: un eje central que contrasta Gen Z vs. millennials en cada hallazgo (barras comparativas pareadas), organizado en 5-6 bloques temáticos (Dinero, Liderazgo, Aprendizaje/IA, Bienestar, Propósito) alrededor de un mensaje central — "Progreso en sus propios términos" — con un KPI hero destacado (ej. 22,500 encuestados / 44 países) como ancla de credibilidad del estudio.

### Paleta

Paleta verde + tierra por defecto del proyecto (no es una infografía de aplicación/marca específica). Usar un acento adicional para diferenciar visualmente "Gen Z" de "Millennials" dentro de la misma familia cromática (ej. verde oscuro para millennials, verde/ámbar más claro para Gen Z), manteniendo blanco/gris/negro como neutros.

### Branding

No es evento — no aplica "Branding de Evento". Sí aplica dejar visible la atribución a Deloitte Global / Elizabeth Faber como fuente del contenido (ver arriba), junto con la firma personal habitual (LinkedIn + `cacm523`).
