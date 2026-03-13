---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Segundo producto

Accede por indice a una lista de texto.

```thorio
inicio
  definir productos como lista_texto

  productos = ["Cuaderno", "Lapiz", "Regla"]

  mostrar "Segundo producto: " + productos[1]
fin
```
