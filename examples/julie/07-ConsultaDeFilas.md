---
runtime: julie
uses:
  - thorio
  - julie
ide_web_runnable: true
ide_web_reason: "Usa Julie y puede ejecutarse en el entorno temporal del IDE web."
---

# Ejemplo Julie 07 - Consulta de filas

Este ejemplo consulta varias columnas de SQLite y recibe cada fila serializada como texto.

```thorio
funcion resumenFilas(filas: lista_texto) retorna texto
  definir indice como entero
  definir salida como texto

  indice = 0
  salida = ""

  mientras indice < longitud(filas) hacer
    si indice == 0 entonces
      salida = filas[indice]
    si_no
      salida = salida + " || " + filas[indice]
    fin_si
    indice = indice + 1
  fin_mientras

  retornar salida
fin_funcion

inicio
  definir base como texto
  definir filas como lista_texto
  definir texto como texto

  base = "examples/julie/sandbox/filas.sqlite"

  sqlite_ejecutar(base, "create table if not exists cursos(nombre text, nivel text)")
  sqlite_ejecutar(base, "delete from cursos")
  sqlite_ejecutar(base, "insert into cursos(nombre, nivel) values ('Logica', 'basico')")
  sqlite_ejecutar(base, "insert into cursos(nombre, nivel) values ('Funciones', 'medio')")
  sqlite_ejecutar(base, "insert into cursos(nombre, nivel) values ('SQLite', 'avanzado')")

  filas = sqlite_consultar_filas(base, "select nombre, nivel from cursos order by nombre")
  texto = resumenFilas(filas)

  mostrar "Cantidad filas: " + longitud(filas)
  mostrar "Primera fila: " + filas[0]
  mostrar "Resumen: " + texto
fin
```
