---
runtime: camile
uses:
  - thorio
  - camile
ide_web_runnable: false
ide_web_reason: "Usa Camile y requiere dialogos de escritorio, por lo que no es apto para el IDE web."
---

# Calculadora narrada

Muestra calculos del lenguaje base dentro de una experiencia visual.

```thorio
funcion total_con_descuento(subtotal: decimal, descuento: decimal) retorna decimal
  retornar subtotal - descuento
fin_funcion

inicio
  definir subtotal como decimal
  definir descuento como decimal
  definir total como decimal

  subtotal = 249.5
  descuento = 49.5
  total = total_con_descuento(subtotal, descuento)

  mostrar_mensaje("Subtotal: " + subtotal)
  mostrar_mensaje("Descuento aplicado: " + descuento)
  mostrar_mensaje("Total final: " + total)
fin
```
