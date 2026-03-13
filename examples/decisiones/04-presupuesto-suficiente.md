---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Presupuesto suficiente

Compara el costo contra un presupuesto.

```thorio
inicio
  definir costo como decimal
  definir presupuesto como decimal

  costo = 145.0
  presupuesto = 160.0

  si costo <= presupuesto entonces
    mostrar "Compra posible"
  si_no
    mostrar "Falta presupuesto"
  fin_si
fin
```
