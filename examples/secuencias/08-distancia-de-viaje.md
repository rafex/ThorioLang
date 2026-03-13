---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Distancia de viaje

Multiplica velocidad por tiempo.

```thorio
inicio
  definir velocidad como entero
  definir horas como entero
  definir distancia como entero

  velocidad = 70
  horas = 4
  distancia = velocidad * horas

  mostrar "Distancia estimada: " + distancia
fin
```
