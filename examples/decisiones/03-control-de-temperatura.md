---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Control de temperatura

Evalua si la temperatura es alta o moderada.

```thorio
inicio
  definir temperatura como decimal

  temperatura = 31.5

  si temperatura > 30 entonces
    mostrar "Temperatura alta"
  si_no
    mostrar "Temperatura moderada"
  fin_si
fin
```
