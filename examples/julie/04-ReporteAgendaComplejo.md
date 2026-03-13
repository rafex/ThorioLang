---
runtime: julie
uses:
  - thorio
  - julie
ide_web_runnable: true
ide_web_reason: "Usa Julie y puede ejecutarse en el entorno temporal del IDE web."
---

# Ejemplo Julie 04 - Reporte de agenda complejo

Este ejemplo combina SQLite, listas, funciones, condicionales y escritura de un reporte Markdown.

```thorio
funcion unirNombres(valores: lista_texto) retorna texto
  definir indice como entero
  definir salida como texto

  indice = 0
  salida = ""

  mientras indice < longitud(valores) hacer
    si indice == 0 entonces
      salida = valores[indice]
    si_no
      salida = salida + " | " + valores[indice]
    fin_si

    indice = indice + 1
  fin_mientras

  retornar salida
fin_funcion

funcion estadoAgenda(total: entero) retorna texto
  si total >= 3 entonces
    retornar "Agenda completa"
  si_no
    si total == 2 entonces
      retornar "Agenda parcial"
    si_no
      retornar "Agenda minima"
    fin_si
  fin_si
fin_funcion

inicio
  definir base como texto
  definir ruta como texto
  definir cambios como entero
  definir personas como lista_texto
  definir resumen como texto
  definir reporte como texto

  base = "examples/julie/sandbox/reporte_agenda.sqlite"
  ruta = "examples/julie/sandbox/reporte_agenda.md"

  cambios = sqlite_ejecutar(base, "create table if not exists agenda(nombre text)")
  mostrar "Creacion tabla: " + cambios

  cambios = sqlite_ejecutar(base, "delete from agenda")
  mostrar "Limpieza: " + cambios

  cambios = sqlite_ejecutar(base, "insert into agenda(nombre) values ('Ana')")
  cambios = sqlite_ejecutar(base, "insert into agenda(nombre) values ('Luis')")
  cambios = sqlite_ejecutar(base, "insert into agenda(nombre) values ('Marta')")

  personas = sqlite_consultar_texto(base, "select nombre from agenda order by nombre")
  resumen = unirNombres(personas)

  reporte = guardar_texto(ruta, "# Reporte agenda")
  reporte = anexar_texto(ruta, " :: " + estadoAgenda(longitud(personas)))
  reporte = anexar_texto(ruta, " :: Contactos=" + resumen)

  mostrar "Reporte: " + reporte
  mostrar "Total: " + longitud(personas)
  mostrar "Resumen: " + resumen
fin
```
