---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Nivel de prioridad

Clasifica una tarea por urgencia.

```thorio
inicio
  definir urgencia como entero

  urgencia = 9

  si urgencia >= 8 entonces
    mostrar "Prioridad alta"
  si_no
    mostrar "Prioridad normal"
  fin_si
fin
```
