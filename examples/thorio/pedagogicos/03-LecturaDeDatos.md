---
runtime: thorio
uses:
  - thorio
ide_web_runnable: false
ide_web_reason: "Usa 'leer' y requiere entrada interactiva, por lo que no es apto para el IDE web actual."
---

# Ejemplo 03 - Lectura de datos

Este ejemplo muestra como leer informacion desde la entrada.

Al ejecutarlo, el programa esperara dos lineas de entrada:

1. el nombre
2. la edad

```thorio
inicio
  definir nombre como texto
  definir edad como entero

  leer nombre
  leer edad

  mostrar "Hola " + nombre
  mostrar "Tu edad es " + edad
fin
```

## Que aprende el lector

- entrada con `leer`
- uso posterior de los datos capturados
