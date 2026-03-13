---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Clasificar meta

Devuelve una etiqueta segun el valor recibido.

```thorio
funcion clasificar(porcentaje: decimal) retorna texto
  si porcentaje >= 100 entonces
    retornar "Meta completa"
  si_no
    retornar "Meta en avance"
  fin_si
fin_funcion

inicio
  mostrar clasificar(82.0)
fin
```
