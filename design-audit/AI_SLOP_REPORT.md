# AI Slop Report — infografia

Patrones detectados que delatan generación por IA sin dirección artística, con ejemplos reales del repositorio y su alternativa ya validada dentro del propio proyecto.

## 1. "5 iconos en fila + flecha" como proceso genérico

**Ejemplo:** `Construidos/Cultura_Datos/analisis-datos.png` — Recolectar → Limpiar → Analizar → Visualizar → Comunicar, cada paso un cuadrado azul con ícono blanco centrado, flecha gris entre pasos.

Por qué es AI slop: es el layout por defecto que cualquier modelo genera para "explica un proceso de N pasos" sin pensar en la metáfora del contenido. No hay jerarquía (los 5 pasos pesan visualmente igual aunque no lo sean), no hay narrativa espacial, y dejó ~35% de la pieza vacío en la columna izquierda bajo el ícono decorativo de lupa.

**Alternativa ya validada en el repo:** `Construidos/SQL/errores-comunes-group-by.html` — mismo tipo de contenido secuencial, resuelto como comparación código-incorrecto/código-correcto lado a lado con numeración circular, que sí jerarquiza (el error es el protagonista, no el número de paso).

## 2. Grid de tarjetas "beneficio + icono" sin relación entre sí

**Ejemplo:** el bloque "Por Qué Importa" de la misma pieza — 5 tarjetas idénticas (ícono naranja + frase corta), sin conexión visual entre ellas ni con el resto de la pieza.

Por qué es AI slop: es el patrón "bento grid genérico" — cualquier lista de bullets convertida mecánicamente en tarjetas iguales, sin decidir cuál beneficio es el más importante ni por qué esos 5 (y no 4 o 6).

**Mitigación aplicada hoy:** en `GobiernoIA.html` se reemplazó ese tipo de grid por un ciclo de 5 fases numeradas con relación causal explícita entre ellas (fase 1 retroalimenta a fase 5), no una lista plana.

## 3. Dashboards/KPI cards genéricas con barras de progreso sin fuente

**Riesgo detectado, no confirmado como patrón extendido:** en `TrucosSQL.html`, el panel "Impacto en Producción" usa barras de ancho variable (25%/15%/20%) sin cifra numérica visible — es una forma defendible de comunicar "reducción" cualitativa sin fabricar una métrica falsa, pero el patrón de barra-de-progreso-con-ancho-arbitrario es exactamente el que produce AI slop cuando sí lleva un número inventado al lado. Vigilar en piezas futuras: **una barra nunca debe llevar un porcentaje que no venga de una fuente real.**

## 4. Gradientes y "glow blobs" decorativos repetidos sin motivo

Detectado en múltiples piezas del lote de hoy (`TablaPeriodicaIA.html`, `TrucosSQL.html`, `VejesDashboard.html`, `GobiernoIA.html`): dos manchas radiales difuminadas (`filter: blur(80px)`) en las esquinas superior-izquierda e inferior-derecha del canvas, en verde y ámbar translúcidos.

Por qué es un riesgo de convertirse en slop: es un truco visual fácil de repetir sin pensar — si aparece en toda pieza nueva sin variar posición/intensidad/color según el contenido, deja de ser una decisión de dirección de arte y pasa a ser una plantilla. Hoy todavía es sutil y consistente con la paleta, pero es el patrón más "clonado copy-paste entre archivos" de todo el lote reciente.

**Recomendación:** documentarlo como técnica válida en `INFOGRAFIA-SPEC.md` (si no lo está ya) pero exigir que la posición/tamaño varíe según la composición real de cada pieza, no un copy-paste de coordenadas.

## 5. Bordes de color plano en el borde superior de cada card (`::before` de 3px)

Presente en prácticamente toda pieza con grid de tarjetas del lote reciente. Es un patrón visualmente aceptable y coherente con Microsoft Learn/Azure Architecture Center (referencia validada en el spec), así que **no se marca como slop** — es una decisión de marca consistente, no un default sin pensar. Se documenta aquí solo para que quede registrado como patrón *intencional* y no se confunda con los anteriores.

## 6. `backdrop-filter: blur()` como atajo de "look premium"

No es un problema estético sino técnico descubierto esta sesión: usarlo como reflejo (glassmorphism "porque se ve bien") sin verificar el pipeline de renderizado causó contenido invisible en al menos 2 piezas (`EvolucionDeLaIngenieriaDeIA.html`, y preventivamente removido de 11 más). Es un caso donde perseguir una estética de moda sin verificar el resultado real es, en la práctica, el mismo problema de fondo que el AI slop: aplicar un efecto porque "así se ve en las referencias" sin razonar si aporta a esa pieza específica.

## Patrones que el repo ya evita bien (no repetir el error de "corregir lo que no está roto")

- El uso de metáforas visuales concretas (pirámides, icebergs, tablas periódicas, básculas) ya está en la spec y se aplicó hoy en `tabla-periodica-herramientas-ia` — mantenerlo como estándar, no regresar al grid genérico.
- La comparación código-incorrecto/código-correcto lado a lado (SQL) es un patrón fuerte y reutilizable — candidato a generalizarse a otros temas con contraste binario (ej. configuración segura vs. insegura en gobierno de datos).
