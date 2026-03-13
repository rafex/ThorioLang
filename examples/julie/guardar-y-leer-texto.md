---
runtime: julie
uses:
  - thorio
  - julie
ide_web_runnable: true
ide_web_reason: "Usa archivos con Julie y puede ejecutarse en un workspace temporal del IDE web."
---

# Guardar y leer texto

Ejemplo basico de persistencia con archivos usando Julie.

```thorio
inicio
  definir ruta como texto
  definir escrito como texto
  definir contenido como texto

  ruta = "examples/julie/sandbox/nota.txt"

  escrito = guardar_texto(ruta, "Julie guarda texto simple")
  contenido = leer_texto(ruta)

  mostrar "Archivo creado: " + escrito
  mostrar "Contenido leido: " + contenido
fin
```
