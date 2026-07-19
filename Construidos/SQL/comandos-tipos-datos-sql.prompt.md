# Especificación de Diseño — Infografías Técnicas

> Ver INFOGRAFIA-SPEC.md para el detalle completo (composición editorial, sin fotos/escenas/personas, firma LinkedIn + `cacm523`, 1200×627px).

---

## Contexto específico — Comandos y Tipos de Datos en SQL Server (nuevo tema `SQL`)

**Referencia**: `referencias/SQL/comandos-tipos-datos-sql/ComandosSQL.jpeg` (Microsoft SQL Server) — dos infografías densas en una: comandos más utilizados (DML/DDL/DCL-TCL/Utilidades, ~20 comandos) y tipos de datos más utilizados (~24 tipos en 4 categorías). Primera pieza del tema `SQL`, se aprovecha la sección "Código" de INFOGRAFIA-SPEC.md (VS Code, tipografía monoespaciada, sintaxis resaltada) para una composición de código real anotado — deliberadamente distinta de cualquier grid ya usado en el repositorio.

**Comandos reales (categorías conservadas del original)**: DML (SELECT, INSERT, UPDATE, DELETE, TRUNCATE, BULK INSERT), DDL (CREATE TABLE, ALTER TABLE, DROP TABLE, CREATE INDEX, CREATE VIEW, CREATE PROCEDURE), DCL & TCL (GRANT, REVOKE, DENY, COMMIT, ROLLBACK, SAVEPOINT), Utilidades (BACKUP, RESTORE, EXEC).

**Tipos de datos reales (condensados a 4 categorías, contenido real)**: Numéricos (int, bigint, smallint, decimal(p,s), float, money), Cadenas (varchar(n), nvarchar(n), char(n), text), Fecha y Hora (datetime, datetime2, date, time), Binarios y Otros (varbinary(n), uniqueidentifier, xml, bit).

**Dirección visual (deliberadamente arriesgada)**: ventana de editor estilo VS Code como pieza central, con un script T-SQL real y válido (CREATE TABLE, INSERT, SELECT, UPDATE, GRANT, transacción con COMMIT) resaltado por sintaxis, anotado con las 4 categorías de comandos como callouts laterales — en vez de un grid de tarjetas. Franja inferior compacta de tipos de datos como "cheat sheet".
