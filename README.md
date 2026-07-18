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
├── referencias/<Tema>/   → imágenes de referencia que se suministran para ese tema (input)
├── <Tema>/               → salida: infografías generadas para ese tema, incremental en el tiempo
│   ├── <topico>.prompt.md
│   ├── <topico>.png       (o <topico>.html si no hay imagen generada)
├── publicaciones.json    → catálogo único e incremental de metadata de todas las infografías
├── INFOGRAFIA-SPEC.md    → spec de diseño visual (fija)
└── INFOGRAFIA-INVESTIGAR.md → spec de análisis/metadata (fija)
```

`<Tema>` es una categoría amplia (ej. `Arquitectura`, `Python`, `Power BI`) — dentro de una misma carpeta de tema conviven, en el tiempo, varias infografías de distintos tópicos.

## 🛠️ Stack Técnico

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

Sin framework, sin bundler, sin paso de build. Cada infografía se construye en HTML/CSS puro (contenedor fijo 1200×627px) y se exporta automáticamente a PNG en alta resolución — sin depender de una herramienta externa de generación de imágenes.

## 🎨 Diseño

Todas las infografías siguen el mismo sistema de diseño, definido en [INFOGRAFIA-SPEC.md](INFOGRAFIA-SPEC.md): infografía técnica editorial (nunca fotografía ni escena real), paleta fija, tipografía, marca de agua y firma, tamaño 1200×627px optimizado para LinkedIn.

Para crear una infografía nueva: se listan imágenes de referencia en `referencias/<Tema>/`, y ese contexto se combina con el spec de diseño en `/<Tema>/<topico>.prompt.md` — ver [CLAUDE.md](CLAUDE.md) para el flujo completo.

## 📄 Catálogo de publicaciones

Cada infografía agrega una entrada a [publicaciones.json](publicaciones.json), generada con el prompt de análisis de [INFOGRAFIA-INVESTIGAR.md](INFOGRAFIA-INVESTIGAR.md): tema, tópico y descripción en español e inglés, listos para programar la publicación. Las fechas se espacian +2 días entre entradas sucesivas, sin más de dos publicaciones el mismo día.

Como último paso, el PNG final y esa misma entrada se publican también en el sitio real: `paginaweb/publications/` (imagen) y `paginaweb/publications/publicaciones.js` (catálogo consumido por el sitio, misma regla de incremental — nunca se sobreescribe).

## 🗺️ Estado

- ✅ Automatización vs Autonomía: Arquitectura de Sistemas de IA Agénticos — tema `Automatización` — [HTML](Automatización/automatizacion-agentesia.html) · [PNG](Automatización/automatizacion-agentesia.png)
- ✅ Automatización de Reportes con Python: de Excel a Producción — tema `Automatización` — [HTML](Automatización/automatizacion-python.html) · [PNG](Automatización/automatizacion-python.png)
- ✅ Orquestación de Scripts en Python: Ejecución Programada a Nivel de Sistema Operativo — tema `Automatización` — [HTML](Automatización/automatizacion-python-programada.html) · [PNG](Automatización/automatizacion-python-programada.png)
- ✅ Arquitectura de Pipelines de Big Data en AWS — tema `Arquitectura` — [HTML](Arquitectura/arquitectura-aws.html) · [PNG](Arquitectura/arquitectura-aws.png)
- ✅ Arquitectura de Datos en Azure: Patrón Medallón de Extremo a Extremo — tema `Arquitectura` — [HTML](Arquitectura/arquitectura-azure.html) · [PNG](Arquitectura/arquitectura-azure.png)
- ✅ Stack de Datos Serverless en Google Cloud Platform — tema `Arquitectura` — [HTML](Arquitectura/arquitectura-google.html) · [PNG](Arquitectura/arquitectura-google.png)
- ✅ Arquitectura Lakehouse en Oracle Cloud Infrastructure (OCI) — tema `Arquitectura` — [HTML](Arquitectura/arquitectura-oracle.html) · [PNG](Arquitectura/arquitectura-oracle.png)
- ✅ Evolución del Análisis de Datos: de Registrar Datos a Delegar Tareas — tema `IA` — Datafest 2026 / Bancolombia — [HTML](IA/analisis-datos-ia.html) · [PNG](IA/analisis-datos-ia.png)
- ✅ Finalidades de las IA: el Enfoque Detrás de Cada Modelo — tema `IA` — Datafest 2026 / Bancolombia — [HTML](IA/finalidades-de-las-ia.html) · [PNG](IA/finalidades-de-las-ia.png)
- ✅ La Evolución de los Agentes de IA: de Workflows Rígidos a Arquitecturas Goal-Based — tema `IA` — Datafest 2026 / AWS — [HTML](IA/ia-agentes.html) · [PNG](IA/ia-agentes.png)
- ✅ Arquitecturas de Datos: 9 Patrones que Todo Arquitecto Debe Conocer — tema `Arquitectura` — [HTML](Arquitectura/arquitectura-datos.html) · [PNG](Arquitectura/arquitectura-datos.png)
- ✅ Arquitectura Medallion: Bronze, Silver y Gold sin Atajos — tema `Arquitectura` — [HTML](Arquitectura/arquitectura-medallon.html) · [PNG](Arquitectura/arquitectura-medallon.png)
- ✅ Bases de Datos Populares: un Mapa por Familias para Elegir con Criterio — tema `Base de Datos` — [HTML](Base_de_Datos/bases-de-datos-populares.html) · [PNG](Base_de_Datos/bases-de-datos-populares.png)
- ✅ BI vs BA: del Espejo Retrovisor a la Brújula del Negocio — tema `BI` — [HTML](BI/bi-vs-ba.html) · [PNG](BI/bi-vs-ba.png)
- ✅ BI de Autoservicio: Analítica sin Depender de TI en Cada Pregunta — tema `BI` — [HTML](BI/bi-autoservicio.html) · [PNG](BI/bi-autoservicio.png)
- ✅ 5 Razones para Implementar Big Data y Analytics — tema `Bigdata` — [HTML](Bigdata/razones-implementar-bigdata.html) · [PNG](Bigdata/razones-implementar-bigdata.png)
- ✅ Big Data = Big Innovation: Cómo los Datos Transforman Sectores Enteros — tema `Bigdata` — [HTML](Bigdata/bigdata-big-innovation.html) · [PNG](Bigdata/bigdata-big-innovation.png)
- ✅ CONPES 3920: la Política Nacional de Big Data en Colombia — tema `Bigdata` — [HTML](Bigdata/conpes-3920-bigdata.html) · [PNG](Bigdata/conpes-3920-bigdata.png)
- ✅ Big Data en las Grandes Empresas: de la Pila Técnica al Valor de Negocio — tema `Bigdata` — [HTML](Bigdata/bigdata-grandes-empresas.html) · [PNG](Bigdata/bigdata-grandes-empresas.png)
- ✅ Cómo Escribir Prompts Efectivos para ChatGPT — tema `ChatGPT` — [HTML](ChatGPT/prompts-efectivos-chatgpt.html) · [PNG](ChatGPT/prompts-efectivos-chatgpt.png)
- ✅ Claude Llega a Excel y lo Cambia Todo — tema `Claude` — [HTML](Claude/claude-excel.html) · [PNG](Claude/claude-excel.png)
- ✅ El Ciclo de Vida de un Proyecto de Ciencia de Datos — tema `Cultura_Datos` — [HTML](Cultura_Datos/ciclo-vida-ciencia-datos.html) · [PNG](Cultura_Datos/ciclo-vida-ciencia-datos.png)
- ✅ Estadística Práctica para Científicos de Datos — tema `Cultura_Datos` — [HTML](Cultura_Datos/estadisticas-ciencia-datos.html) · [PNG](Cultura_Datos/estadisticas-ciencia-datos.png)
- ✅ De Datos a Decisiones: la Escalera del Valor Analítico — tema `Cultura_Datos` — [HTML](Cultura_Datos/escalera-valor-analitico.html) · [PNG](Cultura_Datos/escalera-valor-analitico.png)
- ✅ La Pregunta Define el Análisis — tema `Cultura_Datos` — [HTML](Cultura_Datos/preguntas-analisis.html) · [PNG](Cultura_Datos/preguntas-analisis.png)
- ✅ Leer Datos vs. Analizar Información — tema `Cultura_Datos` — [HTML](Cultura_Datos/leer-datos-vs-analizar-informacion.html) · [PNG](Cultura_Datos/leer-datos-vs-analizar-informacion.png)
- ✅ Tipos de Normalización en Ciencia de Datos — tema `Cultura_Datos` — [HTML](Cultura_Datos/normalizacion-ciencia-datos.html) · [PNG](Cultura_Datos/normalizacion-ciencia-datos.png)
- ✅ Beneficios de una Cultura de Datos — tema `Cultura_Datos` — [HTML](Cultura_Datos/beneficios-cultura-dato.html) · [PNG](Cultura_Datos/beneficios-cultura-dato.png)
- ✅ Cómo Construir una Cultura de Datos — tema `Cultura_Datos` — [HTML](Cultura_Datos/construir-cultura-dato.html) · [PNG](Cultura_Datos/construir-cultura-dato.png)
- ✅ Modernizando la Integración de Datos — tema `Cultura_Datos` — [HTML](Cultura_Datos/modernizacion-integracion-datos.html) · [PNG](Cultura_Datos/modernizacion-integracion-datos.png)
- ✅ La Regla del Z en Dashboards — tema `Dashboard` — [HTML](Dashboard/reglas-diseno-dashboard.html) · [PNG](Dashboard/reglas-diseno-dashboard.png)
- ✅ Tipos de Dashboards — tema `Dashboard` — [HTML](Dashboard/tipos-dashboard.html) · [PNG](Dashboard/tipos-dashboard.png)
- ✅ Top 6 Conceptos de Datos — tema `Cultura_Datos` — [HTML](Cultura_Datos/conceptos-datos.html) · [PNG](Cultura_Datos/conceptos-datos.png)
- ✅ 10 Términos Esenciales de Ciencia de Datos y Machine Learning — tema `Cultura_Datos` — [HTML](Cultura_Datos/terminos-ciencia-datos.html) · [PNG](Cultura_Datos/terminos-ciencia-datos.png)
- ✅ Databricks: Datos en Conocimiento 12x Más Rápido — tema `Arquitectura` — [HTML](Arquitectura/databricks.html) · [PNG](Arquitectura/databricks.png)
- ✅ ¿Docente o Líder de Aprendizaje? Los 3 Cambios que Redefinen la Enseñanza — tema `Docencia` — [HTML](Docencia/docente-lider-aprendizaje.html) · [PNG](Docencia/docente-lider-aprendizaje.png)
- ✅ ¿Cómo Liderar a Cada Generación? 8 Claves para Boomers, Gen X, Millennials y Gen Z — tema `Liderazgo` — [HTML](Liderazgo/liderar-cada-generacion.html) · [PNG](Liderazgo/liderar-cada-generacion.png)
- ✅ 8 Conceptos Estadísticos Esenciales para Ciencia de Datos — tema `Cultura_Datos` — [HTML](Cultura_Datos/conceptos-estadisticos-basicos.html) · [PNG](Cultura_Datos/conceptos-estadisticos-basicos.png)
- ✅ Hoja de Ruta de Estadística para Analistas de Datos — tema `Cultura_Datos` — [HTML](Cultura_Datos/hoja-de-ruta-estadistica.html) · [PNG](Cultura_Datos/hoja-de-ruta-estadistica.png)
- ✅ ¿Para Qué Sirve la Correlación? Guía Práctica del Coeficiente R — tema `Cultura_Datos` — [HTML](Cultura_Datos/correlacion-estadistica.html) · [PNG](Cultura_Datos/correlacion-estadistica.png)
- ✅ 4 Gráficos de Excel que Todo Analista de Costos Debería Usar — tema `Excel` — [HTML](Excel/graficos-excel.html) · [PNG](Excel/graficos-excel.png)
- ✅ XLSX vs. TXT/CSV vs. Parquet: Qué Formato Usar para Análisis Masivo — tema `Excel` — [HTML](Excel/tipos-archivos-excel.html) · [PNG](Excel/tipos-archivos-excel.png)
- ✅ Automatiza tus Excel con Macros VBA: Guía Práctica — tema `Excel` — [HTML](Excel/automatizar-macros-excel.html) · [PNG](Excel/automatizar-macros-excel.png)
- ✅ Tablas Dinámicas en Excel: Qué Son y Cuándo Usarlas — tema `Excel` — [HTML](Excel/tablas-dinamicas-excel.html) · [PNG](Excel/tablas-dinamicas-excel.png)

Este README se irá actualizando con un enlace por cada infografía nueva.

---

## 📈 Estadísticas del Repositorio

Cifras reales de este repositorio (calculadas con `git log`/`git shortlog` sobre este mismo git — sin servicios externos ni redirecciones a otros sitios, instantánea al 2026-07-16):

<p align="center">
  <img src="https://img.shields.io/badge/Commits-6-00C9A7?style=for-the-badge&logo=git&logoColor=white"/>
  &nbsp;
  <img src="https://img.shields.io/badge/Archivos-65-1A56E8?style=for-the-badge&logo=files&logoColor=white"/>
  &nbsp;
  <img src="https://img.shields.io/badge/Líneas%20%2B%2F%E2%88%92-5%2C590%20%2F%20571-0B1426?style=for-the-badge&logo=git&logoColor=white"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Primer%20commit-2026--07--16-00C9A7?style=flat&logo=git&logoColor=white"/>
  &nbsp;
  <img src="https://img.shields.io/badge/Último%20commit-2026--07--16-1A56E8?style=flat&logo=git&logoColor=white"/>
</p>

**Commits por autor:**

<p align="center">
  <img src="https://img.shields.io/badge/caesar523__dev-6%20commits-00C9A7?style=flat&logo=github&logoColor=white"/>
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
