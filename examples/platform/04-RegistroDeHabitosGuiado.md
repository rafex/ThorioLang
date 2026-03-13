# Registro de habitos guiado

Combina dialogos de `Camile` con escritura de archivos de `Julie`.

```thorio
inicio
  definir nombre como texto
  definir habito como texto
  definir ruta como texto
  definir completado como logico

  nombre = pedir_texto("Como te llamas?")
  habito = pedir_texto("Que habito quieres registrar?")
  completado = confirmar("Completaste " + habito + " hoy?")
  ruta = "examples/platform/sandbox/habitos.md"

  guardar_texto(ruta, "# Habitos del dia\n")
  anexar_texto(ruta, "- Persona: " + nombre + "\n")
  anexar_texto(ruta, "- Habito: " + habito + "\n")
  anexar_texto(ruta, "- Completado: " + completado + "\n")

  mostrar_mensaje("Registro guardado en " + ruta)
fin
```
