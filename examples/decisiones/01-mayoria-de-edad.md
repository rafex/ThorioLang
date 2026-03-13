---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Mayoria de edad

Decide si una persona ya es mayor de edad.

```thorio
inicio
  definir edad como entero

  edad = 20

  si edad >= 18 entonces
    mostrar "Es mayor de edad"
  si_no
    mostrar "Aun es menor de edad"
  fin_si
fin
```
