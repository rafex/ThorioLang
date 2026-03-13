---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Ejemplo técnico 01 - Contador acumulado

Este ejemplo recorre una secuencia y acumula un total.

Sirve para probar:

- variables enteras
- suma incremental
- ciclo `mientras`
- salida intermedia y final

```thorio
inicio
  definir contador como entero
  definir suma como entero

  contador = 1
  suma = 0

  mientras contador <= 5 hacer
    suma = suma + contador
    mostrar "Paso " + contador + ": suma = " + suma
    contador = contador + 1
  fin_mientras

  mostrar "Total final: " + suma
fin
```
