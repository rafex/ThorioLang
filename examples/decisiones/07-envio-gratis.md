---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Envio gratis

Determina si aplica un beneficio.

```thorio
inicio
  definir monto como decimal

  monto = 520.0

  si monto >= 500 entonces
    mostrar "Aplica envio gratis"
  si_no
    mostrar "Envio con costo"
  fin_si
fin
```
