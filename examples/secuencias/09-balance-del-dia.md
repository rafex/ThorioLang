---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Balance del dia

Combina ingresos y gastos en una resta.

```thorio
inicio
  definir ingresos como decimal
  definir gastos como decimal
  definir balance como decimal

  ingresos = 950.0
  gastos = 640.0
  balance = ingresos - gastos

  mostrar "Balance del dia: " + balance
fin
```
