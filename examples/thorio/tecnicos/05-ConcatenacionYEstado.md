---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Ejemplo técnico 05 - Concatenación y estado lógico

Este ejemplo combina texto, enteros y valores lógicos.

Sirve para probar:

- coerción a texto en `mostrar`
- concatenación de distintos tipos
- valor `logico`

```thorio
inicio
  definir usuario como texto
  definir intentos como entero
  definir bloqueado como logico

  usuario = "rafa"
  intentos = 3
  bloqueado = verdadero

  mostrar "Usuario: " + usuario
  mostrar "Intentos: " + intentos
  mostrar "Bloqueado: " + bloqueado
fin
```
