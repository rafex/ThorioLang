---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Descuento basico

Resta un descuento fijo a un subtotal.

```thorio
inicio
  definir subtotal como decimal
  definir descuento como decimal
  definir total como decimal

  subtotal = 180.0
  descuento = 25.0
  total = subtotal - descuento

  mostrar "Total final: " + total
fin
```
