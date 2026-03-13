---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Presentacion personal

Concatena varios textos para formar una presentacion breve.

```thorio
inicio
  definir nombre como texto
  definir ciudad como texto

  nombre = "Lucia"
  ciudad = "Merida"

  mostrar "Hola, soy " + nombre
  mostrar "Vivo en " + ciudad
fin
```
