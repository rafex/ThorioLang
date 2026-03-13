---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Ejemplo técnico 08 - Expresiones combinadas

Este ejemplo fuerza varias operaciones en una sola expresión.

Sirve para probar:

- precedencia aritmética
- uso de parentesis
- mezcla de multiplicación, suma y resta

```thorio
inicio
  definir resultado como decimal

  resultado = ((10 + 5) * 2 - 4) / 3

  mostrar "Resultado: " + resultado
fin
```
