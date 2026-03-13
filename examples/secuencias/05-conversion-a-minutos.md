---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Conversion a minutos

Transforma horas a minutos con una multiplicacion.

```thorio
inicio
  definir horas como entero
  definir minutos como entero

  horas = 3
  minutos = horas * 60

  mostrar "Minutos: " + minutos
fin
```
