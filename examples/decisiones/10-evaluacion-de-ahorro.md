---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Evaluacion de ahorro

Compara dos cantidades y muestra un mensaje final.

```thorio
inicio
  definir ahorro como decimal
  definir meta como decimal

  ahorro = 1250.0
  meta = 1000.0

  si ahorro >= meta entonces
    mostrar "Meta alcanzada"
  si_no
    mostrar "Meta en proceso"
  fin_si
fin
```
