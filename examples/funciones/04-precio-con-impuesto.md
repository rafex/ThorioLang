---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Precio con impuesto

Aplica una operacion decimal dentro de una funcion.

```thorio
funcion precio_final(subtotal: decimal, impuesto: decimal) retorna decimal
  retornar subtotal + impuesto
fin_funcion

inicio
  mostrar "Total: " + precio_final(240.0, 38.4)
fin
```
