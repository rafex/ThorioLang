---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Ejemplo 05 - Ciclo mientras

Los ciclos sirven para repetir instrucciones.

En este caso mostramos los numeros del 1 al 5.

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

## Que aprende el lector

- repeticion con `mientras`
- actualizacion de variables dentro del ciclo
- condicion de parada
