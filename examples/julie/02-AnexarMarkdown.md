---
runtime: julie
uses:
  - thorio
  - julie
ide_web_runnable: true
ide_web_reason: "Usa Julie y puede ejecutarse en el entorno temporal del IDE web."
---

# Ejemplo Julie 02 - Anexar sobre Markdown

Este ejemplo crea un archivo `.md`, agrega mas contenido y luego muestra el resultado final.

```thorio
inicio
  definir ruta como texto
  definir creado como texto
  definir actualizado como texto
  definir documento como texto

  ruta = "examples/julie/sandbox/bitacora.md"

  creado = guardar_texto(ruta, "# Bitacora")
  actualizado = anexar_texto(ruta, " - entrada_1")
  documento = leer_texto(ruta)

  mostrar "Archivo base: " + creado
  mostrar "Archivo final: " + actualizado
  mostrar "Documento: " + documento
fin
```
