# Especificación de Diseño — Infografías Técnicas

> Ver INFOGRAFIA-SPEC.md para el detalle completo. Sin fotos/escenas/personas, firma LinkedIn + `cacm523`, 1200×627px.

## Contexto específico — Data Governance for Master Data Management

**Referencias** (3 PDF en `referencias/GobiernoDatos/data-governance-mdm/`, analizados en su contenido real, no asumidos por nombre de archivo):

1. `DataGovernance.pdf` — *"Data Governance for Master Data Management and Beyond"* (David Loshin / SAS, whitepaper). Fuente principal de esta pieza.
2. `GestioDatos.pdf` — *"SAS: Una Plataforma Completa para el Gobierno de Big Data..."* (Sunil Soares). Material de marketing de producto SAS — se usa solo como contexto de fondo (arquitectura de referencia de big data en 3 capas), sin promocionar productos SAS por nombre en la pieza final.
3. `futuro-data-management.pdf` — *"El Futuro del Data Management"* (Fiona McNeil / Ron Agresta). Tendencia: automatización creciente y autoservicio en la gestión de datos.

**Nota de marca**: los 3 PDF son material de SAS/terceros — se extrae únicamente la idea técnica (nunca logos, nombres de producto ni branding de SAS/Information Asset), redibujada con el sistema de diseño propio, como pide INFOGRAFIA-SPEC.md.

**Contenido real usado (del PDF 1, sin inventar cifras)**:

- **Tesis central**: un programa de Master Data Management (MDM) exitoso depende de que la gobernanza de datos esté integrada desde el inicio — sin gobierno, un repositorio maestro centralizado es solo una copia consolidada del caos, no una fuente de verdad confiable.
- **Marco de responsabilidad y rendición de cuentas** (Figura 2 del PDF, jerarquía de 4 niveles, de arriba hacia abajo):
  1. **Director de Gobierno de Datos** — patrocinio: gestión día a día, preside el comité de supervisión, consigue respaldo a nivel ejecutivo (C-level).
  2. **Comité de Supervisión de Gobierno (DGOB)** — comité estratégico que aprueba políticas y prioridades, y delimita la rendición de cuentas.
  3. **Consejo de Coordinación de Datos** — equipo táctico: define métricas y umbrales de aceptación, gestiona el gobierno entre líneas de negocio.
  4. **Data Stewards por línea de negocio** — estructura de gobierno a nivel operativo: define criterios de calidad y reporta issues al consejo de coordinación.
- **Tres pilares para MDM ("Pulling It All Together")**:
  1. **Elementos críticos de datos** — identificar consenso sobre términos de negocio, investigar su fuente autoritativa y acordar definiciones comunes en el repositorio maestro.
  2. **Políticas de información** — traducir políticas de negocio en reglas de datos medibles y reportables.
  3. **Rendición de cuentas** — empoderar a las personas correctas y definir una estructura de gobierno con incentivos reales, no solo políticas en papel.
- **Mirando al futuro** (síntesis del PDF 3, como cierre): la gestión de datos avanza hacia mayor autoservicio y automatización — sistemas que se autoajustan y anticipan necesidades — pero esa automatización solo es confiable sobre una base de gobierno ya establecida.

**Dirección visual**: pirámide organizacional de 4 niveles (Director en la cúspide, Data Stewards en la base — más angosto arriba, más ancho abajo) como elemento principal, con los 3 pilares como tarjetas de apoyo a la derecha. Paleta: azul marino/grafito (seriedad corporativa, distinto de las otras piezas del mismo lote).
