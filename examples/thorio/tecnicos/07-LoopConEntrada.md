---
runtime: thorio
uses:
  - thorio
ide_web_runnable: false
ide_web_reason: "Usa 'leer' y requiere entrada interactiva, por lo que no es apto para el IDE web actual."
---

# Ejemplo técnico 07 - Bucle con entrada inicial

Este ejemplo toma un valor inicial desde la entrada y luego lo incrementa en un ciclo.

Sirve para probar:

- `leer` seguido de `mientras`
- estado mutable
- salida repetida

```thorio
inicio
  definir contador como entero

  leer contador

  mientras contador <= 3 hacer
    mostrar "Valor actual: " + contador
    contador = contador + 1
  fin_mientras
fin
```
