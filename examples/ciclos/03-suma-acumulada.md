---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Suma acumulada

Suma los primeros numeros naturales.

```thorio
inicio
  definir contador como entero
  definir suma como entero

  contador = 1
  suma = 0

  mientras contador <= 5 hacer
    suma = suma + contador
    contador = contador + 1
  fin_mientras

  mostrar "Suma: " + suma
fin
```
