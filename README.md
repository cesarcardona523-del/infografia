<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0B1426,100:00C9A7&height=180&section=header&text=Infograf%C3%ADas&fontSize=42&fontColor=fff&fontAlignY=38&desc=Arquitectura%20BI%20%7C%20An%C3%A1lisis%20de%20Datos&descAlignY=58&descColor=d0f0e8"/>

</div>

<p align="center">
  <a href="https://linkedin.com/in/cacm523">
    <img src="https://img.shields.io/badge/LinkedIn-Conectar-0A66C2?style=flat&logo=linkedin"/>
  </a>
  &nbsp;
  <a href="mailto:cesarcardona523@gmail.com">
    <img src="https://img.shields.io/badge/Email-Escribir-1A56E8?style=flat&logo=gmail&logoColor=white"/>
  </a>
</p>

---

## 👨‍💻 Sobre este proyecto

Este repositorio reúne **infografías técnicas premium** para LinkedIn sobre temas de datos y tecnología — Arquitectura, Python, Power BI, y los que se vayan sumando — organizadas por tema, con un catálogo de metadata incremental listo para publicar.

## 📁 Estructura

```text
infografia/
├── referencias/<Tema>/          → imágenes de referencia que se suministran para ese tema (input)
├── Construidos/<Tema>/          → salida: infografías generadas para ese tema, incremental en el tiempo
│   ├── <topico>.prompt.md
│   ├── <topico>.png              (o <topico>.html si no hay imagen generada)
├── publicaciones.json    → catálogo único e incremental de metadata de todas las infografías
├── INFOGRAFIA-SPEC.md    → spec de diseño visual (fija)
└── INFOGRAFIA-INVESTIGAR.md → spec de análisis/metadata (fija)
```

`<Tema>` es una categoría amplia (ej. `Arquitectura`, `Python`, `Power BI`) — dentro de una misma carpeta de tema conviven, en el tiempo, varias infografías de distintos tópicos. Toda infografía ya construida vive dentro de `Construidos/<Tema>/`, nunca directamente en la raíz del repositorio.

## 🛠️ Stack Técnico

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

Sin framework, sin bundler, sin paso de build. Cada infografía se construye en HTML/CSS puro (contenedor fijo 1200×627px) y se exporta automáticamente a PNG en alta resolución — sin depender de una herramienta externa de generación de imágenes.

## 🎨 Diseño

Todas las infografías siguen el mismo sistema de diseño, definido en [INFOGRAFIA-SPEC.md](INFOGRAFIA-SPEC.md): infografía técnica editorial (nunca fotografía ni escena real), paleta fija, tipografía, marca de agua y firma, tamaño 1200×627px optimizado para LinkedIn.

Para crear una infografía nueva: se listan imágenes de referencia en `referencias/<Tema>/`, y ese contexto se combina con el spec de diseño en `Construidos/<Tema>/<topico>.prompt.md` — ver [CLAUDE.md](CLAUDE.md) para el flujo completo.

El proyecto mantiene un rol permanente de mejora continua: cada vez que se trabaja un tema, las piezas ya construidas de ese tema se revisan y, si hay una mejora objetiva real, se regeneran conservando el mismo nombre de archivo — sin tocar las que ya son consistentes con el estándar actual. INFOGRAFIA-SPEC.md evoluciona como design system vivo bajo el mismo criterio (ver "Rol permanente y mejora continua" en [CLAUDE.md](CLAUDE.md)).

## 📄 Catálogo de publicaciones

Cada infografía agrega una entrada a [publicaciones.json](publicaciones.json), generada con el prompt de análisis de [INFOGRAFIA-INVESTIGAR.md](INFOGRAFIA-INVESTIGAR.md): categoría principal, temas, tipo de contenido, tópico y descripción en español e inglés, listos para programar la publicación. Las fechas se espacian +2 días entre entradas sucesivas, sin más de dos publicaciones el mismo día.

Desde el 2026-07-20, la clasificación usa una taxonomía cerrada de 10 categorías principales, ~45 temas reutilizables y 13 tipos de contenido — ver [`taxonomia.json`](taxonomia.json) y "Gobernanza de la taxonomía" en [CLAUDE.md](CLAUDE.md). Reemplaza el antiguo campo `tema` de texto libre.

Como último paso, el PNG final y esa misma entrada se publican también en el sitio real: `paginaweb/publications/` (imagen) y `paginaweb/publications/publicaciones.js` (catálogo consumido por el sitio).

Antes de crear una entrada nueva, el proyecto analiza si el contenido amplía o corrige una publicación ya existente (mismo tópico exacto); si es así, esa entrada se actualiza en el mismo lugar en vez de duplicarse, y la versión anterior de los archivos se conserva archivada en `Archivadas/` — ver "Gestión inteligente de publicaciones e infografías" en [CLAUDE.md](CLAUDE.md).

## 🗺️ Estado

- ✅ Automatización vs Autonomía: Arquitectura de Sistemas de IA Agénticos — tema `Automatización` — [HTML](Construidos/Automatización/automatizacion-agentesia.html) · [PNG](Construidos/Automatización/automatizacion-agentesia.png)
- ✅ Automatización de Reportes con Python: de Excel a Producción — tema `Automatización` — [HTML](Construidos/Automatización/automatizacion-python.html) · [PNG](Construidos/Automatización/automatizacion-python.png)
- ✅ Orquestación de Scripts en Python: Ejecución Programada a Nivel de Sistema Operativo — tema `Automatización` — [HTML](Construidos/Automatización/automatizacion-python-programada.html) · [PNG](Construidos/Automatización/automatizacion-python-programada.png)
- ✅ Arquitectura de Pipelines de Big Data en AWS — tema `Arquitectura` — [HTML](Construidos/Arquitectura/arquitectura-aws.html) · [PNG](Construidos/Arquitectura/arquitectura-aws.png)
- ✅ Arquitectura de Datos en Azure: Patrón Medallón de Extremo a Extremo — tema `Arquitectura` — [HTML](Construidos/Arquitectura/arquitectura-azure.html) · [PNG](Construidos/Arquitectura/arquitectura-azure.png)
- ✅ Stack de Datos Serverless en Google Cloud Platform — tema `Arquitectura` — [HTML](Construidos/Arquitectura/arquitectura-google.html) · [PNG](Construidos/Arquitectura/arquitectura-google.png)
- ✅ Arquitectura Lakehouse en Oracle Cloud Infrastructure (OCI) — tema `Arquitectura` — [HTML](Construidos/Arquitectura/arquitectura-oracle.html) · [PNG](Construidos/Arquitectura/arquitectura-oracle.png)
- ✅ Evolución del Análisis de Datos: de Registrar Datos a Delegar Tareas — tema `IA` — Datafest 2026 / Bancolombia — [HTML](Construidos/IA/analisis-datos-ia.html) · [PNG](Construidos/IA/analisis-datos-ia.png)
- ✅ Finalidades de las IA: el Enfoque Detrás de Cada Modelo — tema `IA` — Datafest 2026 / Bancolombia — [HTML](Construidos/IA/finalidades-de-las-ia.html) · [PNG](Construidos/IA/finalidades-de-las-ia.png)
- ✅ La Evolución de los Agentes de IA: de Workflows Rígidos a Arquitecturas Goal-Based — tema `IA` — Datafest 2026 / AWS — [HTML](Construidos/IA/ia-agentes.html) · [PNG](Construidos/IA/ia-agentes.png)
- ✅ Arquitecturas de Datos: 9 Patrones que Todo Arquitecto Debe Conocer — tema `Arquitectura` — [HTML](Construidos/Arquitectura/arquitectura-datos.html) · [PNG](Construidos/Arquitectura/arquitectura-datos.png)
- ✅ Arquitectura Medallion: Bronze, Silver y Gold sin Atajos — tema `Arquitectura` — [HTML](Construidos/Arquitectura/arquitectura-medallon.html) · [PNG](Construidos/Arquitectura/arquitectura-medallon.png)
- ✅ Bases de Datos Populares: un Mapa por Familias para Elegir con Criterio — tema `Base de Datos` — [HTML](Construidos/Base_de_Datos/bases-de-datos-populares.html) · [PNG](Construidos/Base_de_Datos/bases-de-datos-populares.png)
- ✅ BI vs BA: del Espejo Retrovisor a la Brújula del Negocio — tema `BI` — [HTML](Construidos/BI/bi-vs-ba.html) · [PNG](Construidos/BI/bi-vs-ba.png)
- ✅ BI de Autoservicio: Analítica sin Depender de TI en Cada Pregunta — tema `BI` — [HTML](Construidos/BI/bi-autoservicio.html) · [PNG](Construidos/BI/bi-autoservicio.png)
- ✅ 5 Razones para Implementar Big Data y Analytics — tema `Bigdata` — [HTML](Construidos/Bigdata/razones-implementar-bigdata.html) · [PNG](Construidos/Bigdata/razones-implementar-bigdata.png)
- ✅ Big Data = Big Innovation: Cómo los Datos Transforman Sectores Enteros — tema `Bigdata` — [HTML](Construidos/Bigdata/bigdata-big-innovation.html) · [PNG](Construidos/Bigdata/bigdata-big-innovation.png)
- ✅ CONPES 3920: la Política Nacional de Big Data en Colombia — tema `Bigdata` — [HTML](Construidos/Bigdata/conpes-3920-bigdata.html) · [PNG](Construidos/Bigdata/conpes-3920-bigdata.png)
- ✅ Big Data en las Grandes Empresas: de la Pila Técnica al Valor de Negocio — tema `Bigdata` — [HTML](Construidos/Bigdata/bigdata-grandes-empresas.html) · [PNG](Construidos/Bigdata/bigdata-grandes-empresas.png)
- ✅ Cómo Escribir Prompts Efectivos para ChatGPT — tema `ChatGPT` — [HTML](Construidos/ChatGPT/prompts-efectivos-chatgpt.html) · [PNG](Construidos/ChatGPT/prompts-efectivos-chatgpt.png)
- ✅ Claude Llega a Excel y lo Cambia Todo — tema `Claude` — [HTML](Construidos/Claude/claude-excel.html) · [PNG](Construidos/Claude/claude-excel.png)
- ✅ El Ciclo de Vida de un Proyecto de Ciencia de Datos — tema `Cultura_Datos` — [HTML](Construidos/Cultura_Datos/ciclo-vida-ciencia-datos.html) · [PNG](Construidos/Cultura_Datos/ciclo-vida-ciencia-datos.png)
- ✅ Estadística Práctica para Científicos de Datos — tema `Cultura_Datos` — [HTML](Construidos/Cultura_Datos/estadisticas-ciencia-datos.html) · [PNG](Construidos/Cultura_Datos/estadisticas-ciencia-datos.png)
- ✅ De Datos a Decisiones: la Escalera del Valor Analítico — tema `Cultura_Datos` — [HTML](Construidos/Cultura_Datos/escalera-valor-analitico.html) · [PNG](Construidos/Cultura_Datos/escalera-valor-analitico.png)
- ✅ La Pregunta Define el Análisis — tema `Cultura_Datos` — [HTML](Construidos/Cultura_Datos/preguntas-analisis.html) · [PNG](Construidos/Cultura_Datos/preguntas-analisis.png)
- ✅ Leer Datos vs. Analizar Información — tema `Cultura_Datos` — [HTML](Construidos/Cultura_Datos/leer-datos-vs-analizar-informacion.html) · [PNG](Construidos/Cultura_Datos/leer-datos-vs-analizar-informacion.png)
- ✅ Tipos de Normalización en Ciencia de Datos — tema `Cultura_Datos` — [HTML](Construidos/Cultura_Datos/normalizacion-ciencia-datos.html) · [PNG](Construidos/Cultura_Datos/normalizacion-ciencia-datos.png)
- ✅ Beneficios de una Cultura de Datos — tema `Cultura_Datos` — [HTML](Construidos/Cultura_Datos/beneficios-cultura-dato.html) · [PNG](Construidos/Cultura_Datos/beneficios-cultura-dato.png)
- ✅ Cómo Construir una Cultura de Datos — tema `Cultura_Datos` — [HTML](Construidos/Cultura_Datos/construir-cultura-dato.html) · [PNG](Construidos/Cultura_Datos/construir-cultura-dato.png)
- ✅ Modernizando la Integración de Datos — tema `Cultura_Datos` — [HTML](Construidos/Cultura_Datos/modernizacion-integracion-datos.html) · [PNG](Construidos/Cultura_Datos/modernizacion-integracion-datos.png)
- ✅ La Regla del Z en Dashboards — tema `Dashboard` — [HTML](Construidos/Dashboard/reglas-diseno-dashboard.html) · [PNG](Construidos/Dashboard/reglas-diseno-dashboard.png)
- ✅ Tipos de Dashboards — tema `Dashboard` — [HTML](Construidos/Dashboard/tipos-dashboard.html) · [PNG](Construidos/Dashboard/tipos-dashboard.png)
- ✅ Top 6 Conceptos de Datos — tema `Cultura_Datos` — [HTML](Construidos/Cultura_Datos/conceptos-datos.html) · [PNG](Construidos/Cultura_Datos/conceptos-datos.png)
- ✅ 10 Términos Esenciales de Ciencia de Datos y Machine Learning — tema `Cultura_Datos` — [HTML](Construidos/Cultura_Datos/terminos-ciencia-datos.html) · [PNG](Construidos/Cultura_Datos/terminos-ciencia-datos.png)
- ✅ Databricks: Datos en Conocimiento 12x Más Rápido — tema `Arquitectura` — [HTML](Construidos/Arquitectura/databricks.html) · [PNG](Construidos/Arquitectura/databricks.png)
- ✅ ¿Docente o Líder de Aprendizaje? Los 3 Cambios que Redefinen la Enseñanza — tema `Docencia` — [HTML](Construidos/Docencia/docente-lider-aprendizaje.html) · [PNG](Construidos/Docencia/docente-lider-aprendizaje.png)
- ✅ ¿Cómo Liderar a Cada Generación? 8 Claves para Boomers, Gen X, Millennials y Gen Z — tema `Liderazgo` — [HTML](Construidos/Liderazgo/liderar-cada-generacion.html) · [PNG](Construidos/Liderazgo/liderar-cada-generacion.png)
- ✅ 8 Conceptos Estadísticos Esenciales para Ciencia de Datos — tema `Cultura_Datos` — [HTML](Construidos/Cultura_Datos/conceptos-estadisticos-basicos.html) · [PNG](Construidos/Cultura_Datos/conceptos-estadisticos-basicos.png)
- ✅ Hoja de Ruta de Estadística para Analistas de Datos — tema `Cultura_Datos` — [HTML](Construidos/Cultura_Datos/hoja-de-ruta-estadistica.html) · [PNG](Construidos/Cultura_Datos/hoja-de-ruta-estadistica.png)
- ✅ ¿Para Qué Sirve la Correlación? Guía Práctica del Coeficiente R — tema `Cultura_Datos` — [HTML](Construidos/Cultura_Datos/correlacion-estadistica.html) · [PNG](Construidos/Cultura_Datos/correlacion-estadistica.png)
- ✅ 4 Gráficos de Excel que Todo Analista de Costos Debería Usar — tema `Excel` — [HTML](Construidos/Excel/graficos-excel.html) · [PNG](Construidos/Excel/graficos-excel.png)
- ✅ XLSX vs. TXT/CSV vs. Parquet: Qué Formato Usar para Análisis Masivo — tema `Excel` — [HTML](Construidos/Excel/tipos-archivos-excel.html) · [PNG](Construidos/Excel/tipos-archivos-excel.png)
- ✅ Automatiza tus Excel con Macros VBA: Guía Práctica — tema `Excel` — [HTML](Construidos/Excel/automatizar-macros-excel.html) · [PNG](Construidos/Excel/automatizar-macros-excel.png)
- ✅ Tablas Dinámicas en Excel: Qué Son y Cuándo Usarlas — tema `Excel` — [HTML](Construidos/Excel/tablas-dinamicas-excel.html) · [PNG](Construidos/Excel/tablas-dinamicas-excel.png)
- ✅ El Mapa de Vocabulario Esencial de IA — tema `IA` — [HTML](Construidos/IA/terminos-ia.html) · [PNG](Construidos/IA/terminos-ia.png)
- ✅ 30 Skills de Claude para Pequeñas Empresas — tema `Claude` — [HTML](Construidos/Claude/skill-claude.html) · [PNG](Construidos/Claude/skill-claude.png)
- ✅ Hay una Diferencia Abismal entre Saber Usar y Dominar Power BI — tema `PowerBI` — [HTML](Construidos/PowerBI/usar-dominar-power-bi.html) · [PNG](Construidos/PowerBI/usar-dominar-power-bi.png)
- ✅ 15 Prompts Esenciales para Implementar un SGC ISO 9001 — tema `Cultura_Datos` — [HTML](Construidos/Cultura_Datos/prompts-iso-9001.html) · [PNG](Construidos/Cultura_Datos/prompts-iso-9001.png)
- ✅ Conecta Power BI con Python: Pronóstico de Datos — tema `PowerBI` — [HTML](Construidos/PowerBI/integracion-python-power-bi.html) · [PNG](Construidos/PowerBI/integracion-python-power-bi.png)
- ✅ La Pelea Diaria de un Analista de Datos con los KPIs — tema `Roles` — [HTML](Construidos/Roles/kpi-analista-datos.html) · [PNG](Construidos/Roles/kpi-analista-datos.png)
- ✅ Arquitectura Medallion: Datos Confiables en Cada Capa — tema `Arquitectura` — [HTML](Construidos/Arquitectura/arquitectura-medallon-datos-confiables.html) · [PNG](Construidos/Arquitectura/arquitectura-medallon-datos-confiables.png)
- ✅ Relación de Dependencia e Integración: Python, Estadística, ML e IA — tema `Cultura_Datos` — [HTML](Construidos/Cultura_Datos/integracion-python-estadistica-ml-ia.html) · [PNG](Construidos/Cultura_Datos/integracion-python-estadistica-ml-ia.png)
- ✅ Stack de Claude 2026 para Líderes Empresariales — tema `Claude` — [HTML](Construidos/Claude/stack-claude.html) · [PNG](Construidos/Claude/stack-claude.png)
- ✅ La Realidad de la Transformación con IA — tema `IA` — [HTML](Construidos/IA/transformacion-ia.html) · [PNG](Construidos/IA/transformacion-ia.png)
- ✅ Evolución de las Herramientas que Debe Dominar un Analista de Datos — tema `Roles` — [HTML](Construidos/Roles/evolucion-herramientas-analistas-datos.html) · [PNG](Construidos/Roles/evolucion-herramientas-analistas-datos.png)
- ✅ Comandos y Tipos de Datos en SQL Server — tema `SQL` — [HTML](Construidos/SQL/comandos-tipos-datos-sql.html) · [PNG](Construidos/SQL/comandos-tipos-datos-sql.png)
- ✅ Modelo de Excelencia Operacional en Hospitales Privados — tema `Modelos` — [HTML](Construidos/Modelos/modelos-salud-hospitales-privados.html) · [PNG](Construidos/Modelos/modelos-salud-hospitales-privados.png)
- ✅ Árbol de Modelos de Claude: Cómo Elegir el Correcto — tema `Claude` — [HTML](Construidos/Claude/arbol-modelos-claude.html) · [PNG](Construidos/Claude/arbol-modelos-claude.png)
- ✅ Análisis de Datos: Convertir Información en Mejores Decisiones — tema `Cultura_Datos` — [HTML](Construidos/Cultura_Datos/analisis-datos.html) · [PNG](Construidos/Cultura_Datos/analisis-datos.png)
- ✅ ¿Quién Hace Qué en Datos? Ingeniería, Análisis, Ciencia y BI — tema `Roles` — [HTML](Construidos/Roles/quien-hace-que-en-datos.html) · [PNG](Construidos/Roles/quien-hace-que-en-datos.png)
- ✅ 9 Tipos de Gestión de Proyectos: Marcos Predictivos, Ágiles y Técnicas de Optimización — tema `Proyectos` — [HTML](Construidos/Proyectos/tipos-gestion-proyectos.html) · [PNG](Construidos/Proyectos/tipos-gestion-proyectos.png)
- ✅ El Gobierno de Datos no es Solo Tecnología: Reglas, Responsables y Confianza — tema `Gobierno_de_Datos` — [HTML](Construidos/Gobierno_de_Datos/gobierno-de-datos.html) · [PNG](Construidos/Gobierno_de_Datos/gobierno-de-datos.png)
- ✅ Estrategia de Datos: el Equilibrio entre Capacidades Ofensivas y Defensivas — tema `Estrategia_de_Datos` — [HTML](Construidos/Estrategia_de_Datos/estrategia-de-datos.html) · [PNG](Construidos/Estrategia_de_Datos/estrategia-de-datos.png)
- ✅ Gobernanza de Datos en Tableros de BI: Confianza en los Datos, Decisiones con Impacto — tema `Gobernanza_Tableros_BI` — [HTML](Construidos/Gobernanza_Tableros_BI/gobernanza-tableros-bi.html) · [PNG](Construidos/Gobernanza_Tableros_BI/gobernanza-tableros-bi.png)
- ✅ Calidad de Datos en Gobierno de Datos: 6 Dimensiones con Caso Aplicado en Banca — tema `Calidad_Datos_Gobierno` — [HTML](Construidos/Calidad_Datos_Gobierno/calidad-datos-gobierno.html) · [PNG](Construidos/Calidad_Datos_Gobierno/calidad-datos-gobierno.png)
- ✅ Data Governance for Master Data Management: Roles, Políticas y Rendición de Cuentas — tema `Data_Governance_MDM` — [HTML](Construidos/Data_Governance_MDM/data-governance-mdm.html) · [PNG](Construidos/Data_Governance_MDM/data-governance-mdm.png)
- ✅ Métricas para Evaluar Modelos de IA: Regresión vs. Clasificación — tema `Metricas_Modelos_IA` — [HTML](Construidos/Metricas_Modelos_IA/metricas-modelos-ia.html) · [PNG](Construidos/Metricas_Modelos_IA/metricas-modelos-ia.png)
- ✅ Comparación de Herramientas de IA para Desarrollo: Codex, Claude Code y OpenCode — tema `Comparacion_Herramientas_IA_Desarrollo` — [HTML](Construidos/Comparacion_Herramientas_IA_Desarrollo/herramientas-desarrollo-ia.html) · [PNG](Construidos/Comparacion_Herramientas_IA_Desarrollo/herramientas-desarrollo-ia.png)
- ✅ Los 3 Niveles de Adopción de IA: Refactorizar, Reinventar, Reimaginar — tema `Adopcion_IA` — [HTML](Construidos/Adopcion_IA/adopcion-ia.html) · [PNG](Construidos/Adopcion_IA/adopcion-ia.png)
- ✅ De Turing a GPT: la Historia de la IA en 6 Hitos — tema `Escuela_IA` (evento: Escuela de Inteligencia Artificial · Uniremington) — [HTML](Construidos/Escuela_IA/historia-ia-de-turing-a-gpt.html) · [PNG](Construidos/Escuela_IA/historia-ia-de-turing-a-gpt.png)
- ✅ Cómo Funciona un LLM — tema `Escuela_IA` (evento: Escuela de Inteligencia Artificial · Uniremington) — [HTML](Construidos/Escuela_IA/como-funciona-un-llm.html) · [PNG](Construidos/Escuela_IA/como-funciona-un-llm.png)
- ✅ Capacidades y Límites de los LLM — tema `Escuela_IA` (evento: Escuela de Inteligencia Artificial · Uniremington) — [HTML](Construidos/Escuela_IA/capacidades-y-limites-llm.html) · [PNG](Construidos/Escuela_IA/capacidades-y-limites-llm.png)
- ✅ El Ciclo del Hype de la IA — tema `Escuela_IA` (evento: Escuela de Inteligencia Artificial · Uniremington) — [HTML](Construidos/Escuela_IA/ciclo-del-hype-ia.html) · [PNG](Construidos/Escuela_IA/ciclo-del-hype-ia.png)
- ✅ Chain of Thought — tema `Escuela_IA` (evento: Escuela de Inteligencia Artificial · Uniremington) — [HTML](Construidos/Escuela_IA/chain-of-thought-prompting.html) · [PNG](Construidos/Escuela_IA/chain-of-thought-prompting.png)
- ✅ Cuando la IA Alucina: 3 Casos Reales — tema `Escuela_IA` (evento: Escuela de Inteligencia Artificial · Uniremington) — [HTML](Construidos/Escuela_IA/cuando-la-ia-alucina.html) · [PNG](Construidos/Escuela_IA/cuando-la-ia-alucina.png)
- ✅ SQL Joins: Cómo Elegir Entre INNER, LEFT, RIGHT y FULL OUTER JOIN — tema `SQL` — [HTML](Construidos/SQL/sql-joins.html) · [PNG](Construidos/SQL/sql-joins.png)

Este README se irá actualizando con un enlace por cada infografía nueva.

---

## 📈 Estadísticas del Repositorio

Cifras reales de este repositorio (calculadas con `git log`/`git shortlog` sobre este mismo git — sin servicios externos ni redirecciones a otros sitios, instantánea al 2026-07-21):

<p align="center">
  <img src="https://img.shields.io/badge/Commits-34-00C9A7?style=for-the-badge&logo=git&logoColor=white"/>
  &nbsp;
  <img src="https://img.shields.io/badge/Archivos-383-1A56E8?style=for-the-badge&logo=files&logoColor=white"/>
  &nbsp;
  <img src="https://img.shields.io/badge/Líneas%20%2B%2F%E2%88%92-62%2C536%20%2F%201%2C044-0B1426?style=for-the-badge&logo=git&logoColor=white"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Primer%20commit-2026--07--16-00C9A7?style=flat&logo=git&logoColor=white"/>
  &nbsp;
  <img src="https://img.shields.io/badge/Último%20commit-2026--07--21-1A56E8?style=flat&logo=git&logoColor=white"/>
</p>

**Commits por autor:**

<p align="center">
  <img src="https://img.shields.io/badge/caesar523__dev-34%20commits-00C9A7?style=flat&logo=github&logoColor=white"/>
</p>

> Esta sección se debe recalcular y actualizar cada vez que se agregue o modifique contenido en este repositorio — ver la regla correspondiente en [CLAUDE.md](CLAUDE.md).

---

## 📬 Contacto

<p align="center">
  <a href="https://linkedin.com/in/cacm523">
    <img src="https://img.shields.io/badge/LinkedIn-C%C3%A9sar%20Cardona-0A66C2?style=for-the-badge&logo=linkedin"/>
  </a>
  &nbsp;
  <a href="mailto:cesarcardona523@gmail.com">
    <img src="https://img.shields.io/badge/Email-cesarcardona523%40gmail.com-1A56E8?style=for-the-badge&logo=gmail&logoColor=white"/>
  </a>
</p>

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:00C9A7,100:0B1426&height=100&section=footer"/>
</div>
