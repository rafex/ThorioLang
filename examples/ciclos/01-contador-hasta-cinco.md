---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Contador hasta cinco

Cuenta del uno al cinco usando mientras.

```thorio
inicio
  definir contador como entero

  contador = 1

  mientras contador <= 5 hacer
    mostrar contador
    contador = contador + 1
  fin_mientras
fin
```
