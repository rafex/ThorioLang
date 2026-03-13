---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Revision de stock

Incrementa un contador hasta alcanzar una meta.

```thorio
inicio
  definir cajas como entero

  cajas = 3

  mientras cajas < 8 hacer
    mostrar "Cajas disponibles: " + cajas
    cajas = cajas + 1
  fin_mientras

  mostrar "Meta alcanzada"
fin
```
