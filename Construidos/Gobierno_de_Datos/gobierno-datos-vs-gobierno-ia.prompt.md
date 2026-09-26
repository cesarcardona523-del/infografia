# Especificación de Diseño — Infografías Técnicas

(Ver el archivo raíz `INFOGRAFIA-SPEC.md` para el contenido completo compartido por todo el catálogo.)

## Contexto específico — Gobierno de Datos no es Gobierno de IA

**Tema**: 6 diferencias concretas entre gobernar datos y gobernar sistemas de IA, y por qué ambos marcos son complementarios, no intercambiables — el gobierno de datos gobierna la entrada (qué se recolecta, cómo se protege, quién accede), mientras que el gobierno de IA gobierna el comportamiento de un sistema en vivo que razona y decide de forma autónoma.

**Referencia** (1 imagen pegada en el chat, diseño circular hub-and-spoke azul vs ámbar): dos círculos centrales "Gobierno de Datos" / "Gobierno de IA" con 5 nodos numerados cada uno alrededor + 1 par adicional de tarjetas (Linaje de Datos / Notificación de Brechas vs Trazabilidad de Decisiones / Incidentes y Divulgación) — 6 diferencias pareadas en total: Gobierna la entrada↔Gobierna el comportamiento, Estático por diseño↔Diseñado para la deriva, Exactitud de los registros↔Exactitud de las decisiones, Control de acceso↔Autoridad de intervención, Linaje de datos↔Trazabilidad de decisiones, Notificación de brechas↔Incidentes y divulgación.

**Reinterpretación de composición**: en vez del diagrama circular hub-and-spoke (difícil de leer con 12 nodos + texto a 1200×627 sin saturar), se reestructura como **dos columnas pareadas de 6 filas**, una por marco de gobierno, manteniendo el mismo emparejamiento 1 a 1 y el mismo contenido, con una franja central "VS" — más legible sin perder la comparación punto por punto.

**Paleta**: verde+tierra no aplica bien a una comparación de dos conceptos que ya tienen su propio código de color en la referencia (azul=datos, ámbar=IA) — se mantiene esa dualidad azul/ámbar como los dos acentos de la pieza (azul `#2563EB` para Gobierno de Datos, ámbar/tierra `#B8834A` para Gobierno de IA), sobre canvas claro, consistente con "un color de acento además del verde" de la sección Riqueza Visual, aplicado aquí como acento dual en vez de verde+tierra por ser una comparación conceptual 1 a 1, no una aplicación de marca.

**Sin logo de tercero** — firma habitual del catálogo (LinkedIn + cacm523).

**Catálogo**: `categoriaPrincipal: "gobierno-de-datos"`, `temas: ["gobierno-datos", "ia"]` — incluye tema IA (gobierno de sistemas de IA), aplica publicación inmediata.
