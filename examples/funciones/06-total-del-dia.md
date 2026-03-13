---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Total del dia

Combina varias operaciones en una sola funcion.

```thorio
funcion balance(ingresos: decimal, gastos: decimal) retorna decimal
  retornar ingresos - gastos
fin_funcion

inicio
  mostrar "Balance: " + balance(1200.0, 845.5)
fin
```
