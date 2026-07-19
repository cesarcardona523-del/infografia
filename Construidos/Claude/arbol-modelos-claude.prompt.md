# Especificación de Diseño — Infografías Técnicas

> Ver INFOGRAFIA-SPEC.md para el detalle completo (composición editorial, sin fotos/escenas/personas, firma LinkedIn + `cacm523`, 1200×627px).

---

## Contexto específico — Árbol de Modelos de Claude

**Referencia**: `referencias/Claude/arbol-modelos-claude/ModelosClaude.jpeg` (Henry Jiménez / Evolupedia) — árbol de decisión real de 3 preguntas binarias que termina en 4 modelos. Se conserva la estructura de árbol/flowchart genuino (diamantes de decisión, ramas SÍ/NO) en vez de convertirlo en un grid — es la forma correcta de representar una decisión secuencial.

**El árbol completo (contenido real)**:
- Raíz: "¿Tu tarea necesita algo más que una respuesta rápida?"
  - NO → "¿Necesitas máxima velocidad y el menor gasto de tokens?"
    - SÍ → **Haiku 4.5** (ligero, ahorra tokens) — chat sin archivos, activa búsqueda web. Prompt: "Quiero [resultado] con [condiciones]. Hazme preguntas usando AskUserQuestion antes de empezar."
    - NO → **Sonnet 5** (rápido, modelo del día a día) — tareas simples, conecta con Slack/Drive/Notion/Figma y 50+ más. Prompt: "Eres [rol]. [Tarea] con [input]. Mantenlo en [longitud]. Tono: [casual/formal]. Sin preámbulos. Solo el resultado."
  - SÍ → "¿Es este tu trabajo más difícil y más ambicioso?"
    - NO → **Opus 4.8** (modelo para trabajo profundo) — Cowork + esfuerzo en High siempre, usa Skills en Projects. Prompt: "8 herramientas de IA que uso cada día. NO empieces aún. Hazme preguntas de aclaración para afinar el enfoque paso a paso."
    - SÍ → **Fable 5** (el modelo más inteligente) — tareas complejas de extremo a extremo, investigación profunda y razonamiento duro. Prompt: "Este es mi objetivo: [objetivo]. Estas son mis restricciones: [restricciones]. Piensa alternativas, propón 2-3 enfoques y recomienda uno con tu razonamiento." Nota: reservar para el 10% de tareas que de verdad lo necesitan (consume más tokens).

**Dirección visual**: árbol de decisión real (flowchart genuino con nodos de pregunta y ramas SÍ/NO en verde/rojo) que desciende hacia 4 tarjetas de modelo — composición nueva en el repositorio, ya que ningún otro tema usa un árbol de decisión binario real.
