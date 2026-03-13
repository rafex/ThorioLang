---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Ahorro semanal

Acumula un ahorro constante en varias semanas.

```thorio
inicio
  definir semana como entero
  definir ahorro como entero

  semana = 1
  ahorro = 0

  mientras semana <= 4 hacer
    ahorro = ahorro + 100
    mostrar "Semana " + semana + ": " + ahorro
    semana = semana + 1
  fin_mientras
fin
```
