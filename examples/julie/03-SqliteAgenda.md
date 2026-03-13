---
runtime: julie
uses:
  - thorio
  - julie
ide_web_runnable: true
ide_web_reason: "Usa Julie y puede ejecutarse en el entorno temporal del IDE web."
---

# Ejemplo Julie 03 - SQLite agenda simple

Este ejemplo crea una base SQLite, inserta datos y consulta la primera columna como `lista_texto`.

```thorio
inicio
  definir base como texto
  definir cambios como entero
  definir personas como lista_texto

  base = "examples/julie/sandbox/agenda.sqlite"

  cambios = sqlite_ejecutar(base, "create table if not exists agenda(nombre text)")
  mostrar "Creacion tabla: " + cambios

  cambios = sqlite_ejecutar(base, "delete from agenda")
  mostrar "Limpieza: " + cambios

  cambios = sqlite_ejecutar(base, "insert into agenda(nombre) values ('Ana')")
  mostrar "Insert 1: " + cambios

  cambios = sqlite_ejecutar(base, "insert into agenda(nombre) values ('Luis')")
  mostrar "Insert 2: " + cambios

  personas = sqlite_consultar_texto(base, "select nombre from agenda order by nombre")

  mostrar "Cantidad: " + longitud(personas)
  mostrar "Primero: " + personas[0]
  mostrar "Lista: " + personas
fin
```
