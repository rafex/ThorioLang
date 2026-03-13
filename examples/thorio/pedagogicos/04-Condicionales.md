---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Ejemplo 04 - Condicionales

Las condiciones permiten tomar decisiones.

Aqui preguntamos si una persona puede votar.

```thorio
inicio
  definir edad como entero

  edad = 20

  si edad >= 18 entonces
    mostrar "Puede votar"
  si_no
    mostrar "Aun no puede votar"
  fin_si
fin
```

## Que aprende el lector

- comparacion con `>=`
- estructura `si`, `si_no`, `fin_si`
- caminos alternativos de ejecucion
