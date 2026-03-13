---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Ejemplo 06 - Calculo simple

Este ejemplo combina variables, operaciones y salida.

Calcula el promedio de dos numeros.

```thorio
inicio
  definir nota1 como decimal
  definir nota2 como decimal
  definir promedio como decimal

  nota1 = 8.5
  nota2 = 9.0
  promedio = (nota1 + nota2) / 2

  mostrar "Promedio: " + promedio
fin
```

## Que aprende el lector

- numeros decimales
- uso de parentesis
- operadores aritmeticos
