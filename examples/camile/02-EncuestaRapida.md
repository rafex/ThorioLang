---
runtime: camile
uses:
  - thorio
  - camile
ide_web_runnable: false
ide_web_reason: "Usa Camile y requiere dialogos de escritorio, por lo que no es apto para el IDE web."
---

# Encuesta rapida

Ejemplo inicial de `Camile` con preguntas, confirmacion y mensajes.

```thorio
inicio
  definir nombre como texto
  definir objetivo como texto
  definir continuar como logico

  nombre = pedir_texto("Como te llamas?")
  objetivo = pedir_texto("Que quieres practicar hoy?")
  continuar = confirmar("Quieres iniciar una sesion para " + objetivo + "?")

  si continuar entonces
    mostrar_mensaje("Hola " + nombre)
    mostrar_mensaje("Perfecto, hoy trabajaremos: " + objetivo)
  si_no
    mostrar_mensaje("Sin problema. Puedes volver cuando quieras.")
  fin_si
fin
```
