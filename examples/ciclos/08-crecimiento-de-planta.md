---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Crecimiento de planta

Acumula una altura diaria.

```thorio
inicio
  definir dia como entero
  definir altura como decimal

  dia = 1
  altura = 12.0

  mientras dia <= 4 hacer
    altura = altura + 1.5
    mostrar "Dia " + dia + ": " + altura
    dia = dia + 1
  fin_mientras
fin
```
