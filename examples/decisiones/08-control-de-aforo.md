---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Control de aforo

Compara asistentes contra capacidad.

```thorio
inicio
  definir asistentes como entero
  definir capacidad como entero

  asistentes = 34
  capacidad = 30

  si asistentes > capacidad entonces
    mostrar "Aforo excedido"
  si_no
    mostrar "Aforo disponible"
  fin_si
fin
```
