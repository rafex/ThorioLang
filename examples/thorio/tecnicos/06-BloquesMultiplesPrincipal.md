---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Ejemplo técnico 06 - Varios bloques con principal explícito

Este archivo explora el alcance de Thorio cuando un Markdown contiene más de un bloque ejecutable.

El primer bloque es un ejemplo auxiliar y el segundo es el programa principal.

```thorio
inicio
  mostrar "Snippet auxiliar"
fin
```

Texto libre que explica el algoritmo principal.

```thorio main="true" role="demo"
inicio
  definir base como entero
  definir altura como entero
  definir area como entero

  base = 8
  altura = 4
  area = base * altura

  mostrar "Area del rectangulo: " + area
fin
```
