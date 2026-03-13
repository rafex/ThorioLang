---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Lista de tareas

Declara una lista de texto y la muestra completa.

```thorio
inicio
  definir tareas como lista_texto

  tareas = ["leer", "practicar", "descansar"]

  mostrar "Tareas: " + tareas
  mostrar "Cantidad: " + longitud(tareas)
fin
```
