---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Control de pasos

Acumula pasos caminados con un ciclo.

```thorio
inicio
  definir tramo como entero
  definir pasos como entero

  tramo = 1
  pasos = 0

  mientras tramo <= 3 hacer
    pasos = pasos + 1500
    mostrar "Tramo " + tramo + ": " + pasos
    tramo = tramo + 1
  fin_mientras
fin
```
