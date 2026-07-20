# Especificación de Diseño — Infografías Técnicas

> Ver INFOGRAFIA-SPEC.md para el detalle completo. Sin fotos/escenas/personas, firma LinkedIn + `cacm523`, 1200×627px.

## Contexto específico — Cómo Funciona un LLM

**Evento**: Escuela de Inteligencia Artificial · **Realizado por**: Uniremington. Mismo branding que el resto del lote (logo real, azul `#00467F` + rojo `#EE3124`).

**Referencias**: `referencias/Escuela de Inteligencia Artificial/image (3).png, (7).png, (13).png, (15).png, (16).png` — Sesión 1, sección de mecanismo técnico.

**Contenido real (sin inventar cifras), 4 conceptos**:
1. **Aprende de datos** — ejemplo real de la referencia: enseñar a una computadora a reconocer gatos sin explicarle qué es un gato, solo mostrándole miles de fotos etiquetadas. Flujo: Miles de fotos → Intenta adivinar → Se corrige → Aprende (después de millones de intentos). Las capas internas detectan cosas cada vez más complejas (bordes, formas, orejas, bigotes) hasta entender "gato" — por eso se llama *deep* learning.
2. **Convierte palabras en números** — cada palabra se transforma en una lista de números que captura su significado. "Rey" y "Reina" tienen números parecidos porque significan cosas similares.
3. **Presta atención a todo el contexto** — en vez de leer palabra por palabra, el modelo mira TODA la oración a la vez y decide qué palabras se relacionan entre sí. Ejemplo real: en *"El banco estaba lleno de peces"*, la atención conecta "banco" con "peces" para entender que es un banco de peces, no uno financiero.
4. **Predice el siguiente token** — el modelo calcula una distribución de probabilidad sobre la siguiente palabra posible. Ejemplo real: ante el input *"El gato se"*, predice "sentó" (72%), "subió" (15%), "durmió" (8%). No "entiende": calcula probabilidades sobre todo lo que leyó.

**Cierre (idea central de la referencia)**: no "entiende" el lenguaje — calcula qué palabra es más probable, basado en patrones aprendidos de billones de textos. Por eso sin buen contexto las respuestas son genéricas.

**Dirección visual**: grid 2×2 de tarjetas, cada una con su ejemplo concreto real integrado (mini-flujo, par de palabras, oración resaltada, o barras de probabilidad) — el elemento gráfico no textual varía por tarjeta en vez de repetir el mismo patrón. Numeración 1-4 como secuencia lógica (de cómo aprende a cómo predice).
