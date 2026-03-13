---
runtime: platform
uses:
  - thorio
  - camile
  - julie
ide_web_runnable: false
ide_web_reason: "Combina Camile y Julie; la parte visual de Camile no es apta para el IDE web."
---

# Agenda visual con SQLite

Recoge un dato desde UI, lo persiste y muestra un resumen inmediato.

```thorio
inicio
  definir base como texto
  definir tarea como texto
  definir conteo como lista_texto

  base = "examples/platform/sandbox/agenda_visual.sqlite"
  tarea = pedir_texto("Que tarea quieres guardar?")

  sqlite_ejecutar(base, "create table if not exists tareas (nombre text);")
  sqlite_ejecutar(base, "insert into tareas values ('" + tarea + "');")

  conteo = sqlite_consultar_texto(base, "select count(*) from tareas;")

  mostrar_mensaje("Tarea guardada: " + tarea)
  mostrar_mensaje("Total de tareas en la agenda: " + conteo[0])
fin
```
