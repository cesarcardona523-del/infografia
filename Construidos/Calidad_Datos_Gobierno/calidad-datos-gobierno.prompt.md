# Especificación de Diseño — Infografías Técnicas

> Ver INFOGRAFIA-SPEC.md para el detalle completo. Sin fotos/escenas/personas, firma LinkedIn + `cacm523`, 1200×627px.

## Contexto específico — Calidad de Datos en Gobierno de Datos

**Referencia**: `referencias/GobiernoDatos/calidad-datos-gobierno/CalidadDatos.jpg` — pieza de marca de un tercero ("Data&Analytics"). **Se descarta su logo, URL y hashtags** (branding ajeno) y se conserva únicamente el contenido técnico real, redibujado con el sistema de diseño propio.

**Contenido real (sin inventar cifras)**:

- **Caso aplicado**: Banca y Microfinanzas — Entidad: Caja Rural ABC. Problema: la entidad identificó inconsistencias en su información de clientes, generando riesgos en la evaluación crediticia y el cumplimiento regulatorio. Objetivo: evaluar la calidad de los datos con las 6 dimensiones para tomar decisiones más confiables.
- **Las 6 dimensiones de calidad de datos** (cada una con descripción, caso aplicado y consulta SQL real de la referencia):
  1. **Exactitud** — los datos representan correctamente la realidad. Caso: ingresos mensuales fuera de rangos normales. `SELECT cliente_id, ingreso_mensual FROM clientes WHERE ingreso_mensual > 50000;`
  2. **Completitud** — no faltan los valores requeridos. Caso: clientes sin teléfono o dirección. `SELECT cliente_id, nombre FROM clientes WHERE telefono IS NULL OR direccion IS NULL;`
  3. **Consistencia** — un mismo dato coincide entre sistemas y registros. Caso: diferencias en el estado del cliente entre Core y CRM. `SELECT c.cliente_id, c.estado AS estado_core, crm.estado AS estado_crm FROM clientes_core c JOIN clientes_crm crm ON c.cliente_id = crm.cliente_id WHERE c.estado <> crm.estado;`
  4. **Validez** — los valores cumplen el formato y las reglas de negocio. Caso: fechas de nacimiento inválidas. `SELECT cliente_id, fecha_nacimiento FROM clientes WHERE fecha_nacimiento > CURRENT_DATE;`
  5. **Unicidad** — cada entidad se registra una sola vez, sin duplicados. Caso: duplicidad de clientes por DNI. `SELECT dni, COUNT(*) cantidad FROM clientes GROUP BY dni HAVING COUNT(*) > 1;`
  6. **Oportunidad** — los datos están disponibles y actualizados a tiempo. Caso: clientes sin actualización de datos en más de 1 año. `SELECT cliente_id, fecha_actualizacion FROM clientes WHERE fecha_actualizacion < CURRENT_DATE - INTERVAL '365 DAY';`
- **Resultado del análisis (cifra real de la referencia)**: se mejoró la calidad de los datos en un 32%, reduciendo riesgos, optimizando la evaluación crediticia y garantizando el cumplimiento normativo.

**Dirección visual**: grid 2×3 de tarjetas, cada una con número, ícono semántico, título, descripción, caso y un bloque de código estilo VS Code (fondo oscuro, sintaxis resaltada) con la consulta SQL real — esto es lo que aporta el elemento gráfico no textual real (código), no un gráfico inventado. Header con el contexto del caso (Caja Rural ABC). Footer con el resultado cuantitativo real (32%).
