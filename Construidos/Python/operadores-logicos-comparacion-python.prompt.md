# Especificación de Diseño — Infografías Técnicas

(Ver el archivo raíz `INFOGRAFIA-SPEC.md` para el contenido completo compartido por todo el catálogo.)

## Contexto específico — Operadores de Comparación y Lógicos en Python

**Tema**: análogo en Python de `Construidos/SQL/operadores-comparacion-and-or-sql.html` (usado como referencia interna/base de este tópico, según lo pedido por el usuario) — los 6 operadores de comparación, los conectores lógicos `and`/`or` como intersección/unión, y una sección potenciada nueva (no existía en la versión SQL) sobre operadores de **identidad y pertenencia**: `is`, `is not`, `in`, `not in`.

**Diferencias reales de contenido frente a la versión SQL** (no es una copia — Python se comporta distinto y eso es lo que hace valioso el contraste):
- En SQL, `< > <= >=` **no aplican a texto** (un motor SQL no puede decidir si "Bogotá" es "mayor" que "Cali" sin una colación explícita). En Python, en cambio, **sí aplican a strings** — Python compara cadenas lexicográficamente (orden alfabético/Unicode), por eso `'ana' < 'bruno'` es `True`. Esta es la diferencia central que justifica no solo traducir la sintaxis sino rediseñar la tabla de aplicabilidad.
- `and`/`or` en Python son minúsculas (vs. `AND`/`OR` de SQL) y tienen **evaluación de cortocircuito** (short-circuit): `and` devuelve el primer valor falsy o el último; `or` devuelve el primer valor truthy o el último — no son solo booleanos, devuelven el valor real.
- **Potenciación pedida explícitamente por el usuario**: agregar `is`, `is not`, `in`, `not in` — operadores que no tienen equivalente directo en el WHERE de SQL de la pieza original:
  - `is` / `is not` comparan **identidad** (mismo objeto en memoria), no valor — distinto de `==`/`!=` que comparan valor. Caso de uso real y muy común: `x is None` en vez de `x == None`.
  - `in` / `not in` comprueban **pertenencia** a una secuencia (lista, tupla, string, set, dict) — sin equivalente de una sola palabra en SQL estándar (el más cercano es la cláusula `IN (...)`, pero conceptualmente distinta: en SQL es sintaxis de la cláusula WHERE, en Python es un operador de propósito general sobre cualquier iterable).

**Paleta — corregida (2026-09-15, señalado por el usuario)**: Python es el lenguaje/aplicación protagonista y exclusiva de esta pieza → aplica la excepción de "Colores de marca por aplicación" de CLAUDE.md: azul y amarillo de marca (`#3776AB`, `#FFD43B`), no el verde+tierra por defecto. El ícono oficial de Python (`assets/iconos-apps/python.svg`) también debe usarse en el eyebrow, embebido inline — un error de la primera versión de esta pieza fue usar la paleta por defecto y un ícono genérico dibujado a mano en vez del real, corregido en esta revisión.

**Catálogo**: `categoriaPrincipal: "programacion"`, `temas: ["python"]`.
