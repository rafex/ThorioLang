---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Ejemplo 07 - Multiples bloques Thorio

Un archivo Markdown puede tener varios bloques `thorio`.

Eso permite documentar varias ideas en un mismo archivo, pero solo uno puede ser el programa principal cuando existen varios bloques.

En este ejemplo:

- el primer bloque es solo un ejemplo auxiliar
- el segundo bloque marca `main="true"` y es el que debe compilarse

```thorio
inicio
  mostrar "Este bloque explica una idea"
fin
```

Texto libre del capitulo.

```thorio main="true"
inicio
  definir nombre como texto
  nombre = "Lucia"
  mostrar "Programa principal: " + nombre
fin
```

## Que aprende el lector

- uso de varios bloques `thorio`
- seleccion explicita del bloque principal con `main="true"`
