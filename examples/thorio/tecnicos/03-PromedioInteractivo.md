---
runtime: thorio
uses:
  - thorio
ide_web_runnable: false
ide_web_reason: "Usa 'leer' y requiere entrada interactiva, por lo que no es apto para el IDE web actual."
---

# Ejemplo técnico 03 - Promedio interactivo

Este ejemplo calcula un promedio leyendo datos desde la entrada.

Sirve para probar:

- lectura de `decimal`
- operaciones con parentesis
- division
- salida de resultados calculados

```thorio
inicio
  definir nota1 como decimal
  definir nota2 como decimal
  definir nota3 como decimal
  definir promedio como decimal

  leer nota1
  leer nota2
  leer nota3

  promedio = (nota1 + nota2 + nota3) / 3

  mostrar "Promedio final: " + promedio
fin
```
