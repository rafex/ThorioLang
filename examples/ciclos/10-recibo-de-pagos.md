---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Recibo de pagos

Cuenta varios pagos recibidos y calcula el total.

```thorio
inicio
  definir pago como entero
  definir total como decimal

  pago = 1
  total = 0.0

  mientras pago <= 3 hacer
    total = total + 250.0
    mostrar "Pago " + pago + ": " + total
    pago = pago + 1
  fin_mientras
fin
```
