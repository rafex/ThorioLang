---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Area de triangulo

Calcula un resultado dentro de una funcion.

```thorio
funcion area_triangulo(base: decimal, altura: decimal) retorna decimal
  retornar (base * altura) / 2
fin_funcion

inicio
  mostrar "Area: " + area_triangulo(8.0, 5.0)
fin
```
