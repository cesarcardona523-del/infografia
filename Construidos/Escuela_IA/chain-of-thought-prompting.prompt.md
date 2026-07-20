# Especificación de Diseño — Infografías Técnicas

> Ver INFOGRAFIA-SPEC.md para el detalle completo. Sin fotos/escenas/personas, firma LinkedIn + `cacm523`, 1200×627px.

## Contexto específico — Chain of Thought

**Evento**: Escuela de Inteligencia Artificial · **Realizado por**: Uniremington. Mismo branding que el resto del lote.

**Referencias**: `referencias/Escuela de Inteligencia Artificial/image (25).png, (26).png` — Sesión 2 (Prompt Engineering), primera pieza de esa sesión en este lote.

**Contenido real (sin inventar cifras)**:

- **Técnica clave**: pedirle a la IA que "piense paso a paso" mejora dramáticamente la calidad de sus respuestas. No es un truco — es cómo funciona mejor la arquitectura del modelo.
- **Sin Chain of Thought** — Prompt: *"Hazme una página web para venta de boletería"*. Respuesta: genera un HTML genérico con formulario básico, sin considerar pagos, asientos ni validaciones.
- **Con Chain of Thought** — Prompt: *"Piensa paso a paso: ¿qué necesita una página web de venta de boletería? Primero lista los requisitos, luego diseña la estructura, y finalmente genera el código."* Respuesta: analiza requisitos (catálogo de eventos, selección de asientos, pasarela de pago, confirmación por email), propone arquitectura, y genera código completo y funcional.
- **¿Por qué funciona?**: el modelo genera un token a la vez. Cuando le pides razonar paso a paso, cada paso intermedio se convierte en contexto para el siguiente — como darle más "espacio para pensar". 3 mecanismos: (1) **Descompone el problema** — en vez de saltar a la respuesta, identifica sub-problemas. (2) **Genera contexto intermedio** — cada paso que escribe se vuelve parte del input para el siguiente. (3) **Reduce errores acumulados** — los pasos visibles permiten "corregir el rumbo" antes de la conclusión.

**Dirección visual**: comparación superior de dos columnas (Sin CoT en gris/apagado vs. Con CoT en verde/vívido) con prompt + respuesta real de cada una; fila inferior de 3 mecanismos numerados que explican por qué funciona.
