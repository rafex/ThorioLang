---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Rango de temperatura

Devuelve un texto segun una comparacion.

```thorio
funcion rango(temperatura: decimal) retorna texto
  si temperatura > 30 entonces
    retornar "calida"
  si_no
    retornar "templada"
  fin_si
fin_funcion

inicio
  mostrar "La tarde esta " + rango(27.5)
fin
```
