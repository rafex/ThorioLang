---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Actualizar calificacion

Modifica un elemento de una lista numerica.

```thorio
inicio
  definir notas como lista_decimal

  notas = [8.0, 7.5, 9.0]
  notas[1] = 8.5

  mostrar "Notas actualizadas: " + notas
fin
```
