---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Tabla del dos

Genera una tabla de multiplicar corta.

```thorio
inicio
  definir factor como entero

  factor = 1

  mientras factor <= 5 hacer
    mostrar "2 x " + factor + " = " + (2 * factor)
    factor = factor + 1
  fin_mientras
fin
```
