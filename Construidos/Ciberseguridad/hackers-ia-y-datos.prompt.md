# Especificación de Diseño — Infografías Técnicas

(Ver el archivo raíz `INFOGRAFIA-SPEC.md` para el contenido completo compartido por todo el catálogo.)

## Contexto específico — Hackers, IA y Datos

**Evento**: AVANZATEC — Masterclass junto a IBM.
**Realizado por**: IBM.

**Tema**: cómo la inteligencia artificial cambió simultáneamente el ataque y la defensa en ciberseguridad — de "genio en capucha" a atacante-empresa aumentado por IA (phishing perfecto, voz/video clonados, perfilado automático, explotación en horas), y del lado defensivo, IA que detecta comportamiento anómalo, actúa como copiloto del analista y responde en segundos — cerrando con cifras 2026 de impacto y un plan de acción de 3 hábitos.

**Referencia**: ~20 capturas de un mismo deck de la masterclass (algunas con anotaciones a mano en rojo), cubriendo: 1) triángulo Hackers/IA/Datos, 2) evolución del atacante 80s→2024, 3) frase "el hacker de hoy es una empresa" + caso LockBit, 4) cómo la IA ataca (6 técnicas), 5) cómo la IA defiende (Big Sleep de Google como caso real), 6-9) diapositivas propias de IBM sobre ataques impulsados por IA / a la IA / robo de IA y matriz de riesgo, 10) estadísticas de velocidad de contención (IBM Cost of a Data Breach Report 2026), 11) estadísticas de costo/terceros/uso no autorizado de IA (IBM CODB 2026 + Verizon DBIR 2026), 12) el correo como llave maestra, 13) cifras de Colombia Q1 2026 (Policía Nacional/Ministerio de Defensa vía El Tiempo), 14) plan de 7 días, 15) "Hackearon la confianza", 16) qué viene 2026→2031, 17) cierre Pausa/Verifica/Protege.

**Curación obligatoria**: el material fuente son ~20 diapositivas de una charla completa — no cabe todo en 1200×627. Se seleccionó el arco narrativo esencial (quién ataca/con qué/qué buscan → cómo cambió el atacante → IA ataca vs IA defiende → cifras de impacto 2026 → plan de acción) y se omitieron las diapositivas de encuesta interactiva (sin contenido propio) y las diapositivas que son capturas literales de slides internas de IBM con anotaciones a mano de un tercero (esas se resumen como dato, no se replican visualmente).

**No se replica ninguna marca de tercero** de las capturas (nombres de presentadores, anotaciones a mano) — solo la firma habitual del catálogo (LinkedIn + cacm523) y el branding del evento (AVANZATEC / Realizado por IBM).

**Colores de marca**: IBM — azul `#0F62FE` (IBM Blue, Carbon Design System) sobre base oscura `#161616` (Carbon Gray 100), con acentos cian/naranja tomados de la propia codificación de color del deck original (cian = defensa con IA, naranja/rojo = ataque). Aplica la excepción de paleta de Branding de Evento (paleta propia, no verde+tierra).

**Íconos reales usados**: `assets/iconos-apps/ibm.svg` (logo oficial, descargado de dashboardicons.com para esta pieza).

**Fuentes citadas en la pieza** (según las diapositivas de origen): IBM Cost of a Data Breach Report 2026; Verizon Data Breach Investigations Report 2026; Policía Nacional y Ministerio de Defensa de Colombia, vía El Tiempo (mayo 2026).

**Catálogo**: `categoriaPrincipal: "inteligencia-artificial"`, `temas: ["ia"]` (no existe una clave "ciberseguridad" en `taxonomia.json`; no se inventa una nueva sin autorización del usuario — se usa únicamente `ia`, que cubre el eje central de la pieza), `tipoContenido: "evento"` — `fechaPublicacion` = fecha/hora actual (regla de Branding de Evento), no la cola normal.
