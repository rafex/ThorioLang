---
runtime: thorio
uses:
  - thorio
ide_web_runnable: false
ide_web_reason: "Usa 'leer' y requiere entrada interactiva, por lo que no es apto para el IDE web actual."
---

# Seguimiento de habito

Muestra varias repeticiones de un mismo habito.

```thorio
inicio
  definir dia como entero

  dia = 1

  mientras dia <= 7 hacer
    mostrar "Dia " + dia + ": leer 20 minutos"
    dia = dia + 1
  fin_mientras
fin
```
