---
runtime: thorio
uses:
  - thorio
ide_web_runnable: true
ide_web_reason: "Usa solo el lenguaje base y puede ejecutarse en el IDE web."
---

# Ejemplo técnico 04 - Clasificación por rango

Este ejemplo clasifica una calificación usando decisiones anidadas.

Sirve para probar:

- comparaciones encadenadas
- bloques `si` dentro de otros bloques `si_no`
- rutas de ejecución más largas

```thorio
inicio
  definir nota como entero

  nota = 85

  si nota >= 90 entonces
    mostrar "Nivel excelente"
  si_no
    si nota >= 70 entonces
      mostrar "Nivel aprobado"
    si_no
      mostrar "Nivel en riesgo"
    fin_si
  fin_si
fin
```
