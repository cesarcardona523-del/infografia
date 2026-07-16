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

Este README se irá actualizando con un enlace por cada infografía nueva.

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
