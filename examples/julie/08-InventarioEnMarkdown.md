---
runtime: julie
uses:
  - thorio
  - julie
ide_web_runnable: true
ide_web_reason: "Usa Julie y puede ejecutarse en el entorno temporal del IDE web."
---

# Inventario en Markdown

Guarda una lista de articulos en un archivo Markdown y despues la vuelve a leer.

```thorio
funcion ultimo_item(items: lista_texto) retorna texto
  retornar items[longitud(items) - 1]
fin_funcion

inicio
  definir ruta como texto
  definir items como lista_texto
  definir leidos como lista_texto

  ruta = "examples/julie/sandbox/inventario.md"
  items = ["Cuaderno", "Lapiz", "Regla", "Borrador"]

  guardar_lineas(ruta, items)
  leidos = leer_lineas(ruta)

  mostrar "Items guardados: " + longitud(leidos)
  mostrar "Primer item: " + leidos[0]
  mostrar "Ultimo item: " + ultimo_item(leidos)
fin
```
