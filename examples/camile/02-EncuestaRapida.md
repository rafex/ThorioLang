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
