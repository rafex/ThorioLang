---
runtime: julie
uses:
  - thorio
  - julie
ide_web_runnable: true
ide_web_reason: "Usa Julie y puede ejecutarse en el entorno temporal del IDE web."
---

# SQLite metricas de estudio

Crea una base de datos, inserta registros y consulta resultados agregados.

```thorio
inicio
  definir base como texto
  definir totales como lista_texto
  definir materias como lista_texto

  base = "examples/julie/sandbox/metricas_estudio.sqlite"

  sqlite_ejecutar(base, "drop table if exists sesiones;")
  sqlite_ejecutar(base, "create table sesiones (materia text, minutos integer);")
  sqlite_ejecutar(base, "insert into sesiones values ('Matematicas', 45);")
  sqlite_ejecutar(base, "insert into sesiones values ('Historia', 30);")
  sqlite_ejecutar(base, "insert into sesiones values ('Matematicas', 50);")

  totales = sqlite_consultar_texto(base, "select sum(minutos) from sesiones;")
  materias = sqlite_consultar_texto(base, "select materia from sesiones order by rowid;")

  mostrar "Minutos acumulados: " + totales[0]
  mostrar "Materias registradas: " + materias
fin
```
