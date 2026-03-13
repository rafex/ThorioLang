---
runtime: camile
uses:
  - thorio
  - camile
ide_web_runnable: false
ide_web_reason: "Usa Camile y requiere dialogos de escritorio, por lo que no es apto para el IDE web."
---

# Hola Camile

Este ejemplo usa primitivas visuales registradas por la extensión Camile.

```thorio
inicio
  definir nombre como texto
  definir continuar como logico

  nombre = pedir_texto("¿Cómo te llamas?")
  mostrar_mensaje("Hola " + nombre)
  continuar = confirmar("¿Quieres continuar?")

  si continuar entonces
    mostrar_mensaje("Seguimos trabajando con Thorio y Camile")
  si_no
    mostrar_mensaje("Hasta luego " + nombre)
  fin_si
fin
```
