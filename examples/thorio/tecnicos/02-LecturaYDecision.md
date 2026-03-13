---
runtime: thorio
uses:
  - thorio
ide_web_runnable: false
ide_web_reason: "Usa 'leer' y requiere entrada interactiva, por lo que no es apto para el IDE web actual."
---

# Ejemplo técnico 02 - Lectura y decisión

Este ejemplo recibe dos valores y decide cuál es mayor.

Sirve para probar:

- `leer`
- comparaciones
- condicionales
- combinacion de entrada y salida

```thorio
inicio
  definir a como entero
  definir b como entero

  leer a
  leer b

  si a > b entonces
    mostrar "El mayor es a: " + a
  si_no
    mostrar "El mayor es b: " + b
  fin_si
fin
```
