---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Ejemplo técnico 14 - Tabla de multiplicar

Este ejemplo genera la tabla del 7 del 1 al 10.

Sirve para probar:

- bucle simple
- multiplicación
- construcción de salida paso a paso

```thorio
inicio
  definir numero como entero
  definir factor como entero
  definir resultado como entero

  numero = 7
  factor = 1

  mientras factor <= 10 hacer
    resultado = numero * factor
    mostrar numero + " x " + factor + " = " + resultado
    factor = factor + 1
  fin_mientras
fin
```
