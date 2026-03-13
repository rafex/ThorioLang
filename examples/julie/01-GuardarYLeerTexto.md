---
runtime: julie
uses:
  - thorio
  - julie
ide_web_runnable: false
ide_web_reason: "Usa 'leer' y Julie; requiere entrada interactiva, por lo que no es apto para el IDE web actual."
---

# Ejemplo Julie 01 - Guardar y leer texto

Este ejemplo crea un archivo `.txt`, guarda contenido y luego lo vuelve a leer.

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
