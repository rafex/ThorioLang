---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Promedio de tres notas

Usa decimales para calcular un promedio sencillo.

```thorio
inicio
  definir nota1 como decimal
  definir nota2 como decimal
  definir nota3 como decimal
  definir promedio como decimal

  nota1 = 8.5
  nota2 = 9.0
  nota3 = 7.5
  promedio = (nota1 + nota2 + nota3) / 3

  mostrar "Promedio: " + promedio
fin
```
