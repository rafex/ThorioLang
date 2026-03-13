---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Area de rectangulo

Calcula un area simple con enteros.

```thorio
inicio
  definir base como entero
  definir altura como entero
  definir area como entero

  base = 8
  altura = 5
  area = base * altura

  mostrar "Area: " + area
fin
```
