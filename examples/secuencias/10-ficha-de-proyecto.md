---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Ficha de proyecto

Muestra varias lineas de un proyecto corto.

```thorio
inicio
  definir proyecto como texto
  definir estado como texto

  proyecto = "Catalogo de ejemplos"
  estado = "en progreso"

  mostrar "Proyecto: " + proyecto
  mostrar "Estado: " + estado
fin
```
