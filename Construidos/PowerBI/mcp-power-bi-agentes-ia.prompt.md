# Especificación de Diseño — Infografías Técnicas

(Ver el archivo raíz `INFOGRAFIA-SPEC.md` para el contenido completo compartido por todo el catálogo.)

## Contexto específico — MCP + Power BI

**Tema**: cómo el Power BI MCP server (Microsoft, en preview público) permite que agentes de IA (Copilot, Claude u otro cliente MCP) se conecten de forma gobernada a modelos semánticos de Power BI — consultar en lenguaje natural, generar DAX y, en el servidor local, modelar — respetando permisos y sin copiar los datos fuera del sistema.

**Referencia** (1 imagen pegada en el chat, sin marca de tercero visible, tema oscuro azul marino con acento ámbar): header con ícono de escudo, dos tarjetas "¿Qué es MCP?" / "¿Qué es el Power BI MCP?", banda "Cómo funciona" con flujo Usuario→Agente IA→Servidor MCP→Modelo semántico→Insights (con logos de Microsoft Copilot, Model Context Protocol y Power BI), dos paneles "Servidor remoto" vs "Servidor local", y una sección final "Por qué importa para tu organización" con 4 bullets. Cita fuente: Microsoft Learn — documentación del Power BI MCP server (preview público).

**Colores de marca combinados** (regla "varias marcas en una misma pieza" — Power BI y Microsoft Copilot son protagonistas explícitos del flujo): Power BI (`#F2C811` amarillo/dorado, `#000000`) como acento principal, Microsoft Copilot (`#0067B8`→`#50E6FF`) para su nodo del flujo — MCP (Model Context Protocol) no tiene identidad de marca propia con color oficial, se usa iconografía semántica genérica (nodo de conexión/enchufe) en un tono neutro.

**Íconos reales usados**: `assets/iconos-apps/power-bi.svg`, `microsoft-copilot.svg` (ya en el repo). MCP sin logo oficial — ícono genérico de "conexión/protocolo".

**Sin logo de tercero** — la referencia no trae marca visible de otro creador; firma habitual del catálogo (LinkedIn + cacm523).

**Catálogo**: `categoriaPrincipal: "powerbi-y-visualizacion"`, `temas: ["power-bi", "ia", "agentes-ia"]` — incluye tema IA (agentes conectándose vía MCP), aplica publicación inmediata al ser también contenido de IA.
