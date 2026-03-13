---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Ejemplo 02 - Variables y tipos

Ahora introducimos variables y tipos basicos.

En este ejemplo se definen variables de texto, entero y logico.

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

## Que aprende el lector

- declaracion con `definir`
- tipos `texto`, `entero`, `logico`
- asignacion con `=`
- concatenacion con `+`
