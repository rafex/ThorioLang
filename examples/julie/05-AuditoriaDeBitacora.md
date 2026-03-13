---
runtime: julie
uses:
  - thorio
  - julie
ide_web_runnable: true
ide_web_reason: "Usa Julie y puede ejecutarse en el entorno temporal del IDE web."
---

# Ejemplo Julie 05 - Auditoria de bitacora

Este ejemplo construye una bitacora a partir de datos guardados en SQLite y la persiste en un archivo `.txt`.

```thorio
funcion construirBitacora(eventos: lista_texto) retorna texto
  definir indice como entero
  definir salida como texto

  indice = 0
  salida = "Eventos"

  mientras indice < longitud(eventos) hacer
    salida = salida + " -> " + eventos[indice]
    indice = indice + 1
  fin_mientras

  retornar salida
fin_funcion

funcion estadoAuditoria(total: entero) retorna texto
  si total >= 4 entonces
    retornar "Auditoria amplia"
  si_no
    retornar "Auditoria breve"
  fin_si
fin_funcion

inicio
  definir base como texto
  definir ruta como texto
  definir cambios como entero
  definir eventos como lista_texto
  definir bitacora como texto
  definir archivo como texto

  base = "examples/julie/sandbox/auditoria.sqlite"
  ruta = "examples/julie/sandbox/auditoria.txt"

  cambios = sqlite_ejecutar(base, "create table if not exists eventos(nombre text)")
  cambios = sqlite_ejecutar(base, "delete from eventos")
  cambios = sqlite_ejecutar(base, "insert into eventos(nombre) values ('inicio')")
  cambios = sqlite_ejecutar(base, "insert into eventos(nombre) values ('lectura')")
  cambios = sqlite_ejecutar(base, "insert into eventos(nombre) values ('validacion')")
  cambios = sqlite_ejecutar(base, "insert into eventos(nombre) values ('cierre')")

  eventos = sqlite_consultar_texto(base, "select nombre from eventos")
  bitacora = construirBitacora(eventos)

  archivo = guardar_texto(ruta, bitacora)
  archivo = anexar_texto(ruta, " :: " + estadoAuditoria(longitud(eventos)))

  mostrar "Archivo generado: " + archivo
  mostrar "Cantidad eventos: " + longitud(eventos)
  mostrar "Bitacora: " + leer_texto(ruta)
fin
```
