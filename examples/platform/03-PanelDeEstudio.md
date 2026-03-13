---
runtime: platform
uses:
  - thorio
  - camile
  - julie
ide_web_runnable: false
ide_web_reason: "Combina Camile y Julie; la parte visual de Camile no es apta para el IDE web."
---

# Ejemplo integrado 03 - Panel de estudio

Este ejemplo mezcla listas, archivos por lineas, validacion de existencia, SQLite y dialogos visuales.

```thorio
funcion unirTareas(tareas: lista_texto) retorna texto
  definir indice como entero
  definir salida como texto

  indice = 0
  salida = ""

  mientras indice < longitud(tareas) hacer
    si indice == 0 entonces
      salida = tareas[indice]
    si_no
      salida = salida + " -> " + tareas[indice]
    fin_si
    indice = indice + 1
  fin_mientras

  retornar salida
fin_funcion

inicio
  definir carpeta como texto
  definir archivo como texto
  definir base como texto
  definir tareas como lista_texto
  definir tareasLeidas como lista_texto
  definir filas como lista_texto
  definir existe como logico

  carpeta = crear_directorio("examples/platform/sandbox/panel")
  archivo = carpeta + "/plan.md"
  base = carpeta + "/panel.sqlite"

  tareas = ["Leer", "Practicar", "Repasar"]
  guardar_lineas(archivo, tareas)
  tareasLeidas = leer_lineas(archivo)
  existe = existe_archivo(archivo)

  sqlite_ejecutar(base, "create table if not exists panel(nombre text, estado text)")
  sqlite_ejecutar(base, "delete from panel")
  sqlite_ejecutar(base, "insert into panel(nombre, estado) values ('Leer', 'hecho')")
  sqlite_ejecutar(base, "insert into panel(nombre, estado) values ('Practicar', 'pendiente')")
  sqlite_ejecutar(base, "insert into panel(nombre, estado) values ('Repasar', 'pendiente')")

  filas = sqlite_consultar_filas(base, "select nombre, estado from panel order by nombre")

  mostrar_mensaje("Archivo listo: " + existe)
  mostrar_mensaje("Plan: " + unirTareas(tareasLeidas))
  mostrar_mensaje("Panel: " + unirTareas(filas))

  si confirmar("¿Eliminar el plan guardado?") entonces
    eliminar_archivo(archivo)
    mostrar_mensaje("Archivo eliminado")
  si_no
    mostrar_mensaje("Archivo conservado")
  fin_si
fin
```
