---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Acceso a biblioteca

Usa una bandera logica en una decision.

```thorio
inicio
  definir membresia como logico

  membresia = verdadero

  si membresia == verdadero entonces
    mostrar "Acceso permitido"
  si_no
    mostrar "Acceso denegado"
  fin_si
fin
```
