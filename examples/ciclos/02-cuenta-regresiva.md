---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Cuenta regresiva

Realiza una cuenta regresiva simple.

```thorio
inicio
  definir contador como entero

  contador = 5

  mientras contador >= 1 hacer
    mostrar contador
    contador = contador - 1
  fin_mientras
fin
```
