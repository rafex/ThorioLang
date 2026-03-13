---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Aprobado o pendiente

Clasifica un resultado escolar.

```thorio
inicio
  definir calificacion como decimal

  calificacion = 7.8

  si calificacion >= 6 entonces
    mostrar "Aprobado"
  si_no
    mostrar "Pendiente"
  fin_si
fin
```
