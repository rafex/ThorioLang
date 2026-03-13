---
runtime: platform
uses:
  - thorio
  - camile
  - julie
ide_web_runnable: false
ide_web_reason: "Combina Camile y Julie; la parte visual de Camile no es apta para el IDE web."
---

# Agenda visual persistente

Ejemplo integrado con entrada visual, SQLite y exportacion a texto.

```thorio
funcion unirContactos(contactos: lista_texto) retorna texto
  definir indice como entero
  definir salida como texto

  indice = 0
  salida = ""

  mientras indice < longitud(contactos) hacer
    si indice == 0 entonces
      salida = contactos[indice]
    si_no
      salida = salida + " | " + contactos[indice]
    fin_si
    indice = indice + 1
  fin_mientras

  retornar salida
fin_funcion

inicio
  definir carpeta como texto
  definir base como texto
  definir reporte como texto
  definir nombre1 como texto
  definir nombre2 como texto
  definir contactos como lista_texto
  definir continuar como logico

  carpeta = crear_directorio("examples/platform/sandbox/agenda")
  base = carpeta + "/agenda.sqlite"
  reporte = carpeta + "/agenda.txt"

  sqlite_ejecutar(base, "create table if not exists agenda(nombre text)")
  sqlite_ejecutar(base, "delete from agenda")

  nombre1 = pedir_texto("Primer contacto")
  nombre2 = pedir_texto("Segundo contacto")

  sqlite_ejecutar(base, "insert into agenda(nombre) values ('" + nombre1 + "')")
  sqlite_ejecutar(base, "insert into agenda(nombre) values ('" + nombre2 + "')")

  contactos = sqlite_consultar_texto(base, "select nombre from agenda order by nombre")
  guardar_texto(reporte, "Agenda: " + unirContactos(contactos))

  mostrar_mensaje("Contactos guardados: " + longitud(contactos))
  continuar = confirmar("¿Mostrar resumen final?")

  si continuar entonces
    mostrar_mensaje(leer_texto(reporte))
  si_no
    mostrar_mensaje("Resumen omitido")
  fin_si
fin
```
