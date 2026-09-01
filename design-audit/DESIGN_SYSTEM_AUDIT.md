# Design System Audit — infografia

No existe un design system en el sentido de tokens/componentes en tiempo de ejecución (correcto para el formato del proyecto — ver `PROJECT_INVENTORY.md`). Lo que sí existe es un **design system documental**: las reglas de [INFOGRAFIA-SPEC.md](../INFOGRAFIA-SPEC.md) que cada HTML reimplementa por su cuenta en CSS. Esta auditoría evalúa esa capa documental y su nivel real de cumplimiento en las piezas construidas.

## Tipografía

- **Regla documentada:** familia sans-serif consistente (Inter/system), jerarquía definida.
- **Cumplimiento observado:** alto en piezas recientes; varias piezas antiguas (`Cultura_Datos`, `Bigdata`) importaban Google Fonts vía `<link>`/`@import` — **bug de robustez, no solo de consistencia**, porque el pipeline de export es Chrome headless sin garantía de red disponible en el momento del render. Corregido en las 20 piezas del lote de hoy (fuentes removidas, fallback a system fonts).
- **Recomendación:** auditar el resto del catálogo histórico (86 piezas previas) por el mismo patrón de `@import`/`<link>` a Google Fonts la próxima vez que se toque cada tema, no en un barrido dedicado (consistente con la regla de "no auditar todos los temas de una sola vez").

## Paleta de colores

- **Regla documentada:** verde primario + un acento tierra, excepción de paleta arriesgada por pieza dentro de un mismo tema (agregada hoy).
- **Cumplimiento observado:** alto en el lote de hoy. Riesgo puntual detectado y corregido: `BlueArquitecturaDatos.html` traía una paleta azul/cian de "blueprint" que no seguía el sistema — se recoloreó a verde+tierra antes de publicar.
- **Deuda histórica:** `Bigdata/` usa una paleta ámbar/marrón dominante (no verde) en varias piezas — no auditada a fondo esta pasada; candidata a revisión si se vuelve a tocar ese tema.

## Espaciados

- **Regla documentada (nueva, agregada hoy):** ninguna tarjeta debe quedar con más de 30-40% de altura vacía bajo su contenido; el ajuste de tamaño de fuente es una herramienta de último recurso, no la primera respuesta.
- **Cumplimiento observado:** la regla nació precisamente porque el patrón contrario (espacio vacío resuelto agrandando fuente o dejándolo así) era sistemático en piezas antiguas y en los primeros intentos del lote de hoy (`GobiernoIA.html` necesitó 2 iteraciones para cumplirla realmente).

## Componentes recurrentes (no compartidos en código, pero sí en convención)

| "Componente" informal | Consistencia entre piezas | Nota |
|---|---|---|
| Tarjeta con borde superior de 3px de color | Alta en lote reciente | Buen patrón de marca, digno de mantenerse |
| Signature block (LinkedIn + `cacm523`) | Alta en todo el catálogo | Es la pieza más "componentizada" del proyecto, aunque solo por copy-paste |
| Badge/tag con fondo translúcido de color | Media | Nombres de clase inconsistentes entre piezas (`.tag`, `.badge`, `.pillar-freq`) — mismo propósito visual, sin convención de nombre compartida |
| Bloque de código con syntax highlighting manual | Media-alta en piezas técnicas recientes (SQL, arquitectura) | Cada pieza reimplementa sus propias clases `.kw`/`.str`/`.fn` — funciona pero es CSS duplicado entre archivos sin fuente compartida |

## Estados e interacción

No aplica — el formato es una imagen estática sin runtime (hover, focus, error states no existen en el entregable final). Cualquier CSS de esos estados en el HTML fuente es código muerto y debería eliminarse al modificar un archivo, por la regla de "Calidad de código" ya vigente en CLAUDE.md.

## Accesibilidad

- El entregable final es un PNG — no hay accesibilidad de navegación/teclado que auditar en el output.
- Lo único auditable es **contraste de color** dentro de la imagen. No se detectaron violaciones evidentes de contraste en las piezas revisadas hoy (texto oscuro sobre fondo claro, texto claro sobre fondo oscuro consistente).

## Responsive

No aplica — tamaño fijo 1200×627px por diseño del proyecto, coherente con el formato de imagen para redes sociales.

## Conclusión

El "design system" del proyecto vive más en la disciplina de un documento (`INFOGRAFIA-SPEC.md`) que se re-lee y re-aplica manualmente en cada pieza, que en artefactos de código reutilizables. Es una arquitectura válida para el volumen y formato actual (106 piezas, sin runtime compartido), pero acumula deuda silenciosa: nombres de clase inconsistentes entre piezas para el mismo propósito visual, y CSS duplicado (bloques de código, badges) que un snippet de referencia compartido —documentado, no ejecutado— podría reducir sin violar la regla de "no hay stylesheet compartido en runtime".
