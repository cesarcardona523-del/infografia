# Especificación de Diseño — Infografías Técnicas

(Ver el archivo raíz `INFOGRAFIA-SPEC.md` para el contenido completo compartido por todo el catálogo.)

## Contexto específico — CTE (WITH): la Forma Moderna de Ordenar tus Consultas

**Tema**: qué es una Common Table Expression (CTE, `WITH`) en SQL, qué problema resuelve frente a las subconsultas anidadas (legibilidad, orden de lectura de arriba hacia abajo en vez de de adentro hacia afuera), y cómo se pueden encadenar varios CTEs para construir consultas complejas por pasos.

**Referencia** (1 imagen pegada en el chat, paleta clara con acentos azul/naranja/verde — sin marca de tercero visible): 4 bloques — 1) Qué es un CTE + ejemplo de código, 2) comparación lado a lado "Antes" (subconsulta anidada) vs "Ahora" (CTE) con el mismo resultado, 3) Se puede encadenar (varios CTEs referenciando a los anteriores), 4) En resumen (3 checks).

**Estándar visual — Dark IDE obligatorio** (regla fija del tema SQL en CLAUDE.md, no depende de la paleta clara de la referencia): se reconstruye en el archetype oscuro tipo editor de código ya usado en el resto de `Construidos/SQL/` (`#1E1E2E`/`#181825` de fondo, bloques de código en `#14141F`, sintaxis resaltada keyword azul/función ámbar/string verde/comentario gris). SQL genérico/ANSI, sin atarse a un motor concreto.

**Sin logo de tercero** — la referencia no trae marca visible; firma habitual del catálogo (LinkedIn + cacm523).

**Catálogo**: `categoriaPrincipal: "bases-de-datos"`, `temas: ["sql"]` — mismo tratamiento que el resto del tema SQL (cola normal de +2 días, no es contenido de IA).
