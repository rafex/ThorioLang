---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Variables y tipos

Ejemplo basico para guardar informacion y reutilizarla.

```thorio
inicio
  definir nombre como texto
  definir edad como entero
  definir activo como logico

  nombre = "Ana"
  edad = 12
  activo = verdadero

  mostrar "Nombre: " + nombre
  mostrar "Edad: " + edad
  mostrar "Activo: " + activo
fin
```
