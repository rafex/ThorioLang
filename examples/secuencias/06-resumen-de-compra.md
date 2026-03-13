---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Resumen de compra

Suma precios y muestra un total.

```thorio
inicio
  definir pan como decimal
  definir leche como decimal
  definir total como decimal

  pan = 24.5
  leche = 28.0
  total = pan + leche

  mostrar "Total de compra: " + total
fin
```
