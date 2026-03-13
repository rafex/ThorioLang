# Reporte de filas formateadas

Consulta multiples columnas desde SQLite y muestra las filas renderizadas.

```thorio
inicio
  definir base como texto
  definir filas como lista_texto

  base = "examples/julie/sandbox/reporte_filas.sqlite"

  sqlite_ejecutar(base, "drop table if exists cursos;")
  sqlite_ejecutar(base, "create table cursos (nombre text, nivel text, cupos integer);")
  sqlite_ejecutar(base, "insert into cursos values ('Algoritmos', 'intermedio', 18);")
  sqlite_ejecutar(base, "insert into cursos values ('Bases de datos', 'avanzado', 12);")

  filas = sqlite_consultar_filas(base, "select nombre, nivel, cupos from cursos order by nombre;")

  mostrar "Total de filas: " + longitud(filas)
  mostrar filas[0]
  mostrar filas[1]
fin
```
