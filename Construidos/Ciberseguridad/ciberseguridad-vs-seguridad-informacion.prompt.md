# Especificación de Diseño — Infografías Técnicas

> Fuente de verdad del diseño — evoluciona con el proyecto (ver "Rol permanente y mejora continua" en CLAUDE.md). **No se modifica con contenido técnico específico de un tema** — eso vive en el `prompt.md` de su propia carpeta. Solo se actualiza aquí cuando una mejora de diseño generaliza a todas las infografías.

(Ver el archivo raíz `INFOGRAFIA-SPEC.md` para el contenido completo compartido por todo el catálogo — paleta, tipografía, composición, elementos prohibidos, branding, firma, tamaño 1200×627px.)

## Contexto específico — Ciberseguridad vs Seguridad de la Información (+ el factor IA)

**Tema**: aclarar la diferencia entre dos disciplinas que suelen confundirse — Seguridad de la Información (protege la información en sí, cualquiera sea su soporte) y Ciberseguridad (defiende la tecnología que la contiene, contra amenazas digitales) — y sumar cómo la IA está cambiando ambas disciplinas al mismo tiempo.

**Referencia suministrada por el usuario** (1 imagen pegada en el chat, sin archivo guardado en disco): infografía de marca personal (Mario Najera) con layout de 3 columnas — Seguridad de la Información (izquierda) / Diferencias Clave (centro, franja angosta con 5 criterios: Alcance, Enfoque, Objetivo, Pregunta Clave, Impacto) / Ciberseguridad (derecha) — cierra con 3 cajas de resumen y firma de marca.

**Corrección explícita pedida por el usuario sobre la referencia** (antes de construir): el encabezado de la referencia (ícono de bombilla gigante + título en 3 líneas ocupando toda la esquina superior izquierda) se ve invasivo y ocupa demasiado espacio. **No replicar ese tratamiento** — usar el header compacto ya estandarizado en el catálogo: eyebrow en píldora pequeña y alargada (ícono + texto en una sola línea) + título + subtítulo, igual que en el resto de las piezas del proyecto (ver `modelos-ia-lideres-mercado-2026.html` o `data-lake-warehouse-lakehouse.html` como referencia de estilo ya validado).

**Aporte pedido por el usuario tras la corrección de diseño**: potenciar el tema con lo que está pasando con la IA en ambas disciplinas — se agrega una banda transversal "El Nuevo Factor: la IA" que cruza ambas columnas, con el impacto de la IA en Seguridad de la Información (gobernanza de datos de entrenamiento, clasificación de información usada por modelos, políticas de uso responsable) y en Ciberseguridad (IA como arma de ataque — phishing/deepfakes generados por IA, malware más sofisticado — e IA como herramienta de defensa — detección de anomalías, respuesta automatizada a incidentes). Contenido cualitativo y conceptual, sin cifras o benchmarks específicos no verificables (no hay una fuente de datos numérica para este tema, a diferencia de las piezas de modelos de IA).

**Estructura elegida** (variante del "blueprint numerado" de INFOGRAFIA-SPEC.md — comparación de 2 vías + banda transversal):
- Header compacto: eyebrow + título + subtítulo (sin ícono grande).
- 3 columnas: Seguridad de la Información (numerada 1) | Diferencias Clave (franja central angosta, 5 criterios con ícono) | Ciberseguridad (numerada 2).
- Banda transversal inferior "El Nuevo Factor: la IA", con dos mitades (una por disciplina) mostrando cómo la IA la está transformando.
- Cierre: 3 cajas de resumen breve (una por columna + una integradora), firma profesional.

**Paleta**: verde+tierra por defecto del proyecto — la referencia usa azul/cian corporativo de la marca Mario Najera, pero este no es un tema de aplicación/herramienta con marca propia (es un tema de gobierno/seguridad), así que no aplica la excepción de "Colores de marca por aplicación": se usa la paleta estándar del catálogo, no la de la referencia.

**Iconografía**: íconos semánticos genéricos (escudo, candado, radar, alcance/target, engranaje, pregunta, gráfico de impacto, cerebro/IA) — ninguno es una marca comercial.

**Taxonomía — pendiente de aprobación del usuario**: `taxonomia.json` no tiene actualmente ningún `tema` para "ciberseguridad" ni "seguridad-informacion", y el contenido no encaja con precisión en ningún `categoriaPrincipal`/`tema` existente (lo más cercano es `gobierno-de-datos`/`gobierno-datos`, pero no es exactamente lo mismo). Por la regla de gobernanza de la taxonomía del proyecto, no se agrega la entrada al catálogo (`publicaciones.json`/`publicaciones.js`) hasta que el usuario apruebe cómo clasificarla — la pieza (HTML/PNG/prompt.md) se construye y queda lista, pero la publicación en el catálogo queda pendiente de esa decisión.
